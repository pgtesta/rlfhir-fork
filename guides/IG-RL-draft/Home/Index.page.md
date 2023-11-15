# {{page-title}}

<div class="alert alert-warning">
Questa pagina è da considerare IN LAVORAZIONE. 

Il contenuto del sito rappresenterà a regime la Guida di Implementazione del progetto FHIR per Regione Lombardia. 

Attualmente viene descritta una panoramica del progetto \[si veda {{pagelink:Home/Contesto/Panoramica-di-progetto.page.md}}\], 
ed è possibile consultare le risorse FHIR rilasciate e attualmente in uso.
</div>

<div class="alert alert-danger">
Questa guida di implementazione fa riferimento all'ambiente di <b>test</b>, di conseguenza le risorse potrebbero essere soggette a revisione e modifiche.
</div>

## Novità
La versione corrente della guida implementativa, che fa riferimento all'ultimo rilascio in ambiente di <b>produzione</b>, gestisce i seguenti concetti:

- È stata aggiunta una nuova valutazione denominata "Campi extra del flusso SIAD" relativa alle informazioni presenti nel flusso SIAD che non appartengono alla scheda SIAD semplificata. I campi della nuova valutazione sono:
  - Indicatore supporto sociale;
  - Presenza di assistente non familiare;
  - Cognitività;
  - ECG;
  - Telemetria;
  - Assistenza Stato di terminalità oncologica;
  - Assistenza Stato di terminalità non oncologica;
  - Trasfusioni;
  - Uso dei servizi igienici;
  - Abbigliamento.
- Nel profilo RLPatientCittadino sono stati aggiunti i campi relativi ai contatti del paziente, al caregiver e alla locazione temporanea.
- Nel profilo RLGoalObiettiviSalute è stato aggiunto il campo “category” per indicare l’ambito degli obiettivi di salute con la relativa nuova codifica
- Nel profilo RLServiceRequestServiziSocioAssistenziali è stato aggiunto il campo extension medicoPrescrittore che verrà valorizzato con il codice regionale del medico,  mentre nel campo “requisition” è stato aggiunto il codice della ricetta medica e la sua data di decorrenza.
- Nel profilo RLProcedurePrestazione sono stati resi obbligatori i campi extension dataPresaInCarico, numeroAccesso, modalitaErogazione, tipoAccesso.
- Nel profilo RLQuestionnaireResponseValutazione è stato aggiunto un codice identificativo alle risposte di tutte le domande delle valutazioni eccetto per la valutazione InterRAI HomeCare.
- Nel value-set “SGDT Percorsi CDom” è stato aggiunto il percorso “Trattamenti Terapeutici” e sono stati modificati alcuni codici dei percorsi.
- Nel value-set “SGDT Motivo Segnalazione” è stato cambiato il testo di alcune voci. 
- Nel value-set “SGDT Valutazione” è stata aggiunta la valutazione “Campi extra del flusso SIAD”.
- È stato revisionato l’esempio “Ricerca rivalutazioni e sospensioni” aggiungendo il campo “system” nel campo “identifier” dei profili “RLServiceRequestSospensioneADI” e “RLServiceRequestRivalutazione”;
- Sono stati revisionati gli esempi per allinearli alle nuove modifiche;
- Nel profilo RLQuestionnaireResponseValutazione sono stati aggiunti due campi extension a testo libero LuogoValutazione e PartecipantiValutazione;
- Nel value-set "SGDT Qualifica Professionista Sanitario" è stato aggiunto il valore PROFSAN22 = Medico Specialista;
- Nella sezione Terminologia è stata aggiunta la pagina "Anagrafica delle schede di valutazione" contenente le tabelle delle domande e delle risposte con il corrispettivo identificativo delle valutazioni "Scheda Triage", "Scheda semplificata SIAD" e "Campi extra del flusso SIAD".


Per il dettaglio esaustivo delle precedenti versioni della guida rilasciate è possibile fare riferimento al seguente [link](https://simplifier.net/guide/ig-rlfhir-versionhistory/home?version=current).

## Come leggere questa guida
Questa guida presenta diverse sezioni che sono elencate nella barra dei menù, presente nella parte alta di ciascuna pagina.
- **Home**: la presente pagina, nonché la pagina iniziale della Implementation Guide.
- **Contesto**: contiene diverse pagine relative al contesto del progetto e alle tematiche di applicazione.
- **Profili ed Estensioni**: contiene la pagina della libreria di tutti i profili e quella di tutte le estensioni implementate.
- **Terminologia**: raccoglie la libreria di tutti i value set, ovvero le codifiche utilizzate nei profili.
- **Esempi**: contiene la pagina con la libreria completa degli esempi.
  

