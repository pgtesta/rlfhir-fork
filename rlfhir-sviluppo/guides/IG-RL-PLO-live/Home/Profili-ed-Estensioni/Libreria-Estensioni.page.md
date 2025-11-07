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
          <td>RLLocationAreaDegenza</td>
          <td>Location</td>
          <td>Area degenza</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationAreaDegenza}}
          </td>
        </tr>
        <tr>
          <td>RLLocationDataOraAccettazione</td>
          <td>Location</td>
          <td>Data e ora di accettazione</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationDataOraAccettazione}}
          </td>
        </tr>
        <tr>
          <td>RLLocationDataOraDimissionePrevista</td>
          <td>Location</td>
          <td>Data e ora di dimissione prevista</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationDataOraDimissionePrevista}}
          </td>
        </tr>
        <tr>
          <td>RLLocationDataOraOccupazioneLetto</td>
          <td>Location</td>
          <td>Data e ora di occupazione posto letto</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationDataOraOccupazioneLetto}}
          </td>
        </tr>
        <tr>
          <td>RLLocationDimissioneProtetta</td>
          <td>Location</td>
          <td>Dimissione Protetta</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationDimissioneProtetta}}
          </td>
        </tr>
        <tr>
          <td>RLLocationRegimeRicovero</td>
          <td>Location</td>
          <td>Regime ricovero</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationRegimeRicovero}}
          </td>
        </tr>
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
          <td>RLOrganizationAddressIstatCode</td>
          <td>Address</td>
          <td>Codice ISTAT del comune a cui fa riferimento l'indirizzo</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressIstatCode}}
          </td>
        </tr>
        <tr>
          <td>RLOrganizationDataCessazione</td>
          <td>Organization</td>
          <td>Data di cessazione dell'ente</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataCessazione}}
          </td>
        </tr>
        <tr>
          <td>RLOrganizationDataCostituzione</td>
          <td>Organization</td>
          <td>Data di costituzione dell'ente</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataCostituzione}}
          </td>
        </tr>
        <tr>
          <td>RLOrganizationDataFineValidita</td>
          <td>Organization</td>
          <td>Data di fine della validità di esercizio dell'ente</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita}}
          </td>
        </tr>
        <tr>
          <td>RLOrganizationDataInizioValidita</td>
          <td>Organization</td>
          <td>Data di inizio della validità di esercizio dell'ente</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
