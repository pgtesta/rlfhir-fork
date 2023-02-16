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
    <h1>Raccolta esempi</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti tutti gli esempi creati per il progetto.
        <br />
        Usare la casella di ricerca sottostante per filtrare le informazioni
        desiderate.
      </p>
      <input id="myInput" type="text" placeholder="Cerca.." />
    </div>
    <br/>
    <table style="width: fit-content">
      <thead>
        <tr>
          <th>Tag</th>
          <th>ResourceType</th>
          <th>Descrizione</th>
          <th>Link Simplifier</th>
        </tr>
      </thead>
      <tbody id="myTable">
        <tr>
          <td>CDOM</td>
          <td>Bundle</td>
          <td>Ricerca prestazioni erogate</td>
          <td>{{link:esempio-ricerca-prestazioni-erogate}}</td>
        </tr>
        <tr>
          <td>CDOM</td>
          <td>Bundle</td>
          <td>Ricerca progetti individuali attivi</td>
          <td>{{link:esempio-ricerca-pi-attivi}}</td>
        </tr>
        <tr>
          <td>CDOM</td>
          <td>Bundle</td>
          <td>Ricerca rivalutazioni e sospensioni</td>
          <td>{{link:esempio-ricerca-rivalutazioni-sospensioni}}</td>
        </tr>
        <tr>
          <td>CDOM</td>
          <td>Bundle</td>
          <td>Ricerca rivalutazioni</td>
          <td>{{link:esempio-ricerca-rivalutazioni}}</td>
        </tr>
        <tr>
          <td>CDOM</td>
          <td>Bundle</td>
          <td>Ricerca sospensioni</td>
          <td>{{link:esempio-ricerca-sospensione}}</td>
        </tr>
        <tr>
          <td>CDOM</td>
          <td>Bundle</td>
          <td>Ricerca storico progetti individuali</td>
          <td>{{link:esempio-ricerca-storico-pi}}</td>
        </tr>
        <tr>
          <td>CDOM</td>
          <td>Bundle</td>
          <td>Ricerca valutazioni</td>
          <td>{{link:esempio-ricerca-valutazioni}}</td>
        </tr>
        <tr>
          <td>CDOM</td>
          <td>Patient</td>
          <td>Esempio del profilo RLPatientCittadino</td>
          <td>{{link:esempio-Patient-Cittadino}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>Organization</td>
          <td>Esempio del profilo RLOrganizationL1</td>
          <td>{{link:esempio-RLOrganizationL1}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>Organization</td>
          <td>Esempio del profilo RLOrganizationL2</td>
          <td>{{link:esempio-RLOrganizationL2}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>Organization</td>
          <td>Esempio del profilo RLOrganizationL3</td>
          <td>{{link:esempio-RLOrganizationL3}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>Practitioner</td>
          <td>Esempio del profilo Practitioner</td>
          <td>{{link:esempio-Practitioner}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>PractitionerRole</td>
          <td>Esempio del profilo PractitionerRole</td>
          <td>{{link:esempio-PractitionerRole}}</td>
        </tr>
        <tr>
          <td>Errori, CDOM</td>
          <td>OperationOutcome</td>
          <td>OperationOutcome: parametro non supportato</td>
          <td>{{link:esempio-searchfail}}</td>
        </tr>
        <tr>
          <td>Errori, CDOM</td>
          <td>OperationOutcome</td>
          <td>OperationOutcome: eccezione generica</td>
          <td>{{link:esempio-exception}}</td>
        </tr>
        <tr>
          <td>Errori</td>
          <td>Bundle</td>
          <td>
            Esempio di messaggio di notifica errore di coerenza in caso di ricerca
            tramite parametri
          </td>
          <td>{{link:esempio-bundle-notifica-errori-bundle}}</td>
        </tr>
        <tr>
          <td>Errori</td>
          <td>Bundle</td>
          <td>
            Esempio di messaggio di notifica errore di coerenza in caso di ricerca
            tramite ID
          </td>
          <td>{{link:esempio-bundle-notifica-errori-resource}}</td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>Observation</td>
          <td>Esempio del profilo RLObservationPLO</td>
          <td>{{link:esempio-PLO}}</td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>HealthcareService</td>
          <td>Esempio del profilo RLHealthcareServiceRSAInfoBase</td>
          <td>{{link:esempio-RSAInfoBase}}</td>
        </tr>
        <tr>
          <td>UDO</td>
          <td>HealthcareService</td>
          <td>Esempio del profilo RLHealthcareServiceUDO</td>
          <td>{{link:esempio-UDO}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>Observation</td>
          <td>Esempio del profilo RLObservationEsitoValutazione</td>
          <td>{{link:esempio-Observation-EsitoValutazione}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>MedicationRequest</td>
          <td>Esempio del profilo RLMedicationRequestTerapiaFarmacologica</td>
          <td>{{link:esempio-MedicationRequest-TerapiaFarmacologica}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>MedicationRequest</td>
          <td>Esempio del profilo RLMedicationRequestRequestOssigenoterapia</td>
          <td>{{link:esempio-MedicationRequest-Ossigenoterapia}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>Goal</td>
          <td>Esempio del profilo RLGoalObiettiviSalute</td>
          <td>{{link:esempio-Goal-ObiettiviSalute}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>Encounter</td>
          <td>Esempio del profilo RLEncounterEncounterAccesso</td>
          <td>{{link:esempio-Encounter-Accesso}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>DeviceRequest</td>
          <td>Esempio del profilo RLDeviceRequestProtesiAusili</td>
          <td>{{link:esempio-DeviceRequest-ProtesiAusili}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>Condition</td>
          <td>
            Esempio del profilo RLConditionPatologiaPrimariaSecondariaUlteriore
          </td>
          <td>{{link:esempio-Condition-PatologiaPrimariaSecondariaUlteriore}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>CareTeam</td>
          <td>Esempio del profilo RLCareTeamTeamEquipe</td>
          <td>{{link:esempio-CareTeam-Equipe}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>CarePlan</td>
          <td>Esempio del profilo RLCarePlanProgettoIndividuale</td>
          <td>{{link:esempio-CarePlan-Progetto-Individuale}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>ServiceRequest</td>
          <td>Esempio del profilo RLServiceRequestServiziSocioAssistenziali</td>
          <td>{{link:esempio-ServiceRequest-ServiziSocioAssistenziali}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>PractitionerRole</td>
          <td>Esempio del profilo RLPractitionerRoleProfessionistaSanitario</td>
          <td>{{link:esempio-PractitionerRole-ProfessionistaSanitario}}</td>
        </tr>
        <tr>
          <td>CDOM</td>
          <td>PractitionerRole</td>
          <td>Esempio del profilo RLPractitionerRoleOperatoreADI</td>
          <td>{{link:esempio-PractitionerRole-OperatoreADI}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>Practitioner</td>
          <td>Esempio del profilo RLPractitionerProfessionistaSanitario</td>
          <td>{{link:esempio-Practitioner-ProfessionistaSanitario}}</td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>Bundle</td>
          <td>
            Esempio di bundle di risposta per il numero di posti letto occupati
          </td>
          <td>{{link:esempio-bundle-PLO-esitopositivo}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>ServiceRequest</td>
          <td>Esempio del profilo RLServiceRequestInterventoEducazionale</td>
          <td>{{link:esempio-ServiceRequest-InterventoEducazionale}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>ServiceRequest</td>
          <td>Esempio del profilo RLServiceRequestPrestazioniInfermieristiche</td>
          <td>{{link:esempio-ServiceRequest-PrestazioniInfermieristiche}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>ServiceRequest</td>
          <td>Esempio del profilo RLServiceRequestPrestazioniSpecialistiche</td>
          <td>{{link:esempio-ServiceRequest-PrestazioniSpecialistiche}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>ServiceRequest</td>
          <td>Esempio del profilo RLServiceRequestRivalutazione</td>
          <td>{{link:esempio-ServiceRequest-Rivalutazione}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>ServiceRequest</td>
          <td>Esempio del profilo RLServiceRequestServiziSocioAssistenziali</td>
          <td>{{link:esempio-ServiceRequest-ServiziSocioAssistenziali}}</td>
        </tr>
        <tr>
          <td>PI</td>
          <td>ServiceRequest</td>
          <td>Esempio del profilo RLServiceRequestSospensioneADI</td>
          <td>{{link:esempio-ServiceRequest-SospensioneADI}}</td>
        </tr>
      </tbody>
    </table>
  </body>
</html>






