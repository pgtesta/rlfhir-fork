# RLObservationCoreStoriaClinica

- [RLObservationCoreStoriaClinica](#rlobservationcorestoriaclinica)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)


## Descrizione

Il profilo RLObservationCoreStoriaClinica è stato strutturato a partire dalla risorsa generica FHIR [Observation](http://hl7.org/fhir/R4/observation.html) volto a contenere le informazioni relative alla storia clinica del paziente in Regione Lombardia.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreStoriaClinica}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreStoriaClinica, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreStoriaClinica, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreStoriaClinica, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreStoriaClinica, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreStoriaClinica, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreStoriaClinica, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Storia Clinica: {{link: Observation/rl-observation-storiaclinica}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLObservationCoreStoriaClinica.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| valueCodeableConcept |  Criticità Clinica | La codifica è definita dal ValueSet [Criticità Clinica](https://fhir.siss.regione.lombardia.it/ValueSet/CriticitaClinica) |