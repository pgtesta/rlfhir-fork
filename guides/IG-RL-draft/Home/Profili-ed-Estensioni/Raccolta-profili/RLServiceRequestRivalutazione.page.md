# RLServiceRequestRivalutazione

- [RLServiceRequestRivalutazione](#rlservicerequestrivalutazione)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [Dettagli della necessità di rivalutazione del paziente](#dettagli-della-necessità-di-rivalutazione-del-paziente)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLServiceRequestRivalutazione è stato strutturato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) ed è volto a notificare la necessità di una rivalutazione di un paziente attualmente in ricovero domiciliare.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:Examples-Example-ServiceRequest-Rivalutazione}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

### Dettagli della necessità di rivalutazione del paziente

Questa ricerca deve essere utilizzata da un’ASST nel momento in cui deve essere appurato se un paziente attualmente in ricovero domiciliare necessita di una rivalutazione. Mediante il numero pratica del servizio e cure domiciliari viene definita l’associazione della prestazione erogata con l’assistito.  

Il parametro da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	requisition: numero pratica del servizio di cure domiciliari.

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Dettagli della necessità di rivalutazione del paziente  |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | https://\<nome_host_Ente\>/\<contesto_FHIR\>/\<codiceCudesL1\>/\<versione\>/erogazione-adi |
| URL | ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione<br>&requisition=\{_numeroPratica_\}<br>&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=\{_codiceLivello2_\} |

A titolo esemplificativo, la chiamate: 
  
    ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione&requisition=2022000001&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=03014300

Restituirà, se presenti, tutte le rivalutazioni necessarie alla pratica numero "2022000001" afferente alla struttura "03014300".

Un esempio di Bundle di risposta può essere consultato qui: {{link:esempio-ricerca-rivalutazioni}}.

Poiché questa ricerca è di prassi utilizzata per ricavare anche i dettagli relativi alle sospensioni temporanee dei servizi di cure domiciliari del paziente, strutturati nel profilo RLServiceRequestSopensioneADI, vengono di seguito riportate le informazioni per effettuare la ricerca congiunta.

Il parametro da valorizzare  obbligatoriamente per effettuare la ricerca per entrambi i profili interessati (RLServiceRequestSopensioneADI e RLServiceRequestRivalutazione) è:
-	requisition: numero pratica del servizio di cure domiciliari.

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Dettagli della sospensione temporanea del ricovero domiciliare e necessità di rivalutazione del paziente |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | https://\<nome_host_Ente\>/\<contesto_FHIR\>/\<codiceCudesL1\>/\<versione\>/erogazione-adi |
| URL | ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione,<br>https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI<br>&requisition=\{_numeroPratica_\}<br>&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=\{_codiceLivello2_\}
 |

La chiamata:
  
    ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione,https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI&requisition=2022000001&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=03014300

Restituirà, se presenti, tutte le sospensioni temporanee e rivalutazioni relative pratica numero "2022000001" afferente alla struttura "03014300".

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

Attualmente non sono definiti value set specifici per il profilo RLServiceRequestRivalutazione.