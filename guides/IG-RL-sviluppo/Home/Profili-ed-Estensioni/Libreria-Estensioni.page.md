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
    <h1>Racolta estensioni in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolte tutte le estensioni sviluppate
        per i profili del progetto.
        <br />
        Usare la casella di ricerca sottostante per filtrare le informazioni
        desiderate.
      </p>
      <input id="myInput" type="text" placeholder="Cerca.." />
    </div>
    <br />
    <table>
      <thead>
        <tr>
          <th>Nome Extension e link Simplifier</th>
          <th>Nome campo esteso</th>
          <th>Descrizione</th>
          <th>Contesto</th>
          <th>Usato in</th>
        </tr>
      </thead>
      <tbody id="myTable">
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanVersionePAI}}
          </td>
          <td>VersionePAI</td>
          <td>Versione del progetto individuale</td>
          <td>CarePlan</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanProgettoIndividuale.page.md}}
          </td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressDistrettoCode}}
          </td>
          <td>DistrettoCode</td>
          <td>
            Distretto territoriale così definito dalla legge regionale 22-2021
            della Regione Lombardia
          </td>
          <td>Organization.Address</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}},
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}
          </td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressIstatCode}}
          </td>
          <td>IstatCode</td>
          <td>Codice ISTAT</td>
          <td>Organization.Address</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}},
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}
          </td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationASSTAfferenza}}
          </td>
          <td>ASSTAfferenza</td>
          <td>
            ASST sotto la quale l'ente eroga servizi sociosanitari sul
            territorio di competenza
          </td>
          <td>Organization</td>
          <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}</td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationATSAfferenza}}
          </td>
          <td>ATSAfferenza</td>
          <td>ATS alla quale il presidio afferisce territorialmente</td>
          <td>Organization</td>
          <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}</td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataCessazione}}
          </td>
          <td>DataCessazione</td>
          <td>Data di cessazione dell'ente</td>
          <td>Organization</td>
          <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}}</td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataCostituzione}}
          </td>
          <td>DataCostituzione</td>
          <td>Data di costituzione dell'ente</td>
          <td>Organization</td>
          <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}}</td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita}}
          </td>
          <td>DataFineValidita</td>
          <td>
            Data di fine della validità di esercizio dell'ente descritto dal
            profilo
          </td>
          <td>Organization</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}},
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}},
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL3.page.md}}
          </td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita}}
          </td>
          <td>DataInizioValidita</td>
          <td>
            Data di inizio della validità di esercizio dell'ente descritto dal
            profilo
          </td>
          <td>Organization</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}},
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}},
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL3.page.md}}
          </td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInsert}}
          </td>
          <td>DataInsert</td>
          <td>Data di inserimento del record</td>
          <td>Organization</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}},
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}
          </td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataUpdate}}
          </td>
          <td>DataUpdate</td>
          <td>Data di aggiornamento del record</td>
          <td>Organization</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}},
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}
          </td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerDataInsert}}
          </td>
          <td>DataInsert</td>
          <td>Data di inserimento del record</td>
          <td>Practitioner</td>
          <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerMedicoPrescrittore.page.md}}</td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerDataUpdate}}
          </td>
          <td>DataUpdate</td>
          <td>Data dell'ultima modifica del record</td>
          <td>Practitioner</td>
          <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerMedicoPrescrittore.page.md}}</td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleDataInsert}}
          </td>
          <td>DataInsert</td>
          <td>Data di inserimento del record</td>
          <td>PractitionerRole</td>
          <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleMedicoPrescrittore.page.md}}</td>
        </tr>
        <tr>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleDataUpdate}}
          </td>
          <td>DataUpdate</td>
          <td>Data dell'ultima modifica del record</td>
          <td>PractitionerRole</td>
          <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleMedicoPrescrittore.page.md}}</td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
