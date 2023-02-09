---
title: Visual Editing Helper-Erweiterung
description: Entdecken Sie die Chrome-Erweiterung Visual Editing Helper, mit der Sie Web-Seiten in Journey Optimizer erstellen und in der Vorschau anzeigen können.
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
source-git-commit: 01fc9bfba54e9cdbd356c1ed06ef2caeb3705a0a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Visual Editing Helper-Erweiterung {#visual-editing-helper}

Um Ihre Web-Erlebnisse schnell erstellen und in der Vorschau anzeigen zu können, können Sie mit der Browser-Erweiterung Visual Editing Helper von Adobe Experience Cloud für Google Chrome Websites zuverlässig in den Web-Designer von Adobe [!DNL Journey Optimizer] laden.

>[!NOTE]
>
>Die Web-Kanal-Funktion ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar.

## Installieren der Erweiterung Visual Editing Helper {#install-visual-editing-helper}

Gehen Sie wie folgt vor, um die Browser-Erweiterung Visual Editing Helper abzurufen und zu installieren.

1. Navigieren Sie im Google Chrome Web Store zum [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} Browsererweiterung.

1. Klicken Sie auf **[!UICONTROL Zu Chrome hinzufügen]** > **[!UICONTROL Erweiterung hinzufügen]**.

1. Erstellen Sie eine Web-Kanalkampagne in [!DNL Journey Optimizer]. [Weitere Informationen dazu](author-web.md#create-web-campaign)

1. Öffnen Sie den [!DNL Journey Optimizer]-Web-Designer, um mit der Erstellung Ihres Web-Erlebnisses zu beginnen. [Weitere Informationen](author-web.md)

1. Stellen Sie sicher, dass die Browser-Erweiterung Visual Editing Helper in der Symbolleiste Ihres Chrome-Browsers aktiviert ist, indem Sie auf das entsprechende Symbol klicken.

   ![](assets/web-visual-editing-extension.png)

Der Visual Editing Helper von Adobe Experience Cloud wird jetzt automatisch aktiviert, wenn eine Website im [!DNL Journey Optimizer]-Web-Designer geöffnet wird, um die Inhaltserstellung zu unterstützen.

Die Erweiterung verfügt über keine bedingten Einstellungen und verarbeitet alle Einstellungen automatisch, einschließlich der SameSite-Cookie-Einstellungen.

>[!NOTE]
>
>Einige Websites werden möglicherweise aus einem der folgenden Gründe nicht zuverlässig im [!DNL Journey Optimizer]-Web-Designer geöffnet:
>
> * Die Website hat strikte Sicherheitsrichtlinien.
> * Die Website befindet sich in einem iFrame.
> * Die QA- oder Status-Site von Kundinnen und Kunden kann extern nicht abgerufen werden (interne Site).


## Fehlerbehebung

Wenn Sie bei Verwendung des Adobe [!DNL Journey Optimizer]-Web-Designers versuchen, eine Website zu laden, die nicht geladen werden kann, wird eine Meldung angezeigt, die die Installation der [Browser-Erweiterung Visual Editing Helper](#install-visual-editing-helper) empfiehlt.

Wenn das Adobe Experience Platform Web SDK noch nicht auf der Website implementiert wurde, wird im Webdesigner eine Meldung angezeigt, die empfiehlt, die Browsererweiterung Visual Editing Helper zu installieren und die [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"}.

Wenn die Site nicht geladen werden kann oder sich unerwartet verhält, besteht die Möglichkeit, Cookies auf Ihrer Website im Browser zu akzeptieren, bevor Sie versuchen, sie in Adobe [!DNL Journey Optimizer] zu laden.

Wenn das Laden der Anmeldeseite bei Seiten mit Authentifizierung fehlschlägt oder wenn Sie nach dem Anmeldeversuch nicht angemeldet sind, versuchen Sie, sich zunächst auf einer anderen Registerkarte Ihres Browsers anzumelden und dann die Website im Adobe [!DNL Journey Optimizer]-Web-Designer zu laden.
