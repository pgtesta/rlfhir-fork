# RLProvenanceDocumentoCDA2

- [RLProvenanceDocumentoCDA2](#RLProvenanceDocumentoCDA2)
  - [Descrizione](#descrizione)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione

Il profilo RLProvenanceDocumentoCDA2 è stato strutturato a partire dalla risorsa generica FHIR [Provenance](http://hl7.org/fhir/R4/provenance.html) per contenere la descrizione delle informazioni della provenienza delle risorse FHIR richieste per il caso d'uso regionale.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProvenanceLDO, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProvenanceLDO, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProvenanceLDO, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProvenanceLDO, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProvenanceLDO, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProvenanceLDO, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>

<br>
</div>


## Search parameter



<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLProvenanceDocumentoCDA2:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| agent.type | Tipo di attore che aggiunge informazioni di contesto sull'osservazione | La codifica è definita dal ValueSet {{link:http://hl7.org/fhir/ValueSet/provenance-agent-type}} |
