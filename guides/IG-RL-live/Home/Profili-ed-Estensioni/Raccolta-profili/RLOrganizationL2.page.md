# RLOrganizationL2

- [RLOrganizationL2](#rlorganizationl2)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [1. Enti erogatori gestiti amministrativamente da un ente di codice L1](#1-enti-erogatori-gestiti-amministrativamente-da-un-ente-di-codice-l1)
    - [2. Enti erogatori presenti nell’ambito territoriale di una ASST](#2-enti-erogatori-presenti-nellambito-territoriale-di-una-asst)
    - [3. Enti erogatori accreditati nell’ambito territoriale di una ASST](#3-enti-erogatori-accreditati-nellambito-territoriale-di-una-asst)
    - [4. Enti erogatori accreditati nell’ambito territoriale di una ASST di una specifica tipologia](#4-enti-erogatori-accreditati-nellambito-territoriale-di-una-asst-di-una-specifica-tipologia)
    - [5. Enti erogatori accreditati nell’ambito territoriale di una ATS di una specifica tipologia](#5-enti-erogatori-accreditati-nellambito-territoriale-di-una-ats-di-una-specifica-tipologia)
    - [6. Enti erogatori accreditati in uno specifico distretto](#6-enti-erogatori-accreditati-in-uno-specifico-distretto)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLOrganizationL2 è stato strutturato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) per contenere le informazioni anagrafiche e di contatto delle strutture identificate attraverso un codice regionale di livello 2 (L2). Sebbene in Regione Lombardia le strutture identificate da un codice L2 siano di varie tipologie, attualmente questo profilo contiene esclusivamente le informazioni degli enti erogatori pubblici o privati accreditati di servizi socioassistenziali. (es. RSA, erogatori di ADI, Centri Diurni Integrati, ecc)

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
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

## Tipologie di ricerca

Di seguito la descrizione dei criteri di ricerca inerenti al profilo RLOrganizationL2.

###	1. Enti erogatori gestiti amministrativamente da un ente di codice L1

Questa ricerca può essere effettuata per ricavare gli entri erogatori di servizi socioassistenziali che afferiscono amministrativamente ad un ente di codice L1. Dunque, questa ricerca permette, ad esempio, di ricavare tutte le ASST che afferiscono ad una ATS, oppure tutti gli Enti Erogatori di servizi socioassistenziali privati accreditati.

Il parametro da valorizzare obbligatoriamente per effettuare la ricerca è:
-	partOf.reference(RLOrganizationL1).identifier:  codice L1 dell’ente di interesse

Inoltre, è possibile valorizzare il seguente parametro per raffinare la ricerca escludendo eventuali strutture che abbiano cessato l’erogazione dei servizi:
-	dataFineValidità: data di interesse

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Ricerca tutti gli enti erogatori gestiti amministrativamente da un ente di codice L1 |
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | /Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}&partof:Organization.identifier=\{_codicelivelloL1_\} |

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&partof:Organization.identifier=030720

restituirà tutte le strutture afferenti alla ASST Bergamo Est (030720) con una data di fine validità superiore al 05/04/2018.

### 2. Enti erogatori presenti nell’ambito territoriale di una ASST
Questa ricerca può essere effettuata per ricercare tutti gli enti erogatori di servizi socioassistenziali la cui sede operativa ricade in un distretto afferente ad una determinata ASST. 

Il parametro da valorizzare obbligatoriamente per effettuare la ricerca è:
-	distrettoTerritoriale.ASSTAfferenza.coding.code: codice dell’ASST di afferenza di interesse 

Inoltre, è possibile valorizzare il seguente parametro per raffinare la ricerca escludendo eventuali strutture che abbiano cessato l’erogazione dei servizi:
-	dataFineValidità: data di interesse

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:
 
| SCOPE | Ricerca tutti gli enti erogatori presenti nell’ambito territoriale di una ASST |
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | /Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}<br>&distrettoTerritorialeASSTAfferenza=\{_ASSTAfferenza_\} |

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&distrettoTerritorialeASSTAfferenza=030718

restituirà tutte le strutture la cui sede operativa ricade nel distretto afferente della ASST Papa Giovanni XXIII (030718) con una data di fine validità superiore al 05/04/2018.

### 3. Enti erogatori accreditati nell’ambito territoriale di una ASST 
Questa ricerca può essere effettuata per ricercare tutti gli entri erogatori di servizi socioassistenziali che si sono accreditati in almeno un distretto afferente ad una determinata ASST. Verranno restituite dalla ricerca anche le stesse ASST nel caso eroghino servizi socioassistenziali (es. cure domiciliari).

Il parametro da valorizzare obbligatoriamente per effettuare la ricerca è:
- distrettoAccreditamento.ASSTAfferenza.coding.code: codice dell’ASST di afferenza di interesse 

Inoltre, è possibile valorizzare il seguente parametro per raffinare la ricerca escludendo eventuali strutture che abbiano cessato l’erogazione dei servizi:
-	dataFineValidità: data di interesse

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Ricerca tutti gli enti erogatori accreditati nell’ambito territoriale di una ASST |
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | /Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}<br>&distrettoAccreditamentoAsstAfferenza=\{_ASSTAfferenza_\} |

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&distrettoAccreditamentoAsstAfferenza=714

restituirà tutte le strutture che si sono accreditate in almeno un distretto afferente alla ASST della Valcamonica (714) con una data di fine validità superiore al 05/04/2018.

### 4. Enti erogatori accreditati nell’ambito territoriale di una ASST di una specifica tipologia

Questa ricerca può essere effettuata per ricercare tutti gli entri erogatori di uno specifico servizio socioassistenziale che si sono accreditati in almeno un distretto afferente ad una determinata ASST. Verranno restituite dalla ricerca anche le stesse ASST nel caso siano enti erogatori del servizio socioassistenziale d’interesse (es. cure domiciliari).

I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	distrettoAccreditamento.ASSTAfferenza.coding.code: codice dell’ASST di afferenza di interesse 
-	type.coding.code: codice della tipologia del servizio socioassistenziale ente erogatore

Inoltre, è possibile valorizzare il seguente parametro per raffinare la ricerca escludendo eventuali strutture che abbiano cessato l’erogazione dei servizi:
-	dataFineValidità: data di interesse

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Ricerca tutti gli enti erogatori accreditati nell’ambito territoriale di una ASST di una specifica tipologia |
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | /Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}<br>&distrettoAccreditamentoAsstAfferenza=\{_ASSTAfferenza_\}<br>&type=\{_tipologia_\} |

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&distrettoAccreditamentoAsstAfferenza=714&type=C-DOM

restituirà tutte le strutture di tipo C-DOM che si sono accreditate in almeno un distretto afferente alla ASST della Valcamonica (714) con una data di fine validità superiore al 05/04/2018.

### 5. Enti erogatori accreditati nell’ambito territoriale di una ATS di una specifica tipologia
Questa ricerca può essere effettuata per ricercare tutti gli enti erogatori di uno specifico servizio socioassistenziale che si sono accreditati in almeno un distretto afferente ad una ASST o più ASST che afferiscono alla medesima ATS. Verranno restituite dalla ricerca anche le stesse ASST nel caso siano enti erogatori del servizio socioassistenziale d’interesse (es. cure domiciliari).

Il parametro da valorizzare obbligatoriamente per effettuare la ricerca è:
-	distrettoAccreditamento.ATSAfferenza.coding.code: codice dell’ATS di afferenza di interesse
-	type.coding.code: codice della tipologia del servizio socioassistenziale ente erogatore

Inoltre, è possibile valorizzare il seguente parametro per raffinare la ricerca escludendo eventuali strutture che abbiano cessato l’erogazione dei servizi:
-	dataFineValidità: data di interesse

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Ricerca tutti gli enti erogatori accreditati nell’ambito territoriale di una ATS di una specifica tipologia |
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | /Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}<br>&distrettoAccreditamentoAtsAfferenza=\{_ATSAfferenza_\}<br>&type=\{_tipologia_\} |

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&distrettoAccreditamentoAtsAfferenza=323&type=C-DOM

restituirà tutte le strutture di tipo C-DOM che si sono accreditate nelle ASST che afferiscono all'ATS della Montagna con una data di fine validità superiore al 05/04/2018.

### 6. Enti erogatori accreditati in uno specifico distretto
Questa ricerca può essere effettuata per ricercare tutti gli entri erogatori di servizi socioassistenziali che si sono accreditati in uno determinato distretto sanitario.

Il parametro da valorizzare obbligatoriamente per effettuare la ricerca è:
-	distrettoAccreditamento.codiceDistretto.coding.code: codice del distretto sanitario di interesse

Inoltre, è possibile valorizzare il seguente parametro per raffinare la ricerca escludendo eventuali strutture che abbiano cessato l’erogazione dei servizi:
-	dataFineValidità: data di interesse

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

| SCOPE | Ricerca tutti gli enti erogatori accreditati in uno specifico distretto |
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | /Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}<br>&distrettoAccreditamentoCodiceDistretto=\{_CodiceDistretto_\} |

A titolo esemplificativo, la chiamata: 

    http://localhost:52773/nprifhirgtw/api/v1/fhir/r4/operatori-siss-fhir-service-v1/Organization?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&distrettoAccreditamentoCodiceDistretto=22038

restituirà tutte le strutture che si sono accreditate nel distretto sanitario 22038 (Tavernerio) con una data di fine validità superiore al 05/04/2018.


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard:
-	_profile
-	Identifier
-	type
-	partOf

I parametri di ricerca del profilo RLOrganizationL2, oltre ai campi standard della risorsa Organization, sono definiti nella seguente tabella:

| Nome | Descrizione | Link Simplifier |
|---|---|---|
| dataFineValidita | Data di fine validità per strutture SISS. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataFineValidita}} |
| dataInizioValidita | Data inizio validità per strutture SISS. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataInizioValidita}} |
| distrettoAccreditamentoAsstAfferenza | ASST di afferenza del distretto territoriale sotto la quale   l'Ente Erogatore si è accreditato per erogare i servizi sociosanitari. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoAsstAfferenza}} |
| distrettoAccreditamentoAtsAfferenza | ATS di afferenza del distretto territoriale sotto la quale   l'Ente Erogatore si è accreditato per erogare i servizi sociosanitari. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoAtsAfferenza}} |
| distrettoAccreditamentoCodiceDistretto | Distretto di accreditamento nel quale l'Ente eroga i servizi   sociosanitari. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoCodiceDistretto}} |
| distrettoTerritorialeASSTAfferenza | ASST nella quale l'Ente erogatore ha la sede operativa. | {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoTerritorialeASSTAfferenza}} |

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLOrganizationL2:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| type | Codifica del tipo di presidio L2 | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2}} |
