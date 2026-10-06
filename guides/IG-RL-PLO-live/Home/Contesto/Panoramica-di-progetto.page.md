# {{page-title}}

In ottica di standardizzazione ed interoperabilità dei dati, così come già previsto per il Fascicolo Sanitario Nazionale 2.0, Regione Lombardia ha adottato lo standard FHIR come best practice di scambio, gestione e consultazione dei dati funzionali alla presa in carico territoriale del cittadino ed alla gestione della sanità territoriale e di prossimità.

Lo standard FHIR è basato su un criterio di interrogazione dei dati definito da API RESTful in logica PULL attraverso la definizione di parametri di ricerca. 

Nel proseguo del documento verranno descritti tutti i criteri di ricerca attuabili alle risorse attualmente definite.

Lo scopo del caso d’uso è ottenere i dati relativi all’occupazione dei posti letto dei pazienti assistiti dalle strutture sociosanitarie in Regione Lombardia, in un’ottica di standardizzazione per la gestione, lo scambio e la consultazione dei dati.

In questo paragrafo sono introdotti i principali requisiti funzionali dell'interfaccia FHIR definita per recuperare i dati relativi ai posti letto occupati. In particolare, le principali informazioni raccolte sono relative a: 
* struttura di ricovero, 
* reparto fisico e clinico,
* area di degenza, 
* stanza, piano e edificio, 
* posto letto, 
* regime di ricovero,
* data di dimissione prevista,
* dimissione protetta.

Per il caso d'uso è stata definita una raccolta di profili FHIR che sono consultabili nella pagina *Profili ed Estensioni - Libreria Profili* utilizzando come TAG di ricerca *PLO*.

Gli applicativi degli enti ospedalieri esporranno i dati in modalità API FHIR RESTful e la sintassi della chiamata e della risposta sarà di tipo JSON. 

Deve essere esposta l'API relativa al dettaglio delle informazioni sulla locazione e sulle caratteristiche di ricovero del posto letto occupato. 
La risorsa FHIR da esporre è Location e segue le specifiche definite dal profilo *RLLocationPLOLetto*, consultabile nella pagina *Profili ed Estensioni - Libreria Profili*.


Per ulteriori dettagli tecnici riguardo l'endpoint e le API da esporre si rimanda alla pagina *Contesto - API RESTful*. 

## Glossario
Raccolta di acronimi e termini usati nel progetto:
 
| Voce | Descrizione |
|---|---|
| DDC | Distribuzione Dati Codificati |
| DP | Dimissione Protette |
| PI | Progetto Individuale (Piano Assistenziale Individuale) |
| RSA | Residenza Sanitaria Assistenziale |
| PLO | Numero Posti Occupati |
| L1 | Codice   identificativo di livello 1 degli enti aderenti al progetto SISS. La risorsa   FHIR che descrive questa tipologia di struttura è _RLOrganizationL1_ |
| L2 | Codice identificativo di livello 2 degli Enti Erogatori di servizi socioassistenziali. La risorsa FHIR che descrive questa tipologia di struttura è _RLOrganizationL2_. |
| Posti abilitati | Capacità ricettiva in termini di posti letto conformi ai requisiti generali e specifici di esercizio previsti dalla normativa che l’azienda sociosanitaria può occupare per erogare servizi e prestazioni al paziente. |
| Posti accreditati | Capacità ricettiva in termini di posti letto conformi ai requisiti di accreditamento regionali, oltre i requisiti minimi abilitanti, che l’azienda sociosanitaria garantisce al servizio sanitario regionale per i servizi e prestazioni ai pazienti. Il numero di posti letto accreditati è minore o uguale al numero di posti letto abilitati. |
| Posti a contratto | Capacità ricettiva in termini di posti letto conformi ai requisiti di accreditamento regionali, oltre i requisiti minimi abilitanti, che l’azienda sociosanitaria garantisce in forza di contratti in essere con il servizio sanitario regionale per l’erogazione di servizi e prestazioni. Il numero di posti letto a contratto è minore o uguale al numero di posti letto accreditati. |