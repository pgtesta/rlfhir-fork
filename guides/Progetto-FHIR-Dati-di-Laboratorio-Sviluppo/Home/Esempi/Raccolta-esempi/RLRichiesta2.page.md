# Esempio di ricerca esame specifico di laboratorio per un determinato paziente 

Questa ricerca permette di recuperare una serie di documenti di laboratorio sulla base del paziente a cui è associato e la data in cui è stato prodotto.

I parametri obbligatori da valorizzare per effettuare la ricerca sono: 

- composition.subject
- composition.date 
- composition.code = 11506-2


**Richiesta:** 

| SCOPE | Ricerca esame specifico di laboratorio per un determinato paziente |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Bundle?composition.subject=AAABBB12D55I999D&composition.date=gt2023-01-01&composition.date=lt2024-06-14&composition.code=11502-2  |
|Descrizione risposta | Restituirà i documenti FHIR di laboratorio associato al paziente AAABBB12D55I999D successivi al 14 giugno 2024. |

**Risposta**

{{json:Bundle/esempio-richiesta-2}}
