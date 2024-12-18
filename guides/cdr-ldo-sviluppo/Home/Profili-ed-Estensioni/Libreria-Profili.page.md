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
        {{pagelink:Home/Contesto/Panoramica-di-progetto}}).
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
          <td>LDO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationLDO.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medication.html">Medication</a>
          </td>
          <td>
            Profilo che è utilizzato per l'identificazione e definizione di un farmaco. 
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationLDO}}
          </td>
        </tr>
        <tr>
          <td>LDO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestLDO.page.md}}
          </td>
          <td>
            <a href="https://hl7.org/fhir/R4/medicationrequest.html">Medication Request</a>
          </td>
          <td>
             Ordine o richiesta sia per la fornitura del farmaco che per le istruzioni per la somministrazione del farmaco a un paziente.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestLDO}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
