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

La versione corrente della guida implementativa, che fa riferimento all'ultimo rilascio in ambiente di produzione, gestisce i seguenti concetti:

 - È stato descritto il nuovo scenario di cooperazione applicativa tra le Cartelle Elettroniche in uso dai Medici di Medicina Generale (CE-MMG) per la gestione dei pazienti cronici e il SGDT. Nella sezione Contesto sono state aggiornate le pagine.
  - Panoramica di progetto;
  - Tematiche di applicazione;
  - Paradigmi di integrazione e API RestFUL.
 - Nella sezione Profili ed Estensioni sono stati aggiunti i profili RLMessageHeaderMMG, RLPatientBase, RLOperationOutcomeMMG, RLBundleMMG, RLBundleRispostaMMG e RLServiceRequestPrestazioni.
 - Nel profilo RLConditionProblemiSalute è stato aggiunto il campo “severity”, è stato aggiornato il campo “code” ed è stata aggiornata la cardinalità del campo “meta”.
 - Nel profilo RLMedicationRequestTerapiaFarmacologica è stato aggiunto il campo “text”, è stato aggiornato il campo “medication” ed è stata aggiornata la cardinalità del campo “meta” e “basedOn”.
 - Nel profilo RLCarePlanProgettoIndividuale è stato aggiornato l’esempio della chiamata per la ricerca dei Progetti Individuali attivi.
 - Nel profilo RLOrganizationL2 è stata aggiornata la descrizione e aggiunto il parametro “dataCessazione” per alcune tipologie di ricerca.
 - Nel profilo RLGoalObiettiviSalute sono state aggiornate le descrizioni dei campi “description” e “note”.
 - Nella sezione Terminologia sono stati aggiunti i seguenti value-set:
  - SGDT MessageEvents;
  - GPC LivelloGravita;
  - GPC ContenutoOperationOutcomeMMG;
  - SGDT operation error;
  - SGDT Tipologia Prestazione.
 - Nella sezione Esempi sono stati aggiunti i seguenti esempi:
  - Esempio Bundle di attivazione dei servizi di presa in carico dei pazienti cronici da parte del MMG;
  - Esempio Bundle di richiesta di interventi di Assistenza Domiciliare Programmata da parte del MMG;
  - Esempio Bundle Risposta del messaggio con esito positivo;
  - Esempio Bundle Risposta del messaggio con errore.


Per il dettaglio esaustivo delle precedenti versioni della guida rilasciate è possibile fare riferimento al seguente [link](https://simplifier.net/guide/ig-rlfhir-versionhistory/home?version=current).

## Come leggere questa guida
Questa guida presenta diverse sezioni che sono elencate nella barra dei menù, presente nella parte alta di ciascuna pagina.
- **Home**: la presente pagina, nonché la pagina iniziale della Implementation Guide.
- **Contesto**: contiene diverse pagine relative al contesto del progetto e alle tematiche di applicazione.
- **Profili ed Estensioni**: contiene la pagina della libreria di tutti i profili e quella di tutte le estensioni implementate.
- **Terminologia**: raccoglie la libreria di tutti i value set, ovvero le codifiche utilizzate nei profili.
- **Esempi**: contiene la pagina con la libreria completa degli esempi.
  
