# RLCompositionLabReport

- [RLCompositionLabReport](#RLCompositionLabReport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [1. Progetti individuali attivi](#1-progetti-individuali-attivi)
    - [2. Progetti individuali di un paziente](#2-progetti-individuali-di-un-paziente)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Il profilo RLCompositionLabReport è stato strutturato a partire dalla risorsa generica FHIR [Composition](https://hl7.org/fhir/r4/composition.html), il profilo è volto a descrivere il referto di laboratorio.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:http://hl7.it/fhir/lab-report/StructureDefinition/composition-it-lab}}.

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
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/composition-it-lab, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/composition-it-lab, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/composition-it-lab, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:http://hl7.it/fhir/lab-report/StructureDefinition/composition-it-lab, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:http://hl7.it/fhir/lab-report/StructureDefinition/composition-it-lab, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/composition-it-lab, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca




<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter


<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set relativi al profilo RLCompositionLabReport:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| confidentiality | Codice di confidenzialità della composition | La codifica è definita dal Valueset [Confidentiality] (https://terminology.hl7.org/5.3.0/ValueSet-v3-Confidentiality.html)  |
| sezione referto laboratorio| Valueset contenente i codici LOINC per la specialità di laboratorio | La codifica è definita dal Valueset (https://www.hl7.it/fhir/lab-report/0.2.0/ValueSet-sezione-referto-laboratorio.html)  |
| language | Lingua utilizzata per descrivere la risorsa  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/languages)  |
| composition status | Stato della composition  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/composition-status|4.0.1)  |
| lab report type | Tipo di report di laboratorio | La codifica è definita dal Valueset (http://hl7.eu/fhir/laboratory/ValueSet/lab-reportType-eu-lab)  |
| document classcodes| Tipo di documento - ad alto livello | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/document-classcodes)  |
|lab study type| tipo di studio di laboratorio (????) | La codifica è definita dal Valueset (http://hl7.eu/fhir/laboratory/ValueSet/lab-studyType-eu-lab)  |
|lab specialty type| specialità di laboratorio (??) | La codifica è definita dal Valueset (http://hl7.eu/fhir/laboratory/ValueSet/lab-specialty-eu-lab)  |
|confidentiality| confidenzialità della composition  | La codifica è definita dal Valueset (http://terminology.hl7.org/ValueSet/v3-Confidentiality)  |
|composition attestation mode| modo in cui una persona ha autenticato la composition| La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/composition-attestation-mode|4.0.1)  |
|doc section codes| document section codes (???)| La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/doc-section-codes)  |
|sezione referto laboratorio| codici LOINC per la specialità di laboratorio| La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/sezione-referto-laboratorio)  |

<br> 
