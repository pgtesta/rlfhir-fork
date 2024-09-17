# {{page-title}}

## Paradigma FHIR RESTful
Il modello di interoperabilità REST in standard FHIR prevede l’interscambio di informazioni tra un generico “richiedente” (Client) e un generico “espositore” (Server): 

- Il server FHIR espone le Risorse/Profili su specifici punti di accesso (endpoint) raggiungibili con il protocollo https. 
- Il client FHIR può eseguire le chiamate di interesse agli endpoint dove sono presenti le interfacce programmatiche API (Application Programming Interface) che implementano, in modo semplice e snello conforme all’approccio RESTful, i metodi di fruizione dei dati esposti. 

Tale modalità di consultazione dei dati è definita “logica PULL”, e prevede esclusivamente chiamate di tipo GET per consultare i dati esposti. Il risultato di ogni chiamata è la produzione di una risorsa bundle. Questa risorsa ha lo scopo di raccogliere una serie di Risorse/Profili FHR sulla base dei parametri di ricerca utilizzati nella chiamata GET. 

Mentre, l'interazione che permette di creare una nuova risorsa, in una posizione assegnata dal server, avviene tramite una richiesta HTTPs POST.

## Consultazione


Num Richiesta|Metodo HTTP|URL|Esempio|Detentore del dato|
|---|---|---|---|
|1|GET|<base_API_Manager>/Bundle?identifier=[id univoco del documento]|-|CDR|
|2|GET|<base_API_Manager>/Bundle?composition.subject=[identificativo paziente]&composition.date=gt[data di ricerca]&composition.date=lt[data di ricerca]&composition.code=11506-2|-|CDR|
|3|GET|<base_API_Manager>Observation?date=gt[data ricerca]&date=lt[data ricerca]&category=laboratory&_include=Observation:patient&patient.identifier=[identificativo paziente]&_include=Observation:specimen&_include:iterate=Observation:performer&_revinclude:iterate=Provenance:target&
_include:iterate=Provenance:agent&_include=PractitionerRole:practitioner &_include=PractitionerRole:organization&_include=Observation:encounter|-|CDR|
|4|GET|<base_API_Manager>Observation?code=[codice esame]date=gt[data ricerca]&date=lt[data ricerca]&category=laboratory&_include=Observation:patient&patient.identifier=[identificativo paziente]&_include=Observation:specimen&_include:iterate=Observation:performer&_revinclude:iterate=Provenance:target&
_include:iterate=Provenance:agent&_include=PractitionerRole:practitioner &_include=PractitionerRole:organization&_include=Observation:encounter-|CDR|

### Richiesta 1
Recupero di un FHIR document tramite il suo identificativo univoco.
Parametri obbligatori:
- *identifier=[id univoco del documento]*: identificativo univoco del documento secondo la sintassi FHIR: *\[value\]|\[system\]*

### Richiesta 2
Recupero dei referti di medicina di laboratorio in FHIR di uno specifico paziente.

Parametri obbligatori:
- *composition.subject=[identificativo paziente]*: da valorizzare con l'identificativo del paziente soggetto del documento, ad esempio il codice fiscale;
- *composition.code=11506-2*: selezione dei FHIR document tra quelli di laboratorio
- *composition.date=gt[data di ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) da cui cominciare la ricerca

Parametri opzionali:
- *composition.date=lt[data di ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) finale più recente in cui fare la ricerca

### Richiesta 3
Recupero risultati degli esami di laboratorio di uno specifico paziente.

Parametri obbligatori:
- *patient.identifier=[identificativo paziente]*: da valorizzare con l'identificativo del paziente soggetto delle osservazioni, ad esempio il codice fiscale
- *_include=Observation:patient*: include nella risposta la risorsa Patient
- *category=laboratory*: selezione delle osservazioni provenienti da referti di medicina di laboratorio
- *date=gt[data ricerca]:* da valorizzare con la data (nel formato YYYY-MM-DD) da cui cominciare la ricerca

Parametri opzionali:
- *date=lt[data di ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) finale più recente in cui fare la ricerca

Inoltre, è possibile aggiungere opzionalmente ulteriori risorse alla richiesta utilizzando lo strumento FHIR search 'include' e 'revinclude'. Sono riportati i dettagli dei parametri che possono essere aggiunti alla richiesta:
- *_include=Observation:specimen* : include nella risposta la risorsa Specimen che contiene l'informazione sul campione di laboratorio che ha prodotto il risultato.
- *_revinclude=Provenance:target* : include nella risposta la risorsa Provenance che contiene le informazioni sul documento da cui è stata estratta l'informaizone.
- *_include:iterate=Provenance:agent* : include nella risposta la risorsa PractitionerRole e Organization che sono referenziati all'interno di Provenance. Questi rappresentano il custodian del documento (azienda responsabile dell'osservazione - Organization) e il firmatario del documento (PractitionerRole).
- *_include=Observation:performer*: include nella risposta la risorsa PractitionerRole del responsabile dell'osservazione.
- *_include=PractitionerRole:practitioner &_include=PractitionerRole:organization*: include nella risposta le informazioni sul Medico (Practitioner) e Azienda (Organization) referenziati dai PractitionerRole inclusi nella richiesta.
- *_include=Observation:encounter*: questo permette di includere la risorsa Encounter che contiene le informazioni sull'identificativo dell'episodio, se presente, in cui è stato prodotto il referto e il regime di assistenza del paziente al momento dell'esame.


### Richiesta 4
Recupero risultati di uno specifico esame di laboratorio di uno specifico paziente.

Parametri obbligatori:
- *_include=Observation:patient&patient.identifier=[identificativo paziente]*: da valorizzare con l'identificativo del paziente soggetto delle osservazioni, ad esempio il codice fiscale;
- *category=laboratory*: selezione delle osservazioni provenienti da referti di medicina di laboratorio
- *code=[codice esame]*: da valorizzare con il codice LOINC dell'esame di cui si vuole avere l'andamento
- *date=gt[data ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) da cui cominciare la ricerca

Parametri opzionali:
- *date=lt[data di ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) finale più recente in cui fare la ricerca
- *_include=Observation:specimen: da inserire se si vuole ottenere anche l'informazione sul campione di laboratorio che ha prodotto il risultato

Inoltre, è possibile aggiungere opzionalmente ulteriori risorse alla richiesta utilizzando lo strumento FHIR search 'include' e 'revinclude'. Sono riportati i dettagli dei parametri che possono essere aggiunti alla richiesta:
- *_include=Observation:specimen* : include nella risposta la risorsa Specimen che contiene l'informazione sul campione di laboratorio che ha prodotto il risultato.
- *_revinclude=Provenance:target* : include nella risposta la risorsa Provenance che contiene le informazioni sul documento da cui è stata estratta l'informaizone.
- *_include:iterate=Provenance:agent* : include nella risposta la risorsa PractitionerRole e Organization che sono referenziati all'interno di Provenance. Questi rappresentano il custodian del documento (azienda responsabile dell'osservazione - Organization) e il firmatario del documento (PractitionerRole).
- *_include=Observation:performer*: include nella risposta la risorsa PractitionerRole del responsabile dell'osservazione.
- *_include=PractitionerRole:practitioner &_include=PractitionerRole:organization*: include nella risposta le informazioni sul Medico (Practitioner) e Azienda (Organization) referenziati dai PractitionerRole inclusi nella richiesta.
- *_include=Observation:encounter*: questo permette di includere la risorsa Encounter che contiene le informazioni sull'identificativo dell'episodio, se presente, in cui è stato prodotto il referto e il regime di assistenza del paziente al momento dell'esame.
