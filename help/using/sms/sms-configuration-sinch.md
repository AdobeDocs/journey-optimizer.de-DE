---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines Sinch-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten mit Journey Optimizer mit Sinch konfigurieren.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: a196a27fd22a03915838ab4a9bb6139f85242f6b
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 80%

---

# Konfigurieren eines Sinch-Anbieters {#sms-configuration-sinch}

Wenn Sie den Sinch-Anbieter mit Journey Optimizer verwenden, können Sie zwischen zwei verschiedenen Optionen wählen:

* **SMS-Konfiguration**: Richten Sie Ihre Sinch-API-Anmeldedaten ein, um nahtlos SMS-Nachrichten zu versenden.

* **MMS-Konfiguration**: Konfigurieren Sie für Multimedia Messaging (MMS) Ihre Sinch-MMS-API-Anmeldedaten. Beachten Sie, dass das Tracking und Beantworten von eingehenden Nachrichten über die SMS-Konfiguration erfolgt. Die MMS-Einrichtung ist nur für den ausgehenden Versand der MMS-Nachricht vorgesehen.

## Sinch-API-Anmeldedaten{#create-api}

Gehen Sie wie folgt vor, um Ihren Sinch-Anbieter zum Senden von SMS-Nachrichten und MMS in Journey Optimizer zu konfigurieren:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** `>` **[!UICONTROL SMS-Einstellungen]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten, wie unten beschrieben.

   * **[!UICONTROL SMS-Anbieter]**: Sinch.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL Service-ID]** und **[!UICONTROL API-Token]**: Rufen Sie die API-Seite auf. Ihre Anmeldedaten finden Sie auf der Registerkarte „SMS“. Weitere Informationen finden Sie in der [Sinch-Dokumentation](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Opt-in-Keywords]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **[!UICONTROL Opt-in-Nachricht]** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Opt-in-Nachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als **[!UICONTROL Opt-in-Nachricht]** gesendet wird.

   * **[!UICONTROL Opt-out-Keywords]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **[!UICONTROL Opt-out-Nachricht]** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Opt-out-Nachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als **[!UICONTROL Opt-out-Nachricht]** gesendet wird.

   * **[!UICONTROL Hilfe-Keywords]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **Hilfenachricht** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Hilfenachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als **Hilfenachricht** gesendet wird.

   * **[!UICONTROL Double-Opt-in-Suchbegriffe]**: Geben Sie die Suchbegriffe ein, die den Double-Opt-in-Prozess auslösen. Wenn kein Benutzerprofil vorhanden ist, wird es nach erfolgreicher Bestätigung erstellt. Verwenden Sie für mehrere Keywords durch Kommas getrennte Werte. [Erfahren Sie mehr über das SMS-Double-Opt-in](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Double-Opt-in-Nachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch nach der Double-Opt-in-Bestätigung gesendet wird.

   * **[!UICONTROL Eingehende Zahl]**: Fügen Sie Ihre eindeutige eingehende Zahl oder ihren Kurz-Code hinzu. Auf diese Weise können Sie dieselben API-Anmeldeinformationen für verschiedene Sandboxes verwenden, von denen jede über eine eigene eingehende Zahl oder einen eigenen Kurz-Code verfügt.

   * **[!UICONTROL Benutzerdefinierte eingehende Suchbegriffe]**: Definieren Sie eindeutige Suchbegriffe für bestimmte Aktionen, z. B. DISCOUNT, ANGEBOTE, ENROLL. Diese Suchbegriffe werden als Profilattribute erfasst und gespeichert, sodass Sie eine Streaming-Segmentqualifizierung innerhalb der Journey Trigger und eine benutzerdefinierte Antwort oder Aktion bereitstellen können.

   * **[!UICONTROL Standardmäßige eingehende Antwortnachricht]**: Geben Sie die Standardantwort ein, die gesendet wird, wenn ein Endbenutzer eine eingehende SMS sendet, die keinem der definierten Schlüsselwörter entspricht.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldeinformationen]** auf das Papierkorbsymbol, um Ihre API-Anmeldeinformationen zu löschen.

1. Um vorhandene Anmeldeinformationen zu ändern, suchen Sie die gewünschten API-Anmeldeinformationen und klicken Sie auf die Option **[!UICONTROL Bearbeiten]** , um die erforderlichen Änderungen vorzunehmen.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für SMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

## Sinch-MMS-API-Anmeldedaten {#sinch-mms}

>[!IMPORTANT]
>
> Neben der MMS-Einrichtung müssen Sie auch Sinch-API-Anmeldedaten speziell für das Tracking eingehender Nachrichten und die Verwaltung von Zustimmungsanfragen erstellen.

Gehen Sie wie folgt vor, um Sinch MMS mit Journey Optimizer für das Senden von MMS zu konfigurieren:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** `>` **[!UICONTROL SMS-Einstellungen]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre MMS-API-Anmeldedaten, wie unten beschrieben.

   * **[!UICONTROL SMS-Anbieter]**: Sinch MMS.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL Projekt-ID]**, **[!UICONTROL App-ID]** und **[!UICONTROL API-Token]**: Führen Sie die folgenden Schritte aus, um Ihre MMS-API-Anmeldeinformationen zu erfassen.

      * Für **[!UICONTROL Projekt-ID]** und **[!UICONTROL App-ID]**: Greifen Sie auf die Seite [Überblick über die Konversations-API](https://dashboard.sinch.com/convapi/overview) Ihres Sinch-Projekts in Ihrem Sinch-Dashboard zu.
      * Für **[!UICONTROL API-Token]**: Rufen Sie die [Zugriffsschlüssel](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) für Ihr Sinch-Pojekt auf und generieren Sie einen **Base64-API-Token** aus den **Zugriffsschlüsseln** Ihres Sinch-Projekts.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldeinformationen]** auf das Papierkorbsymbol, um Ihre API-Anmeldeinformationen zu löschen.

1. Um vorhandene Anmeldeinformationen zu ändern, suchen Sie die gewünschten API-Anmeldeinformationen und klicken Sie auf die Option **[!UICONTROL Bearbeiten]** , um die erforderlichen Änderungen vorzunehmen.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für MMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)
