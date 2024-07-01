# {{page-title}}


Questa IG definisce il modello dati e le API utilizzate per il caso d’uso “Movimentazione Paziente”, che si instaura nel contesto del Clinical Data Repository (CDR).

<div class="alert alert-info">
Regione Lombardia, al fine di favorire la progettazione di un’architettura integrata con un ecosistema FSE 2.0 orientato ai dati, intende valorizzare il patrimonio informativo sanitario disponibile attraverso la progressiva introduzione, nei contesti aziendali, di Clinical Data Repository (CDR) quali punti di acquisizione e consolidamento dei dati prodotti dai sistemi dipartimentali. 
</div>

La "Movimentazione paziente" permette il monitoraggio degli spostamenti dei pazienti mediante un sistema in grado di raccogliere dati in tempo near real time. L'alimentazione del CDR, per questa finalità, produrrà gli indicatori di interesse (ad esempio tempi medi di occupazione per posto-letto, tempi di attesa del posto letto, ecc.) su dashboard interattive. Il caso d’uso fa riferimento al perimetro aziendale di visibilità dei dati. 

Nello specifico, con movimentazione si intende ogni cambiamento di posto letto tra reparti dello stesso presidio ospedaliero al quale un paziente è sottoposto dal momento del primo accesso in struttura e per tutto il suo percorso di cura.  

I dati raccolti sugli spostamenti tra reparti potranno fornire degli insight utili per valutazioni organizzative e per la programmazione e la gestione delle risorse sanitarie, attuabili attraverso la messa a punto di opportuni KPI di monitoraggio (descritti nel paragrafo Principali funzionalità del servizio), in ottica di ottimizzare la pianificazione relativa ai posti letto e al fine di migliorare l’efficienza del servizio ospedaliero. 

Come servizio per gli utenti, è prevista quindi la creazione di un portale di monitoraggio con cui visualizzare i dati relativi alle movimentazioni dei pazienti, con particolare riferimento alle specificità cliniche del paziente (es. diagnosi associata).  

## Utenti fruitori

Gli utenti identificati come fruitori del caso d’uso sono i seguenti:
- Direzione socio-sanitaria: utilizzano i KPI per prendere decisioni strategiche e operative.
- Direzione sanitaria: utilizzano i KPI per monitorare eventuali pattern clinici e percorsi preferenziali associati a pazienti con determinate diagnosi.

In particolare, un operatore incaricato del monitoraggio dei dati e della messa a disposizione dei KPI (indicati nel paragrafo Principali funzionalità del servizio) aiuterà il personale sanitario di reparto che ne farà richiesta a utilizzare tali dati per motivi logistici e operativi (es. previsione picchi di domanda) e di cura.

## Fonte dato

Per tracciare gli spostamenti dei posti letto intra-aziendali ed alimentare il CDR, verranno utilizzati il sistema **ADT** e la **CCE**.

Il sistema ADT permette di monitorare in tempo reale le ammissioni, i trasferimenti e le dimissioni dei pazienti, assicurando una gestione efficiente e aggiornata dei letti disponibili. 

La CCE, invece, fornirà informazioni cliniche dettagliate sui pazienti (es. diagnosi). 


## Glossario
Raccolta di acronimi e termini usati nel progetto:
 
| Voce | Descrizione |
|---|---|
| DDC | Distribuzione Dati Codificati |
| DP | Dimissione Protette |
| L1 | Codice   identificativo di livello 1 degli enti aderenti al progetto SISS. La risorsa   FHIR che descrive questa tipologia di struttura è _RLOrganizationL1_ |
| L2 | Codice identificativo di livello 2 degli Enti Erogatori di servizi socioassistenziali. La risorsa FHIR che descrive questa tipologia di struttura è _RLOrganizationL2_. |