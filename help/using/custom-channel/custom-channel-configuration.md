---
title: Erstellen einer Kanalkonfiguration für einen benutzerdefinierten Kanal
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer eine Kanalkonfiguration für einen benutzerdefinierten Kanal erstellen.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 2%

---


# Erstellen einer Kanalkonfiguration {#create-channel-config}

Eine Kanalkonfiguration verknüpft Ihren benutzerdefinierten Kanal mit einer benannten, wiederverwendbaren Vorgabe, die Marketing-Experten beim Erstellen von Kampagnen und Journey auswählen.

Gehen Sie wie folgt vor, um eine Kanalkonfiguration für einen benutzerdefinierten Kanal zu erstellen.

1. Gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Kanalkonfigurationen]** und klicken Sie auf **[!UICONTROL Kanalkonfiguration erstellen]**. Weitere Informationen finden Sie unter [Erstellen einer Kanalkonfiguration](../configuration/channel-surfaces.md).

1. Wählen **[!UICONTROL in der Dropdown]** Liste Kanal auswählen einen der aktivierten benutzerdefinierten Kanäle aus.

   ![Kanal auswählen](assets/custom_channel_select_channel.png){width="100%"}

1. Wenn der ausgewählte Kanal eine Authentifizierung verwendet (der Typ ist nicht **None**), wird das Feld **[!UICONTROL API-]**&quot; angezeigt. Wählen Sie die für diese Konfiguration zu verwendenden Anmeldeinformationen aus. [Weitere Informationen zu API-Anmeldeinformationen](custom-channel-api-credentials.md)

   ![API-Anmeldeinformationen auswählen](assets/custom_channel_config_api_credentials.png){width="100%"}

1. Wenn Sie in [!DNL Journey Optimizer] Subdomains für benutzerdefinierte Kanäle eingerichtet haben, können Sie eine delegierte Subdomain auswählen, die für das Tracking von Links verwendet wird, die in der Payload für diese Konfiguration vorhanden sind. [Erfahren Sie, wie Sie eine Subdomain delegieren](custom-channel-subdomains.md)

1. Wenn der ausgewählte Kanal für die Endpunkt-URL [&#x200B; Kopfzeilen oder Abfrageparameter (als &#x200B;](create-custom-channel.md#endpoint-configuration) definiert) hat, **der Abschnitt** Dynamische Parameter“ angezeigt.

   Geben Sie den Wert für jeden Parameter ein. Sie können den Personalisierungseditor verwenden, um dynamische Werte einzufügen (z. B. eine aus dem Profil gelöste Benutzerkennung). Auf diese Weise können Sie die Anfrage für jede Empfängerin und jeden Empfänger auf der Grundlage ihrer Profildaten anpassen.

   ![Dynamische Parameter](assets/custom_channel_config_dynamic_parameters.png){width="100%"}

1. Wenn für den benutzerdefinierten Kanal Payload-Felder mit aktiviertem Kontrollkästchen **[!UICONTROL Kanalkonfiguration]** vorhanden sind, werden diese Felder im Abschnitt **[!UICONTROL Payload-Konfiguration]** angezeigt. [Weitere Informationen](create-custom-channel.md#payload-configuration)

   ![Payload-Felder](assets/custom_channel_config_payload.png){width="100%"}

   Konfigurieren Sie für jedes Feld einen Wert, der für diese Konfiguration geeignet ist. Dies eignet sich für Felder, die je nach Kampagnenkontext oder Journey variieren können, z. B. Absenderinformationen oder Nachrichtenvorlagen.

1. Für koordinierte Kampagnen füllen Sie den Abschnitt **[!UICONTROL Ausführungsdetails]** aus, um Profildimensionen zuzuordnen und die Ausführungsadresse anzugeben.

   ![Ausführungsdetails in orchestrierten Kampagnen](assets/custom_channel_oc_execution_details.png){width="80%"}

1. Klicken Sie **[!UICONTROL Senden]**, um die Kanalkonfiguration zu speichern und zu aktivieren.

<!--
>[!CAUTION]
>
>If your organization uses approval policies, you may need to request approval before activating journeys or campaigns that use this channel configuration. [Learn more](../test-approve/gs-approval.md)
-->

## Nächste Schritte {#next-steps}

Ihr benutzerdefinierter Kanal ist jetzt vollständig konfiguriert. Marketing-Experten können damit beginnen, Kundenerlebnisse zu schaffen:

* [Erstellen benutzerdefinierter Kanalerlebnisse](create-custom-experience.md)
* [Testen des benutzerdefinierten Kanals](test-custom-channel.md)
* [Überwachen benutzerdefinierter Kanäle](configure-custom-channel.md)
