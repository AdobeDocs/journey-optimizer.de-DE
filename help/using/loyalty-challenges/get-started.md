---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Herausforderungen im Zusammenhang mit Treueprogrammen erstellen und verwalten können, um ansprechende, lohnende Treueprogramme zu erstellen.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
source-git-commit: 0769c486386ce27079244a3ff36cdd2fedf27214
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 15%

---

# Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

**[Erste Schritte mit den Herausforderungen im Zusammenhang mit](get-started.md)**◀︎ **Sie sind hier**

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Herausforderungen erstellen und verwalten**

* [Zugriff und Verwaltung von Herausforderungen und Aufgaben](access-loyalty-challenges.md)
* [Herausforderungen schaffen](create-challenges.md)
* [Aufgaben erstellen](create-tasks.md)
* [Überwachen der Leistung beim Treueprogramm](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Konfigurieren und Integrieren**

<!-- * [Configure loyalty challenges](loyalty-admin.md) -->
* [Treuedaten und -datensätze](loyalty-data-and-datasets.md)
* [API-Referenz für Herausforderungen im Treueprogramm](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **privaten Betaversion**. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](../rn/releases.md).

## Überblick {#overview}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="Treue-Challenges"
>abstract="Mit Treue-Challenges können Sie ansprechende, spielerisch gestaltete Treueprogramme entwickeln, die das Kundenverhalten positiv beeinflussen und die Markenbindung stärken. Entwickeln Sie Challenges, bei denen Kundinnen und Kunden Prämien für bestimmte Aktionen erhalten – von Einkäufen über das Verfassen von Rezensionen bis hin zu Interaktionen in Social Media und der Weiterempfehlung an Freundinnen und Freunde."

Mit Treue-Challenges können Sie ansprechende, spielerisch gestaltete Treueprogramme entwickeln, die das Kundenverhalten positiv beeinflussen und die Markenbindung stärken. Entwickeln Sie Challenges, bei denen Kundinnen und Kunden Prämien für bestimmte Aktionen erhalten – von Einkäufen über das Verfassen von Rezensionen bis hin zu Interaktionen in Social Media und der Weiterempfehlung an Freundinnen und Freunde.

Herausforderungen im Zusammenhang mit der Kundentreue bieten Ihnen folgende Möglichkeiten:

* **Entwerfen Sie flexible**: Erstellen Sie Standard-, Streak- oder sequenzielle Herausforderungen, um Ihre Geschäftsziele zu erreichen
* **Prämien strategisch konfigurieren**: Punkte an Aufgaben-Meilensteinen oder nach vollständigem Abschluss liefern, um die Interaktion aufrechtzuerhalten
* **Personalisieren des Erlebnisses**: Verwenden Sie Inhaltskarten und Multi-Channel-Messaging, um beeindruckende Markenerlebnisse zu schaffen
* **Nahtlose Integration**: Verbinden Sie sich mit Ihren bestehenden Treueanbietern und nutzen Sie Experience Platform-Daten
* **Automatisch nachverfolgen**: Überwachen des Kundenfortschritts über automatisch generierte Journey ohne benutzerdefinierte Entwicklung
* **Leistung messen**: Verwenden Sie integrierte Reporting-Dashboards, um Programm-KPIs, Challenge-Ergebnisse und Metriken auf Aufgabenebene zu verfolgen

![](assets/challenges-gs.png)

Sie können die folgenden Arten von Challenge-Erlebnissen erstellen:

* **Standardherausforderungen**: Kunden führen eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus. Verwenden Sie diesen Typ, wenn Sie Flexibilität und mehrere Pfade zum Abschluss wünschen.\
  *Beispiel: „Summer Wellness Challenge“ - 3 von 5 Aufgaben erledigen: Gesundheitsprodukte kaufen, in den sozialen Medien teilen, einen Freund verweisen, eine Bewertung schreiben oder an einer virtuellen Veranstaltung teilnehmen*

* **Streak Challenges**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus. Verwenden Sie diesen Typ, um im Laufe der Zeit ein konsistentes, wiederholtes Verhalten zu fördern.\
  *Beispiel: „Coffee Lover&#39;s Week“ - Kaufen Sie Kaffeeprodukte für 7 aufeinander folgende Tage, um eine Belohnung für kostenlose Getränke zu erschließen*

* **Sequenzielle Herausforderungen**: Kunden führen Aufgaben in einer definierten Reihenfolge aus. Verwenden Sie diesen Typ, um Kunden durch einen bestimmten Journey- oder Onboarding-Prozess zu führen.\
  *Beispiel: „New Member Journey&quot; - Melden Sie sich für E-Mails an → tätigen Sie Ihren ersten Kauf → schreiben Sie eine Produktbewertung → Empfehlen Sie einem Freund (in dieser exakten Bestellung vollständig)*

* **Bringen Sie Ihre eigenen Datenherausforderungen** (eingeschränkte Verfügbarkeit): Das Challenge-Framework (Aufgaben und Belohnungen) wird aus Ihrer Datenintegration für die Treueprogramm-Herausforderungen zusammengestellt. Sie konfigurieren Inhalt, Messaging und Zielgruppe so, wie Sie es für jeden anderen Herausforderungstyp tun würden.

## Funktionsweise {#how-it-works}

Dieser Workflow ermöglicht das Erstellen und Starten einer Herausforderung zum Treueprogramm:

1. **Herausforderung erstellen** - Definiert die grundlegenden Challenge-Eigenschaften, einschließlich Name, Typ (Standard, Streak, Sequential oder Bring Your Own Data, falls verfügbar) und Datumsbereich. [Erfahren Sie, wie Sie einen Challenge-Typ &#x200B;](create-challenges.md#create-the-challenge).

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

<!--

+++Configure the loyalty program (administrators)

To configure **[!UICONTROL Loyalty Admin]** (reward providers, event definitions, and global settings), you need administrator access to your Journey Optimizer organization. Marketers who only create challenges do not need access to this area. [Learn how to configure the loyalty program](loyalty-admin.md).

Contact your administrator if **[!UICONTROL Loyalty Admin]** is not visible in the left navigation.

+++

-->

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
    <a href="access-loyalty-challenges.md"><strong>Zugreifen auf und Verwalten von Challenges und Aufgaben</strong></a>
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
    <a href="create-challenges.md"><strong>Erstellen von Challenges</strong></a>
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
    <a href="create-tasks.md"><strong>Erstellen von Aufgaben</strong></a>
    </div>
    <p>
    <em>Erfahren Sie, wie Sie Aufgaben definieren, die Kundinnen und Kunden für Herausforderungen ausführen müssen</em>
    </p>
  </td>
  <td>
    <a href="loyalty-reporting.md">
      <img alt="Berichte" src="assets/do-not-localize/icon-reporting.png" width="200"/>
    </a>
    <div>
    <a href="loyalty-reporting.md"><strong>Überwachen der Performance</strong></a>
    </div>
    <p>
    <em>Verfolgen Sie Programm-KPIs, Challenge-Ergebnisse und Aufgabenmetriken mit integrierten Dashboards</em>
    </p>
  </td>
  &lt;!--

<td>
    <a href="loyalty-admin.md">
      <img alt="Konfiguration" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="loyalty-admin.md"><strong>Konfigurieren des Treueprogramms</strong></a>
    </div>
    <p>
    <em>Richten Sie Belohnungsanbieter, Ereignisdefinitionen und Organisationseinstellungen für die Erfüllung ein</em>
    </p>
  </td>

-->
</tr>
</table>

## API-Referenz {#api-reference}

Um Herausforderungen im Zusammenhang mit der Treue programmgesteuert zu verwalten, verwenden Sie die [API für Herausforderungen im Zusammenhang mit der Treue](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}. Mit der -API können Sie über REST-Endpunkte Herausforderungen und Aufgaben erstellen, aktualisieren und verwalten.
