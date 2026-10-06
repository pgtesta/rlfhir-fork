# RLMessageHeaderMMG

- [RLMessageHeaderMMG](#RLMessageHeaderMMG)
  - [Descrizione](#descrizione)


## Descrizione

Il profilo RLMessageHeaderMMG è stato strutturato a partire dalla risorsa generica FHIR [MessageHeader](https://hl7.org/fhir/R4/messageheader.html) in modo da contenere le informazioni pertinenti al messaggio scambiato tra la Cartella Clinica Elettronica dell’MMG e la piattaforma SGDT.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMessageHeaderMMG}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMessageHeaderMMG, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMessageHeaderMMG, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMessageHeaderMMG, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMessageHeaderMMG, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMessageHeaderMMG, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMessageHeaderMMG, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Risposta negativa: {{link:Examples/Example_RLMessageHeaderMMG_negativa.json}}
<br>
Risposta positiva: {{link:Examples/Example_RLMessageHeaderMMG_positiva.json}}
<br>
Messaggio di richiesta: {{link:Examples/Example_RLMessageHeaderMMG_MMGpicMMG.json}}
<br>
</div>


<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa MessageHeader.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLMessageHeaderMMG:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| eventCoding | Codice e descrizione dell’evento rappresentato dal messaggio | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/message-events/sgdt}} |
