---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines Sinch-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten mit Journey Optimizer mit Sinch konfigurieren.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 604af3a0ac9febb62f2e2b1705e2751b2c476e04
workflow-type: ht
source-wordcount: '990'
ht-degree: 100%

---

# Konfigurieren eines Sinch-Anbieters {#sms-configuration-sinch}

Wenn Sie den Sinch-Anbieter mit Journey Optimizer verwenden, können Sie zwischen drei verschiedenen Optionen wählen:

* **SMS-Konfiguration**: Richten Sie Ihre Sinch-API-Anmeldedaten ein, um nahtlos SMS-Nachrichten zu versenden.

* **MMS-Konfiguration**: Konfigurieren Sie für Multimedia Messaging (MMS) Ihre Sinch-MMS-API-Anmeldedaten. Beachten Sie, dass das Tracking und Beantworten von eingehenden Nachrichten über die SMS-Konfiguration erfolgt. Die MMS-Einrichtung ist nur für den ausgehenden Versand der MMS-Nachricht vorgesehen.

* **RCS-Konfiguration**: Richten Sie Ihre Sinch-API-Anmeldedaten ein, um nahtlos RCS-Nachrichten zu versenden.

## Konfigurieren von API-Anmeldedaten für SMS{#create-api}

>[!BEGINSHADEBOX]

Wenn keine Opt-in- oder Opt-out-Keywords angegeben werden, werden standardmäßige Einverständnisnachrichten verwendet, um den Datenschutz der Benutzenden zu berücksichtigen. Durch das Hinzufügen benutzerdefinierter Keywords werden die Standardwerte automatisch überschrieben.

**Standard-Keywords:**

* **Opt-in**: SUBSCRIBE, YES, UNSTOP, START, CONTINUE, RESUME, BEGIN
* **Opt-out**: STOP, QUIT, CANCEL, END, UNSUBSCRIBE, NO
* **Hilfe**: HELP.

>[!ENDSHADEBOX]

Gehen Sie wie folgt vor, um Ihren Sinch-Anbieter zum Senden von SMS-Nachrichten und MMS in Journey Optimizer zu konfigurieren:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** `>` **[!UICONTROL SMS-Einstellungen]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten wie unten beschrieben:

+++ Liste der SMS-Anmeldedaten für die Konfiguration

   | Konfigurationsfelder | Beschreibung |
   |---|---|    
   | SMS-Anbieter | Sinch |
   | Name | Wählen Sie einen Namen für Ihre API-Anmeldedaten. |
   | Service-ID und API-Token | Rufen Sie die API-Seite auf. Sie finden Ihre Anmeldedaten auf der Registerkarte „SMS“. Weitere Informationen finden Sie in der [Sinch-Dokumentation](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}. |
   | Opt-in-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Opt-in-Nachricht automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Opt-in-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Opt-in-Nachricht gesendet wird. |
   | Opt-out-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Opt-out-Nachricht automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Opt-out-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Opt-out-Nachricht gesendet wird. |
   | Hilfe-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **Hilfenachricht** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Hilfenachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als **Hilfenachricht** gesendet wird. |
   | Double-Opt-in-Keywords | Geben Sie die Keywords ein, die den Double-Opt-in-Prozess auslösen. Wenn kein Benutzerprofil vorhanden ist, wird es nach erfolgreicher Bestätigung erstellt. Verwenden Sie für mehrere Keywords kommagetrennte Werte. [Erfahren Sie mehr über das SMS-Double-Opt-in](https://video.tv.adobe.com/v/3440289/?learn=on&captions=ger). |
   | Double-Opt-in-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch nach der Double-Opt-in-Bestätigung gesendet wird. |
   | Eingehende Nummer | Fügen Sie Ihre eindeutige eingehende Nummer oder Ihren eindeutigen Kurz-Code hinzu. Auf diese Weise können Sie dieselben API-Anmeldedaten für verschiedene Sandboxes verwenden, von denen jede über eine eigene eingehende Zahl oder einen eigenen Kurz-Code verfügt. |
   | Benutzerdefinierte eingehende Keywords | Definieren Sie eindeutige Keywords für bestimmte Aktionen, z. B. RABATT, ANGEBOTE, REGISTRIEREN. Diese Keywords werden als Attribute im Profil erfasst und gespeichert, sodass Sie eine Streaming-Segmentqualifikation innerhalb der Journey auslösen und eine benutzerdefinierte Antwort oder Aktion bereitstellen können. |
   | Eingehende Standard-Antwortnachricht | Geben Sie die Standardantwort ein, die gesendet wird, wenn eine Endanwenderin oder ein Endanwender eine eingehende SMS sendet, die keinem der definierten Keywords entspricht. |
   | Überschreibungs-URL | Geben Sie Ihre benutzerdefinierte URL ein, um die Standard-Endpunkte für SMS-Versandberichte, Feedback-Daten, eingehende Nachrichten oder Ereignisbenachrichtigungen zu ersetzen. Sinch sendet alle relevanten Aktualisierungen an diese URL anstelle der vordefinierten. |

+++

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldedaten]** auf das Papierkorbsymbol, um Ihre API-Anmeldedaten zu löschen.

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für SMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

## Konfigurieren von API-Anmeldedaten für MMS{#sinch-mms}

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

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldedaten]** auf das Papierkorbsymbol, um Ihre API-Anmeldedaten zu löschen.

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für MMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

## Konfigurieren der API-Anmeldedaten für RCS

<!--![](assets/do-not-localize/rcs-sms.png)-->

RCS-Messaging (Rich Communication Services) wird in Journey Optimizer über Sinch unterstützt und ermöglicht den Versand von einfachen Nachrichten unter Verwendung verifizierter Geschäftsprofile mit Branding-Elementen wie Logos und Absendenamen.

Beachten Sie, dass Nachrichten automatisch über SMS gesendet werden, wenn das Gerät des Profils RCS nicht unterstützt oder über RCS vorübergehend unerreichbar ist.

➡️ [Erfahren Sie in der Sinch-Dokumentation, wie RCS von Sinch unterstützt wird](https://sinch.com/blog/rcs-api-guide/)

So konfigurieren Sie RCS mit Sinch:

1. **Einrichten eines an Ihre Marke angepassten RCS-Agenten**

   Wenden Sie sich an den Adobe-Support, um einen an Ihre Marke angepassten RCS-Agenten einzurichten. [Weitere Informationen zu an Marken angepassten RCS-Agenten](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Einrichten Ihrer [Sinch-API-Anmeldedaten](#create-api)**

   Nachdem der RCS-Agent genehmigt wurde, müssen Sie Ihre Sinch-API-Anmeldedaten einrichten, die Ihren Zugriffsschlüssel, Ihr Geheimnis und die Service-Plan-ID enthalten. Diese Anmeldedaten werden von Journey Optimizer zum Authentifizieren und Senden von Nachrichten über die Sinch-Plattform verwendet.

1. **Erstellen einer [Kanalkonfiguration](sms-configuration-surface.md) für Ihre RCS-Nachrichten**

   Konfigurieren Sie eine Kanaloberfläche in Journey Optimizer, indem Sie Ihre Sinch-Anmeldedaten verknüpfen und die Messaging-Parameter definieren. Mit diesem Setup können Sie RCS-Nachrichten in Journey Optimizer erstellen und von dort aus senden.

