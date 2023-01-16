# {{page-title}}

Endpoints FHIR

Le API RESTful FHIR sono esposte ai seguenti endpoint sul dominio <em>https://api.servizirl.it</em>:

        GET https://api.servizirl.it/c/operatori.siss/[ambitoTBD]/v1.0.0/[servizioTBD]/CarePlan

        GET https://api.servizirl.it/c/operatori.siss/[ambitoTBD]/v1.0.0/[servizioTBD]/ServiceRequest

È necessario passare un header dello scope per permettere a APIManager di gestire l'_AccessToken_.

Nell'header sarà inoltre specificato che le informazioni saranno scambiate in formato json tramite il parametro di chiamata <code>content_type=json</code>.