# RLDiagnosticReportLabReport

- [RLDiagnosticReportLabReport](#RLDiagnosticReportLabReport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione

Il profilo RLDiagnosticReportLabReport è stato strutturato a partire dalla risorsa generica FHIR  [Diagnostic Report](https://hl7.org/fhir/R4/diagnosticreport.html) per descrivere le informazioni cliniche per il referto di laboratorio.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:http://hl7.it/fhir/lab-report/StructureDefinition/diagnosticreport-it-lab}}.

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
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/diagnosticreport-it-lab , snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/diagnosticreport-it-lab , diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/diagnosticreport-it-lab , hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:http://hl7.it/fhir/lab-report/StructureDefinition/diagnosticreport-it-lab , snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:http://hl7.it/fhir/lab-report/StructureDefinition/diagnosticreport-it-lab , snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/diagnosticreport-it-lab , snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>

</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Condition.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set relativi al profilo RLDiagnosticReportLabReport:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| report status| Valueset di codici per identificare lo stato del report diagnostico | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/diagnostic-report-status)  |
| lab study type| Tipo di studio di laboratorio| La codifica è definita dal Valueset (http://hl7.eu/fhir/laboratory/ValueSet/lab-studyType-eu-lab)  |
| lab specialty type| Tipo di specialità di laboratorio| La codifica è definita dal Valueset (http://hl7.eu/fhir/laboratory/ValueSet/lab-specialty-eu-lab)  |
| lab report type| Tipo di report di laboratorio| La codifica è definita dal Valueset (http://hl7.eu/fhir/laboratory/ValueSet/lab-reportType-eu-lab)  |



