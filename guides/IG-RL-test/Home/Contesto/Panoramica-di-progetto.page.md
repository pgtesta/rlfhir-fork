# {{page-title}}

In ottica di standardizzazione ed interoperabilità dei dati, così come già previsto per il Fascicolo Sanitario Nazionale 2.0, Regione Lombardia ha adottato lo standard FHIR come best practice di scambio, gestione e consultazione dei dati funzionali alla presa in carico territoriale del cittadino ed alla gestione della sanità territoriale e di prossimità.

Lo standard FHIR è basato su un criterio di interrogazione dei dati definito da API RESTful in logica PULL attraverso la definizione di parametri di ricerca. 

Nel proseguo del documento verranno descritti tutti i criteri di ricerca attuabili alle risorse attualmente definite.

## Glossario
Raccolta di acronimi e termini usati nel progetto:
 
| Voce | Descrizione |
|---|---|
| DDC | Distribuzione Dati Codificati |
| UDO | Unità d'Offerta |
| DP | Dimissione Protette |
| PAI | Piano Assistenziale Individuale |
| RSA | Residenza Sanitaria Assistenziale |
| PLO | Numero Posti Occupati |
| L1 | Codice   identificativo di livello 1 degli enti aderenti al progetto SISS. La risorsa   FHIR che descrive questa tipologia di struttura è RLOrganizationL1 |
| L2 | Codice   identificativo di livello 2 delle strutture di tipo UdO. La risorsa FHIR che   descrive questa tipologia di struttura è RLOrganizationL2. |
| UdO | Strutture   presenti nella rete territoriale che rendono disponibili servizi   sociosanitari e assistenziali. |
| Posti abilitati | Capacità ricettiva in termini di posti letto conformi ai requisiti generali e specifici di esercizio previsti dalla normativa che l’azienda sociosanitaria può occupare per erogare servizi e prestazioni al paziente. |
| Posti accreditati | Capacità ricettiva in termini di posti letto conformi ai requisiti di accreditamento regionali, oltre i requisiti minimi abilitanti, che l’azienda sociosanitaria garantisce al servizio sanitario regionale per i servizi e prestazioni ai pazienti. Il numero di posti letto accreditati è minore o uguale al numero di posti letto abilitati. |
| Posti a contratto | Capacità ricettiva in termini di posti letto conformi ai requisiti di accreditamento regionali, oltre i requisiti minimi abilitanti, che l’azienda sociosanitaria garantisce in forza di contratti in essere con il servizio sanitario regionale per l’erogazione di servizi e prestazioni. Il numero di posti letto a contratto è minore o uguale al numero di posti letto accreditati. |