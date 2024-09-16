# Esempio di recupero Observation di laboratorio di un paziente

Questa ricerca permette di reperire i dettagli dei risultati di uno o più referti relativi agli esami di laboratorio effettuati da un determinato paziente presso una struttura sanitaria.

I parametri da valorizzare per effettuare la ricerca sono:
-	category = laboratory
- _include=Observation:patient&patient.identifier=[identificativo paziente]
- _include=Observation:specimen
- _include:iterate=Observation:performer
- _include=Observation:encounter

**Richiesta:** 

| SCOPE |  Ricerca Observation di laboratorio di un paziente|
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Observation?category=laboratory&_include:iterate=Observation:patient&patient.identifier=RSSMRA70A01A399Z&_include=Observation:specimen&_include:iterate=Observation:performer&_include=Observation:encounter  |
|Descrizione risposta | Restituirà tutte le Observation di laboraotorio associate al paziente RSSMRA70A01A399Z, includendo le informazioni relative al paziente, ai campioni associate alle osservazioni, al medico responsabile dell'osservazione e all'evento clinico in cui sono state prodotte. |

**Risposta**

{{json:Bundle/esempio-con-encounter}}
