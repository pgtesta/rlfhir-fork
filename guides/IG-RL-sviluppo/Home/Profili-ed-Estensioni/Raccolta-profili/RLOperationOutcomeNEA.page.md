# RLOperationOutcomeNEA

- [RLOperationOutcomeNEA](#RLOperationOutcomeNEA)
  - [Descrizione](#descrizione)


## Descrizione

Il profilo RLOperationOutcomeMMG è stato strutturato a partire dalla risorsa standard FHIR [OperationOutcome](http://hl7.org/fhir/R4/operationoutcome.html) per contenere il dettaglio delle informazioni relative all’elaborazione dell’operazione tentata, nello specifico del messaggio scambiato tra l’applicativo di gestione 116117 NEA e la piattaforma SGDT.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOperationOutcomeNEA, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOperationOutcomeNEA, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOperationOutcomeNEA, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOperationOutcomeNEA, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOperationOutcomeNEA, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOperationOutcomeNEA, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
  Risposta positiva: {{link:Examples/Example_RL_OperationOutcomeNEA_Positiva.json}}
  <br>
  Risposta negativa: {{link:Examples/Example_RL_OperationOutcomeNEA_Negativa.json}}
  <br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa OperationOutcome.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLOperationOutcomeNEA:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| issue | Codice dell’esito del messaggio | La codifica è definita dal ValueSet {{link:http://hl7.org/fhir/ValueSet/issue-type}} |
| errore | Codice e descrizione dell’elaborazione terminata in errore del messaggio | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/ErroriMessaggio}} |