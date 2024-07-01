# RLOrganizationL1

- [RLOrganizationL1](#rlorganizationl1)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [Enti attualmente attivi](#enti-attualmente-attivi)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLOrganizationL1 è stato strutturato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html). Contiene le informazioni anagrafiche e di contatto relative agli enti identificati attraverso un codice regionale di livello 1 “L1”, quali ATS, ASST, Enti Erogatori Privati Accreditati, così come Medici di Medicina Generale e Pediatri di Libera Scelta.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
  {{link:esempio-RLOrganizationL1}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter


<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value-set relativi al profilo RLOrganizationL1

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| type    | Codifica della tipologia di Ente (L1) | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL1}}   |