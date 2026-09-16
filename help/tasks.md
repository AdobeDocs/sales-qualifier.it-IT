---
title: Attività in Adobe Marketo Qualifier
description: Scopri come elaborare le attività manuali di outreach e rivedere i potenziali clienti suggeriti dall’agente nella coda delle attività di Adobe Marketo Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/MbTN1r-ARrW-XYtdIS-KZT7K1Lk-B3GihT8iXL60GrQ'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: d967b633fcb63c64169d3e3fbf305fd2ff82236d
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%
---

# Attività

Utilizza **[!UICONTROL Attività]** per completare le azioni generate dai flussi di lavoro in uscita. Selezionare un&#39;attività, eseguire un&#39;azione, contrassegnarla come completata e continuare con l&#39;attività successiva senza uscire dalla pagina.

Nel menu di navigazione a sinistra, vai a **[!UICONTROL Attività]** > **[!UICONTROL Attività]**.

![Pannello attività](assets/tasks.png)

## Visualizzazioni attività

La pagina presenta due schede:

* **[!UICONTROL Attività manuali]**—Chiamate telefoniche, LinkedInMails e revisioni e-mail per potenziali clienti iscritti a un flusso di lavoro in uscita.
* **[!UICONTROL Suggerimenti agente]**: potenziali clienti che soddisfano i criteri di targeting di un flusso di lavoro in uscita e sono consigliati per la registrazione.

Ogni scheda ha i propri filtri, opzioni di ordinamento e layout a due pannelli. L&#39;elenco delle attività viene visualizzato a sinistra, mentre il pannello di lavoro viene visualizzato a destra. Quando si seleziona un’attività, i relativi dettagli vengono caricati nel pannello di lavoro. Quando si completa un&#39;attività, l&#39;attività successiva viene selezionata automaticamente.

## Attività manuali

### Tipi di attività

Le attività manuali sono associate ai passaggi del flusso di lavoro in uscita e sono disponibili in tre tipi:

* **[!UICONTROL Chiamata telefonica]**—Creata quando una cadenza raggiunge un passaggio di chiamata telefonica. Il pannello di lavoro mostra il numero di telefono del potenziale cliente e, se disponibile, uno script di chiamata generato dall’intelligenza artificiale.

* **[!UICONTROL LinkedIn InMail]**—Creato quando una cadenza raggiunge un passaggio LinkedInMail. Il pannello di lavoro mostra il contenuto da copiare e inviare da LinkedIn. Espandi **[!UICONTROL Motivo IA]** per rivedere il motivo.

* **[!UICONTROL Revisione e-mail]** - Creata dopo che Adobe Marketo Qualifier ha generato le e-mail personalizzate di un potenziale cliente. Seleziona **[!UICONTROL Rivedi e-mail]** per rivedere e approvare le bozze prima dell&#39;inizio dell&#39;estensione. Consulta [Rivedere e perfezionare le e-mail generate](outbound-workflows.md#review-and-refine-generated-emails).

![Revisione e-mail](assets/tasks-review.png)

### Pannello Lavoro

Per un&#39;attività **[!UICONTROL Chiamata telefonica]** o **[!UICONTROL LinkedInMail]**, il pannello di lavoro contiene:

* **[!UICONTROL Prospect]**: nome, indirizzo di posta elettronica e numero di telefono del prospect, se applicabile.
* **[!UICONTROL Flusso di lavoro in uscita]** - Il nome del flusso di lavoro in uscita collegato, la data di scadenza e l&#39;indicatore di salto automatico, se applicabile.
* **Contenuto attività**: script di chiamata o contenuto InMail.
* **[!UICONTROL Note]** - Le note vengono salvate automaticamente quando si seleziona un&#39;altra attività. Non è possibile modificare le note dopo che un&#39;attività è stata completata, saltata o annullata.

### Generare uno script di chiamata

Per un&#39;attività **[!UICONTROL Phone Call]**, selezionare **[!UICONTROL Generate call script]**. Al termine della generazione, selezionare **[!UICONTROL Visualizza script di chiamata dettagliato]**. Se la generazione non riesce, riprova dal pannello.

### Azioni attività

Nell’intestazione del pannello di lavoro sono disponibili due azioni:

* **[!UICONTROL Contrassegna come completato]**. Utilizzare questa azione dopo aver eseguito la chiamata, inviato InMail o esaminato le e-mail. La coda avanza all&#39;operazione successiva.
* **[!UICONTROL Ignora]** - Utilizza questa azione quando non riesci a completare il passaggio ma desideri mantenere il prospect nel flusso di lavoro in uscita. Il prospect avanza al passaggio successivo.

Le attività di telefonata e LinkedInMail possono essere ignorate automaticamente se rimangono aperte oltre la soglia configurata. Un salto automatico fa avanzare il prospect attraverso la cadenza e non influisce sui punti di contatto e-mail pianificati.

### Filtrare, cercare e ordinare

La barra degli strumenti sopra l’elenco controlla quali attività vengono visualizzate e in quale ordine. Le opzioni di filtro e ordinamento vengono salvate e riapplicate alla successiva apertura della pagina.

* **[!UICONTROL Filtro]**—Apri il pannello dei filtri:
  * **[!UICONTROL Stato]**—**[!UICONTROL Corrente]**, **[!UICONTROL In Arrivo]**, **[!UICONTROL Scaduto]**, **[!UICONTROL Completato]**, **[!UICONTROL Annullato]**, **[!UICONTROL Ignorato]**.
  * **[!UICONTROL Tipo di attività]**—**[!UICONTROL Revisione e-mail]**, **[!UICONTROL LinkedIn InMail]**, **[!UICONTROL Chiamata telefonica]**.
  * **[!UICONTROL Data di scadenza]**.
  * **[!UICONTROL Flusso di lavoro in uscita]**: elenco dei flussi di lavoro in uscita in cui è possibile eseguire ricerche.
* **[!UICONTROL Ordina]**—Ordina per data di scadenza o data di creazione. L&#39;ordinamento determina anche l&#39;ordine di avanzamento della coda.
* **[!UICONTROL Cerca attività]** - Trova le attività in base al nome del prospect, al nome della società o al flusso di lavoro in uscita. La ricerca è applicabile con i filtri attivi.

I filtri attivi vengono visualizzati come chip sotto la barra degli strumenti. Seleziona **[!UICONTROL Cancella tutto]** per reimpostarli.

### Stato attività

Ogni attività mostra il proprio stato corrente:

| Stato | Descrizione |
| --- | --- |
| **[!UICONTROL Corrente]** | Scade ora e pronto ad agire. Le attività correnti non mostrano alcun distintivo. |
| **[!UICONTROL In arrivo]** | Il passaggio precedente è completo, ma la data di scadenza è nel futuro. Puoi agire in anticipo se il momento è giusto. |
| **[!UICONTROL Scaduto]** | Scaduta e non ancora completata. L&#39;attività è contrassegnata per l&#39;attenzione. |
| **[!UICONTROL Completato]** | Hai completato l’azione e contrassegnato l’attività come completata. |
| **[!UICONTROL Ignorato]** | Il passaggio è stato saltato oppure è stato saltato automaticamente. Il prospect avanza nel flusso di lavoro in uscita. |
| **[!UICONTROL Annullato]** | Il sistema ha annullato l&#39;attività a causa di una modifica del flusso di lavoro in uscita. |

Le attività completate, saltate e annullate sono definitive. Le azioni non sono più disponibili e le note sono di sola lettura.

## Suggerimenti agente

Nella scheda **[!UICONTROL Suggerimenti agente]** sono elencati i potenziali clienti che soddisfano i criteri di targeting di un flusso di lavoro in uscita e sono consigliati per la registrazione. Per attivare i consigli, vedi [Flussi di lavoro in uscita](outbound-workflows.md).

Selezionare un suggerimento per esaminarlo nel pannello di lavoro:

* Un badge di recency contrassegna ogni suggerimento come **[!UICONTROL Nuovo]** o **[!UICONTROL Precedente]**.
* Nella tabella **[!UICONTROL contatti consigliati]** o **[!UICONTROL contatti consigliati]** sono elencati i potenziali clienti proposti con colonne per **[!UICONTROL Nome]**, **[!UICONTROL Titolo]**, **[!UICONTROL Account]**, **[!UICONTROL Stato]**, **[!UICONTROL E-mail]** e **[!UICONTROL Ultimo aggiornamento]**.

Sono disponibili due azioni:

* **[!UICONTROL Rivedi potenziali clienti]**—Apri il flusso di lavoro in uscita per rivedere e registrare i potenziali clienti consigliati. Consulta [Aggiungi potenziali clienti e avvia la generazione di e-mail](outbound-workflows.md#step-5-add-prospects-and-start-email-generation).
* **[!UICONTROL Contrassegna come completato]**—Ignora il suggerimento dopo averlo esaminato.

La scheda **[!UICONTROL Suggerimenti agente]** include **[!UICONTROL Filtri di stato Corrente]**, **[!UICONTROL Completata]** e **[!UICONTROL Annullata]**, un filtro del flusso di lavoro in uscita e un ordinamento in base alla data di creazione.

## Completare attività da un flusso di lavoro in uscita

Nella visualizzazione **[!UICONTROL Prospect coinvolti]** di un flusso di lavoro in uscita, un punto di contatto manuale fornisce le stesse opzioni **[!UICONTROL Contrassegna come completato]**, **[!UICONTROL Salta]** e note. Il completamento di un&#39;attività ne aggiorna lo stato anche nella pagina **[!UICONTROL Attività]**. Vedi [Flussi di lavoro in uscita](outbound-workflows.md).

## Stati vuoti

* Se non hai attività su cui intervenire, l&#39;elenco mostra un messaggio _Sei stato contattato per oggi_.
* Quando i filtri non corrispondono a nessuna attività, l’elenco segnala che nessuna attività corrisponde ai filtri.
* Quando non è selezionata alcuna attività, il pannello di lavoro richiede di selezionare un’attività per visualizzarne i dettagli.

>[!MORELIKETHIS]
>
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Prestazioni in uscita](performance.md)
>* [Potenziali clienti](prospects.md)
