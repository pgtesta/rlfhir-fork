# RLServiceRequestSospensioneADI

- [RLServiceRequestSospensioneADI](#rlservicerequestsospensioneadi)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [Dettagli della sospensione temporanea del ricovero domiciliare del paziente](#dettagli-della-sospensione-temporanea-del-ricovero-domiciliare-del-paziente)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLServiceRequestSopensioneADI è stato strutturato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) e riporta i dettagli della sospensione temporanea del ricovero domiciliare di un paziente.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI}}.

<br>
<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Hybrid View')">Hybrid View</button>
  <button class="tablinks" onclick="openTab(event, 'Snapshot View')">Snapshot View</button>
  <button class="tablinks" onclick="openTab(event, 'Differential View')">Differential View</button>
  <button class="tablinks" onclick="openTab(event, 'Table View')">Table View</button>
  <button class="tablinks" onclick="openTab(event, 'XML View')">XML View</button>
  <button class="tablinks" onclick="openTab(event, 'JSON View')">JSON View</button>
  <button class="tablinks" onclick="openTab(event, 'Esempi')">Esempi applicati al profilo</button>
</div>

<div id="Snapshot View" class="tabcontent">
  <h3>Snapshot View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:Examples-Example-ServiceRequest-SospensioneADI}}
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

### Dettagli della sospensione temporanea del ricovero domiciliare del paziente 

Questa ricerca deve essere effettuata da un’ASST per ottenere le informazioni riassuntive delle sospensioni temporanee del ricovero domiciliare di un paziente. L’elenco delle sospensioni temporanee è generato a partire dalla data di attivazione del ricovero domiciliare (primo accesso di un operatore a domicilio) ed aggiornato alla data corrente della richiesta. Mediante il numero pratica del servizio di cure domiciliari viene definita l’associazione della prestazione erogata con l’assistito.  

Il parametro da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	requisition: numero pratica del servizio di cure domiciliari.

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Dettagli della sospensione temporanea del ricovero domiciliare del paziente |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | https://\<nome_host_Ente\>/\<contesto_FHIR\>/\<codiceCudesL1\>/\<versione\>/erogazione-adi |
| URL | ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI<br>&requisition=\{_numeroPratica_\}<br>&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=\{_codiceLivello2_\} |

A titolo esemplificativo, la chiamata: 
  
    ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI&requisition=2022000001&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=03014300

restituirà, se presenti, tutte le sospensioni richieste per la pratica numero "2022000001" afferente alla struttura "03014300".

Un esempio di Bundle di risposta può essere consultato qui: {{link:esempio-ricerca-sospensione}}.

Poiché questa ricerca è di prassi utilizzata per ricavare anche i dettagli relativi alla necessità di rivalutazione del paziente, strutturati nel profilo RLServiceRequestRivalutazione, vengono di seguito riportate le informazioni per effettuare la ricerca congiunta.

Il parametro da valorizzare obbligatoriamente per effettuare la ricerca per entrambi i profili interessati (RLServiceRequestSopensioneADI e RLServiceRequestRivalutazione) è:
-	requisition: numero pratica del servizio di cure domiciliari.

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Dettagli della sospensione temporanea del ricovero domiciliare e necessità di rivalutazione del paziente |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | https://\<nome_host_Ente\>/\<contesto_FHIR\>/\<codiceCudesL1\>/\<versione\>/erogazione-adi |
| URL | ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione,<br>https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI<br>&requisition=\{_numeroPratica_\}<br>&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=\{_codiceLivello2_\} |

La chiamata:
  
    ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione,https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI&requisition=2022000001&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=03014300

restituirà, se presenti, tutte le sospensioni temporanee e rivalutazioni relative pratica numero "2022000001" afferente alla struttura "03014300".

Un esempio di Bundle di risposta può essere consultato qui: {{link:esempio-ricerca-rivalutazioni-sospensioni}}.

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.
<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- _profile
- based-on
- requisition

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value-set relativi al profilo RLServiceRequestSospensioneADI.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| Code | Codice e descrizione del motivo della sospensione temporanea | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-MotiviSospensione}} |