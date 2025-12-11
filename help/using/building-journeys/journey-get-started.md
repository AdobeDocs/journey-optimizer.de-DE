---
solution: Journey Optimizer
product: journey optimizer
title: Journey Orchestration - Vollständiges Handbuch
description: Umfassendes Handbuch für die ersten Schritte mit der Journey-Orchestrierung in Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
keywords: Journey, Orchestrierung, Erste Schritte, Onboarding, Funktionen
source-git-commit: 902790b2e172ef02e868592794fc110d3e14ac07
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 51%

---


# Journey Orchestration - Vollständiges Handbuch{#journey-orchestration-guide}

Mit Journeys in Adobe Journey Optimizer können Sie personalisierte, mehrstufige Customer Journeys erstellen, die sich in Echtzeit an das Verhalten und die Bedürfnisse Ihrer Zielgruppe anpassen. Mithilfe einer intuitiven Drag-and-Drop-Arbeitsfläche können Sie Nachrichten und Aktionen über mehrere Kanäle hinweg orchestrieren und dabei kontextuelle Daten und Audience-Targeting nutzen, um eine maximale Wirkung zu erzielen.

Unabhängig davon, ob Sie Echtzeit-Trigger untersuchen, Journey-Eigenschaften verwalten oder erweiterte Tools wie benutzerdefinierte Aktionen und Ausdrücke verwenden, bietet dieses Handbuch eine klare Roadmap für die vertrauensvolle Gestaltung und Verfeinerung von Journey, die aussagekräftige, zeitnahe Kundenerlebnisse bereitstellen.

➡️ [Journey Optimizer entdecken (Video)](#video)

>[!BEGINTABS]

>[!TAB Übersicht]

## Was sind Journey?

Verwenden Sie [!DNL Journey Optimizer], um Anwendungsfälle für die Echtzeit-Orchestrierung mithilfe von in Ereignissen oder Datenquellen gespeicherten kontextuellen Daten zu erstellen. Entwickeln Sie mehrstufige erweiterte Szenarien, die in Echtzeit auf Kundenverhalten und Geschäftsereignisse reagieren.

Der Journey-Designer von Journey Optimizer bietet alles, was Marketing-Fachleute und Journey-Anwendende benötigen, um mehrstufige 1:1-Journeys kanalübergreifend zu orchestrieren. Dazu gehört eine intuitive Drag-and-Drop-Arbeitsfläche zum Orchestrieren aller Schritte der Journey, Definieren der Zielgruppe und kanalübergreifendem Einschließen der Nachrichten, Angebote und Inhalte, die die Mitglieder der Zielgruppe basierend auf ihrem Verhalten, kontextuellen Daten und Geschäftsereignissen zu sehen bekommen.

![Benutzeroberfläche des Journey-Designers mit Palette, Arbeitsfläche und Eigenschaftenbereich](assets/journey38.png)

**Bereit mit dem Bauen?** Auf dieser Seite erfahren Sie, wie Sie Ihre erste Journey erstellen [&#x200B; gestalten](journey-gs.md).

>[!TAB Schlüsselfunktionen]

## Was kannst du mit Journey machen?

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/send-real-time.svg)

**Versand in Echtzeit und per Batch**

Führen Sie einen **unitären Versand** in Echtzeit aus, ausgelöst durch den Empfang eines Ereignisses, oder **als Batch** unter Verwendung von Adobe Experience Platform-Zielgruppen.

[Informationen zum Journey-Eintrag](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

**Kontextbezogene Daten**

Nutzen Sie **kontextuelle Daten** aus Ereignissen, Informationen aus Adobe Experience Platform oder Daten aus API-Services von Drittanbietern.

[Arbeiten mit Datenquellen](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/message.svg?lang=de)

**Integrierte Aktionen**

Verwenden Sie **integrierten Kanalaktionen** um in [!DNL Journey Optimizer] entworfene Nachrichten per E-Mail, Push, SMS/MMS und mehr zu senden.

[Senden von Nachrichten in Journey](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg?lang=de)

**Benutzerdefinierte Aktionen**

Erstellen Sie **benutzerdefinierte Aktionen** wenn Sie zum Senden Ihrer Nachrichten oder zum Herstellen einer Verbindung zu externen APIs ein Drittanbietersystem verwenden.

[Benutzerdefinierter Aktionen konfigurieren](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/canvas.svg)

**Visual Journey Designer**

Erstellen Sie mit dem **Journey-Designer** mehrstufige Anwendungsfälle: Ziehen Sie einfach per Drag-and-Drop ein Eintrittsereignis oder eine Aktivität vom Typ „Zielgruppe lesen“ in die Benutzeroberfläche, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

[Erkunden des Journey-Designers](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/test.svg)

**Testen und Optimieren**

Testen Sie Ihre Journey vor der Veröffentlichung, überwachen Sie deren Leistung und optimieren Sie den Versand mit erweiterten Funktionen wie der Sendezeitoptimierung.

[Journey testen und veröffentlichen](testing-the-journey.md)
:::

::::

>[!TAB Anwendungsfälle]

## Beispiele für reales Journey

Vom Journey-Designer aus können Marketing-Fachleute in Echtzeit ausgelöste 1:1-Nachrichten über jeden Kanal senden, wenn ein Ereignis auftritt. Wenn Kundinnen oder Kunden beispielsweise einen Service abonnieren, kann dies [das Versenden einer Begrüßungs-E-Mail auslösen](message-to-subscribers-uc.md), in der sie aufgefordert werden, sich zum ersten Mal bei der App anzumelden und ihre Voreinstellungen festzulegen. Aktionen wie der Abschluss des Kaufs, das Öffnen der E-Mail und die Anmeldung bei der App können verwendet werden, damit neue Kundinnen und Kunden in ihrer Journey fortfahren.

### Beliebte Journey-Anwendungsfälle

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/email.svg)

**Willkommen bei neuen Abonnenten**

Senden Sie eine personalisierte Willkommens-Journey, wenn Kunden Ihren Service abonnieren, und führen Sie sie durch die Onboarding-Schritte.

[Weitere Informationen](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar.svg?lang=de)

**Optimieren der E-Mail-Versandzeiten**

Verwenden Sie die KI-gestützte Sendezeitoptimierung , um E-Mails zu versenden, wenn jede Kundin und jeder Kunde mit der größten Wahrscheinlichkeit interagiert.

[Weitere Informationen](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/delivery.svg)

**Steigern der Versandaktivität**

Erhöhen Sie das Nachrichtenvolumen schrittweise, um Ihre Reputation beim Versand zu verbessern und Probleme mit der Zustellbarkeit zu vermeiden.

[Weitere Informationen](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/targeting.svg)

**Target nach Wochentag**

Senden Sie je nach Wochentag, an dem Kundinnen und Kunden Ihre Journey betreten, unterschiedliche Inhalte.

[Weitere Informationen](weekday-email-uc.md)
:::

::::

### Weitere Anwendungsfälle

Der [Journey-Designer](using-the-journey-designer.md) bietet [integrierte Kanalaktionen](journeys-message.md), die ausgehende Nachrichten wie E-Mails, Push-Benachrichtigungen und SMS/MMS sowie eingehende Kanäle wie Apps, Websites und Code-basierte Erlebnisse unterstützen, die direkt in Journey Optimizer erstellt werden. Sie können auch Drittanbietersysteme zum Senden von Nachrichten verwenden. Journey Optimizer enthält [benutzerdefinierte Aktionen](using-custom-actions.md) mit denen diese Systeme direkt vom Journey-Designer in Journey integriert werden können.

**Erkunden Sie alle Journey-** auf [dieser Seite](jo-use-cases.md) um End-to-End-Szenarien zu ermitteln, die Sie implementieren können.

>[!NOTE]
>
>Leitlinien und Einschränkungen für Journeys werden auf [dieser Seite](../start/guardrails.md) beschrieben.

>[!TAB Lernressourcen]

## Master-Journey-Gebäude

### Video-Tutorial {#video}

Entdecken Sie die Komponenten einer Journey und lernen Sie die Grundlagen des Erstellens einer Journey auf der Arbeitsfläche kennen.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

### Nach Thema durchsuchen

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=de)

**Erstellen und Verwalten von Journey**

Schrittweise Anleitungen zum Entwerfen, Testen, Veröffentlichen und Tracking von Customer Journeys zum Erstellen personalisierter Omni-Channel-Kampagnen.

[Erkunden der Journey-Erstellung](/help/rp_landing_pages/create-journey-landing-page.md) | [Erfahren Sie mehr über die Verwaltung von Journey](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=de)

**Journey-Aktivitäten**

Entdecken Sie, wie Sie Aktivitäten wie Trigger, Entscheidungsschritte, Zielgruppen-Management und personalisiertes Messaging in Journeys konfigurieren und verwenden.

[Aktivitäten erkunden](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=de)

**Ausdrücke und Bedingungen**

Meistern Sie die Erstellung von Ausdrücken für dynamische Workflows, Datenmanipulation und erweiterte Journey-Orchestrierung mit leistungsstarken Tools und Syntax.

[Mehr zu Ausdrücken](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/monitor.svg)

**Fehlerbehebung und Überwachung**

Diagnostizieren und beheben Sie Journey-Ausführungsprobleme mit Tools, Fehlercodes und Best Practices für Debugging und Optimierung.

[Handbuch zur Fehlerbehebung](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

::::

### Weitere Ressourcen

* **[Häufig gestellte Fragen zu Journeys](journey-faq.md)** – Häufig gestellte Fragen zu Journeys
* **[Referenz zu Fehler-Codes](error-codes-reference.md)** – Journey-Fehler-Codes und Schritte zur Fehlerbehebung
* **[Warnhinweise](../reports/alerts.md)** – Richten Sie Warnhinweise für das Monitoring von Journeys ein
* **[Fehlerbehebung](troubleshooting.md)** – Häufige Probleme mit Journeys und deren Lösungen
* **[Journey-Tutorials](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - Lernen Sie das Erstellen von Journey durch praktische Video-Tutorials

>[!ENDTABS]

