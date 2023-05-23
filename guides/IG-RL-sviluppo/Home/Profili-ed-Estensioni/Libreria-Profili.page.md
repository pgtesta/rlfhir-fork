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
      </tr>
    </thead>
    <tbody id="myTable">
      <tr>
        <td>C-DOM</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleOperatoreADI.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/practitionerrole.html"
            >PractitionerRole</a
          >
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
      </tr>
      <tr>
        <td>C-DOM</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestSospensioneADI.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
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
      </tr>
      <tr>
        <td>DDC</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
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
      </tr>
      <tr>
        <td>DDC</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerMedicoPrescrittore.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/practitioner.html">Practitioner</a>
        </td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleMedicoPrescrittore.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/practitionerrole.html"
            >PractitionerRole</a
          >
        </td>
      </tr>
      <tr>
        <td>Errori</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLBundleNotificaErrori.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/bundle.html">Bundle</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLAllergyIntoleranceAllergie.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/allergyintolerance.html"
            >AllergyIntolerance</a
          >
        </td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanProgettoIndividuale.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/careplan.html">CarePlan</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCareTeamEquipe.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/careteam.html">CareTeam</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionPatologiaPrimariaSecondariaUlteriore.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/condition.html">Condition</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionProblemaInfermieristico.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/condition.html">Condition</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCoverageEsenzioni.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/coverage.html">Coverage</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLDeviceRequestProtesiAusili.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/devicerequest.html">DeviceRequest</a>
        </td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLEncounterAccesso.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/encounter.html">Encounter</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLGoalObiettiviSalute.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/goal.html">Goal</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationLuogoPrestazioneCureDom.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/location.html">Location</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestOssigenoterapia.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/medicationrequest.html"
            >MedicationRequest</a
          >
        </td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestTerapiaFarmacologica.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/medicationrequest.html"
            >MedicationRequest</a
          >
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
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationEsitoValutazione.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/observation.html">Observation</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationStiliVita.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/observation.html">Observation</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOperationOutcome.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/operationoutcome.html"
            >OperationOutcome</a
          >
        </td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientCittadino.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/patient.html">Patient</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerProfessionistaSanitario.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/practitioner.html">Practitioner</a>
        </td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleProfessionistaSanitario.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/practitionerrole.html"
            >PractitionerRole</a
          >
        </td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedurePrestazione.page.md}}
        </td>
        <td><a href="http://hl7.org/fhir/R4/procedure.html">Procedure</a></td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLQuestionnaireValutazione.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/questionnaire.html">Questionnaire</a>
        </td>
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLQuestionnaireResponseValutazione.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/questionnaireresponse.html"
            >QuestionnaireResponse</a
          >
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
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestPrestazioniInfermieristiche.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
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
      </tr>
      <tr>
        <td>PI</td>
        <td>
          {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestPrestazioniSpecialistiche.page.md}}
        </td>
        <td>
          <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
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
      </tr>
    </tbody>
  </table>
  </body>
</html>
