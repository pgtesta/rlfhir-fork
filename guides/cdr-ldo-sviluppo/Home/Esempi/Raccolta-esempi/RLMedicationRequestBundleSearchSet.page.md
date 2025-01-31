# Ricerca risultati di laboratorio di un paziente in un periodo di 5 mesi 

Recupero delle prescrizioni farmaceutiche assegnate al paziente alla dimissione di un evento di ricovero.

Parametri obbligatori:
- *patient.identifier=[identificativo paziente]*: da valorizzare con l'identificativo del paziente soggetto delle prescrizioni, ad esempio il codice fiscale.

Parametri opzionali:
- *medication.code=[codice farmaco]*: da valorizzare con il codice del farmaco, utilizzando la codifica AIC, ATC o GE.
- *authoredOn=gt[data ricerca]*: da valorizzare con la data in cui è stata prescritta la terapia (nel formato YYYY-MM-DD) da cui cominciare la ricerca 
- *authoredOn=lt[data di ricerca]*: da valorizzare con la data in cui è stata prescritta la terapia (nel formato YYYY-MM-DD) finale più recente in cui fare la ricerca
- *_has:Provenance:target:agent:_has:Organization.identifier=[codice azienda]: identificativo aziendale (custodian del documento).

Inoltre, è possibile aggiungere opzionalmente ulteriori risorse alla richiesta utilizzando lo strumento FHIR search 'include' e 'revinclude'. Sono riportati i dettagli dei parametri che possono essere aggiunti alla richiesta:
- *_include=MedicationRequest:patient*: include nella risposta la risorsa Patient
- *_revinclude=Provenance:target* : include nella risposta la risorsa Provenance che contiene le informazioni sul documento da cui è stata estratta l'informaizone.
- *_include=Provenance:agent* : include nella risposta la risorsa PractitionerRole e Organization che sono referenziati all'interno di Provenance dall'attributo *agent*. 
- *_include=MedicationRequest:requester*: include nella risposta la risorsa PractitionerRole del medico che ha prescritto la terapia.
- *_include=PractitionerRole:practitioner &_include=PractitionerRole:organization*: include nella risposta le informazioni sul Medico (Practitioner) e Azienda (Organization) referenziati dai PractitionerRole inclusi nella richiesta.
- *_include=MedicationRequest:encounter*: questo permette di includere la risorsa Encounter che contiene le informazioni sull'identificativo dell'episodio, se presente, in cui è stato prodotto il referto e il regime di assistenza del paziente al momento dell'esame.

**Richiesta:** 

| SCOPE | Ricerca risultati di laboratorio di un paziente in un periodo di 5 mesi |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | / MedicationRequest?medication.code=J01CE01&patient.identifier=RSSMRA80A01F205X&authoredOn=gt2024-01-01&authoredOn=lt2025-01-01&_include=MedicationRequest:medication&_has:Provenance:target:agent:_has:Organization.identifier=030712&_revinclude=Provenance:target&_include=Provenance:agent&_include=MedicationRequest:encounter&_include=MedicationRequest:requester&_include=PractitionerRole:practitioner&_include=PractitionerRole:organization   |
|Descrizione risposta | Restituirà tutte le prescrizioni farmaceutiche associate al paziente AAABBB12D55I999D in un determinato periodo di tempo. Nella risposta sono incluse le informazioni del paziente, le informazioni sul documento da cui sono state ricavate le osservazioni, e i professionisti sanitari e le aziende responsabili. |

**Risposta**

{{json:Bundle/bundle-recupero-prescrizioni-farmaceutiche}}
