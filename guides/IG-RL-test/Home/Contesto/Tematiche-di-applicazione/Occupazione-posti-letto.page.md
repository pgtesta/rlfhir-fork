# {{page-title}}

Lo scopo del caso d’uso è ottenere dati aggiornati sull’occupazione dei posti letto delle strutture socio-sanitarie di diversa tipologia, ad esempio: RSA, RSD, ecc., presenti in Regione Lombardia.

Il seguente elenco definisce il principale contenuto informativo che sarà disponibile per questo caso d’uso.

| Attributo | Definizione | Risorsa FHIR |
|---|---|---|
|L1|Codice L1 identificativo della struttura|Organization|
|L2|Codice L2 identificativo della struttura (codice CUDES)|Organization|
|Categoria|Identifica la categoria relativa ai posti letto|Observation|
|Numero di letti occupati|Numero di posti letto occupati nella struttura|Observation|
|DataOra Aggiornamento|Data e ora di aggiornamento della misura di occupazione|Observation|

## Diagramma UML

La risorsa FHIR cardine di questo caso d’uso è “Observation” che rappresenta, in generale, una qualsiasi misura o asserzione fatta su un paziente, un dispositivo o qualsiasi altro soggetto. L’Observation è referenziata alla risorsa Organization che esprime il soggetto, ossia la struttura, a cui si applica la misura.

{{render:guides-IG-RL-draft-pics-diagramma-UML-Observation}} 

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
|*performer:Organization.identifier* |permette di ricercare tutte le Observation per una specifica Organization |

Nel caso in esame si ha l’obiettivo di recuperare il numero di posti letto occupati dalle strutture socio-sanitarie, quindi bisognerà effettuare una GET avente Observation come tipo di risorsa, in quanto è la risorsa che contiene l’informazione relativa al numero di posti letto occupati per una particolare struttura.
Nella risposta del server si vuole ottenere anche un riferimento alla struttura sanitaria a cui il dato fa riferimento quindi è possibile utilizzare il parametro di ricerca **_include**. Il valore del parametro include presenta due parti separate dal carattere “:”, il primo valore indica il nome della risorsa di partenza da cui proviene il join (in questo caso Observation), mentre il secondo valore è il nome del parametro di ricerca che deve essere di tipo reference (in questo caso performer indica un riferimento ad una Organization di tipo L2).


## Risposta

Quando il server risponde ad una HTTP Request, elabora la chiamata a seconda del metodo utilizzato e restituisce al client una HTTP Response che contiene un:
* **Body**: corpo della risposta in formato JSON che contiene l’informazione richiesta dal client a seguito della richiesta;
* **Codice di stato HTTP**: restituito dal server in modo da informare il client sul risultato della richiesta (ad esempio 200: indica che la risorsa è stata trovata e il messaggio è stato elaborato con successo);
* **Headers**: forniscono informazioni extra sulla risposta.

### Risposta esito positivo

GET {BASE_URL}/Observation?_include=Observation:performer&Parametro1=ValoreParametro1&…

Il risultato della precedente GET è un Bundle che contiene tutte le Observation insieme alle Organization L2 referenziate mediante il parametro performer contenuto nella risorsa Observation. Tutte le Organization verranno messe in coda alla fine di tutte le Observation.
Il risultato della GET sarà una risorsa di tipo Bundle contenente informazioni relative alle risorse Observation ed Organization.


#### Stuttura del Bundle

|Percorso JSON|Formato|Descrizione|
|-
|*Bundle.resourceType*|string|“Bundle”|
|*Bundle.id*|string|Identificativo univoco del bundle restituito|
|*Bundle.type*|string|“searchset”|
|*Bundle.timestamp*|dateTime|Timestamp in formato FHIR: YYYY-MM-DDThh:mm:ssZ|
|*Bundle.total*|integer|numero di risorse di tipo match restituite|
|*Bundle.link.relation*|string|“self”|
|*Bundle.link.url*|string|URL della chiamata ricevuta|
|*Bundle.entry.fullUrl*|string|URL della risorsa sul sistema sorgente|
|*Bundle.entry[i].resource[i]*|FHIRResource|Elemento JSON della risorsa restituita|
|*Bundle.entry[i].search.mode*|string|Assume valori:<br>   - "match" se la risorsa restituita è quella richiesta<br>   - "include" se la risorsa è restituita perchè referenziata da una risorsa di tipo match|

#### Stuttura di Observation

Nella tabella sottostante si riportano le principali caratteristiche degli attributi della risorsa Observation che aderisce al profilo FHIR “RLObservationNPO”. Maggiori informazioni sul profilo (quali ad esempio cardinalità, formato, ecc…) sono disponibili sul sito di Simplifier.

|Percorso JSON|Formato|Descrizione|
|-
|*Observation.resourceType*|string|“Observation”|
|*Observation.id*|string|Identificativo univoco della observation restituita|
|*Observation.meta.versionId*|string|versione della risorsa|
|*Observation.meta.profile*|string|URL del profilo Observation|
|*Observation.meta.lastUpdated*|string|data ultimo aggiornamento in formato FHIR: YYYY-MM-DDThh:mm:ssZ|
|*Observation.identifier.system*|string|URL del sistema di identificazione utilizzato per l’Observation|
|*Observation.identifier.value*|string|Contiene il valore dell’identificativo in formato: codiceL1-codiceL2|
|*Observation.code.coding.system*|string|URL del sistema di codifica del tipo di Observation|
|*Observation.code.coding.code*|string|codifica del tipo di Observation|
|*Observation.code.coding.display*|string|descrizione del tipo di Observation|
|*Observation.status*|string|“final”|
|*Observation.performer.reference*|string|reference organization L2|
|*Observation.performer.display*|string|descrizione organization L2|
|*Observation.effectiveDateTime*|dateTime|data dell’osservazione in formato FHIR: YYYY-MM-DDThh:mm:ssZ|
|*Observation.component.code.coding.system*|string|URL codifica tipologia posti letto|
|*Observation.component.code.coding.code*|string|Codice identificativo del tipo di posto letto|
|*Observation.component.code.coding.display*|string|descrizione della tipologia dei posti letto|
|*Observation.component.valueInteger*|integer|numero di posti letto occupati|
|*Observation.search.mode*|string|“match”|

In aggiunta, grazie all’utilizzo del parametro di ricerca _include, la risposta conterrà anche le informazioni relative all’Organization referenziata dal parametro performer in Observation. In particolare non tutte le informazioni contenute nella risorsa FHIR **Organization** sono obbligatorie ma è importante che ci siano le informazioni descritte nel paragrafo che segue.

#### Struttura di Organization

Nella tabella sottostante si riportano le principali caratteristiche degli attributi della risorsa Organization che aderisce al profilo FHIR “RLOrganizationL2”. Maggiori informazioni sul profilo (quali ad esempio cardinalità, formato, ecc…) sono disponibili sul sito di Simplifier.

|Percorso JSON|Formato|Descrizione|
|-
|*Organization.resourceType*|string|“Organization”|
|*Organization.id*|string|identificativo univoco della organization restituita|
|*Organization.meta.profile*|string|URL del profilo Observation L2|
|*Organization.identifier.system*|string|URL del sistema di identificazione utilizzato per l’Organization|
|*Organization.identifier.value*|string|codice ministeriale del presidio|
|*Organization.type.coding.system*|string|URL del sistema di codifica della tipologia di struttura|
|*Organization.type.coding.code*|string|codice del tipo di struttura L2|
|*Organization.name*|string|denominazione del presidio|
|*Organization.search.mode*|string|“include”|

Di seguito un esempio di Bundle di risposta con esito positivo:
{{json:bundle_esempio}}

### Risposta esito positivo senza risultati

Nel caso in cui in seguito ad una interrogazione FHIR, l’applicativo risponda con zero risultati, la risposta è comunque di esito positivo in quanto il codice di stato è HTTP 200.

#### Struttura del Bundle

|Percorso JSON|Formato|Descrizione|
|-
|*Bundle.resourceType*|string|“Bundle”|
|*Bundle.id*|string|Identificativo univoco del bundle restituito|
|*Bundle.type*|string|“searchset”|
|*Bundle.timestamp*|dateTime|Timestamp in formato FHIR: YYYY-MM-DDThh:mm:ssZ|
|*Bundle.total*|integer |numero di risorse di tipo match restituite (“0”)|
|*Bundle.link.relation*|string|“self”|
|*Bundle.link.url*|string|URL della chiamata ricevuta|

Di seguito un esempio di Bundle di risposta con esito positivo con zero risultati.

```json
{
    "resourceType": "Bundle",
    "id": "dbb16aa8-02b9-11ed-ac24-02001700b287",
    "type": "searchset",
    "timestamp": "2022-07-13T14:41:19Z",
    "total": 0,
    "link": [
        {
            "relation": "self",
            "url": "http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4/Observation?_include=Observation:performer"
        }
    ]
}
```

### Risposta esito negativo

Nel caso in cui la risposta ottenuta dall’applicativo del IS è negativa e l’errore è a livello di Web Service, essa conterrà i codici di stato propri del protocollo HTTP; ad esempio:
* 404 Not Found, se la risorsa web non è stata trovata;
* 410 Gone, se la risorsa è stata eliminata;
* Ecc.

Nel caso in cui l’applicativo abbia errori sull’interfaccia FHIR (ad. esempio un parametro non è riconosciuto), verrà restituita come risposta un JSON contente la risorsa Bundle al cui interno è presente la risorsa OperationOutcome.

#### Struttura di OperationOutcome

|Percorso JSON|Formato|Descrizione|
|-
|*OperationOutcome.resourceType*|string|“OperationOutcome”|
|*OperationOutcome.id*|string|Identificativo della risorsa|
|*OperationOutcome.Issue.severity*|string|Severità dell’errore|
|*OperationOutcome.Issue.code*|string|Codice dell’errore|
|*OperationOutcome.Issue.diagnostics*|string|Riferimento dell’errore|
|*OperationOutcome.Issue.details.text*|string|Dettagli dell’errore|

Di seguito un esempio di risposta negativa a seguito di un parametro di ricerca non riconosciuto.

```json
{
    "resourceType": "Bundle",
    "id": "f8cd72d2-0460-11ed-aa12-02001700b287",
    "type": "searchset",
    "timestamp": "2022-05-15T17:10:05Z",
    "total": 0,
    "link": [
        {
            "relation": "self",
            "url": "http://localhost:8080/fhirserver/fhir/r4/Observation"
        }
    ],
    "entry": [
        {
            "resource": {
                "resourceType": "OperationOutcome",
                "id": "1",
                "issue": [{
                        "severity": "error",
                        "code": "invalid",
                        "diagnostics": "ParameterNotSupported",
                        "details": {
                            "text": "Unrecognized parameter '_id1'. 123456"
                        }
                    }
                ]
            }
            "search": {
                "mode": "outcome"
            }
        }
    ]
}


```

