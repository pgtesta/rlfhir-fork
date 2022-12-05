# RLCarePlanProgettoIndividuale

- [RLCarePlanProgettoIndividuale](#rlcareplanprogettoindividuale)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Progetti individuali attivi contenenti esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato a un determinato ente erogatore](#progetti-individuali-attivi-contenenti-esclusivamente-i-dettagli-dellattivazione-di-un-servizio-sociosanitario-affidato-a-un-determinato-ente-erogatore)
    - [Progetto individuale attivo di un paziente contenente esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato a un determinato ente erogatore](#progetto-individuale-attivo-di-un-paziente-contenente-esclusivamente-i-dettagli-dellattivazione-di-un-servizio-sociosanitario-affidato-a-un-determinato-ente-erogatore)
  - [Search parameter](#search-parameter)
  - [Value set](#value-set)


## Descrizione

Profilo declinato a partire dalla risorsa generica FHIR [CarePlan](http://hl7.org/fhir/R4/careplan.html) per descrivere il progetto individuale di un cittadino. All’interno del profilo sono contenute informazioni generali quali: durata del progetto, obiettivi di salute, case manager, esiti delle valutazioni, patologie principali, secondarie e addizionali, allergie, esenzioni e stili di vita del cittadino; così come le attività di natura clinica, infermieristica e sociale che compongono il progetto. 

La pagina Simplifier della risorsa è consultabile qui: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, text: qui}}.

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

<!-- ===================================================FINE SESSIONE=================================================== -->


## Extension
Di seguito la descrizione delle extension inerenti al profilo RLCarePlanProgettoIndividuale:

| Nome   Extension e link Simplifier | Nome campo esteso | Descrizione | Contesto |
|---|---|---|---|
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanVersionePAI}} | VersionePAI | Versione del progetto individuale | CarePlan |
| {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanEsenzioni}} | Esenzioni | Esenzioni relative al cittadino | CarePlan |

<!-- ===================================================FINE SESSIONE=================================================== -->

## Criteri di ricerca

Di seguito la descrizione dei criteri di ricerca inerenti al profilo RLCarePlanProgettoIndividuale.

###	Progetti individuali attivi contenenti esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato a un determinato ente erogatore
Esiste sempre un'unica versione del progetto individuale in stato “attivo” e quindi in corso di validità. 
I parametri da valorizzare per effettuare la ricerca sono:
-	status: da compilare con il valore “active”
-	activity.reference(RLServiceRequestServiziSociosanitari).code.coding.code: codice del servizio sociosanitario d’interesse
-	activity.reference(RLServiceRequestServiziSociosanitari).performer: codice L2 dell’ente erogatore di interesse
-	lastUpdated: data e ora dell’ultimo aggiornamento dei dati 

L’esito della ricerca permette di recuperare le informazioni relative ai progetti individuali attivi dei cittadini per i quali è stata prevista l’attivazione di un servizio sociosanitario di una determinata tipologia di UdO sociosanitaria e per il quali è stato assegnato un determinato ente erogatore responsabile della presa in carico.

|     SCOPE    |    Ricerca tutti i profili RLCarePlanProgettoIndividuale in stato attivo che contengono almeno una reference al profilo RLServiceRequestServiziSociosanitari relativa ai servizi sociosanitari di una determinata tipologia (es. C-DOM, RSA, ecc.) e per il quale è stato individuato l’ente erogatore del servizio (RLOrganizationL2). |
|---|---|
|     VERB    |     GET    |
|     BASE    |          |
|     URL    |          |

A titolo esemplificativo, la chiamata: 

    CarePlan?_profile=https://example.org/fhir/StructureDefinition/ 

Restituirà..

### Progetto individuale attivo di un paziente contenente esclusivamente i dettagli dell’attivazione di un servizio sociosanitario affidato a un determinato ente erogatore
Questo criterio di ricerca permette di fruire dello storico dei progetti individuali con il dettaglio dell’attivazione di uno specifico servizio sociosanitario assegnato ad un ente erogatore per un determinato paziente 
I parametri da valorizzare per effettuare la ricerca sono:
-	activity.reference(RLServiceRequestServiziSociosanitari).code coding.code: codice del servizio sociosanitario d’interesse
-	activity.reference(RLServiceRequestServiziSociosanitari).performer: codice L2 dell’ente erogatore di interesse
-	subject.reference(RLPatientCittadino).identifier: da compilare con il codice fiscale del paziente
L’esito della ricerca permette di recuperare le informazioni relative ai progetti individuali redatti a un cittadino per i quale è stata prevista l’attivazione di un servizio sociosanitario di una determinata tipologia di UdO sociosanitaria e per il quali è stato assegnato l’ente erogatore responsabile della presa in carico.


|     SCOPE    |Ricerca tutti i profili RLCarePlanProgettoIndividuale che contengono almeno una reference al profilo RLServiceRequestServiziSociosanitari relativo ai servizi sociosanitari di una determinata tipologia (es. C-DOM, RSA, ecc.) e per il quale è stato individuato l’ente erogatore del servizio (profilo RLOrganizationL2). |
|---|---|
|     VERB    |     GET    |
|     BASE    |          |
|     URL    |          |

A titolo esemplificativo, la chiamata:

  CarePlan?_profile=https%3A//example.org/fhir/StructureDefinition/ 

Restituirà..

<!-- ===================================================FINE SESSIONE=================================================== -->

## Search parameter

Attualmente non sono definiti Search Parameters oltre ai campi standard della risorsa CarePlan.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Value set

Attualmente non sono presenti value set nei campi del profilo RLCarePlanProgettoIndividuale.

<br> 
