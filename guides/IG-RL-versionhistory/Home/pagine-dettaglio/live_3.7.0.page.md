# IG RLFHIR Live 3.7.0

Versione rilasciata il 27/10/2023. 

La guida è consultabile a questo [link](https://simplifier.net/guide/ig-rlfhir?version=3.7.0).

Questa versione della Implementation Guide fa riferimento agli elementi FHIR contenuti nel pacchetto [rl.fhir.r4 0.0.8](https://simplifier.net/packages/rl.fhir.r4/0.0.8).

## Novità
### Risorse FHIR

- È stata aggiunta una nuova valutazione denominata "Campi extra del flusso SIAD" relativa alle informazioni presenti nel flusso SIAD che non appartengono alla scheda SIAD semplificata.
- Nel profilo RLPatientCittadino sono stati aggiunti i campi relativi ai contatti del paziente, al caregiver e alla locazione temporanea.
- Nel profilo RLGoalObiettiviSalute è stato aggiunto il campo “category” per indicare l’ambito degli obiettivi di salute con la relativa nuova codifica
- Nel profilo RLServiceRequestServiziSocioAssistenziali è stato aggiunto il campo extension medicoPrescrittore che verrà valorizzato con il codice regionale del medico,  mentre nel campo “requisition” è stato aggiunto il codice della ricetta medica e la sua data di decorrenza.
- Nel profilo RLProcedurePrestazione sono stati resi obbligatori i campi extension dataPresaInCarico, numeroAccesso, modalitaErogazione, tipoAccesso.
- Nel profilo RLQuestionnaireResponseValutazione è stato aggiunto un codice identificativo alle risposte di tutte le domande delle valutazioni eccetto per la valutazione InterRAI HomeCare.
- Nel value-set “SGDT Percorsi CDom” è stato aggiunto il percorso “Trattamenti Terapeutici” e sono stati modificati alcuni codici dei percorsi.
- Nel value-set “SGDT Motivo Segnalazione” è stato cambiato il testo di alcune voci. 
- Nel value-set “SGDT Valutazione” è stata aggiunta la valutazione “Campi extra del flusso SIAD”.
- È stato revisionato l’esempio “Ricerca rivalutazioni e sospensioni” aggiungendo il campo “system” nel campo “identifier” dei profili “RLServiceRequestSospensioneADI” e “RLServiceRequestRivalutazione”.
- Aggiornati esempi
  

### Implementation Guide
- Riviste e aggiornate le pagine di descrizione dei profili