# RLPatientCore

- [RLPatientCore](#rlpatientcore)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
TODO 

Il profilo RLPatientCore è stato strutturato a partire dalla risorsa generica FHIR [Patient](http://hl7.org/fhir/R4/patient.html) per contenere le informazioni del paziente cittadino, assistito in Regione Lombardia.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>

<br>
</div>


<!-- ===================================================FINE SEZIONE=================================================== -->


## ValueSet
Nella seguente tabella sono elencati i value set relativi al profilo RLPatientBase:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| extension:luogoNascitaCodeable | Codice ISTAT del comune e/o dello stato di nascita | La codifica è definita dal ValueSet http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali |
| identifier |  Codice Fiscale del paziente | La codifica è definita dal ValueSet http://hl7.it/sid/codiceFiscale |
| identifier |  Codice STP del paziente | La codifica è definita dal ValueSet http://terminology.hl7.it/ValueSet/uri-idStp |
| identifier |  Codice della tessera TEAM del paziente | La codifica è definita dal ValueSet https://fhir.siss.regione.lombardia.it/sid/tesseraTeam |  
| identifier |  Codice ENI del paziente | La codifica è definita dal ValueSet http://terminology.hl7.it/ValueSet/uri-idEni |
| identifier |  Identificativo unico nazionale (ANPR) del paziente | La codifica è definita dal ValueSet http://hl7.it/sid/anpr |
| identifier |  Identificativo unico regionale del paziente | La codifica è definita dal ValueSet http://terminology.hl7.it/ValueSet/uri-idRegionali |
| maritalStatus |  Stato civile del paziente | La codifica è definita dal ValueSet https://www.hl7.it/fhir/base/ValueSet-statoCivile.html |