# RLQuestionnaireResponseValutazione

- [RLQuestionnaireResponseValutazione](#rlquestionnaireresponsevalutazione)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Ultime valutazioni effettuate da un paziente specifico](#ultime-valutazioni-effettuate-da-un-paziente-specifico)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione
Profilo declinato a partire dalla risorsa generica FHIR [QuestionnaireResponse](http://hl7.org/fhir/R4/questionnaireresponse.html) per il dettaglio delle risposte ai quesiti delle valutazioni dei bisogni alla quale il paziente è stato sottoposto.

La pagina Simplifier della risorsa è consultabile qui: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione, text: qui}}.

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

<!-- ===================================================FINE SESSIONE=================================================== -->

## Criteri di ricerca

### Ultime valutazioni effettuate da un paziente specifico

I parametri da valorizzare per effettuare la ricerca sono:
-	status: da compilare con il valore “completed” 
-	source.reference(RLPatientiCittadino).identifier: da compilare con il codice fiscale del paziente 
-	basedOn.reference(RLCarePlanProgettoIndividuale).activity.reference(RLServiceRequestServiziSocioSanitari).type.coding.code: da compilare con il valore “C-DOM”
-	basedOn.reference(RLCarePlanProgettoIndividuale).activity.reference(RLServiceRequestServiziSocioSanitari).perfomer.reference(RLOganizationL2).identifier: codice L2 dell’ente assegnato per l’erogazione del servizio di cure domiciliari.

L’esito della ricerca permette di recuperare l’ultima versione delle valutazioni a cui un paziente specifico assegnato ad un determinato ente erogatore di cure domiciliari è stato sottoposto.

|     SCOPE    |Ricerca tutti i profili RLQuestionnaireResponseValutazione in stato completato che si riferiscono ad un determinato paziente (RLPatientCittadino)|
|---|---|
| VERB | GET |
| BASE | https://api.servizirl.it/c/operatori.siss/\[ambitoTBD\]/v1.0.0/\[servizioTBD\]/\[fhir_resource_name\] |
| URL | QuestionnaireResponse?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione&based-on.activity-reference.code=C-DOM&based-on.activity-reference.performer.identifier=\{_codiceLivello2_\}&source.identifier=\{_codiceFiscaleAssistito_\}&status=completed&_include=QuestionnaireResponse:questionna |

A titolo esemplificativo, la chiamata: 

    QuestionnaireResponse?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione&based-on.activity-reference.code=C-DOM&based-on.activity-reference.performer.identifier=03014300&source.identifier=RSSMRA80A01F205X&status=completed&_include=QuestionnaireResponse:questionnaire

Restituirà l’ultima versione della valutazione, e la tipologia della stessa, effettuata al paziente con codice fiscale “RSSMRA80A01F205”.


<!-- ===================================================FINE SESSIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre quelli previsti dallo standard per la risorsa QuestionnaireResponse.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Value set

Attualmente non sono definiti value set specifici per il profilo RLQuestionnaireResponseValutazione.