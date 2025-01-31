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
    <h1>Raccolta esempi</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti tutti gli esempi creati per il progetto.
        <br />
        Usare la casella di ricerca sottostante per filtrare le informazioni
        desiderate.
      </p>
      <input id="myInput" type="text" placeholder="Cerca.." />
    </div>
    <br/>
    <table style="width: fit-content">
  <thead>
    <tr>
      <th>Tag</th>
      <th>ResourceType</th>
      <th>Descrizione</th>
      <th>Pagina dell'esempio</th>
      <th>Link Simplifier</th>
    </tr>
  </thead>
  <tbody id="myTable">
    <tr>
      <td>LDO</td>
      <td>AllergyIntolerance</td>
      <td>Esempio di allergia al formaggio</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLRichiesta3.page.md}}</td>
      <td>{{link:AllergyIntolerance/esempio-allergia-cibo-ldo}}</td>
    </tr>
    <tr>
      <td>LDO</td>
      <td>AllergyIntolerance</td>
      <td>Esempio di allergia al farmaco</td>
      <td>-</td>
      <td>{{link:AllergyIntolerance/esempio-allergia-farmaci-ldo}}</td>
    </tr>
    <tr>
      <td>LDO</td>
      <td>Bundle</td>
      <td>Recupero delle osservazioni in decorso ospedaliero di un paziente</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLAllergyIntoleranceBundleSearchSet.page.md}}</td>
      <td>{{link:Bundle/bundle-recupero-osservazioni-decorso-ospedaliero}}</td>
    </tr>
    <tr>
      <td>LDO</td>
      <td>Bundle</td>
      <td>Recupero delle osservazioni in decorso ospedaliero di un paziente</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLBundleSearchSetDecorsoOspedaliero.page.md}}</td>
      <td>{{link:Bundle/bundle-recupero-osservazioni-decorso-ospedaliero}}</td>
    </tr>
    <tr>
      <td>LDO</td>
      <td>Bundle</td>
      <td>Recupero delle osservazioni in decorso ospedaliero di un paziente</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLBundleSearchSetDimissioneOspedaliera.page.md}}</td>
      <td>{{link:Bundle/bundle-recupero-osservazioni-decorso-ospedaliero}}</td>
    </tr>
    <tr>
      <td>LDO</td>
      <td>Bundle</td>
      <td>Recupero delle osservazioni in decorso ospedaliero di un paziente</td>
      <td>{{pagelink:Home/Esempi/Raccolta-esempi/RLMedicationRequestBundleSearchSet.page.md}}</td>
      <td>{{link:Bundle/bundle-recupero-osservazioni-decorso-ospedaliero}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>LocationCore</td>
      <td>Esempio di location di una stanza</td>
      <td>-</td>
      <td>{{link:Location/esempio-location-operation room-ldo}}</td>
    </tr>
    <tr>
      <td>LDO</td>
      <td>Medication</td>
      <td>Esempio di identificazione di una formulazione generica</td>
      <td>-</td>
      <td>{{link:Medication/esempio-medication-formulazione-ldo}}</td>
    </tr>
    <tr>
      <td>LDO</td>
      <td>MedicationRequest</td>
      <td>Esempio di ordine di un farmaco con istruzioni sulla somministrazione</td>
      <td>-</td>
      <td>{{link:MedicationRequest/esempio-MedicationRequest-ldo}}</td>
    </tr>
    <tr>
      <td>LDO</td>
      <td>Observation</td>
      <td>Esempio di una rilevazione clinica</td>
      <td>-</td>
      <td>{{link:Observation/esempio-observation-ldo}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>OrganizationCore</td>
      <td>Esempio del profilo che descrive un'azienda</td>
      <td>-</td>
      <td>{{link:Organization/esempio-organization-core-ldo}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>PatientCore</td>
      <td>Esempio del profilo che descrive un paziente</td>
      <td>-</td>
      <td>{{link:Patient/esempio-patient-ldo}}</td>
    </tr>
    <tr>
    <tr>
      <td>CORE</td>
      <td>PractitionerCore</td>
      <td>Esempio del profilo che descrive un operatore sanitario</td>
      <td>-</td>
      <td>{{link:Practitioner/esempio-practitioner-core-ldo}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>PractitionerRoleCore</td>
      <td>Esempio del profilo che descrive il ruolo e la struttura di un operatore sanitario</td>
      <td>-</td>
      <td>{{link:PractitionerRole/esempio-practitionerRole-core-ldo}}</td>
    </tr>
      <td>LDO</td>
      <td>Provenance</td>
      <td>Esempio di un documento clinico da cui sono estratte le informazioni</td>
      <td>-</td>
      <td>{{link:Provenance/esempio-provenance-ldo}}</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
