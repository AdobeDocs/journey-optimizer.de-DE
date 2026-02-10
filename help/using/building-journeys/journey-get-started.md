---
solution: Journey Optimizer
product: journey optimizer
title: Vollständiges Handbuch zur Journey-Orchestrierung
description: Umfassendes Handbuch für die ersten Schritte mit der Journey-Orchestrierung in [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
keywords: Journey, Orchestrierung, Erste Schritte, Onboarding, Funktionen
exl-id: 96b1d619-986d-493d-a73b-d7c63b92cca8
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 93%

---

# Vollständiges Handbuch zur Journey-Orchestrierung{#journey-orchestration-guide}

Journey in [!DNL Adobe Journey Optimizer] ermöglichen es Ihnen, personalisierte, mehrstufige Kunden-Journey zu erstellen, die sich in Echtzeit an das Verhalten und die Bedürfnisse Ihrer Zielgruppe anpassen. Mithilfe einer intuitiven Drag-and-Drop-Arbeitsfläche können Sie Nachrichten und Aktionen über mehrere Kanäle hinweg orchestrieren und dabei kontextuelle Daten und Zielgruppen-Targeting nutzen, um maximale Wirkung zu erzielen.

Unabhängig davon, ob Sie Echtzeit-Trigger untersuchen, Journey-Eigenschaften verwalten oder erweiterte Tools wie benutzerdefinierte Aktionen und Ausdrücke verwenden, bietet dieses Handbuch eine klare Roadmap für die souveräne Gestaltung und Verfeinerung von Journeys, die aussagekräftige, zeitnahe Kundenerlebnisse bereitstellen.

## Was sind Journeys?

Verwenden Sie [!DNL Journey Optimizer], um Anwendungsfälle für die Echtzeit-Orchestrierung mithilfe von in Ereignissen oder Datenquellen gespeicherten kontextuellen Daten zu erstellen. Entwickeln Sie mehrstufige erweiterte Szenarien, die in Echtzeit auf Kundenverhalten und Geschäftsereignisse reagieren.

Der Journey-Designer von Journey Optimizer bietet alles, was Marketing-Fachleute und Journey-Anwendende benötigen, um mehrstufige 1:1-Journeys kanalübergreifend zu orchestrieren. Dazu gehört eine intuitive Drag-and-Drop-Arbeitsfläche zum Orchestrieren aller Schritte der Journey, Definieren der Zielgruppe und kanalübergreifendem Einschließen der Nachrichten, Angebote und Inhalte, die die Mitglieder der Zielgruppe basierend auf ihrem Verhalten, kontextuellen Daten und Geschäftsereignissen zu sehen bekommen.

![Benutzeroberfläche des Journey-Designers mit Palette, Arbeitsfläche und Eigenschaftenbereich](assets/journey38.png)

**Bereit, mit dem Erstellen zu beginnen?** Weitere Informationen zum Erstellen und Entwerfen Ihrer ersten Journey finden Sie [auf dieser Seite](journey-gs.md).


## Wichtigste Funktionen {#capabilities}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=de)

**Echtzeit- und Batch-Versand**

Versand in Echtzeit **Einzelversand** ausgelöst durch den Empfang eines Ereignisses, oder **im Batch** unter Verwendung [!DNL Adobe Experience Platform] Zielgruppen.

[Weitere Informationen zum Eintritt in Journeys](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=de)

**Kontextuelle Daten**

Nutzen Sie **kontextuelle Daten** aus Ereignissen, Informationen aus [!DNL Adobe Experience Platform] oder Daten aus API-Services von Drittanbietern.

[Arbeiten mit Datenquellen](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=de)

**Integrierte Aktionen**

Verwenden Sie **integrierte Kanalaktionen**, um in [!DNL Journey Optimizer] entworfene Nachrichten per E-Mail, Push, SMS/MMS und mehr zu senden.

[Senden von Nachrichten in Journeys](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=de)

**Benutzerdefinierte Aktionen**

Erstellen Sie **benutzerdefinierte Aktionen**, wenn Sie ein Drittanbietersystem zum Senden Ihrer Nachrichten oder zum Verbinden mit externen APIs verwenden.

[Konfigurieren benutzerdefinierter Aktionen](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=de)

**Grafischer Journey-Designer**

Erstellen Sie mit dem **Journey-Designer** mehrstufige Anwendungsfälle: Ziehen Sie einfach per Drag-and-Drop ein Eintrittsereignis oder eine Aktivität vom Typ „Zielgruppe lesen“ in die Benutzeroberfläche, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

[Kennenlernen des Journey-Designers](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=de)

**Testen und Optimieren**

Testen Sie Ihre Journeys vor der Veröffentlichung, überwachen Sie deren Leistung und optimieren Sie den Versand mit erweiterten Funktionen wie der Versandzeitoptimierung.

[Testen und Veröffentlichen von Journeys](testing-the-journey.md)
:::

::::

## Anwendungsfälle und Beispiele {#use-cases}

Vom Journey-Designer aus können Marketing-Fachleute in Echtzeit ausgelöste 1:1-Nachrichten über jeden Kanal senden, wenn ein Ereignis auftritt. Wenn Kundinnen oder Kunden beispielsweise einen Service abonnieren, kann dies [das Versenden einer Begrüßungs-E-Mail auslösen](message-to-subscribers-uc.md), in der sie aufgefordert werden, sich zum ersten Mal bei der App anzumelden und ihre Voreinstellungen festzulegen. Aktionen wie der Abschluss des Kaufs, das Öffnen der E-Mail und die Anmeldung bei der App können verwendet werden, damit neue Kundinnen und Kunden in ihrer Journey fortfahren.

Der [Journey-Designer](using-the-journey-designer.md) bietet [integrierte Kanalaktionen](journeys-message.md), die ausgehende Nachrichten wie E-Mails, Push-Benachrichtigungen und SMS/MMS sowie eingehende Kanäle wie Apps, Websites und Code-basierte Erlebnisse unterstützen, die direkt in Journey Optimizer erstellt werden. Sie können auch Drittanbietersysteme verwenden, um Nachrichten zu senden. Journey Optimizer umfasst [benutzerdefinierte Aktionen](using-custom-actions.md), mit denen diese Systeme direkt über den Journey-Designer in Journeys integriert werden können.


:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=de)

**Lernen durch Anwendungsfälle**

Erkunden Sie umfassende End-to-End-Journey-Anwendungsfälle, die reale Implementierungen und Best Practices demonstrieren.

[Erkunden aller Anwendungsfälle](jo-use-cases.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=de)

**Begrüßen neuer Abonnentinnen und Abonnenten**

Senden Sie eine personalisierte Willkommens-Journey, wenn Kundinnen und Kunden Ihren Service abonnieren, und führen Sie sie so durch die Onboarding-Schritte.

[Weitere Informationen](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=de)

**Optimieren der E-Mail-Versandzeiten**

Verwenden Sie die KI-gestützte Versandzeitoptimierung, um E-Mails dann zu versenden, wenn jede Kundin und jeder Kunde mit der größten Wahrscheinlichkeit interagiert.

[Weitere Informationen](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=de)

**Steigern der Versandaktivität**

Erhöhen Sie das Nachrichtenvolumen schrittweise, um Ihre Reputation beim Versand zu verbessern und Probleme mit der Zustellbarkeit zu vermeiden.

[Weitere Informationen](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=de)

**Ansprechen nach Wochentag**

Senden Sie unterschiedliche Inhalte je nach Wochentag, an dem Kundinnen und Kunden in Ihre Journey eintreten.

[Weitere Informationen](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/question.svg?lang=de)

**Häufig gestellte Fragen zu Journeys**

Hier finden Sie Antworten auf häufig gestellte Fragen zur Journey-Erstellung, Fehlerbehebung und zu Best Practices.

[Häufig gestellte Fragen anzeigen](journey-faq.md)
:::

::::



## Lernressourcen {#learning-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=de)

**Erstellen und Verwalten von Journeys**

Schrittweise Anleitungen zum Entwerfen, Testen, Veröffentlichen und Tracking von Customer Journeys, um personalisierter Omni-Channel-Kampagnen zu erstellen.

[Erkunden der Journey-Erstellung](../../rp_landing_pages/create-journey-landing-page.md) | [Weitere Informationen zum Journey-Management](../../rp_landing_pages/manage-journey-landing-page.md) | [Journey-Workflow-Schritte](journey.md#workflow)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=de)

**Journey-Aktivitäten**

Entdecken Sie, wie Sie Aktivitäten wie Trigger, Entscheidungsschritte, Zielgruppen-Management und personalisiertes Messaging in Journeys konfigurieren und verwenden.

[Aktivitäten erkunden](../../rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=de)

**Ausdrücke und Bedingungen**

Meistern Sie die Erstellung von Ausdrücken für dynamische Workflows, Datenmanipulation und erweiterte Journey-Orchestrierung mit leistungsstarken Tools und Syntax.

[Mehr zu Ausdrücken](../../rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=de)

**Fehlerbehebung und Überwachung**

Diagnostizieren und beheben Sie Probleme bei der Ausführung von Journeys mit Tools, Fehler-Codes und Best Practices für Debugging und Optimierung.

[Handbuch zur Fehlerbehebung](../../rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=de)

**Journey-Designer – Überblick**

Machen Sie sich mit der Journey-Arbeitsfläche, der Palette und dem Design Ihrer Customer Journeys vertraut.

[Kennenlernen des Designers](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=de)

**Testen und Veröffentlichen**

Testen Sie Ihre Journeys gründlich, bevor Sie sie veröffentlichen, um sicherzustellen, dass sie wie erwartet funktionieren und das richtige Erlebnis bieten.

[Testleitfaden](testing-the-journey.md)
:::

::::

### Video-Tutorial {#video}

Entdecken Sie die Komponenten einer Journey und lernen Sie die Grundlagen des Erstellens einer Journey auf der Arbeitsfläche kennen.

>[!VIDEO](https://video.tv.adobe.com/v/3432378?captions=ger&quality=12)

### Weitere Ressourcen

* **[Referenz zu Fehler-Codes](error-codes-reference.md)** – Journey-Fehler-Codes und Schritte zur Fehlerbehebung
* **[Warnhinweise](../reports/alerts.md)** – Richten Sie Warnhinweise für das Monitoring von Journeys ein
* **[Fehlerbehebung](troubleshooting.md)** – Häufige Probleme mit Journeys und deren Lösungen
* **[Journey-Tutorials](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** – Erfahren Sie mehr über das Erstellen von Journeys anhand praktischer Video-Tutorials
* **[Leitlinien und Einschränkungen bei Journeys](../start/guardrails.md)** – Erhalten Sie Informationen zu Leitlinien und Einschränkungen bei der Verwendung von [!DNL Adobe Journey Optimizer]
