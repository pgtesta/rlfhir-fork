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
        <a href="https://terminology.hl7.org/5.5.0/CodeSystem-icd9.html" target="_blank">HL7 ICD-9 Code System</a>
      </td>
      <td>ValueSet relativo alla codifica ICD9 </td>
<td>https://terminology.hl7.org/5.5.0/CodeSystem-icd9.html</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.org/fhir/ValueSet/location-physical-type}}
      </td>
      <td> ValueSet relativo alla codifica del physical-type per il letto </td>
<td>http://hl7.org/fhir/ValueSet/location-physical-type</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/RegimeRicovero}}
      </td>
      <td> ValueSet relativo alla codifica del regime di ricovero </td>
<td>https://fhir.siss.regione.lombardia.it/ValueSet/RegimeRicovero</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/tipoOrganizzazione" target="_blank">Tipo Organizzazione</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di organizzazione </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/tipoOrganizzazione</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/tipoOrganizzazione" target="_blank">Tipo Organizzazione</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di organizzazione </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/tipoOrganizzazione</td>
    </tr>
    <tr>
      <td>
      <a href="https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL1" target="_blank">DDC-L1</a>
      </td>
      <td> ValueSet relativo alla codifica della tipologia di Ente (L1) </td>
<td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL1</td>
    </tr>
    <tr>
      <td>
      <a href="https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2" target="_blank">DDC-L2</a>
      </td>
      <td> ValueSet relativo alla codifica della tipologia di Ente (L1) </td>
<td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2</td>
    </tr>
    <tr>
      <td>
      <a href="https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2" target="_blank">DDC-L2</a>
      </td>
      <td> ValueSet relativo alla codifica della tipologia di Ente (L1) </td>
<td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali" target="_blank">ISTAT</a>
      </td>
      <td> ValueSet relativo alla codifica ISTAT </td>
<td>http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/sid/codiceFiscale" target="_blank">Codice Fiscale</a>
      </td>
      <td> ValueSet relativo alla codifica del Codice Fiscale </td>
<td>http://hl7.it/sid/codiceFiscale</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.it/ValueSet/uri-idStp" target="_blank">ID-STP</a>
      </td>
      <td> ValueSet relativo alla codifica del codice STP </td>
<td>http://terminology.hl7.it/ValueSet/uri-idStp</td>
    </tr>
    <tr>
      <td>
      <a href="https://fhir.siss.regione.lombardia.it/sid/tesseraTeam" target="_blank">ID-tesseraTEAM</a>
      </td>
      <td> ValueSet relativo alla codifica del codice TEAM </td>
<td>https://fhir.siss.regione.lombardia.it/sid/tesseraTeam</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.it/ValueSet/uri-idEni" target="_blank">ID-ENI</a>
      </td>
      <td> ValueSet relativo alla codifica del codice ENI </td>
<td>http://terminology.hl7.it/ValueSet/uri-idEni</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/sid/anpr" target="_blank">ANPR</a>
      </td>
      <td> ValueSet relativo alla codifica del codice ANPR </td>
<td>http://hl7.it/sid/anpr</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.it/ValueSet/uri-idRegionali" target="_blank">idRegionali</a>
      </td>
      <td> ValueSet relativo alla codifica dell'id regionale </td>
<td>http://terminology.hl7.it/ValueSet/uri-idRegionali</td>
    </tr>
    <tr>
      <td>
      <a href="https://www.hl7.it/fhir/base/ValueSet-statoCivile.html" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>https://www.hl7.it/fhir/base/ValueSet-statoCivile.html</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
