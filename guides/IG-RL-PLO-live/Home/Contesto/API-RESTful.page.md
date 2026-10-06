# {{page-title}}

## Endpoint FHIR

### API Manager
L'API Manager espone i servizi FHIR definiti nell'ecosistema di Regione Lombardia. 
Il base_url con cui accedere a tali servizi è il seguente:
        
        <base_API_Manager> = https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri

L'elenco delle API esposte è:

|Metodo HTTP|URL|Detentore del dato|
|---|---|---|
|GET|<base_API_Manager>/_Organization_|DDC FHIR Server|
|GET|<base_API_Manager>/_Location_|NPRI FHIR Server|

### API Enti erogatori
I servizi FHIR esposti dai Sistemi Informativi degli Enti Erogatori sono accessibili attraverso i canali protetti tra ARIAspa e gli Enti stessi.
Il base_url con cui accedere a tali servizi è il seguente:

        <base_API_Ente> = https://<nome_host_Ente>/<contesto_FHIR>/<codice_Cudes_L1>/v1.0.0/<tipologia_servizio_sociosanitario>

dove:
- <nome_host_Ente>: alias corrispondente all’indirizzo IP dell’Ente definito sul canale protetto; la risoluzione dell’alias è inserita nel DNS di ARIAspa
- <contesto_FHIR>: fhir per la Produzione reale; fhirtest per la Produzione virtuale, da utilizzare per i test delle integrazioni propedeutici all’avvio in produzione
- <codice_Cudes_L1>: codice L1 dell’Ente Erogatore, al quale è collegato il canale protetto
- <tipologia_servizio_sociosanitario>: nome della tipologia del servizio sociosanitario offerto dall'erogatore, ad esempio _erogazione-adi_.

L'elenco delle API esposte è:

|Metodo HTTP|URL|Detentore del dato|
|---|---|---|
|POST|<base_API_Ente>/_Bundle_|Ente Erogatore|
|GET|<base_API_Ente>/_Location_|Ente Erogatore|

## Header 
Le chiamate HTTP relative all'integrazione FHIR devono contenere i seguenti header:

|Nome header|Valore|Descrizione|
|---|---|---|
|Content-Type|application/fhir+json|mime type del formato di scambio|
|Authorization | Bearer \<valore\> | \<valore\>: rappresenta il valore dell’Access Token ottenuto in precedenza invocando i servizi di autenticazione di API Manager |


