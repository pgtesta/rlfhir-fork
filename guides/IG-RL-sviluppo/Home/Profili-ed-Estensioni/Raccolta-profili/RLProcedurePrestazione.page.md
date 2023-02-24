# RLProcedurePrestazione

- [RLProcedurePrestazione](#rlprocedureprestazione)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [Dettaglio delle prestazioni erogate al paziente in regime di ricovero domiciliare](#dettaglio-delle-prestazioni-erogate-al-paziente-in-regime-di-ricovero-domiciliare)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLProcedurePrestazione è stato strutturato a partire dalla risorsa generica FHIR [Procedure](http://hl7.org/fhir/R4/procedure.html) per riportare il dettaglio di una singola prestazione erogata al paziente in qualsiasi setting assistenziale.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
  {{link:esempio-Procedure-Prestazione}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

###	Dettaglio delle prestazioni erogate al paziente in regime di ricovero domiciliare

Questa ricerca deve essere effettuata da un’ASST per ottenere il dettaglio delle prestazioni che un Ente Erogatore ha erogato ad un paziente in regime di ricovero domiciliare. Mediante il numero pratica del servizio e cure domiciliari viene definita l’associazione della prestazione erogata con l’assistito.  

L’elenco delle prestazioni è generato a partire dalla data di attivazione del ricovero domiciliare (primo accesso di un operatore a domicilio) ed aggiornato alla data corrente della richiesta. Ogni istanza del profilo deve riferirsi ad una singola e specifica prestazione erogata. Dunque, anche nel caso in cui una prestazione sia erogata più volte durante un singolo accesso il bundle generato contiene un numero di istanze del profilo pari al numero di volte in cui la prestazione è stata effettuata.

I parametri da valorizzare per effettuare la ricerca sono:
-	basedOn.reference(RLServiceRequestServiziSociosanitari).identifier: numero pratica del servizio di cure domiciliari.
-	basedOn.reference(RLServiceRequestServiziSociosanitari).performer.reference(RLOrganizationL2).identifier: codice CUDES L2 dell’Ente Erogatore che ha in carico il pazient

| SCOPE | Dettaglio delle prestazioni erogate al paziente in regime di ricovero domiciliare |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | https://\<nome_host_Ente\>/\<contesto_FHIR\>/\<codiceCudesL1\>/\<versione\>/erogazione-adi |
| URL | Procedure?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione<br>&basedOn:ServiceRequest.code.coding.code=CDOM<br>&basedOn:ServiceRequest.performer.identifier=\{_codiceLivello2_\}<br>&basedOn:ServiceRequest.identifier=\{_numeroPratica_\}<br>&_include=Procedure:basedOn&_include=Procedure:subject |

A titolo esemplificativo, la chiamata: 

  Procedure?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione&basedOn:ServiceRequest.code.coding.code=CDOM&basedOn:ServiceRequest.performer.identifier=03014300&basedOn:ServiceRequest.identifier=2022000001&_include=Procedure:basedOn&_include=Procedure:subject

Restituirà tutte le prestazioni erogate per pratica numero "2022000001" e afferenti alla struttura "03014300".

Un esempio di Bundle di risposta può essere consultato qui: {{link:esempio-ricerca-prestazioni-erogate}}.

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- _include
- _profile
- based-on


<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value-set relativi al profilo RLProcedurePrestazione.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| modalitaErogazione | Codice e descrizione della modalità di erogazione della prestazione erogata in regime di ricovero domiciliare | La codifica esaustiva è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ModalitaErogazione}} |
| Category | Codice e descrizione dei setting assistenziali delle prestazioni | La codifica esaustiva è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-SettingAssistenziale}} |
| Code | Codice e descrizione delle prestazioni  | La codifica esaustiva è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/Prestazioni}}. Sulla base del setting assistenziale di interesse è possibile consultare la relativa codifica delle prestazioni erogabili|
| performer.function | Codice e descrizione della tipologia di operatore che ha effettuato la prestazione | La codifica esaustiva è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipoOperatore}} |
| tipoAccesso | Codice e descrizione del tipo di accesso | La codifica esaustiva è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipoAccesso}} |