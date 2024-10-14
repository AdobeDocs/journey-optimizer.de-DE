---
title: Zuweisen von Prioritätswerten zu Journeys und Kampagnen
description: Erfahren Sie, wie Sie Journey und Kampagnen Prioritätsbewertungen zuweisen.
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 6%

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

Mit Journey Optimizer können Sie einer Journey oder Kampagne eine Prioritätsbewertung zuweisen. Die Priorität ist von wesentlicher Bedeutung, um eine Journey, Kampagne oder Aktion zu priorisieren, wenn eine erzwungene Einschränkung vorliegt (z. B. eine Frequenzbegrenzung). Wenn ein Kunde für viele Journey, Kampagnen oder Mitteilungen qualifiziert ist und Sie selektiv sein möchten, in welche Bereiche er eintreten und welche er empfangen soll, sollten Sie dieses Feld nutzen.

>[!NOTE]
>
>Die Prioritätsbewertung ist für eingehende Kanäle verfügbar: Web-, In-App- und code-basierte Kanäle. Unter Journey ist die Prioritätsbewertung nur für die Kanäle **in der App** und **code-basiert** verfügbar.

Die Zuweisung eines Prioritätswerts ist für die eingehende Kommunikation wie Web, Mobile und In-App-Nachrichten von entscheidender Bedeutung. Wenn mehrere Kampagnen dieselbe Kanalkonfiguration verwenden (z. B. ein Banner oben auf Ihrer Webseite), kann dies problematisch sein, da nur Inhalte einer Kampagne angezeigt werden können. In der Prioritätsbewertung legen Sie Ihre Voreinstellung fest, für welche Kampagne angezeigt werden soll, wenn sich der Empfänger für mehr als eine Kampagne qualifizieren kann.

Um einer Journey oder Kampagne eine Prioritätsbewertung zuzuweisen, geben Sie einen numerischen Wert (von 0-100) in das Feld **[!UICONTROL Prioritätsbewertung]** ein, das sich in den Journey- oder Kampagneneigenschaften befindet. Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn Sie diese Kampagne erstellen und sicherstellen möchten, dass dieser Kampagneninhalt angezeigt wird, erhalten Sie eine Punktzahl von 100.

![](assets/priority-score.png)

In Situationen, in denen zwei Kampagnen dieselbe Prioritätsbewertung aufweisen, wird die zuvor aktivierte Kampagne angezeigt.
