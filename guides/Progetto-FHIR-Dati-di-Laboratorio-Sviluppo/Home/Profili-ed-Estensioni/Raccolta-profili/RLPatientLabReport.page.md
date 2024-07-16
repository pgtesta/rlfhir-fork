# RLPatientLabReport

- [RLPatientLabReport](#RLPatientLabReport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione

Il profilo RLPatientLabReport è stato strutturato a partire dalla risorsa generica FHIR [Patient](http://hl7.org/fhir/R4/patient.html) per contenere le informazioni anagrafiche di base di un cittadino.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:http://hl7.it/fhir/lab-report/StructureDefinition/patient-it-lab}}.

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
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/patient-it-lab, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/patient-it-lab, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/patient-it-lab, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:http://hl7.it/fhir/lab-report/StructureDefinition/patient-it-lab, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:http://hl7.it/fhir/lab-report/StructureDefinition/patient-it-lab, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/patient-it-lab, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Al momento non ci sono esempi disponibili.
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Patient.

<!-- ===================================================FINE SEZIONE=================================================== -->


## ValueSet
Nella seguente tabella sono elencati i value set relativi al profilo RLPatientLabReport

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| language | Lingua utilizzata per descrivere la risorsa  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/languages)  |
| istat - luogo di nascita | Codice Istat comune - stato di nascita | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/istat-luogoNascita)  |
| istat - cittadinanza | Codice Istat per la cittadinanza | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/istat-cittadinanza)  |
| istat - professione | Codice Istat per la professione | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/istat-professione)  |
| istat - titolo di studio | Codice Istat per indicare il titolo di studio | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/istat-titoloStudio)  |
|tipo identificatore | Codice che descrive i diversi tipi di identificatori | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/VstipoIdentificatore)  |
|anagrafi regionali | Anagrafi regionali | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/vs-anagrafi-regionali)  |
|uri - idEni | Identificativi per codici ENI regionali | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/uri-idEni)  |
|uri - idStp | Identificativi per codici STP regionali  | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/URI-idStp)  |
