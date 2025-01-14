# RLLocationLabReport

- [RLAllergyIntoleranceLDO](#RLAllergyIntoleranceLDO)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Allergy Intolerance](https://hl7.org/fhir/r4/allergyintolerance.html) volto a contenere le informazioni su allergie, intolleranze e reazioni avverse di un paziente. 
Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:}}.

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
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/location-it-lab, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/location-it-lab, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/location-it-lab, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:http://hl7.it/fhir/lab-report/StructureDefinition/location-it-lab, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:http://hl7.it/fhir/lab-report/StructureDefinition/location-it-lab, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/location-it-lab, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:Location/esempio-Location-PLO-Edificio}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Nella seguente tabella sono elencati i parametri di ricerca utilizzabili per il profilo AllergyIntoleranceLDO.

Allergie attive:
| SCOPE | Recupero, se presenti, delle informazioni sulle allergie o intolleranze attive di un paziente    |
|---|---|
| VERB | GET |
| BASE | tbd    |
| URL | /AllergyIntolerance?clinical-status=active<br>&subject.identifier=\{_identificativo paziente_\}<br>    |


Allergia per categoria:
| SCOPE | Recupero, se presenti, delle allergie ai farmaci di un paziente    |
|---|---|
| VERB | GET |
| BASE | tbd    |
| URL | /AllergyIntolerance?category=medication<br>&subject.identifier=\{_identificativo paziente_\}<br>    |

| SCOPE | Recupero, se presenti, delle allergie ad alimenti di un paziente    |
|---|---|
| VERB | GET |
| BASE | tbd    |
| URL | /AllergyIntolerance?category=food<br>&subject.identifier=\{_identificativo paziente_\}<br>    |

| SCOPE | Recupero, se presenti, delle allergie a fattori ambientali di un paziente    |
|---|---|
| VERB | GET |
| BASE | tbd    |
| URL | /AllergyIntolerance?category=enviroment<br>&subject.identifier=\{_identificativo paziente_\}<br>    |

Ricerca nel tempo:

| SCOPE | Recupero, se presenti, delle allergie in una finestra temporale di un paziente    |
|---|---|
| VERB | GET |
| BASE | tbd    |
| URL | /AllergyIntolerance?<br>last-date=\{_data di fine ricerca_\}<br><br>&subject.identifier=\{_identificativo paziente_\}<br>    |

I parametri di ricerca possono essere utilizzati in modo congiunto per poter filtrare ulteriormente i risultati della ricerca.
<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet


Nella seguente tabella sono elencati i value set relativi al profilo RLAllergyIntoleranceLDO:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| ATC | Codice e descrizione del farmaco per ATC |La codifica è definita dal ValueSet https://fhir.siss.regione.lombardia.it/CodeSystem/DDC-FarmacoATC |
| AIC | Codice e descrizione del farmaco per AIC |La codifica è definita dal ValueSet https://fhir.siss.regione.lombardia.it/CodeSystem/DDC-FarmacoAIC |
| GE | Codice e descrizione del farmaco per GE |La codifica è definita dal ValueSet https://fhir.siss.regione.lombardia.it/CodeSystem/DDC-FarmacoGE |


