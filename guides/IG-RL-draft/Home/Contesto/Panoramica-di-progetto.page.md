# {{page-title}}

Con lo scopo di introdurre un processo di standardizzazione ed interoperabilità dei dati, così come già previsto nella maggior parte dei progetti a livello nazionale e regionale nell’ambito della sanità digitale, Regione Lombardia ha previsto l’adozione  dello standard HL7-FHIR® come best practice di scambio, gestione e consultazione dei dati funzionali alla presa in carico assistenziale del cittadino ed alla gestione della sanità territoriale e di prossimità. Il Sistema di Gestione Digitale del Territorio (SGDT) è la piattaforma che gestisce i processi relativi a tali servizi assistenziali. 
Il progetto FHIR per Regione Lombardia è descritto tramite diverse Guide Implementative, ognuna della quali si occupa di illustrare uno o più scenari di integrazione relativi ad uno stesso ambito di applicazione. La presente Guida Implementativa contiene i profili FHIR, le codifiche e le specifiche dei vari scenari di cooperazione applicativa definite per le integrazioni gestite dal SGDT.
Ad oggi la piattaforma SGDT supporta le seguenti integrazioni:
•	Cooperazione applicativa con i verticali degli Enti Erogatori Privati Accreditati (EEPA) per la gestione degli assistiti nell’ambito del servizio delle Cure Domiciliari. I principali profili FHIR utilizzati sono: RLCarePlanProgettoIndividuale, RLServiceRequestServiziSocioAssistenziali e RLProcedurePrestazione;
•	Cooperazione applicativa con le Cartelle Elettroniche in uso dai Medici di Medicina Generale (CE-MMG) per la gestione dei pazienti cronici. I principali profili FHIR utilizzati sono: RLMessageHeaderMMG, RLPatientBase, RLConditionProblemiSalute e RLOperationOutcomeMMG;
•	l’acquisizione delle informazioni relative al catalogo dell’offerta dei servizi assistenziali attivabili in Regione Lombardia attraverso la consultazione del patrimonio informativo contenuto nei  Dati Codificati (DDC). Il principale profilo utilizzato è RLOrganizationL2.
Il protocollo di interoperabilità HL7-FHIR® utilizzato per ogni integrazione è definito nella sezione API RESTful della Guida Implementativa. Attualmente lo scenario di cooperazione applicativa con gli EEPA nell’ambito delle Cure Domiciliari prevede uno scambio dati in logica PULL attraverso la definizione di parametri di ricerca, mentre lo scenario di cooperazione applicativa con le CE-MMG per i pazienti cronici prevede uno scambio di dati tramite messaggistica FHIR.


## Glossario
Raccolta di acronimi e termini usati nel progetto:

| Voce | Descrizione |
|---|---|
|ADP  |Assistenza Domiciliare Programmata |
|API  |Application Programming Interface  |
|ASST |Azienda Socio-Sanitaria Territoriale    |
|C-DOM|Cure Domiciliari    |
|CE-MMG    |Cartella Elettronica del Medico di Medicina Generale   |
|DDC  |Distribuzione Dati Codificati |
|EEPA |Ente Erogatore Privato Accreditato |
|EVM  |Equipe di Valutazione   Multidimensionale    |
|FHIR |Fast Healthcare Interoperability Resource    |
|IG   |Implementation   Guide   |
|L1   |Codice   identificativo di livello 1 degli enti aderenti al progetto SISS. La risorsa   FHIR che descrive questa tipologia di struttura è RLOrganizationL1 |
|L2   |Codice   identificativo di livello 2 degli Enti Erogatori di servizi   socioassistenziali. La risorsa FHIR che descrive questa tipologia di   struttura è RLOrganizationL2.    |
|MMG  |Medico di   Medicina Generale |
|NAR  |Nuova   Anagrafe Regionale    |
|NPRI |Nuova   Piattaforma Regionale di Integrazione|
|PAI  |Piano   Assistenziale Individuale  |
|PI   |Progetto Individuale|
|PIPP |Prestazioni di Particolare Impegno   Professionale|
|SGDT |Sistema di   Gestione Digitale del Territorio|
|SISS |Sistema   Informativo Socio-Sanitario   |
|REST |Representational   State Transfer  |
|UdO  |Unità d’Offerta. Strutture   presenti nella rete territoriale che rendono disponibili servizi   sociosanitari e assistenziali.    |