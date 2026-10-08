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
        {{link:http://loinc.org}}
      </td>
      <td>Tipologia di documento</td>
      <td>http://loinc.org</td>
    </tr>
    <tr>
      <td>
        {{link:https://www.eumed.it/icd9cm/}}
      </td>
      <td>Classificazione internazionale delle malattie ICD-9-CM</td>
      <td>https://www.eumed.it/icd9cm/</td>
    </tr>
    <tr>
      <td>
        {{link:https://www.fascicolosanitario.gov.it/portale/sistema-di-codifica-aic}}
      </td>
      <td>Codici AIC dei medicinali</td>
      <td>https://www.fascicolosanitario.gov.it/portale/sistema-di-codifica-aic/</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.org/fhir/ValueSet/composition-status}}
      </td>
      <td>Stato del documento</td>
      <td>http://hl7.org/fhir/ValueSet/composition-status</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.org/fhir/ValueSet/composition-attestation-mode}}
      </td>
      <td>Modalità di attestazione del documento</td>
      <td>http://hl7.org/fhir/ValueSet/composition-attestation-mode</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali}}
      </td>
      <td>Codice identificativo di ciascuna sezione del documento</td>
      <td>http://loinc.org
      </td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali}}
      </td>
      <td>Codice identificativo di ciascuna sezione del documento</td>
      <td>urn:oid:1.2.840.10008.2.16.4
      </td>
    </tr>
    <tr>
      <td>
        {{link:http://terminology.hl7.org/CodeSystem/v3-RouteOfAdministration}}
      </td>
      <td>Via di somministrazione di farmaci e vaccini</td>
      <td>urn:oid:2.16.840.1.113883.5.112
      </td>
    </tr>
    <tr>
      <td>
        {{link:http://terminology.hl7.org/CodeSystem/v3-ActSite}}
      </td>
      <td>Sede anatomica di somministrazione di farmaci e vaccini</td>
      <td>urn:oid:2.16.840.1.113883.5.1052
      </td>
    </tr>
  </tbody>
</table>
  </body>
</html>
