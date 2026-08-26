---
title: Creare e gestire flussi di lavoro in uscita
description: Scopri come creare, condividere, rivedere e gestire flussi di lavoro in uscita generati dall’intelligenza artificiale in Sales Qualifier per eseguire cadenze di sensibilizzazione basate su obiettivi.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/n3FbuiM2zF9QSqaKx1bhBSdbsf-w7vEsEGjCQTBo3g4'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 1905
ht-degree: 0%

---


# Flussi di lavoro in uscita

Un flusso di lavoro in uscita è una cadenza di estensione guidata da un obiettivo. Puoi definire l’obiettivo e i criteri di targeting. L’intelligenza artificiale propone quindi una cadenza multi-touch e scrive contenuti e-mail personalizzati per ogni potenziale cliente. Prima di attivare la cadenza, rivedi e approva ogni e-mail.

Un flusso di lavoro in uscita collega quattro elementi:

* **Obiettivo**: il risultato desiderato dall&#39;estensione, ad esempio la prenotazione di una chiamata di individuazione o l&#39;aumento della registrazione dell&#39;evento.
* **Filtri di targeting**—Condizioni che determinano quali potenziali clienti sono idonei.
* **Cadenza punto di contatto**: sequenza ordinata di passaggi di e-mail, telefonata e LinkedIn InMail.
* **Contenuto e-mail personalizzato**: contenuto generato da IA in base al profilo del potenziale cliente, al contesto dell&#39;account, alla cronologia del coinvolgimento e alle notizie recenti.

L’intelligenza artificiale utilizza l’obiettivo di suggerire filtri di targeting, progettare la cadenza, redigere i prompt dei punti di contatto e personalizzare ogni e-mail generata.

## Concetti chiave

| Concetto | Descrizione |
| --- | --- |
| **Flusso di lavoro in uscita** | Un’attività in uscita riutilizzabile definita da un obiettivo, da filtri di targeting, cadenza e impostazioni. |
| **Obiettivo** | Cosa dovrebbe fare la sensibilizzazione. |
| **Punto di contatto** | Un passaggio nella cadenza (e-mail, chiamata telefonica o LinkedInMail), pianificato in relazione all’iscrizione. |
| **Prompt punto di contatto** | Le istruzioni che l’IA segue durante la generazione di una riga dell’oggetto e del corpo dell’e-mail per un potenziale cliente, tra cui tono, lunghezza, focus e call to action. |
| **Cadenza** | La sequenza completa dei punti di contatto: quanti, in quale ordine e in quali giorni. |
| **Filtro di targeting** | Condizione che limita il flusso di lavoro in uscita a un sottoinsieme di potenziali clienti. |
| **Bozza** | Un’e-mail generata pronta per la revisione ma non ancora approvata. |
| **Motivazione** | Spiegazione dell’intelligenza artificiale di come ha scritto una determinata e-mail, inclusi i segnali e le origini dati utilizzati. |
| **Iscrizione** | Approvazione delle bozze di un potenziale cliente, che attiva la cadenza e mette in coda le e-mail da inviare durante la finestra di invio del flusso di lavoro in uscita. |

Le sezioni seguenti spiegano come creare un flusso di lavoro in uscita, esaminare le e-mail generate, approvare i potenziali clienti e gestire i flussi di lavoro in uscita.

## Creare un flusso di lavoro in uscita

La procedura guidata Flusso di lavoro in uscita prevede cinque passaggi: **[!UICONTROL Obiettivo]**, **[!UICONTROL Targeting]**, **[!UICONTROL Generazione punti di contatto]**, **[!UICONTROL Impostazioni]** e **[!UICONTROL Aggiungi potenziali]**. L&#39;obiettivo determina i passaggi rimanenti.

1. Nel menu di navigazione a sinistra, seleziona **[!UICONTROL Flussi di lavoro in uscita]**.
1. Nella scheda **[!UICONTROL Sfoglia]**, seleziona **[!UICONTROL + Crea flusso di lavoro in uscita]** nell&#39;angolo superiore destro.

### Passaggio 1: definire l’obiettivo

L’obiettivo definisce il risultato previsto e guida il targeting, la cadenza e la generazione di e-mail.

1. Seleziona **[!UICONTROL Inizia da zero]** per scrivere il tuo obiettivo oppure seleziona **[!UICONTROL Inizia da modello]** per utilizzare un modello salvato.

1. Seleziona uno dei **[!UICONTROL obiettivi consigliati]** corrispondenti alla tua azienda. Ogni raccomandazione include una breve spiegazione del perché. Seleziona un consiglio per completare l&#39;obiettivo, seleziona **[!UICONTROL Visualizza tutti]** per sfogliare l&#39;intero set di consigli o inserisci un obiettivo personalizzato. Puoi anche scegliere dall&#39;elenco **[!UICONTROL Obiettivi popolari]**.
1. Seleziona **[!UICONTROL Successivo: Targeting]**.

Indica un risultato specifico nell’obiettivo. Ad esempio, immettere `Book a 15-minute discovery call with marketing leaders evaluating campaign automation` anziché `Promote campaign automation`.

### Passaggio 2: configurare i filtri di targeting

I filtri di targeting definiscono quali potenziali clienti sono idonei. Quando si aggiungono i potenziali clienti in un secondo momento, nell&#39;elenco di selezione vengono visualizzati solo i potenziali clienti che corrispondono a questi filtri.

![Filtri di destinazione](assets/create-workflow-targeting.png){width="800" zoomable="yes"}

1. Selezionare la freccia rivolta verso il basso per aprire l&#39;elenco **[!UICONTROL Aggiungi un filtro]**, quindi selezionare un filtro.

1. Imposta i valori per il filtro.
1. Aggiungi altri filtri per restringere il pubblico.

1. Seleziona **[!UICONTROL Avanti: genera punti di contatto]**.

### Passaggio 3: generare e rivedere i punti di contatto

Dopo aver configurato il targeting, l’intelligenza artificiale analizza l’obiettivo e i criteri di targeting, definisce la cadenza e scrive un prompt per ogni punto di contatto. La cadenza può includere passaggi e-mail, telefonata e LinkedInMail.

![Punti di contatto](assets/create-workflow-touchpoints.png){width="800" zoomable="yes"}

Espandi un punto di contatto e-mail per leggerne il prompt. Il prompt guida l’intelligenza artificiale durante la scrittura dell’e-mail di ogni potenziale cliente, inclusi il tono, la lunghezza, lo stato attivo e call to action.

#### Rigenera la cadenza

Se la cadenza non è quella desiderata, selezionare **[!UICONTROL Rigenera]** e immettere un&#39;istruzione di ottimizzazione. Ad esempio:

* `Use three touchpoints across two weeks`
* `Lead with an executive briefing offer in the first email`
* `Add a nurture touch focused on a relevant case study`

AI riscrive la frequenza completa in base alle istruzioni. Per regolare un punto di contatto e-mail, modificane il prompt invece di rigenerare l’intera cadenza.

Imposta un ritardo del punto di contatto in giorni, ore e minuti. Imposta giorni, ore e minuti su `0` per inviare il punto di contatto senza alcuna attesa dopo l’iscrizione o il completamento del punto di contatto precedente. Utilizza un ritardo più lungo per spaziare i punti di contatto successivi all’interno della cadenza.

#### Utilizzare il Knowledge Center nei prompt

Se l&#39;organizzazione ha creato un playbook del [Centro informazioni](knowledge-center.md), fare riferimento al file nel prompt. Denomina il documento e descrivi il contesto da utilizzare. Immettere ad esempio `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`.

Quando la cadenza e i prompt sono pronti, selezionare **[!UICONTROL Avanti: Impostazioni]**.

Affina i prompt dei punti di contatto prima di generare le e-mail dei potenziali clienti. IA utilizza questi prompt per ogni prospect selezionato.

### Passaggio 4: configurare le impostazioni del flusso di lavoro in uscita

Il passaggio **[!UICONTROL Impostazioni]** controlla il modo in cui viene eseguito il flusso di lavoro in uscita.

![Pannello impostazioni](assets/create-workflow-settings.png){width="800" zoomable="yes"}

1. Rivedi il nome del flusso di lavoro in uscita **** e modificalo se necessario.
1. In **[!UICONTROL Numero massimo di potenziali clienti per flusso di lavoro in uscita]**, confermare il numero massimo di potenziali clienti che il flusso di lavoro in uscita può gestire contemporaneamente.
1. Imposta la **[!UICONTROL finestra di invio]** per le ore in cui le e-mail in uscita possono essere inviate.
1. Seleziona i giorni della settimana in cui le e-mail possono essere inviate. Per evitare gli invii di fine settimana, seleziona solo i giorni della settimana invece di utilizzare un&#39;impostazione **[!UICONTROL Ignora fine settimana]** separata.
1. Scegli se inviare durante le ore più attive di ogni prospect.
1. Per interrompere automaticamente i punti di contatto di follow-up quando un prospect registra una riunione, attivare **[!UICONTROL Pausa prenotazione riunione]**.
1. Scegli se utilizzare il fuso orario di ogni prospect o il flusso di lavoro in uscita **[!UICONTROL Fuso orario]** per la tempistica di invio. Se utilizzi il fuso orario del flusso di lavoro in uscita, verifica che corrisponda al pubblico.
1. In **[!UICONTROL Autorizzazioni]**, mantieni **[!UICONTROL Privato]** (impostazione predefinita) o seleziona **[!UICONTROL Condiviso con tutti]**. Per ulteriori dettagli, vedere [Condividere un flusso di lavoro in uscita](#share-an-outbound-workflow).
1. Seleziona **[!UICONTROL Salva e aggiungi prospect]**.

Il piè di pagina di rinuncia è configurato a livello globale da un amministratore e si applica alle e-mail in uscita indipendentemente dalle impostazioni del flusso di lavoro in uscita. Consulta [Configurare la rinuncia e-mail globale](integrations.md#configure-global-email-opt-out).

### Passaggio 5: aggiungere potenziali clienti e avviare la generazione di e-mail

Il salvataggio apre la vista di selezione del prospect con i filtri di targeting del passaggio 2 applicati.

1. Rivedi l&#39;elenco.

   Le righe in genere includono il nome del potenziale cliente, l’account, l’e-mail, la qualifica professionale, lo stato del coinvolgimento e lo stato del potenziale cliente.

1. Regolare i filtri qui se è necessario espandere o restringere l’elenco.
1. Seleziona i potenziali clienti utilizzando le caselle di controllo.
1. Seleziona **[!UICONTROL Successivo: controlla i punti di contatto]** per avviare la generazione di e-mail per ogni potenziale cliente.

IA genera un’e-mail personalizzata per ogni potenziale cliente e punto di contatto e-mail selezionati. I punti di contatto Phone e LinkedInMail rimangono passaggi pianificati. Per continuare a lavorare durante la generazione, selezionare **[!UICONTROL Notifica quando pronto]**.

Per ogni potenziale cliente, l’intelligenza artificiale combina il prompt del punto di contatto con i dati di persone e account, la cronologia del coinvolgimento e le notizie recenti per produrre un oggetto e un corpo.

## Rivedere e perfezionare le e-mail generate

Al termine della generazione, nella vista dei dettagli Flusso di lavoro in uscita viene richiesto di esaminare le bozze. Sales Qualifier invia l’e-mail solo dopo l’approvazione.

1. Nella visualizzazione dei dettagli del flusso di lavoro in uscita, selezionare **[!UICONTROL Rivedi bozze]** nel banner.
1. Il passaggio **[!UICONTROL Rivedi punti di contatto]** ha due schede:
   * **[!UICONTROL Pronto per la revisione]**: messaggi di posta elettronica che hanno completato la generazione.
   * **[!UICONTROL Generazione in corso]** - Messaggi di posta elettronica ancora in fase di scrittura.
1. Nell’elenco dei potenziali clienti a sinistra, seleziona un nome per caricare i punti di contatto del potenziale cliente a destra.
1. Utilizzare la freccia (**>**) in un punto di contatto per espandere e leggere l&#39;oggetto e il corpo completi.

### Leggere il ragionamento dell’intelligenza artificiale

Per ogni e-mail generata, **[!UICONTROL Reasoning]** spiega come l&#39;intelligenza artificiale ha creato il messaggio, inclusi segnali, attributi e origini che hanno modellato il contenuto e call to action. Esamina queste informazioni e convalida la personalizzazione prima di approvare.

### Modifica direttamente le e-mail

Per piccole modifiche di testo o tono:

1. Nel punto di contatto espanso, seleziona l&#39;icona **[!UICONTROL Modifica]** per aprire l&#39;editor.
1. Modifica l&#39;oggetto o il corpo.
1. Seleziona **[!UICONTROL Salva]**.

### Ottimizzare le e-mail con l’intelligenza artificiale

Per modifiche strutturali o di enfasi, utilizza **[!UICONTROL Genera con IA]**. AI riscrive l’e-mail mantenendo il contesto di personalizzazione.

1. Nell&#39;editor e-mail, seleziona **[!UICONTROL Genera con IA]**.

1. Immettere un&#39;istruzione di cancellazione, ad esempio:
   * `Make it shorter and more direct. Keep it under 100 words.`
   * `Focus more on the prospect's role and how the solution helps them specifically.`
   * `Change the call-to-action to suggest a 15-minute introductory call instead.`
1. Rivedi la revisione e modificala se necessario.
1. Seleziona **[!UICONTROL Salva]**.

>[!TIP]
>
>Utilizza modifiche dirette per le modifiche di testo e tono. Utilizza **[!UICONTROL Genera con IA]** per riscrivere l&#39;e-mail.

## Approva e iscrivi potenziali clienti

L’approvazione attiva la cadenza per un potenziale cliente. Il sistema non invia e-mail a un potenziale cliente finché non li approvi e non li registri.

1. Nell’elenco a sinistra dei potenziali clienti, seleziona i potenziali clienti di cui hai rivisto e-mail e che sei pronto a inviare.
1. Seleziona **[!UICONTROL Approva e iscrivi prospect]** nell&#39;angolo inferiore destro.

Le e-mail approvate vengono inviate in base ai giorni selezionati, alla finestra di invio, all’opzione ore attive e all’impostazione del fuso orario del flusso di lavoro in uscita. Un punto di contatto con un ritardo pari a zero invia senza attesa; ogni punto di contatto segue il ritardo configurato. I potenziali clienti non approvati rimangono in **[!UICONTROL Pronti per la revisione]**.

## Condividere un flusso di lavoro in uscita

Ogni flusso di lavoro in uscita ha un&#39;impostazione **[!UICONTROL Autorizzazioni]**. I flussi di lavoro in uscita sono **[!UICONTROL Privati]** per impostazione predefinita. Il proprietario può selezionare **[!UICONTROL Condiviso con tutti]** per rendere disponibile al team un flusso di lavoro in uscita.

>[!CAUTION]
>
>La condivisione è permanente. Dopo che un flusso di lavoro in uscita è impostato su **[!UICONTROL Condiviso con tutti]**, non può essere ripristinato su **[!UICONTROL Privato]**.

In un flusso di lavoro in uscita condiviso, i team possono registrare i propri potenziali clienti. Ogni persona può gestire o mettere in pausa solo i potenziali clienti a cui è iscritta, incluso l’utilizzo di azioni in blocco. Solo il proprietario del flusso di lavoro in uscita può modificare le impostazioni a livello di piano, tra cui la pianificazione, il fuso orario, la cadenza e altre impostazioni. Queste impostazioni sono di sola lettura per i colleghi.

Utilizza questi filtri per mantenere attivi i flussi di lavoro in uscita condivisi e i risultati:

* In **[!UICONTROL Potenziali coinvolti]** e **[!UICONTROL Prestazioni]**, utilizza **[!UICONTROL Iscritto da]** per filtrare i potenziali clienti in base alla persona che li ha iscritti. Il filtro utilizza come valori predefiniti i potenziali clienti che hai iscritto.
* Nella scheda **[!UICONTROL Sfoglia]**, utilizza il filtro di condivisione per selezionare **[!UICONTROL Condiviso da me]**, **[!UICONTROL Condiviso con me]**, **[!UICONTROL Privato]** o **[!UICONTROL Tutto]**.

## Gestione delle risposte fuori sede

Quando un potenziale cliente risponde con un messaggio fuori sede, il flusso di lavoro in uscita lo gestisce automaticamente.

* **Ripresa automatica**: attivata per impostazione predefinita. Se la risposta fuori sede include una data di ritorno, il flusso di lavoro in uscita riprende la cadenza in tale data. Se non viene specificata una data di ritorno, il flusso di lavoro in uscita riprende dopo un buffer di ripresa dopo configurabile dal team.
* **Opzioni manuali**: un rappresentante può comunque selezionare **[!UICONTROL Riprendi ora]** o pianificare una data di ripresa specifica. Vedi [Gestione dei flussi di lavoro in uscita esistenti](#manage-existing-outbound-workflows).

## Gestisci flussi di lavoro in uscita esistenti

Nella pagina **[!UICONTROL Flussi di lavoro in uscita]**, la scheda **[!UICONTROL Sfoglia]** elenca tutti i flussi di lavoro in uscita disponibili. Ogni scheda mostra l’obiettivo, i punti di contatto configurati e le metriche delle prestazioni. Utilizzare questa visualizzazione per monitorare i flussi di lavoro in uscita, esaminare le bozze o aggiungere potenziali clienti.

## Posta in uscita e-mail

Nella [Posta in uscita](email-outbox.md) sono elencate le e-mail automatizzate inviate per tuo conto ed eventuali risposte.

## Prenotazione riunione

Quando connetti il calendario, Sales Qualifier genera un collegamento di prenotazione personale che i potenziali clienti possono utilizzare per pianificare con te il tempo.

* **Collegamenti prenotazione** - Configura la connessione al calendario e la disponibilità in [Impostazioni profilo](profile-settings.md). Aggiungi il collegamento di prenotazione alla firma e-mail in modo che venga visualizzato nelle e-mail in uscita.
* **Inserimento cadenza** - Sales Qualifier inserisce il collegamento di prenotazione nei punti rilevanti di una cadenza. Potete modificarne la posizione.
* **Pausa prenotazione** - Quando un prospect registra una riunione, **[!UICONTROL Pausa prenotazione riunione]** interrompe ulteriori follow-up. Vedere [Passaggio 4: Configurare le impostazioni del flusso di lavoro in uscita](#step-4-configure-outbound-workflow-settings).

Tieni traccia degli esiti della prenotazione nella pagina [Prestazioni in uscita](performance.md).

## Best practice per i flussi di lavoro in uscita

* **Definisci un obiettivo specifico.** Il targeting, la cadenza e le e-mail derivano tutti dall’obiettivo. Indicare il risultato che si desidera ottenere con il flusso di lavoro in uscita.
* **Finalizza i prompt dei punti di contatto prima della generazione per singolo prospect.** Dopo la generazione in blocco, le modifiche vengono in genere apportate un prospect alla volta.
* **Usa il ragionamento come controllo qualità.** Se viene enfatizzato il segnale sbagliato o se manca un segnale rilevante, modifica l’e-mail o rivedi il prompt del punto di contatto e rigenera la cadenza.
* **Corrispondenza tra lo strumento di modifica e la modifica.** Utilizza modifiche dirette per la formulazione e il tono. Utilizza **[!UICONTROL Genera con IA]** per la ristrutturazione o la ridefinizione dei frame.
* **Approva solo ciò che hai rivisto.** Espandi i punti di contatto, leggi il contenuto e perfeziona eventualmente prima dell’iscrizione.

>[!MORELIKETHIS]
>
>* [Attività](tasks.md)
>* [Centro conoscenze](knowledge-center.md)
>* [Prestazioni in uscita](performance.md)
