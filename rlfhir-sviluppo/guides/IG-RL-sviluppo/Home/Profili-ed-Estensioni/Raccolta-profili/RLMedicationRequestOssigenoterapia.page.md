# RLMedicationRequestOssigenoterapia

- [RLMedicationRequestOssigenoterapia](#rlmedicationrequestossigenoterapia)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione

Il profilo RLMedicationRequestOssigenoterapia è stato strutturato a partire dalla risorsa generica FHIR [MedicationRequest](http://hl7.org/fhir/R4/medicationrequest.html) e riporta le informazioni riguardo l’ossigenoterapia prescritta ad un cittadino in fase di redazione del progetto individuale.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestOssigenoterapia}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestOssigenoterapia, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestOssigenoterapia, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestOssigenoterapia, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestOssigenoterapia, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestOssigenoterapia, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestOssigenoterapia, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-MedicationRequest-Ossigenoterapia}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa MedicationRequest.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLMedicationRequestOssigenoterapia:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| medicationCodeableConcept | Codice e descrizione dell’ossigenoterapia da attivare |  La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaOssigeno}}|
