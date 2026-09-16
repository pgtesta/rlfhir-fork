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
        {{link:http://hl7.org/fhir/ValueSet/location-physical-type}}
      </td>
      <td>ValueSet relativo alla codifica della tipologia di location</td>
      <td>http://hl7.org/fhir/ValueSet/location-physical-type</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.it/fhir/lab-report/ValueSet/tipoOrganizzazione}}
      </td>
      <td>ValueSet relativo alla codifica della tipologia di organizzazione</td>
      <td>http://hl7.it/fhir/lab-report/ValueSet/tipoOrganizzazione</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali}}
      </td>
      <td>ValueSet relativo alla codifica ISTAT delle unità amministrative territoriali</td>
      <td>http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali</td>
    </tr>
    <tr>
      <td>
      <a href="https://www.hl7.it/fhir/base/ValueSet-statoCivile.html" target="_blank">Stato civile</a>
      </td>
      <td>ValueSet relativo allo stato civile del paziente</td>
      <td>https://www.hl7.it/fhir/base/ValueSet-statoCivile</td>
    </tr>
    <tr>
      <td>
      <a href="https://fhir.siss.regione.lombardia.it/ValueSet/ReazioniAllergiche.html" target="_blank">Reazioni Allergiche</a>
      </td>
      <td>Value Set ReazioniIntolleranza_PSSIT DYNAMIC per le reazioni da intolleranza; Value Set ReazioniAllergiche_PSSIT DYNAMIC per le reazioni allergiche.</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/ReazioniAllergiche</td>
    </tr>
    <tr>
      <td>
      <a href="https://terminology.hl7.org/3.1.0/CodeSystem-v3-RoleCode.html" target="_blank">Parentela con Paziente</a>
      </td>
      <td>Value Set relativo alla codifica del tipo di parentela.</td>
      <td>https://terminology.hl7.org/3.1.0/CodeSystem-v3-RoleCode.html</td>
    </tr>
    <tr>
      <td>
      <a href="https://fhir.siss.regione.lombardia.it/ValueSet/CriticitaClinica.html" target="_blank">Criticità Clinica</a>
      </td>
      <td>Value Set relativo alla codifica della criticità clinica della patologia.</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/CriticitaClinica</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
