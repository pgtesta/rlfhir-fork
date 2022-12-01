# RLServiceRequestSospensioneADI

- [RLServiceRequestSospensioneADI](#rlservicerequestsospensioneadi)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Periodo e causale della sospensione temporanea del ricovero domiciliare e la necessità di effettuare una rivalutazione del paziente](#periodo-e-causale-della-sospensione-temporanea-del-ricovero-domiciliare-e-la-necessità-di-effettuare-una-rivalutazione-del-paziente)
  - [Seacrh parameter](#seacrh-parameter)
  - [Value set](#value-set)


## Descrizione

Profilo declinato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) che descrive i dettagli della sospensione temporanea del ricovero domiciliare di un paziente.

La pagina Simplifier della risorsa è consultabile qui: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, text: qui}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Al momento non ci sono esempi disponibili. 
</div>

<!-- ===================================================FINE SESSIONE=================================================== -->

## Extension

Non sono state sviluppate extension per questo profilo.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Criteri di ricerca

### Periodo e causale della sospensione temporanea del ricovero domiciliare e la necessità di effettuare una rivalutazione del paziente
Parametri di ricerca:
- ...
- ...

L’esito della ricerca permette di recuperare le informazioni relative alla sospensione temporanea del ricovero domiciliare del cittadino.


| SCOPE |     |
|---|---|
| VERB | GET |
| BASE |     |
| URL |     |

<!-- ===================================================FINE SESSIONE=================================================== -->

## Seacrh parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa ServiceRequest.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Value set

Nella seguente tabella sono elencati i value-set relativi al profilo RLServiceRequestSospensioneADI.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| Code | Codice e descrizione del motivo della sospensione temporanea | Il riferimento alla lista esaustiva dei motivi della sospensione temporanea ricavate dal tracciato SIAD 5 è consultabile al seguente {{pagelink:Home/CodeSystem-e-ValueSet/ValueSet.page.md, text:link}} |