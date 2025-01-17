# {{page-title}}

Lo scopo del caso d’uso è ottenere i dati relativi all’occupazione dei posti letto dei pazienti assistiti dalle strutture sociosanitarie in Regione Lombardia, in un’ottica di standardizzazione per la gestione, lo scambio e la consultazione dei dati.

In questo paragrafo sono introdotti i principali requisiti funzionali dell'interfaccia FHIR definita per recuperare i dati relativi ai posti letto occupati. In particolare, le principali informazioni raccolte sono relative a: 
* struttura di ricovero, 
* reparto fisico e clinico,
* area di degenza, 
* stanza, piano e edificio, 
* posto letto, 
* regime di ricovero,
* data di dimissione prevista,
* dimissione protetta.

Per il caso d'uso è stata definita una raccolta di profili FHIR che sono consultabili nella pagina *Profili ed Estensioni - Libreria Profili* utilizzando come TAG di ricerca *PLO*.

Gli applicativi degli enti ospedalieri esporranno i dati in modalità API FHIR RESTful e la sintassi della chiamata e della risposta sarà di tipo JSON. 

Deve essere esposta l'API relativa al dettaglio delle informazioni sulla locazione e sulle caratteristiche di ricovero del posto letto occupato. 
La risorsa FHIR da esporre è Location e segue le specifiche definite dal profilo *RLLocationPLOLetto*, consultabile nella pagina *Profili ed Estensioni - Libreria Profili*.


Per ulteriori dettagli tecnici riguardo l'endpoint e le API da esporre si rimanda alla pagina *Contesto - API RESTful*. 