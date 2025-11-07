# {{page-title}}


L'esito delle chiamate FHIR è definito dal codice di stato HTTP e dal contenuto del messaggio restituito.
In aggiunta ai normali codici di stato HTTP, i seguenti codici sono utilizzati per descrivere stati o errori relativi a FHIR.

## Consultazione
In caso una chiamata di consultazione vada a buon fine, verrà restituito al chiamante uno stato HTTP della categoria 2xx e la risorsa nel corpo.
In caso non possa essere eseguita, la risposta contiene il codice di errore HTTP delle categorie 4xx e 5xx e la risorsa nel corpo.

|Codice Stato|Descrizione|
|---|---|
|200 OK | La risposta è stata correttamente generata |
|400 Bad Request | La richiesta non può essere processata o fallisce le regole di validazione FHIR|
|401 Not Authorized | Per eseguire la ricerca è necessaria l'autorizzazione|
|404 Not Found | La tipologia di risorsa cercata non esiste o è indirizzata a un endpoint non FHIR|
|422 Unprocessable Entity | La risorsa da creare non soddisfa i profili o regole criteri FHIR definiti|
|500 Internal Server Error | Messaggio di errore generico|
