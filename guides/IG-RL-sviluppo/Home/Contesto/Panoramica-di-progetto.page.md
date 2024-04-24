# {{page-title}}

Con lo scopo di introdurre un processo di standardizzazione ed interoperabilità dei dati, così come già previsto nella maggior parte dei progetti a livello nazionale e regionale nell’ambito della sanità digitale, Regione Lombardia ha previsto l’adozione  dello standard HL7-FHIR® come best practice di scambio, gestione e consultazione dei dati funzionali alla presa in carico assistenziale del cittadino ed alla gestione della sanità territoriale e di prossimità. Il Sistema di Gestione Digitale del Territorio (SGDT) è la piattaforma che gestisce i processi relativi a tali servizi assistenziali. 
Il progetto FHIR per Regione Lombardia è descritto tramite diverse Guide Implementative, ognuna della quali si occupa di illustrare uno o più scenari di integrazione relativi ad uno stesso ambito di applicazione. La presente Guida Implementativa contiene i profili FHIR, le codifiche e le specifiche dei vari scenari di cooperazione applicativa definite per la integrazioni gestite dal SGDT.
Ad oggi la piattaforma SGDT supporta le seguenti integrazioni:
- Cooperazione applicativa con i verticali degli Enti Erogatori Privati Accreditati (EEPA) per la gestione degli assistiti nell’ambito del servizio delle Cure Domiciliari. I principali profili FHIR utilizzati sono: RLCarePlanProgettoIndividuale, RLServiceRequestServiziSocioAssistenziali e RLProcedurePrestazione;
- l’acquisizione delle informazioni relative al catalogo dell’offerta dei servizi assistenziali attivabili in Regione Lombardia attraverso la consultazione del patrimonio informativo contenuto nei  Dati Codificati (DDC). Il principale profilo utilizzato è RLOrganizationL2;
- la Nuova Anagrafe Regionale (NAR) per l’acquisizione dei dati anagrafici degli assistiti. Il principale profilo FHIR utilizzato è RLPatientCittadino.
Il protocollo di interoperabilità HL7-FHIR® utilizzato per ogni integrazione è definito nella sezione API RESTful della Guida Implementativa. Attualmente tutte gli scenari di cooperazione applicativa prevedono uno scambio dati in logica PULL attraverso la definizione di parametri di ricerca. 


## Glossario
Raccolta di acronimi e termini usati nel progetto:
 
| Voce | Descrizione |
|---|---|
| DDC | Distribuzione Dati Codificati |
| DP | Dimissione Protette |
| PI | Progetto Individuale (Piano Assistenziale Individuale) |
| RSA | Residenza Sanitaria Assistenziale |
| PLO | Numero Posti Occupati |
| L1 | Codice   identificativo di livello 1 degli enti aderenti al progetto SISS. La risorsa   FHIR che descrive questa tipologia di struttura è _RLOrganizationL1_ |
| L2 | Codice identificativo di livello 2 degli Enti Erogatori di servizi socioassistenziali. La risorsa FHIR che descrive questa tipologia di struttura è _RLOrganizationL2_. |