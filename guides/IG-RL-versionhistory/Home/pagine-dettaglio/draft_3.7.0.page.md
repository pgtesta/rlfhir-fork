# IG RLFHIR Draft 3.7.0

Versione rilasciata il 31/05/2023. 

La guida è consultabile a questo [link](https://simplifier.net/guide/ig-rlfhir-draft?version=3.7.0).

Questa versione della Implementation Guide fa riferimento agli elementi FHIR contenuti nel pacchetto [rl.fhir.r4 0.0.12](https://simplifier.net/packages/rl.fhir.r4.draft/0.0.12).

## Novità
### Risorse FHIR

- Modificato profilo RLMedicationRequestTerapiaFarmacologica, RLPatientCittadino, RLCarePlanProgettoIndividuale,
  RLGoalObiettiviSalute, RLMedicationRequestTerapiaFarmacologica, RLProcedurePrestazione, RLServiceRequestPrestazioniInfermieristiche;
- Rinominato profilo RLConditionPatologiaPrimariaSecondariaUlteriore in RLPatologiaRLConditionProblemiSalute;
- Eliminato profilo  RLConditionProblemaInfermieristico;
- Cancellato il valueSet SGDT-PrestazioniInfermieristiche, codesystem incluso nel valueset Prestazione;
- Rinominato ValueSet e CodeSystem da TipologiaPaziente in CondizioneClinica;
- Rinominato valueset da SGDT-TipologiaPatologia a SGDT-TipologiaProblemaSalute;
- Modificata pagina ConditionProblemiSalute IG;
  

### Implementation Guide
- aggiornate le pagine "Libreria Profili", "Libreria Value Set" e "Libreria Esempi"