# {{page-title}}

## Paradigma FHIR RESTful
Il modello di interoperabilità REST in standard FHIR prevede l’interscambio di informazioni tra un generico “richiedente” (Client) e un generico “espositore” (Server): 

- Il server FHIR espone le Risorse/Profili su specifici punti di accesso (endpoint) raggiungibili con il protocollo https. 
- Il client FHIR può eseguire le chiamate di interesse agli endpoint dove sono presenti le interfacce programmatiche API (Application Programming Interface) che implementano, in modo semplice e snello conforme all’approccio RESTful, i metodi di fruizione dei dati esposti. 

Tale modalità di consultazione dei dati è definita “logica PULL”, e prevede esclusivamente chiamate di tipo GET per consultare i dati esposti. Il risultato di ogni chiamata è la produzione di una risorsa bundle. Questa risorsa ha lo scopo di raccogliere una serie di Risorse/Profili FHR sulla base dei parametri di ricerca utilizzati nella chiamata GET. 

Mentre, l'interazione che permette di creare una nuova risorsa, in una posizione assegnata dal server, avviene tramite una richiesta HTTPs POST.

## Creazione
### API Manager
L'API Manager espone i servizi FHIR definiti nell'ecosistema di Regione Lombardia. Il base_url con cui accedere a tali servizi è il seguente:
 
        <base_API_Manager> = [QUI CI SARà l'ENDPOINT DELL'API MANAGER]
  

L'elenco delle API esposte è:

|Metodo HTTP|URL|Nome profilo|Detentore del dato|
|---|---|---|
|POST|<base_API_Manager>/_Bundle_|RLBundleNuovoAccessoPaz|ADT/CCE|
|POST|<base_API_Manager>/_Bundle_|RLBundleTrasferimentoPaz|ADT/CCE|
|POST|<base_API_Manager>/_Bundle_|RLBundleDimissionePaz|ADT/CCE|

## Consultazione


|Metodo HTTP|URL|Nome profilo|Detentore del dato|
|---|---|---|
|GET|<base_API_Manager>/Encounter?patient.identifier=[idPaziente]&location-period=gt[data inizio]&location-period=lt[data fine]&_include=location:Location|-|CDR|
|GET|<base_API_Manager>/Encounter?location=location.identifier=[IDLETTO]|-|CDR|
|GET|<base_API_Manager>Encounter?identifier=[idEpisodio]&patient.identifier=[idpz]|-|CDR|


**1. Tempi medi di occupazione per posto-letto**: numero medio di giorni durante i quali un letto è occupato da un paziente in un determinato periodo.
La query filtra le risorse encounter sulla base dell'idPaziente a cui è associato, tramite l'attributo "subject", con riferimento a risorsa di tipo Patient. I risultati vengono ulteriormente selezionati sulla base del periodo di ricovero di interesse. In output si ottengono le location ( posto letto ) occupati.

**2. Intervalli di turn over**: tempo medio che intercorre tra la dimissione di un paziente e l'ammissione di un nuovo paziente nello stesso letto;
Si applica un filtro sull'id del posto letto ricercato e si ottiene in output la risorsa Encounter che fa riferimento.

**TODO** : tempi di attesa del posto letto: periodo che intercorre tra la richiesta di un posto letto e l'effettiva assegnazione dello stesso; 

**3. numero di spostamenti per paziente**: numero di volte che un paziente viene trasferito da un letto o reparto all'altro durante la sua degenza. Si effettua un filtro sia sull'identificativo del paziente, sia numero di identificativo del ricovero a cui fa riferimento la statistica.
