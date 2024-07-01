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
          <td>RLLocationRepartoClinico</td>
          <td>Location</td>
          <td>Reparto clinico</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationRepartoClinico}}
          </td>
        </tr>
        <tr>
          <td>RLLocationRepartoFisico</td>
          <td>Location</td>
          <td>Reparto Fisico</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationRepartoFisico}}
          </td>
        </tr>
        <tr>
          <td>RLEncounterDatiDimissione</td>
          <td>Encounter</td>
          <td>Dati dimissione: paziente dimissibile, motivo per cui non avviene la dimissione se paziente dimissibile, dimissione protetta</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterDatiDimissione}}
          </td>
        </tr>
        <tr>
          <td>plannedEndDate</td>
          <td>Encounter</td>
          <td>Data prevista di dimissione</td>
          <td>
            {{link:http://hl7.org/fhir/6.0/StructureDefinition/extension-Encounter.plannedEndDate}}
          </td>
        </tr>
        </tbody>
    </table>
  </body>
</html>
