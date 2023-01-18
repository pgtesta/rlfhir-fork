# RLProcedurePrestazione

- [RLProcedurePrestazione](#rlprocedureprestazione)
  - [Descrizione](#descrizione)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Dettaglio delle prestazioni erogate al paziente in regime di ricovero domiciliare](#dettaglio-delle-prestazioni-erogate-al-paziente-in-regime-di-ricovero-domiciliare)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione
Profilo declinato a partire dalla risorsa generica FHIR [Procedure](http://hl7.org/fhir/R4/procedure.html) che contiene il dettaglio di una prestazione erogata al paziente in qualsiasi setting assistenziale.

Profilo declinato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) volto a contenere le informazioni anagrafiche e di contatto relative alle strutture di tipo ente L1. In Regione Lombardia gli enti univocamente identificati da un codice L1 sono di varie tipologie e possono essere ASST o ATS così come MMG/PLS.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, text: qui}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
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
{{pagelink:Home/Esempi/ASST-della-Brianza.page.md}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

###	Dettaglio delle prestazioni erogate al paziente in regime di ricovero domiciliare

Questa ricerca deve essere effettuata da un’ASST per ottenere il dettaglio delle prestazioni che un Ente Erogatore ha erogato ad un paziente in regime di ricovero domiciliare. L’elenco delle prestazioni è da intendersi come riassuntivo del periodo che va dalla data di attivazione del ricovero domiciliare (primo accesso di un operatore a domicilio) alla data corrente della richiesta. 

L’associazione al paziente è definita tramite il numero pratica del servizio di cure domiciliari.

I parametri da valorizzare per effettuare la ricerca sono:
-	basedOn.reference(RLServiceRequestServiziSociosanitari).identifier: numero pratica del servizio di cure domiciliari.
-	basedOn.reference(RLServiceRequestServiziSociosanitari).performer.reference(RLOrganizationL2).identifier: codice L2 dell’Ente Erogatore che ha in carico il paziente

L’esito della ricerca produrrà un bundle contenente le informazioni relative alle prestazioni effettuate dall’ente erogatore della presa in carico del cittadino in regime di ricovero domiciliare aggiornate alla data corrente della richiesta.

| SCOPE | Ricerca tutti i profili RLProcedurePrestazione che sono riferiti ad una pratica di erogazione di cure domiciliare (profilo RLServiceRequestServiziSociosanitari) |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | https://<nome_host_Ente>/<contesto_FHIR>/<codiceCudesL1>/<versione>/erogazione-adi |
| URL | Procedure?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione&basedOn:ServiceRequest.code.coding.code=C-DOM&basedOn:ServiceRequest.performer.identifier=\{_codiceLivello2_\}&basedOn:ServiceRequest.identifier=\{_numeroPratica_\}&_include=Procedure:basedOn&_include=Procedure:subject |

A titolo esemplificativo, la chiamata: 

  Procedure?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione&basedOn:ServiceRequest.code.coding.code=C-DOM&basedOn:ServiceRequest.performer.identifier=03014300&basedOn:ServiceRequest.identifier=000001&_include=Procedure:basedOn&_include=Procedure:subject

Restituirà tutte le prestazioni erogate per pratica numero "000001" e afferenti alla struttura "03014300".

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre ai campi standard della risorsa Procedure.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Nella seguente tabella sono elencati i value-set relativi al profilo RLProcedurePrestazione.

| Nome  | Descrizione  | Riferimento al dettaglio della codifica  |
|---|---|---|
| modalitaErogazione  | Codice e descrizione della modalità di erogazione  | Il riferimento alla lista esaustiva delle modalità di erogazione ricavate dal tracciato SIAD 3 è consultabile al seguente {{pagelink:Home/CodeSystem-e-ValueSet/ValueSet.page.md, text:link}}  |
| Code  | Codice e descrizione della prestazione  | Il riferimento alla lista esaustiva delle prestazioni ricavate dal tracciato SIAD 3 è consultabile al seguente {{pagelink:Home/CodeSystem-e-ValueSet/ValueSet.page.md, text:link}}  |
