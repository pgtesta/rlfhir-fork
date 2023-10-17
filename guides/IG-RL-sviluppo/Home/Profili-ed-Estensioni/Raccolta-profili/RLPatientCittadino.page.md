# RLPatientCittadino

- [RLPatientCittadino](#rlpatientcittadino)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione

Il profilo RLPatientCittadino è stato strutturato a partire dalla risorsa generica FHIR [Patient](http://hl7.org/fhir/R4/patient.html) e riporta i dettagli anagrafici di un cittadino.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Al momento non ci sono esempi disponibili.
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca
Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- identifier

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set relativi al profilo RLPatientCittadino:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| maritalStatus | Stato civile del cittadino | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-StatoCivile}} |
| titoloDiStudio | Titolo di studio del cittadino | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TitoloStudio}} |
| posizioneDellaProfessione | Posizione lavorativa del cittadino | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-PosizioneProfessione}} |
| situazionePensionistica | Situazione pensionistica del cittadino | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-SituazionePensionistica}} |
| contact.relationship | Tipologia caregiver | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/TipologiaCaregiver}} |
