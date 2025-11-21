---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erste Schritte mit dem Entscheidungs-Management
description: Erfahren Sie, wie Adobe Journey Optimizer Ihnen dabei helfen kann, Ihren Kunden das richtige Angebot zum richtigen Zeitpunkt zu senden.
badge: label="Legacy" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 100%

---

# Erste Schritte mit dem Entscheidungs-Management {#about-decision-management}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

Verwenden Sie [!DNL Journey Optimizer], um Ihren Kunden über alle Berührungspunkte hinweg zur richtigen Zeit das beste Angebot und Erlebnis zu bieten. Nach der Erstellung können Sie personalisierte Angebote an Ihre Zielgruppen senden.

Entscheidungs-Management erleichtert die Personalisierung durch eine zentrale Bibliothek mit Marketing-Angeboten und eine Entscheidungs-Engine. Dabei werden Regeln und Einschränkungen auf die von Adobe Experience Platform erstellten Echtzeitprofile angewendet, sodass Sie Ihren Kundinnen und Kunden zum richtigen Zeitpunkt das richtige Angebot senden können.

Entscheidungs-Management besteht aus zwei Hauptkomponenten:

* Die **zentrale Angebotsbibliothek** ist die Oberfläche, über die Sie die verschiedenen Elemente erstellen und verwalten können, aus denen Ihre Angebote bestehen. Außerdem können Sie hier entsprechende Regeln und Begrenzungen definieren.
* Die **Offer Decisioning-Engine** nutzt Adobe Experience Platform-Daten und Echtzeit-Kundenprofile sowie die Angebotsbibliothek, um die richtigen Zeitpunkte, Kunden und Kanäle für das Unterbreiten von Angeboten auszuwählen.

![](../assets/architecture.png)

Zu den Vorteilen zählen:

* Verbesserte Kampagnen-Performance durch die Bereitstellung personalisierter Angebote über mehrere Kanäle hinweg,
* Verbesserte Workflows: Anstatt mehrere Sendungen oder Kampagnen zu erstellen, können Marketing-Teams den Workflow verbessern, indem sie einen einzelnen Versand erstellen und die Angebote in verschiedenen Vorlagenbereichen variieren.
* Steuern Sie, wie oft ein Angebot in Kampagnen und für Kundschaft angezeigt wird.

➡️ [Weitere Informationen zum Entscheidungs-Management finden Sie in diesen Videos](#video)

>[!NOTE]
>
>Wenn Sie in [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=de){target="_blank"} die Anwendung **Offer Decisioning** nutzen, gelten alle in diesem Abschnitt beschriebenen Funktionen zum Entscheidungs-Management auch für Sie.

## Über Angebote und Entscheidungen {#about-offers-and-decisions}

Ein **Angebot** besteht aus Inhalten, Eignungsregeln und Begrenzungen. Diese definieren die Bedingungen, unter denen das Angebot Ihren Kundinnen und Kunden präsentiert wird.

Es wird mithilfe der **Angebotsbibliothek** erstellt, die einen zentralen Angebotskatalog bietet. In diesem können Sie Eignungsregeln und Begrenzungen mehreren Inhaltselementen zuordnen, um Angebote zu erstellen und zu veröffentlichen (siehe [Benutzeroberfläche der Angebotsbibliothek](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

Sobald die Angebotsbibliothek um Angebote erweitert wurde, können Sie diese in **Entscheidungen** integrieren.

Entscheidungen sind Container für Ihre Angebote, die die Offer Decisioning-Engine nutzen, um das beste Angebot auszuwählen, das je nach Zielgruppe des Versandes unterbreitet werden kann.

## Häufige Anwendungsfälle {#common-use-cases}

Dank der Entscheidungs-Management-Funktionen und der Integration mit Adobe Experience Platform können Sie zahlreiche Anwendungsfälle abdecken, um die Interaktion und Konversion von Kunden zu verbessern.

* Zeigen Sie auf der Startseite Ihrer Website Angebote an, die basierend auf Daten aus Adobe Experience Platform dem Point of Interest der Besucherinnen und Besucher entsprechen.

  ![](../assets/website.png)

* Wenn sich Kundinnen und Kunden in der Nähe eines Ihrer Geschäfte aufhalten, senden Sie ihnen Push-Benachrichtigungen, um sie an verfügbare Angebote zu erinnern, die ihren Attributen entsprechen (Treuestufe, Geschlecht, frühere Käufe).

  ![](../assets/push_sample.png)

* Zudem hilft Ihnen Entscheidungs-Management dabei, das Kundenerlebnis zu verbessern, wenn sich Kunden an Ihr Supportteam wenden. Mit Entscheidungs-Management-APIs können Sie im Portal Ihrer Callcenter-Agenten Informationen über die eingelösten und nächstbesten Angebote anzeigen.

  ![](../../assets/do-not-localize/call-center.png)

## Zugriff auf das Entscheidungs-Management gewähren {#granting-acess-to-decision-management}

Die Zugriffsberechtigungen und die Verwendung der Entscheidungsfunktionen werden mithilfe der [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/managing/user-guide.html){target="_blank"} verwaltet.

Um Zugriff auf die Funktionen des Entscheidungs-Managements zu gewähren, müssen Sie ein **[!UICONTROL Produktprofil]** erstellen und den Benutzenden die entsprechenden Berechtigungen zuweisen. Weitere Informationen zur Verwaltung von [!DNL Journey Optimizer]-Benutzenden und -Berechtigungen finden Sie in [diesem Abschnitt](../../administration/permissions.md).

Die für das Entscheidungs-Management spezifischen Berechtigungen sind in [diesem Abschnitt](../../administration/high-low-permissions.md#decisions-permissions) aufgeführt.

## Glossar {#glossary}

Unten finden Sie eine Liste der wichtigsten Konzepte bei der Verwendung des Entscheidungs-Managements.

* **Begrenzung** oder **Frequenzlimitierung**: Per Begrenzung wird festgelegt, wie oft ein Angebot angezeigt wird. Es gibt zwei Arten von Begrenzungen: wie oft ein Angebot für die kombinierte Zielgruppe vorgeschlagen werden kann (Gesamtbeschränkungen) und wie oft ein Angebot derselben Endbenutzerin bzw. demselben Endbenutzer vorgeschlagen werden kann (Profilbegrenzung).

* **Sammlungen**: Sammlungen sind Teilmengen von Angeboten, die auf von einem Marketing-Experten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.

* **Entscheidung**: Eine Entscheidung enthält die Logik, die die Auswahl eines Angebots bestimmt.

* **Entscheidungsregel**: Entscheidungsregeln sind Begrenzungen, die einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.

* **Geeignetes Angebot**: Ein geeignetes Angebot erfüllt zuvor definierte Begrenzungen, die einem Profil konsistent unterbreitet werden können.

* **Entscheidungs-Management**: Ermöglicht die Erstellung und Bereitstellung personalisierter Angebotserlebnisse für Endbenutzer über verschiedene Kanäle und Anwendungen mithilfe von Business-Logik und Entscheidungsregeln.

* **Fallback-Angebote**: Ein Fallback-Angebot ist das Standardangebot, das angezeigt wird, wenn eine Endanwenderin oder ein Endanwender für keines der personalisierten Angebote in der verwendeten Sammlung qualifiziert ist.

* **Angebot**: Ein Angebot ist eine Marketing-Botschaft, der ggf. Regeln zugeordnet sind, die angeben, wer sich zum Anzeigen des Angebots eignet.

* **Angebotsbibliothek**: Die Angebotsbibliothek ist eine zentrale Bibliothek, die zum Verwalten von personalisierten Angeboten sowie Fallback-Angeboten, Entscheidungsregeln und Entscheidungen dient.

* **Personalisierte Angebote**: Ein personalisiertes Angebot ist eine anpassbare Marketing-Botschaft, die auf Eignungsregeln und Begrenzungen basiert.

* **Platzierungen**: Eine Platzierung ist der Speicherort und/oder Kontext, in dem ein Angebot für Endbenutzende erscheint.

* **Priorität**: Die Priorität ist eine Zahl, die zur Einstufung von Angeboten verwendet wird, die alle Begrenzungen wie Berechtigungen, Termine und Obergrenzen erfüllen.

* **Darstellungen**: Eine Darstellung besteht aus Informationen, die von einem Kanal verwendet werden, z. B. Ort oder Sprache zur Anzeige eines Angebots.

## Anleitungsvideos{#video}

### Was ist Entscheidungs-Management? {#what-is-offer-decisioning}

Das folgende Video bietet eine Einführung in die wichtigsten Funktionen, Architekturmerkmale und Anwendungsfälle des Entscheidungs-Managements:

>[!VIDEO](https://video.tv.adobe.com/v/340413?captions=ger&quality=12&learn=on)

### Angebote definieren und verwalten {#use-offer-decisioning}

Das folgende Video zeigt, wie Sie mit dem Entscheidungs-Management Angebote definieren und verwalten sowie Echtzeit-Kundendaten nutzen können.

>[!VIDEO](https://video.tv.adobe.com/v/340351?captions=ger&quality=12&learn=on)


