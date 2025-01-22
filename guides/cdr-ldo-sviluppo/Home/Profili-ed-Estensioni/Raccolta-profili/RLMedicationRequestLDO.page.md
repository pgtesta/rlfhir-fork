# RLMedicationRequestLDO

- [RLMedicationRequestLDO](#RLMedicationRequestLDO)
  - [Descrizione](#descrizione)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Il profilo RLMedicationRequestLDO è stato strutturato a partire dalla risorsa generica FHIR [MedicationRequest](https://hl7.org/fhir/r4/medicationrequest.html), il profilo è volto a descrivere il contenuto informativo delle prescrizioni farmaceutiche prodotte durante il ricovero.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
<br>
</div>


## Search parameter

Attualmente non sono definiti Search Parameters.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set relativi al profilo RLMedicationRequestLDO:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| ATC | Codice e descrizione del farmaco per ATC |La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/Valueset/DDC-FarmacoATC}} |
| AIC | Codice e descrizione del farmaco per AIC |La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/Valueset/DDC-FarmacoAIC}} |
| GE | Codice e descrizione del farmaco per GE |La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/Valueset/DDC-FarmacoGE}} |