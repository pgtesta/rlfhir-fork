# RLMeasureReportPLO

- [RLMeasureReportPLO](#rlmeasurereportplo)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [1. Totale posti letto occupati per L2](#1-totale-posti-letto-occupati-per-l2)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [MeasureReport](http://hl7.org/fhir/R4/measurereport.html) per contenere le informazioni relative al report della misura del totale dei posti letto occupati per reparto e per struttura ospedaliera.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:MeasureReport/esempio-measureReport-PLO}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

###	1. Totale posti letto occupati per L2

Questa ricerca ha lo scopo di ottenere il totale dei posti letto occupati per un determinato L2.

I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	reporter:Organization.identifier: codice L2 dell'ente di riferimento

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

|     SCOPE    | Totale PLO |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | MeasureReport?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO<br>&MeasureReport?reporter:Organization.identifier={codiceL2} |

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/MeasureReport?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO&reporter:Organization.identifier=016235



<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Location.


<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Attualmente non sono definiti value set specifici per il profilo RLMeasureReportPLO.
