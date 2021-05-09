---
title: Erste Schritte mit der Entscheidungsverwaltung
description: Beginnen Sie mit der Entscheidungsverwaltung. Erfahren Sie mehr über die Architektur, die Angebot und Entscheidungen sowie über gängige Anwendungsfälle, die es Ihnen ermöglicht, diese zu erfüllen.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Informationen zur Entscheidungsverwaltung {#about-offer-decision}

Verwenden Sie [!DNL Journey Optimizer], um Ihren Kunden das beste Angebot und Erlebnis für alle Berührungspunkte zur richtigen Zeit bereitzustellen. Zielgruppen Sie Ihre Audiencen nach der Planung mit personalisierten Angeboten.

Die Entscheidungsverwaltungskapazität besteht aus zwei Hauptkomponenten:

* Die **Zentralisierte Angebot-Bibliothek** ist die Schnittstelle, auf der Sie die verschiedenen Elemente erstellen und verwalten, die Ihre Angebot zusammenstellen, und deren Regeln und Einschränkungen definieren.
* Die **Angebot Decision Engine**, die Adobe Experience Platform-Daten und Echtzeit-Kundendaten sowie die Angebot-Bibliothek nutzt, um die richtige Uhrzeit, Kunden und Kanal auszuwählen, an die die Angebot geliefert werden.

![](../assets/architecture.png)

Zu den Vorteilen zählen:

* Verbesserte Leistung der Kampagne durch die Bereitstellung personalisierter Angebot über mehrere Kanal hinweg,
* Verbesserte Workflows: Anstatt mehrere Versand oder Kampagnen zu erstellen, können Marketingteams die Workflows verbessern, indem sie einen einzigen Versand erstellen und die Angebot in verschiedenen Teilen der Vorlage variieren,
* Steuern Sie, wie oft ein Angebot in Kampagnen und Kunden angezeigt wird.

![](../assets/do-not-localize/how-to-video.png) [Sehen Sie sich diese ](#tutorial-videos) Videos an, um mehr über die Entscheidungsverwaltung zu erfahren.

## Angebote und Entscheidungen {#offers-offer-activities}

Ein **Angebot** besteht aus Inhalten, Eignungsregeln und Einschränkungen, die die Bedingungen definieren, unter denen es Ihren Kunden präsentiert wird.

Sie wird mit der **Angebot-Bibliothek** erstellt, die einen zentralen Angebotskatalog bereitstellt, in dem Sie Eignungsregeln und Einschränkungen mit mehreren Inhaltselementen verknüpfen können, um Angebot zu erstellen und zu veröffentlichen (siehe [Angebot-Bibliotheks-Benutzeroberfläche](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

Nachdem die Angebot-Bibliothek mit Angeboten erweitert wurde, können Sie Ihre Angebot in **entscheidungen** (früher &quot;Angebot-Aktivitäten&quot;) integrieren.

Entscheidungen sind Container für Ihre Angebot, die die Entscheidungsmaschine für Angebote nutzen, um das beste Angebot zu wählen, das je nach Zielgruppe des Versands bereitgestellt werden kann.

## Allgemeine Anwendungsfälle

Die Entscheidungsverwaltungsfunktionen und die Integration mit Adobe Experience Platform ermöglichen es Ihnen, zahlreiche Anwendungsfälle zu behandeln, um die Interaktion und Konversion Ihrer Kunden zu steigern.

* Zeigen Sie auf Ihrer Website Angebot an, die auf der Grundlage von Daten aus Adobe Experience Platform dem Interessensgebiet des Besuchers entsprechen.

   ![](../assets/website.png)

* Wenn Kunden in der Nähe eines Ihrer Geschäfte gehen, senden Sie ihnen Push-Benachrichtigungen, um sie an verfügbare Angebot entsprechend ihren Attributen (Loyalität, Geschlecht, frühere Käufe usw.) zu erinnern.

   ![](../assets/push_sample.png)

* Die Entscheidungsverwaltung hilft Ihnen auch, das Kundenerlebnis zu verbessern, wenn Sie sich an Ihr Supportteam wenden. Mit den Entscheidungs-Management-APIs können Sie im Portal Ihrer Call-Center-Agenten Informationen über die eingelösten und nächsten besten Angebot des Kunden anzeigen.

   ![](../assets/call-center.png)

## Übungsvideos {#tutorial-videos}

>[!NOTE]
>
>Diese Videos gelten für den auf Adobe Experience Platform aufbauenden Offer decisioning-Anwendungsdienst und sind nicht spezifisch für [!DNL Adobe Journey Optimizer]. Sie enthält jedoch allgemeine Leitlinien für die Verwendung der Entscheidungsverwaltung im Kontext von [!DNL Journey Optimizer].

### Was ist Entscheidungsverwaltung? {#what-is-offer-decisioning}

Das nachstehende Video bietet eine Einführung in die wichtigsten Funktionen, Architektur und Anwendungsfälle von Decision Management:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Definieren und Verwalten von Angeboten {#use-offer-decisioning}

Das unten stehende Video zeigt, wie Sie mithilfe von Decision Management Ihre Angebot definieren und verwalten und Echtzeit-Kundendaten nutzen können.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)
