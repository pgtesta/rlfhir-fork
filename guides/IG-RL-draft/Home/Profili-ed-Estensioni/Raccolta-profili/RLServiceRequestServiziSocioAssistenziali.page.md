# RLServiceRequestServiziSocioAssistenziali

- [RLServiceRequestServiziSocioAssistenziali](#rlservicerequestservizisocioassistenziali)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione
Il profilo RLServiceRequestServiziSocioAssistenziali è stato strutturato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) e definisce i dettagli relativi all’attivazione di un servizio socioassistenziale per un assistito come previsto dal proprio progetto individuale. Se già noto, all’interno del profilo verrà riportato l’Ente Erogatore della rete territoriale responsabile della presa in carico. 

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Al momento non ci sono esempi disponibili. 
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono stati definiti criteri di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- code
- identifier
- performer
- type

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Nella seguente tabella sono elencati i value-set relativi al profilo RLServiceRequestServiziSocioAssistenziali.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| Code | Codice e descrizione del servizio sociosanitario da attivare | Il riferimento alla codifica esaustiva, definito nella tabella “Codifica della tipologia UdO”, è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}} |
| ReasonCode | Codice e descrizione dei percorsi di cure domiciliari | Il riferimento alla codifica esaustiva, definito nella tabella “Codifica dei percorsi di cure domiciliari”, è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}} |
| causaleDimissione  | Codice e descrizione della causale di dimissione | Il riferimento alla codifica esaustiva, definito nella tabella “Codifica della causale di dimissione di un ricovero domiciliare”, è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}} |
| soggettoProponentePIC | Codice e descrizione del soggetto che ha proposto la presa in carico dell'assistito | Il riferimento alla codifica esaustiva, definito nella tabella “Codifica del soggetto che ha proposto la presa in carico”, è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}} |