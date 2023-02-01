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
    <h1>Racolta ValueSet in uso</h1>
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
    <table>
        <thead>
            <tr>
            <th>Nome</th>
            <th>Descrizione</th>
            <th>Link Simplifier</th>
            </tr>
        </thead>
        <tbody id="myTable">
            <tr>
            <td>DDC Ausilio Protesi</td>
            <td>ValueSet che identifica gli ausili di protesica</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-AusilioProtesi}}
            </td>
            </tr>
            <tr>
            <td>DDC Desc L1</td>
            <td>ValueSet relativo alle tipologia di enti di livello 1</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL1}}
            </td>
            </tr>
            <tr>
            <td>DDC Desc L2</td>
            <td>ValueSet relativo alla tipologia UdO</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2}}
            </td>
            </tr>
            <tr>
            <td>DDC Farmaco</td>
            <td>
                ValueSet che identifica l'anagrafica dei farmaci secondo
                la codifica ministeriale
            </td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-Farmaco}}
            </td>
            </tr>
            <tr>
            <td>DDC Prest Spec SISS</td>
            <td>ValueSet che identifica le prestazioni specialistiche SISS</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-PrestSpecSISS}}
            </td>
            </tr>
            <tr>
            <td>DDC Tipo Prescrittore</td>
            <td>ValueSet relativo alle qualifiche dei medici prescrittori</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-TipoPrescrittore}}
            </td>
            </tr>
            <tr>
            <td>SIAD Motivi Sospensione</td>
            <td>ValueSet relativo ai motivi della sospensione</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-MotiviSospensione}}
            </td>
            </tr>
            <tr>
            <td>SGDT Motivo Segnalazione</td>
            <td>ValueSet relativo al motivo della segnalazione</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-MotivoSegnalazione}}
            </td>
            </tr>
            <tr>
            <td>SGDT TipologiaAccesso</td>
            <td>ValueSet relativo alla tipologia di accesso</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaAccesso}}
            </td>
            </tr>
            <tr>
            <td>SGDT Interventi Educazionali</td>
            <td>ValueSet relativo alla codifica degli interventi educazionali</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-InterventiEducazionali}}
            </td>
            </tr>
            <tr>
            <td>SGDT Modalità Erogazione Int Edu</td>
            <td>
                ValueSet relativo alla modalità di erogazione
                dell'intervento educazionale
            </td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ModalitaErogazioneIntEdu}}
            </td>
            </tr>
            <tr>
            <td>SGDT Obiettivi Salute</td>
            <td>ValueSet relativo agli obiettivi salute</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-ObiettiviSalute}}
            </td>
            </tr>
            <tr>
            <td>SGDT Percorsi CDom</td>
            <td>ValueSet relativo ai percorsi di cure domiciliari</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-PercorsiCDom}}
            </td>
            </tr>
            <tr>
            <td>SGDT Qualifica Professionista Sanitario</td>
            <td>ValueSet relativo alla qualifica del professionista sanitario</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-QualificaProfessionistaSanitario}}
            </td>
            </tr>
            <tr>
            <td>SGDT Stili Vita</td>
            <td>ValueSet relativo agli stili di vita</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-StiliVita}}
            </td>
            </tr>
            <tr>
            <td>SGDT Tipologia Esenzioni</td>
            <td>ValueSet relativo alla tipologia di esenzioni</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaEsenzioni}}
            </td>
            </tr>
            <tr>
            <td>SGDT Tipologia Ossigeno</td>
            <td>ValueSet relativo alla tipologia di ossigenoterapia</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaOssigeno}}
            </td>
            </tr>
            <tr>
            <td>SGDT Tipologia Patologia</td>
            <td>CodeSystem che identifica la tipologia di patologia</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaPatologia}}
            </td>
            </tr>
            <tr>
            <td>SGDT Tipologia Valutazione</td>
            <td>ValueSet relativo alla tipologia di valutazione</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaValutazione}}
            </td>
            </tr>
            <tr>
            <td>SGDT Valutazione</td>
            <td>ValueSet relativo alla codifica delle valutazioni specifiche</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-Valutazione}}
            </td>
            </tr>
            <tr>
            <td>SIAD Causale Dimissione</td>
            <td>ValueSet relativo alla causale di dimissione</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-CausaleDimissione}}
            </td>
            </tr>
            <tr>
            <td>SIAD Modalità Erogazione</td>
            <td>ValueSet relativo alla modalità di erogazione</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ModalitaErogazione}}
            </td>
            </tr>
            <tr>
            <td>SIAD Tipologia Di Luogo</td>
            <td>
                ValueSet relativo alla tipologia di luogo in cui
                vengono erogate le prestazioni di cure domiciliari
            </td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipologiaDiLuogo}}
            </td>
            </tr>
            <tr>
            <td>SIAD Posizione Professione</td>
            <td>ValueSet relativo alla codifica della posizione professionale</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-PosizioneProfessione}}
            </td>
            </tr>
            <tr>
            <td>SIAD Proponente PIC</td>
            <td>
                ValueSet relativo alla codifica del soggetto che ha
                proposto la presa in carico
            </td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ProponentePIC}}
            </td>
            </tr>
            <tr>
            <td>SIAD Responsabilità Genitoriale</td>
            <td>
                ValueSet relativo alla codifica delle
                responsabilità genitoriale
            </td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ResponsabilitaGenitoriale}}
            </td>
            </tr>
            <tr>
            <td>SIAD Situazione Pensionistica</td>
            <td>ValueSet relativo alla codifica della situazione pensionistica</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-SituazionePensionistica}}
            </td>
            </tr>
            <tr>
            <td>SIAD Stato Civile</td>
            <td>ValueSet relativo alla codifica dello stato civile</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-StatoCivile}}
            </td>
            </tr>
            <tr>
            <td>SIAD Tipo Accesso</td>
            <td>ValueSet relativo alla codifica del tipo di accesso</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipoAccesso}}
            </td>
            </tr>
            <tr>
            <td>SIAD Tipologia Operatori ADI</td>
            <td>ValueSet relativo alla tipologia di operatore ADI</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipoOperatore}}
            </td>
            </tr>
            <tr>
            <td>SIAD Tipologia Paziente</td>
            <td>ValueSet relativo alla codifica della tipologia del paziente</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TipologiaPaziente}}
            </td>
            </tr>
            <tr>
            <td>SIAD Titolo Studio</td>
            <td>ValueSet relativo alla codifica del titolo di studio</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-TitoloStudio}}
            </td>
            </tr>
            <tr>
            <td>SGDT Tipologia Prestazione</td>
            <td>ValueSet relativo alla tipologia di prestazione</td>
            <td>
                {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-TipologiaPrestazione}}
            </td>
            </tr>
        </tbody>
        </table>
  </body>
</html>
