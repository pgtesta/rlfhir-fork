# RLServiceRequestLabReport

- [RLServiceRequestLabReport](#RLServiceRequestLabReport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione

Il profilo RLServiceRequestLabReport è stato strutturato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) per contenere la descrizione delle informazioni della prescrizione per il referto di laboratorio.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:http://hl7.it/fhir/lab-report/StructureDefinition/servicerequest-it-lab}}.

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
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/servicerequest-it-lab, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/servicerequest-it-lab, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/servicerequest-it-lab, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:http://hl7.it/fhir/lab-report/StructureDefinition/servicerequest-it-lab, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:http://hl7.it/fhir/lab-report/StructureDefinition/servicerequest-it-lab, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/servicerequest-it-lab, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>

<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa PractitionerRole.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLServiceRequestLabReport:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| RequestIntent | Codici che indicano il grado di autorità/intenzionalità associato a una richiesta. | La codifica è definita dal ValueSet {{link:http://hl7.org/fhir/ValueSet/request-intent}} |
| RequestPriority | La priorità clinica di un ordine diagnostico. | La codifica è definita dal ValueSet {{link:http://hl7.org/fhir/ValueSet/request-priority}} |
| LabOrderCodes | Codice della richiesta per un esame di Laboratorio. | La codifica è definita dal ValueSet {{link:http://hl7.it/fhir/lab-report/ValueSet/lab-orderCodes-it-lab}} |