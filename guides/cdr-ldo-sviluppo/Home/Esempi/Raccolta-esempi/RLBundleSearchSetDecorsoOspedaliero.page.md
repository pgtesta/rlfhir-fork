# Esempio di recupero delle osservazioni relative al decorso ospedaliero di un paziente

Questa ricerca permette di reperire i risultati di una o più osservazioni relative agli esami di laboratorio effettuati da un determinato paziente presso una struttura sanitaria.

Parametri obbligatori:
- *patient.identifier=[identificativo paziente]*: da valorizzare con l'identificativo del paziente soggetto del documento, ad esempio il codice fiscale;
- *code=8648-8*: da valorizzare fisso, rappresenta il codice LOINC del decorso ospedaliero e permette di filtrare a sole queste osservazioni la ricerca.

Parametri opzionali:
- *date=gt[data ricerca]:* da valorizzare con la data (nel formato YYYY-MM-DD) da cui cominciare la ricerca
- *date=lt[data di ricerca]*: da valorizzare con la data (nel formato YYYY-MM-DD) finale più recente in cui fare la ricerca.
- *_has:Provenance:target:agent:_has:Organization.identifier=[codice azienda]*: identificativo aziendale (custodian del documento).

Inoltre, è possibile aggiungere opzionalmente ulteriori risorse alla richiesta utilizzando lo strumento FHIR search 'include' e 'revinclude'. Sono riportati i dettagli dei parametri che possono essere aggiunti alla richiesta:
- *_revinclude=Provenance:target* : include nella risposta la risorsa Provenance che contiene le informazioni sul documento da cui è stata estratta l'informazione.
- *_include=Provenance:agent* : include nella risposta la risorsa PractitionerRole e Organization che sono referenziati all'interno di Provenance dall'attributo *agent*. 
- *_include=PractitionerRole:practitioner &_include=PractitionerRole:organization*: include nella risposta le informazioni sul Medico (Practitioner) e Azienda (Organization) referenziati dai PractitionerRole inclusi nella richiesta.
- *_include=Observation:encounter*: questo permette di includere la risorsa Encounter che contiene le informazioni sul ricovero.

**Richiesta:** 

| SCOPE               | Ricerca di tutte le Observation di un paziente in decorso ospedaliero                                                  |
|---------------------|--------------------------------------------------------------------------------------------------|
| VERB                | GET                                                                                              |
| BASE                | [base_API_Manager]                                                                               |
| URL                 | /Observation?code=8648-8&date=gt2020-01-01&date=lt2025-01-01&patient.identifier=RSSMRA80A01F205X&_has:Provenance:target:agent:_has:Organization.identifier=030712&_revinclude=Provenance:target&_include=observation:patient&_include=Observation:encounter&_include=PractitionerRole:practitioner &_include=PractitionerRole:organization |
| Descrizione risposta | Restituirà tutte le Observation associate al paziente RSSMRA80A01F205X, includendo le informazioni relative al paziente, <br> al documento da cui sono estratte le informazioni, al medico e all'organizzazione responsabili dell'osservazione e all'evento clinico in cui sono state prodotte. |


**Risposta**

{{json:Bundle/bundle-recupero-osservazioni-decorso-ospedaliero}}
