---
title: Visual Editing Helper-Erweiterung
description: Entdecken Sie die Chrome-Erweiterung Visual Editing Helper , mit der Sie Web-Seiten in Journey Optimizer erstellen und in der Vorschau anzeigen können.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Visual Editing Helper-Erweiterung {#visual-editing-helper}

Um Ihre Web-Erlebnisse schnell erstellen und in der Vorschau anzeigen zu können, können Sie mit der Adobe Experience Cloud Visual Editing Helper-Browsererweiterung für Google Chrome Websites zuverlässig in Adobe laden [!DNL Journey Optimizer] Webdesigner.

>[!NOTE]
>
>Die Webkanalfunktion ist derzeit als Beta-Version verfügbar, über die nur Benutzer ausgewählt werden können.

## Installieren der Visual Editing Helper-Erweiterung {#install-visual-editing-helper}

Gehen Sie wie folgt vor, um die Browsererweiterung Visual Editing Helper abzurufen und zu installieren.

1. Navigieren Sie im Google Chrome Web Store zum [Visual Editing Helper von Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=&quot;_blank&quot;} Browsererweiterung.

1. Klicken **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.

1. Erstellen Sie eine Webkanalkampagne in [!DNL Journey Optimizer]. [Erfahren Sie mehr](author-web.md#create-web-campaign)

1. Öffnen Sie die [!DNL Journey Optimizer] Webdesigner , um mit der Erstellung Ihres Web-Erlebnisses zu beginnen. [Weitere Infos](author-web.md)

1. Stellen Sie sicher, dass die Browsererweiterung Visual Editing Helper in der Symbolleiste Ihres Chrome-Browsers aktiviert ist, indem Sie auf das entsprechende Symbol klicken.

   ![](assets/web-visual-editing-extension.png)

Der Visual Editing Helper von Adobe Experience Cloud wird jetzt automatisch aktiviert, wenn eine Website im [!DNL Journey Optimizer] Webdesigner zur Unterstützung der Inhaltserstellung.

Die Erweiterung verfügt über keine bedingten Einstellungen und verarbeitet alle Einstellungen automatisch, einschließlich der SameSite-Cookie-Einstellungen.

>[!NOTE]
>
>Einige Websites werden möglicherweise nicht zuverlässig in der [!DNL Journey Optimizer] Webdesigner aus einem der folgenden Gründe:
>
> * Die Website hat strenge Sicherheitsrichtlinien.
> * Die Website befindet sich in einem iFrame.
> * Die QA- oder Staging-Site des Kunden ist nicht für die Außenwelt verfügbar (die Site ist intern).


## Fehlerbehebung

Bei Verwendung von Adobe [!DNL Journey Optimizer] Webdesigner: Wenn Sie versuchen, eine Website zu laden, die nicht geladen werden kann, wird eine Meldung angezeigt, die empfiehlt, die [Visual Editing Helper-Browsererweiterung](#install-visual-editing-helper).

Wenn das Adobe Experience Platform Web SDK noch nicht auf der Website implementiert wurde, wird im Webdesigner eine Meldung angezeigt, die darauf hinweist, dass Sie die Browsererweiterung Visual Editing Helper installieren und die [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;}.

Wenn die Site nicht geladen werden kann oder sich unerwartet verhält, besteht die Möglichkeit, Cookies auf Ihrer Website im Browser zu akzeptieren, bevor versucht wird, sie in Adobe zu laden [!DNL Journey Optimizer].

Für Seiten, die sich unter der Authentifizierung befinden, wenn das Laden der Anmeldeseite fehlschlägt oder wenn Sie nach dem Anmeldeversuch immer noch nicht angemeldet sind, versuchen Sie, sich zunächst in einer anderen Registerkarte Ihres Browsers anzumelden und dann die Website in Adobe zu laden. [!DNL Journey Optimizer] Webdesigner.
