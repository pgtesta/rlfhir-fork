# Esempio di ricerca delle allergie per un determinato paziente 

Parametri obbligatori:
- *patient.identifier=[identificativo paziente]*: da valorizzare con l'identificativo del paziente soggetto del documento, ad esempio il codice fiscale;

Parametri opzionali:
- *category=[tipo di allergia]*: è possibile filtrare sulla base della categoria di allergia da specificare indicando uno dei codici presenti nel valueset {{link:http://hl7.org/fhir/ValueSet/allergy-intolerance-category}}.
- *last-date=[data di ultima osservazione]*: corrispondente all'attributo *AllergyIntolerance.lastOccurrence* e permette di filtrare per data di ultima manifestazione allergica. 
- *clinical-status=[stato allergia]*: indica lo stato dell'allergia e può assumere valore *active*, *inactive* o *resolved* secondo il valueset {{link:http://hl7.org/fhir/ValueSet/allergyintolerance-clinical}}.


Inoltre, è possibile aggiungere opzionalmente ulteriori risorse alla richiesta utilizzando lo strumento FHIR search 'include' e 'revinclude'. Sono riportati i dettagli dei parametri che possono essere aggiunti alla richiesta:
- *_revinclude=Provenance:target* : include nella risposta la risorsa Provenance che contiene le informazioni sul documento da cui è stata estratta l'informazione.
- *_include=Provenance:agent* : include nella risposta la risorsa PractitionerRole e Organization che sono referenziati all'interno di Provenance dall'attributo *agent*. 
- *_include=PractitionerRole:practitioner &_include=PractitionerRole:organization*: include nella risposta le informazioni sul Medico (Practitioner) e Azienda (Organization) referenziati dai PractitionerRole inclusi nella richiesta.
- *_include=AllergyIntolerance:encounter*: questo permette di includere la risorsa Encounter che contiene le informazioni sul ricovero.

**Richiesta:** 

| SCOPE | Ricerca delle allergie di un determinato paziente |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /AllergyIntolerance?clinical-status=active&category=medication&last-date=2021-06-01&patient.identifier=RSSMRA80A01F205X&_has:Provenance:target:agent:_has:Organization.identifier=030712&_revinclude=Provenance:target&_include=AllergyIntolerance:patient&_include=PractitionerRole:practitioner &_include=PractitionerRole:organization   |
|Descrizione risposta | Restituirà tutte le risorse AllergyIntolerance, filtrate per ultima data di manifestazione, del paziente con codice fiscale RSSMRA80A01F205X, insieme alle informazioni del paziente, <br> al documento da cui sono estratte le informazioni, al medico e all'organizzazione responsabili dell'osservazione e all'evento clinico in cui sono state prodotte. |

**Risposta**

{{json:Bundle/bundle-recupero-allergie-farmaceutiche}}
