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
La versione corrente della guida implementativa ha recepito e gestisce attraverso la progettazione dei profili e dei relativi criteri di ricerca i seguenti concetti:
- inclusione delle valutazioni effettuate dal paziente nel bundle di risorse contenute in fase di consultazione di un progetto individuale (si veda il criterio di ricerca ”progetti individuali attivi” del profilo RLCarePlanProgettoIndividuale).
- gestione di due percorsi di cure domiciliari attivati ad un paziente nell’ambito di una stessa pratica e definiti all’interno del progetto individuale (si veda la mappatura della risorsa RLServiceRequestServiziSocioAssistenziali)

## Come leggere questa guida
Questa guida presenta diverse sezioni che sono elencate nella barra dei menù, presente nella parte alta di ciascuna pagina.
- **Home**: la presente pagina, nonché la pagina iniziale della Implementation Guide.
- **Contesto**: contiene diverse pagine relative al contesto del progetto e alle tematiche di applicazione.
- **Profili ed Estensioni**: contiene la pagina della libreria di tutti i profili e quella di tutte le estensioni implementate.
- **Terminologia**: raccoglie la libreria di tutti i value set, ovvero le codifiche utilizzate nei profili.
- **Esempi**: contiene la pagina con la libreria completa degli esempi.
- **Contatti**: in questa sezione è possibile recuperare le informazioni di contatto utili
- **Dowload**: da questa pagina è possibile scaricare l'ultimo package fhir rilasciato, oltre a trovare altri riferimenti a documentazione esterne.
  

