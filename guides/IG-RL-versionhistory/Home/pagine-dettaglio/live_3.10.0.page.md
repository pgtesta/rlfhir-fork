# IG RLFHIR Live 3.10.0

Versione rilasciata il 03/07/2024. 

La guida è consultabile a questo [link](https://simplifier.net/guide/ig-rlfhir?version=3.10.0).

Questa versione della Implementation Guide fa riferimento agli elementi FHIR contenuti nel pacchetto [rl.fhir.r4 0.0.13](https://simplifier.net/packages/rl.fhir.r4/0.0.13).

## Novità
### Risorse FHIR

La versione corrente della guida implementativa, che fa riferimento all'ultimo rilascio in ambiente di <b>produzione</b>, gestisce i seguenti concetti:

- È stato descritto il nuovo scenario di cooperazione applicativa tra le Cartelle Elettroniche in uso dai Medici di Medicina Generale (CE-MMG) per la gestione dei pazienti cronici e il SGDT. Nella sezione Contesto sono state aggiornate le pagine.
  - Panoramica di progetto;
  - Tematiche di applicazione;
  - Paradigmi di integrazione e API RestFUL.
- Nella sezione Profili ed Estensioni sono stati aggiunti i profili RLMessageHeaderMMG, RLPatientBase, RLOperationOutcomeMMG, RLBundleMMG, RLBundleRispostaMMG e RLServiceRequestPrestazioni.
- Nel profilo RLOperationOutcome sono stati aggiornati i campi “issue.code” e “details.coding.code” e i value-set ad essi associati.
- Nel profilo RLConditionProblemiSalute è stato aggiunto il campo “severity”, è stato aggiornato il campo “code” ed è stata aggiornata la cardinalità del campo “meta”.
- Nel profilo RLMedicationRequestTerapiaFarmacologica è stato aggiunto il campo “text”, è stato aggiornato il campo “medication” ed è stata aggiornata la cardinalità del campo “meta” e “basedOn”.
- Nel profilo RLCarePlanProgettoIndividuale è stato aggiornato l’esempio della chiamata per la ricerca dei Progetti Individuali attivi.
- Nel profilo RLOrganizationL2 è stata aggiornata la descrizione e aggiunto il parametro “dataCessazione” per alcune tipologie di ricerca.
- Nel profilo RLGoalObiettiviSalute sono state aggiornate le descrizioni dei campi “description” e “note”.
- Nella sezione Terminologia sono stati aggiunti i seguenti value-set:
  - SGDT MessageEvents;
  - GPC LivelloGravita;
  - GPC ContenutoOperationOutcomeMMG;
  - SGDT operation error;
  - SGDT Tipologia Prestazione.
- Nella sezione Esempi sono stati aggiunti i seguenti esempi:
  - Esempio Bundle di attivazione dei servizi di presa in carico dei pazienti cronici da parte del MMG;
  - Esempio Bundle di richiesta di interventi di Assistenza Domiciliare Programmata da parte del MMG;
  - Esempio Bundle Risposta del messaggio con esito positivo;
  - Esempio Bundle Risposta del messaggio con errore.

### Implementation Guide
- Riviste e aggiornate le pagine di descrizione dei profili