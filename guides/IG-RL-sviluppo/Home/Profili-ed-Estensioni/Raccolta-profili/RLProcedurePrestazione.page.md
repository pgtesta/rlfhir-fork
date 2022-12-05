# RLProcedurePrestazione

- [RLProcedurePrestazione](#rlprocedureprestazione)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Dettaglio delle prestazioni erogate al paziente in regime di ricovero domiciliare aggiornate alla data e ora di richiesta](#dettaglio-delle-prestazioni-erogate-al-paziente-in-regime-di-ricovero-domiciliare-aggiornate-alla-data-e-ora-di-richiesta)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione
Profilo declinato a partire dalla risorsa generica FHIR [Procedure](http://hl7.org/fhir/R4/procedure.html) che contiene il dettaglio di una prestazione erogata al paziente in qualsiasi setting assistenziale.

Profilo declinato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) volto a contenere le informazioni anagrafiche e di contatto relative alle strutture di tipo ente L1. In Regione Lombardia gli enti univocamente identificati da un codice L1 sono di varie tipologie e possono essere ASST o ATS così come MMG/PLS.

La pagina Simplifier della risorsa è consultabile qui: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione, text: qui}}.

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

<!-- ===================================================FINE SESSIONE=================================================== -->

## Extension
Non sono state sviluppate extension per questo profilo.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Criteri di ricerca

### Dettaglio delle prestazioni erogate al paziente in regime di ricovero domiciliare aggiornate alla data e ora di richiesta
Il dettaglio delle prestazioni è inteso come riassuntivo del periodo che va dalla data di attivazione  del ricovero domiciliare (primo accesso di un operatore a domicilio) alla data corrente della richiesta. 
I parametri da valorizzare per effettuare la ricerca sono:
-	basedOn.reference(RLServiceRequestServiziSociosanitari).identifier
-	basedOn.reference(RLServiceRequestServiziSociosanitari).code

L’esito della ricerca permette di recuperare le informazioni relative alle prestazioni erogate dall’ente erogatore della presa in carico al cittadino in regime di ricovero domiciliare aggiornate alla data corrente della richiesta.


| SCOPE | Ricerca |
|---|---|
| VERB | GET |
| BASE |    |
| URL |     |

<!-- ===================================================FINE SESSIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre ai campi standard della risorsa Procedure.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Value set

Nella seguente tabella sono elencati i value-set relativi al profilo RLProcedurePrestazione.

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| Code    | Codice e descrizione della prestazione    | Il riferimento alla lista esaustiva delle prestazioni ricavate dal tracciato SIAD 3 è consultabile al seguente {{pagelink:Home/CodeSystem-e-ValueSet/ValueSet.page.md, text:link}}   |