# Ricerca risultati di laboratorio di un paziente in un periodo di 5 mesi 

Questa ricerca permette di reperire la lista delle osservazioni fatte su un paziente, nelle strutture afferenti all’ente che sta facendo la richiesta, utilizzando un periodo di osservazione di 5 mesi da oggi. Si vuole includere nella risposta anche il dettaglio del paziente (Patient), del documento da cui provengono le osservazioni (Provenance), dell’azienda (Organization) e del firmatario (PractitionerRole, Practitioner, Organization), nonché dell’evento di incontro che ha prodotto il referto di medicina di laboratorio (Encounter). 

- category = laboratory
- date = gt[data inizio ricerca] 
- _include:iterate=Observation:patient&patient.identifier=[identificativo paziente]
- _include:iterate=Observation:patient
- _revinclude:iterate=Provenance:target

**Richiesta:** 

| SCOPE | Ricerca risultati di laboratorio di un paziente in un periodo di 5 mesi |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | / Observation?date=gt01-04-2024&date=lt01-09-2024&category=laboratory&_include:iterate=Observation:patient&patient.identifier=AAABBB12D55I999D&_revinclude:iterate=Provenance:target   |
|Descrizione risposta | Restituirà tutte le osservazioni di laboratorio associate al paziente AAABBB12D55I999D in un periodo di tempo compreso tra il 1° Aprile 2024 e il 1° Settembre 2024, per un totale di 5 mesi. Nella risposta sono incluse le informazioni del paziente, le informazioni sul documento da cui sono state ricavate le osservazioni, e i professionisti sanitari e le aziende responsabili. |

**Risposta**

{{json:Bundle/esempio-nel-tempo}}
