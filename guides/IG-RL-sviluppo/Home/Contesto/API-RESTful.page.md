# {{page-title}}

Endpoints FHIR

Le API RESTful FHIR sono esposte ai seguenti endpoint sul dominio <em>https://api.servizirl.it</em>:

        GET https://api.servizirl.it/c/operatori.siss/[ambitoTBD]/v1.0.0/[servizioTBD]/CarePlan

        GET https://api.servizirl.it/c/operatori.siss/[ambitoTBD]/v1.0.0/[servizioTBD]/QuestionnaireResponse

È necessario passare un header dello scope per permettere a APIManager di gestire l'_AccessToken_.

Nell'header sarà inoltre specificato che le informazioni saranno scambiate in formato json tramite il parametro di chiamata <code>content_type=json</code>.


## SGDT --> Ente:

### SGDT--> NPRI FHIR

<<url_da_definire>>

### NPRI FHIR --> Ente
i servizi FHIR esposti dai Sistemi Informativi degli Enti Erogatori sono accessibili attraverso i canali protetti tra ARIAspa e gli Enti stessi.
Il base_url con cui accedere a tali servizi è il seguente:

        <<url_ente>> = https://<nome_host_Ente>/<contesto_FHIR>/<codiceCudesL1>/v1.0.0/erogazione-adi/<resource_name>

dove:
- _nome\_host\_Ente_ = alias corrispondente all’indirizzo IP dell’Ente definito sul canale protetto; la risoluzione dell’alias è inserita nel DNS di ARIAspa
- _contesto\_FHIR_ = fhir per la Produzione reale; fhirtest per la Produzione virtuale, da utilizzare per i test delle integrazioni propedeutici all’avvio in produzione 
- _codiceCudesL1_ = codice L1 dell’Ente Erogatore, al quale è collegato il canale protetto
- _resource\_name_: _Procedure_ , _ServiceRequest_

## Ente --> SGDT:

### Ente --> NPRI FHIR

 <<url_da_definire>>

### NPRI FHIR --> SGDT [ref. 6.2]
I servizi FHIR esposti da SGDT sono accessibili attraverso il componente API Manager.
Il base_url con cui accedere a tali servizi è il seguente:

        <<url_sgdt>> = https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri/<resource_name> 

resource_name : _CarePlan_, _QuestionnaireResponse_