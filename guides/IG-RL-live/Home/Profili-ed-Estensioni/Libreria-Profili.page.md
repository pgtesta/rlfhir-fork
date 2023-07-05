<html>
  <head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <script>
      $(document).ready(function () {
        $("#myInput").on("keyup", function () {
          var value = $(this).val().toLowerCase();
          $("#myTable tr").filter(function () {
            $(this).toggle($(this).text().toLowerCase().indexOf(value) > -1);
          });
        });
      });
    </script>
  </head>
  <body>
    <h1>Raccolta profili in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti tutti i profili attivi; ad ogni
        profilo è associato un tema di utilizzo (si veda la pagina
        {{pagelink:Home/Contesto/Panoramica-di-progetto.page.md}}).
        <br />
        Usare la casella di ricerca sottostante per filtrare le informazioni
        desiderate.
      </p>
      <input id="myInput" type="text" placeholder="Cerca.." />
    </div>
    <br />
    <table style="width: fit-content">
      <thead>
        <tr>
          <th>Tag</th>
          <th>Nome profilo e pagina di dettaglio</th>
          <th>Risorsa base</th>
          <th>Descrizione</th>
          <th>Link Simplifier</th>
        </tr>
      </thead>
      <tbody id="myTable">
        <tr>
          <td>C-DOM</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleOperatoreADI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/practitionerrole.html">PractitionerRole</a>
          </td>
          <td>Profilo contentente le tipologie di operatori ADI</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleOperatoreADI}}
          </td>
        </tr>
        <tr>
          <td>C-DOM</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestRivalutazione.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo volto a notificare la necessità di una
            rivalutazione di un paziente in ricovero domiciliare
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione}}
          </td>
        </tr>
        <tr>
          <td>C-DOM</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestSospensioneADI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo che descrive i dettagli della sospensione
            temporanea del ricovero domiciliare di un paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSospensioneADI}}
          </td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo che descrive una struttura o un ente
            identificato univocamente da un codice di ente L1
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1}}
          </td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo che descrive una struttura o un ente
            identificato univocamente da un codice di ente L2
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2}}
          </td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL3.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo che descrive un reparto appartenente ad una
            struttura di ricovero identificata da un codice L2
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3}}
          </td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerMedicoPrescrittore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/practitioner.html">Practitioner</a>
          </td>
          <td>
            Profilo che contiene l’anagrafica dei medici
            prescrittori della Regione Lombardia destinatari di
            ricettari RUR.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerMedicoPrescrittore}}
          </td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleMedicoPrescrittore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/practitionerrole.html">PractitionerRole</a>
          </td>
          <td>
            Risorsa che raccoglie i ruoli e le qualifiche di
            un determinato medico prescrittore
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleMedicoPrescrittore}}
          </td>
        </tr>
        <tr>
          <td>Errori</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLBundleNotificaErrori.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/bundle.html">Bundle</a>
          </td>
          <td>
            Profilo volto a contenere le informazioni utili a
            tener traccia delle risorse che falliscono i controlli
            di coerenza.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLBundleNotificaErrori}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLAllergyIntoleranceAllergie.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/allergyintolerance.html">AllergyIntolerance</a>
          </td>
          <td>
            Profilo volto a descrivere le allergie di cui il paziente
            è affetto.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntoleranceAllergie}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanProgettoIndividuale.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/careplan.html">CarePlan</a>
          </td>
          <td>
            Profilo contenente tutte le attività e le
            informazioni definite in un progetto individuale di un
            cittadino redatto sul Sistema di Gestione Digitale del
            Territorio.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCareTeamEquipe.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/careteam.html">CareTeam</a>
          </td>
          <td>Profilo volto a definire un equipe di professionisti sanitari</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCareTeamEquipe}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionProblemiSalute.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/condition.html">Condition</a>
          </td>
          <td>
            Profilo volto a descrivere i problemi di salute 
            dei quali un paziente è affetto.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionProblemiSalute}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCoverageEsenzioni.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/coverage.html">Coverage</a>
          </td>
          <td>
            Profilo volto a descrivere le esenzioni di cui il
            paziente beneficia
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoverageEsenzioni}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLDeviceRequestProtesiAusili.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/devicerequest.html">DeviceRequest</a>
          </td>
          <td>
            Profilo volto a descrivere la prostesi o l’ausilio di cui
            il paziente necessita come definito dal suo progetto
            individuale.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestProtesiAusili}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLEncounterAccesso.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/encounter.html">Encounter</a>
          </td>
          <td>
            Profilo volto a descrivere i dettagli dell’accesso
            del cittadino alla struttura di prossimità.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterAccesso}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLGoalObiettiviSalute.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/goal.html">Goal</a>
          </td>
          <td>
            Profilo volto a descrivere gli obbiettivi di salute che
            il paziente deve traguardare sulla base delle attività
            previste dal progetto individuale (PI).
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLGoalObiettiviSalute}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationLuogoPrestazioneCureDom.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo contenente il dettaglio della tipologia del luogo
            in cui viene erogata una prestazione al paziente in
            regime di ricovero domiciliare.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationLuogoPrestazioneCureDom}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestOssigenoterapia.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
          </td>
          <td>
            Profilo volto a contenere le indicazioni
            riguardo un’ossigenoterapia prescritta al cittadino
            all’interno del suo progetto individuale.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestOssigenoterapia}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestTerapiaFarmacologica.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
          </td>
          <td>
            Profilo volto a contenere le indicazioni riguardo una
            terapia farmacologica prescritta al cittadino
            all’interno del suo progetto individuale.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestTerapiaFarmacologica}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMessageHeaderControlloCoerenza.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/messageheader.html">MessageHeader</a>
          </td>
          <td>
            Profilo volto a notificare all'ente chiamato la presenza
            di errori di coerenza dei dati inviati.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMessageHeaderControlloCoerenza}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationEsitoValutazione.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo volto a descrivere l’esito della valutazione al
            quale il paziente è stato sottoposto.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationEsitoValutazione}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationStiliVita.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo volto a descrivere le osservazioni sugli stili di
            vita del paziente.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationStiliVita}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOperationOutcome.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/operationoutcome.html">OperationOutcome</a>
          </td>
          <td>
            Profilo volto a restituire il dettaglio del controllo
            di coerenza non superato.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOperationOutcome}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientCittadino.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/patient.html">Patient</a>
          </td>
          <td>Profilo contenente i dettagli anagrafici di un cittadino</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerProfessionistaSanitario.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/practitioner.html">Practitioner</a>
          </td>
          <td>
            Profilo contenente i dettagli anagrafici di un
            professionista sanitario
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerProfessionistaSanitario}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleProfessionistaSanitario.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/practitionerrole.html">PractitionerRole</a>
          </td>
          <td>
            Profilo contentente la tipologia del professionista
            sanitario con riferimento al dettaglio anagrafico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleProfessionistaSanitario}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedurePrestazione.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/procedure.html">Procedure</a>
          </td>
          <td>
            Profilo contentente il dettaglio di una prestazione erogata
            al paziente in qualsiasi setting assistenziale.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLQuestionnaireResponseValutazione.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/questionnaireresponse.html">QuestionnaireResponse</a>
          </td>
          <td>
            Profilo volto a mostrare il dettaglio delle risposte
            ai quesiti della valutazione alla quale il paziente è
            stato sottoposto.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLQuestionnaireValutazione.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/questionnaire.html">Questionnaire</a>
          </td>
          <td>
            Profilo volto a descrivere la tipologia della valutazione
            al quale il paziente è stato sottoposto.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireValutazione}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestInterventoEducazionale.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo volto a descrivere l’intervento educazionale di cui
            il paziente necessita come definito dal suo progetto
            individuale.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestInterventoEducazionale}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestPrestazioniInfermieristiche.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo volto a contenere le informazioni relative ad
            una prestazione infermieristiche afferente ad un
            progetto individuale di un cittadino.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioniInfermieristiche}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestPrestazioniSociali.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo volto a contenere le informazioni relative ad
            una prestazione sociale afferente ad un progetto
            individuale di un cittadino.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioniSociali}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestPrestazioniSpecialistiche.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo volto a contenere i dettagli una
            prestazione specialistica e/o diagnostica definita
            nell’ambito di un progetto individuale di un cittadino.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPrestazioniSpecialistiche}}
          </td>
        </tr>
        <tr>
          <td>PI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestServiziSocioAssistenziali.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo volto a contenere le informazioni riguardanti
            il servizio socioassistenziale da attivare ad un
            cittadino nell’ambito del suo progetto individuale.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali}}
          </td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationPLOEdificio.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo per descrivere le informazioni relative
            all'edificio di una struttura ospedaliera.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOEdificio}}
          </td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationPLOLetto.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Questo profilo riporta le informazioni relative al posto
            letto occupato.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto}}
          </td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationPLOPiano.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo per descrivere le informazioni relative al piano
            di una struttura ospedaliera.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOPiano}}
          </td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationPLOStanza.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo per descrivere le informazioni relative alla stanza
            di una struttura ospedaliera.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOStanza}}
          </td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMeasurePLO.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/measure.html">Measure</a>
          </td>
          <td>
            Profilo relativo alla misura del totale dei posti
            letto occupati per reparto e per struttura ospedaliera
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasurePLO}}
          </td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMeasureReportPLO.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/measurereport.html">MeasureReport</a>
          </td>
          <td>
            Profilo contenente la misura del totale dei posti
            letto occupati per reparto e per struttura ospedaliera
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMeasureReportPLO}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
