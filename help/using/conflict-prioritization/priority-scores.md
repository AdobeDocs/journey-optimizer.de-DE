---
title: Zuweisen von Prioritätswerten zu Journeys und Kampagnen
description: Erfahren Sie, wie Sie Journeys und Kampagnen Prioritätswerte zuweisen.
role: User
level: Beginner
exl-id: f33ca0a8-ed33-4964-a85c-8705a4ff728e
source-git-commit: e8f7f5862e3816481680fa999657ae90334ff888
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 46%

---

# Zuweisen von Prioritätswerten {#priority}

Mit Journey Optimizer können Sie einer Journey, einer Kampagne oder einer eingehenden Kanalaktion innerhalb der Journey (Action)-Aktivität einen **[!UICONTROL zuweisen]**.

Die Priorität ist wichtig, um eine Journey, Kampagne oder Aktion zu priorisieren, wenn eine Einschränkung vorliegt (z. B. eine Frequenzlimitierung).

In Situationen, in denen Ihre Kundschaft für viele Journeys, Kampagnen oder Mitteilungen infrage kommt und Sie selektiv auswählen möchten, welche sie betreten und erhalten soll, sollten Sie dieses Feld verwenden.

## Zuweisen von Prioritätswerten zu Journeys und Kampagnen {#priority-journey-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorität"
>abstract="Weisen Sie der Kampagne eine Prioritätsbewertung zu. Die Priorität ist wichtig, um eine Kampagne zu priorisieren, wenn eine Einschränkung vorliegt, z. B. eine Frequenzlimitierung.</br>Geben Sie einen numerischen Wert ein (von 0-100). Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn zwei Kampagnen die gleiche Priorität haben, wird die Kampagne angezeigt, die zuerst aktiviert wurde."

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorität"
>abstract="Weisen Sie der Journey eine Prioritätsbewertung zu. Die Priorität ist wichtig, um eine Journey zu priorisieren, wenn eine auferlegte Einschränkung wie eine Frequenzlimitierung vorliegt.</br>Geben Sie einen numerischen Wert ein (von 0-100). Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn zwei Kampagnen die gleiche Prioritätsbewertung haben, wird die Journey angezeigt, die zuerst aktiviert wurde."

➡️ [Funktion im Video kennenlernen](#video)

Die Zuweisung eines Prioritätswerts ist für eingehende Kommunikation wie Web, Mobile und In-App entscheidend. Wenn Sie mehrere Kampagnen mit derselben Kanalkonfiguration haben (z. B. ein Banner am oberen Rand Ihrer Web-Seite), kann dies problematisch sein, da nur Inhalte aus einer Kampagne angezeigt werden können. Bei dem Prioritätswert geben Sie an, welche Kampagne angezeigt werden soll, wenn die empfangende Person für mehr als eine Kampagne infrage kommt.

>[!NOTE]
>
>In Kampagnen ist der Prioritätswert nur für eingehende Web-, In-App- und Code-basierte Kanäle verfügbar.

Um einer Journey oder Kampagne einen Prioritätswert zuzuweisen, geben Sie einen numerischen Wert (von 0 bis 100) in das Feld **[!UICONTROL Prioritätswert]** ein, das sich in den Journey- oder Kampagneneigenschaften befindet. Je höher die Zahl, desto höher die Priorität.

Wenn Sie diese Kampagne erstellen und sicherstellen möchten, dass der Inhalt dieser Kampagne angezeigt wird, sollten Sie ihr den Wert 100 geben.

![](assets/priority-score.png)

>[!IMPORTANT]
>
>Wenn zwei Journeys oder Kampagnen den gleichen Prioritätswert haben, verfügt das System über keinen Unentschiedenheitsmechanismus. Stellen Sie sicher, dass Prioritätswerte eindeutig sind, um Konflikte zu vermeiden.

## Zuweisen von Prioritätswerten zu eingehenden Kanalaktionen {#priority-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_priority"
>title="Priorität"
>abstract="Weisen Sie der Journey-Aktion einen Prioritätswert zu. Wenn mehrere Journey-Aktionen oder -Kampagnen mit derselben Kanalkonfiguration vorhanden sind, muss die Priorität für eingehende Aktionen beibehalten werden.</br>Geben Sie einen numerischen Wert ein (von 0-100). Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Standardmäßig wird der Prioritätswert für die Aktion vom Gesamtprioritätswert für die Journey übernommen."

Journey Optimizer ermöglicht es Ihnen auch, den eingehenden Kanalaktionen innerhalb der Aktivität **[!UICONTROL Aktion“ einen]** zuzuweisen.

Auf diese Weise können Sie eine eingehende Aktion priorisieren, wenn mehrere Journey-Aktionen oder -Kampagnen mit derselben Kanalkonfiguration vorhanden sind.

>[!NOTE]
>
>In der Aktivität **[!UICONTROL Aktion]** ist der Prioritätswert nur für die Web-, In-App- und Code-basierten eingehenden Kanäle verfügbar.

Im **[!UICONTROL Konfliktmanagement]** ist standardmäßig die Option **[!UICONTROL Journey-Priorität verwenden]** ausgewählt, was bedeutet, dass der Prioritätswert für die Aktion vom Gesamtprioritätswert für die Journey übernommen wird.

Um den eingehenden Aktionen, die in der Aktivität **[!UICONTROL Action]** definiert sind, einen Prioritätswert zuzuweisen, deaktivieren Sie die Option **[!UICONTROL Journey-Priorität verwenden]** und geben Sie einen numerischen Wert (von 0-100) in das Feld **[!UICONTROL Priority]** ein. Je höher die Zahl, desto höher die Priorität.

![](assets/action-journey-priority-score.png){width=70%}

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435529?quality=12)
