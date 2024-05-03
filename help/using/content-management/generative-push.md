---
solution: Journey Optimizer
product: journey optimizer
title: Push-Generierung mit dem AI-Assistenten
description: Erstellen von Push-Inhalten mit dem AI-Assistenten
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: ff7f2b42d63e8a3d02f5dbebd926eda26c646752
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 62%

---

# Push-Generierung mit dem AI-Assistenten {#generative-push}

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

* [Erste Schritte mit dem KI-Assistenten](gs-generative.md)
* [Generierung von E-Mails mit dem KI-Assistenten](generative-email.md)
* [Generierung von SMS mit dem KI-Assistenten](generative-sms.md)
* **[Push-Generierung mit dem AI-Assistenten](generative-push.md)**
* [Inhaltsexperiment mit dem KI-Assistenten](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Bevor Sie mit der Verwendung dieser Funktion beginnen, lesen Sie die entsprechenden Informationen zu [Schutzmechanismen und Begrenzungen](gs-generative.md#generative-guardrails).

Nachdem Sie Ihre Nachrichten erstellt und personalisiert haben, stellen Sie mit dem KI-Assistenten in Adobe Journey Optimizer den Inhalt Ihrer Push-Benachrichtigung auf die nächste Stufe.

Auf den folgenden Registerkarten erfahren Sie, wie Sie den AI-Assistenten in Journey Optimizer verwenden.

>[!BEGINTABS]

>[!TAB Vollständige Push-Generierung]

In diesem speziellen Beispiel erfahren Sie, wie Sie mit dem AI-Assistenten eine ansprechende Push-Benachrichtigung senden.

Führen Sie folgende Schritte aus:

1. Klicken Sie nach der Erstellung und Konfiguration Ihrer Push-Benachrichtigungskampagne auf **[!UICONTROL Inhalt bearbeiten]**.

   Weiterführende Informationen zur Konfiguration Ihrer Push-Benachrichtigungskampagne finden Sie im Abschnitt [diese Seite](../push/create-push.md).

1. Füllen Sie die **[!UICONTROL Grundlegende Details]** für Ihre Kampagne. Klicken Sie abschließend auf **[!UICONTROL Inhalt bearbeiten]**.

1. Personalisieren Sie Ihre Push-Benachrichtigung nach Bedarf. [Weitere Informationen](../push/design-push.md)

1. Rufen Sie das Menü **[!UICONTROL KI-Assistenten anzeigen]** auf.

   ![](assets/push-genai-full-1.png){zoomable=&quot;yes&quot;}

1. Aktivieren Sie die **[!UICONTROL Originalinhalt verwenden]** Option für den KI-Assistenten, um neuen Inhalt basierend auf Ihrem Kampagneninhalt, Ihrem Namen und der ausgewählten Zielgruppe zu personalisieren.

   Ihr Prompt muss immer an einen bestimmten Kontext gebunden sein.

1. Passen Sie den Inhalt an, indem Sie im Feld **[!UICONTROL Prompt]** beschreiben, was Sie generieren möchten.

   Wenn Sie Hilfe bei der Erstellung Ihrer Eingabeaufforderung benötigen, rufen Sie die **[!UICONTROL Eingabebibliothek]** , die eine Vielzahl von schnellen Ideen zur Verbesserung Ihrer Kampagnen bietet.

   ![](assets/push-genai-full-2.png){zoomable=&quot;yes&quot;}

1. Wählen Sie **[!UICONTROL Marken-Asset hochladen]** aus, um ein beliebiges Marken-Asset hinzuzufügen, das Inhalte enthält, die zusätzlichen Kontext für den KI-Assistenten bieten können.

1. Wählen Sie das zu erzeugende Feld aus: **[!UICONTROL Titel]** und/oder **[!UICONTROL Nachricht]**.

1. Passen Sie Ihr Prompt mit den verschiedenen Optionen an:

   * **[!UICONTROL Kommunikationsstrategie]**: Wählen Sie den am besten geeigneten Kommunikationsstil für den generierten Text aus.
   * **[!UICONTROL Sprache]**: Wählen Sie die Sprache aus, in der Sie Ihre Inhalte generieren möchten.
   * **[!UICONTROL Ton]**: Der Ton der E-Mail sollte bei Ihrer Zielgruppe ankommen. Je nachdem, ob Sie informativ, humorvoll oder überzeugend klingen möchten, kann der KI-Assistent die Nachricht entsprechend anpassen.

   ![](assets/push-genai-full-3.png){zoomable=&quot;yes&quot;}

1. Wenn das Prompt fertig ist, klicken Sie auf **[!UICONTROL Generieren]**.

1. Durchsuchen Sie die generierten **[!UICONTROL Varianten]** und klicken Sie auf **[!UICONTROL Vorschau]**, um eine Vollbildversion der ausgewählten Variante anzuzeigen.

1. Navigieren Sie zur Option **[!UICONTROL Verfeinern]** im Fenster **[!UICONTROL Vorschau]**, um auf zusätzliche Anpassungsfunktionen zuzugreifen:

   * **[!UICONTROL Als Referenzinhalt verwenden]**: Die gewählte Variante dient hierbei als Referenzinhalt für die Generierung anderer Ergebnisse.

   * **[!UICONTROL Umformulierungen]**: Der KI-Assistent kann Ihre Nachricht auf verschiedene Arten umformulieren, sodass Ihre Texte für verschiedene Zielgruppen interessant und ansprechend klingen.

   * **[!UICONTROL Einfache Sprache]**: Nutzen Sie den KI-Assistenten, um Ihre Sprache zu vereinfachen und den Inhalt auf diese Weise für eine breitere Zielgruppe verständlich und zugänglich zu machen.

   ![](assets/push-genai-full-4.png){zoomable=&quot;yes&quot;}

1. Klicken Sie auf **[!UICONTROL Auswählen]**, sobald Sie den passenden Inhalt gefunden haben.

   Sie können auch Experimente für Ihren Inhalt aktivieren. [Weitere Informationen](generative-experimentation.md)

1. Fügen Sie Personalisierungsfelder ein, um Ihre E-Mail-Inhalte auf der Grundlage von Profildaten anzupassen. Klicken Sie danach auf die Schaltfläche **[!UICONTROL Inhalte simulieren]**, um das Rendern zu steuern, und überprüfen Sie die Personalisierungseinstellungen mit Testprofilen. [Weitere Informationen](../personalization/personalize.md)

Wenn Sie Inhalt, Zielgruppe und Zeitplan definiert haben, können Sie Ihre Push-Kampagne vorbereiten. [Weitere Informationen](../campaigns/review-activate-campaign.md)

>[!TAB Textgenerierung]

In diesem Beispiel erfahren Sie, wie Sie den KI-Assistenten für bestimmte Inhalte verwenden. Führen Sie folgende Schritte aus:

1. Klicken Sie nach der Erstellung und Konfiguration Ihrer Push-Benachrichtigungskampagne auf **[!UICONTROL Inhalt bearbeiten]**.

   Weiterführende Informationen zur Konfiguration einer Push-Kampagne finden Sie im Abschnitt [diese Seite](../push/create-push.md).

1. Füllen Sie die **[!UICONTROL Grundlegende Details]** für Ihre Kampagne. Klicken Sie abschließend auf **[!UICONTROL Inhalt bearbeiten]**.

1. Personalisieren Sie Ihre Push-Benachrichtigung nach Bedarf. [Weitere Informationen](../push/design-push.md)

1. Zugriff auf **[!UICONTROL AI-Assistenten anzeigen]** Menü neben Ihrem **[!UICONTROL Titel]** oder **[!UICONTROL Nachricht]** -Felder.

   ![](assets/push-genai-1.png){zoomable=&quot;yes&quot;}

1. Aktivieren Sie die **[!UICONTROL Referenzinhalt verwenden]** Option für den KI-Assistenten, um neuen Inhalt basierend auf Ihrem Kampagneninhalt, Ihrem Namen und der ausgewählten Zielgruppe zu personalisieren.

   Ihr Prompt muss immer an einen bestimmten Kontext gebunden sein.

1. Passen Sie den Inhalt an, indem Sie im Feld **[!UICONTROL Prompt]** beschreiben, was Sie generieren möchten.

   Wenn Sie Hilfe bei der Erstellung Ihrer Eingabeaufforderung benötigen, rufen Sie die **[!UICONTROL Eingabebibliothek]** , die eine Vielzahl von schnellen Ideen zur Verbesserung Ihrer Kampagnen bietet.

   ![](assets/push-genai-2.png){zoomable=&quot;yes&quot;}

1. Wählen Sie **[!UICONTROL Marken-Asset hochladen]** aus, um ein beliebiges Marken-Asset hinzuzufügen, das Inhalte enthält, die zusätzlichen Kontext für den KI-Assistenten bieten können.

   ![](assets/push-genai-3.png){zoomable=&quot;yes&quot;}

1. Passen Sie Ihr Prompt mit den verschiedenen Optionen an:

   * **[!UICONTROL Kommunikationsstrategie]**: Wählen Sie den am besten geeigneten Kommunikationsstil für den generierten Text aus.
   * **[!UICONTROL Sprache]**: Wählen Sie die Sprache aus, in der Sie Ihre Inhalte generieren möchten.
   * **[!UICONTROL Ton]**: Der Ton der E-Mail sollte bei Ihrer Zielgruppe ankommen. Je nachdem, ob Sie informativ, humorvoll oder überzeugend klingen möchten, kann der KI-Assistent die Nachricht entsprechend anpassen.
   * **[!UICONTROL Länge]**: Legen Sie die Länge Ihres Inhalts mit dem Schieberegler fest.

   ![](assets/push-genai-4.png){zoomable=&quot;yes&quot;}

1. Wenn das Prompt fertig ist, klicken Sie auf **[!UICONTROL Generieren]**.

1. Durchsuchen Sie die generierten **[!UICONTROL Varianten]** und klicken Sie auf **[!UICONTROL Vorschau]**, um eine Vollbildversion der ausgewählten Variante anzuzeigen.

1. Navigieren Sie zur Option **[!UICONTROL Verfeinern]** im Fenster **[!UICONTROL Vorschau]**, um auf zusätzliche Anpassungsfunktionen zuzugreifen:

   * **[!UICONTROL Als Referenzinhalt verwenden]**: Die gewählte Variante dient hierbei als Referenzinhalt für die Generierung anderer Ergebnisse.

   * **[!UICONTROL Weiter ausführen]**: Der KI-Assistent kann Ihnen dabei helfen, genauer auf bestimmte Themen einzugehen und zusätzliche Details zum besseren Verständnis und für mehr Interaktion zu liefern.

   * **[!UICONTROL Zusammenfassen]**: Zu ausführliche Informationen können die Empfangenden einer E-Mail überfordern. Nutzen Sie den KI-Assistenten, um die wichtigsten Punkte in klaren, prägnanten Aussagen zusammenzufassen, die die Aufmerksamkeit der Leserinnen und Leser wecken und sie zum Weiterlesen anregen.

   * **[!UICONTROL Umformulieren]**: Der KI-Assistent kann Ihre Nachricht auf verschiedene Arten umformulieren, sodass Ihr Text frisch und für verschiedene Zielgruppen ansprechend bleibt.

   * **[!UICONTROL Einfachere Sprache verwenden]**: Nutzen Sie den KI-Assistenten, um Ihre Sprache zu vereinfachen und für eine breitere Zielgruppe Klarheit und Barrierefreiheit zu gewährleisten.

   ![](assets/push-genai-5.png){zoomable=&quot;yes&quot;}

1. Klicken Sie auf **[!UICONTROL Auswählen]**, sobald Sie den passenden Inhalt gefunden haben.

   Sie können auch Experimente für Ihren Inhalt aktivieren. [Weitere Informationen](generative-experimentation.md)

1. Fügen Sie Personalisierungsfelder ein, um Ihre E-Mail-Inhalte auf der Grundlage von Profildaten anzupassen. Klicken Sie danach auf die Schaltfläche **[!UICONTROL Inhalte simulieren]**, um das Rendern zu steuern, und überprüfen Sie die Personalisierungseinstellungen mit Testprofilen. [Weitere Informationen](../personalization/personalize.md)

Wenn Sie Inhalt, Zielgruppe und Zeitplan definiert haben, können Sie Ihre Push-Kampagne vorbereiten. [Weitere Informationen](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
