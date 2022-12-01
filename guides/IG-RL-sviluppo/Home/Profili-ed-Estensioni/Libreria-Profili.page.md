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
    <h1>Racolta profili in uso</h1>
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
    <table>
    <thead>
      <tr>
        <th>Tema</th>
        <th>Nome Profilo</th>
        <th>Descrizione</th>
        <th>Risorsa base</th>
        <th>Link Simplifier</th>
      </tr>
    </thead>
    <tbody id="myTable">
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL1.page.md}}</td>
        <td>Profilo che descrive una struttura o un ente identificato univocamente da un codice di ente L1</td>
        <td><a href="http://hl7.org/fhir/R4/organization.html">Organization</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1}}</td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}</td>
        <td>Profilo che descrive un’unità d’offerta identificata univocamente da un codice L2</td>
        <td><a href="http://hl7.org/fhir/R4/organization.html">Organization</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2}}</td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL3.page.md}}</td>
        <td>Profilo che descrive un reparto appartenente ad una struttura di ricovero identificata da un codice L2</td>
        <td><a href="http://hl7.org/fhir/R4/organization.html">Organization</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3}}</td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitioner.page.md}}</td>
        <td>Profilo che contiene l’anagrafica dei medici prescrittori della Regione Lombardia destinatari di ricettari RUR</td>
        <td><a href="http://hl7.org/fhir/R4/practitioner.html">Practitioner</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitioner}}</td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRole.page.md}}</td>
        <td>Risorsa che raccoglie i ruoli e le qualifiche di un determinato medico prescrittore</td>
        <td><a href="http://hl7.org/fhir/R4/practitionerrole.html">PractitionerRole</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRole}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientCittadino.page.md}}</td>
        <td>Dettagli anagrafici del cittadino</td>
        <td><a href="http://hl7.org/fhir/R4/patient.html">Patient</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanProgettoIndividuale.page.md}}</td>
        <td>Profilo che contiene tutte le attività e le informazioni definite in un progetto individuale (PAI) di un cittadino redatto sul Sistema di Gestione Digitale del Territorio.</td>
        <td><a href="http://hl7.org/fhir/R4/careplan.html">CarePlan</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLQuestionnaireResponseValutazione.page.md}}</td>
        <td>(missing)</td>
        <td><a href="http://hl7.org/fhir/R4/questionnaireresponse.html">QuestionnaireResponse</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedurePrestazione.page.md}}</td>
        <td>(missing)</td>
        <td><a href="http://hl7.org/fhir/R4/procedure.html">Procedure</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestSopensioneADI.page.md}}</td>
        <td>(missing)</td>
        <td><a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSopensioneADI}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestRivalutazione .page.md}}</td>
        <td>(missing)</td>
        <td><a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a></td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione }}</td>
      </tr>
    </tbody>
    </table>
  </body>
</html>
