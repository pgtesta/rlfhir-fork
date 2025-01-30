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
      <td>LDO</td>
      <td>AllergyIntollerance</td>
      <td>Esempio di allergia al formaggio</td>
      <td>-</td>
      <td>{{link:AllergyIntollerance/esempio-allergia-cibo-ldo}}</td>
    </tr>
     <tr>
      <td>LDO</td>
      <td>AllergyIntollerance</td>
      <td>Esempio di allergia al farmaco</td>
      <td>-</td>
      <td>{{link:AllergyIntollerance/esempio-allergia-cibo-ldo}}</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
