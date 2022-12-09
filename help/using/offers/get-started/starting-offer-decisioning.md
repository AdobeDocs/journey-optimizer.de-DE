---
title: Erste Schritte mit der Entscheidungsverwaltung
description: Erfahren Sie, wie Adobe Journey Optimizer Ihnen dabei helfen kann, Ihren Kunden das richtige Angebot zur richtigen Zeit zu senden.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# Über die Entscheidungsverwaltung {#about-decision-management}

Verwendung [!DNL Journey Optimizer] , um Ihren Kunden zur richtigen Zeit über alle Kontaktpunkte hinweg das beste Angebot und Erlebnis bereitzustellen. Danach können Sie Ihre Zielgruppen mit personalisierten Angeboten ansprechen.

Die Entscheidungsverwaltung erleichtert die Personalisierung mit einer zentralen Bibliothek von Marketing-Angeboten und einer Entscheidungs-Engine, die Regeln und Einschränkungen auf umfassende Echtzeit-Profile anwendet, die von Adobe Experience Platform erstellt wurden, damit Sie Ihren Kunden zum richtigen Zeitpunkt das richtige Angebot unterbreiten können.

Die Entscheidungsverwaltungsfunktion besteht aus zwei Hauptkomponenten:

* Die **Zentralisierte Angebotsbibliothek** auf der Sie die verschiedenen Elemente erstellen und verwalten, aus denen Ihre Angebote bestehen, und deren Regeln und Begrenzungen definieren.
* Die **Offer Decisioning-Engine** , das Adobe Experience Platform-Daten und Echtzeit-Kundenprofile gemeinsam mit der Angebotsbibliothek nutzt, um die richtigen Zeitpunkte, Kunden und Kanäle für die Bereitstellung von Angeboten auszuwählen.

![](../assets/architecture.png)

Zu den Vorteilen zählen:

* Verbesserte Kampagnenleistung durch die Bereitstellung personalisierter Angebote über mehrere Kanäle hinweg,
* Verbesserte Workflows: Anstatt mehrere Sendungen oder Kampagnen zu erstellen, können Marketingteams Workflows verbessern, indem sie einen einzigen Versand erstellen und die Angebote in verschiedenen Teilen der Vorlage variieren.
* Kontrolle darüber, wie oft ein Angebot in Kampagnen und Kunden angezeigt wird.

➡️ [Weitere Informationen zur Entscheidungsverwaltung finden Sie in diesen Videos](#video)


>[!NOTE]
>
>Wenn Sie [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target=&quot;_blank&quot;} Benutzer, der die **Offer Decisioning** Anwendungsdienst, gelten auch alle in diesem Abschnitt beschriebenen Funktionen zur Entscheidungsverwaltung für Sie.

## Über Angebote und Entscheidungen {#about-offers-and-decisions}

Ein **Angebot** besteht aus Inhalten, Eignungsregeln und Einschränkungen, die die Bedingungen definieren, unter denen sie Ihren Kunden präsentiert werden.

Sie wird mithilfe der **Angebotsbibliothek**, bietet einen zentralen Angebotskatalog, in dem Sie Eignungsregeln und Einschränkungen mit mehreren Inhaltselementen verknüpfen können, um Angebote zu erstellen und zu veröffentlichen (siehe [Benutzeroberfläche der Angebotsbibliothek](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

Sobald die Angebotsbibliothek mit Angeboten angereichert wurde, können Sie Ihre Angebote in **Entscheidungen**.

Entscheidungen sind Container für Ihre Angebote, die die Offer Decisioning-Engine nutzen, um je nach Zielgruppe des Versands das beste Angebot auszuwählen, das bereitgestellt werden kann.

## Häufige Anwendungsfälle {#common-use-cases}

Die Funktionen zur Entscheidungsverwaltung und die Integration mit Adobe Experience Platform ermöglichen es Ihnen, zahlreiche Anwendungsfälle abzudecken, um die Interaktion und Konversion von Kunden zu verbessern.

* Zeigen Sie auf der Startseite Ihrer Website Angebote an, die basierend auf Daten aus Adobe Experience Platform dem Zielpunkt des Besuchers entsprechen.

   ![](../assets/website.png)

* Wenn Kunden in der Nähe eines Ihrer Geschäfte gehen, senden Sie ihnen Push-Benachrichtigungen, um sie an verfügbare Angebote zu erinnern, die ihren Attributen entsprechen (Treuestufe, Geschlecht, frühere Käufe usw.).

   ![](../assets/push_sample.png)

* Die Entscheidungsverwaltung hilft Ihnen auch, das Kundenerlebnis bei der Kontaktaufnahme mit Ihrem Support-Team zu verbessern. Mit Entscheidungsmanagement-APIs können Sie im Portal Ihrer Callcenter-Agenten Informationen über die eingelösten und nächsten besten Angebote anzeigen.

   ![](../../assets/do-not-localize/call-center.png)

## Zugriff auf die Entscheidungsverwaltung gewähren {#granting-acess-to-decision-management}

Berechtigungen für den Zugriff auf und die Verwendung von Entscheidungsfunktionen werden mithilfe des [Adobe Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Um Zugriff auf die Entscheidungsverwaltungsfunktionen zu gewähren, müssen Sie eine **[!UICONTROL Product profile]** und weisen Sie Ihren Benutzern die entsprechenden Berechtigungen zu. Weitere Informationen zur Verwaltung [!DNL Journey Optimizer] Benutzer und Berechtigungen in [diesem Abschnitt](../../administration/permissions.md).

Die spezifischen Berechtigungen für die Entscheidungsverwaltung finden Sie unter [diesem Abschnitt](../../administration/high-low-permissions.md#decisions-permissions).

## Glossar {#glossary}

Unten finden Sie die Liste der wichtigsten Konzepte, mit denen Sie bei der Verwendung von Entscheidungsmanagement arbeiten werden.

* **Begrenzung** oder **Frequenzlimitierung**: Begrenzungen dienen dazu, festzulegen, wie oft ein Angebot unterbreitet wird. Es gibt zwei Arten von Begrenzungen: wie oft ein Angebot für die kombinierte Zielgruppe vorgeschlagen werden kann, auch &quot;Gesamtbeschränkungen&quot;genannt, und wie oft ein Angebot demselben Endbenutzer vorgeschlagen werden kann, auch als &quot;Profilbegrenzung&quot;bezeichnet.

* **Sammlungen**: Kollektionen sind Untergruppen von Angeboten, die auf von einem Marketing-Experten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.

* **Entscheidung**: Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots informiert.

* **Entscheidungsregel**: Entscheidungsregeln sind Einschränkungen, die einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um die Eignung zu bestimmen.

* **Geeignetes Angebot**: Ein geeignetes Angebot erfüllt zuvor definierte Bedingungen, die einem Profil auf kohärente Weise unterbreitet werden können.

* **Entscheidungsverwaltung**: Ermöglicht die Erstellung und Bereitstellung personalisierter Angebotserlebnisse für Endbenutzer über Kanäle und Anwendungen hinweg mithilfe von Business-Logik und Entscheidungsregeln.

* **Fallback-Angebote**: Ein Fallback-Angebot ist das Standardangebot, das angezeigt wird, wenn ein Endbenutzer für keines der personalisierten Angebote in der Sammlung qualifiziert ist.

* **Angebot**: Ein Angebot ist eine Marketing-Botschaft, der ggf. Regeln zugeordnet sind, die angeben, wer zum Anzeigen des Angebots berechtigt ist.

* **Angebotsbibliothek**: Die Angebotsbibliothek ist eine zentrale Bibliothek, die zur Verwaltung von personalisierten Angeboten und Fallback-Angeboten, Entscheidungsregeln und Entscheidungen verwendet wird.

* **Personalisierte Angebote**: Ein personalisiertes Angebot ist eine anpassbare Marketing-Botschaft, die auf Eignungsregeln und Einschränkungen basiert.

* **Praktika**: Eine Platzierung ist der Ort und/oder Kontext, in dem ein Angebot für einen Endbenutzer angezeigt wird.

* **Priorität**: Mit &quot;Priorität&quot;werden Angebote sortiert, die alle Einschränkungen erfüllen, wie Eignung, Kalender und Begrenzung.

* **Darstellungen**: Eine Darstellung sind Informationen, die von einem Kanal verwendet werden, z. B. Ort oder Sprache zur Anzeige eines Angebots.

## Anleitungsvideos{#video}

>[!NOTE]
>
>Diese Videos gelten für den Offer Decisioning-Anwendungsdienst, der auf Adobe Experience Platform aufbaut, und sind nicht spezifisch für [!DNL Adobe Journey Optimizer]. Sie bieten jedoch allgemeine Leitlinien für die Verwendung des Entscheidungsmanagements im Rahmen von [!DNL Journey Optimizer].

### Was ist Entscheidungsmanagement? {#what-is-offer-decisioning}

Das folgende Video bietet eine Einführung in die wichtigsten Funktionen, Architekturmerkmale und Anwendungsfälle der Entscheidungsverwaltung:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Angebote definieren und verwalten {#use-offer-decisioning}

Im folgenden Video erfahren Sie, wie Sie mithilfe von Decision Management Ihre Angebote definieren und verwalten und Echtzeit-Kundendaten nutzen können.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


