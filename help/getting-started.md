---
title: Guida introduttiva ad Adobe Marketo Qualifier
description: Scopri come completare la configurazione amministratore una tantum per Adobe Marketo Qualifier, inclusi i gruppi di utenti e una connessione di gestione delle relazioni con i clienti, prima che il team inizi a utilizzare l’applicazione.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/-nfmFwZyZFUZhm-uQUjSyTvrORuqJgKSKnENWYtvubs'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: d967b633fcb63c64169d3e3fbf305fd2ff82236d
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 0%
---

# Guida introduttiva ad Adobe Marketo Qualifier

Dopo il provisioning di Adobe Marketo Qualifier per l&#39;organizzazione, un amministratore di sistema [!DNL Marketo] deve creare i gruppi di utenti richiesti e connettere Salesforce o Microsoft Dynamics 365.

![Home page del qualificatore Marketo](assets/homepage.png){width="800" zoomable="yes"}

## Configurare i gruppi di utenti

I gruppi di utenti in Adobe Admin Console vengono utilizzati per controllare l’accesso a Marketo Qualifier. Entrambi i gruppi devono essere creati prima che gli utenti possano accedere.

Per informazioni sulla configurazione dei gruppi, consulta la [documentazione di Adobe Admin Console](https://helpx.adobe.com/it/business/enterprise/users/users-and-groups/user-groups.html).

>[!PREREQUISITES]
>
>L’amministratore che crea i gruppi deve soddisfare entrambi i requisiti seguenti:
>
>* Essere amministratore organizzazione con accesso a **[!UICONTROL Admin Console]** dal commutatore di app Adobe.
>* Essere assegnato al prodotto Adobe Experience Platform o essere amministratore di sistema. In caso contrario, Adobe Experience Platform non viene visualizzato nell’elenco dei prodotti.

### Utenti qualificatore Marketo

Gli utenti devono appartenere al gruppo di utenti `Marketo Qualifier` per accedere all&#39;applicazione.

Questi passaggi vengono eseguiti in Adobe Admin Console.

1. Dal commutatore app, seleziona **[!UICONTROL Admin Console]**.
1. Seleziona **[!UICONTROL Utenti]** > **[!UICONTROL Gruppi di utenti]** > **[!UICONTROL Nuovo gruppo di utenti]**.
1. Immetti `Marketo Qualifier` per il nome del gruppo e seleziona **[!UICONTROL Salva]**.
1. Apri **[!UICONTROL Profili di prodotto assegnati]** e seleziona **[!UICONTROL Assegna profilo]**.
1. Seleziona **[!UICONTROL Adobe Experience Platform]**.
1. Seleziona il profilo di prodotto **[!UICONTROL Accesso predefinito a tutti i prodotti]**, seleziona **[!UICONTROL Applica]**, quindi seleziona **[!UICONTROL Salva]**.
1. Apri **[!UICONTROL Utenti]** e seleziona **[!UICONTROL Aggiungi utenti]** per aggiungere tutti coloro che hanno bisogno di accedere a Marketo Qualifier.

### Amministratori qualificatori Marketo

Gli amministratori che configurano le connessioni CRM, il [Centro informazioni](admin-settings.md#knowledge-center) e le impostazioni di rinuncia e-mail globali devono appartenere anche al gruppo di utenti `Marketo Qualifier Admins`.

1. In Adobe Admin Console, selezionare **[!UICONTROL Utenti]** > **[!UICONTROL Gruppi di utenti]** > **[!UICONTROL Nuovo gruppo di utenti]**.
1. Immetti `Marketo Qualifier Admins` per il nome del gruppo e seleziona **[!UICONTROL Salva]**.
1. Apri **[!UICONTROL Utenti]**, seleziona **[!UICONTROL Aggiungi utenti]**, quindi aggiungi gli amministratori.
1. Verificare che ogni amministratore sia anche membro del gruppo `Marketo Qualifier`.

L&#39;appartenenza a entrambi i gruppi rende **[!UICONTROL Impostazioni amministratore]** visibili in **[!UICONTROL Amministrazione]** nella barra di navigazione a sinistra. Gli utenti standard utilizzano i campi, i filtri e la playbook configurati dagli amministratori. Il piè di pagina di rinuncia configurato si applica automaticamente alle e-mail in uscita. Gli utenti standard non possono modificare queste impostazioni.

I nomi dei gruppi di utenti devono corrispondere esattamente come mostrato nei passaggi precedenti.

È inoltre possibile creare un gruppo `Marketo Qualifier BDR managers` facoltativo. I membri di questo gruppo possono accedere ai rapporti sulle prestazioni delle e-mail.

## Connetti il tuo CRM

Marketo Qualifier si connette a Salesforce o Microsoft Dynamics 365 per fornire ai BDR una visualizzazione unificata di utenti, lead, contatti, account, opportunità, mapping di proprietari e attività correlate. La connessione iniziale richiede l&#39;accesso in sola lettura a questi dati CRM. Per preparare le credenziali prima di connettere Marketo Qualifier, rivolgiti al tuo amministratore CRM. Consulta [Integrazioni](integrations.md) per i dettagli di integrazione.

>[!PREREQUISITES]
>
>Per accedere all&#39;interfaccia di amministrazione di CRM, è necessario appartenere al gruppo Adobe Admin Console `Marketo Qualifier Admins` e al gruppo `Marketo Qualifier`.

>[!BEGINTABS]

>[!TAB Salesforce]

Un amministratore di sistema Salesforce crea un’app client esterna (denominata anche app connessa) e ne configura l’utente Run-as.

>[!PREREQUISITES]
>
>Conferma che l’amministratore di Salesforce disponga delle seguenti autorizzazioni:
>
>* Personalizza applicazione
>* Visualizza configurazione e configurazione
>* Modifica tutti i dati
>* Gestione app collegate
>
>L&#39;amministratore richiede _Gestione app collegate_ per visualizzare l&#39;ID client e il segreto client.

1. In Salesforce, vai a **[!UICONTROL Configurazione]** > **[!UICONTROL Gestione app]** e seleziona **[!UICONTROL Nuova app connessa]** o **[!UICONTROL Nuova app client esterna]**.
1. Immettere il nome di un&#39;applicazione e l&#39;indirizzo e-mail del contatto amministrativo.
1. Abilita OAuth e immetti un URL di callback.

   Se la connessione non utilizza un reindirizzamento, immetti un URL valido.

1. Aggiungi i seguenti ambiti OAuth:

   * Accedi al servizio URL identità (`id`, `profile`, `email`, `address`, `phone`)
   * Gestisci dati utente tramite API (`api`)
   * Accedi a identificatori utente univoci (`openid`)

1. Abilitare il flusso di credenziali client e selezionare un utente **[!UICONTROL Esegui come]**.
1. Verificare che l&#39;utente RunAs disponga dell&#39;accesso **Read** a `Leads`, `Accounts`, `Contacts`, `Tasks`, `Events`, `Opportunity`, `OpportunityContactRoles` e `OpportunityLineItems`. Verificare inoltre che **Attività di accesso** sia abilitato.
1. Salva l’applicazione.
1. Da **[!UICONTROL App Manager]**, apri l&#39;applicazione e seleziona **[!UICONTROL Visualizza]** > **[!UICONTROL Dettagli consumatore]**.
1. Copia i seguenti valori per la connessione Marketo Qualifier:

   * Chiave consumer (ID client)
   * Segreto consumer (segreto client)
   * URL di callback
   * URL istanza Salesforce

I passaggi sono leggermente diversi da quelli qui descritti. Per ulteriori informazioni, consulta la [documentazione di Salesforce](https://help.salesforce.com/s/?language=en_US).

### Trovare l’URL dell’istanza di Salesforce

1. Accedi e annota il sottodominio _Dominio personale_ dell&#39;organizzazione dalla barra degli indirizzi del browser (il valore `{{mydomain}}`).
1. Utilizzare il modulo canonico per il qualificatore Marketo: `https://{{mydomain}}.my.salesforce.com`.

Non utilizzare un URL `lightning.force.com` come URL dell&#39;istanza.

>[!TIP]
>
>Se l&#39;interfaccia delle connessioni CRM segnala ambiti mancanti, controllare il profilo dell&#39;utente RunAs in **[!UICONTROL Autorizzazioni oggetto standard]** per l&#39;accesso **Lettura** a lead, contatti, account e opportunità. Controlla anche **[!UICONTROL Impostazioni oggetto]** in ogni set di autorizzazioni assegnato.

>[!TAB Microsoft Dynamics 365]

Un amministratore Microsoft Dynamics 365 o Azure registra un’applicazione e la aggiunge all’ambiente Dynamics.

1. In Microsoft Entra ID, seleziona **[!UICONTROL Registrazioni app]** e registra un&#39;applicazione.
1. Copia l’ID client e l’ID tenant e crea un segreto client.
1. Nel **[!UICONTROL centro di amministrazione di Power Platform]**, selezionare **[!UICONTROL Ambienti]** e aprire l&#39;ambiente Dynamics.
1. Vai a **[!UICONTROL Impostazioni]** > **[!UICONTROL Utenti + autorizzazioni]** > **[!UICONTROL Utenti dell&#39;applicazione]** e seleziona **[!UICONTROL Nuovo utente dell&#39;app]**.
1. Selezionare l&#39;applicazione Microsoft Entra registrata.
1. Assegna un ruolo di sicurezza che consenta l&#39;accesso in lettura a lead, contatti, account, opportunità e attività.

   È necessario un ruolo di sicurezza. È necessario un ruolo di sicurezza affinché l&#39;applicazione possa accedere ai dati Dynamics.

1. Raccogli l’ID client, il segreto client, l’ID tenant e l’URL dell’istanza di Dynamics. Utilizzare il modulo URL canonico `https://{{mydomain}}.crm.dynamics.com`.

>[!ENDTABS]

### Inserisci la connessione

1. Come membro di entrambi i gruppi Marketo Qualifier richiesti, accedi a Marketo Qualifier e conferma che sia selezionato l’ambiente o la sandbox corretta.
1. Nel menu di navigazione a sinistra, espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Impostazioni amministratore]**.
1. Seleziona **[!UICONTROL connessioni CRM]** in **[!UICONTROL Integrazioni]**.

   Nella pagina sono visualizzate le schede per Salesforce e Microsoft Dynamics. Una connessione inattiva mostra **[!UICONTROL Connessione]**. Una connessione configurata mostra **[!UICONTROL Connesso]** e **[!UICONTROL Gestisci]**.

   ![Credenziali Salesforce](assets/crm-salesforce-config.png){width="800" zoomable="yes"}

1. Seleziona **[!UICONTROL Connetti]** per il sistema di gestione delle relazioni con i clienti utilizzato.
1. Immetti le credenziali e l’URL dell’istanza dall’amministratore del sistema di gestione delle relazioni con i clienti.
1. Dopo una connessione riuscita, verificare che nella scheda sia visualizzato **[!UICONTROL Connesso]**.

### Importa campi CRM

Dopo aver connesso il CRM, configura il mapping in entrata per determinare quali campi del CRM vengono visualizzati nel Qualificatore Marketo. Nella scheda del sistema di gestione delle relazioni con i clienti connessa, seleziona **[!UICONTROL Gestisci]** per aprire **[!UICONTROL Mapping in entrata]**, quindi aggiungi una sezione per ogni tipo di entità di cui desideri importare i campi.

Consulta [Mappatura dei campi CRM (mappatura in entrata)](integrations.md#map-crm-fields-inbound-mapping) per i passaggi completi, incluso come rendere disponibili i campi importati come filtri.

## Passaggi successivi

>[!MORELIKETHIS]
>
>* [Potenziali clienti](prospects.md)
>* [Flussi di lavoro in uscita](outbound-workflows.md)
