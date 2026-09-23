# IG OMr - Gestione digitale Rete di Laboratori v1.3.0

Versione rilasciata il 22/07/2024. 

Gli aggiornamenti previsti per questo rilascio includono:
- Modifica cardinalità slice *ServiceRequest:identifier:PlacerOrderNumber*
- Modifica *ServiceRequest.occurrenceDateTime* in *occurrencePeriod*
- Vincolo codifica reg_map_plus nel campo *ServiceRequest.code*
- Modifica sistema di identificazione previsto nella slice in *Patient.identifier:codiceFiscale*
- Aggiunta campo *OperationOutcome.expression*
- Modifica valueset Categoria Ordine
- Modifica *Patient.extension:ASLResidenza* in *Patient.extension:ASLAssistenza*
- Aggiunta attributo *ServiceRequest.subject.type*
- Aggiornamento pagina *Panoramica di progetto*
- Notifica giornaliera: aggiunta pagina degli scenari dedicata, profilo bundle del messaggio ed esempio
- Aggiunta profilo *Organization Laboratorio* 
- Modifica profilo target *Encounter.extension:serviceRequester* 
- Modifica profilo target *ServiceRequest.performer* 
- Aggiornamento esempi

La guida è consultabile a questo [link](https://simplifier.net/guide/gdrlab?version=1.3.0).

Questa versione della Implementation Guide fa riferimento agli elementi FHIR contenuti nel pacchetto [gdrl.fhir.r4 1.3.0](https://simplifier.net/packages/gdrl.fhir.r4/1.3.0).
