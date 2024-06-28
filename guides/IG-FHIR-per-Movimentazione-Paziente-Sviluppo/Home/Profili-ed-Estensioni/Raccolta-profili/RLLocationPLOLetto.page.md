# RLLocationPLOLetto

- [RLLocationPLOLetto](#rllocationploletto)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [1. Ricerca posti letto occupati per identificativo L1](#1-ricerca-posti-letto-occupati-per-identificativo-l1)
    - [2. Ricerca posti letto occupati per identificativo L2](#2-ricerca-posti-letto-occupati-per-identificativo-l2)
    - [3. Ricerca posti letto occupati per identificativo L3 (reparto clinico)](#3-ricerca-posti-letto-occupati-per-identificativo-l3-reparto-clinico)
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
{{link:Location/esempio-Location-PLO-Letto}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

TODO

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

TODO

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLLocationPLOLetto:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| regimeRicovero | Regime di ricovero del paziente | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/RegimeRicovero}} |