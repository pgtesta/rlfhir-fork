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
La versione corrente della guida implementativa gestisce i seguenti concetti:
- Inclusione dei distretti di accreditamento e della relativa ASST e ATS di afferenza per gli enti erogatori di
  servizi sociosanitari (si veda la mappatura della risorsa RLOrganizationL2).
- Inclusione dell’indirizzo di domicilio nella risorsa RLPatientCittadino ed eliminazione dei campi
  reponsabilitàGenitoriale ed ATSResidenza (rimappata nel campo generalPractitioner).
- Inclusione del numero di telefono ed indirizzo dell’ambulatorio nella risorsa RLPractitionerRoleMedicoPrescritore. 
- Inclusione del campo note nella risorsa RLServiceRequestRivalutazione.
- Revisione dei seguenti value-set: “Codifica della causale di dimissione di un ricovero domiciliare”, “Codifica del
  soggetto che ha proposto la presa in carico”, “Codifica dei motivi della sospensione temporanea del ricovero domiciliare”, “Codifica delle prestazioni infermieristiche”, “Codifica della responsabilità genitoriale”, “Codifica delle prestazioni dei servizi di cure domiciliari”, “Codifica delle qualifiche dei medici prescrittori”.
- Eliminato il value-set “Codifica della responsabilità genitoriale”.
- Inclusione dei profili relativi al caso d'uso "Posti Letto Occupati".


Per il dettaglio esaustivo delle precedenti versioni della guida rilasciate è possibile fare riferimento al seguente [link](https://simplifier.net/guide/ig-rlfhir-versionhistory/home?version=current).

## Come leggere questa guida
Questa guida presenta diverse sezioni che sono elencate nella barra dei menù, presente nella parte alta di ciascuna pagina.
- **Home**: la presente pagina, nonché la pagina iniziale della Implementation Guide.
- **Contesto**: contiene diverse pagine relative al contesto del progetto e alle tematiche di applicazione.
- **Profili ed Estensioni**: contiene la pagina della libreria di tutti i profili e quella di tutte le estensioni implementate.
- **Terminologia**: raccoglie la libreria di tutti i value set, ovvero le codifiche utilizzate nei profili.
- **Esempi**: contiene la pagina con la libreria completa degli esempi.
  
