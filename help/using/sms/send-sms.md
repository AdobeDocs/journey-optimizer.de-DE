---
solution: Journey Optimizer
product: journey optimizer
title: Anzeigen einer Vorschau der SMS-Nachricht
description: Erfahren Sie, wie Sie eine Vorschau Ihrer SMS-Nachricht in Journey Optimizer anzeigen und einen Testversand durchführen.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: ht
source-wordcount: '277'
ht-degree: 100%

---

# Senden einer SMS-Nachricht {#send-sms}

## Anzeigen einer Vorschau der SMS-Nachricht {#preview-sms}

Sobald der Inhalt der Nachricht erstellt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie personalisierte Inhalte eingefügt haben, können Sie überprüfen, wie diese Inhalte in der Nachricht angezeigt werden, indem Sie Testprofildaten verwenden.

1. Klicken Sie auf **[!UICONTROL Inhalt simulieren]**.

1. Klicken Sie auf **[!UICONTROL Testprofile verwalten]**, um ein Testprofil hinzuzufügen.

1. Suchen Sie Ihr Testprofil mit den Feldern **[!UICONTROL Identity-Namespace]** und **[!UICONTROL Identitätswert]**. Klicken Sie anschließend auf **[!UICONTROL Profil hinzufügen]**.

   ![](assets/sms_preview_3.png)

1. Nachdem Sie Ihr Testprofil ausgewählt haben, können Sie das Fenster **[!UICONTROL Testprofil hinzufügen]** schließen.

   ![](assets/sms_preview_1.png)

1. Im Fenster „Vorschau und Testen“ werden im Nachrichteninhalt Testprofildaten verwendet.

   Beispielsweise sind für diese SMS-Nachricht beide Nachrichteninhalte personalisiert:

   ![](assets/sms_preview_2.png)

## Validieren Ihrer SMS{#sms-preview}

>[!NOTE]
>
> Zur besseren Zustellbarkeit sollte stets die Telefonnummern in den vom Provider unterstützten Formaten verwendet werden. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

Sie müssen auch Warnhinweise im oberen Bereich des Editors überprüfen.  Einige davon sind einfache Warnhinweise, andere können die Verwendung der Nachricht verhindern. Es können zwei Arten von Warnhinweisen auftreten:

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. Beispielsweise wird eine Meldung angezeigt, wenn Ihre SMS-Nachricht leer ist.

* **Fehler** verhindern, dass Sie die Journey testen oder aktivieren, solange nicht alle Fehler behoben sind. Beispielsweise wird eine Meldung angezeigt, dass die Betreffzeile fehlt.

![](assets/sms-alert-button.png)

Wenn Ihre SMS-Nachricht fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md), um sie zu versenden.

**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](sms-configuration.md)
* [SMS-Bericht](../reports/journey-global-report.md#sms-global)
* [Erstellen einer SMS-Nachricht](create-sms.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
