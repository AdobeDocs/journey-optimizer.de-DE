---
title: Erstellen von Nachrichtenvorgaben
description: Erfahren Sie, wie Sie Nachrichtenvorgaben konfigurieren und überwachen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 70%

---


# Erstellen von Nachrichtenvorgaben

Mit [!DNL Journey Optimizer] können Sie Nachrichtenvorgaben einrichten, die alle technischen Parameter definieren, die für E-Mail- und Push-Benachrichtigungen erforderlich sind: E-Mail-Typ, Absender-E-Mail und Name, Mobile Apps und mehr.

>[!CAUTION]
>
> * Die Konfiguration von Nachrichtenvorgaben ist auf Journey-Administratoren beschränkt. [Weitere Informationen](../administration/ootb-product-profiles.md#journey-administrator)
>
> * Sie müssen die Konfigurationsschritte für E-Mail und Push-Benachrichtigungen ausführen, bevor Sie Nachrichtenvoreinstellungen definieren.


Nachdem die Nachricht konfiguriert wurde, können Sie sie beim Erstellen von Nachrichten aus der Liste **[!UICONTROL Voreinstellungen]** auswählen.

➡️ [Erfahren Sie in diesem Video, wie Sie E-Mail-Voreinstellungen definieren und verwenden](#video-presets).

## Nachrichtenvoreinstellungen erstellen {#create-message-preset}

Gehen Sie wie folgt vor, um eine Nachrichtenvorgabe zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Nachrichtenvorgaben]** auf und klicken Sie dann auf **[!UICONTROL Nachrichtenvorgabe erstellen]**.

   ![](../assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Vorgabe ein und wählen Sie dann die zu konfigurierenden Kanäle aus.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Konfigurieren Sie die Einstellungen **email** .

   ![](../assets/preset-email.png)

   * Wählen Sie den Nachrichtentyp aus, der mit der Vorgabe gesendet werden soll: **Transaktion** oder **Marketing**

      >[!CAUTION]
      >
      > **Transaktions**-Nachrichten können an Profile gesendet werden, die sich von Marketing-Nachrichten abgemeldet haben. Diese Nachrichten können nur in bestimmten Kontexten gesendet werden, z. B. beim Zurücksetzen des Passworts, beim Bestellstatus oder bei Versandbenachrichtigungen.

   * Wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll. [Weitere Informationen](about-subdomain-delegation.md)
   * Wählen Sie den IP-Pool aus, der mit der Vorgabe verknüpft werden soll. [Weitere Informationen](ip-pools.md)
   * Geben Sie die Header-Parameter für die mit dieser Vorgabe gesendeten E-Mails ein.

      >[!CAUTION]
      >
      >Mit Ausnahme des Feldes **Antwort an (Weiterleiten der E-Mail)** muss die Domain der E-Mail-Adressen die aktuell ausgewählte [zugewiesene Subdomain](about-subdomain-delegation.md) verwenden.

      * **[!UICONTROL Name des Absenders]**: Name des Absenders, wie z. B. der Name Ihrer Marke.

      * **[!UICONTROL Absender-E-Mail]**: Die E-Mail-Adresse, die Sie für Ihre Kommunikation verwenden möchten. Wenn die zugewiesene Subdomain beispielsweise *marketing.luma.com* lautet, können Sie *contact@marketing.luma.com* verwenden.

      * **[!UICONTROL Antwort an (Name)]**: Der Name, der verwendet wird, wenn der Empfänger in seiner E-Mail-Client-Software auf den Button **Antworten** klickt.

      * **[!UICONTROL Antwort an (E-Mail)]**: Die E-Mail-Adresse, die verwendet wird, wenn der Empfänger in seiner E-Mail-Client-Software auf den Button **Antworten** klickt. Die an diese Adresse gesendeten E-Mails werden an die unten angegebene Adresse **[!UICONTROL Antwort an (Weiterleitungs-E-Mail)]** weitergeleitet. Sie müssen eine Adresse verwenden, die in der zugewiesenen Subdomain definiert ist (z. B. *reply@marketing.luma.com*), da ansonsten die E-Mails gelöscht werden.

      * **[!UICONTROL Antwort an (Weiterleitungs-E-Mail)]**: Alle E-Mails, die von [!DNL Journey Optimizer] für die zugewiesene Subdomain empfangen wurden, werden an diese E-Mail-Adresse weitergeleitet. Sie können eine beliebige Adresse angeben, mit Ausnahme einer E-Mail-Adresse, die in der zugewiesenen Subdomain definiert ist. Wenn die zugewiesene Subdomain beispielsweise *marketing.luma.com* lautet, ist jede Adresse wie *abc@marketing.luma.com* verboten.

      * **[!UICONTROL E-Mail-Fehler]**: An dieser Adresse werden alle Fehler empfangen, die von ISPs nach wenigen Tagen der E-Mail-Zustellung erzeugt wurden (asynchrone Bounces).

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

   * Konfigurieren Sie die **E-Mail-Neuversuch-Parameter**. Standardmäßig ist der [Zeitraum für erneute Versuche](retries.md#retry-duration) auf 84 Stunden festgelegt. Sie können diese Einstellung jedoch an Ihre Anforderungen anpassen.

      ![](../assets/preset-retry-paramaters.png)

      Sie müssen einen ganzzahligen Wert (in Stunden oder Minuten) innerhalb des folgenden Bereichs eingeben:
      * Für den Marketing-E-Mail-Typ beträgt die Wiederholungsdauer mindestens 6 Stunden.
      * Für den Transaktions-E-Mail-Typ beträgt die Wiederholungsdauer mindestens 10 Minuten.
      * Für beide E-Mail-Typen beträgt der maximale Wiederholungszeitraum 84 Stunden (oder 5040 Minuten).


1. Konfigurieren Sie die Einstellungen für **Push-Benachrichtigung**.

   ![](../assets/preset-push.png)

   * Wählen Sie mindestens eine Plattform aus: **iOS** und/oder **Android**.

   * Wählen Sie für jede Plattform die zu verwendenden Mobile Apps aus.

      Weiterführende Informationen zur Konfiguration Ihrer Umgebung für den Versand von Push-Benachrichtigungen finden Sie in [diesem Abschnitt](../push-gs.md).

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]**. Sie können die Nachrichtenvorgabe auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

   ![](../assets/preset-submit.png)

1. Nachdem die Nachrichtenvorgabe erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt.

   Während dieses Schritts werden mehrere Prüfungen durchgeführt, um zu verifizieren, dass die Konfiguration korrekt ist. Die Verarbeitungszeit liegt bei **48–72 Stunden** und kann bis zu **7–10 Tage** betragen.

   Zu diesen Prüfungen gehören Zustellbarkeitstests, die vom Adobe-Zustellbarkeits-Team durchgeführt werden:

   * SPF-Validierung
   * DKIM-Validierung
   * MX-Eintragsvalidierung
   * Überprüfung der Blockierungsliste der IPs
   * Helo-Host-Prüfung
   * IP-Pool-Verifizierung
   * A/PTR-Eintrag, Subdomain-Verifizierung t/m/res

   >[!NOTE]
   >
   >Wenn die Prüfungen nicht erfolgreich sind, erfahren Sie mehr über die möglichen Fehlerursachen in [diesem Abschnitt](#monitor-message-presets).

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Nachrichtenvoreinstellung den Status **[!UICONTROL Aktiv]**. Sie kann nun zum Versand von Nachrichten verwendet werden.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Überwachen von Nachrichtenvorgaben {#monitor-message-presets}

Alle Ihre Nachrichtenvorgaben werden im Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Nachrichtenvorgaben]** angezeigt. Ihnen stehen Filter zur Verfügung, mit denen Sie die Liste durchsuchen können (Kanaltyp, Benutzer, Status).

![](../assets/preset-filters.png)

Nachrichtenvorgaben können die folgenden Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Nachrichtenvorgabe wurde als Entwurf gespeichert und noch nicht gesendet. Öffnen Sie sie, um die Konfiguration fortzusetzen.
* **[!UICONTROL Verarbeitung]**: Die Nachrichtenvorgabe wurde übermittelt und durchläuft mehrere Überprüfungsschritte.
* **[!UICONTROL Aktiv]**: Die Nachrichtenvorgabe wurde verifiziert und kann zum Erstellen von Nachrichten ausgewählt werden.
* **[!UICONTROL Fehlgeschlagen]**: Eine oder mehrere Prüfungen sind bei der Verifizierung der Nachrichtenvorgabe fehlgeschlagen.
* **[!UICONTROL Deaktiviert]**: Die Nachrichtenvorgabe ist deaktiviert. Sie kann nicht zum Erstellen neuer Nachrichten verwendet werden.

Wenn die Erstellung einer Nachrichtenvorgabe fehlschlägt, werden die Details zu den möglichen Fehlerursachen nachfolgend beschrieben.

Wenn einer dieser Fehler auftritt, wenden Sie sich an das [Adobe-Support-Team der Kundenunterstützung](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}, um Hilfe zu erhalten.

* **SPF-Validierung fehlgeschlagen**: SPF (Sender Policy Framework) ist ein E-Mail-Authentifizierungsprotokoll, mit dem autorisierte IPs angegeben werden können, die E-Mails von einer bestimmten Subdomain senden können. SPF-Validierungsfehler bedeutet, dass die IP-Adressen im SPF-Datensatz nicht mit den IP-Adressen übereinstimmen, die zum Senden von E-Mails an die Postfachanbieter verwendet werden.

* **DKIM-Validierung fehlgeschlagen**: Mit DKIM kann der Empfängerserver überprüfen, ob die empfangene Nachricht vom echten Absender der zugehörigen Domain gesendet wurde und ob der Inhalt der ursprünglichen Nachricht nicht auf dem Weg verändert wurde. DKIM-Validierungsfehler bedeutet, dass die Empfangs-Mail-Server die Authentizität des Nachrichteninhalts und dessen Zuordnung zur Versanddomäne nicht überprüfen können.

* **MX-Datensatzvalidierung fehlgeschlagen**: MX-Datensatz-Validierungsfehler bedeutet, dass die E-Mail-Server, die für die Annahme eingehender E-Mails im Namen einer bestimmten Subdomain verantwortlich sind, nicht korrekt konfiguriert sind.

* **Zustellbarkeitskonfigurationen fehlgeschlagen**: Zustellbarkeitskonfigurationen können aus einem der folgenden Gründe fehlschlagen:
   * Blockierungsauflistung der zugewiesenen IPs
   * Ungültiger `helo`-Name
   * E-Mails, die von anderen als den im IP-Pool der entsprechenden Vorgabe angegebenen IPs gesendet werden
   * E-Mails können nicht an Postfächer wichtiger ISPs wie Gmail und Yahoo gesendet werden

## Bearbeiten von Nachrichtenvorgaben

Um eine Nachrichtenvorgabe zu bearbeiten, müssen Sie sie zunächst deaktivieren, damit sie für das Erstellen neuer Nachrichten nicht verfügbar ist (veröffentlichte Nachrichten, die diese Vorgabe verwenden, sind davon nicht betroffen und funktionieren weiterhin). Sie müssen die Nachrichtenvorgabe duplizieren, um eine neue Version zu erstellen, mit der Sie dann neue Nachrichten erstellen:

1. Rufen Sie die Liste der Nachrichtenvorgaben auf und deaktivieren Sie dann die zu bearbeitende Nachrichtenvorgabe.

   ![](../assets/preset-deactivate.png)

1. Duplizieren Sie die deaktivierte Nachrichtenvorgabe. Eine Kopie mit dem Status **[!UICONTROL Entwurf]** wird der Liste automatisch hinzugefügt.

   ![](../assets/preset-duplicated.png)

1. Öffnen Sie die duplizierte Nachrichtenvorgabe, ändern Sie sie entsprechend Ihren Anforderungen und übermitteln Sie dann Ihre Änderungen. Die Nachrichtenvorgabe durchläuft denselben Validierungszyklus wie während des [Erstellungsschritts](#create-message-preset).

1. Nach der Validierung erhält sie den Status **[!UICONTROL Aktiv]** und kann zum Erstellen neuer Nachrichten verwendet werden.

   >[!NOTE]
   >
   >Deaktivierte Nachrichtenvorgaben können nicht gelöscht werden, um Probleme in Journey zu vermeiden, die diese Vorgaben zum Senden von Nachrichten verwenden.

## Anleitungsvideo{#video-presets}

Erfahren Sie, wie Sie Nachrichtenvoreinstellungen definieren und verwenden, eine Subdomain zuweisen und einen IP-Pool erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
