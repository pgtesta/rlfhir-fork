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
        {{pagelink:Home/Contesto/Panoramica-di-progetto}}).
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
          <td>LDO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLAllergyIntoleranceLDO.page.md}}
          </td>
          <td>
            <a href="https://hl7.org/fhir/r4/allergyintolerance.html">Allergy Intolerance</a>
          </td>
          <td>
            Risorsa contentente informazioni su allergie, intolleranze e reazioni avverse di un paziente. 
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntoleranceLDO}}
          </td>
        </tr>
        <tr>
          <td>LDO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLEncounterLDO.page.md}}
          </td>
          <td>
            <a href="https://hl7.org/fhir/r4/encounter.html">Encounter</a>
          </td>
          <td>
            Risorsa contentente informazioni sul ricovero del paziente. 
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab}}
          </td>
        </tr>
        <tr>
          <td>LDO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationLDO.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medication.html">Medication</a>
          </td>
          <td>
            Profilo che è utilizzato per l'identificazione e definizione di un farmaco. 
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationLDO}}
          </td>
        </tr>
        <tr>
          <td>LDO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestLDO.page.md}}
          </td>
          <td>
            <a href="https://hl7.org/fhir/R4/medicationrequest.html">Medication Request</a>
          </td>
          <td>
             Ordine o richiesta per la fornitura del farmaco e per le istruzioni per la somministrazione dello stesso a un paziente.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO}}
          </td>
        </tr>
        <tr>
          <td>LDO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationLDO.page.md}}
          </td>
          <td>
            <a href="https://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che è utilizzato per la descrizione delle rilevazioni cliniche.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLDO}}
          </td>
        </tr>
        <tr>
          <td>Core</td>
          <td>
            <a href=https://simplifier.net/guide/ig-core/Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientCore.page.md?version=current}}>
            RLPatientCore
            </a>
          </td>
          <td>
            <a href="https://hl7.org/fhir/R4/patient.html">Patient</a>
          </td>
          <td>
             Informazioni sul paziente secondo il profilo Core di RL.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
