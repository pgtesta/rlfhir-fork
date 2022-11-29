## {{page-title}}

Di seguito la descrizione dei criteri di ricerca inerenti al profilo RLOrganizationL2.

###	Organization L2 appartenenti ad un Organization L1 con data fine validità superiore ad una certa data
Criterio di ricerca che permette di recuperare le informazioni relative alle strutture di tipo L2, descritto nel profilo RLOrganizationL2, con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata struttura L1 (profilo RLOrganizationL1).

| SCOPE | Ricerca tutte le Organization con profilo L2 la cui data di fine validità è maggiore di una data di riferimento e che sono parte   di un determinato codice L1 |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=\{datadiRiferimento\}&partof:Organization.identifier=\{codicelivelloL1\} |

A titolo esemplificativo, la chiamata: 

    Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&partof:Organization.identifier=030720

restituirà tutte le strutture afferenti alla ASST Bergamo Est (030720) con una data di fine validità superiore al 05/04/2018.

### Organization L2 appartenenti ad una ASST Territoriale con data fine validità superiore ad una certa data
Criterio di ricerca che permette di recuperare le informazioni relative alle strutture di tipo L2, descritto nel profilo RLOrganizationL2, con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata ASST Territoriale (profilo RLOrganizationL1).

| SCOPE | Ricerca tutte le Organization con profilo L2 la cui data di fine validità è maggiore di una data di riferimento e che sono parte di un determinato codice L1 afferente ad una ASST Territoriale |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | / Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=\{datadiRiferimento\}&… |

A titolo esemplificativo, la chiamata:

    Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2&dataFineValidita=gt2018-04-05&=030720

restituirà tutte le strutture afferenti alla ASST Bergamo Est (030720) con una data di fine validità superiore al 05/04/2018.

###	Organization L2 appartenenti ad una ASST Territoriale con data fine validità superiore ad una certa data e di una specifica tipologia
Criterio di ricerca che permette di recuperare le informazioni relative alle strutture di tipo L2, descritto nel profilo RLOrganizationL2, di una determinata tipologia di unità d’offerta (UdO) sociosanitaria, con data di fine validità superiore ad una data di riferimento ed afferenti ad una determinata ASST Territoriale (profilo RLOrganizationL1).

| SCOPE | Ricerca tutte le Organization con profilo L2 la cui data di fine validità è maggiore di una data di riferimento, che sono parte di un determinato codice L1 afferente ad una ASST Territoriale e sono di una o più tipologie (es. RIC,RSA) |
|---|---|
| VERB | GET |
| BASE | http://localhost:52773/csp/healthshare/nprifhirserver/fhir/r4 |
| URL | /Organization?_profile=https://example.org/fhir/StructureDefinition/RLOrganizationL2& dataFineValidita={datadiRiferimento}&… |

A titolo esemplificativo, la chiamata: 

    Organization?_profile=https%3A//example.org/fhir/StructureDefinition/ RLOrganizationL2&dataFineValidita=gt2018-04-05 &partof:Organization.identifier=030720&type=CONS

restituirà tutte i consultori (CONS) afferenti alla ASST Bergamo Est (030720) con una data di fine validità superiore al 05/04/2018.
