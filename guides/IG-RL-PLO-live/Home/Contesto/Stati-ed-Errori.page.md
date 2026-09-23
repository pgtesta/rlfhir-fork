# Stati ed Errori

L'esito delle chiamate FHIR è definito dal codice di stato HTTP e dal contenuto del messaggio restituito.
In aggiunta ai normali codici di stato HTTP, i seguenti codici sono utilizzati per descrivere stati o errori relativi a FHIR.

Nella pagina {{pagelink:Home/Esempi/Libreria-Esempi.page.md, Libreria Esempi}}, sono inoltre presenti alcuni esempi di errore.

## Ricerche
In caso una ricerca venga eseguita correttamente, verrà restituito uno stato HTTP della categoria 2xx e il corpo della risposta conterrà una risorsa FHIR di tipo Bundle.
In caso tale chiamata vada in errore, la risposta conterrà il codice di errore HTTP delle categorie 4xx e 5xx e la risorsa OperationOutcome nel corpo. Il profilo OperationOutcome è consultabile al seguente link: {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOperationOutcome.page.md}}.

Per consultare l'associazione completa tra i codici http e i codici di errore utilizzati nell'Operation Outcome di risposta si può fare riferimento al seguente codesystem: {{link:CodeSystem-OperationOutcome-CodiciErrore}}.

|Codice Stato|Descrizione|
|---|---|
|200 OK | La ricerca è andata a buon fine restituendo zero o più risultati contenuti nella risorsa Bundle di tipologia searchset.|
|400 Unauthorized | La richiesta non può essere soddisfatta a causa di errori di sintassi.|
|401 Not Authorized | L'autenticazione è possibile ma è fallita o non può essere fornita.|
|403 Forbidden | La richiesta contiene dati validi ed è stata compresa dal server, ma il server rifiuta l'azione. Ciò può essere dovuto al fatto che l'utente non dispone delle autorizzazioni necessarie per una risorsa o tenta un'azione proibita.|
|404 Not Found | La tipologia di risorsa richiesta non esiste o è indirizzata a un endpoint non FHIR.|
|405 Method Not Allowed| La richiesta è stata eseguita usando un metodo non permesso.|
|406 Not Acceptable| La tipologia di contenuto specificata non é accettabile per gli standard FHIR.|
|422 Unprocessable Entity| Il server comprende il tipo di contenuto dell'entità richiesta e la sintassi della richiesta è corretta, ma non è in grado di processare le istruzioni contenute nella richiesta.|
|429 Too many requests| La richiesta è stata rifiutata perché si é raggiunto il massimo numero di connessioni possibili. Si prega di riprovare più tardi.|
|500 Internal Server Error | Messaggio di errore generico.|
|503 Service Unavailable| Il server non è al momento disponibile. Generalmente è una condizione temporanea. |

## Creazioni
In caso una chiamata di creazione (ad esempio POST) vada a buon fine, verrà restituito al chiamante uno stato HTTP della categoria 2xx.
In caso non possa essere eseguita, la risposta contiene il codice di errore HTTP delle categorie 4xx e 5xx e la risorsa nel corpo.

|Codice Stato|Descrizione|
|---|---|
|201 Created | La richiesta è stata correttamente ricevuta o creata|
|400 Bad Request | La richiesta non può essere processata o fallisce le regole di validazione FHIR|
|401 Not Authorized | Per eseguire la ricerca è necessaria l'autorizzazione|
|404 Not Found | La tipologia di risorsa cercata non esiste o è indirizzata a un endpoint non FHIR|
|422 Unprocessable Entity | La risorsa da creare non soddisfa i profili o regole criteri FHIR definiti|
|500 Internal Server Error | Messaggio di errore generico|

