# RLOrganizationL3

- [RLOrganizationL3](#rlorganizationl3)
  - [Descrizione](#descrizione)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Organization L3 appartenenti ad un codice L2 con data fine validità superiore ad una certa data](#organization-l3-appartenenti-ad-un-codice-l2-con-data-fine-validità-superiore-ad-una-certa-data)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) volto a contenere le informazioni identificative e descrittive relative ad un reparto di ricovero identificato da un codice di tipo L3. In questo profilo è definito il riferimento alle strutture ospedaliere di tipo L2 alla quale il reparto afferisce. 

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3, text: qui}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-RLOrganizationL3}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

### Organization L3 appartenenti ad un codice L2 con data fine validità superiore ad una certa data
I parametri da valorizzare per effettuare la ricerca sono:
-	dataFineValidità: data di interesse
-	partOf.reference(RLOrganizationL2).identifier

L’esito della ricerca permette di recuperare le informazioni relative alle strutture di tipo L3,  con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata struttura L2.

| SCOPE | Ricerca tutti i profili RLOrganizationL3 la cui data di fine validità è maggiore di una data di riferimento e che sono parte di un determinato codice L2 (RLOrganizationL2)    |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4    |
| URL | /    |

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- _profile
- partof

I parametri di ricerca del profilo RLOrganizationL3, oltre ai campi standard della risorsa Organization, sono definiti nella seguente tabella:

| Nome e link Simplifier | Descrizione | Codice |
|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataInizioValidita}} | Parametro di ricerca di strutture SISS di livello 1 e livello   2 specificando la data di inserimento. | dataInizioValidita |

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Attualmente non sono definiti value set specifici per il profilo RLOrganizationL3.
