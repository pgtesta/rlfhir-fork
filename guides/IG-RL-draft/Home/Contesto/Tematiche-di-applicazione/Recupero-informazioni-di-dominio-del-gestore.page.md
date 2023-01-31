# {{page-title}}

Nel caso in esame si ha l’obiettivo di recuperare le informazioni di dominio del gestore dalla risorsa FHIR RLHealthcareServiceRSAInfoBase. Per far ciò bisognerà effettuare una GET avente come tipo di risorsa HealthcareService in quanto è la risorsa che descrive i servizi offerti e le informazioni caratteristiche di una specifica RSA.

Nella risposta del server si vuole ottenere tutte le informazioni contenute nella risorsa HealthcareService relative ad una specifica RSA, quindi è possibile utilizzare il parametro di ricerca organization che permette di specificare l’Organization che fornisce il servizio sanitario di cui si vogliono ottenere le informazioni.

Il valore di questo parametro sarà il codice CUDES ovvero il codice dell’Organization L2 di riferimento. Questo codice sarà univoco per ogni RSA in quanto un codice Organization L2 identifica una specifica struttura sanitaria e quindi di conseguenza identifica univocamente una RSA. 

GET {BASE_URL}/HealthcareService?organization=codiceCUDES

È previsto che il server FHIR effettui una richiesta periodica per ottenere queste informazioni. La frequenza di configurazione della richiesta può essere schedulata settimanalmente o mensilmente in quanto le informazioni richieste non sono soggette a cambi frequenti.
