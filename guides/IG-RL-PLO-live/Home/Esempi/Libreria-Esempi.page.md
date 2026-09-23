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
      <td>DDC</td>
      <td>Organization</td>
      <td>Esempio del profilo RLOrganizationL1</td>
      <td>{{link:Organization/esempio-RLOrganizationL1}}</td>
    </tr>
    <tr>
      <td>DDC</td>
      <td>Organization</td>
      <td>Esempio del profilo RLOrganizationL2</td>
      <td>{{link:Organization/esempio-RLOrganizationL2}}</td>
    </tr>
    <tr>
      <td>DDC</td>
      <td>Organization</td>
      <td>Esempio del profilo RLOrganizationL3</td>
      <td>{{link:Organization/esempio-RLOrganizationL3}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Bundle</td>
      <td>Esempio dei posti letto occupati (risorsa Location)</td>
      <td>{{link:Bundle/esempio-PLO-Location}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationPLOEdificio</td>
      <td>{{link:Location/esempio-Location-PLO-Edificio}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationPLOLetto</td>
      <td>{{link:Location/esempio-Location-PLO-Letto}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationPLOPiano</td>
      <td>{{link:Location/esempio-Location-PLO-Piano}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationPLOStanza</td>
      <td>{{link:Location/esempio-Location-PLO-Stanza}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Measure</td>
      <td>Esempio del profilo RLMeasurePLO</td>
      <td>{{link:Measure/esempio-measure-PLO}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>MeasureReport</td>
      <td>Esempio del profilo RLMeasureReportPLO</td>
      <td>{{link:MeasureReport/esempio-measureReport-PLO}}</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
