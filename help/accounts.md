---
title: Account in Sales Qualifier
description: Scopri come rivedere le informazioni sull’account in Sales Qualifier, incluse ricerche sull’intelligenza artificiale, notizie recenti, opportunità e contatti principali coinvolti, per dare priorità all’estensione.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 632
ht-degree: 0%

---


# Account

La visualizzazione account combina ricerca generata dall’intelligenza artificiale, notizie recenti, opportunità aperte, valore della pipeline e contatti coinvolti. Utilizza queste informazioni per comprendere e assegnare la priorità a un account prima di contattarlo.

## Apri un account

Apri un account dal profilo di un potenziale cliente associato.

1. Seleziona **[!UICONTROL Prospect]** nella barra di navigazione a sinistra e apri un prospect. Vedi [Potenziali clienti](prospects.md).
1. Nella pagina dei dettagli del prospect, selezionare la scheda **[!UICONTROL Account]**.

Sales Qualifier identifica l’account dal record CRM del prospect. La stessa visualizzazione account è disponibile da ogni prospect associato a tale account. Se Sales Qualifier non riesce a trovare un account, nella scheda viene visualizzato _Nessun account trovato_.

>[!NOTE]
>
>Le sezioni e le metriche disponibili dipendono dal CRM in uso, dalla configurazione dell’organizzazione e dai dati dell’account. Se una sezione qui descritta non viene visualizzata, i dati o la funzione richiesti non sono configurati.

La visualizzazione account ha due schede: **[!UICONTROL Dettagli]** e **[!UICONTROL Ricerche account]**.

## Rivedi i dettagli dell’account

La scheda **[!UICONTROL Dettagli]** fornisce un&#39;istantanea dell&#39;account e della relativa pipeline.

### Panoramica dell’account

La scheda panoramica nella parte superiore della scheda identifica l’account e ne riepiloga il valore:

* Il nome e l&#39;area geografica del conto
* **Ricavi ricorrenti annuali (ARR)**: i ricavi ricorrenti annuali per tutti gli abbonamenti attivi. Selezionare **[!UICONTROL Visualizza tutto]** per esaminare ARR per prodotto nella finestra di dialogo **[!UICONTROL Ricavi ricorrenti annuali]**.
* Statistiche sui conti, inclusi i conteggi di opportunità aperte e contatti e il valore della pipeline

### Riepilogo panoramica account

Il pannello **[!UICONTROL Panoramica account]** riepiloga l&#39;account in base ai dati CRM e alla ricerca Account Qualification Agent. Se la ricerca è in corso, il pannello mostra uno stato di caricamento. Se la ricerca non è disponibile, il pannello mostra un messaggio.

### Informazioni sull’account

Utilizza i pulsanti sotto la panoramica per passare da una visualizzazione all’altra. Le visualizzazioni disponibili dipendono dal CRM e dalla configurazione:

| Visualizzazione | Cosa mostra |
| --- | --- |
| **[!UICONTROL Opportunità]** | Opportunità aperte collegate all’account, con campi chiave per ciascuna. Selezionare **[!UICONTROL Visualizza tutto]** per visualizzare l&#39;elenco completo in una tabella. I dettagli dell&#39;opportunità, quali l&#39;area di visualizzazione, il tipo e la data di chiusura, possono essere utilizzati anche per filtrare i contatti dell&#39;account in **[!UICONTROL Contatti opportunità personali]** quando un amministratore rende tali campi filtrabili. |
| **[!UICONTROL Membri principali]** | Contatti principali coinvolti dell’account, classificati per coinvolgimento. Ogni contatto mostra la propria qualifica, l’indirizzo e-mail, il punteggio di coinvolgimento e l’indicatore di urgenza. |
| **[!UICONTROL Dati intento]** | Segnali di intento di acquisto per l’account, ad esempio i prodotti e gli argomenti di ricerca dell’account. |
| **[!UICONTROL Membri team account]** | Persone assegnate all’account, con e-mail, qualifica, territorio e gruppo di prodotti. |
| **[!UICONTROL Campi CRM]** | Campi account importati dal CRM, come configurato nella mappatura in entrata. Consulta [Integrazioni](integrations.md#map-crm-fields-inbound-mapping). |

Dalla visualizzazione **[!UICONTROL Membri principali]**, eseguire una delle azioni seguenti per un contatto:

* **[!UICONTROL Aggiungi al flusso di lavoro in uscita]** - Registra il contatto in un [flusso di lavoro in uscita](outbound-workflows.md).
* **[!UICONTROL Aggiungi a Marketo campaign]** - Attiva una campagna [!DNL Marketo] per il contatto.

## Ricercare l’account

La scheda **[!UICONTROL Ricerca account]** contiene tre aree:

* **[!UICONTROL Categorie di ricerca]**—Argomenti di ricerca. Selezionare una categoria per visualizzarne la ricerca nel riquadro centrale.
* **Contenuto ricerca**: schede di ricerca generate dall&#39;intelligenza artificiale raggruppate per categoria. Una scheda può includere il dominio di origine e le date in cui il segnale è stato rilevato per la prima volta e per l’ultima volta.
* **[!UICONTROL Notizie recenti]** - Notizie aggiornate sull&#39;account, incluse date, tag e collegamenti di origine.

Se non è possibile caricare la ricerca o le notizie, ogni area offre un&#39;azione **[!UICONTROL Ricarica]** per riprovare.

## Utilizzare le informazioni sull’account in outreach

L’intelligenza dell’account è più utile quando determina ciò che invii:

* Fai riferimento a una notizia recente o a un segnale di ricerca per rendere l’apertura rilevante invece di utilizzare un pitch generico.
* Controlla le opportunità aperte e il valore della pipeline per decidere se assegnare la priorità all’account.
* Utilizza **[!UICONTROL Membri principali]** per identificare chi contattare, quindi iscriverli in un flusso di lavoro in uscita.
* Chiedi a [Chat AI](ai-assistant.md) di sviluppare il posizionamento per l&#39;account prima di una chiamata.

>[!MORELIKETHIS]
>
>* [Potenziali clienti](prospects.md)
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Chat IA](ai-assistant.md)
