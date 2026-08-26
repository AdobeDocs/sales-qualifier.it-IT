---
title: Impostare gli elementi di rilievo del marketing
description: Scopri come collegare Marketo a Sales Qualifier in modo che i rappresentanti possano visualizzare e filtrare i potenziali clienti in base alle attività live di Marketo in Dati salienti sul marketing.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 686
ht-degree: 3%

---


# Configurare gli elementi di rilievo del marketing

Gli elementi di rilievo marketing mostrano l&#39;attività [!DNL Marketo] di ogni prospect in tempo reale, ad esempio aperture e clic via e-mail, visite Web e riempimenti di moduli, nella scheda **[!UICONTROL Elementi di rilievo marketing]** di un prospect in Sales Qualifier. Questo articolo spiega come connettere la tua istanza di [!DNL Marketo] in modo che l&#39;attività entri.

>[!IMPORTANT]
>
>Per completare questa installazione è necessario accedere a Adobe Developer Console e a **[!UICONTROL Admin]** in [!DNL Marketo]. Rivolgiti al tuo contatto Adobe e all&#39;amministratore [!DNL Marketo] per completare le quattro parti seguenti.

La configurazione è costituita da quattro parti:

* Parte A: creare le credenziali API in Adobe Developer Console.
* Parte B: raccogliere l’endpoint Sales Qualifier e i relativi identificatori.
* Parte C: configurare un webhook in [!DNL Marketo Engage].
* Parte D: aggiungi il webhook a un trigger Smart Campaign.

Al termine dell&#39;installazione, gli utenti visualizzano e filtrano questa attività in base a **[!UICONTROL Potenziali clienti]** > **[!UICONTROL Marketing Highlights]**.

## Parte A: Creare le credenziali API {#part-a-create-api-credentials}

Queste credenziali consentono a [!DNL Marketo] di eseguire l&#39;autenticazione in modo sicuro in Sales Qualifier.

Per creare le credenziali:

1. Vai a [Adobe Developer Console](https://developer.adobe.com/console/) e accedi con il tuo Adobe ID.
1. Seleziona **[!UICONTROL Crea nuovo progetto]** o apri un progetto esistente.
1. Seleziona **[!UICONTROL Modifica progetto]**, rinomina il progetto in un elemento identificabile, ad esempio `Sales Qualifier Marketing Highlights`, quindi seleziona **[!UICONTROL Salva]**.
1. Seleziona **[!UICONTROL Aggiungi API]**, seleziona **[!UICONTROL API Experience Platform]**, quindi seleziona **[!UICONTROL Avanti]**.
1. Scegli **[!UICONTROL OAuth Server-to-Server]** come tipo di autenticazione, quindi seleziona **[!UICONTROL Next]**.

   **[!UICONTROL Server-to-Server OAuth]** consente a [!DNL Marketo] di chiamare l&#39;API Sales Qualifier direttamente dal server, senza richiedere a una persona di accedere.

1. Immettere un nome di credenziali di almeno 45 caratteri, ad esempio `Sales Qualifier Marketing Highlights Creds`.
1. Selezionare il profilo prodotto da associare, quindi selezionare **[!UICONTROL Salva API configurata]**.
1. In **[!UICONTROL Credenziali connesse]**, apri le credenziali **[!UICONTROL OAuth Server-to-Server]**. Seleziona **[!UICONTROL Recupera segreto client]**, quindi copia **[!UICONTROL ID client]** e **[!UICONTROL Segreto client]**. Questi valori vengono utilizzati nella [Parte C](#part-c-configure-the-marketo-webhook).

>[!WARNING]
>
>Mantieni il segreto client privato. Considerala come una password e non inviarla tramite e-mail. Utilizza il canale sicuro approvato della tua organizzazione per condividerlo con chiunque configuri il webhook.

## Parte B: Raccogliere endpoint e identificatori {#part-b-gather-your-endpoint-and-identifiers}

Sono necessari tre valori per [Parte C](#part-c-configure-the-marketo-webhook):

* **URL endpoint**: l&#39;indirizzo del webhook Sales Qualifier della tua area geografica.
* **imsOrg ID** - Identificatore dell&#39;organizzazione nel sistema Adobe Identity Management (IMS), nel formato `{ORG_ID}@AdobeOrg`.
* **Nome sandbox** - Il nome della sandbox AEP esattamente come appare nell&#39;URL di Sales Qualifier (il valore `sname`), non il nome visualizzato nell&#39;interfaccia utente. Utilizzare il valore URL minuscolo, ad esempio `prod`, non `Prod`.

| Area geografica | URL endpoint webhook |
| --- | --- |
| America del Nord | `https://5r6xakp9k3.execute-api.us-east-1.amazonaws.com/prod/external/marketo/signals` |
| EMEA | `https://pc72i8q1k3.execute-api.eu-west-1.amazonaws.com/prod/external/marketo/signals` |
| APAC/Australia | `https://5cxxxyqlai.execute-api.ap-southeast-2.amazonaws.com/prod/external/marketo/signals` |

{style="table-layout:auto"}

Se non sei sicuro del tuo paese, ID organizzazione IMS o nome sandbox, il contatto Adobe può confermarli.

## Parte C: Configurare il webhook di Marketo {#part-c-configure-the-marketo-webhook}

Per creare il webhook:

1. In [!DNL Marketo], selezionare **[!UICONTROL Amministratore]** > **[!UICONTROL Webhook]**.
1. Seleziona **[!UICONTROL Nuovo webhook]**.
1. Imposta **[!UICONTROL URL]** sull&#39;URL dell&#39;endpoint per la tua area geografica da [Parte B](#part-b-gather-your-endpoint-and-identifiers).
1. Imposta **[!UICONTROL Tipo di richiesta]** su `POST`.
1. Imposta **[!UICONTROL codifica token richiesta]** su `JSON`. Questa impostazione è obbligatoria.
1. Incolla il modello di payload seguente in **[!UICONTROL Modello]**. Utilizza **[!UICONTROL Inserisci token]** di [!DNL Marketo] per far corrispondere i nomi dei campi nella tua istanza.

   >[!NOTE]
   >
   >Con la codifica JSON, non racchiudere i token di stringa tra virgolette. [!DNL Marketo] li aggiunge automaticamente.

   ```json
   {
     "leadId": {{lead.Id:default=0}},
     "email": {{lead.Email Address:default=}},
     "fullName": {{lead.Full Name:default=}},
     "company": {{company.Company Name:default=}},
     "title": {{lead.Job Title:default=}},
     "department": {{lead.Department:default=}},
     "country": {{lead.Country:default=}},
     "score": {{lead.Lead Score:default=0}},
     "rating": {{lead.Lead Rating:default=}},
     "leadStatus": {{lead.Lead Status:default=}},
     "leadSource": {{lead.Lead Source:default=}},
     "isCustomer": {{lead.Is Customer:default=false}},
     "industry": {{company.Industry:default=}},
     "annualRevenue": {{company.Annual Revenue:default=0}},
     "numEmployees": {{company.Num Employees:default=0}},
     "campaignId": {{campaign.id:default=0}},
     "campaignName": {{campaign.name:default=}},
     "programName": {{program.name:default=}},
     "occurredAt": {{system.dateTime:default=}},
     "munchkinId": {{system.munchkinId:default=}},
     "triggerName": {{trigger.Trigger Name:default=}},
     "crmId": {{lead.SFDC ID:default=}},
     "crmType": {{lead.SFDC Type:default=}},
     "crmOwnerEmail": {{lead.Lead Owner Email Address:default=}},
     "crmOwnerFirstName": {{lead.Lead Owner First Name:default=}},
     "crmOwnerLastName": {{lead.Lead Owner Last Name:default=}},
     "attributes": {
       "asset": {{trigger.Name:default=}},
       "link": {{trigger.Link:default=}},
       "subject": {{trigger.Subject:default=}},
       "webPage": {{trigger.Web Page:default=}},
       "category": {{trigger.Category:default=}},
       "details": {{trigger.Details:default=}},
       "sentBy": {{trigger.Sent By:default=}},
       "receivedBy": {{trigger.Received By:default=}},
       "referrer": {{trigger.Referrer:default=}},
       "searchEngine": {{trigger.Search Engine:default=}},
       "searchQuery": {{trigger.Search Query:default=}},
       "imDescription": {{lead.Last Interesting Moment Desc:default=}},
       "imType": {{lead.Last Interesting Moment Type:default=}},
       "imDate": {{lead.Last Interesting Moment Date:default=}},
       "imSource": {{lead.Last Interesting Moment Source:default=}},
       "chatAgentName": {{trigger.Agent Name:default=}},
       "chatAgentEmail": {{trigger.Agent Email:default=}},
       "chatConversationStatus": {{trigger.Conversation Status:default=}},
       "chatConversationSummary": {{trigger.Conversation Summary:default=}},
       "chatGoalName": {{trigger.Goal name:default=}},
       "chatMeetingStatus": {{trigger.meeting status:default=}},
       "chatScheduledFor": {{trigger.Scheduled For:default=}},
       "chatDocumentName": {{trigger.Document Name:default=}},
       "chatDocumentUrl": {{trigger.Document URL:default=}},
       "chatPageUrl": {{trigger.Page URL:default=}}
     }
   }
   ```

1. Seleziona **[!UICONTROL Azioni webhook]** > **[!UICONTROL Imposta intestazione personalizzata]**, quindi aggiungi le intestazioni seguenti, utilizzando i valori di [Parte A](#part-a-create-api-credentials) e [Parte B](#part-b-gather-your-endpoint-and-identifiers):

   | Intestazione | Valore |
   | --- | --- |
   | `Content-Type` | `application/json` |
   | `x-client-id` | ID client |
   | `x-client-secret` | Segreto client |
   | `x-gw-ims-org-id` | ID della tua organizzazione IMS |
   | `x-sandbox-name` | Nome della sandbox |

   {style="table-layout:auto"}

1. Seleziona **[!UICONTROL Salva]**.

## Parte D: Aggiungere il webhook a un trigger Smart Campaign {#part-d-add-the-webhook-to-a-trigger-smart-campaign}

Aggiungi un passaggio di flusso **[!UICONTROL Chiama webhook]** a un trigger di Smart Campaign, esistente o nuovo. I trigger dell’elenco avanzato per tale campagna determinano le attività da inviare a Sales Qualifier.

Per aggiungere il webhook:

1. Apri una campagna avanzata attivatore esistente o creane una nuova (**[!UICONTROL Attività di marketing]** > **[!UICONTROL Nuove]** > **[!UICONTROL Campagna avanzata]**).
1. Nella scheda **[!UICONTROL Elenco avanzato]**, aggiungi il trigger o i trigger per le attività che desideri inviare, ad esempio **[!UICONTROL Clic sul collegamento nell&#39;e-mail]**, **[!UICONTROL Compila modulo]** o **[!UICONTROL Pagina Web visite]**.
1. Nella scheda **[!UICONTROL Flusso]**, aggiungi un passaggio **[!UICONTROL Chiama webhook]** e seleziona il webhook creato in [Parte C](#part-c-configure-the-marketo-webhook).
1. Attiva la campagna avanzata.

L’attività di tale campagna avanzata ora scorre in Sales Qualifier. I rappresentanti visualizzano e filtrano questa attività per **[!UICONTROL Potenziali]** > **[!UICONTROL Elementi di rilievo marketing]**.

>[!MORELIKETHIS]
>
>* [Gestione integrazioni](integrations.md)
>* [Potenziali clienti](prospects.md)
>* [Introduzione](getting-started.md)
