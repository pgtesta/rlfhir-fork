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
    <h1>Raccolta ValueSet in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti i ValueSet sviluppati
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
      <th>Nome e Link Simplifier</th>
      <th>Descrizione</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody id="myTable">
    <tr>
      <td>
      <a href="https://fhir.siss.regione.lombardia.it/ValueSet/LDO-Allergeni" target="_blank">Allergeni</a>
      </td>
      <td> ValueSet relativo alla codifica degli allergeni </td>
<td>https://fhir.siss.regione.lombardia.it/ValueSet/LDO-Allergeni</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/CodeSystem/location-physical-type" target="_blank">Tipo di struttura fisica</a>
      </td>
      <td> ValueSet relativo al tipo di struttura fisica </td>
<td>http://terminology.hl7.org/CodeSystem/location-physical-type</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/tipoOrganizzazione" target="_blank">Tipo di organizzazione</a>
      </td>
      <td> ValueSet relativo al tipo di organizzazione </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/tipoOrganizzazione</td>
    </tr>
    <tr>
      <td>
      <a href="  http://hl7.it/fhir/ValueSet/statoCivile" target="_blank">Stato civile</a>
      </td>
      <td> ValueSet relativo allo stato civile di una persona </td>
<td>  http://hl7.it/fhir/ValueSet/statoCivile</td>
    </tr>