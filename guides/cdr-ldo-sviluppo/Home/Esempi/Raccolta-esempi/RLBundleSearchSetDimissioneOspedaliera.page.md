# Esempio di ricerca di specifiche osservazioni per un determinato paziente e contesto ospedaliero

Recupero dei dati relativi alle osservazioni fatte durante un ricovero di uno specifico paziente.

Parametri obbligatori:
- *patient.identifier=[identificativo paziente]*: da valorizzare con l'identificativo del paziente soggetto delle osservazioni, ad esempio il codice fiscale
- *code=[LOINC]*: da valorizzare per identificare il tipo di osservazioni che si vuole recuperare, è possibile utilizzare '8648-8' (Decorso ospedaliero), '8646-2' (Motivo del ricovero generico), '46241-6' (Motivo del ricovero non strutturata), '8651-2' (Diagnosi alla dimissione generico), '11535-2'(Diagnosi alla dimissione non strutturata).


Parametri opzionali:
- *date=gt[data ricerca]:* da valorizzare con la data (nel formato YYYY-MM-DD) da cui cominciare la ricerca
- *date=lt[data di ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) finale più recente in cui fare la ricerca
- *_has:Provenance:target:agent:_has:Organization.identifier=[codice azienda]*: identificativo aziendale (custodian del documento)

Inoltre, è possibile aggiungere opzionalmente ulteriori risorse alla richiesta utilizzando lo strumento FHIR search 'include' e 'revinclude'. Sono riportati i dettagli dei parametri che possono essere aggiunti alla richiesta:
- *_revinclude=Provenance:target* : include nella risposta la risorsa Provenance che contiene le informazioni sul documento da cui è stata estratta l'informazione.
- *_include=Provenance:agent* : include nella risposta la risorsa PractitionerRole e Organization che sono referenziati all'interno di Provenance dall'attributo *agent*. 
- *_include=PractitionerRole:practitioner &_include=PractitionerRole:organization*: include nella risposta le informazioni sul Medico (Practitioner) e Azienda (Organization) referenziati dai PractitionerRole inclusi nella richiesta.
- *_include=AllergyIntorance:encounter*: questo permette di includere la risorsa Encounter che contiene le informazioni sulle allergie segnalate durante il ricovero.

**Richiesta:** 

| SCOPE |  Ricerca delle osservazioni cliniche di un paziente in un determinato contesto clinico |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Observation?code=8651-2&date=gt2020-01-01&date=lt2025-01-01&patient.identifier=RSSMRA80A01F205X&_has:Provenance:target:agent:_has:Organization.identifier=030712&_revinclude=Provenance:target&_include=observation:patient&_include=Observation:encounter&_include=PractitionerRole:practitioner &_include=PractitionerRole:organization |
|Descrizione risposta | Restituirà tutte le osservazioni del paziente con codice fiscale RSSMRA80A01F205X e in regime di dimissione ospedaliera, insieme alle informazioni del paziente, <br> al documento da cui sono estratte le informazioni, al medico e all'organizzazione responsabili dell'osservazione e all'evento clinico in cui sono state prodotte. |

**Risposta**

{{json:Bundle/bundle-recupero-osservazioni-dimissione-ospedaliera}}
