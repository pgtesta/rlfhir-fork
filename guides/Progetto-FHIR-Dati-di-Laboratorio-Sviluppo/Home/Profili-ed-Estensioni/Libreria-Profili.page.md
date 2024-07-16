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
    <h1>Raccolta profili in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti tutti i profili attivi; ad ogni
        profilo è associato un tema di utilizzo (si veda la pagina
        {{pagelink:Home/Contesto/Panoramica-di-progetto.page.md}}).
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
          <th>Tag</th>
          <th>Nome profilo e pagina di dettaglio</th>
          <th>Risorsa base</th>
          <th>Descrizione</th>
          <th>Link Simplifier</th>
        </tr>
      </thead>
      <tbody id="myTable">
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLBundleRispostaLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/bundle.html">Bundle</a>
          </td>
          <td>
            Profilo che descrive il contenuto informativo del report di un referto di laboratorio
          </td>
          <td>
            {{link:ink:http://hl7.it/fhir/lab-report/StructureDefinition/bundle-it-lab}}
          </td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive il referto di laboratorio
          </td>
          <td>
            {{link:link:http://hl7.it/fhir/lab-report/StructureDefinition/composition-it-lab}}
          </td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLDeviceLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/device.html">Device</a>
          </td>
          <td>
            Profilo che descrive un dispositivo mediante il profilo della risorsa Device per il referto di laboratorio.
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/device-it-lab}}
          </td>
        </tr>
        <tr>
          <td>LAB</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLDiagnosticReportLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/diagnosticreport.html">Diagnostic Report</a>
          </td>
          <td>
            Profilo per descrivere le informazioni cliniche mediante il profilo DiagnosticReport
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/diagnosticreport-it-lab}}
          </td>
        </tr>
        <tr>
          <td>LAB</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLEncounterLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/encounter.html">Encounter</a>
          </td>
          <td>
            Questo profilo riporta la descrizione dei dati relativi all'incontro per la specifica richiesta tramite il profilo della risorsa Encounter per il referto di laboratorio.
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab }}
          </td>
        </tr>
        <tr>
          <td>LAB</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo per descrivere le informazioni relative all'edificio di una struttura ospedaliera.
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/location-it-lab}}
          </td>
        </tr>
        <tr>
          <td>LAB</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMediaLabreport.page.md}}
          </td>
          <td>
            <a href="https://hl7.org/fhir/R4/media.html">Media</a>
          </td>
          <td>
            Profilo per descrivere le informazioni relative ai contenuti multimediali di un referto di laboratorio
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/media-it-lab}}
          </td>
        </tr>
        <tr>
          <td>LAB</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDocumentLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo per descrivere le rilevazioni cliniche effettuate su un paziente
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab}}
          </td>
        </tr>
        <tr>
          <td>LAB</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo per descrivere le rilevazioni cliniche effettuate su un paziente
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/observation-it-lab}}
          </td>
        </tr>
        <tr>
          <td>LAB</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDocumentLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo per descrivere vincoli aggiuntivi per Observation Lab Report
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/observation-doc-it-lab}}
          </td>
        </tr>
        <tr>
          <td>LAB</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientLabReport.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/patient.html">Patient</a>
          </td>
          <td>
            Profilo per descrivere informazioni anagrafiche di base del paziente
          </td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/patient-it-lab}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
