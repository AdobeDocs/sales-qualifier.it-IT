---
title: Potenziali clienti in Sales Qualifier
description: Scopri come creare, filtrare e rivedere l’elenco dei potenziali clienti in Sales Qualifier per dare priorità all’estensione.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 08dd05e1d13b501d43d457e6217a43aaabdb1d0d
workflow-type: tm+mt
source-wordcount: 535
ht-degree: 2%

---


# Potenziali clienti

Seleziona **[!UICONTROL Potenziali]** nella barra di navigazione a sinistra per visualizzare i lead e i contatti a cui puoi accedere. Utilizza l’elenco per rivedere lo stato di ogni prospect e l’ultima attività.

![Tabella dei potenziali clienti con lo stato del lead e l&#39;ultima attività per la gestione dei potenziali clienti](./assets/prospects.png){width="800" zoomable="yes"}

* **[!UICONTROL Lead]** - Lead assegnati all&#39;utente nel CRM connesso.
* **[!UICONTROL Contatti]** - Contatti assegnati all&#39;utente nel CRM connesso.
* **[!UICONTROL Elenco persone]**—Potenziali importati o aggiunti manualmente.

## Crea il tuo elenco di potenziali clienti

L’elenco dei potenziali clienti combina persone provenienti da più origini:

* **Prospetti CRM**: Sales Qualifier importa automaticamente i lead e i contatti assegnati all&#39;utente connesso. Consulta [Integrazioni](integrations.md).
* **Prospect importati** - Prospect importati da un file CSV.
* **Potenziali aggiunti manualmente** - Singoli potenziali aggiunti in Sales Qualifier.

Per aggiungere potenziali clienti non provenienti dal CRM:

1. Nella pagina **[!UICONTROL Potenziali]**, seleziona **[!UICONTROL Elenco persone]**.
1. Seleziona **[!UICONTROL + Aggiungi persone]**, quindi seleziona **[!UICONTROL Importa CSV]** o **[!UICONTROL Aggiungi persona]**.

   * Per un&#39;importazione CSV, carica un file CSV nel formato `firstname,email`.
     È necessario specificare il nome e l’indirizzo e-mail. Il cognome è facoltativo. Il modello CSV non include la colonna ID lead CRM, ma puoi aggiungere la colonna e i relativi valori al file prima dell’importazione. Se l’importazione non riesce, controlla il messaggio di errore per individuare i campi o i valori da correggere, quindi carica di nuovo il file.
   * Per aggiungere manualmente una persona, inserisci i relativi dettagli nel modulo.

1. Seleziona **[!UICONTROL Salva]**.

## Filtrare e trovare potenziali clienti

Seleziona **[!UICONTROL Filtro]** per restringere l&#39;elenco. Puoi filtrare per:

* Stato del piano di coinvolgimento
* Creato da
* Posizione lavorativa
* Account
* Origine
* Ultimo aggiornamento

Gli amministratori possono anche rendere disponibili come filtri i campi CRM mappati. In **[!UICONTROL Impostazioni amministratore]**, attiva **[!UICONTROL Filtrabile]** per ogni campo utilizzato dai rappresentanti per trovare potenziali clienti. Vedi [Mappa campi CRM](integrations.md#map-crm-fields-inbound-mapping).

In **[!UICONTROL Contatti opportunità personali]** è inoltre possibile filtrare i contatti in base ai campi dalle opportunità associate, ad esempio area di visualizzazione, tipo e data di chiusura. I campi dell&#39;opportunità hanno etichette come **[!UICONTROL Stage (Opportunità)]**, che li distingue dai campi del contatto. L’amministratore controlla quali campi dell’opportunità sono disponibili come filtri.

### Coinvolgimento Filtra per Marketo

Trova e assegna la priorità ai potenziali clienti in base al loro coinvolgimento live [!DNL Marketo], ad esempio aperture e clic via e-mail, visite web, riempimenti di moduli e momenti interessanti. Il coinvolgimento appare quasi in tempo reale, come accade.

Per filtrare i potenziali clienti in base al coinvolgimento Marketo:

1. Seleziona **[!UICONTROL Filtro]**.
1. Aggiungi un filtro di coinvolgimento [!DNL Marketo] e imposta il tipo di attività, la campagna o altri attributi in modo che si focalizzino sul coinvolgimento rilevante.

Ogni prospect mostra la sua ultima attività [!DNL Marketo] insieme alla cronologia recente.

Il filtro del coinvolgimento Marketo è disponibile in tutte le aree di produzione. L&#39;amministratore lo attiva per l&#39;organizzazione e la sandbox e un addetto al marketing completa la configurazione una tantum in [!DNL Marketo]. Vedere [Attivare il filtro di coinvolgimento di Marketo](integrations.md#turn-on-marketo-engagement-filtering).

## Rivedi dettagli prospect

Seleziona un potenziale cliente per aprire il suo profilo. Rivedi i segnali importanti prima di contattare:

* **Riepilogo persona IA**: istantanea scritta da IA del lead o del contatto e del loro impegno recente. Utilizza il riepilogo per capire subito la persona prima di rivedere le singole attività. I riepiloghi di persone IA sono disponibili nelle istanze che eseguono Adobe Journey Optimizer B2B edition Prime o Ultimate.
* **Elenco attività**: elenco cronologico delle attività e dei comportamenti recenti.
* **Visualizzazione sequenza temporale**: sequenza temporale visiva del coinvolgimento tra i canali.
* **Contenuto visualizzato**: pagine Web e risorse visualizzate dal prospect. Selezionare un elemento per aprirlo.

>[!MORELIKETHIS]
>
>* [Account](accounts.md)
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Chat IA](ai-assistant.md)
