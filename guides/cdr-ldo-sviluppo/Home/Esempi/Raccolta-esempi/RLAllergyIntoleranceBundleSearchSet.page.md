# Esempio di ricerca delle allergie attive per un determinato paziente 

Questa ricerca permette di reperire le allergie di un determinato paziente registrate presso una struttura sanitaria.
I parametri obbligatori da valorizzare per effettuare la ricerca sono: 

- _has:Provenance:target:agent:_has:Organization.identifier=[codice azienda]
- clinical-status=active
- _revinclude=Provenance:target
- _include=AllergyIntolerance:patient
- _include=PractitionerRole:practitioner 
- _include=PractitionerRole:organization 

**Richiesta:** 

| SCOPE | Ricerca delle allergie attive di un determinato paziente |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /AllergyIntolerance?clinical-status=active&last-date=2021-06-01&patient.identifier=RSSMRA80A01F205X&_has:Provenance:target:agent:_has:Organization.identifier=030712&_revinclude=Provenance:target&_include=AllergyIntolerance:patient&_include=PractitionerRole:practitioner &_include=PractitionerRole:organization   |
|Descrizione risposta | Restituirà tutte le risorse AllergyIntolerance, filtrate per ultima data di manifestazione, del paziente con codice fiscale RSSMRA80A01F205X, insieme alle informazioni del paziente, <br> al documento da cui sono estratte le informazioni, al medico e all'organizzazione responsabili dell'osservazione e all'evento clinico in cui sono state prodotte. |

**Risposta**

{{json:Bundle/bundle-recupero-allergie-farmaceutiche}}
