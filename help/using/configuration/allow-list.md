---
solution: Journey Optimizer
product: journey optimizer
title: Zulassungsliste
description: Erfahren Sie, wie Sie die Zulassungsliste verwenden
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: Zulassungsliste, Liste, sicher, Konfiguration
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: ht
source-wordcount: '1129'
ht-degree: 100%

---

# Zulassungsliste {#allow-list}

Es ist möglich, auf [Sandbox](../administration/sandboxes.md)-Ebene eine spezifische Liste für sicheren Versand zu definieren.

Mit der Zulassungsliste können einzelne E-Mail-Adressen oder Domains angegeben werden, die die einzigen Empfänger oder Domains sind, die zum Empfang der von einer bestimmten Sandbox gesendeten E-Mails berechtigt sind.

>[!NOTE]
>
>Diese Funktion ist jetzt sowohl in Produktions-Sandboxes als auch Nicht-Produktions-Sandboxes verfügbar.

Auf einer produktionsfremden Instanz, bei der Fehler auftreten können, stellt die Zulassungsliste beispielsweise sicher, dass kein Risiko besteht, dass unerwünschte Nachrichten an reale Kundenadressen gesendet werden; dies ist daher eine sichere Umgebung für Testzwecke.

Wenn die Zulassungsliste aktiv, aber leer ist, wird keine E-Mail gesendet. Wenn Sie also auf ein großes Problem stoßen, können Sie diese Funktion verwenden, um alle von [!DNL Journey Optimizer] ausgehenden Nachrichten zu stoppen, bis Sie das Problem behoben haben. Erfahren Sie mehr über die [Logik der Zulassungsliste](#logic).

>[!CAUTION]
>
>Diese Funktion ist nur für den E-Mail-Kanal verfügbar.

## Zugriff auf die Zulassungsliste {#access-allowed-list}

Um auf die detaillierte Liste der zugelassenen E-Mail-Adressen und Domains zuzugreifen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** und klicken Sie auf **[!UICONTROL Zulassungsliste]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>Die Berechtigungen zum Anzeigen, Exportieren und Verwalten der Zulassungsliste sind auf [Journey-Administratoren](../administration/ootb-product-profiles.md#journey-administrator) beschränkt. Weitere Informationen zur Verwaltung der Zugriffsberechtigungen für [!DNL Journey Optimizer]-Benutzende finden Sie in [diesem Abschnitt](../administration/permissions-overview.md).

Um die Zulassungsliste als CSV-Datei zu exportieren, klicken Sie auf den Button **[!UICONTROL CSV herunterladen]**.

Verwenden Sie den Button **[!UICONTROL Löschen]**, um einen Eintrag dauerhaft zu entfernen.

Sie können nach E-Mail-Adressen oder Domains suchen und nach dem **[!UICONTROL Adresstyp]** filtern. Nach der Auswahl können Sie den oben in der Liste angezeigten Filter löschen.

![](assets/allowed-list-filtering-example.png)

## Aktivieren der Zulassungsliste {#enable-allow-list}

Gehen Sie wie folgt vor, um die Zulassungsliste zu aktivieren.

1. Öffnen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Zulassungsliste]**.

1. Wählen Sie den Umschalter aus.

   ![](assets/allow-list-edit.png)

1. Wählen Sie **[!UICONTROL Zulassungsliste aktivieren]** aus. Die Zulassungsliste ist jetzt aktiv.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >Nachdem Sie die Zulassungsliste aktiviert haben, ist sie in Ihren Journeys und Kampagnen nach einer Latenz von 5 Minuten aktiv.

Die Logik der Zulassungsliste wird angewendet, wenn die Funktion aktiviert ist. Weiterführende Informationen finden Sie in [diesem Abschnitt](#logic).

>[!NOTE]
>
>Wenn sie aktiviert ist, wird die Funktion „Zulassungsliste“ beim Ausführen von Journeys, aber auch beim Testen von Nachrichten mit [Testsendungen](../email/preview.md#send-proofs) und beim Testen von Journeys unter Verwendung des [Testmodus](../building-journeys/testing-the-journey.md) berücksichtigt.

## Deaktivieren der Zulassungsliste {#deactivate-allow-list}

Gehen Sie wie folgt vor, um die Zulassungsliste zu deaktivieren.

1. Öffnen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Zulassungsliste]**.

1. Wählen Sie den Umschalter aus.

   ![](assets/allow-list-edit-active.png)

1. Wählen Sie die Option **[!UICONTROL Zulassungsliste deaktivieren]** aus. Die Zulassungsliste ist nicht mehr aktiv.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >Nach der Deaktivierung der Zulassungsliste gibt es eine 5-minütige Latenzzeit, bis dies in Ihren Journeys und Kampagnen wirksam wird.

Die Logik der Zulassungsliste gilt nicht, wenn die Funktion deaktiviert ist. Weiterführende Informationen finden Sie in [diesem Abschnitt](#logic).

## Entitäten zur Zulassungsliste hinzufügen {#add-entities}

Um der Zulassungsliste für eine bestimmte Sandbox neue E-Mail-Adressen oder Domains hinzuzufügen, können Sie entweder [die Liste manuell vervollständigen](#manually-populate-list) oder einen [API-Aufruf](#api-call-allowed-list) verwenden.

>[!NOTE]
>
>Die Zulassungsliste kann bis zu 1.000 Einträge enthalten.

### Manuelles Vervollständigen der Zulassungsliste {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="Hinzufügen von E-Mail-Adressen/Domains zur Zulassungsliste"
>abstract="Sie können der Zulassungsliste manuell neue E-Mail-Adressen oder Domains hinzufügen, indem Sie sie einzeln auswählen."

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="Hinzufügen von E-Mail-Adressen/Domains zur Zulassungsliste"
>abstract="Sie können der Zulassungsliste manuell neue E-Mail-Adressen oder Domains hinzufügen, indem Sie sie einzeln auswählen."

Sie können die [!DNL Journey Optimizer]-Zulassungsliste durch Hinzufügen einer E-Mail-Adresse oder einer Domain über die Benutzeroberfläche vervollständigen.

>[!NOTE]
>
>Sie können jeweils nur eine einzelne E-Mail-Adresse oder Domain hinzufügen.

Gehen Sie dazu wie folgt vor.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL E-Mail-Adresse oder Domain hinzufügen]**.

   ![](assets/allowed-list-add-email.png)

1. Wählen Sie den Adresstyp aus: **[!UICONTROL E-Mail-Adresse]** oder **[!UICONTROL Domain-Adresse]**.

1. Geben Sie die E-Mail-Adresse oder Domain ein, an die Sie E-Mails senden möchten.

   >[!NOTE]
   >
   >Vergewissern Sie sich, dass Sie eine gültige E-Mail-Adresse (z. B. abc@firma.com) oder Domain (z. B. abc.firma.com) eingeben.

1. Geben Sie bei Bedarf einen Grund an.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >Alle ASCII-Zeichen zwischen 32 und 126 sind im Feld **[!UICONTROL Grund]** zulässig. Die vollständige Liste finden Sie zum Beispiel auf [dieser Seite](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"}.

1. Klicken Sie auf **[!UICONTROL Senden]**.

### Hinzufügen von Entitäten mithilfe eines API-Aufrufs {#api-call-allowed-list}

Um die Zulassungsliste zu vervollständigen, können Sie auch die Unterdrückungs-API mit dem Wert `ALLOWED` für das `listType`-Attribut aufrufen. Beispiel:

![](assets/allow-list-api.png)

Sie können die Vorgänge **Hinzufügen**, **Löschen** und **GET** ausführen.

Erfahren Sie mehr über API-Aufrufe in der Referenzdokumentation zu [Adobe Experience Platform-APIs](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=de){target="_blank"}.

## Herunterladen der Zulassungsliste {#download-allowed-list}

Führen Sie die folgenden Schritte aus, um die Zulassungsliste als CSV-Datei zu exportieren:

1. Klicken Sie auf die Schaltfläche **[!UICONTROL CSV herunterladen]**.

   ![](assets/allowed-list-download-csv.png)

1. Warten Sie, bis die Datei generiert wurde.

   ![](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >Die Dauer des Downloads hängt von der Dateigröße ab, d. h. der Anzahl der Adressen, die sich auf der Zulassungsliste befinden.
   >
   >Es kann jeweils nur eine Download-Anfrage für eine Sandbox gleichzeitig verarbeitet werden.

1. Sobald die Datei erstellt wurde, erhalten Sie eine Benachrichtigung. Klicken Sie auf das Glockensymbol oben rechts im Bildschirm, um sie anzuzeigen.

1. Klicken Sie auf die Benachrichtigung selbst, um die Datei herunterzuladen.

   ![](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >Der Link ist 24 Stunden lang gültig.

## Logik der Zulassungsliste {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="Verwalten der Zulassungsliste"
>abstract="Wenn die Zulassungsliste aktiviert ist, erhalten nur die in der Zulassungsliste enthaltenen Empfänger E-Mail-Nachrichten von dieser Sandbox. Nach der Deaktivierung erhalten alle Empfängerinnen und Empfänger eine E-Mail."

Wenn die Zulassungsliste [aktiviert](#enable-allow-list) ist, gilt die folgende Logik:

* Wenn die Zulassungsliste **leer** ist, wird keine E-Mail gesendet.

* Wenn eine Entität **auf der Zulassungsliste** und nicht auf der Unterdrückungsliste steht, wird die E-Mail an den/die entsprechenden Empfänger gesendet. Wenn sich die Entität jedoch auch auf der [Unterdrückungsliste](../reports/suppression-list.md) befindet, erhält der entsprechende Empfänger die E-Mail nicht. Der Grund lautet **[!UICONTROL Unterdrückt]**.

* Wenn eine Entität **nicht auf der Zulassungsliste** und auch nicht auf der Unterdrückungsliste steht, erhält der entsprechende Empfänger die E-Mail nicht. Der Grund lautet **[!UICONTROL Nicht zugelassen]**.

>[!NOTE]
>
>Die Profile mit dem Status **[!UICONTROL Nicht zugelassen]** werden beim Nachrichtenversand ausgeschlossen. Daher zeigen die **Journey-Berichte** zwar an, dass sich diese Profile durch die Journey bewegt haben (Aktivitäten [Segment lesen](../building-journeys/read-segment.md) und [Nachrichtenaktivitäten](../building-journeys/journeys-message.md)), sie sind aber nicht in der Metrik **[!UICONTROL Gesendet]** der **E-Mail-Berichte** enthalten, da sie vor dem E-Mail-Versand herausgefiltert werden.
>
>Erfahren Sie mehr über den [Live-Bericht](../reports/live-report.md) und den [globalen Bericht](../reports/global-report.md).

Wann die Zulassungsliste [deaktiviert](#deactivate-allow-list) ist, werden alle E-Mails, die Sie aus der aktuellen Sandbox senden, an alle Empfänger gesendet (sofern sie nicht auf der Unterdrückungsliste stehen), einschließlich der tatsächlichen Kundenadressen.

## Ausschlussberichte {#reporting}

Wenn die Zulassungsliste aktiv ist, können Sie E-Mail-Adressen oder Domains abrufen, die vom Versand ausgeschlossen wurden, weil sie sich nicht auf der Zulassungsliste befanden. Dazu können Sie den [Abfrage-Service von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=de){target="_blank"} verwenden, um die unten stehenden API-Aufrufe durchzuführen.

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
