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
      <td>RAD</td>
      <td>MedicationStatement-TerapiaFarmacologica</td>
      <td>Terapia farmacologica precedente del paziente</td>
      <td>{{link:MedicationStatement/rl-medicationstatement-001}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>MedicationStatement-TerapiaFarmacologica</td>
      <td>Terapia farmacologica in atto del paziente</td>
      <td>{{link:MedicationStatement/rl-medicationstatement-002}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Esame Eseguito (1)</td>
      <td>{{link:Observation/Example-Observation-EsameEseguito-1-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Esame Eseguito (2)</td>
      <td>{{link:Observation/Example-Observation-EsameEseguito-2-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Precedenti Esami Eseguiti (1)</td>
      <td>{{link:Observation/Example-Observation-PrecedentiEsamiEseguiti-1-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Precedenti Esami Eseguiti (2)</td>
      <td>{{link:Observation/Example-Observation-PrecedentiEsamiEseguiti-2-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Complicanze (1)</td>
      <td>{{link:Observation/Example-Observation-Complicanze-1-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Complicanze (2)</td>
      <td>{{link:Observation/Example-Observation-Complicanze-2-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Composition</td>
      <td>Informazioni mediche paziente</td>
      <td>{{link:Composition/referto-radiologia-0451-20260922}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>ImagingStudy</td>
      <td>ImagingStudy (1)</td>
      <td>{{link:ImagingStudy/Example-ImagingStudy-1-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>ImagingStudy</td>
      <td>ImagingStudy (2)</td>
      <td>{{link:ImagingStudy/Example-ImagingStudy-2-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Quesito Diagnostico</td>
      <td>{{link:Observation/Example-Observation-QuesitoDiagnostico-1-RAD}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>CarePlan</td>
      <td>Piano di cura alla dimissione</td>
      <td>{{link:CarePlan/Example-CarePlan-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>MedicationAdministration</td>
      <td>Terapia farmacologica somministrata in Pronto Soccorso</td>
      <td>{{link:MedicationAdministration/Example-MedicationAdministration-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>MedicationRequest</td>
      <td>Richiesta di terapia farmacologica in Pronto Soccorso</td>
      <td>{{link:MedicationRequest/Example-MedicationRequestTerapiaPS-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>MedicationRequest</td>
      <td>Terapia farmacologica prescritta alla dimissione</td>
      <td>{{link:MedicationRequest/Example-MedicationRequestTerapiaDimissione-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Accertamenti</td>
      <td>{{link:Observation/Example-ObservationAccertamenti-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Complicanze</td>
      <td>{{link:Observation/Example-ObservationComplicanze-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Dimissione - Data decesso</td>
      <td>{{link:Observation/Example-ObservationDataDecesso-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Dimissione - Livello appropriatezza</td>
      <td>{{link:Observation/Example-ObservationLivelloAppropriatezza-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Dimissione - Prognosi</td>
      <td>{{link:Observation/Example-ObservationPrognosi-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Dimissione - Richiesta autopsia</td>
      <td>{{link:Observation/Example-ObservationRichiestaAutopsia-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Motivo della visita - Problema all'accesso</td>
      <td>{{link:Observation/Example-ObservationProblemaAccesso-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Motivo della visita - Ragione della visita</td>
      <td>{{link:Observation/Example-ObservationRagioneVisita-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Triage - Valutazione acutezza</td>
      <td>{{link:Observation/Example-ObservationTriage-1-VPS}}</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
