---
title: Ruoli utente e autorizzazioni
description: Scopri come i gruppi di utenti di Sales Qualifier controllano l’accesso alle applicazioni e all’amministrazione.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/9X9DYGMvLGcPG--G6rHcDEk91hdT9-XYc9wbiL2Qoww'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 4%

---


# Ruoli utente e autorizzazioni

Sales Qualifier utilizza due gruppi di utenti obbligatori per separare le attività di vendita dalla configurazione a livello di organizzazione.

## Gruppi di utenti richiesti

| Gruppo | Chi appartiene | Che cosa viene concesso |
| --- | --- | --- |
| `Sales Qualifier` | Tutti gli utenti, inclusi gli amministratori | Accesso all’applicazione: Prospect, Account, Flussi di lavoro in uscita, Attività, Prestazioni e Impostazioni profilo. |
| `Sales Qualifier Admins` | Solo amministratori, oltre al gruppo `Sales Qualifier` | Accesso a **[!UICONTROL Impostazioni amministratore]**, che gestisce le connessioni CRM, il Knowledge Center e le impostazioni di conformità per l&#39;intera organizzazione. |

Per gli utenti standard è necessario solo il gruppo `Sales Qualifier`. Gli amministratori devono essere membri di entrambi i gruppi. Consulta [Inizia](getting-started.md) per creare questi gruppi.

Le organizzazioni possono anche creare un gruppo `Sales Qualifier BDR managers` facoltativo. I membri possono accedere ai rapporti sulle prestazioni delle e-mail.

## Accesso amministratore

**[!UICONTROL Impostazioni amministratore]** viene visualizzato in **[!UICONTROL Amministrazione]** solo per gli utenti che appartengono a entrambi i gruppi richiesti. Le modifiche a queste impostazioni si applicano all’intera organizzazione.

## Controllo degli amministratori

| Impostazione | Dove configurarlo | Effetto |
| --- | --- | --- |
| Connessione CRM e mappatura campi | [Integrazioni](integrations.md#map-crm-fields-inbound-mapping) | Determina quali campi CRM vengono visualizzati per un prospect o un account e quali campi sono disponibili come filtri. |
| Rinuncia e-mail globale | [Integrazioni](integrations.md#configure-global-email-opt-out) | Aggiunge un piè di pagina per l’annullamento dell’iscrizione a ogni e-mail in uscita. |
| Centro informazioni e playbook | [Centro conoscenze](knowledge-center.md) | Rende disponibile il playbook aziendale nei prompt in uscita e nella [chat AI](ai-assistant.md). |
| Sincronizzazione attività | [Integrazioni](integrations.md#configure-activity-sync-outbound-mapping) | Determina se le attività di estensione di Sales Qualifier vengono visualizzate nel CRM. |

Gli utenti standard possono utilizzare queste impostazioni ma non possono modificarle. Se manca un filtro previsto, un riferimento alla playbook o un campo di gestione delle relazioni con i clienti, contatta un amministratore.

>[!MORELIKETHIS]
>
>* [Introduzione](getting-started.md)
>* [Integrazioni](integrations.md)
>* [Centro conoscenze](knowledge-center.md)
