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
        <td>RLCarePlanVersionePAI</td>
        <td>CarePlan</td>
        <td>Versione del progetto individuale</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanVersionePAI}}</td>
      </tr>
      <tr>
        <td>RLDeviceRequestConsegnaPaziente</td>
        <td>DeviceRequest</td>
        <td>Flag riguardo la consegna a domicilio dell'ausilio al paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestConsegnaPaziente}}</td>
      </tr>
      <tr>
        <td>RLDeviceRequestPrescrizioneElettronica</td>
        <td>DeviceRequest</td>
        <td>Flag riguardo la necessità di una prescrizione elettronica per il paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPrescrizioneElettronica}}</td>
      </tr>
      <tr>
        <td>RLEncounterReferenceCarePlan</td>
        <td>Encounter</td>
        <td>Riferimento al progetto individuale derivato dall'accesso</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterReferenceCarePlan}}</td>
      </tr>
      <tr>
        <td>RLEncounterTipoBisogno</td>
        <td>Encounter</td>
        <td>Codice e descrizione della tipologia del bisogno rilevata al cittadino</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterTipoBisogno}}</td>
      </tr>
      <tr>
        <td>RLMedicationRequestConsegnaOssigenoDomicilio</td>
        <td>MedicationRequest</td>
        <td>Flag riguardo la consegna dell'ossigeno a domicilio</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestConsegnaOssigenoDomicilio}}</td>
      </tr>
      <tr>
        <td>RLMedicationRequestConsegnaPaziente</td>
        <td>MedicationRequest</td>
        <td>Flag riguardo la consegna a domicilio del farmaco al paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestConsegnaPaziente}}</td>
      </tr>
      <tr>
        <td>RLMedicationRequestPrescrizioneElettronica</td>
        <td>MedicationRequest</td>
        <td>Flag riguardo la necessità di una prescrizione elettronica per il paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPrescrizioneElettronica}}</td>
      </tr>
      <tr>
        <td>RLOrganizationAddressDistrettoCode</td>
        <td>Address</td>
        <td>Codice del Distretto di appartenenza del comune a cui fa riferimento l'indirizzo</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressDistrettoCode}}</td>
      </tr>
      <tr>
        <td>RLOrganizationAddressIstatCode</td>
        <td>Address</td>
        <td>Codice ISTAT del comune a cui fa riferimento l'indirizzo</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAddressIstatCode}}</td>
      </tr>
      <tr>
        <td>RLOrganizationAsstAfferenza</td>
        <td>Organization</td>
        <td>ASST sotto la quale l'ente eroga servizi sociosanitari sul territorio di competenza</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAsstAfferenza}}</td>
      </tr>
      <tr>
        <td>RLOrganizationAtsAfferenza</td>
        <td>Organization</td>
        <td>ATS alla quale il presidio afferisce</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAtsAfferenza}}</td>
      </tr>
      <tr>
        <td>RLOrganizationDataCessazione</td>
        <td>Organization</td>
        <td>Data di cessazione dell'ente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataCessazione}}</td>
      </tr>
      <tr>
        <td>RLOrganizationDataCostituzione</td>
        <td>Organization</td>
        <td>Data di costituzione dell'ente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataCostituzione}}</td>
      </tr>
      <tr>
        <td>RLOrganizationDataFineValidita</td>
        <td>Organization</td>
        <td>Data di fine della validità di esercizio dell'ente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita}}</td>
      </tr>
      <tr>
        <td>RLOrganizationDataInizioValidita</td>
        <td>Organization</td>
        <td>Data di inizio della validità di esercizio dell'ente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita}}</td>
      </tr>
      <tr>
        <td>RLOrganizationDataInsert</td>
        <td>Organization</td>
        <td>Data di inserimento del record</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInsert}}</td>
      </tr>
      <tr>
        <td>RLOrganizationDataUpdate</td>
        <td>Organization</td>
        <td>Data di aggiornamento del record</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataUpdate}}</td>
      </tr>
      <tr>
        <td>RLPatientATSResidenza</td>
        <td>Patient</td>
        <td>ATS di residenza del paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientATSResidenza}}</td>
      </tr>
      <tr>
        <td>RLPatientCittadinanza</td>
        <td>Patient</td>
        <td>Cittadinanza del paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCittadinanza}}</td>
      </tr>
      <tr>
        <td>RLPatientLuogoDiNascita</td>
        <td>Patient</td>
        <td>Codice ISTAT del comune/nazione di nascita del paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientLuogoDiNascita}}</td>
      </tr>
      <tr>
        <td>RLPatientPosizioneDellaProfessione</td>
        <td>Patient</td>
        <td>Posizione della professione del paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientPosizioneDellaProfessione}}</td>
      </tr>
      <tr>
        <td>RLPatientResponsabilitaGenitoriale</td>
        <td>Patient</td>
        <td>Codice della responsabilità genitoriale nei confronti dell'assistito se minorenne</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientResponsabilitaGenitoriale}}</td>
      </tr>
      <tr>
        <td>RLPatientSituazionePensionistica</td>
        <td>Patient</td>
        <td>Situazione pensionistica del paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientSituazionePensionistica}}</td>
      </tr>
      <tr>
        <td>RLPatientTEAMNumeroIdentificazioneIstituzioneCompetente</td>
        <td>Patient.identifier</td>
        <td>Numero di identificazione dell'istituzione indicata sulla tessera TEAM</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientTEAMNumeroIdentificazioneIstituzioneCompetente}}</td>
      </tr>
      <tr>
        <td>RLPatientTipologiaCittadino</td>
        <td>Patient</td>
        <td>Codice relativo alla condizione clinica prevalente del paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientTipologiaCittadino}}</td>
      </tr>
      <tr>
        <td>RLPatientTitoloDiStudio</td>
        <td>Patient</td>
        <td>Titolo di studio del paziente</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientTitoloDiStudio}}</td>
      </tr>
      <tr>
        <td>RLPractitionerDataInsert</td>
        <td>Practitioner</td>
        <td>Data di inserimento del record</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerDataInsert}}</td>
      </tr>
      <tr>
        <td>RLPractitionerDataUpdate</td>
        <td>Practitioner</td>
        <td>Data dell'ultima modifica del record</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerDataUpdate}}</td>
      </tr>
      <tr>
        <td>RLPractitionerRoleDataInsert</td>
        <td>PractitionerRole</td>
        <td>Data di inserimento del record</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleDataInsert}}</td>
      </tr>
      <tr>
        <td>RLPractitionerRoleDataUpdate</td>
        <td>PractitionerRole</td>
        <td>Data dell'ultima modifica del record</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleDataUpdate}}</td>
      </tr>
      <tr>
        <td>RLPractitionerRoleDettagliAttivazionePercorsoCure</td>
        <td>PractitionerRole</td>
        <td>0</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleDettagliAttivazionePercorsoCure}}</td>
      </tr>
      <tr>
        <td>RLPractitionerRoleNumeroAccessi</td>
        <td>PractitionerRole</td>
        <td>0</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleNumeroAccessi}}</td>
      </tr>
      <tr>
        <td>RLProcedureNumeroAccesso</td>
        <td>Procedure</td>
        <td>Numero accesso</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedureNumeroAccesso}}</td>
      </tr>
      <tr>
        <td>RLProcedurePrestazioneDataPresaInCarico</td>
        <td>Procedure</td>
        <td>Data della presa in carico del paziente da parte dell'Ente Erogatore</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedureDataPresaInCarico}}</td>
      </tr>
      <tr>
        <td>RLProcedurePrestazioneModalitaErogazione</td>
        <td>Procedure</td>
        <td>Modalità di erogazione</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedureModalitaErogazione}}</td>
      </tr>
      <tr>
        <td>RLProcedureTipoAccesso</td>
        <td>Procedure</td>
        <td>Codice del tipo di accesso</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedureTipoAccesso}}</td>
      </tr>
      <tr>
        <td>RLQuestionnaireResponseEsitoValutazione</td>
        <td>QuestionnaireResponse</td>
        <td>Riferimento all'esito della valutazione (semplice o multidimensionale) al quale il paziente è stato sottoposto</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseEsitoValutazione}}</td>
      </tr>
      <tr>
        <td>RLQuestionnaireResponseTipologiaValutazione</td>
        <td>QuestionnaireResponse</td>
        <td>Codice della tipologia di valutazione</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLQuestionnaireResponseTipologiaValutazione}}</td>
      </tr>
      <tr>
        <td>RLServiceRequestCausaleDimissione</td>
        <td>ServiceRequest</td>
        <td>Nel caso in cui il codice del servizio sociosanitario (campo code) sia "C-DOM" questo campo contiene la causale di dimissione del paziente dal ricovero domiciliare</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestCausaleDimissione}}</td>
      </tr>
      <tr>
        <td>RLServiceRequestDataDimissione</td>
        <td>ServiceRequest</td>
        <td>Nel caso in cui il codice del servizio sociosanitario (campo code) sia "C-DOM" questo campo contiene la data di dimissione del paziente dal ricovero domiciliare</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestDataDimissione}}</td>
      </tr>
      <tr>
        <td>RLServiceRequestDettagliPrenotazione</td>
        <td>ServiceRequest</td>
        <td>Dettagli riguardo le modalità di prenotazione del servizio sociosanitario</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestDettagliPrenotazione}}</td>
      </tr>
      <tr>
        <td>RLServiceRequestSoggettoProponentePIC</td>
        <td>ServiceRequest</td>
        <td>Codice del soggetto che ha proposto la presa in carico dell'assistito</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestSoggettoProponentePIC}}</td>
      </tr>
      <tr>
        <td>RLServiceRequestUlterioriDettagli</td>
        <td>ServiceRequest</td>
        <td>Ulteriori dettagli riguardo la prestazione specialistica e/o diagnostica da erogare</td>
        <td>{{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestUlterioriDettagli}}</td>
      </tr>
    </tbody>
    </table>
  </body>
</html>
