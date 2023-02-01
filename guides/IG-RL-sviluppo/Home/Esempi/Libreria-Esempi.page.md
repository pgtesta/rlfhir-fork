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
    <h1>Racolta esempi</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti tutti gli esempi creati per il progetto.
        <br />
        Usare la casella di ricerca sottostante per filtrare le informazioni
        desiderate.
      </p>
      <input id="myInput" type="text" placeholder="Cerca.." />
    </div>
    <br />
    <table>
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
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca prestazioni erogate</td>
            <td>{{link:ffe258ee-989e-11ed-a8fc-0242ac120002}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca progetti individuali attivi</td>
            <td>{{link:10bb101f-a121-4264-a920-67be9cb82c74}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca sospensioni</td>
            <td>{{link:99e55290-98a7-11ed-a8fc-0242ac120002}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca rivalutazioni</td>
            <td>{{link:99e55291-98a7-11ed-a8fc-0242ac120002}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca sospensioni ADI</td>
            <td>{{link:8109d344-98a8-11ed-a8fc-0242ac120002}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca storico progetti individuali</td>
            <td>{{link:10bb101f-a121-4264-a920-67be9cb82c74}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerva valutazioni</td>
            <td>{{link:c0996f74-9812-11ed-a8fc-0242ac120002}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Patient</td>
            <td>Risorsa con profilo RLPatientCittadino</td>
            <td>{{link:esempio-Patient-Cittadino}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca PI per tipologia, ente erogatore e data ultimo aggiornamento </td>
            <td>{{link:esempio-Bundle-InterrogazioneCarePlan-1}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca PI per tipologia, ente erogatore e CF paziente</td>
            <td>{{link:esempio-Bundle-InterrogazioneCarePlan-2}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca per prestazioni erogate afferenti ad un codice pratica</td>
            <td>{{link:esempio-Bundle-InterrogazioneProcedure-1}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca di un questionario di valutazione per tipologia, ente erogatore, CF paziente e stato completato</td>
            <td>{{link:esempio-Bundle-InterrogazioneQuestionnaireResponse-1}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca di rivalutazioni per codice pratica</td>
            <td>{{link:esempio-Bundle-InterrogazioneServiceRequestRivalutazione-1}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca di sospensioni o rivalutazioni per codice pratica</td>
            <td>{{link:esempio-Bundle-InterrogazioneServiceRequestRivalutazioneESospensioni}}</td>
            </tr>
            <tr>
            <td>CDOM</td>
            <td>Bundle</td>
            <td>Ricerca di sospensioni per codice pratica</td>
            <td>{{link:esempio-Bundle-InterrogazioneServiceRequestSospensione-1}}</td>
            </tr>
            <tr>
            <td>DDC</td>
            <td>Organization</td>
            <td>Risorsa con profilo RLOrganizationL1</td>
            <td>{{link:esempio-RLOrganizationL1}}</td>
            </tr>
            <tr>
            <td>DDC</td>
            <td>Organization</td>
            <td>Risorsa con profilo RLOrganizationL2</td>
            <td>{{link:esempio-RLOrganizationL2}}</td>
            </tr>
            <tr>
            <td>DDC</td>
            <td>Organization</td>
            <td>Risorsa con profilo RLOrganizationL3</td>
            <td>{{link:esempio-RLOrganizationL3}}</td>
            </tr>
            <tr>
            <td>DDC</td>
            <td>Practitioner</td>
            <td>Risorsa con profilo Practitioner</td>
            <td>{{link:esempio-Practitioner}}</td>
            </tr>
            <tr>
            <td>DDC</td>
            <td>PractitionerRole</td>
            <td>Risorsa con profilo PractitionerRole</td>
            <td>{{link:esempio-PractitionerRole}}</td>
            </tr>
            <tr>
            <td>DP</td>
            <td>Patient</td>
            <td>Risorsa con profilo RLPatientDimissioniProtette</td>
            <td>{{link:esempio-Patient-DimissioniProtette}}</td>
            </tr>
            <tr>
            <td>Errori, CDOM</td>
            <td>OperationOutcome</td>
            <td>OperationOutcome: parametro non supportato</td>
            <td>{{link:Esempi-Example-searchfail}}</td>
            </tr>
            <tr>
            <td>Errori, CDOM</td>
            <td>OperationOutcome</td>
            <td>OperationOutcome: eccezione generica</td>
            <td>{{link:Esempi-Example-exception}}</td>
            </tr>
            <tr>
            <td>PLO</td>
            <td>Observation</td>
            <td>Risorsa con profilo RLObservationPLO</td>
            <td>{{link:esempio-PLO}}</td>
            </tr>
            <tr>
            <td>PLO</td>
            <td>Observation</td>
            <td>Risorsa con profilo RLObservationPLO (Reparti ospedale)</td>
            <td>{{link:esempio-PLO-RepartiOspedale}}</td>
            </tr>
            <tr>
            <td>RSA</td>
            <td>HealthcareService</td>
            <td>Risorsa con profilo RLHealthcareServiceRSAInfoBase</td>
            <td>{{link:esempio-RSAInfoBase}}</td>
            </tr>
            <tr>
            <td>UDO</td>
            <td>HealthcareService</td>
            <td>Risorsa con profilo RLHealthcareServiceUDO</td>
            <td>{{link:esempio-UDO}}</td>
            </tr>
        </tbody>
  </table>
  </body>
</html>






