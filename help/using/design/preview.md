---
solution: Journey Optimizer
product: journey optimizer
title: Nachrichtenvorschau und Testversand
description: Erfahren Sie, wie Sie Ihre Nachrichten in der Vorschau darstellen und testen können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: 9b4ab81a362c38dce5ff4b10fb301c81ed117688
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 100%

---

# Nachrichtenvorschau und Testversand{#preview-and-proof}

Sobald der Inhalt der Nachricht erstellt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie [personalisierte Inhalte](../personalization/personalize.md) eingefügt haben, können Sie überprüfen, wie diese Inhalte in der Nachricht angezeigt werden, indem Sie Testprofildaten verwenden.

Um mögliche Fehler in E-Mail-Inhalt oder bei Personalisierungseinstellungen zu erkennen, führen Sie einen Testversand an Testprofile durch. Bei jeder Änderung sollte ein Testversand durchgeführt werden, um den aktualisierten Inhalt zu validieren.

>[!CAUTION]
>
>Um Ihre Nachrichten in der Vorschau darzustellen und einen Testversand durchzuführen, benötigen Sie Testprofile.
>
>Auf [dieser Seite](../segment/creating-test-profiles.md) erfahren Sie, wie Sie Testprofile erstellen.

Zum Testen des Nachrichteninhalts sind folgende Schritte erforderlich:

* [Auswählen der Testprofile](#select-test-profiles)
* [Überprüfen der Nachrichtenvorschau](#preview-your-messages)

Anschließend können Sie den [Testversand](#send-proofs) an Ihre Testprofile starten.

Nutzen Sie außerdem Ihr **Litmus**-Konto in [!DNL Journey Optimizer], um Ihr **E-Mail-Rendering** in gängigen E-Mail-Clients zu überprüfen. Auf diese Weise stellen Sie sicher, dass Ihr E-Mail-Inhalt in jedem Posteingang ansprechend aussieht und korrekt funktioniert. In [diesem Abschnitt](#email-rendering) erfahren Sie, wie Sie die Sperre für Litmus-E-Mail-Vorschauen aufheben

>[!CAUTION]
>
>Bei der Vorschau einer Nachricht oder beim Versand von Testsendungen werden nur Profil-Personalisierungsdaten angezeigt. Personalisierung, die auf Kontextdaten wie Ereignisinformationen basiert, kann nur im Kontext einer Journey getestet werden. In [diesem Anwendungsbeispiel](../personalization/personalization-use-case.md) erfahren Sie, wie Sie die Personalisierung testen können.

➡️ [Erfahren Sie in diesem Video, wie Sie Ihre E-Mail in der Vorschau anzeigen und einen Testversand durchführen können](#video-preview).

## Auswählen der Testprofile{#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Nachrichtenvorschau und Testversand"
>abstract="Sobald der Inhalt der Nachricht erstellt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/validate/preview.html?lang=de#email-rendering" text="E-Mail-Rendering"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/validate/preview.html?lang=de#preview-your-messages" text="Vorschau"

Verwenden Sie [Testprofile](../segment/creating-test-profiles.md), um zusätzliche Empfänger anzusprechen, die nicht den definierten Zielgruppenbestimmungskriterien entsprechen.

Gehen Sie wie folgt vor, um die Testprofile auszuwählen:

1. Klicken Sie im Nachrichtenbereich oder Email Designer auf die Schaltfläche **[!UICONTROL Inhalt simulieren]**, um die Auswahl der Testprofile vorzunehmen.

   ![](assets/email-preview-button.png)

1. Wählen Sie den Namespace aus, der zur Identifizierung der Testprofile verwendet werden soll, indem Sie auf das Auswahlsymbol **[!UICONTROL Identitäts-Namespace]** klicken.

   ![](assets/previewselect-namespace.png)

   Weitere Informationen zu Identitäts-Namespaces von Adobe Experience Platform finden Sie [in diesem Abschnitt](../segment/get-started-identity.md).

   Im folgenden Beispiel verwenden wir den Namespace **E-Mail**.

1. Verwenden Sie das Suchfeld, um den Namespace zu lokalisieren, wählen Sie ihn aus und klicken Sie auf **[!UICONTROL Auswählen]**

   ![](assets/preview-email-namespace.png)

1. Geben Sie den Wert ein, um das Testprofil zu festzulegen, und klicken Sie auf **[!UICONTROL Testprofil hinzufügen]**.

   ![](assets/preview-identity-value.png)

1. Wenn Sie Ihrer Nachricht personalisierten Inhalt hinzugefügt haben, ergänzen Sie weitere Testprofile, damit Sie verschiedene Varianten der Nachricht für unterschiedliche Profildaten testen können. Anschließend werden die Profile unter den Auswahlfeldern aufgelistet.

   ![](assets/preview-profile-list.png)

   Basierend auf den Personalisierungselementen der Nachricht zeigt diese Liste Daten zu den einzelnen Testprofilen in den entsprechenden Spalten an.

## Prüfen der Nachrichtenvorschau{#preview-your-messages}

Nach der Auswahl von [Testprofilen](#select-test-profiles) können Sie Ihre Nachrichten als Vorschau anzeigen und den Inhalt überprüfen.

### Vorschau einer E-Mail{#preview-email}

Gehen Sie wie folgt vor, um eine Vorschau eines E-Mail-Inhalts anzuzeigen:

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** oberhalb des E-Mail-Inhalts.

1. Wählen Sie ein Testprofil aus. Überprüfen Sie die in den Spalten aufgeführten Werte. Verwenden Sie die Pfeile nach rechts oder links, um Daten zu durchsuchen.

   ![](assets/preview-tab-select-profile.png)

1. Klicken Sie auf das Symbol **[!UICONTROL Daten auswählen]** über der Liste, um Spalten hinzuzufügen oder zu entfernen.

   ![](assets/preview-select-data.png)

   Am Ende der Liste sehen Sie Personalisierungsfelder für die aktuelle Nachricht. Bei diesem Beispiel sind dies Ort, Vorname und Nachname des Profils. Wählen Sie diese Felder aus und stellen Sie sicher, dass diese Werte in Ihren Testprofilen definiert sind.

1. In der Nachrichtenvorschau werden die personalisierten Elemente durch die Daten der ausgewählten Testprofile ersetzt.

   Bei dieser Nachricht werden beispielsweise E-Mail-Inhalt und E-Mail-Betreff personalisiert:

   ![](assets/preview-test-profile.png)

1. Wählen Sie für jede Nachrichtenvariante weitere Testprofile zum Rendern von E-Mail-Vorschauen aus.

### Vorschau einer Push-Benachrichtigung{#preview-push}

Gehen Sie wie folgt vor, um eine Vorschau des Inhalts einer Push-Benachrichtigung anzuzeigen:

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** oberhalb des Inhalts einer Push-Benachrichtigung.

1. Wählen Sie ein Testprofil aus. Überprüfen Sie die in den Spalten aufgeführten Werte. Verwenden Sie die Pfeile nach rechts oder links, um Daten zu durchsuchen.

1. Wechseln Sie zur **[!UICONTROL Push]**-Nachricht.

1. Führen Sie dieselben Schritte wie oben beschrieben aus, um ein Testprofil und den Gerätetyp für die Vorschau des Inhalts auszuwählen: **[!UICONTROL iOS]** oder **[!UICONTROL Android]**.

   ![](assets/preview-iOS.png)

1. Für die Push-Vorschau werden die Daten von Testprofilen im Nachrichteninhalt verwendet.

   Bei dieser Push-Benachrichtigung werden beispielsweise Titel und Textkörper personalisiert:

   ![](assets/preview-android.png)

## Durchführen eines Testversands{#send-proofs}

Ein Testversand dient der Validierung einer Nachricht, bevor sie an die wichtigste Audience gesendet wird. Die Empfänger des Testversands sind für die Überprüfung der Nachricht verantwortlich: Darstellung, Inhalt, Personalisierungseinstellungen, Konfiguration.

Sobald [Testprofile](#select-test-profiles) ausgewählt sind, können Sie den Testversand starten.

1. Klicken Sie im Bildschirm **[!UICONTROL Vorschau]** auf die Schaltfläche **[!UICONTROL Testversand starten]**.

   ![](assets/send-proof-button.png)

1. Geben Sie im Fenster **[!UICONTROL Testversand starten]** die E-Mail-Adresse Ihres Empfängers ein und klicken Sie auf **[!UICONTROL Hinzufügen]**, um den Testversand an sich selbst oder Mitglieder Ihrer Organisation zu senden.

   Beachten Sie, dass Sie bis zu zehn Empfänger für Ihren Testversand hinzufügen können.

   ![](assets/send-proof-button_2.png)

1. Wählen Sie anschließend die **Testprofile**, die zur Personalisierung des Nachrichteninhalts verwendet werden.

   Die Anzahl der Testversandnachrichten, die jeder Empfänger erhält, entspricht der Anzahl der ausgewählten Testprofile. Wenn Sie beispielsweise fünf Empfänger-E-Mails hinzugefügt und zehn Testprofile ausgewählt haben, senden Sie fünfzig Testversandnachrichten, von denen jeder Empfänger zehn erhält.

1. Bei Bedarf können Sie der Betreffzeile des Testversands ein Präfix hinzufügen. Nur alphanumerische Zeichen und Sonderzeichen, z. B. . - _ ( ) [ ] sind als Präfix für die Betreffzeile zulässig.

1. Klicken Sie auf **[!UICONTROL Testversand durchführen]**.

   ![](assets/send-proof-select.png)

1. Klicken Sie im Bildschirm **[!UICONTROL Vorschau]** auf die Schaltfläche **[!UICONTROL Testversand anzeigen]**, um den Status zu prüfen.

   ![](assets/send-proof-view.png)

Es wird empfohlen, nach jeder Änderung am Nachrichteninhalt Testsendungen durchzuführen.

>[!NOTE]
>
>Im Testversand an die Testprofile ist der Link zur Mirrorseite nicht aktiv. Er wird erst in den endgültigen Nachrichten aktiviert.

## E-Mail-Rendering{#email-rendering}

Nutzen Sie Ihr **Litmus**-Konto in [!DNL Journey Optimizer], um das **E-Mail-Rendering** in populären E-Mail-Clients zu überprüfen.

Um die Rendering-Funktionen für E-Mails zu nutzen, müssen Sie

* ein Litmus-Konto besitzen
* [Auswählen der Testprofile](#select-test-profiles)

Anschließend gehen Sie wie folgt vor:

1. Klicken Sie in Email Designer auf die Schaltfläche **[!UICONTROL Vorschau]** und wählen Sie die Registerkarte **[!UICONTROL E-Mail-Rendering]**.

1. Klicken Sie auf **Verbinden Sie Ihr Litmus-Konto** im oberen rechten Bereich.

   ![](assets/email-rendering-litmus.png)

1. Geben Sie Ihre Anmeldedaten ein und melden Sie sich an.

   ![](assets/email-rendering-credentials.png)

1. Klicken Sie auf die Schaltfläche **Test ausführen**, um E-Mail-Vorschauen zu generieren.

1. Prüfen Sie Ihren E-Mail-Inhalt auf gängigen Clients für Desktop, mobile Geräte und Web.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>Durch die Verknüpfung Ihres **Litmus**-Kontos mit [!DNL Journey Optimizer] erteilen Sie Ihr Einverständnis, dass Testmeldungen an Litmus gesendet werden: Nach dem Versand werden diese E-Mails nicht mehr von Adobe verwaltet. Dementsprechend gelten für diese E-Mails die Litmus-Richtlinien zur Datenspeicherung, einschließlich der Personalisierungsdaten, die in diesen Testnachrichten enthalten sein können.

## Anleitungsvideo{#video-preview}

Hier erfahren Sie, wie Sie das E-Mail-Rendering für mehrere Posteingänge testen, Ihre personalisierten E-Mails mit Testprofilen in der Vorschau anzeigen und Testsendungen durchführen können.

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)
