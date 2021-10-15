---
title: Erstellen von Nachrichtenvoreinstellungen
description: Erfahren Sie, wie Sie Nachrichtenvoreinstellungen konfigurieren und überwachen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 100%

---

# Erstellen von Nachrichtenvoreinstellungen

Mit [!DNL Journey Optimizer] können Sie Nachrichtenvoreinstellungen einrichten, die alle technischen Parameter definieren, die für E-Mail- und Push-Benachrichtigungen erforderlich sind: E-Mail-Typ, Absender-E-Mail und Name, Mobile Apps und mehr.

>[!CAUTION]
>
> * Die Konfiguration von Nachrichtenvoreinstellungen ist auf Journey-Administratoren beschränkt. [Weitere Informationen](../administration/ootb-product-profiles.md#journey-administrator)
>
> * Sie müssen die Konfigurationsschritte für E-Mail und Push-Benachrichtigungen ausführen, bevor Sie Nachrichtenvoreinstellungen definieren.


Nachdem die Nachricht konfiguriert wurde, können Sie sie beim Erstellen von Nachrichten aus der Liste **[!UICONTROL Voreinstellungen]** auswählen.

➡️ [Erfahren Sie in diesem Video, wie Sie E-Mail-Voreinstellungen definieren und verwenden](#video-presets).

## Nachrichtenvoreinstellungen erstellen {#create-message-preset}

Gehen Sie wie folgt vor, um eine Nachrichtenvoreinstellung zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Nachrichtenvoreinstellungen]** auf und klicken Sie dann auf **[!UICONTROL Nachrichtenvoreinstellung erstellen]**.

   ![](../assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Voreinstellung ein und wählen Sie dann die zu konfigurierenden Kanäle aus.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Konfigurieren von **E-Mail**-Einstellungen.

   ![](../assets/preset-email.png)

   * Wählen Sie den Nachrichtentyp aus, der mit der Voreinstellung gesendet werden soll: **Transaktion** oder **Marketing**

      >[!CAUTION]
      >
      > **Transaktions**-Nachrichten können an Profile gesendet werden, die sich von Marketing-Nachrichten abgemeldet haben. Diese Nachrichten können nur in bestimmten Kontexten gesendet werden, z. B. beim Zurücksetzen des Passworts, beim Bestellstatus oder bei Versandbenachrichtigungen.

   * Wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll. [Weitere Informationen](about-subdomain-delegation.md)
   * Wählen Sie den IP-Pool aus, der mit der Voreinstellung verknüpft werden soll. [Weitere Informationen](ip-pools.md)
   * Geben Sie die Header-Parameter für die mit der Voreinstellung gesendeten E-Mails ein.

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

   * Konfigurieren Sie die **Parameter für weitere Zustellversuche bei E-Mails**. Standardmäßig ist der [Zeitraum für weitere Zustellversuche](retries.md#retry-duration) auf 84 Stunden festgelegt. Sie können diese Einstellung jedoch an Ihre Anforderungen anpassen.

      ![](../assets/preset-retry-paramaters.png)

      Sie müssen einen ganzzahligen Wert (in Stunden oder Minuten) innerhalb des folgenden Bereichs eingeben:
      * Für den Marketing-E-Mail-Typ beträgt der Mindestzeitraum für weitere Zustellversuche 6 Stunden.
      * Für den Transaktions-E-Mail-Typ beträgt der Mindestzeitraum für weitere Zustellversuche 10 Minuten.
      * Für beide E-Mail-Typen beträgt der maximale Zeitraum für weitere Zustellversuch 84 Stunden (oder 5.040 Minuten).


1. Konfigurieren Sie die Einstellungen für **Push-Benachrichtigungen**.

   ![](../assets/preset-push.png)

   * Wählen Sie mindestens eine Plattform aus: **iOS** und/oder **Android**.

   * Wählen Sie für jede Plattform die zu verwendenden Mobile Apps aus.

      Weiterführende Informationen zur Konfiguration Ihrer Umgebung für den Versand von Push-Benachrichtigungen finden Sie in [diesem Abschnitt](../push-gs.md).

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]**. Sie können die Nachrichtenvoreinstellung auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

   ![](../assets/preset-submit.png)

1. Nachdem die Nachrichtenvoreinstellung erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt.

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
   >In [diesem Abschnitt](#monitor-message-presets) erfahren Sie mehr über die möglichen Fehlerursachen, wenn die Prüfungen nicht erfolgreich sind.

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Nachrichtenvoreinstellung den Status **[!UICONTROL Aktiv]**. Sie kann nun zum Versand von Nachrichten verwendet werden.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Überwachen von Nachrichtenvoreinstellungen {#monitor-message-presets}

Alle Ihre Nachrichtenvoreinstellungen werden im Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Nachrichtenvoreinstellungen]** angezeigt. Ihnen stehen Filter zur Verfügung, mit denen Sie die Liste durchsuchen können (Kanaltyp, Benutzer, Status).

![](../assets/preset-filters.png)

Nachrichtenvoreinstellungen können die folgenden Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Nachrichtenvoreinstellung wurde als Entwurf gespeichert und noch nicht gesendet. Öffnen Sie sie, um die Konfiguration fortzusetzen.
* **[!UICONTROL Verarbeitung]**: Die Nachrichtenvoreinstellung wurde übermittelt und durchläuft mehrere Überprüfungsschritte.
* **[!UICONTROL Aktiv]**: Die Nachrichtenvoreinstellung wurde verifiziert und kann zum Erstellen von Nachrichten ausgewählt werden.
* **[!UICONTROL Fehlgeschlagen]**: Eine oder mehrere Prüfungen sind bei der Verifizierung der Nachrichtenvoreinstellung fehlgeschlagen.
* **[!UICONTROL Deaktiviert]**: Die Nachrichtenvoreinstellung ist deaktiviert. Sie kann nicht zum Erstellen neuer Nachrichten verwendet werden.

Im Folgenden finden Sie Details zu möglichen Fehlerursachen, falls die Erstellung einer Nachrichtenvoreinstellung fehlschlägt. 

Wenn einer dieser Fehler auftritt, wenden Sie sich an das [Adobe-Kundenunterstützung-Team](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}, um Hilfe zu erhalten.

* **SPF-Validierung fehlgeschlagen**: SPF (Sender Policy Framework) ist ein E-Mail-Authentifizierungsprotokoll, mit dem autorisierte IPs angegeben werden können, die E-Mails von einer bestimmten Subdomain senden können. Ein SPF-Validierungsfehler bedeutet, dass die IP-Adressen im SPF-Datensatz nicht mit den IP-Adressen übereinstimmen, die zum Senden von E-Mails an die E-Mail-Anbieter verwendet werden.

* **DKIM-Validierung fehlgeschlagen**: Mit DKIM (DomainKeys Identified Mail) kann der Empfänger-Server überprüfen, ob die empfangene Nachricht vom echten Absender der zugehörigen Domain gesendet wurde, und sicherstellen, dass der Inhalt der ursprünglichen Nachricht nicht auf dem Weg verändert wurde. Ein DKIM-Validierungsfehler bedeutet, dass die Empfangs-Mail-Server die Authentizität des Nachrichteninhalts und dessen Zuordnung zur Versand-Domain nicht überprüfen können.:

* **MX-Eintragsvalidierung fehlgeschlagen**: Ein MX-Eintragsvalidierungsfehler (Mail eXchange) bedeutet, dass die E-Mail-Server, die für die Annahme eingehender E-Mails für eine bestimmte Subdomain verantwortlich sind, nicht korrekt konfiguriert sind.

* **Zustellbarkeitskonfigurationen fehlgeschlagen**: Zustellbarkeitskonfigurationsfehler können aus einem der folgenden Gründe auftreten:
   * Blockierungsauflistung der zugewiesenen IPs
   * Ungültiger `helo`-Name
   * E-Mails, die von anderen IPs als den im IP-Pool der entsprechenden Voreinstellung angegebenen gesendet werden
   * E-Mails können nicht an Posteingänge wichtiger ISPs wie Gmail und Yahoo gesendet werden

## Bearbeiten von Nachrichtenvoreinstellungen

Um eine Nachrichtenvoreinstellung zu bearbeiten, müssen Sie sie zunächst deaktivieren, damit sie für das Erstellen neuer Nachrichten nicht verfügbar ist (veröffentlichte Nachrichten, die diese Voreinstellung verwenden, sind davon nicht betroffen und funktionieren weiterhin). Sie müssen die Nachrichtenvoreinstellung duplizieren, um eine neue Version zu erstellen, mit der Sie dann neue Nachrichten erstellen:

1. Rufen Sie die Liste der Nachrichtenvoreinstellung auf und deaktivieren Sie die zu bearbeitende Nachrichtenvoreinstellung.

   ![](../assets/preset-deactivate.png)

1. Duplizieren Sie die deaktivierte Nachrichtenvoreinstellung. Eine Kopie mit dem Status **[!UICONTROL Entwurf]** wird der Liste automatisch hinzugefügt.

   ![](../assets/preset-duplicated.png)

1. Öffnen Sie die duplizierte Nachrichtenvoreinstellung, ändern Sie sie entsprechend Ihren Anforderungen und übermitteln Sie dann Ihre Änderungen. Die Nachrichtenvoreinstellung durchläuft denselben Validierungszyklus wie während des [Erstellungsschritts](#create-message-preset).

1. Nach der Validierung erhält sie den Status **[!UICONTROL Aktiv]** und kann zum Erstellen neuer Nachrichten verwendet werden.

   >[!NOTE]
   >
   >Deaktivierte Nachrichtenvoreinstellungen können nicht gelöscht werden, um Probleme in Journeys zu vermeiden, die diese Voreinstellungen zum Nachrichtenversand verwenden.

## Anleitungsvideo{#video-presets}

Erfahren Sie, wie Sie Nachrichtenvoreinstellungen definieren und verwenden, eine Subdomain zuweisen und einen IP-Pool erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
