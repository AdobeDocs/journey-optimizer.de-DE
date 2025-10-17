---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Textnachrichten (SMS/MMS/RCS)
description: Erfahren Sie, wie Sie in Journey Optimizer Textnachrichten erstellen, testen und veröffentlichen.
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: 243d4e74c15057bc4bd334876a1bc87969d396e0
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 27%

---

# Erste Schritte mit Textnachrichten {#get-started-sms}

Verwenden Sie [!DNL Journey Optimizer], um Textnachrichten (SMS/MMS/RCS) an die Mobilgeräte Ihrer Kundinnen und Kunden zu senden. Mit dem SMS/MMS/RCS-Editor können Sie Nachrichten im Textformat erstellen, personalisieren und in der Vorschau anzeigen.

Textnachrichten können in einer Journey oder in einer Kampagne erstellt und versendet werden. Für SMS, MMS und RCS verwenden Sie die SMS-Aktion.

* In einer **Journey**. Erstellen Sie eine Journey, fügen Sie eine SMS-Aktivität hinzu und definieren Sie die Grundeinstellungen. Navigieren Sie dann zum Bereich SMS-Aktionen auf der rechten Seite, um den Inhalt für die SMS-, MMS- oder RCS-Nachricht zu erstellen. [Erfahren Sie, wie Sie eine Journey erstellen](../building-journeys/journey-gs.md)

* In einer **Kampagne**. Erstellen Sie eine Kampagne, wählen Sie SMS als Aktion aus und definieren Sie die Grundeinstellungen. Bearbeiten Sie dann den Nachrichteninhalt, um die zu sendende SMS-, MMS- oder RCS-Nachricht zu definieren. [Erfahren Sie, wie Sie eine Kampagne erstellen](../campaigns/create-campaign.md#configure)

>[!IMPORTANT]
>
>Wenn Sie zum ersten Mal Textnachrichten erstellen, stellen Sie sicher, dass der SMS-Kanal konfiguriert wurde. [Weitere Informationen](sms-configuration.md)

## Textnachrichten-Funktionen {#sms-capabilities}

Adobe Journey Optimizer bietet umfassende Textnachrichten-Funktionen, mit denen Sie Ihre Kunden über mehrere Kanäle hinweg ansprechen können:

**SMS (Short Message Service)**

Senden Sie Nachrichten mit bis zu 160 Zeichen im Nur-Text-Format. SMS ist das am häufigsten unterstützte Textnachrichtenformat auf allen Mobilgeräten.

**MMS (Multimedia Message Service)**

Verbessern Sie Ihre Kommunikation mit Multimedia-Inhalten, einschließlich Videos, Bildern, Audio-Clips und GIFs. MMS-Nachrichten ermöglichen zusätzlich zu Mediendateien bis zu 1600 Textzeichen. [Erfahren Sie mehr über MMS-Einschränkungen](../start/guardrails.md#sms-guardrails)

**RCS (Rich Communication Services)**

Senden Sie markenspezifische, interaktive Nachrichten mit erweiterten Funktionen wie Karussells, Rich-Cards, empfohlenen Aktionen und erweiterter Medienunterstützung. RCS bietet ein besseres Messaging-Erlebnis auf unterstützten Geräten.

## Wichtigste Funktionen {#key-features}

**Personalization und dynamische Inhalte**

Erstellen von personalisierten Textnachrichten mit dem Personalisierungseditor Fügen Sie Profilattribute, bedingte Inhalte und dynamische Daten hinzu, um Nachrichten an einzelne Empfängerinnen und Empfänger anzupassen. [Erfahren Sie mehr über Personalisierung](../personalization/personalize.md)

**Unterstützung mehrerer Anbieter**

Adobe Journey Optimizer lässt sich mit führenden SMS-Dienstleistern integrieren:

* **Sinch** - [Konfigurationshandbuch](sms-configuration-sinch.md)
* **Twilio** - [Konfigurationshandbuch](sms-configuration-twilio.md)
* **Infobip** - [Konfigurationshandbuch](sms-configuration-infobip.md)
* **Benutzerdefinierte Anbieter** - Konfigurieren Sie jeden anderen SMS-Anbieter mithilfe einer benutzerdefinierten API-Integration. [Weitere Informationen](sms-configuration-custom.md)

**URL-Verkürzung und -Tracking**

Fügen Sie Ihren Nachrichten gekürzte, verfolgbare URLs hinzu, um die Interaktion zu überwachen. Subdomain-Konfiguration ist für die URL-Verkürzungsfunktion erforderlich. [Erfahren Sie, wie Sie SMS-Subdomains konfigurieren](sms-subdomains.md)

**Opt-out-Verwaltung**

Sicherstellen der Einhaltung von Branchenstandards und -vorschriften durch integrierte Opt-out-Verwaltung. Journey Optimizer verarbeitet automatisch Standard-Opt-out-Keywords (STOP, QUIT, CANCEL usw.) für Sinch- und Infobip-Anbieter. [Erfahren Sie mehr über die Opt-out-Verwaltung](sms-opt-out.md)

**Vorschau und Tests**

Testen Sie Ihre Textnachrichten vor dem Versand mithilfe von Testprofilen und Beispieldaten. Vorschau von Personalisierung, Inhalt und Formatierung, um sicherzustellen, dass Ihre Nachrichten korrekt angezeigt werden. [Erfahren Sie, wie Sie Nachrichten senden](send-sms.md)

**Reporting und Analysen**

Verfolgen Sie die Performance Ihrer SMS-Kampagnen und Journey mit umfassenden Reporting-Funktionen:

* [SMS-Kampagnenberichte](../reports/campaign-global-report-cja-sms.md)
* [SMS Journey Berichte](../reports/journey-global-report-cja-sms.md)

## Konfigurationsanforderungen {#configuration-requirements}

Bevor Sie Textnachrichten senden, müssen Sie Folgendes tun:

1. **Wählen Sie einen SMS-Anbieter** - Wählen Sie Sinch, Twilio, Infobip oder konfigurieren Sie einen benutzerdefinierten Anbieter
2. **Einrichten von API-Anmeldeinformationen** - Integrieren der API-Token und Service-IDs Ihres Anbieters in Journey Optimizer
3. **Kanalkonfigurationen erstellen** - Einrichten von SMS-Konfigurationen für Marketing- und Transaktionsnachrichten
4. **Konfigurieren von Subdomains (optional)** - Nur erforderlich, wenn Sie in Ihren Nachrichten eine URL-Verkürzung verwenden möchten

Diese Konfigurationsschritte werden in der Regel von einem Systemadministrator durchgeführt. [Erste Schritte mit der SMS-Konfiguration](sms-configuration.md)

## Schnellstartanleitung {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="Validierung" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>Konfigurieren des SMS-Kanals</strong></a>
</div>
<p>SMS-Provider- und Kanalkonfigurationen einrichten</p>
</td>
<td>
<a href="create-sms.md">
<img alt="Lead" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong>Erstellen einer Textnachricht</strong></a>
</div>
<p>Gestalten und Personalisieren von SMS-, MMS- oder RCS-Inhalten</p>
</td>
<td>
<a href="send-sms.md">
<img alt="Gelegentlich" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>Vorschau und Senden</strong></a>
</div>
<p>Testen und Senden von Textnachrichten an Ihre Zielgruppe</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="Validierung" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>Verwalten von Opt-outs</strong></a>
</div>
<p>Handhabung von Abmeldeanfragen und Sicherstellung der Compliance</p>
</td>
</tr></table>

## Weitere Ressourcen {#additional-resources}

Weitere Informationen zu Textnachrichten in Journey Optimizer finden Sie unter den folgenden Themen.

+++Konfigurationshandbücher

Erfahren Sie, wie Sie Ihre SMS-Umgebung einrichten und konfigurieren:

* [Übersicht über die SMS-Kanalkonfiguration](sms-configuration.md)
* [Erstellen von SMS-Kanalkonfigurationen](sms-configuration-surface.md)
* [Konfigurieren von SMS-Subdomains für die URL-Verkürzung](sms-subdomains.md)

+++

+++Einrichtungshandbücher für Provider

Schrittweise Konfiguration für jeden SMS-Dienstleister:

* [Konfigurieren eines Sinch-Anbieters](sms-configuration-sinch.md)
* [Konfigurieren eines Twilio-Anbieters](sms-configuration-twilio.md)
* [Konfigurieren eines Infobip-Anbieters](sms-configuration-infobip.md)
* [Konfigurieren eines benutzerdefinierten SMS-Anbieters](sms-configuration-custom.md)

+++

+++Inhaltserstellung und -verwaltung

Erstellen, personalisieren und verwalten Sie den Inhalt von Textnachrichten:

* [SMS-/MMS-Nachrichten erstellen](create-sms.md)
* [Vorschau, Testen und Senden von Nachrichten](send-sms.md)
* [Personalization in Textnachrichten](../personalization/personalize.md)
* [Dynamische Inhalte](../personalization/get-started-dynamic-content.md)

+++

+++Compliance und Datenschutz

Stellen Sie sicher, dass Ihre Textnachrichten den Vorschriften und Datenschutzstandards entsprechen:

* [Opt-out-Verwaltung](sms-opt-out.md)
* [Datenschutz und Einverständniserklärung](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

+++

+++Leistungsverfolgung

Überwachen und analysieren Sie Ihre SMS-Kampagnen und die Journey-Leistung:

* [SMS-Kampagnenberichte](../reports/campaign-global-report-cja-sms.md)
* [SMS Journey Berichte](../reports/journey-global-report-cja-sms.md)

+++

+++Integration von Journey und Campaign

Erfahren Sie, wie Sie SMS in Ihre Kunden-Journey und -Kampagnen integrieren:

* [SMS-Nachrichten zu Journey hinzufügen](../building-journeys/journeys-message.md)
* [SMS-Kampagnen erstellen](../campaigns/create-campaign.md)

+++

## Anleitungsvideos {#videos}

**Konfigurieren und Senden von SMS-Nachrichten**

Erfahren Sie, wie Sie SMS-Nachrichten konfigurieren, erstellen und in Ihre Journey integrieren können.

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3422692?captions=ger&learn=on)

+++

**Erkunden Sie die Mobile-Messaging-Funktionen**

Entdecken Sie die umfassenden mobilen Messaging-Funktionen, die Adobe Journey Optimizer Marketing-Experten bietet.

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3430371?captions=ger&quality=12&learn=on)

+++

**Senden von RCS-Nachrichten der Marke**

Finden Sie heraus, wie Sie in Adobe Journey Optimizer an Ihre Marke angepasste, interaktive RCS-Nachrichten mithilfe eines benutzerdefinierten SMS-Anbieters konfigurieren und senden können. 

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3464764?captions=ger)

+++

**Verwandte Themen**

* [Hinzufügen von Nachrichten in Journeys](../building-journeys/journeys-message.md)
* [Erstellen von Marketing-Kampagnen](../campaigns/create-campaign.md)
* [Leitlinien und Einschränkungen](../start/guardrails.md#sms-guardrails)
