# RLMediaLabReport

- [RLMediaLabReport](#RLMediaLabReport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Media](https://hl7.org/fhir/R4/media.html) per descrivere i contenuti multimediali per il referto di laboratorio.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:http://hl7.it/fhir/lab-report/StructureDefinition/media-it-lab}}.

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
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/media-it-lab, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/media-it-lab, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/media-it-lab, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:http://hl7.it/fhir/lab-report/StructureDefinition/media-it-lab, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:http://hl7.it/fhir/lab-report/StructureDefinition/media-it-lab, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/media-it-lab, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>

<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter


<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLMediaLabReport:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| language | Lingua utilizzata per descrivere la risorsa  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/languages)  |
| event status | Codice che identifica il ciclo di vita dell'evento | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/event-status|4.0.1)  |
| media type | Categoria del media - alto livello | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/media-type)  |
| media modality| Codici usati per informazioni dettagliate sull'immagine (tipo, obiettivo) | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/media-modality)  |
| media view| Codici definiti in SNOMED CT che possono essere usati per registrare le visualizzazioni del media | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/media-view)  |
| resource type| Tipo di risorsa | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/resource-types)  |
| procedure reason|  Codici usati per indicare il motivo di una procedura | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/procedure-reason)  |
| body site| Codici dalla codifica SNOMED afferenti a siti anatomici | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/body-site)  |

