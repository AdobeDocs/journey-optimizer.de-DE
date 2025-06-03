---
title: Konflikt-Management und Priorisierung
description: Erfahren Sie, wie Sie die Tools für Konflikt-Management und Priorisierung in Journey Optimizer nutzen können.
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: f55f985375cf360ce55074cb227b6c424db05b5c
workflow-type: ht
source-wordcount: '677'
ht-degree: 100%

---

# Konflikt-Management und Priorisierung {#conflict-prioritization}

>[!AVAILABILITY]
>
>Funktionen für Konflikt-Management und Priorisierung sind derzeit für eine ausgewählte Gruppe von Kundinnen und Kunden verfügbar (eingeschränkte Verfügbarkeit). Sie werden in Zukunft schrittweise für weitere Benutzende eingeführt. Wenden Sie sich an Ihr Accountteam, wenn Sie auf die Warteliste für diese Funktionen gesetzt werden möchten.

In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet mehrere Tools zum Konflikt-Management und zur Priorisierung.

Diese Tools sind für Kampagnen und für unitäre Journeys sowie Journeys vom Typ „Zielgruppen-Qualifizierung“ und „Zielgruppe lesen“ verfügbar.

Mithilfe dieser Tools können Sie reibungslosere und zielgerichtetere Marketing-Maßnahmen gewährleisten und gleichzeitig die richtige Nachricht zur richtigen Zeit senden, wodurch Konflikte und Überlastungen vermieden werden.

## Tools für Konflikt-Management und Priorisierung {#tools}

Mit dem **Konflikterkennungs-Tool** können Sie potenzielle Überschneidungen in Journeys und Kampagnen identifizieren. Dies ist von entscheidender Bedeutung, da zu viele gleichzeitige Mitteilungen zu Kundenermüdung führen können. Mit Journey Optimizer können Sie Elemente wie Timelines, Zielgruppenüberschneidungen und Kanalkonfigurationen überwachen. Durch das frühzeitige Identifizieren von Konflikten können Sie Ihre Kampagnen verfeinern und verhindern, dass Kundinnen und Kunden mehrere Nachrichten gleichzeitig erhalten. [Informationen zum Erkennen potenzieller Konflikte in Journeys und Kampagnen](conflicts.md)

Darüber hinaus können Sie mit den **Prioritätswerten** steuern, welche Kampagnen oder Journeys Vorrang haben, wenn sich eine Kundin oder ein Kunde für mehrere Mitteilungen qualifiziert. Dies ist insbesondere bei eingehenden Kanälen wie Web und Mobile nützlich, in denen immer nur eine Kampagne angezeigt werden kann. Durch Zuweisung eines Prioritätswertes zu jeder Journey oder Kampagne können Sie sicherstellen, dass die wichtigste Nachricht zuerst gesendet wird. [Informationen zum Zuweisen von Prioritätswerten zu Journeys und Kampagnen](priority-scores.md)

Mit **Journey-Begrenzungen und -Schlichtung** können Sie einschränken, wie oft und in wie viele Journeys eine Kundin bzw. ein Kunde innerhalb eines bestimmten Zeitraums eintreten kann. Sie können Regeln einrichten, um die Anzahl der Journey-Eintritte für ein Profil zu begrenzen oder die Anzahl der Journeys zu begrenzen, an denen eine Kundin bzw. ein Kunde gleichzeitig teilnehmen kann. Darüber hinaus können Sie mithilfe von Steuerungseinstellungen festlegen, in welche Journey eine Kundin bzw. ein Kunde eintreten soll, wenn sie bzw. er sich für mehrere Journeys qualifiziert, und mithilfe von Prioritätswerten die beste Wahl bestimmen. [Informationen zum Arbeiten mit Journey-Begrenzungen und -Steuerung](journey-capping.md)

Schließlich können Sie auch Regelsätze verwenden, um die **Frequenzbegrenzung nach Kommunikationstyp** (z. B. Vertrieb, Werbeaktionen) festzulegen, um zu verhindern, dass Kundinnen und Kunden mit ähnlichen Nachrichten überlastet werden. Sie können die Frequenz über mehrere Kanäle hinweg steuern und automatisch Profile ausschließen, die zu oft angesprochen wurden, um ein besseres Kundenerlebnis sicherzustellen. [Informationen zum Arbeiten mit Regelsätzen](../configuration/rule-sets.md)</li></ul>

Mithilfe dieser Funktionen können Sie reibungslosere und zielgerichtetere Marketing-Maßnahmen gewährleisten und gleichzeitig die richtige Nachricht zur richtigen Zeit senden, wodurch Konflikte und Überlastungen vermieden werden.

## Schutzmechanismen und Einschränkungen

**Frequenzbegrenzung und Batch-Zielgruppen**

Bei der Frequenzbegrenzung sowohl für den Kanal als auch für die Journey wird, wenn es sich bei der verwendeten Zielgruppe um eine Batch-Zielgruppe handelt, der Profilzählerwert, auf den zum Zeitpunkt des Eintritts in die Journey verwiesen wird, oder die Nachrichtenlaufzeit für eine Kanalkommunikation aus dem täglichen Schnappschuss entnommen.

Dies kann problematisch sein, da Kundinnen und Kunden die Frequenzbegrenzung überschreiten können, wenn sie in eine andere Journey eingetreten sind oder eine andere Kommunikation zwischen dem Zeitpunkt des täglichen Schnappschusses und dem Zeitpunkt des Eintritts in die Journey (oder der zugestellten Nachricht) erhalten haben.

**Frequenzbegrenzung und Streaming-Zielgruppen**

Bei Streaming-Zielgruppen kann es bis zu 2 Stunden dauern, bis das System einen aktualisierten Zählerwert erkennt. Daher empfehlen wir, Kommunikationen und Journey mit einem Abstand von mindestens 2 Stunden zu präsentieren, um dieses Risiko zu minimieren.

**Journey-Startzeit**

Um sicherzustellen, dass die Funktionen für das Konflikt-Management und die Priorisierung ordnungsgemäß funktionieren, empfehlen wir, die Startzeit Ihrer Journey mindestens 10 Minuten in die Zukunft zu setzen, damit das System den Zähler entsprechend aktualisieren kann.

Wenn Kundinnen und Kunden ihre Obergrenze bereits beim Betreten einer Journey erreicht haben, wird ihnen zwar weiterhin kein Eintritt gewährt, aber wenn sie ihre Obergrenze nicht erreicht haben, wird der Eintrittszähler nicht erhöht.

**Journey-Schlichtung**

Derzeit werden für die Journey-Schlichtung nur Journeys für Zielgruppen nur mit Lesezugriff unterstützt. Schlichtungseinstellungen können nicht für einheitliche Journeys oder Journeys mit Zielgruppenqualifizierung genutzt werden.
