# IG RLFHIR Draft 3.2.2-beta

Versione rilasciata il 09/03/2023. 

La guida è consultabile a questo [link](https://simplifier.net/guide/ig-rlfhir-draft?version=3.2.2-beta).

Questa versione della Implementation Guide fa riferimento agli elementi FHIR contenuti nel pacchetto [rl.fhir.r4.draft 0.0.6](https://simplifier.net/packages/rl.fhir.r4.draft/0.0.6).

## Novità
### Risorse FHIR
- modificato il valueset e codesystem "SGDT Percorsi CDom"
- modificati i profili elencatti di seguito. Tra le varie modifiche, si segnala l'aggiunta dei campi "id", "meta.versionId", "meta.lastUpdated", "meta.profile".
  - RLOrganizationL2, RLOrganizationL3, RLPractitionerRoleMedicoPrescrittore, RLPractitionerMedicoPrescrittore
  - RLAllergyIntoleranceAllergie, RLCarePlanProgettoIndividuale, RLCareTeamEquipe, RLConditionPatologiaPrimariaSecondariaUlteriore, RLConditionProblemaInfermieristico, RLCoverageEsenzioni, RLDeviceRequestProtesiAusili, RLEncounterAccesso, RLGoalObiettiviSalute, RLLocationLuogoPrestazioneCureDom, RLMedicationRequestOssigenoterapia, RLMedicationRequestTerapiaFarmacologica, RLObservationEsitoValutazione, RLObservationStiliVita, RLPatientCittadino, RLPractitionerRoleOperatoreADI, RLPractitionerRoleProfessionistaSanitario, RLPractitionerProfessionistaSanitario, RLProcedurePrestazione, RLQuestionnaireResponseValutazione, RLQuestionnaireValutazione, RLServiceRequestInterventoEducazionale, RLServiceRequestPrestazioniInfermieristiche, RLServiceRequestPrestazioniSociali, RLServiceRequestPrestazioniSpecialistiche, RLServiceRequestRivalutazione, RLServiceRequestServiziSocioAssistenziali, RLServiceRequestSospensioneADI
Aggiunte le extension: RLPractitionerRoleDettagliAttivazionePercorsoCure, RLPractitionerRoleNumeroAccessi, 

### Implementation Guide
- Non ci sono modifiche relative alla IG