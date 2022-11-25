## {{page-title}}

### Enti L1 attualmente attivi
Organization L1 con data fine validità superiore alla data odierna o nulla

| SCOPE | Ricerca tutte le Organization con profilo L2 la cui   data di fine validità è maggiore di una data di riferimento e che sono parte   di un determinato codice L1    |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4    |
| URL | /Organization?_profile=https%3A//example.org/fhir/StructureDefinition/RLOrganizationL2&     dataFineValidita={datadiRiferimento}&partof:Organization.identifier={codicelivelloL1}    |

<br>