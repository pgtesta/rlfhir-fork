# {{page-title}}

<div class="alert alert-warning">
Questa pagina è da considerare IN LAVORAZIONE. 

Il contenuto del sito rappresenterà a regime la Guida di Implementazione del progetto FHIR per Regione Lombardia. 

Attualmente viene descritta una panoramica del progetto \[si veda {{pagelink:Home/Contesto/Panoramica-di-progetto.page.md}}\], 
ed è possibile consultare le risorse FHIR rilasciate e attualmente in uso.
</div>

<div class="alert alert-danger">
Questa guida di implementazione fa riferimento all'ambiente di <b>sviluppo</b>, di conseguenza le risorse potrebbero essere soggette a revisione e modifiche.
</div>

## Novità

La versione corrente della guida implementativa, che fa riferimento all'ultimo rilascio in ambiente di produzione, presenta le seguenti novità:
- È stato descritto il nuovo scenario di cooperazione applicativa tra l'applicativo di gestione 1116117 NEA e SGDT per trasmettere alla rete delle COT in maniera integrata la richiesta di attivazione di un servizio socio-assistenziale. Nella sezione Contesto sono state aggiornate le pagine:
   - Panoramica di progetto;
   - Tematiche di applicazione;
   - Paradigmi di integrazione e API RESTful.
- Nella sezione Profili ed Estensioni sono stati aggiunti i profili RLDocumentReferenceDocumento, RLMessageHeaderNEA, RLOperationOutcomeNEA, RLBundleNEA, RLBundleRispostaNEA e RLBundleStatoNEA.
- Nella sezione Profili ed Estensioni sono stati aggiornati i profili RLServiceRequestServiziSocioAssistenziali, RLPatientCittadino, RLPractitionerRoleProfessionistaSanitario, RLPractitionerProfessionistaSanitario.
- Nella sezione Terminologia sono stati aggiornati i seguenti value-set:
   - DDC Desc L2;
   - SGDT Motivo Segnalazione;
   - Tipologia Evento Messaggio;
   - Errori Messaggio.
- Nella sezione Esempi sono stati aggiunti i seguenti esempi:
   - Esempio Bundle NEA di richiesta di attivazione di un servizio socio-assistenziale da parte dell'applicativo di gestione 116117 NEA;
   - Esempio Bundle Risposta NEA del messaggio con esito positivo;
   - Esempio Bundle Risposta NEA del messaggio con errore;
   - Esempio Bundle Stato NEA per richiedere alla piattaforma SGDT lo Stato della richiesta da parte dell'applicativo di gestione 116117 NEA.


Per il dettaglio esaustivo delle precedenti versioni della guida rilasciate è possibile fare riferimento al seguente [link](https://simplifier.net/guide/ig-rlfhir-versionhistory/home?version=current).

## Come leggere questa guida
Questa guida presenta diverse sezioni che sono elencate nella barra dei menù, presente nella parte alta di ciascuna pagina.
- **Home**: la presente pagina, nonché la pagina iniziale della Implementation Guide.
- **Contesto**: contiene diverse pagine relative al contesto del progetto e alle tematiche di applicazione.
- **Profili ed Estensioni**: contiene la pagina della libreria di tutti i profili e quella di tutte le estensioni implementate.
- **Terminologia**: raccoglie la libreria di tutti i value set, ovvero le codifiche utilizzate nei profili.
- **Esempi**: contiene la pagina con la libreria completa degli esempi.
  
