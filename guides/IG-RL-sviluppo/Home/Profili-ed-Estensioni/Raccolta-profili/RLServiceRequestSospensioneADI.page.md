# RLServiceRequestSospensioneADI

- [RLServiceRequestSospensioneADI](#rlservicerequestsospensioneadi)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Dettagli della sospensione temporanea del ricovero domiciliare del paziente aggiornate alla data e ora di richiesta](#dettagli-della-sospensione-temporanea-del-ricovero-domiciliare-del-paziente-aggiornate-alla-data-e-ora-di-richiesta)
    - [Dettagli della sospensione temporanea del ricovero domiciliare del paziente aggiornate alla data e ora di richiesta e della necessità di rivalutazione del paziente](#dettagli-della-sospensione-temporanea-del-ricovero-domiciliare-del-paziente-aggiornate-alla-data-e-ora-di-richiesta-e-della-necessità-di-rivalutazione-del-paziente)
  - [Search parameter](#search-parameter)
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

### Dettagli della sospensione temporanea del ricovero domiciliare del paziente aggiornate alla data e ora di richiesta 
Il dettaglio delle sospensioni è inteso come riassuntivo del periodo che va dalla data di attivazione del ricovero domiciliare (primo accesso di un operatore a domicilio) alla data corrente della richiesta. 

L’associazione al paziente è definita tramite il numero pratica del servizio di cure domiciliari.

I parametri da valorizzare per effettuare la ricerca sono:
-	requisition: numero pratica del servizio di cure domiciliari.

L’esito della ricerca permette di recuperare le informazioni relative alle sospensioni temporanee del ricovero domiciliare del cittadino che si sono verificate a partire dalla data di attivazione del ricovero domiciliare.

| SCOPE | Ricerca tutti i profili RLServiceRequestSopensioneADI relativi ad un cittadino tramite il numero pratica del servizio di cure domiciliari.    |
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/\[ambitoTBD\]/v1.0.0/\[servizioTBD\]/\[fhir_resource_name\] |
| URL | ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI&requisition=\{_numeroPratica_\} |

A titolo esemplificativo, la chiamata: 

    ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI&requisition=000001

Restituirà, se presenti, tutte le sospensioni temporanee afferenti alla pratica numero 000001.


### Dettagli della sospensione temporanea del ricovero domiciliare del paziente aggiornate alla data e ora di richiesta e della necessità di rivalutazione del paziente

Questa ricerca permette di reperire il dettaglio delle sospensioni e la necessità di rivalutazione del paziente inerente al periodo che va dalla data di attivazione del ricovero domiciliare (primo accesso di un operatore a domicilio) alla data corrente della richiesta.

L’associazione al paziente è definita tramite il numero pratica del servizio di cure domiciliari.

Il parametro da valorizzare per effettuare la ricerca per entrambi i profili interessati (RLServiceRequestSopensioneADI e RLServiceRequestRivalutazione) è:
-	requisition: numero pratica del servizio di cure domiciliari.

| SCOPE | |
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/\[ambitoTBD\]/v1.0.0/\[servizioTBD\]/\[fhir_resource_name\] |
| URL | ServiceRequest?_profile=(https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI OR https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione)&requisition=\{_numeroPratica_\} |

A titolo esemplificativo, la chiamata: 
  
    ServiceRequest?_profile=(https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI OR https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione)&requisition=000001

Restituirà, se presenti, tutte le sospensioni temporanee e rivalutazioni afferenti alla pratica numero 000001.


<!-- ===================================================FINE SESSIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa ServiceRequest.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Value set

Nella seguente tabella sono elencati i value-set relativi al profilo RLServiceRequestSospensioneADI.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| Code | Codice e descrizione del motivo della sospensione temporanea | Il riferimento alla lista esaustiva dei motivi della sospensione temporanea ricavate dal tracciato SIAD 5 è consultabile al seguente {{pagelink:Home/CodeSystem-e-ValueSet/ValueSet.page.md, text:link}} |