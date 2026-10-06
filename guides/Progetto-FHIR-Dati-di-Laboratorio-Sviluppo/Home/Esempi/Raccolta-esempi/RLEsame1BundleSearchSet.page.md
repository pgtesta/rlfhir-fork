# Esempio di ricerca esame specifico di laboratorio per un determinato paziente 

Questa ricerca permette di reperire i dettagli dei risultati di uno o più referti relativi a una specifica tipologia di esame di laboratorio effettuato da un determinato paziente presso una struttura sanitaria, permettendo di selezionare gli esami effettuati a partire da una certa data o all’interno di un certo intervallo temporale. 

I parametri obbligatori da valorizzare per effettuare la ricerca sono: 

- _include=Observation:patient&patient.identifier=[identificativo paziente]
- category = laboratory 
- code = [codice esame]
- date = gt[data inizio ricerca] 


**Richiesta:** 

| SCOPE | Ricerca esame specifico di laboratorio per un determinato paziente |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Observation?code=2339-0&date=gt2024-01-01&category=laboratory&_include=Observation:patient&patient.identifier=RSSMRA71E01F205E   |
|Descrizione risposta | Restituirà tutte le Observation con profilo RLObservationLabReport che hanno il codice LOINC “2339-0” relativo all’esame del glucosio, effettuate dopo la data del 1/01/2024 del paziente con codice fiscale RSSMRA71E01F205E, insieme alle informazioni del paziente (risorsa Patient). |

**Risposta**

{{json:Bundle/esempio-esame-specifico-1}}
