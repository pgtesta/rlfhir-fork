# Esempio di ricerca esame specifico di laboratorio per un determinato paziente e informazioni di contesto

Questa ricerca permette di reperire i dettagli dei risultati di uno o più referti relativi a una specifica tipologia di esame di laboratorio effettuato da un determinato paziente presso una struttura sanitaria, permettendo di selezionare gli esami effettuati a partire da una certa data o all’interno di un certo intervallo temporale. 
Per ottenere ulteriori informazioni rispetto la richiesta {{pagelink:Home/Esempi/Raccolta-esempi/RLEsame1BundleSearchSet.page.md}}, quali ad esempio il campione su cui è stata effettuata l’osservazione o chi ha prodotto i risultati, è possibile aggiungere opzionalmente altre risorse alla richiesta con i seguenti parametri riportati: 

- _include = Observation:specimen: da inserire se si vuole ottenere anche l’informazione sul campione di laboratorio che ha prodotto il risultato 

- _include = Observation:performer: include nella risposta la risorsa PractitionerRole che contiene le informazioni sui soggetti responsabili dell’osservazione di laboratorio 

- _revinclude = Provenance:target:  include nella risposta la risorsa Provenance che contiene le informazioni su chi ha firmato il documento e l’identificativo univoco del referto da cui proviene l’osservazione 

**Richiesta:** 

| SCOPE |  Ricerca esame specifico di laboratorio per un determinato paziente e informazioni di contesto |
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Observation?code=2339-0&date=gt2024-01-01&date=lt2024-08-01&category=laboratory&_include=Observation:patient &patient.identifier=RSSMRA71E01F205E&_include=Observation:specimen&_include=Observation:performer&_revinclude=Provenance:target&_include=Provenance:agent&_include=PractitionerRole:practitioner&_include=PractitionerRole:organization |

**Risposta**

{{json:Bundle/esempio-esame-specifico-2}}
