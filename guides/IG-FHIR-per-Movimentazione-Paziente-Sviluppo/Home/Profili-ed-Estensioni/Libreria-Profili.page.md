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
          <td>MP</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLEncounterMP.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/StructureDefinition/Encounter">Encounter</a>
          </td>
          <td>
            Profilo che descrive le informazioni di un ricovero, dimissione, trasferimento
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterMP}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo che descrive una struttura fisica per il contesto di Regione Lombardia
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationCore}}
          </td>
        </tr>
        <tr>
          <td>PLO</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationPLOLetto.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo per descrivere le informazioni relative
            al posto letto occupato dal paziente in una struttura ospedaliera.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationPLOLetto}}
          </td>
        </tr>
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo che descrive una struttura o un ente
            identificato univocamente da un codice di ente L1
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1}}
          </td>
        </tr>        
        <tr>
          <td>DDC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo che descrive un presidio
            identificato univocamente da un codice di ente L2
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo per descrivere le informazioni relative alla struttura ospedaliera.
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationCore}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/StructureDefinition/Patient">Patient</a>
          </td>
          <td>
            Profilo per descrivere le informazioni relative al paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
