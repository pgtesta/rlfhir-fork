# {{page-title}}

I servizi FHIR consentono all’applicativo di gestione 1116117 NEA di trasmettere alla rete delle COT in maniera integrata la richiesta di attivazione di un servizio socio-assistenziale. 
Nell’integrazione tra l’applicativo di gestione 1116117 NEA e la piattaforma SGDT sono previsti due modelli di interoperabilità, adottati in funzione dei due diversi scenari di integrazione previsti.

1) **Modello di interoperabilità FHIR Messaging - Invio richiesta**

Il modello FHIR Messaging viene utilizzato per trasmettere la richiesta di attivazione di un servizio socio-assistenziale alla rete delle COT. 
Le informazioni contenute in tale richiesta sono state raccolte:
- dagli operatori di NEA nelle fasi di inquadramento telefonico del cittadino per valutarne il bisogno e indicare il possibile setting assistenziale che deve essere attivato dalle COT;
- dal personale di Continuità Assistenziale come esito della eventuale visita domiciliare (Referto Visita).

Queste informazioni devono essere inserite dall’applicativo di gestione 116117 NEA in un Bundle in cui il primo profilo presente è [RLMessageHeaderNEA](Home/Profili-ed-Estensioni/Raccolta-profili/RLMessageHeaderNEA.page.md).
Questo profilo contiene i metadati del messaggio, cioè le informazioni pertinenti il messaggio scambiato tra l’applicativo gestione 116117 NEA e la piattaforma SGDT e i dettagli della richiesta generata sull’applicativo gestione 116117 NEA.
L’altro profilo essenziale contenuto del Bundle è il profilo [RLServiceRequestServiziSocioAssistenziali](Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestServiziSocioAssistenziali.page.md) che contiene i dettagli del servizio socio-assistenziale richiesto.
La piattaforma SGDT risponde con un Bundle contenente il profilo [RLOperationOutcomeNEA](Home/Profili-ed-Estensioni/Raccolta-profili/RLOperationOutcomeNEA.page.md) che descrive l’esito dell’elaborazione del messaggio.

In caso di esito positivo restituisce l’identificativo univoco della richiesta generato da SGDT, associato al profilo [RLServiceRequestServiziSocioAssistenziali](Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestServiziSocioAssistenziali.page.md). Questo identificativo è indispensabile per utilizzare successivamente il servizio di consultazione stato, descritto di seguito.
In caso di esito negativo il profilo [RLOperationOutcomeNEA](Home/Profili-ed-Estensioni/Raccolta-profili/RLOperationOutcomeNEA.page.md) restituisce i dettegli dell’errore.


{{render:guides/IG-RL-sviluppo/pics/nea1.png, fig.cap="Flusso dati logico per l’invio di una richiesta di attivazione di un servizio socio-assistenziale alla piattaforma SGDT"}}
<p style="text-align: center;">Flusso dati logico per l’invio di una richiesta di attivazione di un servizio socio-assistenziale alla piattaforma SGDT</p>

{{render:guides/IG-RL-sviluppo/pics/nea2.png, fig.cap="Flusso dati logico per la risposta da parte della piattaforma SGDT con l’esito dell’elaborazione del messaggio di richiesta"}}
<p style="text-align: center;">
Flusso dati logico per la risposta da parte della piattaforma SGDT con l’esito dell’elaborazione del messaggio di richiesta</p>

2)	**Modello di interoperabilità FHIR REST - Consultazione stato**

Il modello di interoperabilità FHIR REST viene utilizzato per richiedere alla piattaforma SGDT lo stato della richiesta di attivazione di un servizio socio-assistenziale precedentemente inviata.
Il **richiedente** è l’applicativo di gestione 116117 NEA e la richiesta deve contenere, tra i parametri di ricerca, il codice generato dall'applicativo di gestione 116117 NEA quando invia la richiesta a SGDT e il codice generato da SGDT quando la richiesta è stata ricevuta correttamente, entrambi associati al profilo [RLServiceRequestServiziSocioAssistenziali](Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestServiziSocioAssistenziali.page.md).
SGDT è l’**espositore** che risponde con il profilo [RLBundleStatoNEA](Home/Profili-ed-Estensioni/Raccolta-profili/RLBundleStatoNEA.page.md) contenente il profilo [RLServiceRequestServiziSocioAssistenziali](Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestServiziSocioAssistenziali.page.md)i, nel quale è presente lo stato aggiornato della richiesta (*active* se richiesta è nello stato aperta; *completed*: se la richiesta è nello stato chiusa) e il profilo [RLPatientCittadino](Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientCittadino.page.md) contenente i dati anagrafici del paziente. 

{{render:guides/IG-RL-sviluppo/pics/nea3.png, fig.cap="Flusso dati logico per la richiesta dello stato della richiesta alla piattaforma SGDT"}}
<p style="text-align: center;">
Flusso dati logico per la richiesta dello stato della richiesta alla piattaforma SGDT</p>