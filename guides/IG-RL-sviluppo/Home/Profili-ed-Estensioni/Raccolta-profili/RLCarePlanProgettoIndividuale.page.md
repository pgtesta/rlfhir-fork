# RLCarePlanProgettoIndividuale

- [RLCarePlanProgettoIndividuale](#rlcareplanprogettoindividuale)
  - [Descrizione](#descrizione)
  - [Extension](#extension)
  - [Criteri di ricerca](#criteri-di-ricerca)
    - [Progetto individuale contenente i dettagli dell’attivazione di un servizio sociosanitario da un determinato ente erogatore](#progetto-individuale-contenente-i-dettagli-dellattivazione-di-un-servizio-sociosanitario-da-un-determinato-ente-erogatore)
  - [Seacrh parameter](#seacrh-parameter)
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

<table>
  <thead>
    <tr>
      <th>Nome Extension e link Simplifier</th>
      <th>Nome campo esteso</th>
      <th>Descrizione</th>
      <th>Contesto</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
	  {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanVersionePAI}}
      </td>
      <td>VersionePAI</td>
      <td>Versione del progetto individuale</td>
      <td>CarePlan</td>
    </tr>
  </tbody>
</table>


<!-- ===================================================FINE SESSIONE=================================================== -->

## Criteri di ricerca

Di seguito la descrizione dei criteri di ricerca inerenti al profilo RLCarePlanProgettoIndividuale.

###	Progetto individuale contenente i dettagli dell’attivazione di un servizio sociosanitario da un determinato ente erogatore

Parametri di ricerca:
- activity.reference(RLServiceRequestServiziSociosanitari).code
- activity.reference(RLServiceRequestServiziSociosanitari).performer

L’esito della ricerca permette di recuperare le informazioni relative al progetto individuale di un cittadino per il quale è stato previsto l’attivazione di un servizio sociosanitario (profilo RLServiceRequestServiziSociosanitari) di una determinata tipologia di unità d’offerta (UdO) sociosanitaria e per il quale è stato individuato l’ente erogatore (profilo RLOrganizationL2).

|     SCOPE    |     Ricerca tutti i CarePlan   che contengono almeno una ServiceRequest relativa ai servizi sociosanitari di   una determinata tipologia (es. C-DOM, RSA, ecc.) e per il quale è stato individuato   l’ente erogatore del servizio.     |
|---|---|
|     VERB    |     GET    |
|     BASE    |          |
|     URL    |          |

A titolo esemplificativo, la chiamata: 

    CarePlan?_profile=https://example.org/fhir/StructureDefinition/ 

Restituirà..

<!-- ===================================================FINE SESSIONE=================================================== -->

## Seacrh parameter

Attualmente non sono definiti Search Parameters oltre ai campi standard della risorsa CarePlan.

<!-- ===================================================FINE SESSIONE=================================================== -->

## Value set

Attualmente non sono presenti value set nei campi del profilo

<br>
