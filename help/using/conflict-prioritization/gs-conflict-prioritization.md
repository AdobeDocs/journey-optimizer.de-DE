---
title: Konflikt-Management und Priorisierung
description: Erfahren Sie, wie Sie die Tools für Konflikt-Management und Priorisierung in Journey Optimizer nutzen können.
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: dbe312f332031391c49a973f323994f860e354e3
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 51%

---

# Konflikt-Management und Priorisierung {#conflict-prioritization}

>[!AVAILABILITY]
>
>Die Funktionen für Konflikte und Priorisierung stehen derzeit einer ausgewählten Kundengruppe nur eingeschränkt zur Verfügung. Sie werden in Zukunft schrittweise für weitere Benutzende eingeführt. Wenden Sie sich an Ihr Accountteam, wenn Sie auf die Warteliste für diese Funktionen gesetzt werden möchten.

In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet mehrere Tools zum Konflikt-Management und zur Priorisierung.

## Tools für Konfliktmanagement und Priorisierung {#tools}

Mit dem **Konflikterkennungs-Tool** können Sie potenzielle Überschneidungen in Journeys und Kampagnen identifizieren. Dies ist von entscheidender Bedeutung, da zu viele gleichzeitige Mitteilungen zu Kundenermüdung führen können. Mit Journey Optimizer können Sie Elemente wie Timelines, Zielgruppenüberschneidungen und Kanalkonfigurationen überwachen. Durch das frühzeitige Identifizieren von Konflikten können Sie Ihre Kampagnen verfeinern und verhindern, dass Kundinnen und Kunden mehrere Nachrichten gleichzeitig erhalten. [Informationen zum Erkennen potenzieller Konflikte in Journeys und Kampagnen](conflicts.md)

Darüber hinaus können Sie mit den **Prioritätswerten** steuern, welche Kampagnen oder Journeys Vorrang haben, wenn sich eine Kundin oder ein Kunde für mehrere Mitteilungen qualifiziert. Dies ist insbesondere bei eingehenden Kanälen wie Web und Mobile nützlich, in denen immer nur eine Kampagne angezeigt werden kann. Durch Zuweisung eines Prioritätswertes zu jeder Journey oder Kampagne können Sie sicherstellen, dass die wichtigste Nachricht zuerst gesendet wird. [Informationen zum Zuweisen von Prioritätswerten zu Journeys und Kampagnen](priority-scores.md)

**Journey-Begrenzung und Schlichtung** Ermöglicht es Ihnen zu begrenzen, wie oft und wie viele Journey ein Kunde innerhalb eines bestimmten Zeitraums eingeben kann. Sie können Regeln einrichten, um die Anzahl der Journey-Eintritte für ein Profil zu begrenzen oder die Anzahl der Journeys zu begrenzen, an denen eine Kundin bzw. ein Kunde gleichzeitig teilnehmen kann. Darüber hinaus können Sie mithilfe von Steuerungseinstellungen festlegen, in welche Journey eine Kundin bzw. ein Kunde eintreten soll, wenn sie bzw. er sich für mehrere Journeys qualifiziert, und mithilfe von Prioritätswerten die beste Wahl bestimmen. [Informationen zum Arbeiten mit Journey-Begrenzungen und -Steuerung](journey-capping.md)

Schließlich können Sie auch Regelsätze verwenden, um die **Frequenzlimitierung nach Kommunikationstyp“ (z. B.**, Vertrieb, Werbeaktionen) festzulegen, um zu verhindern, dass Kunden mit ähnlichen Nachrichten überlastet werden. Sie können die Häufigkeit über mehrere Kanäle steuern und zu oft angesprochene Profile automatisch ausschließen, um ein besseres Kundenerlebnis zu gewährleisten. [Informationen zum Arbeiten mit Regelsätzen](../configuration/rule-sets.md)</li></ul>

Mithilfe dieser Funktionen können Sie reibungslosere und zielgerichtetere Marketing-Maßnahmen gewährleisten und gleichzeitig die richtige Nachricht zur richtigen Zeit senden, wodurch Konflikte und Überlastungen vermieden werden.

## Leitlinien und Einschränkungen

**Frequenzlimitierung und Batch-Zielgruppen**

Bei der Frequenzlimitierung sowohl für den Kanal als auch für das Journey wird, wenn es sich bei der verwendeten Zielgruppe um eine Batch-Zielgruppe handelt, der Profilzählerwert, auf den zum Zeitpunkt des Eintritts in die Journey verwiesen wird, oder die Nachrichtenlaufzeit für eine Kanalkommunikation aus dem täglichen Schnappschuss entnommen.

Dies kann problematisch sein, da Kunden die Frequenzlimitierung überschreiten können, wenn sie eine andere Journey eingegeben oder eine andere Kommunikation zwischen dem Zeitpunkt des täglichen Schnappschusses und dem Zeitpunkt der Eingabe der Journey (oder der zugestellten Nachricht) erhalten haben.

**Frequenzlimitierung und Streaming-Zielgruppen**

Bei Streaming-Zielgruppen kann es bis zu 2 Stunden dauern, bis das System einen aktualisierten Zählerwert erkennt. Daher empfehlen wir, Kommunikationen und Journey mit einem Abstand von mindestens 2 Stunden zu präsentieren, um dieses Risiko zu minimieren.

**Startzeit der Journey**

Um sicherzustellen, dass die Funktionen für das Konfliktmanagement und die Priorisierung ordnungsgemäß funktionieren, empfehlen wir, die Startzeit Ihrer Journey mindestens 10 Minuten in die Zukunft zu setzen, damit das System den Zähler entsprechend aktualisieren kann.

Wenn Kunden ihre Obergrenze bereits beim Betreten einer Journey erreicht haben, wird ihnen zwar der Einstiegszähler nicht erhöht, aber wenn sie ihre Obergrenze nicht erreicht haben.

**Journey-Schlichtung**

Derzeit werden für die Journey-Schlichtung nur Journey mit Lesezugriff auf Zielgruppen unterstützt. Schlichtungseinstellungen können nicht für Journey mit unitärer oder Zielgruppen-Qualifizierung genutzt werden.
