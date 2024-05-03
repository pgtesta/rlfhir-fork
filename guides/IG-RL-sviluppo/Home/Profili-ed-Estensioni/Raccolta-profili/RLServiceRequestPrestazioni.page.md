# RLServiceRequestPrestazioni

- [RLServiceRequestPrestazioni](#RLServiceRequestPrestazioni)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Il profilo RLServiceRequestPrestazioniè stato strutturato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) e comprende le informazioni riguardanti la richiesta di una prestazione, che può essere, nello specifico,una prestazione specialistica e/o diagnostica, infermieristica o sociale, pianificata all’interno di un progetto individuale di un cittadino. Questo profilo può, inoltre, includere il tipo di intervento educazionale, le rispettive modalità di erogazione e la frequenza di erogazione definiti nel progetto individuale del paziente.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioni}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioni, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioni, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioni, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioni, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioni, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioni, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:Examples-Example-ServiceRequest-PrestazioniSpecialistiche}}
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa ServiceRequest.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value-set relativi al profilo RLServiceRequestPrestazioni.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| category | Codice e descrizione della tipologia di prestazione |La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaPrestazione}} |
| SpecialisticaDiagnostica | Codice e descrizione della prestazione specialistica | Catalogo regionale del SISS |
| Infermieristica| Codice e descrizione della prestazione infermieristica | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/Prestazioni}}|
| PrestazioneSociale| Codice e descrizione della prestazione sociale | *Codifica in fase di definizione|
| InterventoEducazionale | Codice e descrizione dell’intervento educazionale da attivare | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-InterventiEducazionali}} |
| locationCode | Codice e descrizione del canale di comunicazione con il quale verrà erogato l’intervento educazionale | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ModalitaErogazioneIntEdu}} |
