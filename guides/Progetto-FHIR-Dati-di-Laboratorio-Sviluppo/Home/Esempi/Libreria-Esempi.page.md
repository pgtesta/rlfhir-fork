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
      <th>Pagina dell'esempio</th>
      <th>Link Simplifier</th>
    </tr>
  </thead>
  <tbody id="myTable">
    <tr>
      <td>LAB</td>
      <td>Bundle</td>
      <td>Ricerca degli esami effettuati da un paziente e le relative informazioni riguardanti di contesto</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLEncounterBundleSearchSet.page.md}}</td>
      <td>{{link:Bundle/esempio-con-encounter}}</td>
    </tr>
    <tr>
      <td>LAB</td>
      <td>Bundle</td>
      <td>Ricerca risultati di laboratorio di un paziente in un periodo di 5 mesi </td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLNelTempoBundleSearchSet.page.md}}</td>
      <td>{{link:Bundle/esempio-nel-tempo}}</td>
    </tr>
    <tr>
      <td>LAB</td>
      <td>Bundle</td>
      <td>Ricerca esame specifico di laboratorio per un determinato paziente 1</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLEsame1BundleSearchSet.page.md}}</td>
      <td>{{link:Bundle/esempio-esame-specifico-1}}</td>
    </tr>
    <tr>
      <td>LAB</td>
      <td>Bundle</td>
      <td>Ricerca esame specifico di laboratorio per un determinato paziente 2</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLEsame2BundleSearchSet.page.md}}</td>
      <td>{{link:Bundle/esempio-esame-specifico-2}}</td>
    </tr>
    <tr>
      <td>LAB</td>
      <td>Bundle</td>
      <td>Ricerca documento specifico tramite l'identificativo</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLRichiesta1.page.md}}</td>
      <td>{{link:Bundle/esempio-richiesta-1}}</td>
    </tr>
    <tr>
      <td>LAB</td>
      <td>Bundle</td>
      <td>Ricerca dei docuemnti associati ad un paziente</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLRichiesta2.page.md}}</td>
      <td>{{link:Bundle/esempio-richiesta-2}}</td>
    </tr>
    <tr>
      <td>LAB</td>
      <td>Bundle</td>
      <td>Ricerca dei docuemnti associati ad un paziente utilizzando il paging</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLPaging.page.md}}</td>
      <td>{{link:Bundle/esempio-paging-richiesta-1}} {{link:Bundle/esempio-paging-richiesta-2}}</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
