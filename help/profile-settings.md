---
title: Configura impostazioni profilo
description: Scopri come configurare la connessione e-mail, la firma e la disponibilità del calendario nelle impostazioni del profilo di Sales Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/juP3sddkmc-nSTcTEKGWolbCwNWDgSA0yr6XK1X-w94'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 17bfe0a1ce9b289ed85af0f72ddd089b11cca875
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 3%

---


# Impostazioni profilo

Nel menu di navigazione a sinistra, espandi **[!UICONTROL Configurazione]** e seleziona **[!UICONTROL Impostazioni profilo]**. Utilizza queste impostazioni per gestire i tuoi dati personali, la connessione e-mail, il calendario e la disponibilità della chat.

![Impostazioni profilo](assets/profile-email-config.png)

## Impostazioni e-mail

Nella scheda **[!UICONTROL Impostazioni e-mail]**, configura le connessioni e-mail.

* **[!UICONTROL Connessioni e-mail]** - Selezionare Microsoft Outlook o Google e seguire la procedura di accesso. Vedere [Connetti Outlook](integrations.md#connect-outlook) per l&#39;accesso che si approva e il percorso di approvazione dell&#39;amministratore, se necessario.
* **[!UICONTROL Firma e-mail]** - Aggiungi o aggiorna la firma utilizzata nelle e-mail generate. Includi il collegamento [prenotazione riunione](outbound-workflows.md#meeting-booking) per consentire ai potenziali clienti di pianificare il tempo con te.
* **[!UICONTROL Collegamento per la prenotazione della riunione]** - Invia un invito alla riunione tramite e-mail. Accetta l’URL della riunione.

### Contesto di bozza e-mail

![Contesto e-mail](assets/profile-email-instructions.png)

Utilizza **[!UICONTROL Contesto di bozza e-mail]** per impostare il tono, la struttura e lo stile dell&#39;e-mail in modo che le e-mail siano coerenti.

Scrivere il contesto in formato normale nell&#39;area **[!UICONTROL Contesto di bozza delle e-mail]**.
Utilizzala per definire:

* Tono e voce
* Struttura e lunghezza
* Personalization e regole di saluto
* Stile oggetto
* Come vengono utilizzati i segnali di coinvolgimento
* Struttura di metriche, punti bozza e storie di clienti

Per impostazione predefinita, le bozze utilizzano un contesto in stile house, pertanto le bozze esistenti non cambiano finché non si aggiunge un contesto personalizzato.

## Configurazione calendario

Nella scheda **[!UICONTROL Configurazione calendario]**, imposta il tuo fuso orario e la tua disponibilità.

* **[!UICONTROL Connessione calendario]**—Seleziona **[!UICONTROL Connetti]** e segui il processo di accesso a Microsoft.
* **[!UICONTROL E-mail di conferma riunione]**—Definisci l&#39;oggetto e il corpo dell&#39;e-mail di conferma che un potenziale cliente riceve dopo la prenotazione di una riunione.
* **[!UICONTROL Preferenze]** - Imposta la durata predefinita della riunione e il buffer tra le riunioni.

Se si disconnette il calendario:

* I collegamenti di prenotazione attivi non funzionano più.
* Nella pagina di prenotazione viene visualizzato un messaggio di indisponibilità temporanea.
* Le impostazioni vengono mantenute quando ci si riconnette.

## Disponibilità del calendario

La disponibilità del calendario in Sales Qualifier si basa su due input:

* Calendario di lavoro connesso, ad esempio Outlook o Gmail
* Regole di disponibilità e di tempo nella **[!UICONTROL configurazione calendario]**

Sales Qualifier legge lo stato di disponibilità, non i dettagli dell&#39;evento, dal calendario connesso. Combina questo stato con le tue regole per determinare gli intervalli di tempo che i potenziali clienti possono prenotare.

Puoi configurare:

* Ore lavorative per giorno della settimana
* Blocchi multipli al giorno, ad esempio 9:00-mezzogiorno e 13:00-5:00.
* Il tuo fuso orario
* Durata riunione
* Buffer prima e dopo le riunioni
* Avviso minimo
* Finestra di prenotazione

>[!MORELIKETHIS]
>
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Integrazioni](integrations.md)
>* [Attività](tasks.md)
