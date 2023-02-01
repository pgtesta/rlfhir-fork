# RLServiceRequestSospensioneADI

- [RLServiceRequestSospensioneADI](#rlservicerequestsospensioneadi)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [Dettagli della sospensione temporanea del ricovero domiciliare del paziente aggiornate alla data e ora di richiesta e della necessità di rivalutazione del paziente](#dettagli-della-sospensione-temporanea-del-ricovero-domiciliare-del-paziente-aggiornate-alla-data-e-ora-di-richiesta-e-della-necessità-di-rivalutazione-del-paziente)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione
Il profilo RLServiceRequestSopensioneADI è stato strutturato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) e riporta i dettagli della sospensione temporanea del ricovero domiciliare di un paziente.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI}}.

<br>
<div class="tab">
 <button class="tablinks active" onclick="openTab(event, 'Snapshot View')">Snapshot View</button>
  <button class="tablinks" onclick="openTab(event, 'Differential View')">Differential View</button>
  <button class="tablinks" onclick="openTab(event, 'Hybrid View')">Hybrid View</button>
   <button class="tablinks" onclick="openTab(event, 'Table View')">Table View</button>
   <button class="tablinks" onclick="openTab(event, 'XML View')">XML View</button>
  <button class="tablinks" onclick="openTab(event, 'JSON View')">JSON View</button>
  <button class="tablinks" onclick="openTab(event, 'Esempi')">Esempi</button>
</div>

<div id="Snapshot View" class="tabcontent" style="display:block">
  <h3>Snapshot View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
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
Al momento non ci sono esempi disponibili. 
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

### Dettagli della sospensione temporanea del ricovero domiciliare del paziente aggiornate alla data e ora di richiesta e della necessità di rivalutazione del paziente

La ricerca contiene il dettaglio delle sospensioni e la necessità di rivalutazione del paziente inerente al periodo che va dalla data di attivazione del ricovero domiciliare (primo accesso di un operatore a domicilio) alla data corrente della richiesta.

L’associazione al paziente è definita tramite il numero pratica del servizio di cure domiciliari.

Questa ricerca viene effettuata nel momento in cui deve essere appurato se un paziente attualmente in ricovero domiciliare necessita di una rivalutazione. 

I parametri da valorizzare per effettuare la ricerca sono:
- profile: tipologia di profilo che potrà assumere i valori di  RLServiceRequestRivalutazione e/o RLServiceRequestSospensioneADI
- requisition: numero pratica del servizio di cure domiciliari.
- basedOn.reference(RLCarePlanProgettoIndividuale).activity.reference(RLServiceRequestServiziSocioAssistenziali).perfomer.reference(RLOganizationL2).identifier: codice L2 dell’ente assegnato per l’erogazione del servizio di cure domiciliari.

| SCOPE | Ricerca tutti i profili RLServiceRequestRivalutazione relativi ad un cittadino tramite il numero pratica del servizio di cure domiciliari |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | https://<nome_host_Ente>/<contesto_FHIR>/<codiceCudesL1>/<versione>/erogazione-adi |
| URL | ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI&requisition=\{_numeroPratica_\}&basedOn:CarePlan.activity.reference.performer.identifier=\{_codiceLivello2_\} |

A titolo esemplificativo, la chiamata: 
  
    ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI&requisition=000001&basedOn:CarePlan.activity.reference.performer.identifier=03014300

Restituirà, se presenti, tutte le sospensioni richieste per la pratica numero "000001" afferente alla struttura "03014300".

La chiamata:
  
    ServiceRequest?_profile=(https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI OR https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione)&requisition=000001&basedOn:CarePlan.activity.reference.performer.identifier=03014300

Restituirà, se presenti, tutte le sospensioni temporanee e rivalutazioni relative pratica numero "000001" afferente alla struttura "03014300".

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

## Value set

Nella seguente tabella sono elencati i value-set relativi al profilo RLServiceRequestSospensioneADI.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| Code | Codice e descrizione del motivo della sospensione temporanea | Il riferimento alla lista esaustiva dei motivi della sospensione temporanea ricavate dal tracciato SIAD 5 è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}} |