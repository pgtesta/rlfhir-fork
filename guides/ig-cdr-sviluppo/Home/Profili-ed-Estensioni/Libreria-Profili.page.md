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
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlallergyintolerancecore.page.md?version=current">
            RLAllergyIntoleranceCore
      </a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/allergyintolerance.html">AllergyIntolerance</a>
          </td>
          <td>
            Profilo che descrive le allergie e le intolleranze
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntoleranceCore}}
          </td>
        </tr>
        <tr>
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionRAD.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive header e body di un documento di radiologia
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionRAD}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlconditioncore.page.md?version=current">
          RLConditionCore
      </a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/condition.html">Condition</a>
          </td>
          <td>
            Profilo che descrive le patologie di un paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCore}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlencountercore.page.md?version=current">RLEncounterCore</a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/encounter.html">Encounter</a>
          </td>
          <td>
            Profilo che descrive gli episodi clinici
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterCore}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlfammembhistcore.page.md?version=current">
            RLFamilyMemberHistoryCore
      </a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/familymemberhistory.html">FamilyMemberHistory</a>
          </td>
          <td>
            Profilo che descrive l'anamnesi familiare
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLFamilyMemberHistoryCore}}
          </td>
        </tr>
        <tr>
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLImagingStudyRAD.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/imagingstudy.html">ImagingStudy</a>
          </td>
          <td>
            Profilo che descrive studi dicom
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImagingStudyRAD}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rllocationcore.page.md?version=current">
          RLLocationCore
      </a>
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
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationStatementRAD.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationstatement.html">MedicationStatement</a>
          </td>
          <td>
            Profilo che descrive le terapie del paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationStatementRAD}}
          </td>
        </tr>
        <tr>
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationQuesitoDiagnostico.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il quesito diagnostico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationQuesitoDiagnostico}}
          </td>
        </tr>
        <tr>
          <td>CORE,RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationCoreDecorsoClinico.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il decorso clinico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreDecorsoClinico}}
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
            Profilo che descrive le complicanze
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
            Profilo che descrive i precedenti esami eseguiti
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRad}}
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
            Profilo che descrive l'esami eseguito durante l'incontro di radiologia
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationEsameEseguitoRad}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlservicerequestcore.page.md?version=current">
            RLServiceRequestCore
      </a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo che descrive una richiesta
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestCore}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
