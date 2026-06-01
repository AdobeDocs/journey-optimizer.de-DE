---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des SMS-Kanals
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Nachrichten an Mobilgeräte mit Journey Optimizer konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
TQID: https://experienceleague.adobe.com/dO8HoRdGLuYVFN2YVjRCiFJQHmWHApROU8qz2-hKmTs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 69%

---

# Erste Schritte bei der Konfiguration von Mobilnachrichten {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Konfigurieren eines SMS-Anbieters mit Journey Optimizer"
>abstract="Adobe Journey Optimizer versendet Mobilnachrichten über SMS-Dienstanbieter. Wählen Sie Ihren Anbieter aus und geben Sie Ihre API-Anmeldedaten ein."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Konfigurieren Ihres MMS-Anbieters mit Journey Optimizer"
>abstract="Adobe Journey Optimizer versendet Medieninhalte über MMS-Dienstanbieter. Anbieter auswählen und API-Anmeldedaten eingeben."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Konfigurieren Ihres SMS/RCS/MMS-Anbieters mit Journey Optimizer"
>abstract="Vor dem Versand von Mobilnachrichten (SMS/RCS/MMS) müssen die Anbietereinstellungen in Journey Optimizer integriert werden. Danach muss eine SMS/RCS/MMS-Konfiguration erstellt werden. Diese Schritte müssen von Adobe Journey Optimizer-System-Admins durchgeführt werden."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Erstellen einer SMS-Kanalkonfiguration"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Wählen Sie die Konfiguration des SMS-Anbieters aus."
>abstract="Wählen Sie die für Ihren SMS-Anbieter konfigurierten API-Anmeldedaten aus."

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="Unpräzises Opt-out"
>abstract="Wenn diese Option aktiviert ist, erkennt das unpräzise Opt-out eingehende Nachrichten, die definierten Opt-out-Schlüsselwörtern sehr ähnlich sind (z. B. „ABNELDEN“), und sendet automatisch eine Bestätigungsantwort, um die Abmeldeabsicht der Benutzenden zu überprüfen. Wenn Benutzende die Anmeldung über die definierte Eingabeaufforderung bestätigen, wird das Abonnement gekündigt."

Bevor Sie SMS, MMS oder RCS versenden, müssen Sie Ihre Adobe Journey Optimizer-Umgebung konfigurieren. Gehen Sie hierfür wie folgt vor:

1. Integrieren Sie die Provider-Einstellungen in Journey Optimizer.
Die Schritte hängen von Ihrem SMS-Anbieter ab. Über die unten stehenden Links können Sie auf die detaillierte Dokumentation zugreifen:
   * [Infobip](mobile-configuration-infobip.md)
   * [Sinch](mobile-configuration-sinch.md)
   * [Twilio](mobile-configuration-twilio.md)
   * [Benutzerdefinierter Anbieter](mobile-configuration-custom.md)
1. [Erstellen eines Webhook](mobile-webhook.md)
1. [Erstellen einer Mobile-Konfiguration](mobile-configuration-surface.md)

Diese Schritte müssen von Adobe Journey Optimizer-[Systemadmins](../start/path/administrator.md) durchgeführt werden.

## Voraussetzungen{#sms-prerequisites}

Adobe Journey Optimizer lässt sich derzeit mit Drittanbietern integrieren, die unabhängig von Adobe Journey Optimizer mobile Messaging-Services anbieten. Unterstützte Anbieter für Mobile Messaging und MMS sind: **Sinch**, **Twilio** und **Infobip**. Beachten Sie, dass Sie mit der [benutzerdefinierten Anbieterkonfiguration](mobile-configuration-custom.md) zusätzliche Messaging-Anbieter konfigurieren können.

Vor der Konfiguration des Mobile-Kanals müssen Sie bei einem dieser Anbieter ein Konto erstellen, um Ihr **API-Token** und Ihre **Service-ID** abzurufen, über die Sie die Verbindung zwischen Adobe Journey Optimizer und dem entsprechenden Anbieter konfigurieren müssen.

Ihre Nutzung von Mobile-Messaging- und MMS-Services unterliegt zusätzlichen Bedingungen des jeweiligen Anbieters. Als Lösungen von Drittanbietern stehen den Benutzerinnen und Benutzern von Adobe Journey Optimizer Sinch, Twilio und Infobip über eine Integration zur Verfügung. Adobe kontrolliert keine Produkte von Drittanbietern und ist nicht für diese verantwortlich. Wenden Sie sich bei Problemen oder Anfragen zur Unterstützung im Zusammenhang mit den Mobile-Messaging-Services an Ihren Provider.

>[!CAUTION]
>
>Um auf SMS-Subdomains zuzugreifen und sie zu bearbeiten, benötigen Sie die Berechtigung zum **[!UICONTROL Verwalten von SMS-Subdomains]** für die Produktions-Sandbox. Weitere Informationen über Berechtigungen finden Sie auf [dieser Seite](../administration/high-low-permissions.md#administration-permissions).
>

