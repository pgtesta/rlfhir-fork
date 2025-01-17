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
      <a href="http://hl7.org/fhir/ValueSet/composition-status|4.0.1" target="_blank">Composition status</a>
      </td>
      <td> ValueSet relativo allo stato clinico della composition </td>
<td>http://hl7.org/fhir/ValueSet/composition-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/ValueSet/v3-Confidentiality" target="_blank">Confidentiality</a>
      </td>
      <td> ValueSet relativo alla codifica della confidenzialità del documento </td>
<td>http://terminology.hl7.org/ValueSet/v3-Confidentiality</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/composition-attestation-mode|4.0.1" target="_blank">Attestation mode</a>
      </td>
      <td> ValueSet relativo alla codifica del modo in cui una persona ha autenticato la composition </td>
<td>http://hl7.org/fhir/ValueSet/composition-attestation-mode|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/diagnostic-report-status" target="_blank">Diagnostic report status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato del report diagnostico </td>
<td>http://hl7.org/fhir/ValueSet/diagnostic-report-status</td>
    </tr>
     <tr>
      <td>
      <a href="http://hl7.eu/fhir/laboratory/ValueSet/lab-reportType-eu-lab" target="_blank">Report type</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di report </td>
<td>http://hl7.eu/fhir/laboratory/ValueSet/lab-reportType-eu-lab</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/valueset-status-obs-it" target="_blank">Observation status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato della risorsa observation </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/valueset-status-obs-it</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/observation-category" target="_blank">Observation category</a>
      </td>
      <td> ValueSet relativo alla codifica della categoria di observation </td>
<td>http://hl7.org/fhir/ValueSet/observation-category</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione" target="_blank">Risultato osservazione</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di osservazione nel referto </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it" target="_blank">Codice descrizione risultato observation</a>
      </td>
      <td> ValueSet relativo alla codifica della descrizione del risultato della rilevazione </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/istat-professione" target="_blank">Professione</a>
      </td>
      <td> ValueSet relativo alla codifica della professione del paziente </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/istat-cittadinanza</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/VstipoIdentificatore" target="_blank">Tipo di identificatore</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di identificatore</td>
<td>http://hl7.it/fhir/lab-report/ValueSet/VstipoIdentificatore</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-status|4.0.1" target="_blank">Encounter status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato dell'encounter </td>
<td>http://hl7.org/fhir/ValueSet/encounter-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/ValueSet/encounter-class" target="_blank">Encounter Class</a>
      </td>
      <td> ValueSet relativo alla codifica della classe dell'encounter </td>
<td>http://terminology.hl7.org/ValueSet/encounter-class</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/ValueSet/v3-ActEncounterCode" target="_blank">ActEncounterClass</a>
      </td>
      <td> ValueSet relativo alla codifica relativa all'ActEncounterClass </td>
<td>http://terminology.hl7.org/ValueSet/v3-ActEncounterCode</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-participant-type" target="_blank">Encounter participant type</a>
      </td>
      <td> ValueSet relativo alla codifica del modo in cui un soggetto è coinvolto nell'encounter </td>
<td>http://hl7.org/fhir/ValueSet/encounter-participant-type</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-reason" target="_blank">Encounter reason</a>
      </td>
      <td> ValueSet relativo alla codifica del motivo dell'encounter</td>
<td>http://hl7.org/fhir/ValueSet/encounter-reason</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/diagnosis-role" target="_blank">Diagnosis Role</a>
      </td>
      <td> ValueSet relativo alla codifica usata per espirmere il ruolo della diagnosi nell'encounter </td>
<td>http://hl7.org/fhir/ValueSet/diagnosis-role</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-admit-source" target="_blank">Admit source</a>
      </td>
      <td> ValueSet relativo alla codifica della provenienza del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-admit-source</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-special-arrangements" target="_blank">Special arrangements</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di sistemazione/strumentazione fornita durante la visita del paziente </td>
<td>http://hl7.org/fhir/ValueSet/encounter-special-arrangements</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/encounter-location-status|4.0.1" target="_blank">Encounter location status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato della location </td>
<td>http://hl7.org/fhir/ValueSet/encounter-location-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/CodeSystem/location-physical-type" target="_blank">Location physical type</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di location </td>
<td>http://terminology.hl7.org/CodeSystem/location-physical-type</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/location-status|4.0.1" target="_blank">Location status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato della location </td>
<td>http://hl7.org/fhir/ValueSet/location-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://terminology.hl7.org/ValueSet/v2-0116" target="_blank">Stato del letto</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato del letto in cui per un paziente in ingress </td>
<td>http://terminology.hl7.org/ValueSet/v2-0116</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/location-mode|4.0.1" target="_blank">Tipo di location</a>
      </td>
      <td> ValueSet relativo alla codifica della modalità di location: se rappresenta una location specifica o una classe </td>
<td>http://hl7.org/fhir/ValueSet/location-mode|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/days-of-week|4.0.1" target="_blank">Days of week</a>
      </td>
      <td> ValueSet relativo alla codifica dei giorni della settimana </td>
<td>http://hl7.org/fhir/ValueSet/days-of-week|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/event-status|4.0.1" target="_blank">Event status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato dell'evento </td>
<td>http://hl7.org/fhir/ValueSet/event-status|4.0.1</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/media-type" target="_blank">Media type</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di media </td>
<td>http://hl7.org/fhir/ValueSet/media-type</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/resource-types" target="_blank">Resource type</a>
      </td>
      <td> ValueSet relativo alla codifica del tipo di risorsa FHIR </td>
<td>http://hl7.org/fhir/ValueSet/resource-types</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/observation-status" target="_blank">Observation status</a>
      </td>
      <td> ValueSet relativo alla codifica dello stato dell'observation </td>
<td>http://hl7.org/fhir/ValueSet/observation-status</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione" target="_blank">Risultato observation</a>
      </td>
      <td> ValueSet relativo alla codifica del risultato dell'observation </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/risultato-osservazione</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it" target="_blank">Descrizione risultato observation</a>
      </td>
      <td> ValueSet relativo alla codifica della descrizione del risultato dell'observation </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it" target="_blank">Descrizione risultato observation</a>
      </td>
      <td> ValueSet relativo alla codifica della descrizione del risultato dell'observation </td>
<td>http://hl7.it/fhir/lab-report/ValueSet/valueset-valuecodeableconcept-obs-it</td>
    </tr>
    <tr>
      <td>
      <a href="http://hl7.org/fhir/ValueSet/observation-methods" target="_blank">Observation methods - SNOMED CT</a>
      </td>
      <td> ValueSet relativo alla codifica del metodo utilizzato nell'observation </td>
<td>http://hl7.org/fhir/ValueSet/observation-methods</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
