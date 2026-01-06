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
source-git-commit: de418dc4feefd99231155c550ad3a51e4850ee66
workflow-type: ht
source-wordcount: '831'
ht-degree: 100%

---

# Erste Schritte mit Textnachrichten {#get-started-sms}

Verwenden Sie [!DNL Journey Optimizer], um Textnachrichten (SMS/MMS/RCS) an die Mobilgeräte Ihrer Kundinnen und Kunden zu senden. Mit dem SMS/MMS/RCS-Editor können Sie Nachrichten im Textformat erstellen, personalisieren und in der Vorschau anzeigen.

Textnachrichten können in einer Journey oder in einer Kampagne erstellt und versendet werden. Für SMS, MMS und RCS verwenden Sie die SMS-Aktion.

* In einer **Journey**. Erstellen Sie eine Journey, fügen Sie eine SMS-Aktivität hinzu und definieren Sie die Grundeinstellungen. Navigieren Sie dann zum rechten Bereich der SMS-Aktionen, um den Inhalt für die SMS-, MMS- oder RCS-Nachricht zu erstellen. [Erfahren Sie, wie Sie eine Journey erstellen](../building-journeys/journey-gs.md)

* In einer **Kampagne**. Erstellen Sie eine Kampagne, wählen Sie SMS als Aktion aus und definieren Sie die Grundeinstellungen. Bearbeiten Sie dann den Nachrichteninhalt, um die zu sendende SMS-, MMS- oder RCS-Nachricht zu definieren. Erfahren Sie, wie Sie [eine Aktionskampagne](../campaigns/campaign-action.md#action-campaign-action) | [eine durch API ausgelöste Kampagne](../campaigns/api-triggered-campaigns.md) | [eine orchestrierte Kampagne](../orchestrated/create-orchestrated-campaign.md#create) erstellen können

>[!IMPORTANT]
>
>Wenn Sie zum ersten Mal eine Textnachricht erstellen, stellen Sie sicher, dass der SMS-Kanal konfiguriert wurde. [Weitere Informationen](sms-configuration.md)

## Textnachrichtenfunktionen {#sms-capabilities}

Adobe Journey Optimizer bietet umfassende Textnachrichtenfunktionen, mit denen Sie Ihre Kundinnen und Kunden über mehrere Kanäle hinweg ansprechen können:

**SMS (Short Message Service)**

Senden Sie Nachrichten mit bis zu 160 Zeichen im reinen Textformat. SMS ist das am häufigsten unterstützte Textnachrichtenformat auf allen Mobilgeräten.

**MMS (Multimedia Message Service)**

Verbessern Sie Ihre Kommunikation mit Multimedia-Inhalten, einschließlich Videos, Bildern, Audio-Clips und GIFs. MMS-Nachrichten ermöglichen zusätzlich zu Mediendateien die Verwendung von bis zu 1.600 Textzeichen. [Informationen zu MMS-Einschränkungen](../start/guardrails.md#sms-guardrails)

**RCS (Rich Communication Services)**

Senden Sie an Ihre Marke angepasste, interaktive Nachrichten mit erweiterten Funktionen wie Karussells, Rich Cards, empfohlenen Aktionen und erweiterter Medienunterstützung. RCS bietet ein umfangreicheres Messaging-Erlebnis auf unterstützten Geräten.

## Wichtigste Funktionen {#key-features}

**Personalisierung und dynamische Inhalte**

Erstellen Sie personalisierte Textnachrichten mit dem Personalisierungseditor. Fügen Sie Profilattribute, bedingte Inhalte und dynamische Daten hinzu, um Nachrichten an einzelne Empfängerinnen und Empfänger anzupassen. [Informationen zur Personalisierung](../personalization/personalize.md)

**Unterstützung mehrerer Anbieter**

Adobe Journey Optimizer lässt sich mit führenden SMS-Dienstleistern integrieren:

* **Sinch** – [Konfigurationshandbuch](sms-configuration-sinch.md)
* **Twilio** – [Konfigurationshandbuch](sms-configuration-twilio.md)
* **Infobip** – [Konfigurationshandbuch](sms-configuration-infobip.md)
* **Benutzerdefinierte Anbieter** – Konfigurieren Sie jeden anderen SMS-Anbieter mithilfe einer benutzerdefinierten API-Integration. [Weitere Informationen](sms-configuration-custom.md)

**URL-Verkürzung und -Tracking**

Fügen Sie Ihren Nachrichten gekürzte, nachverfolgbare URLs hinzu, um die Interaktion zu überwachen. Für die Funktion der URL-Verkürzung ist eine Subdomain-Konfiguration erforderlich. [Informationen zum Konfigurieren von SMS-Subdomains](sms-subdomains.md)

**Opt-out-Verwaltung**

Stellen Sie die Einhaltung von Branchenstandards und -vorschriften durch native Opt-out-Verwaltung sicher. Journey Optimizer verarbeitet Standard-Opt-out-Keywords (STOP, QUIT, CANCEL usw.) für Sinch- und Infobip-Anbieter automatisch. [Informationen zum Opt-out-Management](sms-opt-out.md)

**Anzeigen einer Vorschau und Testen**

Testen Sie Ihre Textnachrichten vor dem Versand mithilfe von Testprofilen und Beispieldaten. Zeigen Sie eine Vorschau von Personalisierung, Inhalt und Formatierung an, um sicherzustellen, dass Ihre Nachrichten korrekt angezeigt werden. [Informationen zum Senden von Nachrichten](send-sms.md)

**Reporting und Analyse**

Verfolgen Sie die Leistung Ihrer SMS-Kampagnen und Journeys mit umfassenden Reporting-Funktionen:

* [SMS-Kampagnenberichte](../reports/campaign-global-report-cja-sms.md)
* [SMS-Journey-Berichte](../reports/journey-global-report-cja-sms.md)

## Konfigurationsanforderungen {#configuration-requirements}

Bevor Sie Textnachrichten senden, müssen Sie Folgendes tun:

1. **Einen SMS-Anbieter auswählen**: Wählen Sie Sinch, Twilio oder Infobip aus oder konfigurieren Sie einen benutzerdefinierten Anbieter
2. **API-Anmeldedaten einrichten**: Integrieren Sie die API-Token und Service-IDs Ihres Anbieters mit Journey Optimizer
3. **Kanalkonfigurationen erstellen**: Richten Sie SMS-Konfigurationen für Marketing- und Transaktionsnachrichten ein
4. **Subdomains erstellen (optional)**: Nur erforderlich, wenn Sie in Ihren Nachrichten eine URL-Verkürzung verwenden möchten

Diese Konfigurationsschritte werden in der Regel von einer oder einem Systemadmin durchgeführt. [Erste Schritte mit der SMS-Konfiguration](sms-configuration.md)

## Schnellstartanleitung {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="Validierung" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>Konfigurieren des SMS-Kanals</strong></a>
</div>
<p>Einrichten von SMS-Anbieter und Kanalkonfigurationen</p>
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
<a href="send-sms.md"><strong>Anzeigen einer Vorschau und Senden</strong></a>
</div>
<p>Testen der Textnachricht und Senden an die Zielgruppe</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="Validierung" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>Verwalten von Opt-outs</strong></a>
</div>
<p>Umgehen mit Abmeldeanfragen und Sicherstellen von Compliance</p>
</td>
</tr></table>

## Weitere Ressourcen {#additional-resources}

Weitere Informationen zu Textnachrichten in Journey Optimizer finden Sie in den folgenden Themen.

+++Konfigurationshandbücher

Erfahren Sie, wie Sie Ihre SMS-Umgebung einrichten und konfigurieren:

* [Überblick über SMS-Kanalkonfiguration](sms-configuration.md)
* [Erstellen von SMS-Kanalkonfigurationen](sms-configuration-surface.md)
* [Konfigurieren von SMS-Subdomains für die URL-Verkürzung](sms-subdomains.md)

+++

+++Handbücher zur Einrichtung von Anbietern

Detaillierte Konfiguration für jeden SMS-Dienstleister:

* [Konfigurieren des Sinch-Anbieters](sms-configuration-sinch.md)
* [Konfigurieren des Twilio-Anbieters](sms-configuration-twilio.md)
* [Konfigurieren des Infobip-Anbieters](sms-configuration-infobip.md)
* [Konfigurieren des benutzerdefinierten SMS-Anbieters](sms-configuration-custom.md)

+++

+++Inhaltserstellung und -verwaltung

Erstellen, personalisieren und verwalten Sie den Inhalt von Textnachrichten:

* [Erstellen von SMS-/MMS-Nachrichten](create-sms.md)
* [Anzeigen einer Vorschau, Testen und Senden von Nachrichten](send-sms.md)
* [Personalisierung in Textnachrichten](../personalization/personalize.md)
* [Dynamische Inhalte](../personalization/get-started-dynamic-content.md)
* [Generieren von SMS-Inhalt mit dem KI-Assistenten](../content-management/generative-text.md)

+++

+++Compliance und Datenschutz

Stellen Sie sicher, dass Ihre Textnachrichten den Vorschriften und Datenschutzstandards entsprechen:

* [Opt-out-Verwaltung](sms-opt-out.md)
* [Datenschutz und Einverständniserklärung](../privacy/opt-out.md#opt-out-decision-management)

+++

+++Tracking der Leistung

Überwachen und analysieren Sie Ihre SMS-Kampagnen und die Journey-Leistung:

* [SMS-Kampagnenberichte](../reports/campaign-global-report-cja-sms.md)
* [SMS-Journey-Berichte](../reports/journey-global-report-cja-sms.md)

+++

+++Journey- und Kampagnenintegration

Erfahren Sie, wie Sie SMS in Ihre Kunden-Journeys und -Kampagnen integrieren:

* [Hinzufügen von SMS-Nachrichten zu Journeys](../building-journeys/journeys-message.md)
* [Erstellen von SMS-Kampagnen](../campaigns/create-campaign.md)

+++

## Anleitungsvideos {#videos}

**Konfigurieren und Senden von SMS-Nachrichten**

Erfahren Sie, wie Sie SMS-Nachrichten konfigurieren, erstellen und in Ihre Journey integrieren können.

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**Informationen zu Mobile-Messaging-Funktionen**

Entdecken Sie die umfassenden Mobile-Messaging-Funktionen, die Adobe Journey Optimizer Marketing-Fachleuten bietet.

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**Senden von an Marken angepassten RCS-Nachrichten**

Finden Sie heraus, wie Sie in Adobe Journey Optimizer an Ihre Marke angepasste, interaktive RCS-Nachrichten mithilfe eines benutzerdefinierten SMS-Anbieters konfigurieren und senden können. 

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++

**Verwandte Themen**

* [Hinzufügen von Nachrichten in Journeys](../building-journeys/journeys-message.md)
* [Erstellen von Marketing-Kampagnen](../campaigns/create-campaign.md)
* [Leitlinien und Einschränkungen](../start/guardrails.md#sms-guardrails)
* [Tutorials zu SMS und Mobile Messaging](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/channels/sms-channel/sms-mms-messages-overview){target="_blank"}
