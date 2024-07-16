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
        <a href="https://hl7.org/fhir/R4/valueset-identifier-use.html" target="_blank">Identifier use</a>
      </td>
      <td>ValueSet relativo allo scopo dell'identificativo </td>
<td>https://hl7.org/fhir/R4/valueset-identifier-use.html</td>
    </tr>
    <tr>
      <td>
      <a href="https://hl7.org/fhir/R4/valueset-bundle-type.html" target="_blank">Bundle type</a>
      </td>
      <td> ValueSet relativo alla codifica dello scopo del bundle </td>
<td>https://hl7.org/fhir/R4/valueset-bundle-type.html</td>
    </tr>
    <tr>
      <td>
      <a href="https://terminology.hl7.org/5.3.0/ValueSet-v3-Confidentiality.html" target="_blank">Confidentiality</a>
      </td>
      <td> ValueSet relativo alla confidenzialità del documento </td>
<td>https://terminology.hl7.org/5.3.0/ValueSet-v3-Confidentiality.html</td>
    </tr>
    <tr>
      <td>
      <a href="https://www.hl7.it/fhir/lab-report/0.2.0/ValueSet-sezione-referto-laboratorio.html" target="_blank">LOINC specialità laboratorio</a>
      </td>
      <td> ValueSet relativo ai codici LOINC per la specialità di laboratorio </td>
<td>https://www.hl7.it/fhir/lab-report/0.2.0/ValueSet-sezione-referto-laboratorio.html</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/languages" target="_blank">Language</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di organizzazione </td>
<td>http://hl7.org/fhir/ValueSet/languages</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/composition-status|4.0.1" target="_blank">Composition status</a>
      </td>
      <td> ValueSet relativo allo stato clinico della composition </td>
<td>http://hl7.org/fhir/ValueSet/composition-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.eu/fhir/laboratory/ValueSet/lab-reportType-eu-lab" target="_blank">Report type</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di report di laboratorio </td>
<td>http://hl7.eu/fhir/laboratory/ValueSet/lab-reportType-eu-lab</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/R4/valueset-document-classcodes.html" target="_blank">Classcodes</a>
      </td>
      <td> ValueSet relativo al tipo di documento </td>
<td>http://hl7.org/fhir/ValueSet/document-classcodes</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.eu/fhir/laboratory/ValueSet/lab-studyType-eu-lab" target="_blank">Study type</a>
      </td>
      <td> ValueSet relativo alla codifica ISTAT </td>
<td>http://hl7.eu/fhir/laboratory/ValueSet/lab-studyType-eu-lab</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.eu/fhir/laboratory/ValueSet/lab-specialty-eu-lab" target="_blank">Codice Fiscale</a>
      </td>
      <td> ValueSet relativo alla codifica del Codice Fiscale </td>
<td>http://hl7.eu/fhir/laboratory/ValueSet/lab-specialty-eu-lab</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/ValueSet/v3-Confidentiality" target="_blank">ID-STP</a>
      </td>
      <td> ValueSet relativo alla codifica del codice STP </td>
<td>http://terminology.hl7.org/ValueSet/v3-Confidentiality</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/composition-attestation-mode|4.0.1" target="_blank">ID-tesseraTEAM</a>
      </td>
      <td> ValueSet relativo alla codifica del codice TEAM </td>
<td>http://hl7.org/fhir/ValueSet/composition-attestation-mode|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/sezione-referto-laboratorio" target="_blank">ANPR</a>
      </td>
      <td> ValueSet relativo alla codifica del codice ANPR </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/sezione-referto-laboratorio</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/doc-section-codes" target="_blank">ID-Regionale</a>
      </td>
      <td> ValueSet relativo alla codifica dell'id regionale </td>
<td>http://hl7.org/fhir/ValueSet/doc-section-codes</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/diagnostic-report-status" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/diagnostic-report-status</td>
    </tr>
     <tr>
      <td>
      <a href="http://hl7.eu/fhir/laboratory/ValueSet/lab-reportType-eu-lab" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.eu/fhir/laboratory/ValueSet/lab-reportType-eu-lab</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/valueset-status-obs-it" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/valueset-status-obs-it</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/observation-category" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/observation-category</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/observation-category" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/observation-category</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/istat-luogoNascita" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/istat-luogoNascita</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/istat-cittadinanza" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/istat-cittadinanza</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/istat-professione" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/istat-cittadinanza</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/istat-titoloStudio" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/istat-titoloStudio</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/VstipoIdentificatore" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/VstipoIdentificatore</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/vs-anagrafi-regionali" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/vs-anagrafi-regionali</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/uri-idEni" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/uri-idEni</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/URI-idStp" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/URI-idStp</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/udi-entry-type|4.0.1" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/udi-entry-type|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/device-status|4.0.1" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/device-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/device-status-reason" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/device-status-reason</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/device-nametype" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/device-nametype</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/device-type" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/device-type</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-status" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-status</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-status|4.0.1" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/ValueSet/encounter-class" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://terminology.hl7.org/ValueSet/encounter-class</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/ValueSet/v3-ActEncounterCode" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://terminology.hl7.org/ValueSet/v3-ActEncounterCode</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-participant-type" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-participant-type</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-reason" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-reason</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/diagnosis-role" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/diagnosis-role</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-admit-source" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-admit-source</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-special-courtesy" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-special-courtesy</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-special-arrangements" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-special-arrangements</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-location-status|4.0.1" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-location-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/location-physical-type" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/location-physical-type</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/location-status|4.0.1" target="_blank">Marital Status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato civile del paziente </td>
<td>http://hl7.org/fhir/ValueSet/location-status|4.0.1</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
