## {{page-title}}

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

<br>
