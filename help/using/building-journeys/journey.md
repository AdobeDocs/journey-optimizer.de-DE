---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Journeys
description: Erste Schritte mit Journeys
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: Journey, Entdecken, erste Schritte
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: cfac40f73a68362f8490de28cf1865f3dd4952f7
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 31%

---


# Erste Schritte mit Journeys{#jo-general-principle}

Mit Journeys in Adobe Journey Optimizer können Sie personalisierte, mehrstufige Customer Journeys erstellen, die sich in Echtzeit an das Verhalten und die Bedürfnisse Ihrer Zielgruppe anpassen. Mithilfe einer intuitiven Drag-and-Drop-Arbeitsfläche können Sie Nachrichten und Aktionen über mehrere Kanäle hinweg orchestrieren und dabei kontextuelle Daten und Zielgruppen-Targeting nutzen, um maximale Wirkung zu erzielen. Unabhängig davon, ob Sie Echtzeit-Trigger untersuchen, Journey-Eigenschaften verwalten oder erweiterte Tools wie benutzerdefinierte Aktionen und Ausdrücke verwenden, bietet dieser Abschnitt eine klare Roadmap, mit der Sie Journey entwerfen und verfeinern können, die aussagekräftige, zeitnahe Kundenerlebnisse bereitstellen.

Verwenden Sie [!DNL Journey Optimizer], um Anwendungsfälle für die Echtzeit-Orchestrierung mithilfe von in Ereignissen oder Datenquellen gespeicherten kontextuellen Daten zu erstellen. Sie können mehrstufige fortgeschrittene Szenarien mit den folgenden Funktionen entwerfen:

* Versand in Echtzeit **unitärer Versand** ausgelöst durch den Empfang eines [Ereignisses](general-events.md) oder **im Batch** mithilfe von Adobe Experience Platform [Audiences](read-audience.md).

* Nutzen **(kontextuelle**) aus [Ereignissen](../event/about-events.md) Informationen aus Adobe Experience Platform oder Daten aus API-Services von Drittanbietern über [Datenquellen](../datasource/about-data-sources.md).

* Verwenden Sie die **[integrierten Aktionen](journeys-message.md)** zum Senden von in [!DNL Journey Optimizer] entworfenen Nachrichten oder erstellen Sie **[benutzerspezifische Aktionen](using-custom-actions.md)**, wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden.

* Erstellen Sie mit dem **[Journey-Designer](using-the-journey-designer.md)** Ihre mehrstufigen Anwendungsfälle: Ziehen Sie einfach per Drag-and-Drop ein Eintrittsereignis oder eine [Aktivität zum Lesen von Zielgruppen](read-audience.md) hinzu, fügen Sie [Bedingungen](condition-activity.md) hinzu und senden Sie personalisierte Nachrichten.

Der Journey Optimizer [Journey-Designer](using-the-journey-designer.md) bietet alles, was Marketer und Journey-Anwender benötigen, um mehrstufige 1:1-Journey kanalübergreifend zu orchestrieren. Dazu gehört eine intuitive Drag-and-Drop-Arbeitsfläche, um jeden Schritt des Journey zu orchestrieren, die Zielgruppe zu definieren und die Nachrichten, Angebote und Inhalte über alle Kanäle hinweg einzuschließen, die die Mitglieder der Zielgruppe basierend auf ihrem Verhalten, kontextuellen Daten und Geschäftsereignissen sehen werden. Erkunden Sie [Anwendungsfälle aus der Praxis](jo-use-cases.md) um zu sehen, wie Sie diese Funktionen anwenden können.

➡️ [Journey Optimizer entdecken (Video)](#video)

## Überblick über Journeys

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Erste Schritte bei der Erstellung von Journey

Schrittweise Anleitungen zum Entwerfen, Testen, Veröffentlichen und Tracking von Customer Journeys zum Erstellen personalisierter Omni-Channel-Kampagnen.

[Erstellen Ihrer ersten Journey](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Journey Orchestration - Vollständiges Handbuch

Umfassende Dokumentation zu allen Aspekten der Erstellung, Verwaltung und Optimierung von Journey in Adobe Journey Optimizer.

[Erkunden des vollständigen Handbuchs](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Verwalten von Journey

Verwalten Sie Customer Journeys effizient mit Tools für Filterung, Profilverwaltung, Zeitzonen und Optimierungstechniken.

[Informationen zum Journey-Management](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

Journey-Aktivitäten

Entdecken Sie, wie Sie Aktivitäten wie Trigger, Entscheidungsschritte, Zielgruppen-Management und personalisiertes Messaging in Journeys konfigurieren und verwenden.

[Aktivitäten erkunden](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Erstellen von Ausdrücken

Meistern Sie die Erstellung von Ausdrücken für dynamische Workflows, Datenmanipulation und erweiterte Journey-Orchestrierung mit leistungsstarken Tools und Syntax.

[Mehr zu Ausdrücken](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Journey-Anwendungsfälle

Erkunden Sie die realen Anwendungen von Adobe Journey Optimizer, einschließlich Multi-Channel-Messaging und Integration mit externen Systemen.

[Anwendungsfälle entdecken](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Was kannst du mit Journey machen?

Vom Journey-Designer aus können Marketing-Fachleute in Echtzeit ausgelöste 1:1-Nachrichten über jeden Kanal senden, wenn ein Ereignis auftritt. Wenn Kundinnen oder Kunden beispielsweise einen Service abonnieren, kann dies [das Versenden einer Begrüßungs-E-Mail auslösen](message-to-subscribers-uc.md), in der sie aufgefordert werden, sich zum ersten Mal bei der App anzumelden und ihre Voreinstellungen festzulegen. Aktionen wie der Abschluss des Kaufs, das Öffnen der E-Mail und die Anmeldung bei der App können verwendet werden, damit neue Kundinnen und Kunden in ihrer Journey fortfahren.

## Journey-Typen

Adobe Journey Optimizer unterstützt vier Journey-Typen, die jeweils für verschiedene Anwendungsfälle und Eingabemechanismen entwickelt wurden. Wählen Sie den richtigen Typ aus, je nachdem, wie Profile in Ihre Kundenerlebnisse eintreten und wie sie sich entwickeln sollen.

>[!BEGINTABS]

>[!TAB Unitäre Journey]

**Unitäre Journey** werden einzeln durch ein Ereignis ausgelöst, wenn eine bestimmte Aktion auftritt, z. B. ein Kauf, eine App-Anmeldung oder eine Formularübermittlung. Profile wechseln in Echtzeit zum Zeitpunkt des Eingangs des Ereignisses nacheinander auf den Journey. Dies ist ideal für personalisierte, verhaltensgesteuerte Erlebnisse.

**Wichtigste Merkmale:**

* Ereignisgesteuerter Eintritt in Echtzeit
* Individuelle Profilverarbeitung
* Perfekt für Transaktionsnachrichten und sofortige Antworten
* Unterstützt kontextuelle Daten aus dem auslösenden Ereignis

**Anwendungsfälle:**

* Bestellbestätigung nach dem Kauf
* Willkommens-E-Mail, wenn sich jemand anmeldet
* Warenkorbabbruch, ausgelöst durch das Browser-Verhalten
* Benachrichtigungen zum Zurücksetzen des Kennworts

➡️ [Erfahren Sie mehr über die Ereigniskonfiguration](../event/about-events.md) | [Allgemeine Ereignisse](general-events.md) | [Anwendungsfall „Nachricht an Abonnenten“](message-to-subscribers-uc.md)

>[!TAB Audience-Journey lesen]

**Zielgruppen-Journey lesen** Beginnen Sie mit einer Zielgruppe aus Adobe Experience Platform und senden Sie Nachrichten im Batch an alle Profile in dieser Zielgruppe. Dieser Journey-Typ verarbeitet die gesamte Zielgruppe gleichzeitig und ist daher ideal für geplante Kampagnen und wiederkehrende Kommunikation.

**Wichtigste Merkmale:**

* Batch-Verarbeitung von Zielgruppensegmenten
* Geplante oder einmalige Ausführung
* Alle Profile treten gleichzeitig ein
* Unterstützt Kommunikation in großem Maßstab

**Anwendungsfälle:**

* Monatliche Newsletter
* Werbekampagnen für bestimmte Segmente
* Produktankündigungen an alle Kunden
* Saisonale Marketing-Kampagnen

➡️ [Erfahren Sie mehr über die Aktivität „Zielgruppe lesen“](read-audience.md) | [Erste Schritte mit Audiences](../audience/about-audiences.md) | [Anwendungsfall für Multi-Channel-Messaging](journeys-uc.md)

>[!TAB Journey zur Zielgruppenqualifizierung]

**Zielgruppen-Qualifizierungs-Journey** werden ausgelöst, wenn Profile sich für ein bestimmtes Zielgruppensegment qualifizieren (oder daraus austreten). Profile gelangen in Echtzeit individuell auf die Journey, da sie die Zielgruppenkriterien erfüllen, was eine sofortige Interaktion ermöglicht, wenn sich das Kundenverhalten ändert.

**Wichtigste Merkmale:**

* Qualifizierungsbasierte Echtzeit-Eingabe
* Kontinuierliche Überwachung der Zielgruppenzugehörigkeit
* Individuelle Profilverarbeitung nach Qualifizierung
* Am besten geeignet für Streaming-Zielgruppen

**Anwendungsfälle:**

* Benachrichtigungen zu VIP-Stufen-Upgrades
* Erneute Interaktion von Kundinnen und Kunden, wenn sie inaktiv werden
* Nachrichten zum Erstkauf
* Geografisches Targeting beim Umzug von Kunden

➡️ [Informationen zur Zielgruppen-Qualifizierung](audience-qualification-events.md) | [Bedingungsaktivität](condition-activity.md) | [Erstellen von Segmentdefinitionen](../audience/creating-a-segment-definition.md)

>[!TAB Journey für Geschäftsereignisse]

**Geschäftsereignis-Journey** werden durch Geschäftsereignisse ausgelöst (z. B. Lageraktualisierungen, Wetterwarnungen oder Preisänderungen), die sich auf mehrere Profile gleichzeitig auswirken. Diese Journey reagieren nicht auf individuelle Kundenaktionen, sondern auf umfassendere Geschäftsbedingungen oder externe Faktoren.

**Wichtigste Merkmale:**

* Wird durch Ereignisse auf Unternehmensebene ausgelöst, nicht durch einzelne Aktionen
* Wirkt sich auf mehrere Profile gleichzeitig aus
* Targeting einer bestimmten Zielgruppe, wenn das Ereignis auftritt
* Kombiniert ereignisgesteuertes Timing mit Audience-Targeting

**Anwendungsfälle:**

* Warnungen bei geringem Bestand für interessierte Kunden
* Flash-Verkaufsankündigungen
* Wetterbasierte Angebote
* Benachrichtigungen über Preisnachlässe
* Warnhinweise für das Produkt-Backin-Lager

➡️ [Erfahren Sie mehr über Geschäftsereignisse](general-events.md) | [Geschäftsereignisse konfigurieren](../event/about-creating-business.md) | [Zutrittsverwaltung](entry-management.md)

>[!ENDTABS]

## Journey Designer{#journey-designer}

Der [Journey-Designer](using-the-journey-designer.md) ist eine intuitive Drag-and-Drop-Arbeitsfläche, mit der Sie Ihre Kunden-Journey visuell erstellen und orchestrieren können. Es bietet alles, was Sie zum Entwerfen mehrstufiger Erlebnisse benötigen:

* **[Integrierte Kanalaktionen](journeys-message.md)** - Senden von Nachrichten per E-Mail, Push-Benachrichtigungen, SMS/MMS, In-App-, Web- und Code-basierten Erlebnissen und mehr, alles direkt in Journey Optimizer
* **[Benutzerdefinierte Aktionen](using-custom-actions.md)** - Integrieren von Drittanbietersystemen zum Senden von Nachrichten oder Trigger-Workflows in externen Plattformen
* **[Orchestrierungsaktivitäten](about-journey-activities.md)** - Logik, Bedingungen, Wartezeiten und Audience-Targeting hinzufügen, um anspruchsvolle Kundenerlebnisse zu erstellen
* **[Bedingungen](condition-activity.md)** Verzweigen Sie Ihren Journey anhand von Profilattributen, Zielgruppenzugehörigkeiten oder Echtzeit-Ereignissen.
* **[Ausdrücke](expression/expressionadvanced.md)** - Erweiterte Logik und Personalisierung mit dem Ausdruckseditor erstellen

Erfahren Sie, wie Sie den Journey-[&#x200B; verwenden (in diesen End-to-End-Anwendungsfällen](jo-use-cases.md).

>[!NOTE]
>
>Leitlinien und Einschränkungen für Journeys werden auf [dieser Seite](../start/guardrails.md) beschrieben.

## Anleitungsvideo {#video}

Entdecken Sie die Komponenten einer Journey und lernen Sie die Grundlagen des Erstellens einer Journey auf der Arbeitsfläche kennen.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

## Weitere Ressourcen {#additional-resources}

* **[Fehlerbehebung bei Kunden-Journey](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnostizieren und beheben Sie Journey-Ausführungsprobleme mit Tools, Fehlercodes und Best Practices für Debugging und Optimierung
* **[Häufig gestellte Fragen zu Journeys](journey-faq.md)** – Häufig gestellte Fragen zu Journeys
* **[Journey-Warnhinweise](../reports/alerts.md)** - Einrichten von Warnhinweisen für die Journey-Überwachung und Abonnieren von Benachrichtigungen für Echtzeit-Updates
* **[Referenz zu Fehler-Codes](error-codes-reference.md)** – Journey-Fehler-Codes und Schritte zur Fehlerbehebung
* **[Fehlerbehebung](troubleshooting.md)** – Häufige Probleme mit Journeys und deren Lösungen
* **[Journey-Tutorials (Videos)](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - Lernen Sie das Journey-Erstellen durch praktische Video-Tutorials, die Funktionen, Merkmale und Best Practices behandeln
