---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines einzelnen Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung so konfigurieren, dass mit Journey Optimizer mit Sinch Textnachrichten gesendet werden
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 65%

---

# Konfigurieren eines einzelnen Anbieters {#sms-configuration-sinch}

Bei Verwendung des Sinch-Providers mit Journey Optimizer stehen Ihnen zwei verschiedene Optionen zur Verfügung:

* **SMS-Konfiguration**: Richten Sie Ihre Single API-Anmeldeinformationen ein, um SMS-Nachrichten nahtlos zu senden.

* **MMS-Konfiguration**: Konfigurieren Sie für Multimedia-Messaging (MMS) Ihre Single-MMS-API-Anmeldeinformationen. Beachten Sie, dass das Tracking und die Reaktion auf eingehende Nachrichten von der SMS-Konfiguration verarbeitet werden. MMS-Setup dient nur der ausgehenden Bereitstellung der MMS-Nachricht.

## Single-API-Anmeldeinformationen{#create-api}

Gehen Sie wie folgt vor, um Ihren Sinch-Provider so zu konfigurieren, dass SMS-Nachrichten und MMS mit Journey Optimizer gesendet werden:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

   ![](assets/sms_6.png)

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten, wie unten beschrieben.

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

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanaloberfläche für SMS-Nachrichten erstellen. [Weitere Informationen](sms-configuration-surface.md)

## Einmalige MMS-API-Anmeldeinformationen {#sinch-mms}

>[!IMPORTANT]
>
> Neben der MMS-Einrichtung müssen Sie auch Single API-Anmeldeinformationen erstellen, die speziell für die Verfolgung eingehender Nachrichten und die Verwaltung von Zustimmungsanfragen verwendet werden.

Gehen Sie wie folgt vor, um Sinch MMS so zu konfigurieren, dass MMS mit Journey Optimizer gesendet wird:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

   ![](assets/sms_6.png)

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten, wie unten beschrieben.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL Projekt-ID]**, **[!UICONTROL App-ID]** und **[!UICONTROL API-Token]**: Im Menü „Konversations-API“ können Sie Ihre Anmeldedaten im App-Menü finden.  Weitere Informationen finden Sie in der [Sinch-Dokumentation](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html){target="_blank"}.

   * **[!UICONTROL Service-Plan-ID]** und **[!UICONTROL SMS-API-Token]**: Ihre **[!UICONTROL Service-Plan-ID]** und Ihr **[!UICONTROL SMS-API-Token]** befinden sich auf der Registerkarte „SMS“ der API-Seite.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanaloberfläche für MMS-Nachrichten erstellen. [Weitere Informationen](sms-configuration-surface.md)
