# RLOrganizationL2

- [RLOrganizationL2](#rlorganizationl2)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [Enti erogatori gestiti amministrativamente da un ente di codice L1](#enti-erogatori-gestiti-amministrativamente-da-un-ente-di-codice-l1)
    - [Enti erogatori presenti nell’ambito territoriale di una ASST](#enti-erogatori-presenti-nellambito-territoriale-di-una-asst)
    - [Enti erogatori accreditati nell’ambito territoriale di una ASST](#enti-erogatori-accreditati-nellambito-territoriale-di-una-asst)
    - [Enti erogatori accreditati nell’ambito territoriale di una ASST di una specifica tipologia](#enti-erogatori-accreditati-nellambito-territoriale-di-una-asst-di-una-specifica-tipologia)
    - [Enti erogatori accreditati nell’ambito territoriale di una ATS di una specifica tipologia](#enti-erogatori-accreditati-nellambito-territoriale-di-una-ats-di-una-specifica-tipologia)
    - [Enti erogatori accreditati in uno specifico distretto](#enti-erogatori-accreditati-in-uno-specifico-distretto)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLOrganizationL2 è stato strutturato a partire dalla risorsa standard FHIR [Organization](http://hl7.org/fhir/R4/organization.html) per contenere le informazioni anagrafiche e di contatto delle strutture identificate attraverso un codice regionale di livello 2 (L2).Sebbene in Regione Lombardia le strutture univocamente identificate da un codice L2 siano di varie tipologie, attualmente questo profilo contiene esclusivamente informazioni riguardo enti erogatrori pubblici o privati accreditati di servizi socio assistenziali. 

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

###	Enti erogatori gestiti amministrativamente da un ente di codice L1

Questa ricerca può essere effettuata per ricavare gli entri erogatori di servizi socioassistenziali che afferiscono amministrativamente ad un ente di codice L1. Duque, questa ricerca permette, ad esempio, di ricavare tutte le ASST che afferiscono ad una ATS, oppure tutte le strutture erogatrici di servizi ente privato accreditato.

I parametri da valorizzare per effettuare la ricerca sono:
-	dataFineValidità: data di interesse
-	partOf.reference(RLOrganizationL1).identifier:  codice L1 dell’ente di interesse

| SCOPE | Ricerca tutti gli enti erogatori gestiti amministrativamente da un ente di codice L1 |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}&partof:Organization.identifier=\{_codicelivelloL1_\} |

A titolo esemplificativo, la chiamata: 

    Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&partof:Organization.identifier=030720

restituirà tutte le strutture afferenti alla ASST Bergamo Est (030720) con una data di fine validità superiore al 05/04/2018.

### Enti erogatori presenti nell’ambito territoriale di una ASST
Questa ricerca può essere effettuata per ricercare tutti gli entri erogatori di servizi socioassistenziali la cui sede operativa ricade in un distretto afferente ad una determinata ASST. 

I parametri da valorizzare per effettuare la ricerca sono:
-	dataFineValidità: data di interesse
-	distrettoTerritoriale.ASSTAfferenza.coding.code: codice dell’ASST di afferenza di interesse 

| SCOPE | Ricerca tutti gli enti erogatori presenti nell’ambito territoriale di una ASST |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=\{_datadiRiferimento_\}&partof:Organization.identifier=\{_codicelivelloL1_\} |

A titolo esemplificativo, la chiamata: 

    Organization?_profile=https%3A//example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05…

restituirà tutte le strutture afferenti alla ASST.. 

### Enti erogatori accreditati nell’ambito territoriale di una ASST 
Questa ricerca può essere effettuata per ricercare tutti gli entri erogatori di servizi socioassistenziali che si sono accreditati in almeno un distretto afferente ad una determinata ASST. Verranno restituite dalla ricerca anche le stesse ASST siano enti erogatori di servizi socioassistenziali (es. cure domiciliari).

I parametri da valorizzare per effettuare la ricerca sono:
-	dataFineValidità: data di interesse
-	distrettoAccreditamento.ASSTAfferenza.coding.code: codice dell’ASST di afferenza di interesse 


### Enti erogatori accreditati nell’ambito territoriale di una ASST di una specifica tipologia

Questa ricerca può essere effettuata per ricercare tutti gli entri erogatori di uno specifico servizio socioassistenziale (UdO) che si sono accreditati in almeno un distretto afferente ad una determinata ASST. Verranno restituite dalla ricerca anche le stesse ASST nel caso siano enti erogatori del servizio socioassistenziale d’interesse (es. cure domiciliari).

I parametri da valorizzare per effettuare la ricerca sono:
-	dataFineValidità: data di interesse
-	distrettoAccreditamento.ASSTAfferenza.coding.code: codice dell’ASST di afferenza di interesse 
-	type.coding.code: codice della tipologia di UdO


### Enti erogatori accreditati nell’ambito territoriale di una ATS di una specifica tipologia
Questa ricerca può essere effettuata per ricercare tutti gli entri erogatori di uno specifico servizio socioassistenziale (UdO) che si sono accreditati in almeno un distretto afferente ad una ASST o più ASST che afferiscono alla medesima ATS. Verranno restituite dalla ricerca anche le stesse ASST nel caso siano enti erogatori del servizio socioassistenziale d’interesse (es. cure domiciliari).

Il parametro da valorizzare per effettuare la ricerca è:
-	dataFineValidità: data di interesse
-	distrettoAccreditamento.ATSAfferenza.coding.code: codice dell’ATS di afferenza di interesse

L’esito della ricerca permette di recuperare le informazioni relative alle strutture di tipo L2 con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata ATS.

### Enti erogatori accreditati in uno specifico distretto
Questa ricerca può essere effettuata per ricercare tutti gli entri erogatori di servizi socioassistenziali che si sono accreditati in uno determinato distretto sanitario.

Il parametro da valorizzare per effettuare la ricerca è:
-	dataFineValidità: data di interesse
-	distrettoAccreditamento.codiceDistretto.coding.code: codice del distretto sanitario di interesse

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter

Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- _profile: parametro di ricerca standard dell'ente di codice L1 al quale l'ente di codice L2 afferisce amministrativamente
- identifier
- partof
- type

I parametri di ricerca del profilo RLOrganizationL2, oltre ai campi standard della risorsa Organization, sono definiti nella seguente tabella:

| Nome e link Simplifier | Descrizione | Codice |
|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataFineValidita}} | Parametro di ricerca di strutture SISS di livello 2 specificando la data di fine validità. | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataInizioValidita}} | Parametro di ricerca di strutture SISS di livello 2 specificando la data di inserimento. | extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoAsstAfferenza}} | Parametro di ricerca dell’ASST sotto la quale l'ente eroga servizi sociosanitari sul territorio di competenza. | extension.where(url='https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoAsstAfferenza').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoAtsAfferenza}} | Parametro di ricerca dell’ATS sotto la quale l'ente eroga servizi sociosanitari sul territorio di competenza. | extension.where(url='https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoAtsAfferenza').value |
| {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoCodiceDistretto}} | Parametro di ricerca del distretto di accreditamento nel quale l'ente eroga servizi sociosanitari. | extension.where(url='https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDistrettoAccreditamentoCodiceDistretto').value |


<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLOrganizationL2:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| type | Codifica del tipo di presidio L2 | La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2}} |
