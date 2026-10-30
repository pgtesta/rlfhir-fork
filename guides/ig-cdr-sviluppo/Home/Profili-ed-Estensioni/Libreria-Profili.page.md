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
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientRAD.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/patient.html">Patient</a>
          </td>
          <td>
            Profilo che descrive un paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientRAD}}
          </td>
        </tr>
        <tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLImagingStudyRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/imagingstudy.html">ImagingStudy</a>
 </td>
 <td>
 Profilo che descrive lo studio DICOM associato al referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImagingStudyRad}}
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
 Profilo che descrive l'esame eseguito nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationEsameEseguitoRad}}
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
 Profilo che descrive le complicanze nel contesto del referto di radiologia
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
 Profilo che descrive i precedenti esami eseguiti nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRad}}
 </td>
</tr>
<tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationQuesitoDiagnosticoRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive il quesito diagnostico nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationQuesitoDiagnosticoRad}}
 </td>
</tr>

<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
 </td>
 <td>
 Profilo che descrive il documento Piano Terapeutico Individuale
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/careplan.html">CarePlan</a>
 </td>
 <td>
 Profilo che descrive il Piano Terapeutico Individuale: scadenza, flag di prescrizione e condizioni cliniche
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionCondizioniErogabilitaPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/condition.html">Condition</a>
 </td>
 <td>
 Profilo che descrive una condizione di erogabilità del piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCondizioniErogabilitaPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionCriteriEsclusionePti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/condition.html">Condition</a>
 </td>
 <td>
 Profilo che descrive un criterio di esclusione del piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPesoPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive il peso del paziente nel piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPesoPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDurataMalattiaPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive la durata della malattia (BPCO) nel piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
 </td>
 <td>
 Profilo che descrive il programma terapeutico del piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medication.html">Medication</a>
 </td>
 <td>
 Profilo che descrive il farmaco prescritto nel piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPti}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
 </td>
 <td>
 Profilo che descrive il documento lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationAdministrationRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medicationadministration.html">MedicationAdministration</a>
 </td>
 <td>
 Profilo che descrive la terapia farmacologica somministrata durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationAdministrationRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestDimissioneLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
 </td>
 <td>
 Profilo che descrive la terapia farmacologica alla dimissione nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestDimissioneLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
 </td>
 <td>
 Profilo che descrive la terapia farmacologica prescritta durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationComplicanzeLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive le complicanze nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationComplicanzeLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationConsulenzaLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive la consulenza nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationConsulenzaLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDecorsoClinicoLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive il decorso clinico nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDecorsoClinicoLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDiagnosiDimissioneLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive la diagnosi alla dimissione nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDiagnosiDimissioneLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationEsamiEseguitiRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive gli esami eseguiti durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationEsamiEseguitiRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationMotivoRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive il motivo del ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationMotivoRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationProcedureRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive le procedure durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationProcedureRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedureLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/procedure.html">Procedure</a>
 </td>
 <td>
 Profilo che descrive le procedure eseguite durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedureLdo}}
 </td>
</tr>
      </tbody>
    </table>
  </body>
</html>
