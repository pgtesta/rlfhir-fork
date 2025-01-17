# RLObservationLabReport

- [RLObservationLabReport](#RLObservationLabReport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione

Il profilo RLObservationLabReport è stato strutturato a partire dalla risorsa generica FHIR [Observation](http://hl7.org/fhir/R4/observation.html) per descrivere le informazioni cliniche per il referto di laboratorio.

Di seguito è presentato il contenuto del profilo in diversi formati.

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
{{tree: http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab , snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree: http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab , diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree: http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab , hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table: http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab , snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml: http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab , snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab, snapshot}}
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

Sono stati definiti i seguenti parametri di ricerca correlati alla ricerca delle Observation Lab Report:

- *_include=Observation:patient&patient.identifier=[identificativo paziente]*: da valorizzare con l'identificativo del paziente soggetto delle osservazioni, ad esempio il codice fiscale;
- *category=laboratory*: selezione delle osservazioni provenienti da referti di medicina di laboratorio
- *code=[codice esame]*: da valorizzare con il codice LOINC dell'esame di cui si vuole avere l'andamento
- *date=gt[data ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) da cui cominciare la ricerca
- *date=lt[data di ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) finale più recente in cui fare la ricerca

<!-- ===================================================FINE SEZIONE=================================================== -->


## ValueSet
Nella seguente tabella sono elencati i value set relativi al profilo RLObservationDocumentLabReport

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| observation status | Codici di stato per la risorsa Observation Document - Lab Report | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/valueset-status-obs-it)  |
| risultato osservazione | Risultato dell'observation  | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione)  |
| risultato osservazione codificato | Codeableconcept per la descrizione del risultato dell'observation  | La codifica è definita dal Valueset (http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it)  | 
|observation method | Codice SNOMED per il metodo utilizzato nell'observation | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/observation-methods)  |
