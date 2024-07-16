# RLObservationLabReport

- [RLObservationLabReport](#RLObservationLabReport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione

<<<<<<< HEAD
Il profilo RLObservationLabReport è stato strutturato a partire dalla risorsa generica FHIR [Observation](http://hl7.org/fhir/R4/observation.html) per descrivere vincoli aggiuntivi per Observation Lab Report.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{ http://hl7.it/fhir/lab-report/StructureDefinition/observation-doc-it-lab }}.
=======
Il profilo RLObservationLabReport è stato strutturato a partire dalla risorsa generica FHIR [Observation](http://hl7.org/fhir/R4/observation.html) per descrivere le rilevazioni cliniche.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab}}.
>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532

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
<<<<<<< HEAD
{{tree: http://hl7.it/fhir/lab-report/StructureDefinition/observation-doc-it-lab , snapshot}}
=======
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab, snapshot}}
>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
<<<<<<< HEAD
{{tree: http://hl7.it/fhir/lab-report/StructureDefinition/observation-doc-it-lab , diff}}
=======
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab, diff}}
>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
<<<<<<< HEAD
{{tree: http://hl7.it/fhir/lab-report/StructureDefinition/observation-doc-it-lab , hybrid}}
=======
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab, hybrid}}
>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
<<<<<<< HEAD
{{table: http://hl7.it/fhir/lab-report/StructureDefinition/observation-doc-it-lab , snapshot}}
=======
{{table:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab, snapshot}}
>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
<<<<<<< HEAD
{{xml: http://hl7.it/fhir/lab-report/StructureDefinition/observation-doc-it-lab , snapshot}}
=======
{{xml:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab, snapshot}}
>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
<<<<<<< HEAD
{{json: http://hl7.it/fhir/lab-report/StructureDefinition/observation-doc-it-lab , snapshot}}
=======
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab, snapshot}}
>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
<<<<<<< HEAD
Al momento non ci sono esempi disponibili.
=======

>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

<<<<<<< HEAD
Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Patient.

<!-- ===================================================FINE SEZIONE=================================================== -->


## ValueSet
Nella seguente tabella sono elencati i value set relativi al profilo RLObservationDocumentLabReport

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| observation status | Codici di stato per la risorsa Observation Document - Lab Report | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/valueset-status-obs-it)  |
| risultato osservazione | Risultato dell'observation  | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione)  |
| risultato osservazione codificato | Codeableconcept per la descrizione del risultato dell'observation  | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it)  | 
|observation method | Codice SNOMED per il metodo utilizzato nell'observation | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/observation-methods)  |
=======
Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Observation.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLObservationLabReport:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| ObservationStatus | Codici che forniscono lo stato di un'osservazione. | La codifica è definita dal ValueSet {{link:http://hl7.org/fhir/ValueSet/observation-status}} |
| Tipo osservazione | Valueset contente i codici che identificano il tipo di osservazione nel referto di laboratorio.  | La codifica è definita dal ValueSet {{link:http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione}} |
| Risultato osservazione codificato | Valueset contenente i codici per la risorsa Observation - Lab Report per la descrizione del risultato della rilevazione. | La codifica è definita dal ValueSet {{link:http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it}} |
| ObservationMethods | Codici del metodo di osservazione | La codifica è definita dal ValueSet {{link:http://hl7.org/fhir/ValueSet/observation-methods}} |


>>>>>>> ab92391df709b21071f4d736ec6a335b7d208532
