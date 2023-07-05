# {{page-title}}

<div class="alert alert-info">
Il contenuto del sito rappresenta la Guida di Implementazione del progetto FHIR per Regione Lombardia.
</div>

## Novità
La versione corrente della guida implementativa, che fa riferimento all'ultimo rilascio in ambiente di <b>produzione</b>, gestisce i seguenti concetti:

- Sono state apportate le seguenti modifiche per il profilo RLCarePlanProgettoIndividuale o per i profili in esso referenziati: 
  - Sostituzione dei profili “RLConditionPatologiaPrimariaSecondariaUlteriore” e “RLConditionProblemaInfermieristico  con il profilo “RLConditionProblemiSalute”.
  - Il code-system “SGDT Prestazioni Infermieristiche” è stato spostato all’interno del value-set “Prestazioni".
  - Diventati facoltativi i seguenti campi: “contributor” in RLCarePlanProgettoIndividuale che corrisponde al case
    manager del progetto individuale, “author” in RLQuestionnaireResponseValutazione e “performer” in RLObservationEsitoValutazione che corrispondono al professionista sanitario che ha effettuato la valutazione, “organization” in RLPractitionerRoleMedicoPrescrittore, “addresses” e “note” in RLGoalObiettiviSalute.
  - Eliminato il campo “route” in RLMedicationRequestTerapiaFarmacologica.

- Sono stati revisionati i seguenti gli esempi ad una specifica tipologia di ricerca:
  - Ricerca prestazioni erogate;
  - Ricerca progetti individuali attivi;
  - Ricerca rivalutazioni e sospensioni;
  - Ricerca rivalutazioni;
  - Ricerca sospensioni;
  - Ricerca storico progetti individuali;
  - Ricerca valutazioni;
  - Ricerca enti erogatori accreditati nell’ambito territoriale di una ASST di una specifica tipologia.

- Nel value-set “SGDT Percorsi CDom” è stato aggiunto il valore “Liv III C autorizzato”.
  Nel value-set “SGDT Motivo Segnalazione” sono stati aggiunti i seguenti valori:
  - Inviato da PS
  - Presa in carico proattiva
  - Inviato da Enti locali
  - Inviato da IFEC
  - Inviato da Assistente Sociale
  - Inviato da Medico di distretto
  - Inviato da Ospedale
  - Inviato da COT
  - Inviato da Centro Servizi

Per il dettaglio esaustivo delle precedenti versioni della guida rilasciate è possibile fare riferimento al seguente [link](https://simplifier.net/guide/ig-rlfhir-versionhistory/home?version=current).

## Come leggere questa guida
Questa guida presenta diverse sezioni che sono elencate nella barra dei menù, presente nella parte alta di ciascuna pagina.
- **Home**: la presente pagina, nonché la pagina iniziale della Implementation Guide.
- **Contesto**: contiene diverse pagine relative al contesto del progetto e alle tematiche di applicazione.
- **Profili ed Estensioni**: contiene la pagina della libreria di tutti i profili e quella di tutte le estensioni implementate.
- **Terminologia**: raccoglie la libreria di tutti i value set, ovvero le codifiche utilizzate nei profili.
- **Esempi**: contiene la pagina con la libreria completa degli esempi.