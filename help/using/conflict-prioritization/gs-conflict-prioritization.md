---
title: Konflikt-Management und Priorisierung
description: Erfahren Sie, wie Sie die Tools für Konflikt-Management und Priorisierung in Journey Optimizer nutzen können.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: a0eda2e1d021af37eb54f3ffa5bac0ac6e8ef6ce
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 31%

---

# Konflikt-Management und Priorisierung {#conflict-prioritization}

In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Mithilfe von Tools für das Konflikt-Management und die Priorisierung können Sie durchdachte, zeitlich optimal abgestimmte Kommunikation bereitstellen. So wird Kundenmüdigkeit verhindert und sichergestellt, dass Ihre Zielgruppe die richtigen Botschaften erhält. Durch die Verwendung von Konflikterkennung, Prioritätswerten und Regelsätzen können Sie Kampagnen und Journey optimieren, um Überschneidungen zu vermeiden und die Häufigkeit auf allen Kanälen auszugleichen.

Diese Tools sind für Kampagnen sowie für Journey vom Typ „Unitär“, „Zielgruppen-Qualifizierung“ und „Zielgruppe lesen“ verfügbar. Unabhängig davon, ob Sie Einschränkungen für die Häufigkeit des Versands von Nachrichten festlegen oder entscheiden, welche Kampagnen Vorrang haben, vereinfachen diese Funktionen gemeinsam die Entscheidungsfindung und optimieren Ihre Marketing-Strategie.

## Wo Sie beginnen {#where-to-start}

| Ihr Ziel | Tool | Aktion |
|-----------|------|--------|
| Überprüfen, ob sich Journey oder Kampagnen überschneiden (Zeitleiste, Zielgruppe, Kanal) | **Konflikterkennung** | [Identifizieren potenzieller Konflikte](conflicts.md) |
| Festlegen, welche Nachricht den Zuschlag erhält, wenn ein Profil für mehrere Profile qualifiziert ist | **Prioritätswerte** | [Prioritätswerte zuweisen](priority-scores.md) |
| Begrenzung, wie oft oder wie viele Nachrichten ein Profil erhält | **Regelsätze** (Frequenzlimitierung, Journey-Limitierung, ruhige Stunden) | [Festlegen von Begrenzungsregeln für Nachrichten und Journey](../../rp_landing_pages/capping-rules-landing-page.md) |

**Typischer Fluss:** Sie die Konflikterkennung, um Überschneidungen zu erkennen, und wenden Sie dann Prioritätswerte und Regelsätze an, um zu steuern, welche Nachrichten wie oft gesendet werden.

## Tools für Konfliktmanagement und Priorisierung {#tools}

### Konflikt-Management-Tool

Mit dem **Konflikterkennungs-Tool** können Sie potenzielle Überschneidungen in Journeys und Kampagnen identifizieren. Dies ist von entscheidender Bedeutung, da zu viele gleichzeitige Mitteilungen zu Kundenermüdung führen können. Mit Journey Optimizer können Sie Elemente wie Timelines, Zielgruppenüberschneidungen und Kanalkonfigurationen überwachen. Durch das frühzeitige Identifizieren von Konflikten können Sie Ihre Kampagnen verfeinern und verhindern, dass Kundinnen und Kunden mehrere Nachrichten gleichzeitig erhalten.

[Erfahren Sie, wie Sie potenzielle Konflikte in Journey und Kampagnen erkennen](conflicts.md)

### Prioritätswerte

Mit den **Prioritätswerten** können Sie steuern, welche Kampagnen oder Journeys Vorrang haben, wenn sich eine Kundin oder ein Kunde für mehrere Mitteilungen qualifiziert. Dies ist insbesondere bei eingehenden Kanälen wie Web und Mobile nützlich, in denen immer nur eine Kampagne angezeigt werden kann. Durch Zuweisung eines Prioritätswertes zu jeder Journey oder Kampagne können Sie sicherstellen, dass die wichtigste Nachricht zuerst gesendet wird. 

[Erfahren Sie, wie Sie Journey und Kampagnen Prioritätswerte zuweisen](priority-scores.md)

### Regelsätze

Mit Regelsätzen können Sie **mehrere Regeln gruppieren** und auf die Journey und Kampagnen Ihrer Wahl anwenden. Dies bietet eine verbesserte Granularität, um zu begrenzen, wie oft und wie viele Journey ein Kunde innerhalb eines bestimmten Zeitraums eingeben kann, oder um zu steuern, wie oft Benutzer Nachrichten erhalten, je nach Art der Kommunikation.

* **Journey-Begrenzung und Schlichtung** - Beschränken Sie, wie oft und wie viele Journey ein Kunde innerhalb eines bestimmten Zeitraums eingeben kann. Sie können die Anzahl der Journey-Einträge für ein Profil begrenzen oder die Anzahl der Journey begrenzen, in denen ein Kunde gleichzeitig angemeldet sein kann. Verwenden Sie Schlichtungseinstellungen, um zu entscheiden, welchen Journey ein Kunde eingeben soll, wenn er für mehrere Journey qualifiziert ist, und verwenden Sie Prioritätswerte, um die beste Anpassung zu bestimmen. [Informationen zum Arbeiten mit Journey-Begrenzungen und -Steuerung](journey-capping.md)

* **Frequenzlimitierung nach Kanal und Kommunikationstyp** - Legen Sie die Frequenzlimitierung nach Kommunikationstyp fest (z. B. Verkauf, Werbung), um zu verhindern, dass Kunden mit ähnlichen Nachrichten überlastet werden. Kontrollfrequenz über mehrere Kanäle hinweg, wobei zu viele Profile automatisch ausgeschlossen werden. [Erfahren Sie, wie Sie die Frequenzlimitierung nach Kanal und Kommunikationstyp festlegen](channel-capping.md)

* **Ruhezeiten** - Definieren Sie zeitbasierte Ausschlüsse, damit während bestimmter Zeiträume (E-Mail, SMS, Push, WhatsApp) keine Nachrichten gesendet werden. [Erfahren Sie, wie Sie ruhige Stunden festlegen](quiet-hours.md)

[Erfahren Sie, wie Sie mit Regelsätzen arbeiten](rule-sets.md)

## Leitlinien und Einschränkungen {#guardrails}

* **Kampagnen und Prioritätswerte**: In Kampagnen ist der Prioritätswert nur für eingehende **Web-**, **In-App-** und **Code-basierte** Kanäle verfügbar.

* **Latenz bei der Aktualisierung des Profilzählers** - Nachdem ein Kunde eine Journey eingegeben hat, kann es bis zu 10 Minuten dauern, bis der Profilzählerwert aktualisiert wird. Wenn ein Profil innerhalb eines kurzen Zeitfensters in zwei Journeys eintritt, erkennt die zweite Journey möglicherweise nicht richtig, dass die Frequenzbegrenzung bereits erreicht wurde, sodass das Profil möglicherweise in beide Journeys eintreten kann.

* **Namespace-Priorität für die Begrenzung von Journey-Einträgen** - Die Begrenzung von Einträgen wird nur unterstützt, wenn der auf der Journey ausgewählte Namespace der Namespace mit der höchsten Priorität ist, der in der Sandbox definiert ist. Wenn die Namespace-Priorität nicht explizit konfiguriert wurde, hat E-Mail standardmäßige die höchste Priorität.

* Journey **Simultane Aktivierungen in Zielgruppen-Qualifizierungsereignissen** - Wenn mehrere Zielgruppen-Qualifizierungs-Journey durch dasselbe Zielgruppen-Qualifizierungsereignis aktiviert werden, sind die Zählungen für die Begrenzung der Eintritte nicht korrekt. Wenn die Anzahl unter der Obergrenze liegt, schlichtet die Journey weiterhin, aber sie kann nicht die aktuellsten Zählungen mit gleichzeitigen Aktivierungen erhalten.

## Weitere Ressourcen

* **[Identifizieren potenzieller Konflikte](conflicts.md)** - Erfahren Sie, wie Sie Konflikte zwischen sich überschneidenden Kampagnen und Journeys erkennen und lösen können.
* **[Prioritätswerte zuweisen](priority-scores.md)** - Erfahren Sie, wie Sie Prioritätswerte zuweisen und verwenden, um die Priorität des Nachrichtenversands zu steuern.
* **[Arbeiten mit Regelsätzen](rule-sets.md)** - Erfahren Sie, wie Sie Regelsätze für das Konflikt-Management und die Nachrichten-Governance erstellen und anwenden.
* **[Journey-Begrenzung und Schlichtung](journey-capping.md)** - Richten Sie Begrenzungsregeln und Schlichtungen auf Journey-Ebene ein.
* **[Frequenzlimitierung nach Kanal](channel-capping.md)** - Legen Sie Frequenzlimitierungen auf Kanalebene fest, um Übernachrichten zu verhindern.
* **[Stille Stunden festlegen](quiet-hours.md)** - Zeitbasierte Ausschlüsse für den Nachrichtenversand definieren.
* **[Tutorials ](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}** Konfliktmanagement - Schritt-für-Schritt-Video-Tutorials.
