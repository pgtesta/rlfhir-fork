# RLServiceRequestRivalutazione

- [RLServiceRequestRivalutazione](#rlservicerequestrivalutazione)
  - [Descrizione](#descrizione)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Dettagli della sospensione temporanea del ricovero domiciliare del paziente aggiornate alla data e ora di richiesta e della necessità di rivalutazione del paziente](#dettagli-della-sospensione-temporanea-del-ricovero-domiciliare-del-paziente-aggiornate-alla-data-e-ora-di-richiesta-e-della-necessità-di-rivalutazione-del-paziente)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione
Profilo declinato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) volto a notificare la necessità di una rivalutazione di un paziente attualmente in ricovero domiciliare.

La pagina Simplifier della risorsa è consultabile qui: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, text: qui}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
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
Al momento non ci sono esempi disponibili. 
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

### Dettagli della sospensione temporanea del ricovero domiciliare del paziente aggiornate alla data e ora di richiesta e della necessità di rivalutazione del paziente

La ricerca contiene il dettaglio delle sospensioni e la necessità di rivalutazione del paziente inerente al periodo che va dalla data di attivazione del ricovero domiciliare (primo accesso di un operatore a domicilio) alla data corrente della richiesta.

L’associazione al paziente è definita tramite il numero pratica del servizio di cure domiciliari.

Questa ricerca viene effettuata nel momento in cui deve essere appurato se un paziente attualmente in ricovero domiciliare necessita di una rivalutazione. 

I parametri da valorizzare per effettuare la ricerca sono:
- profile: tipologia di profilo che potrà assumere i valori di  RLServiceRequestRivalutazione e/o RLServiceRequestSospensioneADI
- requisition: numero pratica del servizio di cure domiciliari.
- basedOn.reference(RLCarePlanProgettoIndividuale).activity.reference(RLServiceRequestServiziSocioSanitari).perfomer.reference(RLOganizationL2).identifier: codice L2 dell’ente assegnato per l’erogazione del servizio di cure domiciliari.

| SCOPE | Ricerca tutti i profili RLServiceRequestRivalutazione relativi ad un cittadino tramite il numero pratica del servizio di cure domiciliari |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | https://<nome_host_Ente>/<contesto_FHIR>/<codiceCudesL1>/<versione>/erogazione-adi |
| URL | ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione&requisition=\{_numeroPratica_\}&basedOn:CarePlan.activity.reference.performer.identifier=\{_codiceLivello2_\} |

A titolo esemplificativo, la chiamate: 
  
    ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione&requisition=000001&basedOn:CarePlan.activity.reference.performer.identifier=03014300

Restituirà, se presenti, tutte le rivalutazioni necessarie alla pratica numero "000001" afferente alla struttura "03014300".

La chiamata:
  
    ServiceRequest?_profile=(https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI OR https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione)&requisition=000001&basedOn:CarePlan.activity.reference.performer.identifier=03014300

Restituirà, se presenti, tutte le sospensioni temporanee e rivalutazioni relative pratica numero "000001" afferente alla struttura "03014300".

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa ServiceRequest.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Attualmente non sono definiti value set specifici per il profilo RLServiceRequestRivalutazione.