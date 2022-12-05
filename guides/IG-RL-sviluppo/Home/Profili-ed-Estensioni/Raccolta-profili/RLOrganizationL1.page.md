# RLOrganizationL1

- [RLOrganizationL1](#rlorganizationl1)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Enti L1 attualmente attivi](#enti-l1-attualmente-attivi)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) volto a contenere le informazioni anagrafiche e di contatto relative alle strutture di tipo ente L1. In Regione Lombardia gli enti univocamente identificati da un codice L1 sono di varie tipologie e possono essere ASST o ATS così come MMG/PLS.

La pagina Simplifier della risorsa è consultabile qui: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, text: qui}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-RLOrganizationL1}}
<br>
</div>

<!-- ===================================================FINE SESSIONE=================================================== -->

## Extension
Di seguito la descrizione delle extension inerenti al profilo RLOrganizationL1:

| Nome   Extension e link Simplifier | Nome campo esteso | Descrizione | Contesto |
|---|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataCessazione}} | DataCessazione | Data di cessazione dell'ente | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInsert}} | DataInsert | Data di inserimento del record | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataUpdate}} | DataUpdate | Data di aggiornamento del record | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataCostituzione}} | DataCostituzione | Data di costituzione dell'ente | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita}} | DataInizioValidita | Data di inizio della validità di esercizio dell'ente descritto   dal profilo | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita}} | DataFineValidita | Data di fine della validità di esercizio dell'ente descritto   dal profilo | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressIstatCode}} | IstatCode | Codice ISTAT | Organization.Address |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressDistrettoCode}} | DistrettoCode | Distretto territoriale così definito dalla legge regionale   22-2021 della Regione Lombardia | Organization.Address |

<!-- ===================================================FINE SESSIONE=================================================== -->

## Criteri di ricerca

### Enti L1 attualmente attivi
Organization L1 con data fine validità superiore alla data odierna o nulla

| SCOPE | Ricerca tutte le Organization con profilo L2 la cui   data di fine validità è maggiore di una data di riferimento e che sono parte   di un determinato codice L1    |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4    |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=\{datadiRiferimento\}&partof:Organization.identifier=\{codicelivelloL1\}    |

<!-- ===================================================FINE SESSIONE=================================================== -->

## Search parameter

I parametri di ricerca definiti nel profilo RLOrganizationL1 sono definiti nella seguente tabella:

| Nome | Descrizione | URL | Espressione |
|---|---|---|---|
| RLOrganizationDataFineValidita | Parametro di ricerca di strutture SISS di livello 1 e livello 2   specificando la data di fine validità. | https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataFineValidita | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita').value |
| RLOrganizationDataInizioValidita | Parametro di ricerca di strutture SISS di livello 1 e livello 2   specificando la data di inserimento. | https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataInizioValidita | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita').value |

<!-- ===================================================FINE SESSIONE=================================================== -->

## Value set

Nella seguente tabella sono elencati i value-set relativi al profilo RLOrganizationL1.

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| type    | Codifica del tipo di azienda L1    | Il riferimento alla lista esaustiva della tipologia di enti di   livello 1 è consultabile al seguente {{pagelink:Home/CodeSystem-e-ValueSet/ValueSet.page.md, text:link}}   |