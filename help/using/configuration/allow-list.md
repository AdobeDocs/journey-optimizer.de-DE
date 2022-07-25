---
title: Zulassungsliste
description: Erfahren Sie, wie Sie die Zulassungsliste verwenden.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 93%

---

# Zulassungsliste {#allow-list}

Es ist möglich, auf der [Sandbox](../administration/sandboxes.md)-Ebene eine spezielle Sicherheitsliste für den Versand zu definieren, um eine sichere Umgebung für Testzwecke zu haben.

Beispielsweise wird auf einer Nicht-Produktionsinstanz, bei der Fehler auftreten können, durch die Zulassungsliste sichergestellt, dass Sie keine unerwünschten Nachrichten an Ihre Kunden senden.

>[!NOTE]
>
>Diese Funktion ist jetzt in Produktions- und Nicht-Produktions-Sandboxes verfügbar.

Mit der Zulassungsliste können Sie einzelne E-Mail-Adressen oder Domains angeben, die die einzigen Empfänger oder Domains sind, die zum Empfang der von einer bestimmten Sandbox gesendeten E-Mails berechtigt sind. Dadurch können Sie verhindern, dass Sie in einer Testumgebung versehentlich E-Mails an echte Kundenadressen senden.

>[!CAUTION]
>
>Diese Funktion ist nur für den E-Mail-Kanal verfügbar.

## Aktivieren der Zulassungsliste {#enable-allow-list}

<!--To enable the allowed list on a non-production sandbox, you need to update the general settings using the corresponding API end point in the Message Presets Service. Using this API, you can also disable the feature at any time.

You can update the allowed list before or after enabling the feature.-->

Gehen Sie wie folgt vor, um die Zulassungsliste zu aktivieren.

1. Öffnen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Zulassungsliste]**.

   ![](assets/allow-list-access.png)

1. Klicken Sie auf **[!UICONTROL Bearbeiten]**.

   ![](assets/allow-list-edit.png)

1. Wählen Sie **[!UICONTROL Zulassungsliste aktivieren]** aus.

   ![](assets/allow-list-enable.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**. Die Zulassungsliste ist aktiviert.

   ![](assets/allow-list-enabled.png)

Die Logik der Zulassungsliste gilt, wenn die Funktion aktiviert ist **und** wenn die Zulassungsliste **nicht** leer ist. Weiterführende Informationen finden Sie in diesem [Abschnitt](#logic).

>[!NOTE]
>
>Wenn sie aktiviert ist, wird die Funktion „Zulassungsliste“ beim Ausführen von Journey-Tests, aber auch beim Testen von Nachrichten mit [Testsendungen](../design/preview.md#send-proofs) und beim Testen von Journeys unter Verwendung des [Testmodus](../building-journeys/testing-the-journey.md) berücksichtigt.

## Entitäten zur Zulassungsliste hinzufügen {#add-entities}

Um der Zulassungsliste für eine bestimmte Sandbox neue E-Mail-Adressen oder Domains hinzuzufügen, müssen Sie die Unterdrückungs-API mit dem Wert `ALLOWED` für das Attribut `listType` aufrufen. Beispiel:

![](assets/allow-list-api.png)

Sie können die Vorgänge **Hinzufügen**, **Löschen** und **GET** ausführen.

>[!NOTE]
>
>Die Zulassungsliste kann bis zu 1.000 Einträge enthalten.

Erfahren Sie mehr über API-Aufrufe in der Referenzdokumentation zu [Adobe Experience Platform-APIs](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=de){target=&quot;_blank&quot;}.

## Logik der Zulassungsliste {#logic}

Wenn die Zulassungsliste **leer** ist, wird die Logik der Zulassungsliste nicht angewendet. Das bedeutet, dass Sie E-Mails an beliebige Profile senden können, sofern sie nicht auf der [Unterdrückungsliste](../reports/suppression-list.md) stehen.

Wenn die Zulassungsliste **nicht leer** ist, wird die Logik der Zulassungsliste angewendet:

* Wenn eine Entität **nicht auf der Zulassungsliste** und nicht auf der Unterdrückungsliste steht, erhält der entsprechende Empfänger die E-Mail nicht. Der Grund lautet **[!UICONTROL Nicht erlaubt]**.

* Wenn eine Entität **auf der Zulassungsliste** und nicht auf der Unterdrückungsliste steht, kann die E-Mail an den entsprechenden Empfänger gesendet werden. Wenn sich die Entität jedoch auch auf der [Unterdrückungsliste](../reports/suppression-list.md) befindet, erhält der entsprechende Empfänger die E-Mail nicht. Der Grund lautet **[!UICONTROL Unterdrückt]**.

>[!NOTE]
>
>Die Profile mit dem Status **[!UICONTROL Nicht erlaubt]** werden beim Nachrichtenversand ausgeschlossen. Daher muss während der **Journey-Berichte** zeigt diese Profile an, als ob sie sich durch die Journey bewegt haben ([Segment lesen](../building-journeys/read-segment.md) und [Nachrichtenaktivitäten](../building-journeys/journeys-message.md)), die **E-Mail-Berichte** werden sie nicht in die **[!UICONTROL Gesendet]** Metriken, da sie vor dem E-Mail-Versand herausgefiltert werden.
>
>Erfahren Sie mehr über den [Live-Bericht](../reports/live-report.md) und den [globalen Bericht](../reports/global-report.md).

## Ausschlussberichte {#reporting}

Wenn diese Funktion in einer Nicht-Produktions-Sandbox aktiviert ist, können Sie vom Versand ausgeschlossene E-Mail-Adressen oder Domains abrufen, die sich nicht auf der Zulassungsliste befanden. Dazu können Sie den [Abfrage-Service von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=de){target=&quot;_blank&quot;} verwenden, um die unten stehenden API-Aufrufe durchzuführen.

Verwenden Sie die folgende Abfrage, um die **Anzahl der E-Mails** abzurufen, die nicht gesendet wurden, weil die Empfänger nicht auf der Zulassungsliste waren:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Verwenden Sie die folgende Abfrage, um die **Liste der E-Mail-Adressen** abzurufen, die nicht gesendet wurden, weil die Empfänger nicht auf der Zulassungsliste waren:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
