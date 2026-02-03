---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des SMS-Kanals
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten mit Journey Optimizer konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 100%

---

# Erste Schritte bei der SMS-/MMS-/RCS-Konfiguration {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Konfigurieren eines SMS-Anbieters mit Journey Optimizer"
>abstract="Adobe Journey Optimizer versendet Textnachrichten über SMS-Dienstanbieter. Wählen Sie Ihren Anbieter aus und geben Sie Ihre API-Anmeldedaten ein."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Konfigurieren Ihres MMS-Anbieters mit Journey Optimizer"
>abstract="Adobe Journey Optimizer versendet Medieninhalte über MMS-Dienstanbieter. Anbieter auswählen und API-Anmeldedaten eingeben."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Konfigurieren eines SMS/MMS-Anbieters mit Journey Optimizer"
>abstract="Vor dem Versand von Textnachrichten (SMS/MMS) müssen die Anbietereinstellungen in Journey Optimizer integriert werden. Danach muss eine SMS/MMS-Konfiguration erstellt werden. Diese Schritte müssen von Adobe Journey Optimizer-System-Admins durchgeführt werden."
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

1. Integrieren Sie die Anbietereinstellungen mit Journey Optimizer.
Die Schritte hängen von Ihrem SMS-Anbieter ab. Durchsuchen Sie die nachfolgenden Links, um auf ausführliche Dokumentation zuzugreifen:
   * [Infobip](sms-configuration-infobip.md)
   * [Sinch](sms-configuration-sinch.md)
   * [Twilio](sms-configuration-twilio.md)
   * [Benutzerdefinierter Anbieter](sms-configuration-custom.md)
1. [Erstellen eines Webhook](sms-webhook.md)
1. [Erstellen einer SMS-Konfiguration](sms-configuration-surface.md)

Diese Schritte müssen von Adobe Journey Optimizer-[Systemadmins](../start/path/administrator.md) durchgeführt werden.

## Voraussetzungen{#sms-prerequisites}

Adobe Journey Optimizer lässt sich derzeit mit Drittanbietern integrieren, die unabhängig von Adobe Journey Optimizer Textnachrichtendienste anbieten. Unterstützte Anbieter für Textnachrichten und MMS sind: **Sinch**, **Twilio** und **Infobip**. Beachten Sie, dass Sie mit der [benutzerdefinierten Anbieterkonfiguration](sms-configuration-custom.md) zusätzliche Messaging-Anbieter konfigurieren können.

Vor der Konfiguration des SMS-Kanals müssen Sie bei einem dieser Anbieter ein Konto erstellen, um das **API-Token** und die **Service-ID** zu erhalten, über die Sie die Verbindung zwischen Adobe Journey Optimizer und dem entsprechenden Anbieter herstellen können.

Ihre Nutzung von Textnachrichten- und MMS-Diensten unterliegt zusätzlichen Bedingungen des jeweiligen Anbieters. Als Lösungen von Drittanbietern stehen den Benutzerinnen und Benutzern von Adobe Journey Optimizer Sinch, Twilio und Infobip über eine Integration zur Verfügung. Adobe kontrolliert keine Produkte von Drittanbietern und ist nicht für diese verantwortlich. Wenden Sie sich bei Problemen oder Hilfeanfragen im Zusammenhang mit den Textnachrichtendiensten (SMS/MMS) an Ihren Anbieter.

>[!CAUTION]
>
>Um auf SMS-Subdomains zuzugreifen und sie zu bearbeiten, benötigen Sie die Berechtigung zum **[!UICONTROL Verwalten von SMS-Subdomains]** für die Produktions-Sandbox. Weitere Informationen über Berechtigungen finden Sie auf [dieser Seite](../administration/high-low-permissions.md#administration-permissions).
>

