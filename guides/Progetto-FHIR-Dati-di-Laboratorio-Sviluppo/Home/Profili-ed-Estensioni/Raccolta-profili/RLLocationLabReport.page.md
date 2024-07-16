# RLLocationLabReport

- [RLLocationLabReport](#RLLocationLabReport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Location](http://hl7.org/fhir/R4/location.html) volto a contenere le informazioni relative all'edificio di una struttura ospedaliera.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:http://hl7.it/fhir/lab-report/StructureDefinition/location-it-lab}}.

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

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Location.


<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet


Nella seguente tabella sono elencati i value set relativi al profilo RLLocationLabReport:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| language | Lingua utilizzata per descrivere la risorsa  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/languages)  |
| location status | Stato della location | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/location-status|4.0.1)  |
| bed status | Codice per specificare lo stato del letto per l'ingresso del paziente, usato anche per determinare se il paziente può essere assegnato o meno al letto| La codifica è definita dal Valueset (http://terminology.hl7.org/ValueSet/v2-0116)  |
| location mode| Indica se la risorsa rappresenta una location specifica o una classe di location | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/location-mode|4.0.1)  |
|days of week| Giorni della settimana | La codifica è definita dal Valueset (
http://hl7.org/fhir/ValueSet/days-of-week|4.0.1)  |
|service deliveery location role type| Il ruolo che identifica le caratteristiche in cui viene eseguito il servizio| La codifica è definita dal Valueset (
http://terminology.hl7.org/ValueSet/v3-ServiceDeliveryLocationRoleType)  |

