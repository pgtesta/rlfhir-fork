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
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientRAD.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/patient.html">Patient</a>
          </td>
          <td>
            Profilo che descrive un paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientRAD}}
          </td>
        </tr>
        <tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLImagingStudyRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/imagingstudy.html">ImagingStudy</a>
 </td>
 <td>
 Profilo che descrive lo studio DICOM associato al referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImagingStudyRad}}
 </td>
</tr>
<tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationEsameEseguitoRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive l'esame eseguito nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationEsameEseguitoRad}}
 </td>
</tr>
<tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationComplicanzeRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive le complicanze nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationComplicanzeRad}}
 </td>
</tr>
<tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPrecedentiEsamiEseguitiRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive i precedenti esami eseguiti nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRad}}
 </td>
</tr>
<tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationQuesitoDiagnosticoRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive il quesito diagnostico nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationQuesitoDiagnosticoRad}}
 </td>
</tr>
      </tbody>
    </table>
  </body>
</html>
