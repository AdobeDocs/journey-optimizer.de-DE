---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer-Pakete und -Funktionen
description: Erfahren Sie, wie Adobe Journey Optimizer gepackt wird und welche Funktionen basierend auf Ihrem Basisangebot, Kanal-Add-ons und Add-ons für erweiterte Funktionen verfügbar sind, einschließlich einer Referenz für die Paketerstellung mit Legacy Select, Prime und Ultimate.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: Journey Optimizer, Paket, Lizenz, Kampagnen, Journey, Kanäle, Entscheidungsfindung, Outbound, Mobil, Web, modular, SMS, MMS, WhatsApp, Add-ons, Select, Prime, Ultimate, Legacy
hide: true
source-git-commit: ef26246dd1bcd820bab1f226c3564a600ac5b506
workflow-type: tm+mt
source-wordcount: '1992'
ht-degree: 2%

---


# Adobe Journey Optimizer-Pakete und -Funktionen {#ajo-packages}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie die modulare Adobe Journey Optimizer-Paketerstellung für Basisangebote, Kanal-Add-ons und das Decisioning-Add-on funktioniert, damit Sie die Kombination auswählen können, die zu Ihren Interaktions-Anwendungsfällen und Ihrem Budget passt.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] verwendet ein modulares Verpackungsmodell. Beginnen Sie mit dem Basisangebot, das Ihrem primären Anwendungsfall entspricht, und fügen Sie dann die benötigten Kanäle und erweiterten Funktionen hinzu.

>[!TIP]
>
>**Nicht sicher, auf welchem Modell Sie sind?** Wenn Sie [!DNL Adobe Journey Optimizer] unter dem modularen Verpackungsmodell gekauft haben, gelten die auf dieser Seite beschriebenen Basisangebote und Add-ons für Sie. Wenn in Ihrem Vertrag **Select**, **Prime** oder **Ultimate** referenziert wird, verwenden Sie ein veraltetes Verpackungsmodell. Wenden Sie sich zur Bestätigung Ihrer aktuellen Berechtigungen an Ihren Adobe-Support-Mitarbeiter.

>[!NOTE]
>
>Die Verfügbarkeit und die enthaltenen Funktionen hängen von Ihrer Vereinbarung, den ausgewählten Add-ons und der regionalen Verfügbarkeit ab. Wenden Sie sich an den Adobe-Support, um spezifische Informationen zu Ihrem Unternehmen zu erhalten.

## Schnelle Antworten {#quick-answers}

Zwei Fragen, die die meisten Leute haben, bevor sie weiterlesen. Die [FAQ](#faq) finden Sie unten auf der Seite.

+++**Enthält jedes Basisangebot jeden Kanal?**

Nein. [!DNL Adobe Journey Optimizer] verwendet ein modulares Modell: Das Basisangebot bestimmt Ihre Orchestrierungsfähigkeit (Kampagnen, Journey oder beides), und Kanal-Add-ons bestimmen, welche Messaging-Oberflächen Sie ansprechen können. Sie wählen die Kombination aus, die Ihrem Anwendungsfall und Budget entspricht.

+++

+++**Was ist der Unterschied zwischen Kampagnen und Journey?**

**[Kampagnen](../campaigns/get-started-with-campaigns.md)** sind zielgruppenbasiert und werden von Marketing-Experten geplant. Sie definieren eine Zielgruppe, erstellen eine Nachricht und planen oder Triggern sie als Batch-Versand. Sie eignen sich am besten für Werbeaktionen, Newsletter und mehrstufige Zielgruppen-Workflows.

**[Journey](../building-journeys/journey-gs.md)** sind in Echtzeit und ereignisgesteuert - sie reagieren sofort auf das individuelle Kundenverhalten und orchestrieren 1:1 Erlebnisse über Touchpoints hinweg. Sie eignen sich am besten für Onboarding-Flüsse, Nachkaufsequenzen und in Echtzeit ausgelöste Nachrichten.

**Kampagnen und Journey** bietet Ihnen beide Funktionen in einer einzigen Lizenz.

+++

## Schritt 1: Identifizieren Ihres Basisangebots {#base-offers}

>[!NOTE]
>
>**Journey Optimizer wird ausgewertet?** In diesem Schritt wählen Sie das Basisangebot aus, das zu Ihrer Interaktionsstrategie passt. **Sie sind bereits Kunde?** So bestätigen Sie, welches Basisangebot Sie haben und was es tut.

Es stehen drei Basisangebote zur Verfügung. Jede Version entspricht einer anderen Methode, Kunden anzusprechen.

| Basisangebot | Geeignet für | Kernverhalten |
|-----------|---------|--------------|
| **[Journey Optimizer - Kampagnen](../campaigns/get-started-with-campaigns.md)** | Batch-Kontaktaufnahme durch Marketing-Experten | Zielgruppenbasierte, geplante Orchestrierung. Ein- oder mehrstufige Kampagnen-Workflows für Batch-Interaktionen und von Marketing-Experten geplante Kontaktaufnahme. |
| **[Journey Optimizer - Journey](../building-journeys/journey-gs.md)** | Echtzeit-Kundeninteraktion | Ereignisgesteuert, 1:1 Orchestrierung. Unterstützt sowohl die Bereitstellung in Echtzeit als auch die geplante Journey. |
| **Journey Optimizer - Kampagnen und Journey** | Kunden, die beides benötigen | Kombiniert die zielgruppenbasierte Kampagnenorchestrierung und die Echtzeit-Journey-Orchestrierung. |

>[!IMPORTANT]
>
>**Speicherberechtigungen unterscheiden sich je nach Paket.** Die Gesamtberechtigung für das Datenvolumen hängt von Ihrem Basisangebot ab: **Kampagnen**-Kunden erhalten **15 KB** **pro adressierbarem Profil, während** Journey- und **Kampagnen und Journey**-Kunden **75 KB** pro adressierbarem Profil erhalten. Berücksichtigen Sie dies bei der Auswahl oder Bestätigung Ihres Pakets.

### Kampagnen vs. Journey - was ist der Unterschied? {#campaigns-vs-journeys}

| | Journey Optimizer - Kampagnen | JOURNEY OPTIMIZER - JOURNEY | Journey Optimizer - Kampagnen und Journey |
|--|:-----------------------------:|:----------------------------:|:----------------------------------------:|
| [Zielgruppenbasierte Batch-Orchestrierung](../campaigns/get-started-with-campaigns.md) | ✓ | Limited¹ | ✓ |
| [Ereignisgesteuerte Orchestrierung in Echtzeit](../building-journeys/journey-gs.md) | – | ✓ | ✓ |
| Transaktionsnachrichten (E-Mail, Push, SMS) | ✓ | ✓ | ✓ |
| [Channel-Add-ons verfügbar](#channel-addons) | ✓ | ✓ | ✓ |
| [Decisioning-Add-on verfügbar](#decisioning-addon) | ✓ | ✓ | ✓ |

¹ In **Journey Optimizer - Journey** wird die zielgruppenbasierte Orchestrierung nur innerhalb von Journey-Anwendungsfällen unterstützt, nicht als eigenständige Batch-Kampagnen.

## Schritt 2 - Fügen Sie die benötigten Kanäle hinzu {#channel-addons}

Kanäle sind nicht im Basisangebot gebündelt. Wählen Sie das Kanal-Add-on oder -Add-on-Bundle aus, das zu Ihrer Interaktionsstrategie passt.

>[!BEGINTABS]

>[!TAB ✉️ ausgehende Zustellung]

Zielgruppen über ausgehende Nachrichtenkanäle erreichen.

**Enthält:** [E-Mail](../email/get-started-email.md), [Push-](../push/get-started-push.md), [Briefpost](../direct-mail/get-started-direct-mail.md)

**Typische Anwendungsfälle:** Werbe-E-Mails, Transaktions-Push-Benachrichtigungen, physische E-Mail-Kampagnen

**Unterstützte Oberflächen:** Posteingang, Sperrbildschirm für Mobilgeräte / Benachrichtigungsfach, Postanschrift

Umfasst die Zustellbarkeitsgrundlagen für die Unterstützung von IP-Warming auf neuen Instanzen. Für die laufende Überwachung und den von Beratern geleiteten Support **drei „Zustellbarkeitspakete** (Essentials, Enhanced und Plus) als separate Add-ons verfügbar. [Erfahren Sie mehr über die Zustellbarkeit](../reports/deliverability.md)

>[!TAB 📱 mobil]

Interagieren Sie App-Benutzer mit sitzungsinternen und persistenten mobilen Erlebnissen.

**Umfasst** [In-App-Messaging](../in-app/get-started-in-app.md), [Push-Benachrichtigungen](../push/get-started-push.md), [Inhaltskarten](../content-card/get-started-content-card.md) [Code-basierte Kanäle](../code-based/get-started-code-based.md) für mobile Oberflächen

**Typische Anwendungsfälle:**-Onboarding-Flüsse, Funktionsankündigungen, Loyalitäts-Stupser, In-App-Angebote in Echtzeit

**Unterstützte Oberflächen:** Bildschirme der mobilen App, Benachrichtigungsablage, persistente Inhaltssteckplätze, benutzerdefinierte App-Oberflächen über SDK

>[!TAB 🌐 Web]

Personalisieren von Web-Erlebnissen ohne Bereitstellung von Code.

**Enthält:**[Webkanal](../web/get-started-web.md) (visueller und nicht visueller Editor), [Code-basierte Kanäle](../code-based/get-started-code-based.md) für Web-Oberflächen

**Typische Anwendungsfälle:** Homepage-Banner, Landingpage-Personalisierung, A/B-Tests, Headless Web-Personalisierung über API

**Unterstützte Oberflächen:** Browser-Seiten, Single Page Apps (SPA), Headless-Web-Endpunkte

>[!TAB 📦 alle Kanäle]

Das **Alle Kanäle**-Add-on bündelt den ausgehenden Versand + Mobile + Web in einem einzigen Kauf.

**Umfasst:** jeden Kanal der drei einzelnen Add-ons - [E-Mail](../email/get-started-email.md), [Push-Benachrichtigungen](../push/get-started-push.md), [Briefpost](../direct-mail/get-started-direct-mail.md), [In-App-Messaging](../in-app/get-started-in-app.md), [Inhaltskarten](../content-card/get-started-content-card.md), [Webkanal](../web/get-started-web.md) und [Code-basierte Kanäle](../code-based/get-started-code-based.md)

**Typische Anwendungsfälle:** koordinierte Omni-Channel-Programme, die ausgehende, mobile Apps und das Web umfassen - z. B. eine Kampagne, die einer E-Mail mit einer In-App-Nachricht und einem personalisierten Webbanner folgt

**Unterstützte Oberflächen:** alle Oberflächen aus den Add-ons „Ausgehender Versand“, „Mobile“ und „Web“

>[!NOTE]
>
>Das **Alle Kanäle**-Bundle ist in der Regel kostengünstiger als die Lizenzierung von Ausgehender Bereitstellung, Mobile und Web separat. Wenn Sie alle drei Optionen voraussichtlich verwenden werden, bitten Sie Ihren Adobe-Support-Mitarbeiter, die Paketpreise mit den individuellen Add-ons zu vergleichen.

>[!ENDTABS]

### Zusätzliche Kanäle {#additional-channels}

Einige Kanäle sind nicht an ein Einkanal-Add-on gebunden. Ihre Verfügbarkeit hängt von Ihrer lizenzierten Konfiguration, Vereinbarung und - für Partnerkanäle - einem Geschäftskonto eines Drittanbieters ab.

**📲SMS / MMS** — Senden von Text- und Multimedia-Nachrichten an Mobiltelefonnummern. Transaktions-SMS (in Echtzeit, ereignisgesteuert) werden von jedem Basisangebot unterstützt. Eine breitere Marketing-Nutzung von SMS/MMS hängt von Ihrer lizenzierten Konfiguration ab. [Erfahren Sie, wie Sie Nachrichten an Mobilgeräte senden](../mobile/get-started-mobile.md)

**💬WhatsApp** - Senden von Nachrichten über WhatsApp Business. Erfordert ein WhatsApp Business-Konto und die Verfügbarkeit hängt von Ihrer Vereinbarung und der lizenzierten Konfiguration ab. [Erfahren Sie, wie Sie WhatsApp verwenden](../whatsapp/get-started-whatsapp.md)

>[!NOTE]
>
>Bestätigen Sie die Verfügbarkeit von SMS/MMS und WhatsApp für Ihr Unternehmen mit Ihrem Adobe-Support-Mitarbeiter. Diese Kanäle sind nicht Teil der standardmäßigen Add-ons für ausgehende Sendungen, Mobilgeräte oder Web.

## Schritt 3 - Erweiterte Funktionen hinzufügen {#advanced-addons}

### Entscheidungsfindung {#decisioning-addon}

Mit dem **Decisioning**-Add-on können Sie für jedes Profil in Echtzeit und über jeden Kanal hinweg das beste Angebot, die beste Aktion oder das beste Erlebnis definieren, verwalten und bereitstellen.

**Was es freischaltet:**
- Auswahl von Angeboten in Echtzeit mithilfe von Eignungsregeln, Ranking-Logik und Einschränkungen
- KI-gestützte Ranking-Modelle zur automatischen Optimierung der Angebotsleistung
- Entscheidungsrichtlinien, die in Journey, Kampagnen und Code-basierten Erlebnissen verwendet werden können

**Verfügbar unter** Alle drei Basisangebote, vorbehaltlich Ihrer Lizenzvereinbarung. [Erfahren Sie, wie Sie Decisioning verwenden](../experience-decisioning/gs-experience-decisioning.md) | [Erfahren Sie mehr über KI-Modelle](../offers/ranking/ai-models.md)

## Vergleichen auf einen Blick {#comparison-matrix}

Die Funktionen sind in zwei Tabellen unterteilt, sodass jede einfach zu scannen ist: Die Orchestrierungsfunktionen werden von Ihrem **Basisangebot** bestimmt, während Kanäle und erweiterte Funktionen von **Add-ons** entsperrt werden.

### Orchestrierungsfunktionen {#orchestration-capabilities}

Bestimmt durch Ihr Basisangebot.

| Funktion | Kampagnen | Journeys | Kampagnen und Journey |
|-----------|:---------:|:--------:|:--------------------:|
| Transaktionsnachrichten ([E-Mail](../email/get-started-email.md), [Push](../push/get-started-push.md), [SMS](../mobile/get-started-mobile.md)) | ✓ | ✓ | ✓ |
| [Batch-Kampagnen](../campaigns/get-started-with-campaigns.md) | ✓ | – | ✓ |
| [Orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) _(nur E-Mail, SMS, Push, Briefpost)_ | ✓ | – | ✓ |
| [Automated Journey](../building-journeys/journey-gs.md) | – | ✓ | ✓ |
| [Echtzeit-Ereignis-Trigger ](../event/about-events.md) | – | ✓ | ✓ |

### Kanäle und erweiterte Funktionen {#channel-capabilities}

Die meisten Kanäle sind für alle drei Basisangebote verfügbar und erfordern das aufgelistete Add-on. Einige wenige - wie SMS / MMS und WhatsApp - hängen von Ihrer lizenzierten Konfiguration ab.

| Funktion | Verfügbarkeit | Add-on erforderlich |
|-----------|-------------|----------------|
| [E-Mail](../email/get-started-email.md) | Alle Basisangebote | Ausgehender Versand |
| [Push-Benachrichtigungen ](../push/get-started-push.md) | Alle Basisangebote | Ausgehender Versand |
| [Briefpost](../direct-mail/get-started-direct-mail.md) | Alle Basisangebote | Ausgehender Versand |
| [SMS/MMS](../mobile/get-started-mobile.md) | Basierend auf Ihrer lizenzierten Konfiguration | Basierend auf Ihrer lizenzierten Konfiguration |
| [In-App-Messaging](../in-app/get-started-in-app.md) | Alle Basisangebote | Mobile |
| [Inhaltskarten](../content-card/get-started-content-card.md) | Alle Basisangebote | Mobile |
| [Web-Kanal](../web/get-started-web.md) | Alle Basisangebote | Web |
| [Code-basierte Erlebnisse](../code-based/get-started-code-based.md) | Alle Basisangebote | Mobil oder Web |
| [WhatsApp](../whatsapp/get-started-whatsapp.md) | Basierend auf Ihrer lizenzierten Konfiguration | WhatsApp |
| [Entscheidungsfindung](../experience-decisioning/gs-experience-decisioning.md) | Abhängig von der Lizenz | Entscheidungsfindung |
| [KI-gestützte Rangfolge](../offers/ranking/ai-models.md) | Abhängig von der Lizenz | Entscheidungsfindung |

>[!NOTE]
>
>**Transaktionsnachrichten im Vergleich zu Kanal-Add-ons.** Jedes Basisangebot enthält grundlegende Transaktionsnachrichten (ereignisgesteuerte E-Mail, Push und SMS). Die **Ausgehende**, **Mobile** und **Web** ermöglichen die vollständige Marketing- und Kampagnennutzung dieser Kanäle sowie der oben aufgeführten zusätzlichen Oberflächen.

## Häufig gestellte Fragen {#faq}

+++**Welche Kanäle werden in orchestrierten Kampagnen unterstützt?**

[Orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) (mehrstufige Zielgruppen-Workflows mit der Kampagnenorchestrierungsfunktion) unterstützen nur **E-Mail, SMS, Push-Benachrichtigungen und Briefpost**. Web-, In-App-, Code-basierte und Inhaltskarten-Kanäle werden in orchestrierten Kampagnen-Workflows nicht unterstützt.

+++

+++**Ist Decisioning in jeder Konfiguration enthalten?**

Nein. Decisioning ist ein eindeutiges Add-on für erweiterte Funktionen und standardmäßig in keinem Basisangebot enthalten. Wenden Sie sich an den Adobe-Support, um Ihrer Konfiguration Decisioning hinzuzufügen.

+++

+++**Ich habe von Select, Prime oder Ultimate gehört. Sind sie immer noch das aktuelle Verpackungsmodell?**

[!DNL Adobe Journey Optimizer] wird jetzt durch ein modulares Verpackungsmodell angeboten, das auf Basisangeboten (Kampagnen, Journey, Kampagnen und Journey) und Add-ons aufbaut. Wenn Sie Bestandskunde sind und die Terminologie von Select, Prime oder Ultimate verwenden, finden Sie unten unter [Legacy-](#legacy-packaging)) eine Funktionsreferenz, oder wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Ihre aktuellen Berechtigungen zu bestätigen.

+++

## Legacy-Packaging - Select, Prime und Ultimate {#legacy-packaging}

Die obigen Abschnitte beschreiben das aktuelle modulare Verpackungsmodell. Wenn in Ihrer Vereinbarung weiterhin die Terminologie **Select**, **Prime** oder **Ultimate** verwendet wird, erweitern Sie den unten stehenden Verweis, um zu sehen, was jedes Legacy-Paket enthält. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um zum modularen Modell zu wechseln.

+++**Alte Paketreferenz anzeigen**

**Paketzusammenfassungen**

**Select** - Am besten geeignet für Organisationen, die mit Batch- und Transaktionsnachrichten beginnen:

- Geplante Batch-Kampagnen und Transaktionsnachrichten
- Ausführung von Core-Kampagnen und Journey
- Grundlagen für E-Mail-, SMS-, Push- und benutzerdefinierte Aktionskanäle
- Schutzmaßnahmen bei der Standardorchestrierung

**Prime** - Enthält alles in Select sowie Echtzeit-Orchestrierung und eingehende Kanäle:

- Ereignisgesteuerte Journey-Orchestrierung in Echtzeit
- Eingehende Kanäle: Web, In-App-Messaging, Code-basierte Erlebnisse, Inhaltskarten und Briefpost
- Erweiterte Zielgruppensegmentierung und Zielgruppenbestimmung

**Ultimate** - Enthält alles in Prime sowie Entscheidungsfindung und erweiterte Optimierung:

- Echtzeit-Angebotsentscheidung und Personalisierung
- KI-gestützte Ranking- und Optimierungsmodelle
- Erweiterte Reporting- und Experimentierfunktionen

**Alte Funktionsmatrix**

| Funktion | Mögliche Optionen | Auswählen | Prime | Ultimate | Weitere Informationen |
|-----------|----------------|:------:|:-----:|:--------:|-----------|
| **E-Mail** | Gestalten und Senden personalisierter E-Mail-Nachrichten | ✓ | ✓ | ✓ | [Erfahren Sie, wie Sie E-Mails senden](../email/get-started-email.md) |
| **SMS/MMS** | Senden von Text- und Multimedia-Nachrichten | ✓ | ✓ | ✓ | [Erfahren Sie, wie Sie Nachrichten an Mobilgeräte senden](../mobile/get-started-mobile.md) |
| **Push-Benachrichtigungen** | Mobile Push-Benachrichtigungen senden | ✓ | ✓ | ✓ | [Erfahren Sie, wie Sie Push-Benachrichtigungen senden](../push/get-started-push.md) |
| **Batch-Kampagnen** | Planen von Nachrichten für eine Audience | ✓ | ✓ | ✓ | [Erfahren Sie, wie Sie Kampagnen erstellen](../campaigns/get-started-with-campaigns.md) |
| **Automated Journey** | Entwerfen von ereignisgesteuerten Kunden-Journey | ✓ | ✓ | ✓ | [Erfahren Sie, wie Sie Journey bauen](../building-journeys/journey-gs.md) |
| **Echtzeit-Journey-Trigger** | Reagieren auf Kundenverhalten, sobald es passiert | – | ✓ | ✓ | [Erfahren Sie mehr über Journey-Ereignisse](../event/about-events.md) |
| **In-App-Messaging** | Anzeigen von Nachrichten in Ihrer Mobile App | – | ✓ | ✓ | [Erfahren Sie, wie Sie In-App-Messaging verwenden](../in-app/get-started-in-app.md) |
| **Web-Kanal** | Web-Seiten in Echtzeit personalisieren | – | ✓ | ✓ | [Erfahren Sie, wie Sie den Web-Kanal verwenden](../web/get-started-web.md) |
| **Code-basierte Erlebnisse** | Jede Oberfläche über API oder SDK personalisieren | – | ✓ | ✓ | [Erfahren Sie, wie Sie Code-basierte Erlebnisse verwenden](../code-based/get-started-code-based.md) |
| **Inhaltskarten** | Versand persistenter, nicht aufdringlicher produktinterner Nachrichten | – | ✓ | ✓ | [Erfahren Sie, wie Sie Inhaltskarten verwenden](../content-card/get-started-content-card.md) |
| **Briefpost** | Erstellen und Senden von physischen Postsendungen | – | Verfügbar mit Prime und höher | ✓ | [Erfahren Sie, wie Sie Briefpost verwenden](../direct-mail/get-started-direct-mail.md) |
| **Entscheidungsfindung** | Das beste Angebot für jeden Kunden in Echtzeit auswählen | — | – | ✓ | [Erfahren Sie, wie Sie Decisioning verwenden](../experience-decisioning/gs-experience-decisioning.md) |
| **KI-gestützte Rangfolge** | Optimieren der Angebots- und Inhaltsauswahl mithilfe von maschinellem Lernen | — | – | ✓ | [Erfahren Sie mehr über KI-Modelle](../offers/ranking/ai-models.md) |
| **WhatsApp** | Nachrichten über WhatsApp Business senden | Hängt von Ihrer Lizenz und der Kanalkonfiguration ab | Hängt von Ihrer Lizenz und der Kanalkonfiguration ab | Hängt von Ihrer Lizenz und der Kanalkonfiguration ab | [Erfahren Sie, wie Sie WhatsApp verwenden](../whatsapp/get-started-whatsapp.md) |

+++

## Nächste Schritte {#next-steps}

Nachdem Sie nun wissen, wie [!DNL Adobe Journey Optimizer] verpackt ist, können Sie als Nächstes Folgendes tun:

- **Erste Schritte mit dem Produkt** - Richten Sie Ihre Umgebung ein und lernen Sie die wichtigsten Konzepte kennen. [Erste Schritte mit Journey Optimizer](get-started.md)
- **Implementierung planen** - Folgen Sie dem strukturierten Onboarding-Pfad für Ihr Projekt. [Onboarding-Projekthandbuch](onboarding-hub.md)
- **Funktionsverfügbarkeit überprüfen** - Überprüfen Sie, welche Funktionen live sind, ihren Lebenszyklusstatus (GA/LA/Beta) und wann sie versandt wurden. [Funktionsverfügbarkeit](ajo-features-availability.md)
- **Finden des richtigen Anwendungsfalls** - Ordnen Sie Ihre Interaktionsziele den Funktionen zu, die sie unterstützen. [Leitfaden für Anwendungsfälle](ajo-use-case-guide.md)
- **Konfigurieren Sie Ihre Kanäle** - Sobald Sie wissen, welche Add-ons Sie haben, richten Sie die benötigten Kanäle ein: [E-Mail](../email/get-started-email.md), [Push-Benachrichtigungen](../push/get-started-push.md), [SMS/MMS](../mobile/get-started-mobile.md), [In-App-Messaging](../in-app/get-started-in-app.md), [Inhaltskarten](../content-card/get-started-content-card.md), [der Web-Kanal](../web/get-started-web.md) und [Code-basierte Erlebnisse](../code-based/get-started-code-based.md).
