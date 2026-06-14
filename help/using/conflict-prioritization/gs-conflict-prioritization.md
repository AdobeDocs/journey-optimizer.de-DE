---
title: Konflikt-Management und Priorisierung
description: Erfahren Sie, wie Sie die Tools für Konflikt-Management und Priorisierung in Journey Optimizer nutzen können.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
TQID: https://experienceleague.adobe.com/vx-CmsYwj7QyN2sVMrpJ9VUNDgnXq8qt1nT9lHOFV3s
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: fd59660e-de8a-4bfb-85dc-7fa546030c49
subfeature_v2: id: e23d48b5-7858-4d45-9c56-9e2b4be8500eid: f3fe4813-f254-4f8f-99cc-24bd67f119e1id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
source-git-commit: 49542ca70e8899061bc79772cf96069ab2587ab2
workflow-type: tm+mt
source-wordcount: 896
ht-degree: 95%

---

# Konflikt-Management und Priorisierung {#conflict-prioritization}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Konflikterkennung, Prioritätswerte und Regelsätze zusammenarbeiten, um Überschneidungen bei der Kommunikation zu vermeiden und zu steuern, wie oft Kunden benachrichtigt werden.

>[!ENDSHADEBOX]

In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Die Tools für Konflikt-Management und Priorisierung helfen Ihnen dabei, gut durchdachte, zeitlich optimal abgestimmte Kommunikationen bereitzustellen und so eine Ermüdung Ihrer Kundschaft zu verhindern und sicherzustellen, dass Ihre Zielgruppe die richtigen Nachrichten erhält. Durch die Verwendung von Konflikterkennung, Prioritätswerten und Regelsätzen können Sie Kampagnen und Journeys optimieren, um Überschneidungen zu vermeiden und die Häufigkeit zwischen den Kanälen auszugleichen.

Diese Tools sind für Kampagnen und für unitäre Journeys sowie Journeys vom Typ „Zielgruppenqualifizierung“ und „Zielgruppe lesen“ verfügbar. Ganz gleich, ob Sie die Häufigkeit des Versendens von Nachrichten begrenzen oder entscheiden, welche Kampagnen Vorrang haben sollen – diese Funktionen wirken zusammen, um die Entscheidungsfindung zu vereinfachen und Ihre Marketing-Strategie zu optimieren.

## Ausgangspunkt {#where-to-start}

| Ihr Ziel | Tool | Aktion |
|-----------|------|--------|
| Überprüfen, ob sich Journeys oder Kampagnen überschneiden (Timeline, Zielgruppe, Kanal) | **Konflikterkennung** | [Identifizieren potenzieller Konflikte](conflicts.md) |
| Festlegen, welche Nachricht gesendet wird, wenn ein Profil für mehrere qualifiziert ist | **Prioritätswerte** | [Zuweisen von Prioritätswerten](priority-scores.md) |
| Begrenzen, wie oft oder wie viele Nachrichten ein Profil erhält | **Regelsätze** (Frequenzbegrenzung, Journey-Begrenzung, Ruhezeiten) | [Festlegen von Regeln für die Nachrichten- und Journey-Begrenzung](../../rp_landing_pages/capping-rules-landing-page.md) |

**Typischer Fluss:** Verwenden Sie die Konflikterkennung, um Überschneidungen zu ermitteln, und wenden Sie dann Prioritätswerte und Regelsätze an, um zu steuern, welche Nachrichten wie oft gesendet werden.

## Tools für Konflikt-Management und Priorisierung {#tools}

### Konflikt-Management-Tool

Mit dem **Konflikterkennungs-Tool** können Sie potenzielle Überschneidungen in Journeys und Kampagnen identifizieren. Dies ist von entscheidender Bedeutung, da zu viele gleichzeitige Mitteilungen zu Kundenermüdung führen können. Mit Journey Optimizer können Sie Elemente wie Timelines, Zielgruppenüberschneidungen und Kanalkonfigurationen überwachen. Durch das frühzeitige Identifizieren von Konflikten können Sie Ihre Kampagnen verfeinern und verhindern, dass Kundinnen und Kunden mehrere Nachrichten gleichzeitig erhalten.

[Weitere Informationen zum Erkennen potenzieller Konflikte in Journeys und Kampagnen](conflicts.md)

### Prioritätswerte

Mit den **Prioritätswerten** können Sie steuern, welche Kampagnen oder Journeys Vorrang haben, wenn sich eine Kundin oder ein Kunde für mehrere Mitteilungen qualifiziert. Dies ist insbesondere bei eingehenden Kanälen wie Web und Mobile nützlich, in denen immer nur eine Kampagne angezeigt werden kann. Durch Zuweisung eines Prioritätswertes zu jeder Journey oder Kampagne können Sie sicherstellen, dass die wichtigste Nachricht zuerst gesendet wird.

[Weitere Informationen zum Zuweisen von Prioritätswerten zu Journeys und Kampagnen](priority-scores.md)

### Regelsätze

Mit Regelsätzen können Sie **mehrere Regeln gruppieren** und diese auf die Journeys und Kampagnen Ihrer Wahl anwenden. Dies bietet verbesserte Granularität, um zu begrenzen, wie oft und in wie viele Journeys Kundinnen und Kunden innerhalb eines bestimmten Zeitrahmens eintreten können, oder um zu steuern, wie oft Benutzende je nach Kommunikationsart Nachrichten erhalten.

* **Journey-Begrenzung und -Schlichtung**: Begrenzen Sie, wie oft und in wie viele Journeys eine Kundin bzw. ein Kunde innerhalb eines bestimmten Zeitrahmens eintreten kann. Sie können auch die Anzahl der Journey-Eintritte für ein Profil begrenzen oder die Anzahl der Journeys begrenzen, an denen eine Kundin bzw. ein Kunde gleichzeitig teilnehmen kann. Verwenden Sie die Schlichtungseinstellungen, um festzulegen, in welche Journey eine Kundin bzw. ein Kunde eintreten soll, wenn sie bzw. er sich für mehrere Journeys qualifiziert, und mithilfe von Prioritätswerten die beste Wahl zu bestimmen. [Weitere Informationen zum Arbeiten mit Journey-Begrenzung und -Schlichtung](journey-capping.md)

* **Frequenzbegrenzung nach Kanal- und Kommunikationstyp**: Legen Sie Frequenzbegrenzung nach Kommunikationstyp (z. B. Vertrieb, Werbung) fest, um zu verhindern, dass Kundinnen und Kunden mit ähnlichen Nachrichten überhäuft werden. Kontrollieren Sie die Frequenz über mehrere Kanäle hinweg und schließen Sie übermäßig angesprochene Profile automatisch aus. [Weitere Informationen zum Festlegen von Frequenzbegrenzung nach Kanal- und Kommunikationstyp](channel-capping.md)

* **Ruhezeiten**: Definieren Sie zeitbasierte Ausschlüsse, damit während bestimmter Zeiträume keine Nachrichten gesendet werden (E-Mail, SMS, Push, WhatsApp). [Weitere Informationen zum Festlegen von Ruhezeiten](quiet-hours.md)

[Erfahren Sie, wie Sie mit Regelsätzen arbeiten](rule-sets.md)

## Leitlinien und Einschränkungen {#guardrails}

* **Kampagnen und Prioritätswerte**: In Kampagnen ist der Prioritätswert nur für eingehende **Web-**, **In-App-** und **Code-basierte** Kanäle verfügbar.

* **Latenz der Aktualisierung des Profilzählers**: Nachdem eine Kundin bzw. ein Kunde in eine Journey eingetreten ist, kann es bis zu 10 Minuten dauern, bis der Profilzählerwert aktualisiert wird. Wenn ein Profil innerhalb eines kurzen Zeitfensters in zwei Journeys eintritt, erkennt die zweite Journey möglicherweise nicht richtig, dass die Frequenzbegrenzung bereits erreicht wurde, sodass das Profil möglicherweise in beide Journeys eintreten kann.

* **Namespace-Priorität für Journey-Eintrittsbegrenzung**: Die Begrenzung für Eintritte wird nur unterstützt, wenn der in der Journey ausgewählte Namespace der Namespace mit der höchsten Priorität ist, der in der Sandbox definiert ist. Wenn die Namespace-Priorität nicht explizit konfiguriert wurde, hat E-Mail standardmäßige die höchste Priorität.

* **Gleichzeitige Aktivierungen in Journeys des Typs „Zielgruppenqualifizierung“**: Wenn mehrere Journeys des Typs „Zielgruppenqualifizierung“ durch dasselbe Zielgruppenqualifizierungsereignis aktiviert werden, ist die Anzahl für die Eintrittsbegrenzung nicht korrekt. Wenn die Anzahl unter der Begrenzung liegt, schlichtet die Journey weiterhin, aber sie ist nicht in der Lage, die aktuellste Anzahl mit den gleichzeitigen Aktivierungen zu ermitteln.

## Zusätzliche Ressourcen

* **[Identifizieren potenzieller Konflikte](conflicts.md)**: Erfahren Sie, wie Sie Konflikte zwischen überschneidenden Kampagnen und Journeys ermitteln und lösen.
* **[Zuweisen von Prioritätswerten](priority-scores.md)**: Erfahren Sie, wie Sie Prioritätswerte zuweisen und verwenden, um die Vorrangigkeit des Nachrichtenversands zu steuern.
* **[Arbeiten mit Regelsätzen](rule-sets.md)**: Erfahren Sie, wie Sie Regelsätze für das Konflikt-Management und die Nachrichten-Governance erstellen und anwenden.
* **[Journey-Begrenzung und -Schlichtung](journey-capping.md)**: Legen Sie Begrenzungsregeln und Schlichtung auf Journey-Ebene fest.
* **[Frequenzbegrenzung nach Kanal](channel-capping.md)**: Legen Sie Frequenzbegrenzungen auf Kanalebene fest, um übermäßigen Nachrichtenversand zu vermeiden.
* **[Festlegen von Ruhezeiten](quiet-hours.md)**: Definieren Sie zeitbasierte Ausschlüsse für den Nachrichtenversand.
* **[Tutorials zum Konflikt-Management](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}**: Detaillierte Video-Tutorials.
* **[Journey Optimizer-Anwendungsfälle](../building-journeys/jo-use-cases.md)** - Durchsuchen Sie praktische Muster, einschließlich Frequenzlimitierung und Journey-Unterdrückungslogik.
