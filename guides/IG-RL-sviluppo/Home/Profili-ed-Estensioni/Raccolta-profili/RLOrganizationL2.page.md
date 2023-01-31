# RLOrganizationL2

- [RLOrganizationL2](#rlorganizationl2)
  - [Descrizione](#descrizione)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Organization L2 appartenenti ad un codice L1 con data fine validità superiore ad una certa data](#organization-l2-appartenenti-ad-un-codice-l1-con-data-fine-validità-superiore-ad-una-certa-data)
    - [Organization L2 appartenenti ad una ASST di afferenza con data fine validità superiore ad una certa data](#organization-l2-appartenenti-ad-una-asst-di-afferenza-con-data-fine-validità-superiore-ad-una-certa-data)
    - [Organization L2 appartenenti ad un codice L1 con data validità superiore ad una certa data e di una specifica tipologia](#organization-l2-appartenenti-ad-un-codice-l1-con-data-validità-superiore-ad-una-certa-data-e-di-una-specifica-tipologia)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)

## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) volto a contenere le informazioni anagrafiche e di contatto relative alle strutture identificate da un codice di tipo L2 che erogano servizi sanitari e sociosanitari appartenenti agli enti codificati con codice L1. In Regione Lombardia le strutture univocamente identificate da un codice L2 rappresentano le unità d’offerta (es. RSA, centri diurni integrati, consultori, ecc). In questo profilo è definito il riferimento all’ente di tipo L1 alla quale l’UdO afferisce. 

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-RLOrganizationL2}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

Di seguito la descrizione dei criteri di ricerca inerenti al profilo RLOrganizationL2.

###	Organization L2 appartenenti ad un codice L1 con data fine validità superiore ad una certa data

I parametri da valorizzare per effettuare la ricerca sono:
- dataFineValidità: data di interesse
-	partOf.reference(RLOrganizationL1).identifier:  codice L1 dell’ente di interesse

L’esito della ricerca permette di recuperare le informazioni relative alle strutture di tipo L2 con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata struttura L1.

| SCOPE | Ricerca tutti i profili RLOrganizationL2 la cui data di fine validità è maggiore di una data di riferimento e che afferiscono ad una determinata struttura identificata dal codice L1 (RLOrganizationL1) |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}&partof:Organization.identifier=\{_codicelivelloL1_\} |

A titolo esemplificativo, la chiamata: 

    Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&partof:Organization.identifier=030720

restituirà tutte le strutture afferenti alla ASST Bergamo Est (030720) con una data di fine validità superiore al 05/04/2018.

### Organization L2 appartenenti ad una ASST di afferenza con data fine validità superiore ad una certa data
I parametri da valorizzare per effettuare la ricerca sono:
-	dataFineValidità: data di interesse
-	ASSTAfferenza.reference(RLOrganizationL1).identifier:  codice L1 dell’ASST di interesse

L’esito della ricerca permette di recuperare le informazioni relative alle strutture di tipo L2 con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata ASST.

| SCOPE | Ricerca tutti i profili RLOrganizationL2 la cui data di fine validità è maggiore di una data di riferimento e che afferiscono ad una determinata ASST (RLOrganizationL1) |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}&partof:Organization.identifier=\{_codicelivelloL1_\} |

A titolo esemplificativo, la chiamata: 

    Organization?_profile=https%3A//example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05…

restituirà tutte le strutture afferenti alla ASST.. 

### Organization L2 appartenenti ad un codice L1 con data validità superiore ad una certa data e di una specifica tipologia
I parametri da valorizzare per effettuare la ricerca sono:
-	dataFineValidità: data di interesse
-	ASSTAfferenza.reference(RLOrganizationL1).identifier:  codice L1 dell’ASST di interesse
-	type.coding.code: codice della tipologia di UdO

L’esito della ricerca permette di recuperare le informazioni relative alle strutture di tipo L2 di una determinata tipologia di unità d’offerta (UdO) sociosanitaria, con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata ASST.

| SCOPE | Ricerca tutti i profili RLOrganizationL12 la cui data di fine validità è maggiore di una data di riferimento, che sono afferenti ad una determinata ASST (RLOrganizationL1) e sono di una o più tipologie (es. RIC,RSA) |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2& dataFineValidita={_datadiRiferimento_}&partof:Organization.identifier={_codicelivelloL1_}&
type={_tipoRicercato1,...,tipoRicercatoN_} |

A titolo esemplificativo, la chiamata:

    Organization?_profile=https%3A//example.org/fhir/StructureDefinition/ RLOrganizationL2&dataFineValidita=gt2018-04-05 & type=CONS….

restituirà tutte i consultori (CONS) afferenti alla ASST… 

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- _profile
- identifier
- partof
- type

I parametri di ricerca definiti nel profilo RLOrganizationL2 sono definiti nella seguente tabella:

| Nome e link Simplifier | Descrizione | Codice |
|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationASSTAfferenza}} | ASST di afferenza | asstAfferenza |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataFineValidita}} | Parametro di ricerca di strutture SISS di livello 1 e livello   2 specificando la data di fine validità. | dataFineValidita |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataInizioValidita}} | Parametro di ricerca di strutture SISS di livello 1 e livello   2 specificando la data di inserimento. | dataInizioValidita |


<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Nella seguente tabella sono elencati i value set relativi al profilo RLOrganizationL2:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| type | Codifica del tipo di presidio L2 | Il riferimento alla lista esaustiva della tipologia di UdO è consultabile al seguente {{pagelink:Home/Terminologia/Libreria-ValueSet.page.md, text:link}} |
