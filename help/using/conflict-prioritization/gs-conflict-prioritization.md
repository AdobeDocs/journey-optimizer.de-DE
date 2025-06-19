---
title: Konflikt-Management und Priorisierung
description: Erfahren Sie, wie Sie die Tools für Konflikt-Management und Priorisierung in Journey Optimizer nutzen können.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 43fe7ca22a7685944b2b11ca3d1872641d1f4694
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 97%

---

# Konflikt-Management und Priorisierung {#conflict-prioritization}

## Tools für Konflikt-Management und Priorisierung {#tools}

In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet mehrere Tools zum Konflikt-Management und zur Priorisierung.

Diese Tools sind für Kampagnen und für unitäre Journeys sowie Journeys vom Typ „Zielgruppen-Qualifizierung“ und „Zielgruppe lesen“ verfügbar.

Mithilfe dieser Tools können Sie reibungslosere und zielgerichtetere Marketing-Maßnahmen gewährleisten und gleichzeitig die richtige Nachricht zur richtigen Zeit senden, wodurch Konflikte und Überlastungen vermieden werden.

### Konflikt-Management-Tool

Mit dem **Konflikterkennungs-Tool** können Sie potenzielle Überschneidungen in Journeys und Kampagnen identifizieren. Dies ist von entscheidender Bedeutung, da zu viele gleichzeitige Mitteilungen zu Kundenermüdung führen können. Mit Journey Optimizer können Sie Elemente wie Timelines, Zielgruppenüberschneidungen und Kanalkonfigurationen überwachen. Durch das frühzeitige Identifizieren von Konflikten können Sie Ihre Kampagnen verfeinern und verhindern, dass Kundinnen und Kunden mehrere Nachrichten gleichzeitig erhalten.

➡️ [Informationen zum Erkennen potenzieller Konflikte in Journeys und Kampagnen](conflicts.md)

### Prioritätswerte

Mit den **Prioritätswerten** können Sie steuern, welche Kampagnen oder Journeys Vorrang haben, wenn sich eine Kundin oder ein Kunde für mehrere Mitteilungen qualifiziert. Dies ist insbesondere bei eingehenden Kanälen wie Web und Mobile nützlich, in denen immer nur eine Kampagne angezeigt werden kann. Durch Zuweisung eines Prioritätswertes zu jeder Journey oder Kampagne können Sie sicherstellen, dass die wichtigste Nachricht zuerst gesendet wird. 

➡️ [Informationen zum Zuweisen von Prioritätswerten zu Journeys und Kampagnen](priority-scores.md)

### Regelsätze

Mit Regelsätzen können Sie **mehrere Regeln zu Regelsätzen zusammenfassen** und diese auf die Journeys und Kampagnen Ihrer Wahl anwenden. Dies bietet eine verbesserte Granularität, die begrenzt, wie oft und in wie viele Journeys Kundinnen und Kunden innerhalb eines bestimmten Zeitrahmens eintreten können, oder die steuert, wie oft Benutzende je nach Kommunikationsart eine Nachricht erhalten.

* **Journey-Begrenzung und -Steuerung**

  Mit Regelsätzen können Sie einschränken, wie oft und in wie viele Journeys eine Kundin bzw. ein Kunde innerhalb eines bestimmten Zeitrahmens eintreten kann. Sie können auch Regeln einrichten, um die Anzahl der Journey-Eintritte für ein Profil zu begrenzen oder die Anzahl der Journeys zu begrenzen, an denen eine Kundin bzw. ein Kunde gleichzeitig teilnehmen kann. 

  Darüber hinaus können Sie mithilfe von Steuerungseinstellungen festlegen, in welche Journey eine Kundin bzw. ein Kunde eintreten soll, wenn sie bzw. er sich für mehrere Journeys qualifiziert, und mithilfe von Prioritätswerten die beste Wahl bestimmen. 

  ➡️ [Informationen zum Arbeiten mit Journey-Begrenzungen und -Steuerung](journey-capping.md)

* **Frequenzbegrenzung nach Kanal und Kommunikationstyp**

  Sie können Regelsätze auch verwenden, um die Frequenzbegrenzung nach Kommunikationstyp (z. B. Vertrieb, Werbeaktionen) festzulegen, um zu verhindern, dass Kundinnen und Kunden mit ähnlichen Nachrichten überlastet werden. Sie können die Frequenz über mehrere Kanäle hinweg steuern und automatisch Profile ausschließen, die zu oft angesprochen wurden, um ein besseres Kundenerlebnis sicherzustellen.

  ➡️ [Erfahren Sie, wie Sie die Frequenzbegrenzung nach Kanal und Kommunikationstyp festlegen](../conflict-prioritization/channel-capping.md)

## Schutzmechanismen und Einschränkungen

* **Kampagnen und Prioritätswerte**: In Kampagnen ist der Prioritätswert nur für eingehende **Web-**, **In-App-** und **Code-basierte** Kanäle verfügbar.

* **Aktualisierungslatenz des Profilzählers**

  Nachdem eine Kundin bzw. ein Kunde in eine Journey eingetreten ist, kann es bis zu 10 Minuten dauern, bis der Profilzählerwert aktualisiert wird.

  Wenn ein Profil innerhalb eines kurzen Zeitfensters in zwei Journeys eintritt, erkennt die zweite Journey möglicherweise nicht richtig, dass die Frequenzbegrenzung bereits erreicht wurde, sodass das Profil möglicherweise in beide Journeys eintreten kann.

* **Namespace-Priorität für die Begrenzung für Journey-Eintritte**

  Die Begrenzung für Eintritte wird nur unterstützt, wenn der in der Journey ausgewählte Namespace der Namespace mit der höchsten Priorität ist, der in der Sandbox definiert ist. Wenn die Namespace-Priorität nicht explizit konfiguriert wurde, ist die standardmäßige höchste Priorität E-Mail.

* **Simultane Aktivierungen in Journeys zur Zielgruppenqualifizierung**

  Wenn mehrere Journeys zur Zielgruppenqualifizierung durch dasselbe Ereignis zur Zielgruppenqualifizierung aktiviert werden, ist die Anzahl für die Eintrittsbegrenzung nicht korrekt. Wenn die Anzahl unter der Obergrenze liegt, steuert die Journey weiterhin, aber sie ist nicht in der Lage, die aktuellsten Zählungen mit gleichzeitigen Aktivierungen zu erhalten.
