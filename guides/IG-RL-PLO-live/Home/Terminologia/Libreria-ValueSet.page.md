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
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-ASSTAfferenza}}
      </td>
      <td>ValueSet relativo alla codifica ASST Afferenza</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-ASSTAfferenza</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-ATSAfferenza}}
      </td>
      <td>ValueSet relativo alla codifica ATS Afferenza</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-ATSAfferenza</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL1}}
      </td>
      <td>ValueSet relativo alle tipologia di enti di livello 1</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL1</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2}}
      </td>
      <td>ValueSet relativo alla tipologia UdO</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DistrettoSanitario}}
      </td>
      <td>
        ValueSet relativo alla codifica dei distretti sanitari. Si noti che il
        link sottostante non riporta volutamente la lista completa dei distretti
        e dei relativi codici identificativi in quanto possono essere soggetti
        ad aggiornamenti e modifiche da parte del SISS. Per consultare la
        versione aggiornata dei distretti sanitari, l'ASST di Afferenza e la
        relativa ATS si rimanda alla tabella “LR22: Relazione
        Distretto-ASST-ATS” descritta nel documento DC-DDC-SIAA#02 il cui
        contenuto informativo è accessibile tramite i servizi riportati nel
        documento DC-DDC-SIAA#01.
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DistrettoSanitario
      </td>
    </tr>
        <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/RegimeRicovero}}
      </td>
      <td>ValueSet relativo al regime di ricovero</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/RegimeRicovero</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
