# RLPractitionerMedicoPrescrittore

- [RLPractitionerMedicoPrescrittore](#rlpractitionermedicoprescrittore)
  - [Descrizione](#descrizione)
  - [Criteri di ricerca](#criteri-di-ricerca)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)

## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Practitioner](http://hl7.org/fhir/R4/practitioner.html) contenente l’anagrafica dei medici prescrittori della Regione Lombardia destinatari di ricettari RUR. Sono descritte le diverse tipologie di medici a cui è data facoltà di prescrivere prestazioni e farmaci dispensati dal SSR. 

In particolare, il file contiene l’elenco dei:
- Medici di Medicina Generale e Pediatri di Libera Scelta, i cui dati anagrafici sono conosciuti dai servizi NAR di Scelta&Revoca.
-	Medici di ATS che operano nelle strutture dell’azienda, come guardia medica, medico incaricato ecc. I dati di questi medici sono recuperabili dei processi di consegna dei ricettari (RUR) ministeriali.
- Medici di Aziende Sanitarie Ospedaliere sia pubbliche che private anch’essi destinatari di ricettari (RUR).

Dato che un medico può lavorare (o lavorava) come prescrittore per più di una struttura, è possibile la presenza di più record relativi allo stesso codice fiscale. 

La pagina Simplifier della risorsa è consultabile qui: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerMedicoPrescrittore, text: qui}}.

<br>
<div class="tab">
 <button class="tablinks active" onclick="openTab(event, 'Snapshot View')">Snapshot View</button>
  <button class="tablinks" onclick="openTab(event, 'Differential View')">Differential View</button>
  <button class="tablinks" onclick="openTab(event, 'Hybrid View')">Hybrid View</button>
   <button class="tablinks" onclick="openTab(event, 'Table View')">Table View</button>
   <button class="tablinks" onclick="openTab(event, 'XML View')">XML View</button>
  <button class="tablinks" onclick="openTab(event, 'JSON View')">JSON View</button>
  <button class="tablinks" onclick="openTab(event, 'Esempi')">Esempi</button>
</div>

<div id="Snapshot View" class="tabcontent" style="display:block">
  <h3>Snapshot View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerMedicoPrescrittore, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerMedicoPrescrittore, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerMedicoPrescrittore, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerMedicoPrescrittore, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerMedicoPrescrittore, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerMedicoPrescrittore, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-Practitioner}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Practitioner.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Attualmente non sono definiti value set specifici per il profilo RLPractitionerMedicoPrescrittore.
