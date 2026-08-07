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
      <th>Link Simplifier</th>
    </tr>
  </thead>
  <tbody id="myTable">
     <tr>
      <td>CORE</td>
      <td>Patient</td>
      <td>Paziente</td>
      <td>{{link:Patient/e06086d8-a958-11ed-afa1-0242ac120002}}</td>
    </tr>
     <tr>
      <td>CORE</td>
      <td>AllergyIntolerance</td>
      <td>Allergie o intolleranze</td>
      <td>{{link:AllergyIntolerance/rl-allergyintolerance-002}}</td>
    </tr>
     <tr>
      <td>CORE</td>
      <td>Condition</td>
      <td>Diagnosi e Patologie associate al paziente</td>
      <td>{{link:Condition/rl-condition-001}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>PractitionerRole</td>
      <td>Infermiere</td>
      <td>{{link:PractitionerRole/esempio-practitionerrole-core}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>Practitioner</td>
      <td>Medico</td>
      <td>{{link:Practitioner/3a14db34-a959-11ed-afa1-0242ac120002}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>Location</td>
      <td>Struttura fisica</td>
      <td>{{link:Location/esempio-location-core-base}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>Organization</td>
      <td>Azienda sanitaria</td>
      <td>{{link:Organization/esempio-organization-core}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>RelatedPerson</td>
      <td>Soggetto delegato</td>
      <td>{{link:RelatedPerson/rl-relatedperson-001}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>FamilyMemberHistory</td>
      <td>Storia clinica del familiare</td>
      <td>{{link:FamilyMemberHistory/rl-familymemberhistory-001}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>Encounter</td>
      <td>Episodio clinico ambulatoriale</td>
      <td>{{link:Encounter/rl-encounter-ambulatoriale-001}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>Encounter</td>
      <td>Episodio clinico di ricovero</td>
      <td>{{link:Encounter/rl-encounter-ricovero-001}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>ServiceRequest</td>
      <td>Richiesta di servizio sanitario</td>
      <td>{{link:ServiceRequest/rl-servicerequest-001}}</td>
    </tr>
    <tr>
      <td>CORE</td>
      <td>Observation</td>
      <td>Precedenti esami eseguiti del paziente</td>
      <td>{{link:Observation/rl-observation-precedentiesamieseguiti-001}}</td>
    </tr>
     <tr>
      <td>CORE</td>
      <td>Observation</td>
      <td>Storia Clinica Del Paziente</td>
      <td>{{link:Observation/rl-observation-storia-clinica}}</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
