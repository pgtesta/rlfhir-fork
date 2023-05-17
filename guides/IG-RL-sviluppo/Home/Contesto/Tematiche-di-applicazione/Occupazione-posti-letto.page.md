# {{page-title}}

Lo scopo del caso d’uso è ottenere dati aggiornati sull’occupazione dei posti letto delle strutture socio-sanitarie di diversa tipologia, ad esempio: RSA, RSD, ecc., presenti in Regione Lombardia.

Il seguente elenco definisce il principale contenuto informativo che sarà disponibile per questo caso d’uso.

| Attributo | Definizione | Risorsa FHIR |
|---|---|---|
|L1|Codice L1 identificativo della struttura|Organization|
|L2|Codice L2 identificativo della struttura (codice CUDES)|Organization|
|Reparto clinico|Identificativo del reparto clinico che ha in carico il paziente|Location|
|Dettaglio letti|Informazioni relative ai letti occupati nei vari reparti|Location|
|Totale letti occupati|Numero di posti letto occupati nel reparto e/o nella struttura ospedaliera|MeasureReport|

La raccolta dei profili utilizzati per questo caso d'uso sono raggruppati mediante il TAG *PLO*.

## Richiesta

Per interrogare un applicativo tramite interfaccia FHIR si utilizza il metodo GET che permette di recuperare una specifica risorsa, indicando il relativo URI, oppure utilizzare il metodo GET combinando una serie di parametri condizionali. 
Il formato di una ricerca di una risorsa mediante il metodo GET è il seguente:

	GET {BASE_URL}/TipoRisorsa?Parametro1=ValoreParametro1&Parametro2=ValoreParametro2&…


Dove BASE_URL è l’endpoint dell’applicativo che espone il servizio, TipoRisorsa è il nome della risorsa FHIR esposta e le coppie Parametro-ValoreParametro esprimono condizioni di ricerca specifiche. 

Nella tabella sottostante sono riportati alcuni dei parametri di ricerca che possono essere utilizzati per determinare il comportamento della risposta applicativa. Si noti che tali parametri possono essere combinati tra loro con operatori logici (ad esempio & esprime AND logico).

|Parametro|Descrizione parametro|
|---|---|
|*_include* |indica che le risorse oggetto devono essere incluse nei risultati di ricerca |
|*_lastUpdated* |utile per selezionare le risorse in base alla data di ultimo aggiornamento. Possibile specificare se risorse restituite devono avere una data di ultimo aggiornamento superiore/inferiore alla data definita dal parametro |
|*_profile* |utile per selezionare le risorse in base al URL del profilo specificato nell’elemento meta |
|*operationa-status* |permette di ricercare tutte le location con un determinato stato |
|*organization.identifier* |permette di ricercare tutte le location per una specifica Organiation (L2) |
|*repartoClinico* |permette di ricercare tutte le location per un specifico reparto clinico (L3)|

Nel caso in esame si ha l’obiettivo di recuperare il numero di posti letto occupati dalle strutture socio-sanitarie, quindi bisognerà effettuare una GET avente Location come tipo di risorsa, in quanto è la risorsa che contiene l’informazione relativa al posto letto occupato all'interno di una determinata stanza, all'interno di un determinato piano, per una particolare struttura.
Nella risposta del server si vuole ottenere anche un riferimento alla struttura sanitaria a cui il dato fa riferimento quindi è possibile utilizzare il parametro di ricerca **_include**. Il valore del parametro include presenta due parti separate dal carattere “:”, il primo valore indica il nome della risorsa di partenza da cui proviene il join (in questo caso Location), mentre il secondo valore è il nome del parametro di ricerca che deve essere di tipo reference (in questo caso performer indica un riferimento ad una Organization di tipo L2).


## Risposta

Quando il server risponde ad una HTTP Request, elabora la chiamata a seconda del metodo utilizzato e restituisce al client una HTTP Response che contiene un:
* **Body**: corpo della risposta in formato JSON che contiene l’informazione richiesta dal client a seguito della richiesta;
* **Codice di stato HTTP**: restituito dal server in modo da informare il client sul risultato della richiesta (ad esempio 200: indica che la risorsa è stata trovata e il messaggio è stato elaborato con successo);
* **Headers**: forniscono informazioni extra sulla risposta.
