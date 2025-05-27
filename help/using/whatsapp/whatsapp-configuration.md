---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des WhatsApp-Kanals
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von WhatsApp-Nachrichten mit Journey Optimizer konfigurieren.
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: ht
source-wordcount: '461'
ht-degree: 100%

---

# Erste Schritte bei der WhatsApp-Konfiguration {#whatsapp-config}

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

* [Erste Schritte mit WhatsApp-Nachrichten](get-started-whatsapp.md)
* **[Erste Schritte bei der WhatsApp-Konfiguration](whatsapp-configuration.md)**
* [Erstellen einer WhatsApp-Nachricht](create-whatsapp.md)
* [Überprüfen und Senden Ihrer WhatsApp-Nachrichten](send-whatsapp.md)

>[!ENDSHADEBOX]

Bevor Sie Ihre WhatsApp-Nachricht senden, müssen Sie Ihre Adobe Journey Optimizer-Umgebung konfigurieren und mit Ihrem WhatsApp-Konto verknüpfen. Gehen Sie hierfür wie folgt vor:

1. [Erstellen Ihrer WhatsApp-API-Anmeldedaten](#WhatsApp-credentials)
1. [Erstellen Ihrer WhatsApp-Konfiguration](#WhatsApp-configuration)

Diese Schritte müssen von Adobe Journey Optimizer-[Systemadmins](../start/path/administrator.md) durchgeführt werden.

## Erstellen von WhatsApp-API-Anmeldedaten {#whatsapp-credentials}

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]** aus. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre API-Anmeldedaten, wie unten beschrieben:

   * **API-Token**: Geben Sie Ihr API-Token ein. Weitere Informationen finden Sie in der [Meta-Dokumentation](https://developers.facebook.com/docs/facebook-login/guides/access-tokens/).
   * **Geschäftskonto-ID**: Geben Sie die eindeutige Nummer Ihres Geschäftsportfolios ein. Weitere Informationen finden Sie in der [Meta-Dokumentation](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![](assets/whatsapp-api.png)

1. Klicken Sie auf **[!UICONTROL Fortfahren]**.

1. Wählen Sie das **Geschäftskonto**, das mit Ihren WhatsApp-API-Anmeldedaten verbunden werden soll.

   ![](assets/whatsapp-api-2.png)

1. Wählen Sie die **Telefonnummer** aus, die zum Senden Ihrer WhatsApp-Nachrichten verwendet wird.

1. Ihre Telefonnummerneinstellungen werden automatisch ausgefüllt:

   * **Qualitätsbewertung**: Spiegelt das Kunden-Feedback zu den Nachrichten wider, die in den letzten 24 Stunden gesendet wurden.
      * Grün: hohe Qualität
      * Gelb: mittlere Qualität
      * Rot: geringe Qualität

     Weitere Informationen zur [Qualitätsbewertung](https://www.facebook.com/business/help/766346674749731#)

   * **Durchsatz**: Gibt die Rate an, mit der Ihre Telefonnummer Nachrichten senden kann.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie nun eine Kanalkonfiguration für WhatsApp-Nachrichten erstellen. [Weitere Informationen](#whatsapp-configuration)

## Erstellen einer WhatsApp-Konfiguration {#whatsapp-configuration}

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** und wählen Sie **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL Kanalkonfigurationen]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Kanalkonfiguration erstellen]**.

   ![](assets/whatsapp-config-1.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Konfiguration ein und wählen Sie dann den WhatsApp-Kanal aus.

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Wählen Sie **[!DNL WhatsApp]** als Kanal aus.

   ![](assets/whatsapp-config-2.png)

1. Wählen Sie **[!UICONTROL Marketing-Aktion(en)]** aus, um Einverständnisrichtlinien mit den Nachrichten zu verknüpfen, die diese Konfiguration verwenden. Es werden alle mit der Marketing-Aktion verknüpften Einverständnisrichtlinien genutzt, um die Präferenzen Ihrer Kundinnen und Kunden zu respektieren. Weitere Informationen

1. Wählen Sie die zuvor erstellte **[!UICONTROL WhatsApp-API-Konfiguration]** aus.

   ![](assets/whatsapp-config-3.png)

1. Geben Sie die **[!UICONTROL Absendernummer]** ein, die Sie für Ihre Sendungen verwenden möchten.

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]**. Sie können die Kanalkonfiguration auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

1. Nachdem die Kanalkonfiguration erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt.

   >[!NOTE]
   >
   >In [diesem Abschnitt](../configuration/channel-surfaces.md) erfahren Sie mehr über die möglichen Fehlerursachen, wenn die Prüfungen nicht erfolgreich sind.

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Kanalkonfiguration den Status **[!UICONTROL Aktiv]**. Sie kann nun zum Versand von Nachrichten verwendet werden.

Sie können jetzt mit Journey Optimizer WhatsApp-Nachrichten senden.
