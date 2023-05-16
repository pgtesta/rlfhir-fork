# RLLocationPLOLetto

- [RLLocationPLOLetto](#rllocationploletto)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Location](http://hl7.org/fhir/R4/location.html) volto a contenere le informazioni relative al posto letto occupato.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-Location-PLO-Letto}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard:
- _profile
- type
- operational-status
- organization
- partof
- name
- identifier
- _lastUpdated

I parametri di ricerca del profilo RLLocationPLOLetto, oltre ai campi standard della risorsa Organization, sono definiti nella seguente tabella:

| Nome e   link Simplifier | Descrizione | Espressione |
|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationPhysicalType}} | Parametro di ricerca per la tipologia di Location. | physicalType.coding.code |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationRepartoClinico}} | Parametro di ricerca per il reparto clinico che ha in carico il paziente. | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationRepartoClinico').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationRepartoFisico}} | Parametro di ricerca per il reparto fisico dove il paziente risulta allettato. | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationRepartoFisico').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationAreaDegenza}} | Parametro di ricerca per l'area di degenza dove il paziente risulta allettato. | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationAreaDegenza').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationDataOraAccettazione}} | Parametro di ricerca della data e ora di accettazione del paziente (ingresso in struttura). | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationDataOraAccettazione').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationDataOraDimissionePrevista}} | Parametro di ricerca della data e ora prevista per la dimissione del paziente | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationDataOraDimissionePrevista').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationDimissioneProtetta}} | Parametro di ricerca per ricercare se il posto letto è indicato per una dimissione protetta | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationDimissioneProtetta').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationDataOraOccupazioneLetto}} | Parametro di ricerca della data di occupazione del posto letto | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationDataOraOccupazioneLetto').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationRegimeRicovero}} | Parametro di ricerca relativo al regime di ricovero | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationRegimeRicovero').value.coding.code |

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Attualmente non sono definiti value set specifici per il profilo RLLocationPLOLetto.