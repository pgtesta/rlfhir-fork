# RLEncounterAccesso

- [RLEncounterAccesso](#rlencounteraccesso)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)

## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Encounter](http://hl7.org/fhir/R4/encounter.html) volto a descrivere le informazioni di base dell’accesso alla struttura di prossimità e della tipologia di bisogno di un cittadino.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterAccesso}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterAccesso, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterAccesso, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterAccesso, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterAccesso, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterAccesso, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterAccesso, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-Encounter-Accesso}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Encounter.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLEncounterAccesso:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| TipologiaBisogno | Codice e descrizione della tipologia del bisogno rilevata al cittadino| Il riferimento alla lista esaustiva delle tipologie di bisogni è consultabile al seguente  {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}}   |
| Class | Motivo della segnalazione | Il riferimento alla lista esaustiva dei motivi delle segnalazioni è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}}   |
| Type | Tipologia di accesso | Il riferimento alla lista esaustiva delle tipologie di accesso è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}}   |
| ReasonCode |Motivo della segnalazione e setting assistenziale proposto| Il riferimento alla lista esaustiva dei motivi delle segnalazioni e setting assistenziali proposti è consultabile al seguente  {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}}   |
