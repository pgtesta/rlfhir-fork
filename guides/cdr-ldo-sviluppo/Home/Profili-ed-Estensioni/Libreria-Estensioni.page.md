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
    <h1>Raccolta estensioni in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolte tutte le estensioni sviluppate
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
          <th>Nome estensione</th>
          <th>Base</th>
          <th>Descrizione</th>
          <th>Link simplifier</th>
        </tr>
      </thead>
      <tbody id="myTable">
        <tr>
          <td>patient-codeableBirthPlace</td>
          <td>Patient</td>
          <td>Indica il codice istat del comune di nascita</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/patient-codeableBirthPlacel}}
          </td>
        </tr>
        <tr>
          <td>birth-place-ita</td>
          <td>Patient</td>
          <td>Luogo di nascita del paziente</td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/birth-place-ita}}
          </td>
        </tr>
        <tr>
          <td>patient-occupation-it</td>
          <td>Patient</td>
          <td>Occupazione del paziente</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/patient-occupation-it}}
          </td>
        </tr>
        <tr>
          <td>patient-qualification-it</td>
          <td>Patient</td>
          <td>Titolo di studio del paziente</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/patient-qualification-it}}
          </td>
        </tr>
        <tr>
          <td>dataEnterer-time</td>
          <td>Composition</td>
          <td>Data di compilazione</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/dataEnterer-time}}
          </td>
        </tr>
        <tr>
          <td>composition-dataenterer-it</td>
          <td>Composition</td>
          <td>Compilatore del documento</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/composition-dataenterer-it}}
          </td>
        </tr>
        <tr>
          <td>address-official</td>
          <td>Address</td>
          <td>Indica se l’indirizzo è definito ufficiale in quel Paese.</td>
          <td>
            {{link:http://hl7.it/fhir/lab-report/StructureDefinition/address-official}}
          </td>
        </tr>
        <tr>
          <td>address-dug</td>
          <td>Address</td>
          <td>Indica la denominazione urbanistica generica dell'indirizzo.</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/address-dug}}
          </td>
        </tr>
        <tr>
          <td>recordCertification</td>
          <td>Address, Identifier</td>
          <td>Indica se l'elemento associato è stata certificato (od autocertificato) da una certa entità (persona, organizzazione). L’estensione è caratterizzata da: (a) una data di certificazione o da una periodo di validità (b) un codice od un riferimento al certificatore.</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/recordCertification}}
          </td>
        </tr>
        </tbody>
    </table>
  </body>
</html>
