---
title: Potenziali clienti in Sales Qualifier
description: Scopri come creare l’elenco di potenziali clienti da origini CRM, importate e aggiunte manualmente, filtrare i potenziali clienti ed esaminare i dettagli in Sales Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: c7f4e1b7adc4b3420ea5f16c3b426c40bb300d45
workflow-type: tm+mt
source-wordcount: 698
ht-degree: 1%

---


# Potenziali clienti

Seleziona **[!UICONTROL Potenziali]** nella barra di navigazione a sinistra per visualizzare i lead e i contatti a cui puoi accedere. Utilizza l’elenco per rivedere lo stato di ogni prospect e l’ultima attività.

![Tabella dei potenziali clienti con lo stato del lead e l&#39;ultima attività per la gestione dei potenziali clienti](./assets/prospects.png){width="800" zoomable="yes"}

* **[!UICONTROL Lead]** - Lead assegnati all&#39;utente nel CRM connesso.
* **[!UICONTROL Contatti]** - Contatti assegnati all&#39;utente nel CRM connesso.
* **[!UICONTROL Elementi di rilievo marketing]** - Potenziali clienti con attività Marketo live, ad esempio aperture di e-mail o clic.
* **[!UICONTROL Elenco persone]**—Potenziali importati o aggiunti manualmente.

## Crea il tuo elenco di potenziali clienti

L’elenco dei potenziali clienti combina persone provenienti da più origini:

* **Prospetti CRM**: Sales Qualifier importa automaticamente i lead e i contatti assegnati all&#39;utente connesso. Consulta [Integrazioni](integrations.md).
* **Prospect importati** - Prospect importati da un file CSV.
* **Potenziali aggiunti manualmente** - Singoli potenziali aggiunti in Sales Qualifier.

Per aggiungere potenziali clienti non provenienti dal CRM:

1. Nella pagina **[!UICONTROL Potenziali]**, seleziona **[!UICONTROL Elenco persone]**.

   ![Elenco persone](assets/prospects-people-list.png){width="800" zoomable="yes"}

1. Seleziona **[!UICONTROL + Aggiungi persone]**, quindi seleziona **[!UICONTROL Importa CSV]** o **[!UICONTROL Aggiungi persona]**.

   * Per un&#39;importazione CSV, carica un file CSV nel formato `firstname,email`.
     È necessario specificare il nome e l’indirizzo e-mail. Il cognome è facoltativo. Il modello CSV non include la colonna ID lead CRM, ma puoi aggiungere la colonna e i relativi valori al file prima dell’importazione. Se l’importazione non riesce, controlla il messaggio di errore per individuare i campi o i valori da correggere, quindi carica di nuovo il file.
     Mappa qualsiasi campo CSV personalizzato o aggiuntivo, non solo quelli standard. Sales Qualifier salva questi valori in ogni prospect e li rende disponibili in un secondo momento, anche per la [generazione e-mail](outbound-workflows.md#step-5-add-prospects-and-start-email-generation).
   * Per aggiungere manualmente una persona, inserisci i relativi dettagli nel modulo.

1. Seleziona **[!UICONTROL Salva]**.

## Filtrare e trovare potenziali clienti

Seleziona **[!UICONTROL Filtro]** per restringere l&#39;elenco. Puoi filtrare per:

* Stato del flusso di lavoro in uscita
* Creato da
* Posizione lavorativa
* Account
* Origine
* Ultimo aggiornamento

Gli amministratori possono anche rendere disponibili come filtri i campi CRM mappati. In **[!UICONTROL Impostazioni amministratore]**, attiva **[!UICONTROL Filtrabile]** per ogni campo utilizzato dai rappresentanti per trovare potenziali clienti. Vedi [Mappa campi CRM](integrations.md#map-crm-fields-inbound-mapping).

In **[!UICONTROL Contatti opportunità personali]** è inoltre possibile filtrare i contatti in base ai campi dalle opportunità associate, ad esempio area di visualizzazione, tipo e data di chiusura. I campi dell&#39;opportunità hanno etichette come **[!UICONTROL Stage (Opportunità)]**, che li distingue dai campi del contatto. L’amministratore controlla quali campi dell’opportunità sono disponibili come filtri.

### Filtra per elementi di rilievo sul marketing

Trova e assegna la priorità ai potenziali clienti in base al loro coinvolgimento live [!DNL Marketo], ad esempio aperture e clic via e-mail, visite web, riempimenti di moduli e momenti interessanti. Il coinvolgimento appare quasi in tempo reale, come accade.

Per filtrare i potenziali clienti in base alle caratteristiche di marketing:

1. Seleziona **[!UICONTROL Filtro]**.
1. Aggiungi un filtro Marketing Highlights e imposta il tipo di attività, la campagna o altri attributi per concentrarti sul coinvolgimento che conta.

Ogni prospect mostra la sua ultima attività [!DNL Marketo] insieme alla cronologia recente.

Marketing Highlights è disponibile in tutte le aree geografiche di produzione. Un amministratore completa una configurazione una tantum che connette [!DNL Marketo] a Sales Qualifier. Consulta [Configurare le caratteristiche di marketing](integrations.md#turn-on-marketo-engagement-filtering).

## Rivedi dettagli prospect

Seleziona un potenziale cliente per aprire il suo profilo. Rivedi i segnali importanti prima di contattare:

* **Riepilogo persona IA**: istantanea scritta da IA del lead o del contatto e del loro impegno recente. Utilizza il riepilogo per capire subito la persona prima di rivedere le singole attività. I riepiloghi di persone IA sono disponibili nelle istanze che eseguono Adobe Journey Optimizer B2B edition Prime o Ultimate.
* **Elenco attività**: elenco cronologico delle attività e dei comportamenti recenti.
* **Visualizzazione sequenza temporale**: sequenza temporale visiva del coinvolgimento tra i canali.
* **Contenuto visualizzato**: pagine Web e risorse visualizzate dal prospect. Selezionare un elemento per aprirlo.

### Genera preparazione riunione

Oltre al riepilogo permanente della persona di intelligenza artificiale, puoi generare una preparazione della riunione personalizzata per una chiamata specifica in arrivo dalla scheda **[!UICONTROL Ricerca riunione]**, accanto a **[!UICONTROL Ricerca account]**.

* **Basato su obiettivo** - Se il prospect è iscritto a un flusso di lavoro in uscita in esecuzione, selezionarlo. La preparazione è allineata all’obiettivo del flusso di lavoro in uscita, ad esempio la prenotazione di una riunione, un lancio di prodotto, un invito a un evento o il coinvolgimento del potenziale cliente.
* **Prompt personalizzato**: immettere gli elementi per cui si desidera prepararsi, ad esempio `Focus on renewal risk` o `Prepare for a technical deep dive with their IT lead`. La preparazione corrisponde al prompt. L’opzione di richiesta personalizzata è disponibile ogni volta che il prospect non si trova in un flusso di lavoro in uscita in esecuzione.

>[!MORELIKETHIS]
>
>* [Account](accounts.md)
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Chat IA](ai-assistant.md)
