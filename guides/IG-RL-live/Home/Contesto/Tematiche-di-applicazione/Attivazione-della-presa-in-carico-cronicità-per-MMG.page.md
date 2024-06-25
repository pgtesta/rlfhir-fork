# {{page-title}}

I servizi FHIR consentono ai MMG di accedere tramite le proprie Cartelle Cliniche Elettroniche alle funzionalità di SGDT in maniera integrata e senza la necessità di effettuare l’autenticazione nel Sistema con il fine di attivare una presa in carico per cronicità per i propri assistiti redigendone il PAI.

A partire dalla CE, il MMG può attivare il servizio di gestione dei pazienti cronici mediante una funzionalità specifica che genera una chiamata POST ad un API REST FHIR di tipo $process-message verso SGDT. In seguito, la piattaforma processa le informazioni contenute nel messaggio FHIR ricevuto, descritte nel profilo {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMessageHeaderMMG.page.md}} e definito a partire dalla risorsa FHIR [MessageHeader](http://hl7.org/fhir/R4/messageheader.html), in modo da effettuare una serie di validazioni. In particolare, SGDT contatta il sistema NAR per recuperare le informazioni anagrafiche complete, definite nel profilo FHIR {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientBase.page.md}}, e contatta i servizi GPC per verificare le condizioni di arruolabilità del paziente. Se le validazioni sono tutte positive, SGDT prepara all’interno del proprio ambiente le informazioni necessarie per la redazione del PAI e restituisce alla CE-MMG l’URL per il passaggio di contesto; se l’esito è negativo, SGDT restituisce il dettaglio dell’errore alla CE-MMG. 

Dalla Cartella Elettronica viene aperta in automatico via web la schermata di SGDT del Progetto Individuale relativa al paziente. Se l’assistito non è ancora stato preso in carico sulla piattaforma, nella sezione accoglienza verranno precompilati i campi:

* Motivo segnalazione = Inviato da MMG
* Tipologia accesso = Socio-Sanitario
* Tipologia di bisogno = Semplice
* Attività da svolgere = Definizione Del Progetto Individuale

Inoltre, viene creato in automatico il Progetto individuale precompilato con le informazioni relative alle patologie, tra cui il livello di gravità dello stato di cronicità e descritte nel profilo FHIR {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionProblemiSalute.page.md}}, ed eventualmente alla farmacoterapia, definita nel profilo {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestTerapiaFarmacologica.page.md}}, entrambi contenuti nel profilo {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLBundleMMG.page.md}}. Il medico ha la possibilità di modificare o integrare ulteriori informazioni del PI.
Infine, il MMG attiva il Progetto individuale dalla sezione Interventi sanitari e automaticamente invia le informazioni del PI al sistema GPC.
