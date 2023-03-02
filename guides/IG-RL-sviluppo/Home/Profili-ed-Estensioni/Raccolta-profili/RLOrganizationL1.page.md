# RLOrganizationL1

- [RLOrganizationL1](#rlorganizationl1)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [Enti L1 attualmente attivi](#enti-l1-attualmente-attivi)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione
Il profilo RLOrganizationL1 è stato strutturato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) ed è volto a contenere le informazioni anagrafiche e di contatto relative alle strutture di tipo ente L1. In Regione Lombardia gli enti univocamente identificati da un codice L1 sono di varie tipologie e possono essere ASST o ATS così come MMG/PLS. 

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
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

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

### Enti L1 attualmente attivi
I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	DataFineValidita: data di interesse

| SCOPE | Organization L1 con data fine validità superiore alla data odierna o nulla    |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4    |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL1<br>&dataFineValidita=\{_datadiRiferimento_\}    |

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- _profile
- identifier
- partof

I parametri di ricerca del profilo RLOrganizationL1, oltre ai campi standard della risorsa Organization, sono definiti nella seguente tabella:

| Nome e link Simplifier | Descrizione | Espressione |
|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataFineValidita}} | Parametro di ricerca di strutture SISS di livello 1 specificando la data di fine validità. | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataInizioValidita}} | Parametro di ricerca di strutture SISS di livello 1 specificando la data di   inserimento.  |  extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita').value |

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value-set relativi al profilo RLOrganizationL1

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| type    | Codifica del tipo di azienda L1    | Il riferimento alla lista esaustiva della tipologia di enti di livello 1 è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}}   |