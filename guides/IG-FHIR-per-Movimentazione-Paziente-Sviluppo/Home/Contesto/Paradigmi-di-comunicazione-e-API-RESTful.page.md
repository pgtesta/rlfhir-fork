# {{page-title}}

## Paradigma FHIR RESTful
Il modello di interoperabilità REST in standard FHIR prevede l’interscambio di informazioni tra un generico “richiedente” (Client) e un generico “espositore” (Server): 

- Il server FHIR espone le Risorse/Profili su specifici punti di accesso (endpoint) raggiungibili con il protocollo https. 
- Il client FHIR può eseguire le chiamate di interesse agli endpoint dove sono presenti le interfacce programmatiche API (Application Programming Interface) che implementano, in modo semplice e snello conforme all’approccio RESTful, i metodi di fruizione dei dati esposti. 

Tale modalità di consultazione dei dati è definita “logica PULL”, e prevede esclusivamente chiamate di tipo GET per consultare i dati esposti. Il risultato di ogni chiamata è la produzione di una risorsa bundle. Questa risorsa ha lo scopo di raccogliere una serie di Risorse/Profili FHR sulla base dei parametri di ricerca utilizzati nella chiamata GET. 

Mentre, l'interazione che permette di creare una nuova risorsa, in una posizione assegnata dal server, avviene tramite una richiesta HTTPs POST.

### API Manager
L'API Manager espone i servizi FHIR definiti nell'ecosistema di Regione Lombardia. Il base_url con cui accedere a tali servizi è il seguente:
 
        <base_API_Manager> = [QUI CI SARà l'ENDPOINT DELL'API MANAGER]
  

L'elenco delle API esposte è:

|Metodo HTTP|URL|Nome profilo|Detentore del dato|
|---|---|---|
|POST|<base_API_Manager>/_Bundle_|RLBundleNuovoAccessoPaz|ADT/CCE|
|POST|<base_API_Manager>/_Bundle_|RLBundleTrasferimentoPaz|ADT/CCE|

