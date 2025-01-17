# Esempio di ricerca esame specifico di laboratorio per un determinato paziente 

Questa ricerca permette di recuperare un documento tramite il suo identificativo univoco. 

I parametri obbligatori da valorizzare per effettuare la ricerca sono: 

- identifier= identificativo univoco del documento espresso come *value|system*
- composition.custodian

**Richiesta:** 

| SCOPE | Ricerca esame specifico di laboratorio per un determinato paziente |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Bundle?identifier=2.16.840.1.113883.2.7.5.100000\|urn:oid:2.16.840.1.113883.2.9.2.30&composition.custodian=030456  |
|Descrizione risposta | Restituirà un documento FHIR associato all'identificativo indicato nella richiesta nel campo identifier. |

**Risposta**

{{json:Bundle/esempio-richiesta-1}}
