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
    <h1>Raccolta ValueSet in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti i ValueSet sviluppati
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
      <th>Nome e Link Simplifier</th>
      <th>Descrizione</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody id="myTable">
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-ASSTAfferenza}}
      </td>
      <td>ValueSet relativo alla codifica ASST Afferenza</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-ASSTAfferenza</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-ATSAfferenza}}
      </td>
      <td>ValueSet relativo alla codifica ATS Afferenza</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-ATSAfferenza</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-AusilioProtesi}}
      </td>
      <td>ValueSet che identifica gli ausili di protesica</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/DDC-AusilioProtesi
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL1}}
      </td>
      <td>ValueSet relativo alle tipologia di enti di livello 1</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL1</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2}}
      </td>
      <td>ValueSet relativo alla tipologia UdO</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DistrettoSanitario}}
      </td>
      <td>
        ValueSet relativo alla codifica dei distretti sanitari. Si noti che il
        link sottostante non riporta volutamente la lista completa dei distretti
        e dei relativi codici identificativi in quanto possono essere soggetti
        ad aggiornamenti e modifiche da parte del SISS. Per consultare la
        versione aggiornata dei distretti sanitari, l'ASST di Afferenza e la
        relativa ATS si rimanda alla tabella “LR22: Relazione
        Distretto-ASST-ATS” descritta nel documento DC-DDC-SIAA#02 il cui
        contenuto informativo è accessibile tramite i servizi riportati nel
        documento DC-DDC-SIAA#01.
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DistrettoSanitario
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-Farmaco}}
      </td>
      <td>
        ValueSet che identifica l'anagrafica dei farmaci secondo la codifica
        ministeriale
      </td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-Farmaco</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-FarmacoAIC}}
      </td>
      <td>
        ValueSet che identifica l'anagrafica dei farmaci secondo la codifica
        ministeriale AIC
      </td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-FarmacoAIC</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-FarmacoATC}}
      </td>
      <td>
        ValueSet che identifica l'anagrafica dei farmaci secondo la codifica
        ministeriale ATC
      </td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-FarmacoATC</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-FarmacoGE}}
      </td>
      <td>
        ValueSet che identifica l'anagrafica dei farmaci secondo la codifica
        ministeriale GE
      </td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-FarmacoGE</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-PrestSpecSISS}}
      </td>
      <td>ValueSet che identifica le prestazioni specialistiche SISS</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/DDC-PrestSpecSISS</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-TipoPrescrittore}}
      </td>
      <td>ValueSet relativo alle qualifiche dei medici prescrittori</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/DDC-TipoPrescrittore
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/OperationOutcome-CodiciErrore}}
      </td>
      <td>
        ValueSet relativo ai codici di errori ottenuti in risposta
        all'interrogazione di API FHIR. Per chi espone API, si raccomanda
        l'utilizzo degli attributi code e display per maggiore leggibilita.
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/OperationOutcome-CodiciErrore
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/OperationOutcome-DettagliErrore}}
      </td>
      <td>
        ValueSet relativo ai dettagli degli errori ottenuti in risposta
        all'interrogazione di API FHIR. Per chi espone API, si raccomanda
        l'utilizzo degli attributi code e display per maggiore leggibilita.
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/OperationOutcome-DettagliErrore
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/Prestazioni}}
      </td>
      <td>ValueSet relativo alla tipologia di prestazione</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/Prestazioni</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/RegimeRicovero}}
      </td>
      <td>ValueSet relativo al regime di ricovero</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/RegimeRicovero</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-EsitoInterRAI}}
      </td>
      <td>
        ValueSet relativo alla codifica degli esiti della valutazione
        InterRAI-HomeCare
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-EsitoInterRAI
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-InterventiEducazionali}}
      </td>
      <td>ValueSet relativo alla codifica degli interventi educazionali</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-InterventiEducazionali
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ModalitaErogazioneIntEdu}}
      </td>
      <td>
        ValueSet relativo alla modalità di erogazione dell'intervento
        educazionale
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ModalitaErogazioneIntEdu
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-MotivoSegnalazione}}
      </td>
      <td>ValueSet relativo al motivo della segnalazione</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-MotivoSegnalazione
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ObiettiviSalute}}
      </td>
      <td>ValueSet relativo agli obiettivi salute</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ObiettiviSalute
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-PercorsiCDom}}
      </td>
      <td>ValueSet relativo ai percorsi di cure domiciliari</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-PercorsiCDom</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/Prestazioni}}
      </td>
      <td>
        ValueSet relativo alla codifica delle prestazioni erogate in qualsiasi setting assistenziale
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/Prestazioni
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ProblemaInfermieristico}}
      </td>
      <td>ValueSet relativo alla codifica dei problemi infermieristici</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ProblemaInfermieristico
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-QualificaProfessionistaSanitario}}
      </td>
      <td>ValueSet relativo alla qualifica del professionista sanitario</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-QualificaProfessionistaSanitario
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-SettingAssistenziale}}
      </td>
      <td>ValueSet relativo alla codifica del setting assistenziale</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-SettingAssistenziale
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-StiliVita}}
      </td>
      <td>ValueSet relativo agli stili di vita</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-StiliVita</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaAccesso}}
      </td>
      <td>ValueSet relativo alla tipologia di accesso</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaAccesso
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaEsenzioni}}
      </td>
      <td>ValueSet relativo alla tipologia di esenzioni</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaEsenzioni
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaOssigeno}}
      </td>
      <td>ValueSet relativo alla tipologia di ossigenoterapia</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaOssigeno
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaProblemaSalute}}
      </td>
      <td>ValueSet che identifica la tipologia di patologia</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaProblemaSalute
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaValutazione}}
      </td>
      <td>ValueSet relativo alla tipologia di valutazione</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaValutazione
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-Valutazione}}
      </td>
      <td>ValueSet relativo alla codifica delle valutazioni specifiche</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-Valutazione</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-CausaleDimissione}}
      </td>
      <td>ValueSet relativo alla causale di dimissione</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-CausaleDimissione
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ModalitaErogazione}}
      </td>
      <td>ValueSet relativo alla modalità di erogazione</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ModalitaErogazione
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-MotiviSospensione}}
      </td>
      <td>ValueSet relativo ai motivi della sospensione</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-MotiviSospensione
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-PosizioneProfessione}}
      </td>
      <td>ValueSet relativo alla codifica della posizione professionale</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-PosizioneProfessione
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ProponentePIC}}
      </td>
      <td>
        ValueSet relativo alla codifica del soggetto che ha proposto la presa in
        carico
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ProponentePIC
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-SituazionePensionistica}}
      </td>
      <td>ValueSet relativo alla codifica della situazione pensionistica</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-SituazionePensionistica
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-StatoCivile}}
      </td>
      <td>ValueSet relativo alla codifica dello stato civile</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-StatoCivile</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipoAccesso}}
      </td>
      <td>ValueSet relativo alla codifica del tipo di accesso</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipoAccesso</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipologiaDiLuogo}}
      </td>
      <td>
        ValueSet relativo alla tipologia di luogo in cui vengono erogate le
        prestazioni di cure domiciliari
      </td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipologiaDiLuogo
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-CondizioneClinica}}
      </td>
      <td>ValueSet relativo alla codifica della tipologia del paziente</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-CondizioneClinica
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipoOperatore}}
      </td>
      <td>ValueSet relativo alla tipologia di operatore ADI</td>
      <td>
        https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipoOperatore
      </td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TitoloStudio}}
      </td>
      <td>ValueSet relativo alla codifica del titolo di studio</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TitoloStudio</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/TipologiaCaregiver}}
      </td>
      <td>ValueSet relativo alla codifica della tipologia di Caregiver</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/TipologiaCaregiver</td>
    </tr>
    <tr>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-AmbitoObiettiviSalute}}
      </td>
      <td>ValueSet relativo alla codifica degli ambiti degli obiettivi di salute</td>
      <td>https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-AmbitoObiettiviSalute</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
