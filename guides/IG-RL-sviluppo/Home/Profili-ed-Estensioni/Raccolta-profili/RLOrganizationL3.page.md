# RLOrganizationL3

- [RLOrganizationL3](#rlorganizationl3)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Oganization L3 appartenenti ad un codice L2 con data fine validità superiore ad una certa data](#oganization-l3-appartenenti-ad-un-codice-l2-con-data-fine-validità-superiore-ad-una-certa-data)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) volto a contenere le informazioni identificative e descrittive relative ad un reparto di ricovero identificato da un codice di tipo L3. In questo profilo è definito il riferimento alle strutture ospedaliere di tipo L2 alla quale il reparto afferisce. 

La pagina Simplifier della risorsa è consultabile qui: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3, text: qui}}.

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
{{pagelink:Home/Esempi/Medicina-specifica.page.md}}
<br>
</div>

<!-- ===================================================FINE SESSIONE=================================================== -->

## Extension
Di seguito la descrizione delle extension inerenti al profilo RLOrganizationL3:

| Nome   Extension e link Simplifier | Nome campo esteso | Descrizione | Contesto |
|---|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita}} | DataInizioValidita | Data di inizio della validità di esercizio dell'ente descritto dal profilo | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita}} | DataFineValidita | Data di fine della validità di esercizio dell'ente descritto dal profilo | Organization |


<!-- ===================================================FINE SESSIONE=================================================== -->

## Criteri di ricerca

### Oganization L3 appartenenti ad un codice L2 con data fine validità superiore ad una certa data
Parametri di ricerca:
-	dataFineValidità
-	partOf 

L’esito della ricerca permette di recuperare le informazioni relative alle strutture di tipo L3, descritto nel profilo _RLOrganizationL3_, con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata struttura L2 (profilo _RLOrganizationL2_).


| SCOPE | Ricerca tutte le Organization con profilo L3 la cui data di fine validità è maggiore di una data di riferimento e che sono parte di un determinato codice L2    |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4    |
| URL | /    |

<!-- ===================================================FINE SESSIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa Organization.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Value set

Attualmente non sono definiti value set specifici per il profilo RLOrganizationL3.
