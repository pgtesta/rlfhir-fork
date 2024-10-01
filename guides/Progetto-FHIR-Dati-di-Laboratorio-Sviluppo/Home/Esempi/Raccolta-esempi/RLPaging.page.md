# Paging - Esempio di ricerca esame specifico di laboratorio per un determinato paziente 

- [Richiesta 1]{Richiesta-n.1}

- [Richiesta 2]{Richiesta-n.2}

Premessa dell'esempio: nel CDR sono presenti 2 docuementi di laboratorio associati al paziente. Il client vuole recuperarli uno alla volta.
Questa ricerca permette di recuperare un documento di laboratorio alla volta sulla base del paziente a cui è associato e la data in cui è stato prodotto.

I parametri obbligatori da valorizzare per effettuare la ricerca sono: 

- composition.subject
- composition.date 
- composition.code = 11506-2
- _page
- _count

Inizialmente, il client non conosce necessariamente il totale delle risorse che corrispondono ai suoi criteri di ricerca, perciò deve richiedere la prima pagina, dalla quale potrà ricavare le informazioni sul:
- totale delle risorse corrispondenti (Bundle.total);
- url della pagina richiesta (attributo *url* dove Bundle.link.relation = "self");
- url da utilizzare per la GET della pagina successiva (attributo *url* dove Bundle.link.relation = "next"), se presente;
- url da utilizzare per la GET dell'ultima pagina (attributo *url* dove Bundle.link.relation = "previous"), se presente;  
- url da utilizzare per la GET della prima pagina (attributo *url* dove Bundle.link.relation = "first"), presente solo se diversa dalla pagina attuale;
- url da utilizzare per la GET dell'ultima pagina (attributo *url* dove Bundle.link.relation = "last"), presente solo se diversa dalla pagina attuale.

## Richiesta n.1

| SCOPE | Ricerca esame specifico di laboratorio per un determinato paziente |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Bundle?composition.subject=AAABBB12D55I999D&composition.date=gt2023-01-01&composition.code=11502-2&_page=1&_count=1  |
|Descrizione risposta | Restituirà un solo (_count=1) documento FHIR di laboratorio associato al paziente AAABBB12D55I999D successivo al 01 gennaio 2023 e l'indicazione per ricavare i successivi. |

**Risposta**

{{json:Bundle/esempio-paging-richiesta-1}}


## Richiesta 2

| SCOPE | Ricerca esame specifico di laboratorio per un determinato paziente |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Bundle?composition.subject=AAABBB12D55I999D&composition.date=gt2023-01-01&composition.code=11502-2&_page=2&_count=1  |
|Descrizione risposta | Restituirà un solo documento (_count=1) FHIR di laboratorio associato al paziente AAABBB12D55I999D successivo al 01 gennaio 2023 e l'indicazione per ricavare i precedente. |

**Risposta**

{{json:Bundle/esempio-paging-richiesta-2}}
