---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-Funktionen nach Paket
description: Erfahren Sie, welche Adobe Journey Optimizer-Funktionen basierend auf Ihrer Lizenz, Ihrem Paket und den aktivierten Kanälen verfügbar sind.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: Journey Optimizer, Paket, Lizenz, auswählen, Prime, Ultimate, Funktionen, Funktionen, modular, Kanäle
hide: true
source-git-commit: 5e9ffb790127aae281dd15ad0eac03dbe0bb05e2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 6%

---


# Was ist in meinem [!DNL Adobe Journey Optimizer] Paket verfügbar? {#ajo-packages}

[!DNL Adobe Journey Optimizer] Funktionen variieren je nach Lizenzvereinbarung, aktivierten Kanälen und Benutzerberechtigungen. Verwenden Sie dieses Handbuch, um zu verstehen, welche Funktionen normalerweise in Ihrem Paket verfügbar sind, und navigieren Sie direkt zur Produktdokumentation für die einzelnen Funktionen.

Die Verfügbarkeit kann auch von der Kanalkonfiguration, den Implementierungsvoraussetzungen und den erworbenen Add-ons abhängen. Wählen Sie die Ihrem Lizenzmodell entsprechende Registerkarte aus.

>[!BEGINTABS]

>[!TAB Journey und Kampagnen]

Diese Registerkarte gilt für Kundinnen und Kunden, die unter dem aktuellen modularen [!DNL Adobe Journey Optimizer]-Verpackungsmodell (Journey Optimizer - Kampagnen, Journey Optimizer - Journey oder Journey Optimizer - Kampagnen und Journey) lizenziert sind.

## Basispakete {#current-packages}

| Paket | Was es enthält |
|---------|----------------|
| **Journey Optimizer - Kampagnen** | Kampagnenorchestrierung: Ein- oder mehrstufige Zielgruppen-Workflows für Batch-Interaktionen. Transaktionsnachrichten per E-Mail, Push und SMS enthalten. |
| **Journey Optimizer - Journey** | Echtzeit-Journey Orchestration: ereignisgesteuerte Journey mit Unterstützung für Streaming und Batch-Verarbeitung. Transaktionsnachrichten per E-Mail, Push und SMS enthalten. |
| **Journey Optimizer - Kampagnen und Journey** | Kampagnenorchestrierung und Real-time Journey Orchestration kombiniert. Transaktionsnachrichten per E-Mail, Push und SMS enthalten. |

>[!NOTE]
>
>Die Berechtigung für das gesamte Datenvolumen variiert je nach Paket: **Kampagnen**-Kunden haben Anspruch auf 15 KB pro adressierbarem Profil; **Journey** und **Kampagnen und Journey**-Kunden haben Anspruch auf 75 KB pro adressierbarem Profil.

Die folgenden Add-ons erweitern die Kanalabdeckung zusätzlich zu jedem Basispaket. Das **Alle Kanäle**-Add-on bündelt ausgehende Sendungen, Mobile Apps und Web zusammen.

| Add-on | Kanäle entsperrt |
|--------|----------------|
| **Ausgehender Versand** | E-Mail, Push-Benachrichtigungen, Briefpost. Umfasst die Grundlagen der Zustellbarkeit. |
| **Mobile** | In-App-Messaging, Push-Benachrichtigungen, Inhaltskarten und Code-basierte Kanäle für mobile Oberflächen |
| **Web** | Webkanal und codebasierte Kanäle für Weboberflächen |
| **Alle Kanäle** | Bundles Ausgehender Versand + Mobile + Web |
| **Entscheidungsfindung** | Echtzeit-Angebotsentscheidung und KI-gestützte Optimierung |

## Funktionsmatrix {#capability-matrix-current}

| Funktion | Mögliche Optionen | Journey Optimizer - Kampagnen | JOURNEY OPTIMIZER - JOURNEY | Journey Optimizer - Kampagnen und Journey | Add-on erforderlich | Weitere Informationen |
|-----------|----------------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|-----------|
| **Transaktionsnachrichten** | Senden von Nachrichten, die in Echtzeit ausgelöst werden, per E-Mail, Push oder SMS | ✓ | ✓ | ✓ | — | [Erfahren Sie mehr über Transaktionsnachrichten](../building-journeys/journey-gs.md) |
| **E-Mail** | Gestalten und Senden personalisierter E-Mail-Nachrichten | ✓ | ✓ | ✓ | Ausgehender Versand | [Erfahren Sie, wie Sie E-Mails senden](../email/get-started-email.md) |
| **Push-Benachrichtigungen** | Mobile Push-Benachrichtigungen senden | ✓ | ✓ | ✓ | Ausgehender Versand | [Erfahren Sie, wie Sie Push-Benachrichtigungen senden](../push/get-started-push.md) |
| **Briefpost** | Erstellen und Senden von physischen Postsendungen | ✓ | ✓ | ✓ | Ausgehender Versand | [Erfahren Sie, wie Sie Briefpost verwenden](../direct-mail/get-started-direct-mail.md) |
| **SMS/MMS** | Senden von Text- und Multimedia-Nachrichten | ✓ | ✓ | ✓ | Ausgehender Versand | [Erfahren Sie, wie Sie Nachrichten an Mobilgeräte senden](../mobile/get-started-mobile.md) |
| **In-App-Messaging** | Anzeigen von Nachrichten in Ihrer Mobile App | ✓ | ✓ | ✓ | Mobile | [Erfahren Sie, wie Sie In-App-Messaging verwenden](../in-app/get-started-in-app.md) |
| **Inhaltskarten** | Versand persistenter, nicht aufdringlicher produktinterner Nachrichten | ✓ | ✓ | ✓ | Mobile | [Erfahren Sie, wie Sie Inhaltskarten verwenden](../content-card/get-started-content-card.md) |
| **Web-Kanal** | Web-Seiten in Echtzeit personalisieren | ✓ | ✓ | ✓ | Web | [Erfahren Sie, wie Sie den Web-Kanal verwenden](../web/get-started-web.md) |
| **Code-basierte Erlebnisse** | Jede Oberfläche über API oder SDK personalisieren | ✓ | ✓ | ✓ | Mobil oder Web | [Erfahren Sie, wie Sie Code-basierte Erlebnisse verwenden](../code-based/get-started-code-based.md) |
| **WhatsApp** | Nachrichten über WhatsApp Business senden | ✓ | ✓ | ✓ | WhatsApp | [Erfahren Sie, wie Sie WhatsApp verwenden](../whatsapp/get-started-whatsapp.md) |
| **Orchestrierte Kampagnen** | Entwerfen Sie mehrstufige Zielgruppen-Workflows für Batch-Interaktionen. Unterstützte Kanäle: nur E-Mail, SMS, Push und Briefpost. | ✓ | — | ✓ | – | [Erfahren Sie, wie Sie orchestrierte Kampagnen verwenden](../orchestrated/gs-orchestrated-campaigns.md) |
| **Automated Journey** | Entwerfen von ereignisgesteuerten Echtzeit-Kunden-Journey | — | ✓ | ✓ | – | [Erfahren Sie, wie Sie Journey bauen](../building-journeys/journey-gs.md) |
| **Echtzeit-Trigger** | Auf Kundenereignisse reagieren, sobald sie auftreten | — | ✓ | ✓ | – | [Erfahren Sie mehr über Journey-Ereignisse](../event/about-events.md) |
| **Entscheidungsfindung** | Das beste Angebot für jeden Kunden in Echtzeit auswählen | Hängt von Ihrer Lizenz ab | Hängt von Ihrer Lizenz ab | Hängt von Ihrer Lizenz ab | Entscheidungsfindung | [Erfahren Sie, wie Sie Decisioning verwenden](../experience-decisioning/gs-experience-decisioning.md) |
| **KI-gestützte Rangfolge** | Angebotsauswahl mithilfe von maschinellem Lernen optimieren | Hängt von Ihrer Lizenz ab | Hängt von Ihrer Lizenz ab | Hängt von Ihrer Lizenz ab | Entscheidungsfindung | [Erfahren Sie mehr über KI-Modelle](../offers/ranking/ai-models.md) |

>[!TAB Auswählen / Prime / Ultimate]

Diese Registerkarte gilt für Kunden mit bestehenden Lizenzvereinbarungen, die die Paketterminologie Select, Prime oder Ultimate verwenden.

## Paketzusammenfassungen {#package-summaries}

+++**Auswählen**

Am besten geeignet für Organisationen, die mit Batch- und Transaktionsnachrichten beginnen:

- Geplante Batch-Kampagnen und Transaktionsnachrichten
- Ausführung von Core-Kampagnen und Journey
- Grundlagen für E-Mail-, SMS-, Push- und benutzerdefinierte Aktionskanäle
- Schutzmaßnahmen bei der Standardorchestrierung

+++

+++**Prime**

Umfasst alles in Select sowie Echtzeit-Orchestrierung und eingehende Kanäle:

- Ereignisgesteuerte Journey-Orchestrierung in Echtzeit
- Eingehende Kanäle: Web, In-App-Messaging, Code-basierte Erlebnisse, Inhaltskarten und Briefpost
- Erweiterte Zielgruppensegmentierung und Zielgruppenbestimmung

+++

+++**Ultimate**

Umfasst alles in Prime sowie Entscheidungsfindung und erweiterte Optimierung:

- Echtzeit-Angebotsentscheidung und Personalisierung
- KI-gestützte Ranking- und Optimierungsmodelle
- Erweiterte Reporting- und Experimentierfunktionen

+++

## Funktionsmatrix {#capability-matrix-legacy}

| Funktion | Mögliche Optionen | Auswählen | Prime | Ultimate | Weitere Informationen |
|-----------|----------------|:------:|:-----:|:--------:|-----------|
| **E-Mail** | Gestalten und Senden personalisierter E-Mail-Nachrichten | Eingeschlossen | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie E-Mails senden](../email/get-started-email.md) |
| **SMS/MMS** | Senden von Text- und Multimedia-Nachrichten | Eingeschlossen | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie Nachrichten an Mobilgeräte senden](../mobile/get-started-mobile.md) |
| **Push-Benachrichtigungen** | Mobile Push-Benachrichtigungen senden | Eingeschlossen | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie Push-Benachrichtigungen senden](../push/get-started-push.md) |
| **Batch-Kampagnen** | Planen von Nachrichten für eine Audience | Eingeschlossen | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie Kampagnen erstellen](../campaigns/get-started-with-campaigns.md) |
| **Automated Journey** | Entwerfen von ereignisgesteuerten Kunden-Journey | Eingeschlossen | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie Journey bauen](../building-journeys/journey-gs.md) |
| **Echtzeit-Journey-Trigger** | Reagieren auf Kundenverhalten, sobald es passiert | — | Eingeschlossen | Eingeschlossen | [Erfahren Sie mehr über Journey-Ereignisse](../event/about-events.md) |
| **In-App-Messaging** | Anzeigen von Nachrichten in Ihrer Mobile App | — | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie In-App-Messaging verwenden](../in-app/get-started-in-app.md) |
| **Web-Kanal** | Web-Seiten in Echtzeit personalisieren | — | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie den Web-Kanal verwenden](../web/get-started-web.md) |
| **Code-basierte Erlebnisse** | Jede Oberfläche über API oder SDK personalisieren | — | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie Code-basierte Erlebnisse verwenden](../code-based/get-started-code-based.md) |
| **Inhaltskarten** | Versand persistenter, nicht aufdringlicher produktinterner Nachrichten | — | Eingeschlossen | Eingeschlossen | [Erfahren Sie, wie Sie Inhaltskarten verwenden](../content-card/get-started-content-card.md) |
| **Briefpost** | Erstellen und Senden von physischen Postsendungen | — | Verfügbar mit Prime und höher | Eingeschlossen | [Erfahren Sie, wie Sie Briefpost verwenden](../direct-mail/get-started-direct-mail.md) |
| **Entscheidungsfindung** | Das beste Angebot für jeden Kunden in Echtzeit auswählen | — | – | Eingeschlossen | [Erfahren Sie, wie Sie Decisioning verwenden](../experience-decisioning/gs-experience-decisioning.md) |
| **KI-gestützte Rangfolge** | Optimieren der Angebots- und Inhaltsauswahl mithilfe von maschinellem Lernen | — | – | Eingeschlossen | [Erfahren Sie mehr über KI-Modelle](../offers/ranking/ai-models.md) |
| **WhatsApp** | Nachrichten über WhatsApp Business senden | Hängt von Ihrer Lizenz und der Kanalkonfiguration ab | Hängt von Ihrer Lizenz und der Kanalkonfiguration ab | Hängt von Ihrer Lizenz und der Kanalkonfiguration ab | [Erfahren Sie, wie Sie WhatsApp verwenden](../whatsapp/get-started-whatsapp.md) |

>[!ENDTABS]
