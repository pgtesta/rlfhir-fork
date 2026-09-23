# {{page-title}}

## Clinical Data Repository
Regione Lombardia (RL), al fine di favorire la progettazione di un’architettura integrata con un ecosistema FSE 2.0 orientato ai dati, intende valorizzare il patrimonio informativo sanitario disponibile attraverso la progressiva introduzione, nei contesti aziendali, di Clinical Data Repository (CDR) quali punti di acquisizione e consolidamento dei dati prodotti dai sistemi dipartimentali. 

Il CDR è un sistema centralizzato partizionato per Ente Sanitario in grado di abilitare una più efficace ed efficiente valorizzazione del patrimonio informativo disponibile per analisi su tematiche specifiche legate ad esigenze di operatività clinica o di governance sanitaria.

Questo scenario di trasformazione di servizi e tecnologie a disposizione dei professionisti (clinici e amministrativi) garantirà un utilizzo efficiente delle risorse disponibili utilizzando i canali d’integrazione tra il livello centrale e quello periferico in funzione della frequenza e del livello di granularità dei dati con cui questi necessitano di essere analizzati.

Al fine di consentire un’adeguata ideazione, prototipazione e avvio di servizi innovativi abilitati dal Clinical Data Repository è necessario definire le esigenze informative di business a cui i servizi innovativi del CDR devono rispondere e identificare casi d’uso funzionali abilitati dall’adozione del CDR, anche attraverso la valorizzazione di eventuali esperienze già maturate in contesti sanitari. Coerentemente con le esigenze di Regione Lombardia, nell’individuazione dei casi d’uso prioritari viene effettuata una distinzione - a seconda del destinatario del servizio - in casi d’uso clinici (migliore gestione delle cure e migliore assistenza sanitaria ai pazienti in cura) e di governo (monitoraggio di dati aggregati ai fini di governo e programmazione). 

Inoltre, a seconda del perimetro di visibilità dei dati, viene definito un perimetro di riferimento aziendale (consultazione di dati prodotti all’interno dello stesso Ente Sanitario) o sovra-aziendale (consultazione di dati prodotti da tutti i diversi Enti Sanitari).

## Visualizzazione dell’andamento dei risultati di laboratorio
Il caso d’uso “Visualizzazione dell’andamento dei risultati di laboratorio” è volto alla possibilità di ricercare, consultare e visionare l’andamento nel tempo dei risultati dei referti di laboratorio tramite una dashboard configurabile ed interattiva. Il caso d’uso si basa su un sistema in grado di raccogliere dati in modalità near real time ed esporre interfacce per la rappresentazione e visualizzazione delle informazioni di interesse sulla dashboard. Il caso d’uso fa riferimento al perimetro aziendale di visibilità dei dati.

### Utenti fruitori
Gli utenti identificati come fruitori del caso d’uso sono i Medici Ospedalieri che vogliano sfruttare, a supporto della pratica clinica, le potenzialità messe a disposizione dai dati atomici FHIR accessibili dal CDR. 

### Fonti dato 
I Referti di Laboratorio CDA2, prodotti dai LIS, costituiscono le fonti dato da cui sarà possibile estrarre i dati puntuali FHIR che alimenteranno il CDR.

### Contenuto informativo 
Il contenuto informativo d’interesse per le finalità del caso d’uso “Visualizzazione dell’andamento dei risultati di laboratorio” comprende una serie di dati clinici raccolti e gestiti per supportare la pratica clinica e migliorare la qualità delle cure.