---
title: Zuweisen von Prioritätswerten zu Journeys und Kampagnen
description: Erfahren Sie, wie Sie Journeys und Kampagnen Prioritätswerte zuweisen.
role: User
level: Beginner
exl-id: f33ca0a8-ed33-4964-a85c-8705a4ff728e
source-git-commit: 0334d0b6d2fc9665ee1fe407502117679cf220f2
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 77%

---

# Zuweisen von Prioritätswerten zu Journeys und Kampagnen {#priority}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorität"
>abstract="Weisen Sie der Kampagne eine Prioritätsbewertung zu. Die Priorität ist wichtig, um eine Kampagne zu priorisieren, wenn eine Einschränkung vorliegt, z. B. eine Frequenzlimitierung.</br>Geben Sie einen numerischen Wert ein (von 0-100). Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn zwei Kampagnen die gleiche Priorität haben, wird die Kampagne angezeigt, die zuerst aktiviert wurde."

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorität"
>abstract="Weisen Sie der Journey eine Prioritätsbewertung zu. Die Priorität ist wichtig, um eine Journey zu priorisieren, wenn eine auferlegte Einschränkung wie eine Frequenzlimitierung vorliegt.</br>Geben Sie einen numerischen Wert ein (von 0-100). Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn zwei Kampagnen die gleiche Prioritätsbewertung haben, wird die Journey angezeigt, die zuerst aktiviert wurde."

>[!CONTEXTUALHELP]
>id="ajo_journey_action_priority"
>title="Priorität"
>abstract="Weisen Sie der Journey-Aktion einen Prioritätswert zu. Wenn mehrere Journey-Aktionen oder -Kampagnen mit derselben Kanalkonfiguration vorhanden sind, muss die Priorität für eingehende Aktionen beibehalten werden.</br>Geben Sie einen numerischen Wert ein (von 0-100). Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Standardmäßig wird der Prioritätswert für die Aktion vom Gesamtprioritätswert für die Journey übernommen."

Mit Journey Optimizer können Sie einer Journey oder Kampagne einen Prioritätswert zuweisen. Die Priorität ist von wesentlicher Bedeutung, um eine Journey, Kampagne oder Aktion zu priorisieren, wenn eine erzwungene Begrenzung vorliegt (z. B. eine Häufigkeittsbegrenzung). In Situationen, in denen Ihre Kundschaft für viele Journeys, Kampagnen oder Mitteilungen infrage kommt und Sie selektiv auswählen möchten, welche sie betreten und erhalten soll, sollten Sie dieses Feld verwenden.

>[!NOTE]
>
>In Kampagnen ist der Prioritätswert nur für eingehende Web-, In-App- und Code-basierte Kanäle verfügbar.

➡️ [Funktion im Video kennenlernen](#video)

Die Zuweisung eines Prioritätswerts ist für eingehende Kommunikation wie Web, Mobile und In-App entscheidend. Wenn Sie mehrere Kampagnen haben, die dieselbe Kanalkonfiguration verwenden (z. B. ein Banner oben auf Ihrer Webseite), könnte dies problematisch sein, da nur Inhalte aus einer Kampagne angezeigt werden können. Bei dem Prioritätswert geben Sie an, welche Kampagne angezeigt werden soll, wenn die empfangende Person für mehr als eine Kampagne infrage kommt.

Um einer Journey oder Kampagne einen Prioritätswert zuzuweisen, geben Sie einen numerischen Wert (von 0 bis 100) in das Feld **[!UICONTROL Prioritätswert]** ein, das sich in den Journey- oder Kampagneneigenschaften befindet. Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn Sie diese Kampagne erstellen und sicherstellen möchten, dass der Inhalt dieser Kampagne angezeigt wird, sollten Sie ihr den Wert 100 geben.

![](assets/priority-score.png)

>[!IMPORTANT]
>
>Wenn zwei Journeys oder Kampagnen den gleichen Prioritätswert haben, verfügt das System über keinen Unentschiedenheitsmechanismus. Stellen Sie sicher, dass Prioritätswerte eindeutig sind, um Konflikte zu vermeiden.

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3445010?quality=12&captions=ger)
