# {{page-title}}
- [1. Header](#1.-header)
- [2. Paradigma FHIR RESTful](#2.-Paradigma-FHIR-RESTful)
  - [2.1 EndPoint FHIR](#2.1-Endpoint-FHIR)


- [3. Paradigma FHIR messaging](#3.-Paradigma-FHIR-messaging)
  - [3.1 EndPoint FHIR](#3.1-Endpoint-FHIR)
  

## 1. Header 
Le chiamate HTTP relative all'integrazione FHIR devono contenere i seguenti header:

|Nome header|Valore|Descrizione|
|---|---|---|
|Content-Type|application/fhir+json|mime type del formato di scambio|
|Authorization | Bearer \<valore\> | \<valore\>: rappresenta il valore dell’Access Token ottenuto in precedenza invocando i servizi di autenticazione di API Manager |

Per la descrizione dell'API Manager e i servizi esposti si rimanda ai paragrafi riportati di seguto specifici per paradigma di comunicazione.

## 2. Paradigma FHIR RESTful
Il modello di interoperabilità REST in standard FHIR prevede l’interscambio di informazioni tra un generico “richiedente” (Client) e un generico “espositore” (Server): 

- Il server FHIR espone le Risorse/Profili su specifici punti di accesso (endpoint) raggiungibili con il protocollo https. 
- Il client FHIR può eseguire le chiamate di interesse agli endpoint dove sono presenti le interfacce programmatiche API (Application Programming Interface) che implementano, in modo semplice e snello conforme all’approccio RESTful, i metodi di fruizione dei dati esposti. 

Tale modalità di consultazione dei dati è definita “logica PULL”, e prevede esclusivamente chiamate di tipo GET per consultare i dati esposti. Il risultato di ogni chiamata è la produzione di una risorsa bundle. Questa risorsa ha lo scopo di raccogliere una serie di Risorse/Profili FHR sulla base dei parametri di ricerca utilizzati nella chiamata GET. 

Mentre, l'interazione che permette di creare una nuova risorsa, in una posizione assegnata dal server, avviene tramite una richiesta HTTPs POST.

### 2.1 Endpoint FHIR
#### API Manager
L'API Manager espone i servizi FHIR definiti nell'ecosistema di Regione Lombardia. 
Il base_url con cui accedere a tali servizi è il seguente:
        
        <base_API_Manager> = https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri

L'elenco delle API esposte è:

|Metodo HTTP|URL|Nome profilo|Detentore del dato|
|---|---|---|
|GET|<base_API_Manager>/_CarePlan_|RLCarePlanProgettoIndividuale|SGDT|
|GET|<base_API_Manager>/_QuestionnaireResponse_|RLQuestionnaireResponseValutazione|SGDT|
|GET|<base_API_Manager>/_Organization_|RLOrganizationL1, RLOrganizationL2, RLOrganizationL3 |DDC FHIR Server|
|GET|<base_API_Manager>/_Practitioner_|RLPractitionerMedicoPrescrittore|DDC FHIR Server|
|GET|<base_API_Manager>/_PractitionerRole_|RLPractitionerRoleMedicoPrescrittore|DDC FHIR Server|
|GET|<base_API_Manager>/_Location_|RLLocationPLOLetto|NPRI FHIR Server|
|POST|<base_API_Ente>/_Bundle_|RLBundleNotificaErrori|Ente Erogatore|


#### API Enti erogatori
I servizi FHIR esposti dai Sistemi Informativi degli Enti Erogatori sono accessibili attraverso i canali protetti tra ARIAspa e gli Enti stessi.
Il base_url con cui accedere a tali servizi è il seguente:

        <base_API_Ente> = https://<nome_host_Ente>/<contesto_FHIR>/<codice_Cudes_L1>/v1.0.0/<tipologia_servizio_sociosanitario>

dove:
- <nome_host_Ente>: alias corrispondente all’indirizzo IP dell’Ente definito sul canale protetto; la risoluzione dell’alias è inserita nel DNS di ARIAspa
- <contesto_FHIR>: fhir per la Produzione reale; fhirtest per la Produzione virtuale, da utilizzare per i test delle integrazioni propedeutici all’avvio in produzione
- <codice_Cudes_L1>: codice L1 dell’Ente Erogatore, al quale è collegato il canale protetto
- <tipologia_servizio_sociosanitario>: nome della tipologia del servizio sociosanitario offerto dall'erogatore, ad esempio _erogazione-adi_.

L'elenco delle API esposte è:

|Metodo HTTP|URL|Nome profilo|Detentore del dato|
|---|---|---|
|GET|<base_API_Ente>/_Procedure_|RLProcedurePrestazione|Ente Erogatore|
|GET|<base_API_Ente>/_ServiceRequest_|RLServiceRequestSospensioneADI, RLServiceRequestRivalutazione|Ente Erogatore|
|POST|<base_API_Ente>/_Bundle_|RLBundleNotificaErrori|Ente Erogatore|
|GET|<base_API_Ente>/_Location_|RLLocationPLOLetto|Ente Erogatore|


## 3. Paradigma FHIR messaging
Il paradigma scelto per lo scambio dei dati con SGDT è quello del FHIR messaging. Il paradigma messaging prevede un sender, un receiver, un evento di trigger che innesca la creazione e l’invio di un messaggio, un messaggio di richiesta e uno messaggio di risposta.

Un **messaggio FHIR** è un Bundle con Bundle.type=message, avente come prima risorsa MessageHeader. Tale Risorsa contiene i metadati del messaggio: 

- **EventCoding**: evento che porta all'inizio del flusso (*MessageHeader.eventCoding*);
- **Sender**: applicazione che invia il messaggio (*MessageHeader.source*);
- **Receiver**: applicazione che riceve il messaggio (*MessageHeader.destination*);
- **Message Identifier**: identificativo univoco del messaggio (*MessageHeader.id*);
- **Date/Time**: data e ora di creazione del messaggio (*Bundle.timestamp*).

Un messaggio contiene due identifier obbligatori ed univoci per il mittente, ovvero Bundle.id e MessageHeader.id. Ogni volta che viene inviato lo stesso messaggio il Bundle.id deve cambiare mentre MessageHeader.id rimane invariato.

Quando il destinatario elabora il messaggio, risponderà con:
- un nuovo Bundle, avente un nuovo *Bundle.id*;
- la prima risorsa sarà *MessageHeader* con *source* e *destination* opportuni e un nuovo *MessageHeader.id*
- l'attributo *MessageHeader.response.identifier* sarà valorizzato con il *MessageHeader.id* del messaggio di richiesta.

Il receiver può restituire un codice di stato 200 OK se il messaggio è stato elaborato con successo. Mentre, i codici di errore sono:
- 4xx Richiesta malformata o che non ha soddisfatto i criteri d’autorizzazione viene restituito un documento XML di fault con i dettagli dell’eccezione;
- 5xx  Errore interno del server.

NB: “x” rappresenta una coppia di numeri che identificano in modo più dettagliato la tipologia di errore.

Il dettaglio dell’operazione è riportato nella risorsa OperationOutcome.

### 3.1 Endpoint FHIR
#### API Manager
L'API Manager espone i servizi FHIR di messaggistica definiti nell'ecosistema di Regione Lombardia. 
Il base_url con cui accedere a tali servizi è il seguente:
        
        <base_API_Manager> = https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri/message

L'elenco delle API esposte è:

|Metodo HTTP|URL|Nome profilo|Detentore del dato|
|---|---|---|
|POST|<base_API_Manager>/_$Bundle_|RLBundleMMG|SGDT|