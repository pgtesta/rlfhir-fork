# Stati ed Errori HTTP

L'esito delle chiamate FHIR è definito dal codice di stato HTTP e dal contenuto del messaggio restituito.
In aggiunta ai normali codici di stato HTTP, i seguenti codici sono utilizzati per descrivere stati o errori relativi a FHIR.

Nella pagina {{pagelink:Home/Esempi/Libreria-Esempi.page.md, Libreria Esempi}}, sono inoltre presenti alcuni esempi di errore.

## Ricerche

In caso una ricerca venga eseguita correttamente, verrà restituito uno stato HTTP della categoria 2xx e il corpo della risposta conterrà una risorsa FHIR di tipo Bundle.
In caso non possa essere eseguita, la risposta contiene il codice di errore HTTP delle categorie 4xx e 5xx e la risorsa nel corpo.

|Codice Stato|Descrizione|
|---|---|
|200 OK | La ricerca è andata a buon fine restituendo zero o più risultati contenuti nella risorsa Bundle di tipologia searchset|
|400 Bad Request | La richiesta non può essere processata o fallisce le regole di validazione FHIR|
|401 Not Authorized | Per eseguire la richiesta è necessaria l'autorizzazione|
|404 Not Found | La tipologia di risorsa richiesta non esiste o è indirizzata a un endpoint non FHIR|
|500 Internal Server Error | Messaggio di errore generico|

## Creazioni
In caso una chiamata di creazione (ad esempio POST) vada a buon fine, verrà restituito al chiamante uno stato HTTP della categoria 2xx.
In caso tale chiamata vada in errore, la risposta contiene il codice di errore HTTP delle categorie 4xx e 5xx e la risorsa OperationOutcome nel corpo.

|Codice Stato|Descrizione|
|---|---|
|201 Created | La richiesta è stata correttamente ricevuta o creata|
|400 Bad Request | La richiesta non può essere processata o fallisce le regole di validazione FHIR|
|401 Not Authorized | Per eseguire la ricerca è necessaria l'autorizzazione|
|404 Not Found | La tipologia di risorsa cercata non esiste o è indirizzata a un endpoint non FHIR|
|422 Unprocessable Entity | La risorsa da creare non soddisfa i profili o regole criteri FHIR definiti|
|500 Internal Server Error | Messaggio di errore generico|

