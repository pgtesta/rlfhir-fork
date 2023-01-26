# RLCarePlanProgettoIndividuale

- [RLCarePlanProgettoIndividuale](#rlcareplanprogettoindividuale)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Progetti individuali attivi contenenti esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato a un determinato ente erogatore](#progetti-individuali-attivi-contenenti-esclusivamente-i-dettagli-dellattivazione-di-un-servizio-sociosanitario-affidato-a-un-determinato-ente-erogatore)
    - [Progetto individuale attivo di un paziente contenente esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato a un determinato ente erogatore](#progetto-individuale-attivo-di-un-paziente-contenente-esclusivamente-i-dettagli-dellattivazione-di-un-servizio-sociosanitario-affidato-a-un-determinato-ente-erogatore)
  - [Seacrh parameter](#seacrh-parameter)
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


## Extension
Di seguito la descrizione delle extension inerenti al profilo RLCarePlanProgettoIndividuale:

| Nome   Extension e link Simplifier | Nome campo esteso | Descrizione | Contesto |
|---|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanVersionePAI}} | VersionePAI | Versione del progetto individuale | CarePlan |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanEsenzioni}} | Esenzioni | Esenzioni relative al cittadino | CarePlan |

<!-- ===================================================FINE SEZIONE=================================================== -->

## Criteri di ricerca

Di seguito la descrizione dei criteri di ricerca inerenti al profilo RLCarePlanProgettoIndividuale.

###	Progetti individuali attivi contenenti esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato a un determinato ente erogatore
Esiste sempre un'unica versione del progetto individuale in stato “attivo” e quindi in corso di validità. 
I parametri da valorizzare per effettuare la ricerca sono:
- status
- activity.reference(RLServiceRequestServiziSocioAssistenziali).code
- activity.reference(RLServiceRequestServiziSocioAssistenziali).performer

L’esito della ricerca permette di recuperare le informazioni relative ai progetti individuali attivi dei cittadini per i quali è stata prevista l’attivazione di un servizio sociosanitario (profilo _RLServiceRequestServiziSocioAssistenziali_) di una determinata tipologia di UdO sociosanitaria e per il quali è stato individuato l’ente erogatore (profilo _RLOrganizationL2_) responsabile della presa in carico.

|     SCOPE    |    Ricerca tutti i CarePlan in stato attivo che contengono almeno una ServiceRequest relativa ai servizi sociosanitari di una determinata tipologia (es. CDOM, RSA, ecc.) e per il quale è stato individuato l’ente erogatore del servizio.     |
|---|---|
|     VERB    |     GET    |
|     BASE    |          |
|     URL    |          |

A titolo esemplificativo, la chiamata: 

    CarePlan?_profile=https://example.org/fhir/StructureDefinition/ 

Restituirà..

### Progetto individuale attivo di un paziente contenente esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato a un determinato ente erogatore
Esiste sempre un'unica versione del progetto individuale in stato “attivo” e quindi in corso di validità. 
I parametri da valorizzare per effettuare la ricerca sono:
- status
- activity.reference(RLServiceRequestServiziSocioAssistenziali).code
- activity.reference(RLServiceRequestServiziSocioAssistenziali).performer
- activity.reference(RLPatientCittadino).identifier

L’esito della ricerca permette di recuperare le informazioni relative al progetto individuale atttivo di un cittadino per il quale è prevista l’attivazione di un servizio sociosanitario (profilo _RLServiceRequestServiziSocioAssistenziali_) di una determinata tipologia di UdO sociosanitaria e per il quale è stato individuato l’ente erogatore (profilo _RLOrganizationL2_) responsabile della presa in carico.

|     SCOPE    |     Ricerca iltutti i CarePlan in stato attivo relativo ad un determinato cittadino che   contieneengono almeno una ServiceRequest   relativa ai servizi sociosanitari di una determinata tipologia (es. CDOM,   RSA, ecc.) e per il quale è stato individuato l’ente erogatore del servizio.     |
|---|---|
|     VERB    |     GET    |
|     BASE    |          |
|     URL    |          |

A titolo esemplificativo, la chiamata:

  CarePlan?_profile=https%3A//example.org/fhir/StructureDefinition/ 

Restituirà..

<!-- ===================================================FINE SEZIONE=================================================== -->

## Seacrh parameter

Attualmente non sono definiti Search Parameters oltre ai campi standard della risorsa CarePlan.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Value set

Attualmente non sono presenti value set nei campi del profilo RLCarePlanProgettoIndividuale.

<br>
