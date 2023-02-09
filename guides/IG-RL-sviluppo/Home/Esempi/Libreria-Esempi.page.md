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
    <table>
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
          <td>Risorsa con profilo RLPatientCittadino</td>
          <td>{{link:esempio-Patient-Cittadino}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>Organization</td>
          <td>Risorsa con profilo RLOrganizationL1</td>
          <td>{{link:esempio-RLOrganizationL1}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>Organization</td>
          <td>Risorsa con profilo RLOrganizationL2</td>
          <td>{{link:esempio-RLOrganizationL2}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>Organization</td>
          <td>Risorsa con profilo RLOrganizationL3</td>
          <td>{{link:esempio-RLOrganizationL3}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>Practitioner</td>
          <td>Risorsa con profilo Practitioner</td>
          <td>{{link:esempio-Practitioner}}</td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>PractitionerRole</td>
          <td>Risorsa con profilo PractitionerRole</td>
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
          <td>(missing)</td>
          <td>{{link:esempio-bundle-notifica-errori-bundle}}</td>
        </tr>
        <tr>
          <td>Errori</td>
          <td>Bundle</td>
          <td>(missing)</td>
          <td>{{link:esempio-bundle-notifica-errori-resource}}</td>
        </tr>
      </tbody>
    </table>
  </body>
</html>






