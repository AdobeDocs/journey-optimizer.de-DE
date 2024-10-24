---
title: Zuweisen von Prioritätswerten zu Journeys und Kampagnen
description: Erfahren Sie, wie Sie Journey und Kampagnen Prioritätsbewertungen zuweisen.
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit"
hide: true
hidefromtoc: true
source-git-commit: 0eedadee1e8c1d4642d8602d48bcc9a49a0a2e53
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 85%

---


# Zuweisen von Prioritätswerten zu Journeys und Kampagnen {#priority}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit Konfliktmanagement und Priorisierung](gs-conflict-prioritization.md)
* [Potenzielle Konflikte in Journey und Kampagnen erkennen](conflicts.md)
* **[Zuweisung von Prioritätswerten zu Journey und Kampagnen](priority-scores.md)**
* [Journey-Begrenzung und Schlichtung](journey-capping.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Die Tools zur Konfliktverwaltung und Priorisierung sind derzeit nur für ausgewählte Benutzer verfügbar, da sie nur über eingeschränkte Verfügbarkeit verfügen.

Mit Journey Optimizer können Sie einer Journey oder Kampagne einen Prioritätswert zuweisen. Die Priorität ist von wesentlicher Bedeutung, um eine Journey, Kampagne oder Aktion zu priorisieren, wenn eine erzwungene Begrenzung vorliegt (z. B. eine Häufigkeittsbegrenzung). In Situationen, in denen Ihre Kundschaft für viele Journeys, Kampagnen oder Mitteilungen infrage kommt und Sie selektiv auswählen möchten, welche sie betreten und erhalten soll, sollten Sie dieses Feld verwenden.

>[!NOTE]
>
>Der Prioritätswert ist für eingehende Kanäle verfügbar: Web-, In-App- und Code-basierte Kanäle. In Journeys ist der Prioritätswert nur für die Kanäle **In-App** und **Code-basiert** verfügbar.

➡️ [Entdecken Sie diese Funktion im Video](#video)

Die Zuweisung eines Prioritätswerts ist für eingehende Kommunikation wie Web, Mobile und In-App entscheidend. Wenn Sie mehrere Kampagnen haben, die dieselbe Kanalkonfiguration verwenden (z. B. ein Banner oben auf Ihrer Webseite), könnte dies problematisch sein, da nur Inhalte aus einer Kampagne angezeigt werden können. Bei dem Prioritätswert geben Sie an, welche Kampagne angezeigt werden soll, wenn die empfangende Person für mehr als eine Kampagne infrage kommt.

Um einer Journey oder Kampagne einen Prioritätswert zuzuweisen, geben Sie einen numerischen Wert (von 0 bis 100) in das Feld **[!UICONTROL Prioritätswert]** ein, das sich in den Journey- oder Kampagneneigenschaften befindet. Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn Sie diese Kampagne erstellen und sicherstellen möchten, dass der Inhalt dieser Kampagne angezeigt wird, sollten Sie ihr den Wert 100 geben.

![](assets/priority-score.png)

Wenn zwei Kampagnen die gleiche Priorität haben, wird die Kampagne angezeigt, die zuerst aktiviert wurde.

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435529?quality=12)
