# RLCarePlanProgettoIndividuale

- [RLCarePlanProgettoIndividuale](#rlcareplanprogettoindividuale)
  - [Descrizione](#descrizione)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Progetti individuali attivi](#progetti-individuali-attivi)
    - [Progetti individuali di un paziente](#progetti-individuali-di-un-paziente)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione

Profilo declinato a partire dalla risorsa generica FHIR [CarePlan](http://hl7.org/fhir/R4/careplan.html) per descrivere il progetto individuale di un cittadino. All’interno del profilo sono contenute informazioni generali quali: durata del progetto, obiettivi di salute, case manager, esiti delle valutazioni, patologie principali, secondarie e addizionali, allergie, esenzioni e stili di vita del cittadino; così come le attività di natura clinica, infermieristica e sociale che compongono il progetto. 

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, text: qui}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Al momento non ci sono esempi disponibili.
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

Di seguito la descrizione dei criteri di ricerca inerenti al profilo RLCarePlanProgettoIndividuale.

###	Progetti individuali attivi

Questa ricerca deve essere effettuata dagli Enti Erogatori di servizi sociosanitari con lo scopo di ottenere l’elenco dei progetti individuali prodotti da un’ASST per gli assisiti che necessitano dell’attivazione di un servizio sociosanitario presso l’Ente Erogatore stesso. 
Premesso che esiste un'unica versione del progetto individuale in stato “attivo” e quindi in corso di validità, all’Ente Erogatore verrà restituito solo ed esclusivamente il dettaglio informativo del servizio sociosanitario da attivare al cittadino. 

I parametri da valorizzare per effettuare la ricerca sono:
-	status: da compilare con il valore “active”
-	activity.reference(RLServiceRequestServiziSociosanitari).code.coding.code: codice del servizio sociosanitario d’interesse
-	author.reference(RLOrgnizationL1).identifier: codice L1 dell’ASST che ha prodotto il progetto individuale
-	lastUpdated: data e ora dell’ultimo aggiornamento dei dati 

L’esito della ricerca produrrà un bundle che permetterà all’Ente Erogatore di recuperare il contenuto informativo relativo all’attivazione di un servizio sociosanitario previsto nei progetti individuali attivi prodotti da un’ASST.

|     SCOPE    |    Ricerca tutti i profili RLCarePlanProgettoIndividuale in stato attivo prodotti da una determinata ASST (RLOrganizationL1) che contengono almeno una reference al profilo RLServiceRequestServiziSociosanitari relativa ai servizi sociosanitari di una determinata tipologia (es. C-DOM, RSA, ecc.). |
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | <font style="color:red">endpoint FHIR SGDT</font> |
| URL | CarePlan?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale&activity.reference.code.coding.code=C-DOM&activity.reference.performer.identifier=\{_codiceLivelloL2_\}&_lastUpdated=gt\{_dataLimiteIntervalloInferiore_\}&_lastUpdated=lt\{_dataLimiteIntervalloSuperiore_\}&status=active&_include=CarePlan:activity.reference&_include=CarePlan:subject |

A titolo esemplificativo, la chiamata: 

    CarePlan?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale&activity.reference.code.coding.code=C-DOM&activity.reference.performer.identifier=03014300&_lastUpdated=gt2022-11-18T16:00:00+00:00&_lastUpdated=lt2022-11-30T16:00:00+00:00&status=active&_include=CarePlan:activity.reference&_include=CarePlan:subject

Restituirà tutti i Progetti Individuali attivi contenenti esclusivamente i dettagli del ricovero domiciliare in carico all’ente con codice livello 2 "03014300" e creati e/o modificati tra le 16:00 del giorno 18-11-2022 e le 16:00 del giorno 30-11-2022. Il risultato della ricerca conterrà anche le informazioni inerenti al servizio sociosanitario attivo e al paziente stesso.

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.

### Progetti individuali di un paziente

Questa ricerca deve essere effettuata dagli Enti Erogatori di servizi sociosanitari con lo scopo di fruire dello storico dei progetti individuali di un assistito che contengono l’attivazione di un servizio sociosanitario.
L’elenco dei progetti individuali conterrà solo ed esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato all’Ente Erogatore chiamante. In virtù di ciò, lo scopo della ricerca è quello di consentire all’Ente Erogatore il confronto tra le versioni del progetto individuale precedentemente salvate e quelle restituite dalla ricerca.

I parametri da valorizzare per effettuare la ricerca sono:
-	activity.reference(RLServiceRequestServiziSociosanitari).code coding.code: codice del servizio sociosanitario d’interesse
-	activity.reference(RLServiceRequestServiziSociosanitari).identifier: codice identificativo del servizio sociosanitario attivato/da attivare all’assistito
-	subject.reference(RLPatientCittadino).identifier: codice fiscale dell’assistito
 
L’esito della ricerca produrrà un bundle che permetterà all’Ente Erogatore di recuperare le informazioni relative ai progetti individuali redatti a un cittadino per i quale è stata prevista l’attivazione presso l’Ente Erogatore stesso di un servizio sociosanitario.

|     SCOPE    |Ricerca tutti i profili RLCarePlanProgettoIndividuale che si riferiscono ad un determinato assistito (RLPatientCittadino) e che contengono almeno una reference al profilo RLServiceRequestServiziSociosanitari relativo ai servizi sociosanitari di una determinata tipologia (es. C-DOM, RSA, ecc.).  |
|---|---|
|     VERB    |     GET    |
| BASE_APIMANAGER | {{link:Home-Contesto-API-RESTful}} , text:<base_API_Manager>}} |
| BASE_APISOURCE | <font style="color:red">endpoint FHIR SGDT</font> |
|     URL    | CarePlan?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale&activity.reference.code.coding.code=C-DOM&activity.reference.performer.identifier=\{_codiceLivelloL2_\}&activity.reference.identifier=\{_numeroPratica_\}&subject.identifier=\{_codiceFiscale_\}&_include=CarePlan:activity.reference&_include=CarePlan:subject |

A titolo esemplificativo, la chiamata: 

    CarePlan?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale&activity.reference.code.coding.code=C-DOM&activity.reference.performer.identifier=03014300&activity.reference.identifier=000001&subject.identifier=RSSMRA80A01F205X&_include=CarePlan:activity.reference&_include=CarePlan:subject

Restituirà lo storico dei progetti contenenti esclusivamente i dettagli del ricovero domiciliare dell’assistito con codice fiscale “RSSMRA80A01F205X”, afferente alla pratica numero "000001" della struttura con codice livello 2 "03014300". Il risultato della ricerca conterrà anche le informazioni inerenti al servizio sociosanitario attivo e al paziente stesso.

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- _include
- _lastUpdated
- _profile
- activity-reference
- status
- subject

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Attualmente non sono presenti value set nei campi del profilo RLCarePlanProgettoIndividuale.

<br> 
