---
title: Crea un playbook per un Knowledge Center
description: Scopri come caricare materiale collaterale di vendita e creare un playbook nel Knowledge Center di Sales Qualifier per informare l’assistenza e il coinvolgimento di IA.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/5dpADHs-37gBKs-d1lf2rFLP-bJJQs-06kGCzhgGeRw'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 08dd05e1d13b501d43d457e6217a43aaabdb1d0d
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---


# Centro conoscenze

Il **[!UICONTROL Centro conoscenze]** consente al Account Qualification Agent (AQA) di accedere ai materiali di vendita. Sales Qualifier utilizza questi materiali per generare ricerche, approfondimenti sulle qualifiche e attività di sensibilizzazione che riflettono il modo in cui l’organizzazione vende. Solo gli amministratori possono creare e gestire la playbook.

## Carica materiale promozionale

1. Nel menu di navigazione a sinistra, espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Impostazioni amministratore]**.
1. Seleziona **[!UICONTROL Centro informazioni]** in **[!UICONTROL Integrazioni]**.
1. Imposta **[!UICONTROL Nome società]** e **[!UICONTROL URL società]** utilizzati da Sales Qualifier per eseguire ricerche nella società e bozze di e-mail.
1. Carica giochi di vendita, profili cliente ideali (ICP), guide di posizionamento e altro materiale promozionale in formato PDF, PPTX o DOCX.

In ogni documento caricato viene visualizzato il relativo stato di elaborazione, ad esempio **[!UICONTROL Pronto]**, e la data dell&#39;ultimo aggiornamento.

## Creare un playbook

Dopo aver caricato i documenti, seleziona **[!UICONTROL Genera playbook]**.

>[!NOTE]
>
>L&#39;elaborazione di un playbook può richiedere fino a 24 ore.

Quando il playbook è pronto, i rappresentanti possono utilizzarlo in due posizioni:

* **Prompt e-mail in uscita** - In un prompt punto di contatto, assegnare un nome al documento e descrivere il contesto da utilizzare. Immettere ad esempio `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. Consulta [Generare e rivedere i punti di contatto](outbound-workflows.md#step-3-generate-and-review-touchpoints).
* **Chat AI**: fare riferimento al Centro informazioni nella domanda. Immettere ad esempio `From the Knowledge Center, help me position our security solution for ABC Corp before tomorrow's call`. Vedi [Chat AI](ai-assistant.md).

In entrambi i casi, il contenuto generato riflette i messaggi nel playbook anziché la ricerca generica.

>[!MORELIKETHIS]
>
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Chat IA](ai-assistant.md)
>* [Ruoli utente e autorizzazioni](user-roles-permissions.md)
