---
solution: Journey Optimizer
product: journey optimizer
title: Einrichten von Kanaloberflächen
description: Erfahren Sie, wie Sie Kanaloberflächen konfigurieren und überwachen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 0%

---

# Einrichten von Kanaloberflächen {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="Anwendungsoberfläche"
>abstract="Eine Oberfläche ist eine Konfiguration, die von einem Systemadministrator definiert wurde. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomäne, Mobile Apps usw."

Mit [!DNL Journey Optimizer]können Sie Kanaloberflächen (d. h. Nachrichtenvorgaben) einrichten, die alle für Ihre Nachrichten erforderlichen technischen Parameter definieren: E-Mail-Typ, Absender-E-Mail und Name, Mobile Apps, SMS-Konfiguration und mehr.

>[!CAUTION]
>
> * Um Kanaloberflächen zu erstellen, zu bearbeiten und zu löschen, muss die [Kanaloberfläche verwalten](../administration/high-low-permissions.md#manage-channel-surface) Berechtigung.
>
> * Sie müssen die [E-Mail-Konfiguration](../email/get-started-email-config.md), [Push-Konfiguration](../push/push-configuration.md) und [SMS-Konfiguration](../sms/sms-configuration.md) Schritte vor dem Erstellen von Kanaloberflächen.


Sobald die Kanaloberflächen konfiguriert wurden, können Sie sie beim Erstellen von Nachrichten aus einer Journey oder einer Kampagne auswählen.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Erstellen einer Kanaloberfläche {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Kanaloberflächeneinstellungen"
>abstract="Wählen Sie beim Einrichten einer Kanaloberfläche den Kanal aus, auf den sie angewendet wird, und definieren Sie alle technischen Parameter, die für Ihren Versand erforderlich sind, z. B. E-Mail-Typ, Absendername, Mobile Apps, SMS-Konfiguration und mehr."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Kanaloberflächeneinstellungen"
>abstract="Um Aktionen wie E-Mails aus einer Journey oder einer Kampagne erstellen zu können, müssen Sie zunächst eine Kanaloberfläche erstellen, die alle für Ihre Nachrichten erforderlichen technischen Einstellungen definiert. Sie müssen über die Berechtigung zum Verwalten der Kanaloberfläche verfügen, um Kanaloberflächen zu erstellen, zu bearbeiten und zu löschen."

Gehen Sie wie folgt vor, um eine Kanaloberfläche zu erstellen:

1. Zugriff auf **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** Menü und klicken Sie auf **[!UICONTROL Create channel surface]**.

   ![](assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Oberfläche ein und wählen Sie dann die zu konfigurierenden Kanäle aus.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A-Z) beginnen. Sie darf nur alphanumerische Zeichen enthalten. Sie können auch Unterstriche verwenden `_`, Punkt`.` und Bindestrich `-` Zeichen.

1. Wenn Sie die Option **[!UICONTROL Email]** -Kanal konfigurieren Sie Ihre Einstellungen wie unter [diesem Abschnitt](../email/email-settings.md).

   ![](assets/preset-email.png)

1. Für **[!UICONTROL Push Notification]** Kanal, mindestens eine Plattform auswählen -  **iOS** und/oder **Android** - und die für jede Plattform zu verwendenden Mobile Apps.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Weitere Informationen zum Konfigurieren Ihrer Umgebung für den Versand von Push-Benachrichtigungen finden Sie unter [diesem Abschnitt](../push/push-gs.md).

1. Für **[!UICONTROL SMS]** -Kanal, legen Sie Ihre Einstellungen wie im Abschnitt [diesem Abschnitt](../sms/sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Weiterführende Informationen zur Konfiguration der Umgebung für den Versand von SMS-Nachrichten finden Sie im Abschnitt [diesem Abschnitt](../sms/sms-configuration.md).

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie auf **[!UICONTROL Submit]** zur Bestätigung. Sie können die Kanaloberfläche auch als Entwurf speichern und die Konfiguration später fortsetzen.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >Sie können nicht mit der Oberflächenerstellung fortfahren, solange sich der ausgewählte IP-Pool unter [edition](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** -Status) und wurde noch nie mit der ausgewählten Subdomain verknüpft. [Weitere Infos](#subdomains-and-ip-pools)
   >
   >Speichern Sie die Oberfläche als Entwurf und warten Sie, bis der IP-Pool den **[!UICONTROL Success]** -Status, um die Erstellung der Oberfläche wieder aufzunehmen.

1. Nachdem die Kanaloberfläche erstellt wurde, wird sie in der Liste mit der **[!UICONTROL Processing]** Status.

   Während dieses Schritts werden mehrere Prüfungen durchgeführt, um zu überprüfen, ob die Konfiguration korrekt ist. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   >Beim Erstellen der ersten E-Mail-Oberfläche für eine bestimmte Subdomain kann die Verarbeitungszeit dauern **10 Minuten bis 10 Tage**. Wenn die ausgewählte Subdomain bereits auf einer anderen E-Mail-Oberfläche verwendet wird, dauert dies nur bis zu 3 Stunden.

   Zu diesen Prüfungen gehören Konfigurations- und technische Tests, die vom Adobe-Team durchgeführt werden:

   * SPF-Validierung
   * DKIM-Validierung
   * MX-Datensatzvalidierung
   * IP-Blockierungsauflistung überprüfen
   * Helo-Host-Prüfung
   * IP-Poolverifizierung
   * A/PTR-Eintrag, Subdomain-Verifizierung t/m/res
   * FBL-Registrierung (diese Prüfung wird nur durchgeführt, wenn eine E-Mail-Oberfläche für eine bestimmte Subdomain zum ersten Mal erstellt wird)

   >[!NOTE]
   >
   >Wenn die Prüfungen nicht erfolgreich sind, erfahren Sie mehr über die möglichen Fehlerursachen in [diesem Abschnitt](#monitor-channel-surfaces).

1. Sobald die Prüfungen erfolgreich sind, erhält die Kanaloberfläche die **[!UICONTROL Active]** Status. Es kann zum Versand von Nachrichten verwendet werden.

   ![](assets/preset-active.png)

## Bildschirmkanaloberflächen {#monitor-channel-surfaces}

Alle Kanaloberflächen werden im **[!UICONTROL Channels]** > **[!UICONTROL Channel surfaces]** Menü. Es stehen Filter zur Verfügung, mit denen Sie die Liste durchsuchen können (Kanal, Benutzer, Status).

![](assets/preset-filters.png)

Nach der Erstellung können Kanaloberflächen die folgenden Status aufweisen:

* **[!UICONTROL Draft]**: Die Kanaloberfläche wurde als Entwurf gespeichert und wurde noch nicht übermittelt. Öffnen Sie es, um die Konfiguration fortzusetzen.
* **[!UICONTROL Processing]**: Die Kanaloberfläche wurde gesendet und durchläuft mehrere Überprüfungsschritte.
* **[!UICONTROL Active]**: Die Kanaloberfläche wurde überprüft und kann zur Erstellung von Nachrichten ausgewählt werden.
* **[!UICONTROL Failed]**: Bei der Überprüfung der Kanaloberfläche sind eine oder mehrere Prüfungen fehlgeschlagen.
* **[!UICONTROL Deactivated]**: Die Kanaloberfläche wird deaktiviert. Sie kann nicht zum Erstellen neuer Nachrichten verwendet werden.

Wenn die Erstellung einer Kanaloberfläche fehlschlägt, werden die Details zu den möglichen Fehlerursachen nachfolgend beschrieben.

Wenn einer dieser Fehler auftritt, wenden Sie sich an [Adobe-Kundenunterstützung](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}, um Hilfe zu erhalten.

* **SPF-Validierung fehlgeschlagen**: SPF (Sender Policy Framework) ist ein E-Mail-Authentifizierungsprotokoll, mit dem autorisierte IPs angegeben werden können, die E-Mails von einer bestimmten Subdomain senden können. SPF-Validierungsfehler bedeutet, dass die IP-Adressen im SPF-Datensatz nicht mit den IP-Adressen übereinstimmen, die zum Senden von E-Mails an die Postfachanbieter verwendet werden.

* **DKIM-Validierung fehlgeschlagen**: Mit DKIM (DomainKeys Identified Mail) kann der Empfängerserver überprüfen, ob die empfangene Nachricht vom echten Absender der zugehörigen Domain gesendet wurde und ob der Inhalt der ursprünglichen Nachricht nicht verändert wurde. DKIM-Validierungsfehler bedeutet, dass die Empfänger-E-Mail-Server die Authentizität des Nachrichteninhalts und dessen Zuordnung zur sendenden Domain nicht überprüfen können:

* **MX-Datensatzvalidierung fehlgeschlagen**: MX (Mail eXchange)-Datensatz Validierungsfehler bedeutet, dass die E-Mail-Server, die für die Annahme von eingehenden E-Mails im Namen einer bestimmten Subdomain verantwortlich sind, nicht korrekt konfiguriert sind.

* **Zustellbarkeitskonfigurationen fehlgeschlagen**: Zustellbarkeitskonfigurationen können aus einem der folgenden Gründe fehlschlagen:
   * Blockierung der zugewiesenen IPs
   * Ungültig `helo` name
   * E-Mails, die von anderen als den im IP-Pool der entsprechenden Oberfläche angegebenen IP-Adressen gesendet werden
   * E-Mails können nicht an Postfächer großer ISPs gesendet werden

## Kanaloberfläche bearbeiten {#edit-channel-surface}

Gehen Sie wie folgt vor, um eine Kanaloberfläche zu bearbeiten.

>[!NOTE]
>
>Sie können die **[!UICONTROL Push notification settings]**. Wenn eine Kanaloberfläche nur für den Kanal Push-Benachrichtigung konfiguriert ist, kann sie nicht bearbeitet werden.

1. Klicken Sie in der Liste auf einen Namen für die Kanaloberfläche, um ihn zu öffnen.

   ![](assets/preset-name.png)

1. Bearbeiten Sie die Eigenschaften nach Bedarf.

   >[!NOTE]
   >
   >Wenn die Kanaloberfläche die **[!UICONTROL Active]** Status, **[!UICONTROL Name]**, **[!UICONTROL Select channel]** und **[!UICONTROL Subdomain]** -Felder sind ausgegraut und können nicht bearbeitet werden.

1. Klicken **[!UICONTROL Submit]** um Ihre Änderungen zu bestätigen.

   >[!NOTE]
   >
   >Sie können die Kanaloberfläche auch als Entwurf speichern und die Aktualisierung später fortsetzen.

Sobald die Änderungen übermittelt wurden, durchläuft die Kanaloberfläche einen Validierungszyklus, der dem beim [Kanaloberfläche erstellen](#create-channel-surface). Die Bearbeitungszeit kann bis zu **3 Stunden**.

>[!NOTE]
>
>Wenn Sie nur die **[!UICONTROL Description]**, **[!UICONTROL Email type]** und/oder **[!UICONTROL Email retry parameters]** -Felder, ist die Aktualisierung sofort.

### Details aktualisieren {#update-details}

Für Kanaloberflächen mit **[!UICONTROL Active]** -Status, können Sie die Details der Aktualisierung überprüfen. Gehen Sie dazu folgendermaßen vor:

Klicken Sie auf **[!UICONTROL Recent update]** neben dem Namen der aktiven Oberfläche angezeigt.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

Im **[!UICONTROL Recent update]** angezeigt, können Sie Informationen wie den Aktualisierungsstatus und die Liste der angeforderten Änderungen sehen.

<!--![](assets/preset-recent-update-screen.png)-->

### Status aktualisieren {#update-statuses}

Ein Update der Kanaloberfläche kann die folgenden Status aufweisen:

* **[!UICONTROL Processing]**: Die Aktualisierung der Kanaloberfläche wurde eingereicht und durchläuft derzeit mehrere Überprüfungsschritte.
* **[!UICONTROL Success]**: Die aktualisierte Kanaloberfläche wurde überprüft und kann zum Erstellen von Nachrichten ausgewählt werden.
* **[!UICONTROL Failed]**: Bei der Überprüfung der Kanaloberfläche sind eine oder mehrere Prüfungen fehlgeschlagen.

Jeder Status wird nachfolgend beschrieben.

#### Verarbeitung {#surface-processing}

Es werden mehrere Zustellbarkeitsprüfungen durchgeführt, um zu überprüfen, ob die Oberfläche ordnungsgemäß aktualisiert wurde.

>[!NOTE]
>
>Wenn Sie nur die **[!UICONTROL Description]**, **[!UICONTROL Email type]** und/oder **[!UICONTROL Email retry parameters]** -Felder, ist die Aktualisierung sofort.

Die Verarbeitungszeit kann bis **3 Stunden**. Weitere Informationen zu den während des Validierungszyklus durchgeführten Prüfungen finden Sie unter [diesem Abschnitt](#create-channel-surface).

Wenn Sie eine bereits aktive Oberfläche bearbeiten:

* Sein Status bleibt erhalten **[!UICONTROL Active]** während der Validierung ausgeführt wird.

* Die **[!UICONTROL Recent update]** neben dem Namen der Oberfläche in der Liste der Kanaloberflächen angezeigt.

* Während des Validierungsprozesses verwenden die auf dieser Oberfläche konfigurierten Nachrichten weiterhin die ältere Version der Oberfläche.

>[!NOTE]
>
>Während der Aktualisierung kann die Kanaloberfläche nicht geändert werden. Sie können weiterhin auf den Namen klicken, aber alle Felder sind ausgegraut. Die Änderungen werden erst dann übernommen, wenn die Aktualisierung erfolgreich war.

#### Erfolg {#success}

Nach erfolgreicher Validierung wird die neue Version der Oberfläche automatisch in allen Nachrichten verwendet, die diese Oberfläche verwenden. Sie müssen jedoch möglicherweise warten:
* einige Minuten vor der Nutzung durch die einheitlichen Nachrichten,
* bis zum nächsten Batch, damit die Oberfläche in Batch-Nachrichten wirksam ist.

#### Fehlgeschlagen {#failed}

Wenn der Validierungsprozess fehlschlägt, wird weiterhin die ältere Version der Oberfläche verwendet.

Weitere Informationen zu möglichen Fehlerursachen finden Sie unter [diesem Abschnitt](#monitor-channel-surfaces).

Wenn die Aktualisierung fehlschlägt, wird die Oberfläche wieder bearbeitbar. Sie können auf den Namen klicken und die Einstellungen aktualisieren, die korrigiert werden müssen.

## Deaktivieren der Kanaloberfläche {#deactivate-a-surface}

So erstellen Sie eine **[!UICONTROL Active]** Kanaloberfläche nicht verfügbar, um neue Nachrichten zu erstellen, können Sie sie deaktivieren. Die Nachrichten von Journeys, die derzeit diese Oberfläche verwenden, sind jedoch nicht betroffen und funktionieren weiterhin.

>[!NOTE]
>
>Eine Kanaloberfläche kann während der Verarbeitung einer Aktualisierung nicht deaktiviert werden. Sie müssen warten, bis die Aktualisierung erfolgreich war oder fehlgeschlagen ist. Weitere Informationen finden Sie unter [Bearbeitungskanalflächen](#edit-channel-surface) und auf [Aktualisierungsstatus](#update-statuses).

1. Rufen Sie die Liste der Kanaloberflächen auf.

1. Klicken Sie für die aktive Oberfläche Ihrer Wahl auf die **[!UICONTROL More actions]** Schaltfläche.

1. Auswählen **[!UICONTROL Deactivate]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Deaktivierte Kanaloberflächen können nicht gelöscht werden, um Probleme bei Journeys zu vermeiden, die diese Oberflächen zum Senden von Nachrichten verwenden.

Eine deaktivierte Kanaloberfläche kann nicht direkt bearbeitet werden. Sie können sie jedoch duplizieren und die Kopie bearbeiten, um eine neue Version zu erstellen, mit der Sie neue Nachrichten erstellen. Sie können sie auch erneut aktivieren und warten, bis die Aktualisierung erfolgreich abgeschlossen wurde.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
