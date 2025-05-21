---
title: Konflikt-Management und Priorisierung
description: Erfahren Sie, wie Sie die Tools für Konflikt-Management und Priorisierung in Journey Optimizer nutzen können.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 22%

---

# Konflikt-Management und Priorisierung {#conflict-prioritization}

## Tools für Konflikt-Management und Priorisierung {#tools}

In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet mehrere Tools zum Konflikt-Management und zur Priorisierung.

Diese Tools sind für Kampagnen und unitäre, Zielgruppen-Qualifizierungs- und Lese-Zielgruppen-Journey verfügbar.

Durch die Nutzung dieser Tools können Sie sicherstellen, dass Ihre Marketing-Maßnahmen reibungsloser und zielgerichteter verlaufen, die richtige Botschaft zur richtigen Zeit bereitgestellt und Konflikte und Überlastungen vermieden werden.

### Tool zur Konflikterkennung

Mit dem **Konflikterkennungs-Tool** können Sie potenzielle Überschneidungen in Journeys und Kampagnen identifizieren. Dies ist von entscheidender Bedeutung, da zu viele gleichzeitige Mitteilungen zu Kundenermüdung führen können. Mit Journey Optimizer können Sie Elemente wie Timelines, Zielgruppenüberschneidungen und Kanalkonfigurationen überwachen. Durch die frühzeitige Identifizierung von Konflikten können Sie Ihre Kampagnen verfeinern, um zu vermeiden, dass Kunden mit mehreren Nachrichten gleichzeitig bombardiert werden.

➡️ [Erfahren Sie, wie Sie potenzielle Konflikte in Journey und Kampagnen erkennen](conflicts.md)

### Prioritätswerte

**Prioritätswerte** helfen Ihnen zu steuern, welche Kampagnen oder Journey Vorrang haben, wenn ein Kunde für mehrere Kommunikationen qualifiziert ist. Dies ist insbesondere bei eingehenden Kanälen wie Web und Mobile nützlich, in denen immer nur eine Kampagne angezeigt werden kann. Indem Sie jeder Journey oder Kampagne einen Prioritätswert zuweisen, können Sie sicherstellen, dass die wichtigste Nachricht zuerst zugestellt wird.

➡️ [Erfahren Sie, wie Sie Journey und Kampagnen Prioritätswerte zuweisen](priority-scores.md)

### Regelsätze

Mit Regelsätzen können Sie **mehrere Regeln zu Regelsätzen gruppieren** und auf die gewünschten Journey und Kampagnen anwenden. Dies bietet eine verbesserte Granularität, um zu begrenzen, wie oft und wie viele Journey ein Kunde innerhalb eines bestimmten Zeitraums eingeben kann, oder zu steuern, wie oft Benutzer eine Nachricht je nach Kommunikationstyp erhalten.

* **Journey-Begrenzung und -Steuerung**

  Mit Regelsätzen können Sie einschränken, wie oft und wie viele Journey ein Kunde innerhalb eines bestimmten Zeitraums eingeben kann. Sie können auch Regeln einrichten, um die Anzahl der Journey-Einträge für ein Profil zu begrenzen oder die Anzahl der Journey zu begrenzen, in denen eine Kundin oder ein Kunde gleichzeitig angemeldet werden kann.

  Darüber hinaus können Sie mithilfe von Schlichtungseinstellungen entscheiden, welche Journey ein Kunde eingeben soll, wenn er für mehrere Journey qualifiziert ist. Dabei werden Prioritätswerte verwendet, um die beste Anpassung zu ermitteln.

  ➡️ [Erfahren Sie, wie Sie mit Journey-Begrenzung und Schlichtung arbeiten](journey-capping.md)

* **Frequenzlimitierung nach Kanal und Kommunikationstyp**

  Sie können auch Regelsätze verwenden, um die Frequenzlimitierung nach Kommunikationstyp festzulegen (z. B. Verkauf, Werbung), um zu verhindern, dass Kunden mit ähnlichen Nachrichten überlastet werden. Sie können die Frequenz über mehrere Kanäle hinweg steuern und automatisch Profile ausschließen, die zu oft angesprochen wurden, um ein besseres Kundenerlebnis sicherzustellen.

  ➡️ [Erfahren Sie, wie Sie die Frequenzlimitierung nach Kanal und Kommunikationstyp festlegen](../conflict-prioritization/channel-capping.md)

## Schutzmechanismen und Einschränkungen

* **Kampagnen und Prioritätswerte** - In Kampagnen ist der Prioritätswert nur für die **Web**, **In-App** und **Code-basierten** eingehenden Kanäle verfügbar.

* **Aktualisierungslatenz des Profilzählers**

  Es kann bis zu 20 Minuten dauern, nachdem ein Kunde eine Journey eingegeben hat, bis der Profilzählerwert aktualisiert wird.

  Wenn ein Profil innerhalb eines kurzen Zeitfensters in zwei Journey eintritt, erkennt die zweite Journey möglicherweise nicht richtig, dass die Frequenzbegrenzung bereits erreicht wurde, sodass das Profil möglicherweise in beide Journey eintreten kann.

* **Namespace-Priorität für die Journey-Eintragsbegrenzung**

  Die Begrenzung von Einträgen wird nur unterstützt, wenn der auf der Journey ausgewählte Namespace der Namespace mit der höchsten Priorität ist, der in der Sandbox definiert ist. Wenn die Namespace-Priorität nicht explizit konfiguriert wurde, ist die standardmäßige höchste Priorität E-Mail.

* **Simultane Aktivierungen in Journey zur Zielgruppenqualifizierung**

  Wenn mehrere Zielgruppen-Qualifizierungs-Journeys durch dasselbe Zielgruppen-Qualifizierungsereignis aktiviert werden, sind die Zählungen für die Eintragsbegrenzung nicht korrekt. Wenn die Anzahl unter der Obergrenze liegt, schlichtet Journey weiterhin, aber es ist nicht in der Lage, die aktuellsten Zählungen mit gleichzeitigen Aktivierungen zu erhalten.
