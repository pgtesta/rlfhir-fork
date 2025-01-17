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
    <h1>Raccolta estensioni in uso</h1>
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
    <table style="width: fit-content">
      <thead>
        <tr>
          <th>Nome estensione</th>
          <th>Base</th>
          <th>Descrizione</th>
          <th>Link simplifier</th>
        </tr>
      </thead>
      <tbody id="myTable">
        <tr>
          <td>patient-citizienship</td>
          <td>Patient</td>
          <td>Indica il codice di riferimento del paese di cittadinanza </td>
          <td>
            {{link:http://hl7.org/fhir/StructureDefinition/patient-citizenship}}
          </td>
        </tr>
        <tr>
          <td>patient-birthPlace</td>
          <td>Patient</td>
          <td>Indica l'indirizzo di nascita del paziente</td>
          <td>
            {{link:http://hl7.org/fhir/StructureDefinition/patient-birthPlace}}
          </td>
        </tr>
        </tr>
        <tr>
          <td>patient-occupation-it</td>
          <td>Patient</td>
          <td>Occupazione del paziente</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/patient-occupation-it}}
          </td>
        </tr>
        <tr>
          <td>patient-qualification-it</td>
          <td>Patient</td>
          <td>Titolo di studio del paziente</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/patient-qualification-it}}
          </td>
        </tr>
         <tr>
          <td>patient-ATSResidenza</td>
          <td>Patient</td>
          <td>ATS di residenza del paziente</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientATSResidenza}}
          </td>
        </tr>
        </tbody>
    </table>
  </body>
</html>
