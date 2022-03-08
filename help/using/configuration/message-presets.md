---
title: Erstellen von Nachrichtenvoreinstellungen
description: Erfahren Sie, wie Sie Nachrichtenvoreinstellungen konfigurieren und überwachen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '1771'
ht-degree: 99%

---

# Erstellen von Nachrichtenvoreinstellungen {#message-presets-creation}

Mit [!DNL Journey Optimizer] können Sie Nachrichtenvoreinstellungen einrichten, die alle technischen Parameter definieren, die für E-Mail- und Push-Benachrichtigungen erforderlich sind: E-Mail-Typ, Absender-E-Mail und Name, Mobile Apps und mehr.

>[!CAUTION]
>
> * Die Konfiguration von Nachrichtenvoreinstellungen ist auf Journey-Administratoren beschränkt. [Weitere Informationen](../administration/ootb-product-profiles.md#journey-administrator)
>
> * Sie müssen die Konfigurationsschritte für E-Mail und [Push-Benachrichtigungen](../messages/push-configuration.md) ausführen, bevor Sie Nachrichtenvoreinstellungen definieren.


Nachdem Nachrichtenvoreinstellungen konfiguriert wurden, können Sie diese beim Erstellen von Nachrichten aus der Liste der **[!UICONTROL Voreinstellungen]** auswählen.

➡️ [Erfahren Sie in diesem Video, wie Sie E-Mail-Voreinstellungen definieren und verwenden](#video-presets).

>[!NOTE]
>
>Erfahren Sie, wie Sie Landingpage-Vorgaben erstellen in [diesem Abschnitt](../configuration/lp-configuration.md#lp-create-preset).

## Nachrichtenvoreinstellungen erstellen {#create-message-preset}

Gehen Sie wie folgt vor, um eine Nachrichtenvoreinstellung zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Branding]** > **[!UICONTROL Nachrichtenvoreinstellungen]** auf und klicken Sie dann auf **[!UICONTROL Nachrichtenvoreinstellung erstellen]**.

   ![](../assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Voreinstellung ein und wählen Sie dann die zu konfigurierenden Kanäle aus.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Konfigurieren von **E-Mail**-Einstellungen. [Weitere Informationen](#configure-email-settings)

1. Konfigurieren Sie die Einstellungen für **Push-Benachrichtigungen**. [Weitere Informationen](#configure-push-settings)

   <!--Configure SMS settings. [Learn more](#configure-sms-settings) -->

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]**. Sie können die Nachrichtenvoreinstellung auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

   ![](../assets/preset-submit.png)

1. Nachdem die Nachrichtenvoreinstellung erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt.

   Während dieses Schritts werden mehrere Prüfungen durchgeführt, um zu verifizieren, dass die Konfiguration korrekt ist. Die Verarbeitungszeit liegt bei **48–72 Stunden** und kann bis zu **7–10 Werktage** betragen.

   Zu diesen Prüfungen gehören Konfigurations- und technische Tests, die vom Adobe-Team durchgeführt werden:

   * SPF-Validierung
   * DKIM-Validierung
   * MX-Eintragsvalidierung
   * Überprüfung der Blockierungsliste der IPs
   * Helo-Host-Prüfung
   * IP-Pool-Verifizierung
   * A/PTR-Eintrag, Subdomain-Verifizierung t/m/res

   >[!NOTE]
   >
   >In [diesem Abschnitt](#monitor-message-presets) erfahren Sie mehr über die möglichen Fehlerursachen, wenn die Prüfungen nicht erfolgreich sind.

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Nachrichtenvoreinstellung den Status **[!UICONTROL Aktiv]**. Sie kann nun zum Versand von Nachrichten verwendet werden.

   ![](../assets/preset-active.png)

## Konfigurieren von E-Mail-Einstellungen {#configure-email-settings}

![](../assets/preset-email.png)

1. Wählen Sie den Nachrichtentyp aus, der mit der Voreinstellung gesendet werden soll: **Transaktion** oder **Marketing**.

   >[!CAUTION]
   >
   > **Transaktions**-Nachrichten können an Profile gesendet werden, die sich von Marketing-Nachrichten abgemeldet haben. Diese Nachrichten können nur in bestimmten Kontexten gesendet werden, z. B. beim Zurücksetzen des Passworts, beim Bestellstatus oder bei Versandbenachrichtigungen.

1. Wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll. [Weitere Informationen](about-subdomain-delegation.md)

1. Wählen Sie den IP-Pool aus, der mit der Voreinstellung verknüpft werden soll. [Weitere Informationen](ip-pools.md)

1. Geben Sie die Header-Parameter für die mit der Voreinstellung gesendeten E-Mails ein.

   >[!CAUTION]
   >
   >E-Mail-Adressen müssen die aktuell ausgewählte [delegierte Subdomain](about-subdomain-delegation.md) verwenden.

   * **[!UICONTROL Absendername]**: Der Name des Absenders, wie z. B. der Name Ihrer Marke.

   * **[!UICONTROL Absender-E-Mail]**: Die E-Mail-Adresse, die Sie für Ihre Kommunikation verwenden möchten. Wenn die zugewiesene Subdomain beispielsweise *marketing.luma.com* lautet, können Sie *contact@marketing.luma.com* verwenden.

   * **[!UICONTROL Antwort an (Name)]**: Der Name, der verwendet wird, wenn der Empfänger in seiner E-Mail-Client-Software auf den Button **Antworten** klickt.

   * **[!UICONTROL Antwort an (E-Mail)]**: Die E-Mail-Adresse, die verwendet wird, wenn der Empfänger in seiner E-Mail-Client-Software auf den Button **Antworten** klickt. Sie müssen eine Adresse verwenden, die in der zugewiesenen Subdomain definiert ist (z. B. *reply@marketing.luma.com*), da ansonsten die E-Mails gelöscht werden.

   * **[!UICONTROL E-Mail-Fehler]**: An dieser Adresse werden alle Fehlermeldungen empfangen, die von ISPs nach einigen Tagen der E-Mail-Zustellung erzeugt wurden (asynchrone Bounces).
   >[!NOTE]
   >
   >Ab der Version vom Oktober 2021 ist es nicht mehr möglich, in der [!DNL Journey Optimizer]-Benutzeroberfläche eine Weiterleitungs-E-Mail-Adresse zu definieren. Wenn Sie möchten, dass alle bei [!DNL Journey Optimizer] für die delegierte Subdomain eingegangenen E-Mails an eine bestimmte E-Mail-Adresse weitergeleitet werden, wenden Sie sich an das [Supportteam der Adobe-Kundenunterstützung](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

   ![](../assets/preset-header.png)

   >[!NOTE]
   >
   >Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Konfigurieren Sie die **Parameter für weitere Zustellversuche bei E-Mails**. Standardmäßig ist der [Zeitraum für weitere Zustellversuche](retries.md#retry-duration) auf 84 Stunden festgelegt. Sie können diese Einstellung jedoch an Ihre Anforderungen anpassen.

   ![](../assets/preset-retry-paramaters.png)

   Sie müssen einen ganzzahligen Wert (in Stunden oder Minuten) innerhalb des folgenden Bereichs eingeben:
   * Für den Marketing-E-Mail-Typ beträgt der Mindestzeitraum für weitere Zustellversuche 6 Stunden.
   * Für den Transaktions-E-Mail-Typ beträgt der Mindestzeitraum für weitere Zustellversuche 10 Minuten.
   * Für beide E-Mail-Typen beträgt der maximale Zeitraum für weitere Zustellversuch 84 Stunden (oder 5.040 Minuten).

## Konfigurieren der Push-Einstellungen {#configure-push-settings}

1. Wählen Sie mindestens eine Plattform aus: **iOS** und/oder **Android**.

1. Wählen Sie für jede Plattform die zu verwendenden Mobile Apps aus.

![](../assets/preset-push.png)

Weiterführende Informationen zur Konfiguration Ihrer Umgebung für den Versand von Push-Benachrichtigungen finden Sie in [diesem Abschnitt](../messages/push-gs.md).

<!--
## Configure SMS settings {#configure-sms-settings}

1. Select the **[!UICONTROL SMS Type]** that will be sent with the preset: **[!UICONTROL Transactional]** or **[!UICONTROL Marketing]**.

    ![](../assets/preset-sms.png)
    
1. Select the **[!UICONTROL SMS configuration]** to associate with the preset.
        
    For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Enter the **[!UICONTROL Sender number]** ​you want to use for your communications.
-->

## Überwachen von Nachrichtenvoreinstellungen {#monitor-message-presets}

Alle Ihre Nachrichtenvoreinstellungen werden im Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Nachrichtenvoreinstellungen]** angezeigt. Ihnen stehen Filter zur Verfügung, mit denen Sie die Liste durchsuchen können (Kanaltyp, Benutzer, Status).

![](../assets/preset-filters.png)

Nachrichtenvoreinstellungen können die folgenden Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Nachrichtenvoreinstellung wurde als Entwurf gespeichert und noch nicht gesendet. Öffnen Sie sie, um die Konfiguration fortzusetzen.
* **[!UICONTROL Verarbeitung]**: Die Nachrichtenvoreinstellung wurde übermittelt und durchläuft mehrere Überprüfungsschritte.
* **[!UICONTROL Aktiv]**: Die Nachrichtenvoreinstellung wurde verifiziert und kann zum Erstellen von Nachrichten ausgewählt werden.
* **[!UICONTROL Fehlgeschlagen]**: Eine oder mehrere Prüfungen sind bei der Verifizierung der Nachrichtenvoreinstellung fehlgeschlagen.
* **[!UICONTROL Deaktiviert]**: Die Nachrichtenvoreinstellung ist deaktiviert. Sie kann nicht zum Erstellen neuer Nachrichten verwendet werden.

Im Folgenden finden Sie Details zu möglichen Fehlerursachen, falls die Erstellung einer Nachrichtenvoreinstellung fehlschlägt. 

Wenn einer dieser Fehler auftritt, wenden Sie sich an das [Adobe-Kundenunterstützung-Team](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}, um Hilfe zu erhalten.

* **SPF-Validierung fehlgeschlagen**: SPF (Sender Policy Framework) ist ein E-Mail-Authentifizierungsprotokoll, mit dem autorisierte IPs angegeben werden können, die E-Mails von einer bestimmten Subdomain senden können. Ein SPF-Validierungsfehler bedeutet, dass die IP-Adressen im SPF-Datensatz nicht mit den IP-Adressen übereinstimmen, die zum Senden von E-Mails an die E-Mail-Anbieter verwendet werden.

* **DKIM-Validierung fehlgeschlagen**: Mit DKIM (DomainKeys Identified Mail) kann der Empfänger-Server überprüfen, ob die empfangene Nachricht vom echten Absender der zugehörigen Domain gesendet wurde, und sicherstellen, dass der Inhalt der ursprünglichen Nachricht nicht auf dem Weg verändert wurde. Ein DKIM-Validierungsfehler bedeutet, dass die Empfangs-Mail-Server die Authentizität des Nachrichteninhalts und dessen Zuordnung zur Versand-Domain nicht überprüfen können.:

* **MX-Eintragsvalidierung fehlgeschlagen**: Ein MX-Eintragsvalidierungsfehler (Mail eXchange) bedeutet, dass die E-Mail-Server, die für die Annahme eingehender E-Mails für eine bestimmte Subdomain verantwortlich sind, nicht korrekt konfiguriert sind.

* **Zustellbarkeitskonfigurationen fehlgeschlagen**: Zustellbarkeitskonfigurationsfehler können aus einem der folgenden Gründe auftreten:
   * Blockierungsauflistung der zugewiesenen IPs
   * Ungültiger `helo`-Name
   * E-Mails, die von anderen IPs als den im IP-Pool der entsprechenden Voreinstellung angegebenen gesendet werden
   * E-Mails können nicht an Posteingänge wichtiger ISPs wie Gmail und Yahoo gesendet werden

## Bearbeiten einer Nachrichtenvoreinstellung {#edit-message-preset}

Gehen Sie wie folgt vor, um eine Nachrichtenvoreinstellung zu bearbeiten.

>[!NOTE]
>
>Die **[!UICONTROL Einstellungen für Push-Benachrichtigungen]** können Sie nicht bearbeiten. Wenn eine Nachrichtenvoreinstellung nur für den Kanal Push-Benachrichtigung konfiguriert ist, kann sie nicht bearbeitet werden.

1. Klicken Sie in der Liste auf den Namen einer Nachrichtenvoreinstellung, um sie zu öffnen.

   ![](../assets/preset-name.png)

1. Bearbeiten Sie die Eigenschaften nach Bedarf.

   >[!NOTE]
   >
   >Wenn eine Nachrichtenvoreinstellung den Status **[!UICONTROL Aktiv]** hat, sind die Felder **[!UICONTROL Name]**, **[!UICONTROL Kanal auswählen]** und **[!UICONTROL Subdomain]** grau dargestellt und können nicht bearbeitet werden.

1. Klicken Sie auf **[!UICONTROL Senden]**, um Ihre Änderungen zu bestätigen.

   ![](../assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >Sie können die Nachrichtenvoreinstellung auch als Entwurf speichern und die Aktualisierung zu einem späteren Zeitpunkt wieder aufnehmen.

Sobald die Änderungen übermittelt wurden, durchläuft die Nachrichtenvoreinstellung einen ähnlichen Validierungszyklus wie beim [Erstellen einer Voreinstellung](#create-message-preset).

>[!NOTE]
>
>Wenn Sie nur die Felder **[!UICONTROL Beschreibung]**, **[!UICONTROL E-Mail-Typ]** und/oder **[!UICONTROL E-Mail-Wiederholungsparameter]** bearbeiten, wird die Aktualisierung sofort wirksam.

Für Nachrichtenvoreinstellungen mit dem Status **[!UICONTROL Aktiv]** können Sie die Details der Aktualisierung überprüfen. Gehen Sie dazu wie folgt vor:

* Klicken Sie auf das Symbol **[!UICONTROL Letzte Aktualisierung]**, das neben dem Namen der aktiven Voreinstellung angezeigt wird.

   ![](../assets/preset-recent-update-icon.png)

* Sie können auch während der Aktualisierung über eine aktive Nachrichtenvoreinstellung auf die Aktualisierungsdetails zugreifen.

   ![](../assets/preset-view-update-details.png)

Auf dem Bildschirm **[!UICONTROL Letzte Aktualisierung]** können Sie Informationen wie den Aktualisierungsstatus und die Liste der angeforderten Änderungen sehen.

![](../assets/preset-recent-update-screen.png)

### Aktualisieren des Status {#update-statuses}

Eine Aktualisierung einer Nachrichtenvoreinstellung kann die folgenden Status aufweisen:

* **[!UICONTROL Verarbeitung]**: Die Aktualisierung der Nachrichtenvoreinstellung wurde übermittelt und durchläuft aktuell mehrere Überprüfungsschritte.
* **[!UICONTROL Erfolg]**: Die Nachrichtenvoreinstellung wurde verifiziert und kann zum Erstellen von Nachrichten ausgewählt werden.
* **[!UICONTROL Fehlgeschlagen]**: Eine oder mehrere Prüfungen sind bei der Verifizierung der Nachrichtenvoreinstellung fehlgeschlagen.

Jeder Status wird nachfolgend beschrieben.

### In Bearbeitung

Es werden verschiedene Zustellbarkeitsprüfungen durchgeführt, um sicherzustellen, dass die Voreinstellung ordnungsgemäß aktualisiert wurde.

>[!NOTE]
>
>Wenn Sie nur die Felder **[!UICONTROL Beschreibung]**, **[!UICONTROL E-Mail-Typ]** und/oder **[!UICONTROL E-Mail-Wiederholungsparameter]** bearbeiten, wird die Aktualisierung sofort wirksam.

Die Verarbeitungszeit liegt bei **48–72 Stunden** und kann bis zu **7–10 Werktage** betragen. Weitere Informationen zu den während des Validierungszyklus durchgeführten Prüfungen finden Sie in [diesem Abschnitt](#create-message-preset).

Wenn Sie eine bereits aktive Voreinstellung bearbeiten:

* Ihr Status **[!UICONTROL Aktiv]** bleibt erhalten, während der Validierungsprozess ausgeführt wird.

* Das Symbol **[!UICONTROL Letzte Aktualisierung]** wird neben dem Voreinstellungsnamen in der Liste der Nachrichtenvoreinstellungen angezeigt.

* Während des Validierungsprozesses verwenden die mit dieser Voreinstellung konfigurierten Nachrichten weiterhin die ältere Version der Voreinstellung.

>[!NOTE]
>
>Sie können eine Nachrichtenvoreinstellung während der Aktualisierung nicht ändern. Sie können zwar weiterhin auf den Namen klicken, aber alle Felder sind ausgegraut. Die Änderungen werden erst dann übernommen, wenn die Aktualisierung erfolgreich war.

### Erfolgreich {#success}

Nach erfolgreicher Überprüfung wird die neue Version der Voreinstellung automatisch in allen Nachrichten verwendet, die diese Voreinstellung verwenden. Sie müssen jedoch möglicherweise warten:
* einige Minuten, bevor die Voreinstellung von den einzelnen Nachrichten genutzt wird,
* bis zum nächsten Batch, damit die Voreinstellung in Batch-Nachrichten wirksam wird.

### Fehlgeschlagen {#failed}

Wenn der Validierungsprozess fehlschlägt, wird weiterhin die ältere Version der Voreinstellung verwendet.

Weitere Informationen zu möglichen Fehlerursachen finden Sie in [diesem Abschnitt](#monitor-message-presets).

Wenn die Aktualisierung fehlschlägt, kann die Voreinstellung erneut bearbeitet werden. Sie können auf den Namen klicken und die Einstellungen aktualisieren, die korrigiert werden müssen.

## Deaktivieren von Nachrichtenvoreinstellungen {#deactivate-preset}

Wenn Sie möchten, dass eine **[!UICONTROL aktive]** Nachrichtenvoreinstellung nicht verfügbar ist, um neue Nachrichten zu erstellen, können Sie sie deaktivieren. Die mit dieser Voreinstellung schon veröffentlichten Nachrichten sind jedoch davon nicht betroffen und funktionieren weiterhin.

>[!NOTE]
>
>Sie können eine Nachrichtenvoreinstellung nicht deaktivieren, während eine Aktualisierung im Gange ist. Sie müssen warten, bis die Aktualisierung entweder erfolgreich war oder fehlgeschlagen ist. Weitere Informationen finden Sie unter [Bearbeiten von Nachrichtenvoreinstellungen](#edit-message-preset) und [Aktualisierungsstatus](#update-statuses).

1. Rufen Sie die Liste der Nachrichtenvoreinstellungen auf.

1. Klicken Sie für die aktive Voreinstellung Ihrer Wahl auf die Schaltfläche **[!UICONTROL Weitere Aktionen]**.

1. Wählen Sie **[!UICONTROL Deaktivieren]** aus.

   ![](../assets/preset-deactivate.png)

>[!NOTE]
>
>Deaktivierte Nachrichtenvoreinstellungen können nicht gelöscht werden, um Probleme in Journeys zu vermeiden, die diese Voreinstellungen zum Senden von Nachrichten verwenden.

Eine deaktivierte Nachrichtenvoreinstellung kann nicht direkt bearbeitet werden. Sie können sie jedoch duplizieren und die Kopie bearbeiten, um eine neue Version zu entwerfen, mit der Sie neue Nachrichten erstellen können. Sie können sie auch erneut aktivieren und warten, bis die Aktualisierung erfolgreich abgeschlossen wird, bevor Sie sie bearbeiten.

![](../assets/preset-activate.png)

## Anleitungsvideo{#video-presets}

Erfahren Sie, wie Sie Nachrichtenvoreinstellungen definieren und verwenden, eine Subdomain zuweisen und einen IP-Pool erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
