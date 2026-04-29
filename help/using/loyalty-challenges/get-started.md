---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue
description: Learn how to create and manage loyalty challenges in Adobe Journey Optimizer to build engaging loyalty programs.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 4%

---

# Get started with loyalty challenges {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* **Get started with Loyalty Challenges** ◀︎ **You are here**
* [Zugriff und Verwaltung von Herausforderungen und Aufgaben](access-loyalty-challenges.md)
* [Herausforderungen schaffen](create-challenges.md)
* [Aufgaben erstellen](create-tasks.md)
* [API-Referenz für Herausforderungen im Treueprogramm](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **privaten Betaversion**. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](../rn/releases.md).

## Überblick {#overview}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="Treue-Challenges"
>abstract="Loyalty Challenges enable you to create engaging, gamified loyalty programs that drive customer behavior and deepen brand relationships. Build challenges that reward customers for specific actions—from making purchases and writing reviews to engaging on social media and referring friends."

Loyalty Challenges enable you to create engaging, gamified loyalty programs that drive customer behavior and deepen brand relationships. Build challenges that reward customers for specific actions—from making purchases and writing reviews to engaging on social media and referring friends.

With Loyalty Challenges, you can:

* **Design flexible challenge types**: Create Standard, Streak, or Sequential challenges to match your business goals
* **Configure rewards strategically**: Deliver points at task milestones or upon full completion to maintain engagement
* **Personalize the experience**: Use content cards and multi-channel messaging to create immersive, branded experiences
* **Integrate seamlessly**: Connect with your existing loyalty providers and leverage Experience Platform data
* **Track automatically**: Monitor customer progress through auto-generated journeys without custom development

![](assets/challenges-gs.png)

You can create three types of challenge experiences:

* **Standard challenges**: Customers complete any specified number of tasks in any order. Use this type when you want flexibility and multiple paths to completion.\
  *Beispiel: „Summer Wellness Challenge“ - 3 von 5 Aufgaben erledigen: Gesundheitsprodukte kaufen, in den sozialen Medien teilen, einen Freund verweisen, eine Bewertung schreiben oder an einer virtuellen Veranstaltung teilnehmen*

* **Streak Challenges**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus. Verwenden Sie diesen Typ, um im Laufe der Zeit ein konsistentes, wiederholtes Verhalten zu fördern.\
  *Beispiel: „Coffee Lover&#39;s Week“ - Kaufen Sie Kaffeeprodukte für 7 aufeinander folgende Tage, um eine Belohnung für kostenlose Getränke zu erschließen*

* **Sequenzielle Herausforderungen**: Kunden führen Aufgaben in einer definierten Reihenfolge aus. Verwenden Sie diesen Typ, um Kunden durch einen bestimmten Journey- oder Onboarding-Prozess zu führen.\
  *Beispiel: „New Member Journey&quot; - Melden Sie sich für E-Mails an → tätigen Sie Ihren ersten Kauf → schreiben Sie eine Produktbewertung → Empfehlen Sie einem Freund (in dieser exakten Bestellung vollständig)*

## Funktionsweise {#how-it-works}

Dieser Workflow ermöglicht das Erstellen und Starten einer Herausforderung zum Treueprogramm:

1. **Herausforderung erstellen** - Definiert die grundlegenden Eigenschaften der Herausforderung, einschließlich Name, Typ (Standard, Streak oder Sequenziell) und Datumsbereich.

1. **Aufgaben hinzufügen** - Definiert die spezifischen Aktionen, die Kunden durchführen müssen, einschließlich Aufgabentypen (Kauf, Ausgaben), Mengen, Produktfiltern und Belohnungen.

1. **Erstellen von Inhaltskarten** - Erstellen Sie die visuelle Darstellung Ihrer Challenge mit Journey Optimizer-Inhaltskarten, die auf Kundengeräten angezeigt werden. Inhaltskarten zeigen Informationen zu Herausforderungen, Fortschritt und Belohnungen an.

1. **Messaging konfigurieren** (optional) - Richten Sie Multi-Channel-Nachrichten (In-App, E-Mail, Push) für die wichtigsten Lebenszyklusphasen ein: Start, in Bearbeitung und Abschluss.

1. **Ziel-Audience auswählen** - Definieren Sie, welche Kunden an Ihrer Challenge teilnehmen können, indem Sie eine Audience aus Adobe Experience Platform auswählen.

1. **Challenge starten** - Veröffentlichen Sie die Challenge und generieren Sie dann eine Journey. Journey Optimizer erstellt automatisch die Journey für Ihre Challenge. Veröffentlichen Sie die automatisch generierte Journey, um die Challenge für Kunden verfügbar zu machen.

Detaillierte schrittweise Anweisungen finden Sie unter [Erstellen von Herausforderungen](create-challenges.md).

## Voraussetzungen {#prerequisites}

Bevor Sie Herausforderungen im Zusammenhang mit dem Treueprogramm nutzen, stellen Sie Folgendes sicher:

+++Erforderliche Berechtigungen

Um Herausforderungen im Zusammenhang mit der Treue nutzen zu können, benötigen Sie in Journey Optimizer und Adobe Experience Platform die entsprechenden Berechtigungen.

**Journey Optimizer:**

* `journeys.read`
* `journeys.write`
* `journeys.delete`
* `journeys.publish`
* `journeys_events.read`
* `journeys_events.write`
* `journeys_events.delete`
* `journeys_report.read`
* `messages.read`
* `messages_report.read`

**Adobe Experience Platform:**

* `segments.read`
* `profiles.read`
* `identity_namespace.read`

Wenden Sie sich an Ihren Administrator, wenn Sie die Funktion nicht nutzen können oder zusätzliche Berechtigungen benötigen.

+++

+++Zielgruppe

Stellen Sie sicher, dass die benötigte Zielgruppe in Adobe Experience Platform vorhanden ist, bevor Sie eine Challenge erstellen. Bei der Konfiguration der Challenge wählen Sie die Audience aus, die definiert, welche Kunden zur Teilnahme berechtigt sind. [Erfahren Sie, wie Sie mit Audiences arbeiten](../audience/about-audiences.md).

+++

## Tauchen wir tiefer in die Materie ein {#lets-dive-deeper}

Jetzt, da Sie wissen, was Herausforderungen im Zusammenhang mit der Treue sind und wie sie funktionieren, ist es an der Zeit, sich näher mit den Details zu befassen. Erkunden Sie die folgenden Themen, um auf die Benutzeroberfläche zuzugreifen, Ihre erste Herausforderung zu erstellen und die Aufgaben zu definieren, die Ihre Kunden abschließen werden.

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="Zugriff" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Zugriff und Verwaltung von Herausforderungen und Aufgaben</strong></a>
    </div>
    <p>
    <em>Erfahren Sie, wie Sie auf das Inventar zugreifen und Herausforderungen und Aufgaben verwalten können</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="Erstellen" src="assets/do-not-localize/icon-challenge.png" width="200"/>
    </a>
    <div>
    <a href="create-challenges.md"><strong>Herausforderungen schaffen</strong></a>
    </div>
    <p>
    <em>Erfahren Sie, wie Sie Ihre erste Herausforderung bezüglich der Treue aufbauen und konfigurieren</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
      <img alt="Aufgaben" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>Aufgaben erstellen</strong></a>
    </div>
    <p>
    <em>Erfahren Sie, wie Sie Aufgaben definieren, die Kundinnen und Kunden für Herausforderungen ausführen müssen</em>
    </p>
  </td>
</tr>
</table>

## API-Referenz {#api-reference}

Um Herausforderungen im Zusammenhang mit der Treue programmgesteuert zu verwalten, verwenden Sie die [API für Herausforderungen im Zusammenhang mit der Treue](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}. Mit der -API können Sie über REST-Endpunkte Herausforderungen und Aufgaben erstellen, aktualisieren und verwalten.
