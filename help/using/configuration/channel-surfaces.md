---
title: Einrichten von Kanaloberflächen
description: Erfahren Sie, wie Sie Kanaloberflächen konfigurieren und überwachen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 84%

---

# Einrichten von Kanaloberflächen {#set-up-channel-surfaces}

Mit [!DNL Journey Optimizer]können Sie Kanaloberflächen (d. h. Nachrichtenvorgaben) einrichten, die alle für Ihre Nachrichten erforderlichen technischen Parameter definieren: E-Mail-Typ, Absender-E-Mail und Name, Mobile Apps, SMS-Konfiguration und mehr.

>[!CAUTION]
>
> * Um Kanaloberflächen zu erstellen, zu bearbeiten und zu löschen, benötigen Sie die Berechtigung zur [Verwaltung von Kanaloberflächen](../administration/high-low-permissions.md#manage-channel-surface).
>
> * Bevor Sie Kanaloberflächen erstellen können, müssen Sie die Schritte zur Konfiguration von [E-Mails](#configure-email-settings), [Push-Benachrichtigungen](../configuration/push-configuration.md) und [SMS](../configuration/sms-configuration.md) ausführen.


Nachdem die Kanaloberflächen konfiguriert wurden, können Sie sie beim Erstellen von Nachrichten in einer Journey auswählen.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Erstellen einer Kanaloberfläche {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Kanaloberflächeneinstellungen"
>abstract="Wählen Sie beim Einrichten einer Kanaloberfläche den Kanal aus, auf den sie angewendet wird, und definieren Sie alle technischen Parameter, die für Ihre Nachrichten erforderlich sind, z. B. E-Mail-Typ, Subdomain, Absendername, Mobile Apps, SMS-Konfiguration und mehr."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Kanaloberflächeneinstellungen"
>abstract="Wählen Sie beim Einrichten einer Kanaloberfläche den Kanal aus, auf den sie angewendet wird, und definieren Sie alle technischen Parameter, die für Ihre Nachrichten erforderlich sind, z. B. E-Mail-Typ, Absendername, Mobile Apps, SMS-Konfiguration und mehr."

<!--New contextual help content for September release: A channel surface defines all the technical parameters required for your messages (email type, sender name, mobile apps, SMS configuration, etc.): once configured, you will be able to select it when creating actions from a journey or a campaign. Note that you must have the Manage channel surface permission to create, edit and delete channel surfaces.

To create a channel surface, follow these steps:

1. Access the **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** menu, then click **[!UICONTROL Create channel surface]**.

    ![](assets/preset-create.png)

1. Enter a name and a description (optional) for the surface, then select the channel(s) to configure.

    ![](assets/preset-general.png)

    >[!NOTE]
    >
    > Names must begin with a letter (A-Z). It can only contain alpha-numeric characters. You can also use underscore `_`, dot`.` and hyphen `-` characters. 

1. If you selected the **[!UICONTROL Email]** channel, configure your settings as described in [this section](email-settings.md).

    ![](assets/preset-email.png)

1. For the **[!UICONTROL Push Notification]** channel, select at least one platform  -  **iOS** and/or **Android** -, and the mobile applications to use for each platform.

    ![](assets/preset-push.png)
        
    >[!NOTE]
    >
    >For more on how to configure your environment to send push notifications, refer to [this section](push-gs.md).

1. For the **[!UICONTROL SMS]** channel, define your settings as detailed in [this section](sms-configuration.md#message-preset-sms).

    ![](assets/preset-sms.png)

    >[!NOTE]
    >
    >For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the channel surface as draft and resume its configuration later on.

    ![](assets/preset-submit.png)

    >[!NOTE]
    >
    >You cannot proceed with surface creation while the selected IP pool is under [edition](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status), and has never been associated with the selected subdomain. [Learn more](#subdomains-and-ip-pools)
    >
    >Save the surface as draft and wait until the IP pool has the **[!UICONTROL Success]** status to resume surface creation.
    
1. Once the channel surface has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around **48h-72h**, and can take up to **7-10 business days**.

    These checks include configuration and technical tests that are performed by the Adobe team:

    * SPF validation
    * DKIM validation
    * MX record validation
    * Check IPs denylisting
    * Helo host check
    * IP pool verification
    * A/PTR record, t/m/res subdomain verification

    >[!NOTE]
    >
    >If the checks are not successful, learn more on the possible failure reasons in [this section](#monitor-channel-surfaces).  

1. Once the checks are successful, the channel surface gets the **[!UICONTROL Active]** status. It is ready to be used to deliver messages.

    ![](assets/preset-active.png)

## Monitor channel surfaces {#monitor-channel-surfaces}

All your channel surfaces display in the **[!UICONTROL Channels]** > **[!UICONTROL Channel surfaces]** menu. Filters are available to help you browse through the list (channel, user, status).

![](assets/preset-filters.png)

Once created, channel surfaces can have the following statuses:

* **[!UICONTROL Draft]**: The channel surface has been saved as a draft and has not been submitted yet. Open it to resume the configuration.
* **[!UICONTROL Processing]**: The channel surface has been submitted and is going through several verifications steps.
* **[!UICONTROL Active]**: The channel surface has been verified and can be selected to create messages.
* **[!UICONTROL Failed]**: One or several checks have failed during the channel surface verification.
* **[!UICONTROL Deactivated]**: The channel surface is deactivated. It cannot be used to create new messages.

In case a channel surface creation fails, the details on each possible failure reason are described below.

If one of these errors occurs, contact [Adobe Customer Care](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} to get assistance.

* **SPF validation failed**: SPF (Sender Policy Framework) is an email authentication protocol that allows to specify authorized IPs that can send emails from a given subdomain. SPF validation failure means that the IP addresses in the SPF record do not match the IP addresses used for sending emails to the mailbox providers. 

* **DKIM validation failed**: DKIM (DomainKeys Identified Mail) allows the recipient server to verify that the received message was sent by the genuine sender of the associated domain and that the content of the original message was not altered on its way. DKIM validation failure means that the receiving mail servers are unable to verify the authenticity of the message content and its association with the sending domain.:

* **MX record validation failed**: MX (Mail eXchange) record validation failure means that the mail servers responsible for accepting inbound emails on behalf of a given subdomain are not correctly configured.

* **Deliverability configurations failed**: Deliverability configurations failure can happen due to any of the following reasons:
    * Blocklisting of the allocated IPs
    * Invalid `helo` name
    * Emails being sent from IPs other than the ones specified in the IP pool of the corresponding surface
    * Unable to deliver emails to inboxes of major ISPs like Gmail and Yahoo

## Edit a channel surface {#edit-channel-surface}

To edit a channel surface, follow the steps below.

>[!NOTE]
>
>You cannot edit the **[!UICONTROL Push notification settings]**. If a channel surface is only configured for the Push notification channel, it is not editable.

1. From the list, click a channel surface name to open it.

    ![](assets/preset-name.png)

1. Edit its properties as desired.

    >[!NOTE]
    >
    >If a channel surface has the **[!UICONTROL Active]** status, the **[!UICONTROL Name]**, **[!UICONTROL Select channel]** and **[!UICONTROL Subdomain]** fields are greyed out and cannot be edited.

1. Click **[!UICONTROL Submit]** to confirm your changes.

    >[!NOTE]
    >
    >You can also save the channel surface as draft and resume update later on.

Once the changes are submitted, the channel surface will go through a validation cycle similar to the one in place when [creating a channel surface](#create-channel-surface). The edition processing time can take up to **3 hours**.

>[!NOTE]
>
>If you only edit the **[!UICONTROL Description]**, **[!UICONTROL Email type]** and/or **[!UICONTROL Email retry parameters]** fields, the update is instantaneous.

### Update details {#update-details}

For channel surfaces that have the **[!UICONTROL Active]** status, you can check the details of the update. To do so:

Click the **[!UICONTROL Recent update]** icon that is displayed next to the active surface name.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

Auf dem Bildschirm **[!UICONTROL Letzte Aktualisierung]** können Sie Informationen wie den Aktualisierungsstatus und die Liste der angeforderten Änderungen sehen.

<!--![](assets/preset-recent-update-screen.png)-->

### Aktualisieren des Status {#update-statuses}

Eine Aktualisierung einer Kanaloberfläche kann die folgenden Status aufweisen:

* **[!UICONTROL Verarbeitung läuft]**: Die Aktualisierung der Kanaloberfläche wurde übermittelt und durchläuft mehrere Überprüfungsschritte.
* **[!UICONTROL Aktiv]**: Die aktualisierte Kanaloberfläche wurde verifiziert und kann zum Erstellen von Nachrichten ausgewählt werden.
* **[!UICONTROL Fehlgeschlagen]**: Eine oder mehrere Prüfungen sind bei der Verifizierung der Kanaloberflächenaktualisierung fehlgeschlagen.

Jeder Status wird nachfolgend beschrieben.

#### In Bearbeitung {#surface-processing}

Es werden verschiedene Zustellbarkeitsprüfungen durchgeführt, um sicherzustellen, dass die Kanaloberfläche ordnungsgemäß aktualisiert wurde.

>[!NOTE]
>
>Wenn Sie nur die Felder **[!UICONTROL Beschreibung]**, **[!UICONTROL E-Mail-Typ]** und/oder **[!UICONTROL E-Mail-Wiederholungsparameter]** bearbeiten, wird die Aktualisierung sofort wirksam.

Die Verarbeitungszeit kann bis **3 Stunden** dauern. Weitere Informationen zu den während des Validierungszyklus durchgeführten Prüfungen finden Sie in [diesem Abschnitt](#create-channel-surface).

Wenn Sie eine bereits aktive Oberfläche bearbeiten:

* Ihr Status **[!UICONTROL Aktiv]** bleibt erhalten, während der Validierungsprozess ausgeführt wird.

* Das Symbol **[!UICONTROL Letzte Aktualisierung]** wird neben dem Namen der Oberfläche in der Liste der Kanaloberflächen angezeigt.

* Während des Validierungsprozesses verwenden die mit dieser Oberfläche konfigurierten Nachrichten weiterhin die ältere Version der Oberfläche.

>[!NOTE]
>
>Sie können eine Kanaloberfläche während des Aktualisierungsprozesses nicht ändern. Sie können zwar weiterhin auf den Namen klicken, aber alle Felder sind ausgegraut. Die Änderungen werden erst dann übernommen, wenn die Aktualisierung erfolgreich war.

#### Erfolgreich {#success}

Nach erfolgreicher Überprüfung wird die neue Version der Oberfläche automatisch in allen Nachrichten verwendet, die diese Oberfläche verwenden. Sie müssen jedoch möglicherweise warten:
* einige Minuten, bevor die Voreinstellung von den einzelnen Nachrichten genutzt wird,
* bis zum nächsten Batch, damit die Oberfläche in Batch-Nachrichten wirksam wird.

#### Fehlgeschlagen {#failed}

Wenn der Validierungsprozess fehlschlägt, wird weiterhin die ältere Version der Oberfläche verwendet.

Weitere Informationen zu möglichen Fehlerursachen finden Sie in [diesem Abschnitt](#monitor-channel-surfaces).

Wenn die Aktualisierung fehlschlägt, kann die Oberfläche erneut bearbeitet werden. Sie können auf den Namen klicken und die Einstellungen aktualisieren, die korrigiert werden müssen.

## Deaktivieren einer Kanaloberfläche {#deactivate-a-surface}

Wenn Sie möchten, dass eine **[!UICONTROL aktive]** Kanaloberfläche nicht verfügbar ist, um neue Nachrichten zu erstellen, können Sie sie deaktivieren. Nachrichten von Journeys, die diese Oberfläche verwenden, sind jedoch nicht betroffen und funktionieren weiterhin.

>[!NOTE]
>
>Sie können eine Kanaloberfläche nicht deaktivieren, während eine Aktualisierung im Gange ist. Sie müssen warten, bis die Aktualisierung entweder erfolgreich war oder fehlgeschlagen ist. Weitere Informationen finden Sie unter [Bearbeiten von Kanaloberflächen](#edit-channel-surface) und [Aktualisierungsstatus](#update-statuses).

1. Rufen Sie die Liste der Kanaloberflächen auf.

1. Klicken Sie für die aktive Oberfläche Ihrer Wahl auf die Schaltfläche **[!UICONTROL Weitere Aktionen]**.

1. Wählen Sie **[!UICONTROL Deaktivieren]** aus.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Deaktivierte Kanaloberflächen können nicht gelöscht werden, um Probleme in Journeys zu vermeiden, die diese Oberflächen zum Senden von Nachrichten verwenden.

Eine deaktivierte Kanaloberfläche kann nicht direkt bearbeitet werden. Sie können sie jedoch duplizieren und die Kopie bearbeiten, um eine neue Version zu entwerfen, mit der Sie neue Nachrichten erstellen können. Sie können sie auch erneut aktivieren und warten, bis die Aktualisierung erfolgreich abgeschlossen wird, bevor Sie sie bearbeiten.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
