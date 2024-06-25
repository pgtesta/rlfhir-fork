# RLLocationPLOLetto

- [RLLocationPLOLetto](#rllocationploletto)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [1. Ricerca posti letto occupati per identificativo L1](#1-ricerca-posti-letto-occupati-per-identificativo-l1)
    - [2. Ricerca posti letto occupati per identificativo L2](#2-ricerca-posti-letto-occupati-per-identificativo-l2)
    - [3. Ricerca posti letto occupati per identificativo L3 (reparto clinico)](#3-ricerca-posti-letto-occupati-per-identificativo-l3-reparto-clinico)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Location](http://hl7.org/fhir/R4/location.html) volto a contenere le informazioni relative al posto letto occupato.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:Location/esempio-Location-PLO-Letto}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

###	1. Ricerca posti letto occupati per identificativo L1

I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	operational-status: da compilare con il valore “O” per indicare che il posto letto è occupato
-	organization.partof:Organization.identifier: codice L1 dell'ente di riferimento

Inoltre, è possibile valorizzare il seguente parametro:
-	lastUpdated: data e ora dell’ultimo aggiornamento dei dati

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

|     SCOPE    | Progetti individuali attivi |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | Location?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto<br>&operational-status=O<br>&organization.partof:Organization.identifier=030703<br>&_include=Location:organization<br>&_include:iterate=Location:partof|

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Location?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto&operational-status=O&organization.partof:Organization.identifier=030703&_include=Location:organization&_include:iterate=Location:partof

Il risultato della precedente GET è un Bundle che contiene tutte le Location identificate dal profilo RLLocationPLOLetto, con lo stato del letto "occupato", afferenti ad un determinato codice L1.
Il Bundle conterrà anche le Location rappresentanti Stanza, Piano ed Edificio referenziate dal profilo risultante dalla ricerca. Verranno inoltre restituite le Organization a cui afferiscono i letti occupati.

Un esempio di Bundle di risposta può essere consultato qui: {{link:esempio-PLO-Location}}.

###	2. Ricerca posti letto occupati per identificativo L2

I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	operational-status: da compilare con il valore “O” per indicare che il posto letto è occupato
-	organization.identifier: codice L2 dell'ente di riferimento

Inoltre, è possibile valorizzare i seguenti parametri:
-	lastUpdated: data e ora dell’ultimo aggiornamento dei dati
- organization.partof:Organization.identifier: codice L1 dell'ente di riferimento

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

|     SCOPE    | Progetti individuali attivi |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | Location?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto<br>&operational-status=O<br>&organization.identifier=030703009<br>&_include=Location:organization<br>&_include:iterate=Location:partof|

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Location?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto&operational-status=O&organization.identifier=030703009&_include=Location:organization&_include:iterate=Location:partof

Il risultato della precedente GET è un Bundle che contiene tutte le Location identificate dal profilo RLLocationPLOLetto, con lo stato del letto "occupato", afferenti ad un determinato codice L2.
Il Bundle conterrà anche le Location rappresentanti Stanza, Piano ed Edificio referenziate dal profilo risultante dalla ricerca. Verranno inoltre restituite le Organization a cui afferiscono i letti occupati.

###	3. Ricerca posti letto occupati per identificativo L3 (reparto clinico)

I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	operational-status: da compilare con il valore “O” per indicare che il posto letto è occupato
-	organization.identifier: codice L2 dell'ente di riferimento
- repartoClinico: codici L3 del reparto clinico di riferimento

Inoltre, è possibile valorizzare il seguente parametro:
-	lastUpdated: data e ora dell'aggiornamento dei dati
- organization.partof:Organization.identifier: codice L1 dell'ente di riferimento

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

|     SCOPE    | Progetti individuali attivi |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | Location?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto<br>&operational-status=O<br>&organization.identifier=030703009<br>&repartoClinico=0801,0842<br>&_include=Location:organization<br>&_include:iterate=Location:partof|

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Location?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto&operational-status=O&organization.identifier=030703009&repartoClinico=0801,0842&_include=Location:organization&_include:iterate=Location:partof

Il risultato della precedente GET è un Bundle che contiene tutte le Location identificate dal profilo RLLocationPLOLetto, con lo stato del letto "occupato", afferenti ad uno o più reparti clinici, afferenti ad un determinato codice L2.
Il Bundle conterrà anche le Location rappresentanti Stanza, Piano ed Edificio referenziate dal profilo risultante dalla ricerca. Verranno inoltre restituite le Organization a cui afferiscono i letti occupati.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard:
- _profile
- operational-status
- organization
- partof
- name
- identifier
- _lastUpdated

I parametri di ricerca del profilo RLLocationPLOLetto, oltre ai campi standard della risorsa Organization, sono definiti nella seguente tabella:

| Nome | Descrizione | Link Simplifier |
|---|---|---|
| physicalType | Parametro di ricerca per la tipologia di Location. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationPhysicalType}} |
| repartoClinico | Parametro di ricerca per il reparto clinico che ha in carico il paziente. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationRepartoClinico}} |
| repartoFisico | Parametro di ricerca per il reparto fisico dove il paziente risulta allettato. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationRepartoFisico}} |
| areaDegenza | Parametro di ricerca per l'area di degenza dove il paziente risulta allettato. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationAreaDegenza}} |
| dataOraAccettazione | Parametro di ricerca della data e ora di accettazione del paziente (ingresso in struttura). | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationDataOraAccettazione}} |
| dataOraDimissionePrevista | Parametro di ricerca della data e ora prevista per la dimissione del paziente | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationDataOraDimissionePrevista}} |
| dimissioneProtetta | Parametro di ricerca per ricercare se il posto letto è indicato per una dimissione protetta | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationDimissioneProtetta}} |
| dataOraOccupazioneLetto | Parametro di ricerca della data di occupazione del posto letto | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationDataOraOccupazioneLetto}} |
| regimeRicovero | Parametro di ricerca relativo al regime di ricovero | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLLocationRegimeRicovero}} |
<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLLocationPLOLetto:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| regimeRicovero | Regime di ricovero del paziente | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/RegimeRicovero}} |