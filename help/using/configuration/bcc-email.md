---
title: BCC-E-Mail verwenden
description: Erfahren Sie, wie Sie E-Mail-Einstellungen auf der Ebene der Nachrichtenvoreinstellung konfigurieren.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 169ad138ea27b9049698d8d3bfa8a0817ed39fee
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 84%

---

# BCC-E-Mail verwenden {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Definieren einer BCC-E-Mail-Adresse"
>abstract="Sie können eine Kopie der gesendeten E-Mails aufbewahren, indem Sie sie an einen BCC-Posteingang senden. Geben Sie die E-Mail-Adresse Ihrer Wahl ein, sodass jede gesendete E-Mail blind an diese BCC-Adresse gesendet wird. Diese Funktion ist optional."

Sie können eine identische Kopie (oder Blindkopie) einer von [!DNL Journey Optimizer] gesendeten E-Mail an einen BCC-Posteingang senden. Mit dieser optionalen Funktion können Sie Kopien der E-Mail-Nachrichten speichern, die Sie Ihren Benutzern zur Einhaltung der Vorschriften und/oder zu Zwecken der Archivierung senden. Dies ist für die Versandempfänger unsichtbar.

## Aktivieren von BCC-E-Mails {#enable-bcc}

Um die Option **[!UICONTROL BCC-E-Mail]** zu aktivieren, geben Sie die E-Mail-Adresse Ihrer Wahl in das entsprechende Feld ein. Sie können eine beliebige externe Adresse im korrekten Format angeben, mit Ausnahme einer E-Mail-Adresse, die in der zugewiesenen Subdomain definiert ist. Wenn die zugewiesene Subdomain beispielsweise *marketing.luma.com* lautet, ist jede Adresse wie *abc@marketing.luma.com* verboten.

>[!NOTE]
>
>Sie können nur eine BCC-E-Mail-Adresse definieren. Stellen Sie sicher, dass die BCC-Adresse über genügend Aufnahmekapazität verfügt, um alle E-Mails zu speichern, die mit der aktuellen Voreinstellung gesendet werden.
>
>Weitere Empfehlungen finden Sie unter [diesem Abschnitt](#bcc-recommendations-limitations).

![](assets/preset-bcc.png)

Alle E-Mail-Nachrichten, die diese Voreinstellung verwenden, werden blind an die von Ihnen eingegebene BCC-E-Mail-Adresse gesendet. Von dort aus können sie mithilfe eines externen Systems verarbeitet und archiviert werden.

>[!CAUTION]
>
>Die Nutzung der BCC-Funktion wird auf die Anzahl der Nachrichten angerechnet, für die Sie lizenziert sind. Aktivieren Sie sie daher nur für wichtige Kommunikation, die Sie archivieren möchten, in den Voreinstellungen. Prüfen Sie Ihren Vertrag auf das Lizenzvolumen.

Die Einstellung der BCC-E-Mail-Adresse wird sofort auf der Ebene der Voreinstellung gespeichert und verarbeitet. Wenn Sie mit dieser Voreinstellung eine [neue Nachricht erstellen](../messages/get-started-content.md#create-new-message), wird die BCC-E-Mail-Adresse automatisch angezeigt.

![](assets/preset-bcc-in-msg.png)

Die BCC-Adresse wird jedoch gemäß der folgenden Logik für den Versand von Nachrichten übernommen:

* Bei Batch- und Burst-Journeys gilt dies nicht für Batch- oder Burst-Ausführungen, die bereits begonnen hatten, bevor die BCC-Einstellung vorgenommen wurde. Die Änderung wird beim nächsten Intervall oder bei der nächsten Wiederausführung übernommen.

* Bei Transaktionsnachrichten wird die Änderung sofort für die nächste Mitteilung übernommen (bis zu einer Minute Verzögerung).

>[!NOTE]
>
>Sie müssen keine Nachricht oder Journey erneut veröffentlichen, damit die BCC-Einstellung übernommen wird.

## Empfehlungen und Einschränkungen {#bcc-recommendations-limitations}

* Um die Einhaltung der Datenschutzbestimmungen zu gewährleisten, müssen BCC-E-Mails von einem Archivierungssystem verarbeitet werden, in dem personenbezogene Daten (PII) sicher gespeichert werden können.

* Da Nachrichten vertrauliche oder private Daten enthalten können, z. B. personenbezogene Daten (PII), müssen Sie sicherstellen, dass die BCC-Adresse korrekt ist, und den Zugriff auf Nachrichten sicherstellen.

* Ihr Posteingang, der für BCC verwendet wird, sollte in Bezug auf Speicherplatz und Versand ordnungsgemäß verwaltet werden. Wenn der Posteingang Bounces zurückgibt, werden manche E-Mails möglicherweise nicht empfangen und daher nicht archiviert.

* Nachrichten können vor den Zielempfängern an die BCC-E-Mail-Adresse gesendet werden. BCC-Nachrichten können auch dann gesendet werden, wenn die ursprünglichen Nachrichten [bounced](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Öffnen oder klicken Sie nicht durch die an die BCC-Adresse gesendeten E-Mails, da sie in der Gesamtzahl der Öffnungen und Klicks aus der Versandanalyse berücksichtigt werden. Dies könnte zu falschen Berechnungen in [Berichte](../reports/message-monitoring.md).

* Markieren Sie keine Nachrichten im BCC-Posteingang als Spam, da sich dies auf alle anderen an diese Adresse gesendeten E-Mails auswirkt.


>[!CAUTION]
>
>Klicken Sie nicht auf den Abmelde-Link in den an die BCC-Adresse gesendeten E-Mails, da Sie die entsprechenden Empfänger sofort abmelden werden.

## DSGVO-Konformität {#gdpr-compliance}

Vorschriften wie die DSGVO besagen, dass die betroffenen Personen ihr Einverständnis jederzeit ändern können. Da die mit Journey Optimizer gesendeten BCC-E-Mails auf sichere Weise personenbezogene Daten enthalten, müssen Sie das **[!UICONTROL CJM E-Mail-BCC-Feedback-Ereignisschema]** bearbeiten, um diese personenbezogenen Daten unter Einhaltung der DSGVO und ähnlicher Vorschriften verwalten zu können.

Gehen Sie dazu wie folgt vor.

1. Gehen Sie zu **[!UICONTROL Daten-Management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Durchsuchen]** und wählen Sie **[!UICONTROL CJM E-Mail-BCC-Feedback-Ereignisschema]** aus.

   ![](assets/preset-bcc-schema.png)

1. Klicken Sie auf **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagement]** und dann auf **[!UICONTROL secondaryRecipientDetail]**, um die Struktur zu erweitern.

1. Wählen Sie **[!UICONTROL originalRecipientAddress]** aus.

1. In den **[!UICONTROL Feldeigenschaften]** rechts scrollen Sie nach unten zum Kontrollkästchen **[!UICONTROL Identität]**.

1. Markieren Sie es und wählen Sie auch **[!UICONTROL Primäre Identität]** aus.

1. Wählen Sie einen Namespace aus der Dropdown-Liste aus.

   ![](assets/preset-bcc-schema-identity.png)

1. Klicken Sie auf **[!UICONTROL Übernehmen]**.

>[!NOTE]
>
>Weitere Informationen zur Verwaltung der Datenschutzeinstellungen und den geltenden Vorschriften finden Sie in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de){target=&quot;_blank&quot;}.

## BCC-Berichtsdaten {#bcc-reporting}

Das Reporting über BCC als solches ist in den Journey- und Nachrichtenberichten nicht verfügbar. Informationen werden jedoch in einem Systemdatensatz mit dem Namen **[!UICONTROL Datensatz mit AJO BCC-Feedback-Ereignissen]** gespeichert. Sie können Abfragen für diesen Datensatz ausführen, um beispielsweise nützliche Informationen zu Debugging-Zwecken zu finden.

Sie können über die Benutzeroberfläche auf diesen Datensatz zugreifen. Wählen Sie **[!UICONTROL Daten-Management]** > **[!UICONTROL Datensätze]** > **[!UICONTROL Durchsuchen]** aus und aktivieren Sie den Umschalter **[!UICONTROL Anzeigen von Systemdatensätzen]** aus dem Filter, um die systemgenerierten Datensätze anzuzeigen. In [diesem Abschnitt](../start/get-started-datasets.md#access-datasets) erfahren Sie mehr über den Zugriff auf Datensätze.

![](assets/preset-bcc-dataset.png)

Um Abfragen für diesen Datensatz auszuführen, können Sie den Abfrage-Editor verwenden, der vom [Adobe Experience Platform Abfrage-Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=de){target=&quot;_blank&quot;} bereitgestellt wird. Um darauf zuzugreifen, wählen Sie **[!UICONTROL Daten-Management]** > **[!UICONTROL Abfragen]** und klicken Sie auf **[!UICONTROL Abfrage erstellen]**. [Weitere Informationen](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Je nach gesuchten Informationen können Sie die folgenden Abfragen ausführen.

1. Für alle anderen Abfragen unten benötigen Sie die Journey-Aktions-ID. Führen Sie diese Abfrage aus, um alle innerhalb der letzten 2 Tage mit einer bestimmten Journey-Versions-ID verknüpften Aktions-IDs abzurufen:

       ```
       SELECT
       DISTINCT
       CAST(TIMESTAMP AS DATE) AS EventTime,
       _experience.journeyOrchestration.stepEvents.journeyVersionID,
       _experience.journeyOrchestration.stepEvents.actionName,
       _experience.journeyOrchestration.stepEvents.actionID
       FROM journey_step_events
       WHERE
       _experience.journeyOrchestration.stepEvents.journeyVersionID = &#39;&lt;journey version id>&#39; AND
       _experience.journeyOrchestration.stepEvents.actionID is not NULL AND
       TIMESTAMP > NOW() - INTERVAL &#39;2&#39; DAY
       ORDER BY EventTime DESC;
       ```
   
   >[!NOTE]
   >
   >Um den `<journey version id>`-Parameter abzurufen, wählen Sie die entsprechende [Journey-Version](../building-journeys/journey-versions.md) aus dem Menü **[!UICONTROL Journey-Management]** > **[!UICONTROL Journeys]**. Die Journey-Versions-ID wird am Ende der URL angezeigt, die in Ihrem Webbrowser angezeigt wird.
   >
   >![](assets/preset-bcc-action-id.png)

1. Führen Sie diese Abfrage aus, um alle Nachrichten-Feedback-Ereignisse (insbesondere den Feedback-Status) abzurufen, die in den letzten 2 Tagen für eine bestimmte Nachricht, die an einen bestimmten Benutzer gesendet wurde, generiert wurden:

       ```
       SELECT
       _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
       _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID,
       timestamp AS EventTime,
       _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
       _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
       CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       WHEN &#39;sent&#39; THEN &#39;Sent&#39;
       WHEN &#39;delay&#39; THEN &#39;Retry&#39;
       WHEN &#39;out_of_band&#39; THEN &#39;Bounce&#39;
       WHEN &#39;bounce&#39; THEN &#39;Bounce&#39;
       END AS FeedbackStatusCategory
       FROM cjm_message_feedback_event_dataset
       WHERE
       timestamp > now() - INTERVAL &#39;2&#39; day  AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = &#39;&lt;journey version id>&#39; AND
       _experience.customerJourneyManagement.messageExecution.journeyActionID = &#39;&lt;journey action id>&#39; AND
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email address>&#39;
       ORDER BY EventTime DESC;
       ```
   
   >[!NOTE]
   >
   >Um den `<journey action id>`-Parameter abzurufen, führen Sie die erste oben beschriebene Abfrage mit der Journey-Versions-ID aus. Der `<recipient email address>`-Parameter ist die E-Mail-Adresse des Zielkontakts oder des tatsächlichen Empfängers.

1. Führen Sie diese Abfrage aus, um alle BCC-Nachrichten-Feedback-Ereignisse abzurufen, die für eine bestimmte Nachricht, die innerhalb der letzten 2 Tage an einen bestimmten Benutzer gesendet wurde, generiert wurden:

   ```
   SELECT   
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
               WHEN 'sent' THEN 'Sent'
               WHEN 'delay' THEN 'Retry'
               WHEN 'out_of_band' THEN 'Bounce' 
               WHEN 'bounce' THEN 'Bounce'
           END AS FeedbackStatusCategory 
   FROM ajo_bcc_feedback_event_dataset  
   WHERE  
   timestamp > now() - INTERVAL '2' day  AND
   _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
   ORDER BY EventTime DESC;
   ```

1. Führen Sie diese Abfrage aus, um alle Empfängeradressen abzurufen, die die Nachricht nicht erhalten haben, obwohl ihr BCC-Eintrag innerhalb der letzten 30 Tage existierte:

   ```
   SELECT
       DISTINCT 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
   FROM ajo_bcc_feedback_event_dataset bcc
   LEFT JOIN cjm_message_feedback_event_dataset mfe
   ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
           mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
   WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
   ```
