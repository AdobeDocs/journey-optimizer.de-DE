---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Mobile-Nachrichten
description: Erfahren Sie, wie Sie in Journey Optimizer Mobile-Nachrichten erstellen und senden
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
TQID: https://experienceleague.adobe.com/Ev0xJ86fpweQxgf-VjGUEl4ebk6BdzhVof2BgiMR9EM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c13ff12d-60f1-49cd-833a-d43359628223
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 1314
ht-degree: 19%

---

# Erste Schritte mit Mobile-Nachrichten {#get-started-sms}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erste Schritte mit Mobile Messaging in Adobe Journey Optimizer, um SMS-, MMS- und RCS-Nachrichten in Journey und Kampagnen zu erstellen, zu personalisieren und zu senden, einschließlich Provider-Support, Konfigurationsanforderungen und RCS-Voraussetzungen.

>[!ENDSHADEBOX]

Verwenden Sie [!DNL Journey Optimizer], um Mobile-Nachrichten über drei Kanäle (**SMS**, **MMS** und **RCS**) von einem einzigen SMS-/MMS-/RCS-Editor aus an Ihre Kunden zu senden, in dem Sie Inhalte erstellen, personalisieren und in der Vorschau anzeigen können.

* **SMS (Short Message Service)**: Versand von Nur-Text-Nachrichten mit bis zu 160 Zeichen, unterstützt auf allen Mobilgeräten.
* **MMS (Multimedia Message Service)**: Reichern Sie Ihre Nachrichten mit Bildern, Videos, Audioclips und GIFs sowie bis zu 1.600 Textzeichen an. [Informationen zu MMS-Einschränkungen](../start/guardrails.md#sms-guardrails)
* **RCS (Rich Communication Services)**:Deliver markenspezifischer, interaktiver Inhalt direkt in der nativen Messaging-App Ihrer Kunden, ohne dass ein zusätzlicher App-Download erforderlich ist.

>[!IMPORTANT]
>
>Wenn Sie zum ersten Mal Nachrichten für Mobilgeräte erstellen, stellen Sie sicher, dass der Mobile-Nachrichtenkanal konfiguriert wurde. [Weitere Informationen](mobile-configuration.md)

Mobile Nachrichten können in einer Journey oder in einer Kampagne mithilfe der Mobile-Nachrichtenaktion erstellt und gesendet werden:

* Auf einer **Journey**: Fügen Sie eine Mobile-Nachrichtenaktion zu Ihrem Journey hinzu, definieren Sie die Grundeinstellungen und erstellen Sie dann Ihren Inhalt im Bereich für Mobile-Nachrichtenaktionen auf der rechten Seite. [Erfahren Sie, wie Sie eine Journey erstellen](../building-journeys/journey-gs.md)

* Wählen Sie in **Kampagne**:Create Kampagne die Aktion Mobile Nachricht aus, definieren Sie die Grundeinstellungen und bearbeiten Sie dann den Nachrichteninhalt. Erfahren Sie, wie Sie [eine Aktionskampagne](../campaigns/campaign-action.md#action-campaign-action) | [eine durch API ausgelöste Kampagne](../campaigns/api-triggered-campaigns.md) | [eine orchestrierte Kampagne](../orchestrated/create-orchestrated-campaign.md#create) erstellen können

## Anwendungsszenarien {#use-cases}

SMS, MMS und RCS funktionieren am besten, wenn Sie Benutzer zuverlässig erreichen müssen, unabhängig davon, ob sie Ihre App installiert haben oder eine Internetverbindung verfügbar ist.

| Vorteil | Warum | Beispielhafte Anwendungsfälle |
| --- | --- | --- |
| Maximale Reichweite und Unmittelbarkeit | Keine App- oder Internetverbindung erforderlich, um die Nachricht zu erhalten | Benutzer ohne installierte Smartphone-App erreichen |
| Sichtbarkeitsgarantie | Bei SMS liegen die Öffnungsraten bei über 90 % | OTP-Codes, Terminerinnerungen, Versandbenachrichtigungen |
| Rich Content über MMS/RCS | Fügt Bilder, Videos und interaktive Elemente über den reinen Text hinaus hinzu | Markenaktionen, Produktkataloge |
| Benutzer ohne App-Zugriff erreichen | Funktioniert für Empfänger, die Ihre App nicht installiert oder geöffnet haben | Rückgewinnung abgelaufener Mobile-App-Benutzer, Onboarding von Nicht-Mobile-App-Kunden |
| CTAs mit hoher Dringlichkeit | Direkt an ein Gerät gesendet, das Benutzerinnen und Benutzer häufig überprüfen | Flash-Verkäufe, Warnhinweise zu Betrug, Service-Ausfällen |
| Ebenenbildung mit anderen Kanälen | Ergänzt Push-, E-Mail- und In-App-Messaging für eine breitere Abdeckung | Multi-Channel-Journey mit SMS als Fallback-Kanal |

## Verwendung {#when-not-to-use}

SMS, MMS und RCS sind nicht immer die effizienteste oder am besten geeignete Wahl. Betrachten Sie in den folgenden Situationen einen anderen Kanal:

* Die Kosten sind ein Problem bei hohen Versandvolumina, da SMS und MMS pro Nachricht berechnet werden und sich die Kosten pro Nachricht schnell skalieren
* Der Inhalt ist lang oder komplex und besser für E-Mails geeignet, die eine umfassendere Formatierung und längere Texte unterstützen
* Die Empfänger haben sich nicht explizit angemeldet, was in den meisten Regionen und Messaging-Vorschriften rechtliche und Compliance-Risiken birgt

## Wichtigste Funktionen {#key-features}

| Funktion | Beschreibung |
|---|---|
| **Personalisierung** | Passen Sie Nachrichten mit Profilattributen, bedingten Inhalten und dynamischen Daten mit dem Personalisierungseditor an. [Weitere Informationen](../personalization/personalize.md) |
| **Provider-Support** | Verbinden Sie sich über [&#x200B; API](mobile-configuration-sinch.md)Integration mit [Twilio](mobile-configuration-twilio.md), [Infobip](mobile-configuration-infobip.md) oder einem [benutzerdefinierten Anbieter](mobile-configuration-custom.md). |
| **URL-Verkürzung** | Fügen Sie gekürzte, verfolgbare URLs hinzu, um die Interaktion zu überwachen. Subdomain-Konfiguration erforderlich. [Weitere Informationen](mobile-subdomains.md) |
| **Opt-out-Verwaltung** | Integrierte Handhabung von Standard-Opt-out-Keywords (STOP, QUIT, CANCEL usw.) für Sinch und Infobip. [Weitere Informationen](mobile-opt-out.md) |
| **Vorschau und Tests** | Validieren von Inhalten mit Testprofilen und Beispieldaten vor dem Senden. [Weitere Informationen](send-mobile-message.md) |
| **Reporting** | Nachverfolgen der Kampagnen- und Journey-Performance mit [Kampagnenberichten](../reports/campaign-global-report-cja-sms.md) und [Journey-Berichten](../reports/journey-global-report-cja-sms.md). |

## Konfigurationsanforderungen {#configuration-requirements}

Bevor Sie Nachrichten an Mobilgeräte senden, müssen Sie Folgendes tun:

1. **Wählen eines SMS-Anbieters**: Wählen Sie aus Sinch, Twilio, Infobip oder konfigurieren Sie einen benutzerdefinierten Anbieter
2. **Einrichten von API-Anmeldeinformationen**: Integrieren Sie die API-Token und Service-IDs Ihres Anbieters in Journey Optimizer
3. **Kanalkonfigurationen erstellen**: Einrichten von SMS-Konfigurationen für Marketing- und Transaktionsnachrichten
4. **Subdomains konfigurieren (optional)**: Nur erforderlich, wenn in Ihren Nachrichten eine URL-Verkürzung vorgesehen ist

Diese Konfigurationsschritte werden in der Regel von einer oder einem Systemadmin durchgeführt. [Erste Schritte mit der SMS-Konfiguration](mobile-configuration.md)

### Anforderungen für RCS {#requirement-rcs}

Für die Verwendung von RCS in Journey Optimizer sind folgende Voraussetzungen erforderlich:

* **Sinch RCS API-Anmeldeinformationen**: Ein Administrator muss API-Anmeldeinformationen für den Sinch RCS-Anbieter konfigurieren (Projekt-ID, App-ID und API-Token). [Weitere Informationen](mobile-configuration-sinch.md)
* **Konfiguration des mobilen Nachrichtenkanals** Ein Administrator muss eine Kanalkonfiguration mit aktivierten RCS-Anmeldeinformationen erstellen, damit Nachrichten als RCS und nicht als SMS gesendet werden. [Weitere Informationen](mobile-configuration.md)
* **Fallback-SMS**: Dringend empfohlen. Empfänger, deren Geräte RCS nicht unterstützen, erhalten die Nachricht nur, wenn ein SMS-Fallback verfügbar ist. Kunden ohne vorhandenes SMS-Volumen sollten SMS und eine Kurzwahlnummer erwerben. [Weitere Informationen](design-mobile.md#rcs-content)
* **Unterstützter Anbieter**: Für das native RCS-Authoring ist Sinch RCS (Adobe Resell oder Direct) erforderlich. Twilio, Infobip und andere Anbieter müssen eine benutzerdefinierte Anbieterintegration verwenden.
* **Geräteunterstützung**: Die RCS-Bereitstellung wird auf Android- und iOS-Geräten unterstützt. Die Verfügbarkeit der Anbieter und der Regionen ist unterschiedlich, RCS ist weltweit nicht allgemein verfügbar.

## Zusätzliche Ressourcen {#additional-resources}

Weitere Informationen zu Mobile Messaging in Journey Optimizer finden Sie in den folgenden Themen. Weitere Anwendungsfälle und Best Practices finden Sie in der [SMS/MMS](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/mobile-learning-hub/mobile-channels-overview/sms-mms-rcs-overview){target="_blank"}RCS-Übersicht) im Mobile Learning Hub.

+++Konfigurationshandbücher

Erfahren Sie, wie Sie Ihre SMS-Umgebung einrichten und konfigurieren:

* [Überblick über SMS-Kanalkonfiguration](mobile-configuration.md)
* [Erstellen von SMS-Kanalkonfigurationen](mobile-configuration-surface.md)
* [Konfigurieren von SMS-Subdomains für die URL-Verkürzung](mobile-subdomains.md)

+++

+++Handbücher zur Einrichtung von Anbietern

Detaillierte Konfiguration für jeden SMS-Dienstleister:

* [Konfigurieren des Sinch-Anbieters](mobile-configuration-sinch.md)
* [Konfigurieren des Twilio-Anbieters](mobile-configuration-twilio.md)
* [Konfigurieren des Infobip-Anbieters](mobile-configuration-infobip.md)
* [Konfigurieren des benutzerdefinierten SMS-Anbieters](mobile-configuration-custom.md)

+++

+++Inhaltserstellung und -verwaltung

Erstellen, personalisieren und verwalten Sie Ihre Mobile-Nachrichteninhalte:

* [SMS-/RCS-/MMS-Nachrichten erstellen](create-mobile-message.md)
* [Anzeigen einer Vorschau, Testen und Senden von Nachrichten](send-mobile-message.md)
* [Personalization in mobilen Nachrichten](../personalization/personalize.md)
* [Dynamische Inhalte](../personalization/get-started-dynamic-content.md)
* [Generieren von SMS-Inhalt mit dem KI-Assistenten](../content-management/generative-text.md)

+++

+++Compliance und Datenschutz

Stellen Sie sicher, dass Ihre Mobile-Messaging-Richtlinie den Vorschriften und Datenschutzstandards entspricht:

* [Opt-out-Verwaltung](mobile-opt-out.md)
* [Datenschutz und Einverständniserklärung](../privacy/opt-out.md#opt-out-decision-management)

+++

+++Tracking der Leistung

Überwachen und analysieren Sie Ihre SMS-Kampagnen und die Journey-Leistung:

* [SMS-Kampagnenberichte](../reports/campaign-global-report-cja-sms.md)
* [SMS-Journey-Berichte](../reports/journey-global-report-cja-sms.md)

+++

+++Journey- und Kampagnenintegration

Erfahren Sie, wie Sie SMS in Ihre Kunden-Journeys und -Kampagnen integrieren:

* [Hinzufügen von SMS-Nachrichten zu Journeys](../building-journeys/journey-action.md)
* [Erstellen von SMS-Kampagnen](../campaigns/create-campaign.md)

+++

+++Häufig gestellte Fragen zu RCS

**Ist das native RCS Messaging mit Twilio oder Infobip verfügbar?**

Nein. Der native RCS-Designer in Journey Optimizer ist nicht verfügbar, wenn SMS-Drittanbieter wie Twilio oder Infobip verwendet werden. RCS-Nachrichten können jedoch über eine [benutzerdefinierte Provider-Integration) gesendet &#x200B;](mobile-configuration-custom.md).

**Warum sollte man SMS zusammen mit RCS kaufen?**

Um das SMS-Fallback zu ermöglichen, sollten ein SMS-Volumen und eine Kurzwahlnummer erworben werden. Dies ist der empfohlene Pfad. Wenn SMS nicht konfiguriert ist, erhalten Profile, deren Gerät oder Provider RCS nicht unterstützt, die Nachricht überhaupt nicht.

**Ist natives RCS-Messaging für Sinch-Direktkunden verfügbar?**

Ja. Kunden, die die Conversational API von Sinch verwenden, haben Zugriff auf das native RCS-Authoring, einschließlich Adobe Resell- und Sinch Direct-Kunden.

**Ist RCS überall verfügbar?**

Nein. Die Akzeptanz von Betreibern nimmt weltweit weiter zu, aber RCS wird nicht überall in allen Betreibern und Regionen unterstützt. Bei der Planung von RCS-Kampagnen sollten regionale Verfügbarkeit und Carrier-Support untersucht werden.

**Wo erscheinen RCS-Meldungen auf dem Gerät?**

RCS-Nachrichten werden an derselben Stelle wie Standard-SMS-Nachrichten im nativen Messaging-Programm des Geräts angezeigt. Sie kommen von einem markierten, verifizierten Absender, der den Empfängern das Vertrauenssignal gibt, zu wissen, dass die Nachricht legitim ist.

**Welche Zeichenbeschränkungen gibt es für eine RCS-Nachricht?**

Rich-Media-Nachrichtentypen (einzelne) unterstützen bis zu 3.072 Zeichen, was deutlich mehr ist als die Beschränkung von 160 Zeichen für Standard-SMS. Die grundlegenden RCS-Nachrichtentypen sind auf 160 Zeichen beschränkt und entsprechen dem Standard-SMS-Limit.

+++

## Anleitungsvideos {#videos}

**Konfigurieren und Senden von SMS-Nachrichten**

Erfahren Sie, wie Sie SMS-Nachrichten konfigurieren, erstellen und in Ihre Journey integrieren können.

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3422692?captions=ger&learn=on)

+++

**Informationen zu Mobile-Messaging-Funktionen**

Entdecken Sie die umfassenden Mobile-Messaging-Funktionen, die Adobe Journey Optimizer Marketing-Fachleuten bietet.

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3430371?captions=ger&quality=12&learn=on)

+++

**Senden von an Marken angepassten RCS-Nachrichten**

Finden Sie heraus, wie Sie in Adobe Journey Optimizer an Ihre Marke angepasste, interaktive RCS-Nachrichten mithilfe eines benutzerdefinierten SMS-Anbieters konfigurieren und senden können.

+++Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3464764?captions=ger)

+++
