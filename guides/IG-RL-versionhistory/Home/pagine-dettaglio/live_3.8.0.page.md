# IG RLFHIR Live 3.8.0

Versione rilasciata il 15/11/2023. 

La guida è consultabile a questo [link](https://simplifier.net/guide/ig-rlfhir?version=3.8.0).

Questa versione della Implementation Guide fa riferimento agli elementi FHIR contenuti nel pacchetto [rl.fhir.r4 0.0.9](https://simplifier.net/packages/rl.fhir.r4/0.0.9).

## Novità
### Risorse FHIR
- Sono state apportate le seguenti modifiche per il profilo RLCarePlanProgettoIndividuale o per i profili in esso referenziati: 
  - Sostituzione dei profili “RLConditionPatologiaPrimariaSecondariaUlteriore” e “RLConditionProblemaInfermieristico  con il profilo “RLConditionProblemiSalute”.
  - Il code-system “SGDT Prestazioni Infermieristiche” è stato spostato all’interno del value-set “Prestazioni".
  - Diventati facoltativi i seguenti campi: “contributor” in RLCarePlanProgettoIndividuale che corrisponde al case
    manager del progetto individuale, “author” in RLQuestionnaireResponseValutazione e “performer” in RLObservationEsitoValutazione che corrispondono al professionista sanitario che ha effettuato la valutazione, “organization” in RLPractitionerRoleMedicoPrescrittore, “addresses” e “note” in RLGoalObiettiviSalute.
  - Eliminato il campo “route” in RLMedicationRequestTerapiaFarmacologica.

- Sono stati revisionati i seguenti gli esempi ad una specifica tipologia di ricerca:
  - Ricerca prestazioni erogate;
  - Ricerca progetti individuali attivi;
  - Ricerca rivalutazioni e sospensioni;
  - Ricerca rivalutazioni;
  - Ricerca sospensioni;
  - Ricerca storico progetti individuali;
  - Ricerca valutazioni;
  - Ricerca enti erogatori accreditati nell’ambito territoriale di una ASST di una specifica tipologia.

- Nel value-set “SGDT Percorsi CDom” è stato aggiunto il valore “Liv III C autorizzato”.
  Nel value-set “SGDT Motivo Segnalazione” sono stati aggiunti i seguenti valori:
  - Inviato da PS
  - Presa in carico proattiva
  - Inviato da Enti locali
  - Inviato da IFEC
  - Inviato da Assistente Sociale
  - Inviato da Medico di distretto
  - Inviato da Ospedale
  - Inviato da COT
  - Inviato da Centro Servizi

### Implementation Guide
- Riviste e aggiornate le pagine di descrizione dei profili