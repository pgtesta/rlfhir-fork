# RLObservationLDO

- [RLObservationLDO](#RLObservationLDO)
  - [Descrizione](#descrizione)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Observation](https://hl7.org/fhir/r4/observation.html) volto a contenere le informazioni sulle rilevazioni cliniche di un paziente. 
Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLDO}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLDO, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLDO, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLDO, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLDO, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLDO, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLDO, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
TBD
<br>
</div>


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter


N.B : ho preso spunto da quella di https://simplifier.net/guide/Regione-Lombardia---FHIR---Occupazione-Posti-Letto/Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationPLOLetto.page.md?version=current 

I parametri di ricerca definiti nel profilo RLAllergyIntoleranceLDO sono definiti nella seguente tabella:

| Nome | Descrizione | Url di esempio | Link Simplifier |
|---|---|---|---|
| code | Parametro di ricerca per recuperare se presenti, le osservazioni con uno specifico codice LOINC  | /MedicationRequest?<br>medication={_codice farmaco_}&subject.identifier=\{_identificativo paziente_\}<br>&_include=_include=MedicationRequest:subject |  |
|date | Parametro di ricerca per recuperare se presenti, le osservazioni in una finestra temporale | /Observation?<br>date=lt\{_limite superiore di ricerca_}&date=gt\{_limite inferiore di ricerca_}&subject.identifier=\{_identificativo paziente_\} |  |


Nella seguente tabella sono elencati i parametri di ricerca utilizzabili per il profilo RLObservationLDO.

Tramite codice LOINC:
| SCOPE | Recupero, se presenti, delle osservazioni con uno specifico codice LOINC    |
|---|---|
| VERB | GET |
| BASE | tbd    |
| URL | /Observation?<br>code=\{_codice loinc_}&subject.identifier=\{_identificativo paziente_\}<br>    |


Ricerca nel tempo:
| SCOPE | Recupero, se presenti, delle osservazioni in una finestra temporale    |
|---|---|
| VERB | GET |
| BASE | tbd    |
| URL | /Observation?<br>date=lt\{_limite superiore di ricerca_}&date=gt\{_limite inferiore di ricerca_}&subject.identifier=\{_identificativo paziente_\}<br>      |

I parametri di ricerca possono essere utilizzati in modo congiunto per poter filtrare ulteriormente i risultati della ricerca.
<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet


Nella seguente tabella sono elencati i value set relativi al profilo RLObservationLDO:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| code | Codice LOINC della rilevazione |La codifica è definita dal ValueSet http://loinc.org |

