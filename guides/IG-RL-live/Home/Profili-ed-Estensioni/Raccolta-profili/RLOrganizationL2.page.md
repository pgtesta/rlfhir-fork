# RLOrganizationL2

- [RLOrganizationL2](#rlorganizationl2)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Organization L2 appartenenti ad un codice L1 con data fine validità superiore ad una certa data](#organization-l2-appartenenti-ad-un-codice-l1-con-data-fine-validità-superiore-ad-una-certa-data)
    - [Organization L2 appartenenti ad un codice L1 con data validità superiore ad una certa data e di una specifica tipologia](#organization-l2-appartenenti-ad-un-codice-l1-con-data-validità-superiore-ad-una-certa-data-e-di-una-specifica-tipologia)
  - [Serch parameter](#serch-parameter)
  - [Value set](#value-set)

## Descrizione

Profilo declinato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) volto a contenere le informazioni anagrafiche e di contatto relative alle strutture identificate da un codice di tipo L2 che erogano servizi sanitari e sociosanitari appartenenti agli enti codificati con codice L1. In Regione Lombardia le strutture univocamente identificate da un codice L2 rappresentano le unità d’offerta (es. RSA, centri diurni integrati, consultori, ecc). In questo profilo è definito il riferimento all’ente di tipo L1 alla quale l’UdO afferisce. 

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, text: qui}}.

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
{{pagelink:Home/Esempi/esempio-RLOrganizationL2.page.md}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Extension
Di seguito la descrizione delle extension inerenti al profilo RLOrganizationL2:

| Nome   Extension e link Simplifier | Nome campo esteso | Descrizione | Contesto |
|---|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita}} | DataInizioValidita | Data di inizio della validità di esercizio dell'ente descritto   dal profilo | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita}} | DataFineValidita | Data di fine della validità di esercizio dell'ente descritto   dal profilo | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInsert}} | DataInsert | Data di inserimento del record | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataUpdate}} | DataUpdate | Data di aggiornamento del record | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationASSTAfferenza}} | ASSTAfferenza | ASST sotto la quale l'ente eroga servizi sociosanitari sul   territorio di competenza | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationATSAfferenza}} | ATSAfferenza | ATS alla quale il presidio afferisce territorialmente | Organization |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressDistrettoCode}} | DistrettoCode | Distretto territoriale così definito dalla legge regionale   22-2021 della Regione Lombardia | Organization.Address |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressIstatCode}} | IstatCode | Codice ISTAT | Organization.Address |

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

Di seguito la descrizione dei criteri di ricerca inerenti al profilo RLOrganizationL2.

###	Organization L2 appartenenti ad un codice L1 con data fine validità superiore ad una certa data
Parametri di ricerca:
- dataFineValidità
- partOf 

L’esito della ricerca permette di recuperare le informazioni relative alle strutture di tipo L2, descritto nel profilo _RLOrganizationL2_, con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata struttura L1 (profilo _RLOrganizationL1_).

| SCOPE | Ricerca tutte le Organization con profilo L2 la cui data di fine validità è maggiore di una data di riferimento e che sono parte   di un determinato codice L1 |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}&partof:Organization.identifier=\{_codicelivelloL1_\} |

A titolo esemplificativo, la chiamata: 

    Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&partof:Organization.identifier=030720

restituirà tutte le strutture afferenti alla ASST Bergamo Est (030720) con una data di fine validità superiore al 05/04/2018.

### Organization L2 appartenenti ad un codice L1 con data validità superiore ad una certa data e di una specifica tipologia
Parametri di ricerca:
- dataFineValidità
- partOf 
- type

L’esito della ricerca permette di recuperare le informazioni relative alle strutture di tipo L2, descritte nel profilo _RLOrganizationL2_, di una determinata tipologia di unità d’offerta (UdO) sociosanitaria, con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata struttura L1 (profilo _RLOrganizationL1_).


| SCOPE | Ricerca tutte le Organization con profilo L2 la cui data di fine validità è maggiore di una data di riferimento e che sono parte di un determinato codice L1 afferente ad una ASST Territoriale |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2& dataFineValidita={_datadiRiferimento_}&partof:Organization.identifier={_codicelivelloL1_}&
type={_tipoRicercato1,...,tipoRicercatoN_} |

A titolo esemplificativo, la chiamata:

    Organization?_profile=https%3A//example.org/fhir/StructureDefinition/ RLOrganizationL2&dataFineValidita=gt2018-04-05 &partof:Organization.identifier=030720&type=CONS

restituirà tutte i consultori (CONS) afferenti alla ASST Bergamo Est (030720) con una data di fine validità superiore al 05/04/2018.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Serch parameter

I parametri di ricerca definiti nel profilo RLOrganizationL2 sono definiti nella seguente tabella:

| Nome | Descrizione | URL | Espressione |
|---|---|---|---|
| RLOrganizationDataFineValidita | Parametro di ricerca di strutture SISS di livello 1 e livello 2   specificando la data di fine validità. | https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataFineValidita | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita').value |
| RLOrganizationDataInizioValidita | Parametro di ricerca di strutture SISS di   livello 1 e livello 2 specificando la data di inserimento. | https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataInizioValidita | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita').value |

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Nella seguente tabella sono elencati i value set relativi al profilo RLOrganizationL2:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| type | Codifica del tipo di presidio L2 | Il riferimento alla lista esaustiva della tipologia di UdO è consultabile al seguente {{pagelink:Home/CodeSystem-e-ValueSet/ValueSet.page.md, text:link}} |
