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
        <td>Profilo che descrive una struttura o un ente identificato univocamente da&nbsp;&nbsp;&nbsp;un codice di ente L1</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/organization.html"&gt;Organization&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL1}}</td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL2.page.md}}</td>
        <td>Profilo che descrive un’unità d’offerta identificata univocamente da un&nbsp;&nbsp;&nbsp;codice L2</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/organization.html"&gt;Organization&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL2}}</td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationL3.page.md}}</td>
        <td>Profilo che descrive un reparto appartenente ad una struttura di ricovero&nbsp;&nbsp;&nbsp;identificata da un codice L2</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/organization.html"&gt;Organization&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationL3}}</td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitioner.page.md}}</td>
        <td>Profilo che contiene l’anagrafica dei medici prescrittori della Regione&nbsp;&nbsp;&nbsp;Lombardia destinatari di ricettari RUR</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/practitioner.html"&gt;Practitioner&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitioner}}</td>
      </tr>
      <tr>
        <td>DDC</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRole.page.md}}</td>
        <td>Risorsa che raccoglie i ruoli e le qualifiche di un determinato medico&nbsp;&nbsp;&nbsp;prescrittore</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/practitionerrole.html"&gt;PractitionerRole&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRole}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientCittadino.page.md}}</td>
        <td>Dettagli anagrafici del cittadino</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/patient.html"&gt;Patient&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadino}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanProgettoIndividuale.page.md}}</td>
        <td>Profilo che contiene tutte le attività e le informazioni definite in un&nbsp;&nbsp;&nbsp;progetto individuale (PAI) di un cittadino redatto sul Sistema di Gestione&nbsp;&nbsp;&nbsp;Digitale del Territorio.</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/careplan.html"&gt;CarePlan&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLQuestionnaireResponseValutazione.page.md}}</td>
        <td>(missing)</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/questionnaireresponse.html"&gt;QuestionnaireResponse&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseValutazione}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedurePrestazione.page.md}}</td>
        <td>(missing)</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/procedure.html"&gt;Procedure&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePrestazione}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestSopensioneADI.page.md}}</td>
        <td>(missing)</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/servicerequest.html"&gt;ServiceRequest&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSopensioneADI}}</td>
      </tr>
      <tr>
        <td>ADI</td>
        <td>{{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestRivalutazione&nbsp;&nbsp;&nbsp;.page.md}}</td>
        <td>(missing)</td>
        <td>&lt;a&nbsp;&nbsp;&nbsp;href="http://hl7.org/fhir/R4/servicerequest.html"&gt;ServiceRequest&lt;/a&gt;</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestRivalutazione&nbsp;&nbsp;&nbsp;}}</td>
      </tr>
    </tbody>
    </table>
  </body>
</html>
