# IG RLFHIR Draft 3.13.0

Versione rilasciata il 31/01/2024. 

La guida è consultabile a questo [link](https://simplifier.net/guide/ig-rlfhir-draft?version=3.13.0).

Questa versione della Implementation Guide fa riferimento agli elementi FHIR contenuti nel pacchetto [rl.fhir.r4 0.0.20](https://simplifier.net/packages/rl.fhir.r4.draft/0.0.20).

## Novità
### Risorse FHIR

La versione corrente della guida implementativa, che fa riferimento all'ultimo rilascio in ambiente di <b>produzione</b>, gestisce i seguenti concetti:

- Per il profilo “RLConditionProblemiSalute” è stato aggiunto il value-set “SGDT Patologie Non ICD9-CM” visualizzabile nella sezione “Libreria ValueSet”. Questa tabella raccoglie le patologie che presentano una codifica non standard differente dalla ICD9-CM.
- Nella sezione “Anagrafica delle schede di valutazione” è stata aggiunta la domanda “Contributo al caregiver familiare” per la valutazione “Campi extra del flusso SIAD”. Questa domanda viene valorizzata solo se la condizione clinica prevalente è “Paziente in Stato Vegetativo (DGR 6220)” o “Paziente affetto da malattie del motoneurone (circ. 20)”.
- Nella sezione “Stati ed Errori” è stato aggiunto l’errore “504 Service Time-Out”. Questo errore viene generato in caso in cui il tempo di composizione del bundle superi il limite temporale di soglia. Il sistema termina comunque la composizione e memorizza il bundle per un periodo limitato di tempo. Dunque, effettuando la stessa chiamata di consultazione la risposta risulta immediata. 


### Implementation Guide
- aggiornate le pagine "Libreria Profili", "Libreria Value Set" e "Libreria Esempi"