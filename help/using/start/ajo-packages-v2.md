---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-Pakete und -Funktionen
description: Erfahren Sie, wie Adobe Journey Optimizer gepackt wird und welche Funktionen basierend auf Ihrem Basisangebot, Kanal-Add-ons und Add-ons für erweiterte Funktionen verfügbar sind.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: Journey Optimizer, Paket, Lizenz, Kampagnen, Journey, Kanäle, Decisioning, Outbound, Mobile, Web, modular
hide: true
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 3%

---


# Adobe Journey Optimizer-Pakete und -Funktionen {#ajo-packages-v2}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie die modulare Adobe Journey Optimizer-Paketerstellung für Basisangebote, Kanal-Add-ons und das Decisioning-Add-on funktioniert, damit Sie die Kombination auswählen können, die zu Ihren Interaktions-Anwendungsfällen und Ihrem Budget passt.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] verwendet ein modulares Verpackungsmodell. Beginnen Sie mit dem Basisangebot, das Ihrem primären Anwendungsfall entspricht, und fügen Sie dann die benötigten Kanäle und erweiterten Funktionen hinzu.

>[!NOTE]
>
>Die Verfügbarkeit und die enthaltenen Funktionen hängen von Ihrer Vereinbarung, den ausgewählten Add-ons und der regionalen Verfügbarkeit ab. Wenden Sie sich an den Adobe-Support, um spezifische Informationen zu Ihrem Unternehmen zu erhalten.

## Schritt 1: Wählen Sie Ihr Basisangebot {#base-offers}

Es stehen drei Basisangebote zur Verfügung. Wählen Sie diejenige aus, die zu Ihrer primär an Kunden gerichteten Interaktion passt.

| Basisangebot | Geeignet für | Kernverhalten |
|-----------|---------|--------------|
| **Journey Optimizer - Kampagnen** | Batch-Kontaktaufnahme durch Marketing-Experten | Zielgruppenbasierte, geplante Orchestrierung. Ein- oder mehrstufige Kampagnen-Workflows unter Verwendung des relationalen Datenspeichers. |
| **Journey Optimizer - Journey** | Echtzeit-Kundeninteraktion | Ereignisgesteuert, 1:1 Orchestrierung. Unterstützt sowohl Streaming als auch Batch-Journey. |
| **Journey Optimizer - Kampagnen und Journey** | Kunden, die beides benötigen | Kombiniert die zielgruppenbasierte Kampagnenorchestrierung und die Echtzeit-Journey-Orchestrierung. |

### Kampagnen vs. Journey - was ist der Unterschied? {#campaigns-vs-journeys}

| | Journey Optimizer - Kampagnen | JOURNEY OPTIMIZER - JOURNEY | Journey Optimizer - Kampagnen und Journey |
|--|:-----------------------------:|:----------------------------:|:----------------------------------------:|
| Zielgruppenbasierte Batch-Orchestrierung | ✓ | Auf Journey-Anwendungsfälle beschränkt | ✓ |
| Ereignisgesteuerte Orchestrierung in Echtzeit | — | ✓ | ✓ |
| Transaktionsnachrichten (E-Mail, Push, SMS) | ✓ | ✓ | ✓ |
| Verfügbare Kanal-Add-ons | ✓ | ✓ | ✓ |
| Decisioning-Add-on verfügbar | ✓ | ✓ | ✓ |

>[!NOTE]
>
>Die Berechtigung für das gesamte Datenvolumen unterscheidet sich: **Kampagnen**-Kunden erhalten 15 KB pro adressierbarem Profil; **Journey** und **Kampagnen und Journey**-Kunden erhalten 75 KB pro adressierbarem Profil.

## Schritt 2 - Fügen Sie die benötigten Kanäle hinzu {#channel-addons}

Kanäle sind nicht im Basisangebot gebündelt. Wählen Sie das Kanal-Add-on oder -Add-on-Bundle aus, das zu Ihrer Interaktionsstrategie passt.

>[!BEGINTABS]

>[!TAB Ausgehender Versand]

Zielgruppen über ausgehende Nachrichtenkanäle erreichen.

**Umfasst:**-E-Mail, Push-Benachrichtigungen, Briefpost

**Typische Anwendungsfälle:** Werbe-E-Mails, Transaktions-Push-Benachrichtigungen, physische E-Mail-Kampagnen

**Unterstützte Oberflächen:** Posteingang, Sperrbildschirm für Mobilgeräte / Benachrichtigungsfach, Postanschrift

Umfasst die Zustellbarkeitsgrundlagen für die Unterstützung von IP-Warming auf neuen Instanzen. [Erfahren Sie mehr über die Zustellbarkeit](../reports/deliverability.md)

>[!TAB Mobile]

Interagieren Sie App-Benutzer mit sitzungsinternen und persistenten mobilen Erlebnissen.

**Umfasst** In-App-Messaging, Push-Benachrichtigungen, Inhaltskarten, Code-basierte Kanäle für mobile Oberflächen

**Typische Anwendungsfälle:**-Onboarding-Flüsse, Funktionsankündigungen, Loyalitäts-Stupser, In-App-Angebote in Echtzeit

**Unterstützte Oberflächen:** Bildschirme der mobilen App, Benachrichtigungsablage, persistente Inhaltssteckplätze, benutzerdefinierte App-Oberflächen über SDK

>[!TAB Web]

Personalisieren von Web-Erlebnissen ohne Bereitstellung von Code.

**Umfasst:** Webkanal (visueller und nicht visueller Editor), Code-basierte Kanäle für Web-Oberflächen

**Typische Anwendungsfälle:** Homepage-Banner, Landingpage-Personalisierung, A/B-Tests, Headless Web-Personalisierung über API

**Unterstützte Oberflächen:** Browser-Seiten, Single Page Apps (SPA), Headless-Web-Endpunkte

>[!TAB Alle Kanäle]

Das **Alle Kanäle**-Add-on bündelt den ausgehenden Versand + Mobile + Web in einem einzigen Kauf.

Am besten geeignet für Organisationen, die eine vollständige Omni-Channel-Abdeckung über ausgehende, mobile Apps und Web-Oberflächen benötigen.

>[!ENDTABS]

**WhatsApp** ist als separates Add-on für Kunden verfügbar, die Nachrichten über WhatsApp Business senden müssen. [Erfahren Sie, wie Sie WhatsApp verwenden](../whatsapp/get-started-whatsapp.md)

## Schritt 3 - Erweiterte Funktionen hinzufügen {#advanced-addons}

### Entscheidungsfindung {#decisioning-addon}

Mit dem **Decisioning**-Add-on können Sie für jedes Profil in Echtzeit und über jeden Kanal hinweg das beste Angebot, die beste Aktion oder das beste Erlebnis definieren, verwalten und bereitstellen.

**Was es freischaltet:**
- Auswahl von Angeboten in Echtzeit mithilfe von Eignungsregeln, Ranking-Logik und Einschränkungen
- KI-gestützte Ranking-Modelle zur automatischen Optimierung der Angebotsleistung
- Entscheidungsrichtlinien, die in Journey, Kampagnen und Code-basierten Erlebnissen verwendet werden können

**Verfügbar unter** Alle drei Basisangebote, vorbehaltlich Ihrer Lizenzvereinbarung. [Erfahren Sie, wie Sie Decisioning verwenden](../experience-decisioning/gs-experience-decisioning.md) | [Erfahren Sie mehr über KI-Modelle](../offers/ranking/ai-models.md)

## Vergleichen auf einen Blick {#comparison-matrix}

| Funktion | Journey Optimizer - Kampagnen | JOURNEY OPTIMIZER - JOURNEY | Journey Optimizer - Kampagnen und Journey | Add-on erforderlich |
|-----------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|
| Transaktionsnachrichten (E-Mail, Push, SMS) | ✓ | ✓ | ✓ | — |
| Batch-Kampagne | ✓ | — | ✓ | – |
| Orchestrierte Kampagnen _(nur E-Mail, SMS, Push, Briefpost)_ | ✓ | — | ✓ | – |
| Automatisierte Journey | — | ✓ | ✓ | – |
| Echtzeit-Ereignis-Trigger | — | ✓ | ✓ | – |
| E-Mail | ✓ | ✓ | ✓ | Ausgehender Versand |
| Push-Benachrichtigungen | ✓ | ✓ | ✓ | Ausgehender Versand |
| Briefpost | ✓ | ✓ | ✓ | Ausgehender Versand |
| SMS/MMS | ✓ | ✓ | ✓ | Ausgehender Versand |
| In-App-Messaging | ✓ | ✓ | ✓ | Mobile |
| Inhaltskarten | ✓ | ✓ | ✓ | Mobile |
| Web-Kanal | ✓ | ✓ | ✓ | Web |
| Code-basierte Erlebnisse | ✓ | ✓ | ✓ | Mobil oder Web |
| WhatsApp | ✓ | ✓ | ✓ | WhatsApp |
| Entscheidungsfindung | Abhängig von der Lizenz | Abhängig von der Lizenz | Abhängig von der Lizenz | Entscheidungsfindung |
| KI-gestützte Rangfolge | Abhängig von der Lizenz | Abhängig von der Lizenz | Abhängig von der Lizenz | Entscheidungsfindung |

## Häufig gestellte Fragen {#faq}

+++**Enthält jedes Basisangebot jeden Kanal?**

Nein. [!DNL Adobe Journey Optimizer] verwendet ein modulares Modell: Das Basisangebot bestimmt Ihre Orchestrierungsfähigkeit (Kampagnen, Journey oder beides), und Kanal-Add-ons bestimmen, welche Messaging-Oberflächen Sie ansprechen können. Sie wählen die Kombination aus, die Ihrem Anwendungsfall und Budget entspricht.

+++

+++**Was ist der Unterschied zwischen Kampagnen und Journey?**

**Kampagnen** sind zielgruppenbasiert und werden von Marketing-Experten geplant. Sie definieren eine Zielgruppe, erstellen eine Nachricht und planen oder Triggern sie als Batch-Versand. Sie eignen sich am besten für Werbeaktionen, Newsletter und mehrstufige Zielgruppen-Workflows.

**Journey** sind in Echtzeit und ereignisgesteuert - sie reagieren sofort auf das individuelle Kundenverhalten und orchestrieren 1:1 Erlebnisse über Touchpoints hinweg. Sie eignen sich am besten für Onboarding-Flüsse, Nachkaufsequenzen und in Echtzeit ausgelöste Nachrichten.

**Kampagnen und Journey** bietet Ihnen beide Funktionen in einer einzigen Lizenz.

+++

+++**Welche Kanäle werden in orchestrierten Kampagnen unterstützt?**

Orchestrierte Kampagnen (mehrstufige Zielgruppen-Workflows mit der Kampagnenorchestrierungsfunktion) unterstützen nur **E-Mail, SMS, Push-Benachrichtigungen und Briefpost**. Web-, In-App-, Code-basierte und Inhaltskarten-Kanäle werden in orchestrierten Kampagnen-Workflows nicht unterstützt.

+++

+++**Ist Decisioning in jeder Konfiguration enthalten?**

Nein. Decisioning ist ein eindeutiges Add-on für erweiterte Funktionen und standardmäßig in keinem Basisangebot enthalten. Wenden Sie sich an den Adobe-Support, um Ihrer Konfiguration Decisioning hinzuzufügen.

+++

+++**Ich habe von Select, Prime oder Ultimate gehört. Sind sie immer noch das aktuelle Verpackungsmodell?**

[!DNL Adobe Journey Optimizer] wird jetzt durch ein modulares Verpackungsmodell angeboten, das auf Basisangeboten (Kampagnen, Journey, Kampagnen und Journey) und Add-ons aufbaut. Wenn Sie Bestandskunde sind und Terminologie von Select, Prime oder Ultimate verwenden und Fragen zu Ihren aktuellen Berechtigungen haben, wenden Sie sich an Ihren Adobe-Support-Mitarbeiter.

+++
