# RLOrganizationL2

- [RLOrganizationL2](#rlorganizationl2)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLOrganizationL2 è stato strutturato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) per contenere le informazioni anagrafiche e di contatto delle strutture identificate attraverso un codice regionale di livello 2 (L2). Sebbene in Regione Lombardia le strutture identificate da un codice L2 siano di varie tipologie, attualmente questo profilo contiene esclusivamente le informazioni degli enti erogatori pubblici o privati accreditati di servizi socioassistenziali. (es. RSA, erogatori di ADI, Centri Diurni Integrati, ecc)

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-RLOrganizationL2}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLOrganizationL2:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| type | Codifica del tipo di presidio L2 | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2}} |
