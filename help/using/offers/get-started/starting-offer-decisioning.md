---
title: Erste Schritte mit der Entscheidungsverwaltung
description: Beginnen Sie mit der Entscheidungsverwaltung. Erfahren Sie mehr über die Architektur, die Angebot und Entscheidungen sowie über gängige Anwendungsfälle, die es Ihnen ermöglicht, diese zu erfüllen.
translation-type: tm+mt
source-git-commit: b527186d0722492f5f509f1ae0a5315b9a9f771e
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 38%

---


# Informationen zur Entscheidungsverwaltung {#about-offer-decision}

Verwenden Sie [!DNL Journey Optimizer], um Ihren Kunden über alle Berührungspunkte hinweg zur richtigen Zeit das beste Angebot und Erlebnis zu bieten. Zielgruppen Sie Ihre Audiencen nach der Planung mit personalisierten Angeboten.

Die Entscheidungsverwaltungskapazität besteht aus zwei Hauptkomponenten:

* Die **Zentralisierte Angebot-Bibliothek** ist die Schnittstelle, auf der Sie die verschiedenen Elemente erstellen und verwalten, die Ihre Angebot zusammenstellen, und deren Regeln und Einschränkungen definieren.
* Die **Angebot Decision Engine**, die Adobe Experience Platform-Daten und Echtzeit-Kundendaten sowie die Angebot-Bibliothek nutzt, um die richtige Uhrzeit, Kunden und Kanal auszuwählen, an die die Angebot geliefert werden.

![](../../assets/architecture.png)

Zu den Vorteilen zählen:

* Verbesserte Kampagnenleistung durch Unterbreitung personalisierter Angebote über verschiedene Kanäle hinweg.
* Verbesserte Workflows: Anstatt mehrere Sendungen oder Kampagnen erstellen zu müssen, können Marketing-Teams Workflows optimieren, indem sie einen einzelnen Versand erstellen und die Angebote in verschiedenen Teilen der Vorlage variieren.
* Kontrolle darüber, wie häufig ein Angebot in Kampagnen den einzelnen Kunden unterbreitet wird.

![](../../assets/do-not-localize/how-to-video.png) [Sehen Sie sich diese ](#tutorial-videos) Videos an, um mehr über die Entscheidungsverwaltung zu erfahren.

## Angebote und Entscheidungen {#offers-offer-activities}

Ein **Angebot** besteht aus Inhalten, Eignungsregeln und Einschränkungen, die die Bedingungen festlegen, unter denen das Angebot Kunden unterbreitet wird.

Es wird mithilfe der **Angebotsbibliothek** erstellt. Diese bietet einen zentralen Angebotskatalog, in dem Sie Eignungsregeln und Einschränkungen mit unterschiedlichen Inhaltselementen verknüpfen können, um Angebote zu erstellen und zu veröffentlichen (siehe [Benutzeroberfläche der Angebotsbibliothek](../get-started/user-interface.md)).

![](../../assets/offer_structure.png)

Nachdem die Angebot-Bibliothek mit Angeboten erweitert wurde, können Sie Ihre Angebot in **entscheidungen** (früher &quot;Angebot-Aktivitäten&quot;) integrieren.

Entscheidungen sind Container für Ihre Angebot, die die Entscheidungsmaschine für Angebote nutzen, um das beste Angebot zu wählen, das je nach Zielgruppe des Versands bereitgestellt werden kann.

## Häufige Anwendungsfälle

Die Entscheidungsverwaltungsfunktionen und die Integration mit Adobe Experience Platform ermöglichen es Ihnen, zahlreiche Anwendungsfälle zu behandeln, um die Interaktion und Konversion Ihrer Kunden zu steigern.

* Zeigen Sie auf der Startseite Ihrer Website Angebote an, die basierend auf Daten aus Adobe Experience Platform den Interessengebieten des Besuchers entsprechen.

   ![](../../assets/website.png)

* Wenn Kunden an einem Ihrer Geschäfte vorbeigehen, senden Sie ihnen Push-Benachrichtigungen, um sie je nach ihren Attributen (Treuestufe, Geschlecht, frühere Käufe usw.) an verfügbare Angebote zu erinnern.

   ![](../../assets/push_sample.png)

* Die Entscheidungsverwaltung hilft Ihnen auch, das Kundenerlebnis zu verbessern, wenn Sie sich an Ihr Supportteam wenden. Mit den Entscheidungs-Management-APIs können Sie im Portal Ihrer Call-Center-Agenten Informationen über die eingelösten und nächsten besten Angebot des Kunden anzeigen.

   ![](../../assets/call-center.png)

## Anleitungsvideos {#tutorial-videos}

>[!NOTE]
>
>Diese Videos gelten für den auf Adobe Experience Platform aufbauenden Offer decisioning-Anwendungsdienst und sind nicht spezifisch für [!DNL Adobe Journey Optimizer]. Sie enthält jedoch allgemeine Leitlinien für die Verwendung der Entscheidungsverwaltung im Kontext von [!DNL Journey Optimizer].

### Was ist Entscheidungsverwaltung? {#what-is-offer-decisioning}

Das nachstehende Video bietet eine Einführung in die wichtigsten Funktionen, Architektur und Anwendungsfälle von Decision Management:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Angebote definieren und verwalten {#use-offer-decisioning}

Das unten stehende Video zeigt, wie Sie mithilfe von Decision Management Ihre Angebot definieren und verwalten und Echtzeit-Kundendaten nutzen können.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)
