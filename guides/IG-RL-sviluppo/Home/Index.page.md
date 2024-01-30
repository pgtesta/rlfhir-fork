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

- Per il profilo “RLConditionProblemiSalute” è stato aggiunto il value-set “SGDT Patologie Non ICD9-CM” visualizzabile nella sezione “Libreria ValueSet”. Questa tabella raccoglie le patologie che presentano una codifica non standard differente dalla ICD9-CM.
- Nella sezione “Anagrafica delle schede di valutazione” è stata aggiunta la domanda “Contributo al caregiver familiare” per la valutazione “Campi extra del flusso SIAD”. Questa domanda viene valorizzata solo se la condizione clinica prevalente è “Paziente in Stato Vegetativo (DGR 6220)” o “Paziente affetto da malattie del motoneurone (circ. 20)”.
- Nella sezione “Stati ed Errori” è stato aggiunto l’errore “504 Gateway Time-Out”. Questo errore viene generato in caso in cui il tempo di composizione del bundle superi il limite temporale di soglia. Il sistema termina comunque la composizione e memorizza il bundle per un periodo limitato di tempo. Dunque, effettuando la stessa chiamata di consultazione la risposta risulta immediata. 


Per il dettaglio esaustivo delle precedenti versioni della guida rilasciate è possibile fare riferimento al seguente [link](https://simplifier.net/guide/ig-rlfhir-versionhistory/home?version=current).

## Come leggere questa guida
Questa guida presenta diverse sezioni che sono elencate nella barra dei menù, presente nella parte alta di ciascuna pagina.
- **Home**: la presente pagina, nonché la pagina iniziale della Implementation Guide.
- **Contesto**: contiene diverse pagine relative al contesto del progetto e alle tematiche di applicazione.
- **Profili ed Estensioni**: contiene la pagina della libreria di tutti i profili e quella di tutte le estensioni implementate.
- **Terminologia**: raccoglie la libreria di tutti i value set, ovvero le codifiche utilizzate nei profili.
- **Esempi**: contiene la pagina con la libreria completa degli esempi.
  
