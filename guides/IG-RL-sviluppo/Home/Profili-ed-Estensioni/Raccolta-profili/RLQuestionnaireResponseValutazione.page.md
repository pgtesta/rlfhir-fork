# RLQuestionnaireResponseValutazione

- [RLQuestionnaireResponseValutazione](#rlquestionnaireresponsevalutazione)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [Ultime valutazioni effettuate da un paziente](#ultime-valutazioni-effettuate-da-un-paziente)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLQuestionnaireResponseValutazione è stato strutturato a partire dalla risorsa generica FHIR [QuestionnaireResponse](http://hl7.org/fhir/R4/questionnaireresponse.html) per riportare il dettaglio delle risposte ai quesiti delle valutazioni dei bisogni alla quale un assistito è stato sottoposto.
Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione}}.
Inoltre, è possibile consultare le domande e le risposte delle valutazioni ""Scheda Triage"", ""Scheda semplificata SIAD"" e ""Campi extra del flusso SIAD"" con il rispettivo identificativo alla pagina Anagrafica delle schede di valutazione: {{pagelink: Home/Terminologia/Anagrafica-Schede-Valutazione.page.md}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
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

## Tipologie di ricerca

### Ultime valutazioni effettuate da un paziente

Questa ricerca deve essere utilizzata dagli Enti Erogatori di servizi socioassistenziali per recuperare la versione più aggiornata delle valutazioni effettuate da un paziente che ha attivo o sta attivando un determinato servizio socioassistenziale.
 I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	status: da compilare con il valore “completed” 
-	source.reference(RLPatientiCittadino).identifier: codice fiscale del paziente 
-	basedOn.reference(RLCarePlanProgettoIndividuale).activity.reference(RLServiceRequestServiziSocioSanitari).identifier: codice identificativo del servizio socioassistenziale d’interesse
-	basedOn.reference(RLCarePlanProgettoIndividuale).activity.reference(RLServiceRequestServiziSocioSanitari).perfomer.reference(RLOganizationL2).identifier: codice L2 dell’ente assegnato per l’erogazione del servizio socioassistenziale.

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

|     SCOPE    |Ultime valutazioni effettuate da un paziente|
|---|---|
| VERB | GET |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| URL | QuestionnaireResponse?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione<br>&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=\{_codiceLivello2_\}<br>&based-on:CarePlan.activity-reference:ServiceRequest.identifier=\{_numeroPratica_\}<br>&source:Patient.identifier=\{_codiceFiscaleAssistito_\}<br>&status=completed<br>&_include=QuestionnaireResponse:questionnaire<br>&_include=QuestionnaireResponse:extension.esitoValutazione |

A titolo esemplificativo, la chiamata: 

    QuestionnaireResponse?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione&based-on:CarePlan.activity-reference:ServiceRequest.performer:Organization.identifier=03014300&based-on:CarePlan.activity-reference:ServiceRequest.identifier=2022000001&source:Patient.identifier=RSSMRA80A01F205&status=completed&_include=QuestionnaireResponse:questionnaire&_include=QuestionnaireResponse:extension.esitoValutazione

Restituirà l’ultima versione della valutazione afferente alla pratica "2022000001", e la tipologia della stessa, effettuata al paziente con codice fiscale “RSSMRA80A01F205”.

Un esempio di Bundle di risposta può essere consultato qui: {{link:esempio-ricerca-valutazioni}}.

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.
<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Sulla base di quanto descritto nelle tipologie di ricerca sono riportati di seguito i parametri di ricerca del profilo  RLQuestionnaireResponseValutazione: 
- _include
- _profile
- based-on
- source
- status

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Attualmente non sono definiti value set specifici per il profilo RLQuestionnaireResponseValutazione. È possibile consultare le domande e le risposte delle valutazioni "Scheda Triage", "Scheda semplificata SIAD" e "Campi extra del flusso SIAD" con il rispettivo identificativo alla pagina Anagrafica delle schede di valutazione 		{{pagelink: Home/Terminologia/Anagrafica-Schede-Valutazione.page.md}}.
