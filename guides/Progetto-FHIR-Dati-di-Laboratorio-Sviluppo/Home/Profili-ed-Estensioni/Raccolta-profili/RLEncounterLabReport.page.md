# RLEncounterLabReport

- [RLEncounterLabReport](#rlencounterlabreport)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLEncounterLabReport è stato strutturato a partire dalla risorsa generica FHIR [Encounter](http://hl7.org/fhir/R4/encounter.html) per descrivere i dati relativi all'incontro per la specifica richiesta tramite il profilo della risorsa Encounter per il referto di laboratorio.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab }}.

<br>
<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Hybrid View')">Hybrid View</button>
  <button class="tablinks" onclick="openTab(event, 'Snapshot View')">Snapshot View</button>
  <button class="tablinks" onclick="openTab(event, 'Differential View')">Differential View</button>
  <button class="tablinks" onclick="openTab(event, 'Table View')">Table View</button>
  <button class="tablinks" onclick="openTab(event, 'XML View')">XML View</button>
  <button class="tablinks" onclick="openTab(event, 'JSON View')">JSON View</button>
  <button class="tablinks" onclick="openTab(event, 'Esempi')">Esempi applicati al profilo</button>
</div>

<div id="Snapshot View" class="tabcontent">
  <h3>Snapshot View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab , snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab , diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab , hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab , snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab , snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:http://hl7.it/fhir/lab-report/StructureDefinition/encounter-it-lab , snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
  {{link:esempio-Location-LuogoPrestazioneCureDom}}
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

Attualmente non sono state definite tipologie di ricerca.

<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Attualmente non sono definiti Search Parameters.

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set relativi al profilo RLEncounterLabReport:

| Nome    | Descrizione    | Riferimento   al dettaglio della codifica    |
|---|---|---|
| language | Lingua utilizzata per descrivere la risorsa  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/languages)  |
| encounter status | Stato della risorsa encounter  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-status|4.0.1)  |
| encounter class | Classe dell'encounter  | La codifica è definita dal Valueset (http://terminology.hl7.org/ValueSet/encounter-class)  |
| act encounter code | Qualifica dell'ActEncounterClass | La codifica è definita dal Valueset (http://terminology.hl7.org/ValueSet/v3-ActEncounterCode)  |
| encounter type | Tipo di encounter | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-type)  |
| service type | Tipo di servizio | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/service-type)  |
| act priority | Codici per specificare l'urgenza associata all'Act | La codifica è definita dal Valueset (http://terminology.hl7.org/ValueSet/v3-ActPriority)  |
| encounter participant type | Tipo di codice per indicare il modo in cui un utente è coinvolto nell'encounter | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-participant-type)  |
| encounter reason | Codice per indicare il motivo dell'encounter  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-reason)  |
| diagnosis role| Codice per indicare il ruolo di una diagnosi nell'encounter| La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/diagnosis-role)  |
| encounter admit source| Codice per indicare la provenienza del paziente | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-admit-source)  |
| admission indicator| Codice per indicare che il paziente è ri-ammesso in una struttura dalla quale era stato dimesso, e circostanze per cui ciò è avvenuto | La codifica è definita dal Valueset (http://terminology.hl7.org/ValueSet/v2-0092)  |
| encounter diet| Codici usati per indicare le preferenze o restrizioni sulla dieta del paziente  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-diet)  |
| encounter special courtesy| Codici usati per cure speciali rivolte ai pazienti  | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-special-courtesy)  |
| encounter special arrangements|  Codici usati per indicare il tipo di attrezzatura speciale fornita in loco per la visita | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-special-arrangements)  |
| encounter discharge disposition| Codici utilizzati per la dimissione del paziente | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-discharge-disposition)  |
| encounter location status| Stato della location | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/encounter-location-status|4.0.1)  |
| location physical type| Tipo di location | La codifica è definita dal Valueset (http://hl7.org/fhir/ValueSet/location-physical-type)  |


