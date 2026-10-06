# IG RLFHIR Draft 3.11.0

Versione rilasciata il 27/10/2023. 

La guida è consultabile a questo [link](https://simplifier.net/guide/ig-rlfhir-draft?version=3.11.0).

Questa versione della Implementation Guide fa riferimento agli elementi FHIR contenuti nel pacchetto [rl.fhir.r4 0.0.17](https://simplifier.net/packages/rl.fhir.r4.draft/0.0.17).

## Novità
### Risorse FHIR

- Nel profilo RLPatientCittadino sono stati aggiunti i campi relativi ai contatti del paziente, al caregiver e alla locazione temporanea.
- Nel profilo RLGoalObiettiviSalute è stato aggiunto il campo “category” per indicare l’ambito degli obiettivi di salute con la relativa nuova codifica
- Nel profilo RLServiceRequestServiziSocioAssistenziali è stato aggiunto il campo extension medicoPrescrittore che verrà valorizzato con il codice regionale del medico,  mentre nel campo “requisition” è stato aggiunto il codice della ricetta medica e la sua data di decorrenza.
- Nel profilo RLProcedurePrestazione sono stati resi obbligatori i campi extension dataPresaInCarico, numeroAccesso, modalitaErogazione, tipoAccesso.
- Nel profilo RLQuestionnaireResponseValutazione è stato aggiunto un codice identificativo alle risposte di tutte le domande delle valutazioni eccetto per la valutazione InterRAI HomeCare.
- Nel value-set “SGDT Percorsi CDom” è stato aggiunto il percorso “Trattamenti Terapeutici” e sono stati modificati alcuni codici dei percorsi.
- Sono stati revisionati gli esempi per allinearli alle nuove modifiche.
  

### Implementation Guide
- aggiornate le pagine "Libreria Profili", "Libreria Value Set" e "Libreria Esempi"