# RLQuestionnaireResponseValutazione

- [RLQuestionnaireResponseValutazione](#rlquestionnaireresponsevalutazione)
  - [Descrizione](#descrizione)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Ultime valutazioni effettuate da un paziente](#ultime-valutazioni-effettuate-da-un-paziente)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione
Profilo declinato a partire dalla risorsa generica FHIR [QuestionnaireResponse](http://hl7.org/fhir/R4/questionnaireresponse.html) per il dettaglio delle risposte ai quesiti delle valutazioni dei bisogni alla quale il paziente è stato sottoposto.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, text: qui}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, diff}}
</div>

<div id="Hybrid View" class="tabcontent">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Al momento non ci sono esempi disponibili. 
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

### Ultime valutazioni effettuate da un paziente

Questa ricerca deve essere effettuata dagli Enti Erogatori di servizi sociosanitari per recuperare la versione più aggiornata delle valutazioni effettuate da un paziente specifico.

I parametri da valorizzare per effettuare la ricerca sono:
-	status: da compilare con il valore “completed” 
-	source.reference(RLPatientiCittadino).identifier: codice fiscale del paziente 
-	basedOn.reference(RLCarePlanProgettoIndividuale).activity.reference(RLServiceRequestServiziSocioAssistenziali).identifier: codice identificativo del servizio sociosanitario d’interesse
-	basedOn.reference(RLCarePlanProgettoIndividuale).activity.reference(RLServiceRequestServiziSocioAssistenziali).perfomer.reference(RLOganizationL2).identifier: codice L2 dell’ente assegnato per l’erogazione del servizio sociosanitario.


|     SCOPE    |Ricerca tutti i profili RLQuestionnaireResponseValutazione in stato completato che si riferiscono ad un determinato paziente (RLPatientCittadino)|
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| BASE_APISOURCE | <font style="color:red">endpoint FHIR SGDT</font> |
| URL | QuestionnaireResponse?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione&basedOn.activity.reference.code.coding.code=CDOM&basedOn.activity.reference.performer.identifier=\{_codiceLivello2_\}&basedOn.activity.reference.identifier=\{_numeroPratica_\}&source.identifier=\{_codiceFiscaleAssistito_\}&status=completed&_include=QuestionnaireResponse:questionnaire&_include=QuestionnaireResponse:extension.esitoValutazione |

A titolo esemplificativo, la chiamata: 

    QuestionnaireResponse?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione&basedOn:CarePlan.activity.reference.code.coding.code=CDOM&basedOn:CarePlan.activity.reference.performer.identifier=03014300&basedOn.activity.reference.identifier=000001&source.identifier=RSSMRA80A01F205&status=completed&_include=QuestionnaireResponse:questionnaire&_include=QuestionnaireResponse:extension.esitoValutazione

Restituirà l’ultima versione della valutazione afferente alla pratica "000001", e la tipologia della stessa, effettuata al paziente con codice fiscale “RSSMRA80A01F205”.

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.
<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Per questo profilo sono utilizzati i seguenti parametri di ricerca previsti dallo standard: 
- _include
- _profile
- based-on
- source
- status

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Attualmente non sono definiti value set specifici per il profilo RLQuestionnaireResponseValutazione.