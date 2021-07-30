---
title: Erstellen von Nachrichtenvorgaben
description: Erfahren Sie, wie Sie Nachrichtenvorgaben konfigurieren und überwachen
feature: Anwendungskonfiguration
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 7e879a56a5ed416cc12c2acc3131e17f9dd1e757
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 100%

---


# Erstellen von Nachrichtenvorgaben

Mit [!DNL Journey Optimizer] können Sie Nachrichtenvorgaben einrichten, die alle technischen Parameter definieren, die für E-Mail- und Push-Benachrichtigungen erforderlich sind: E-Mail-Typ, Absender-E-Mail und Name, Mobile Apps und mehr.

>[!CAUTION]
>
> * Die Konfiguration von Nachrichtenvorgaben ist auf Journey-Administratoren beschränkt. [Weitere Informationen](../administration/ootb-product-profiles.md#journey-administrator)
   >
   > 
* Sie müssen die Konfigurationsschritte für E-Mail und Push-Benachrichtigungen ausführen, bevor Sie Nachrichtenvoreinstellungen definieren.


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

1. Konfigurieren von **E-Mail**-Einstellungen.

   ![](../assets/preset-email.png)

   * Wählen Sie den Nachrichtentyp aus, der mit der Vorgabe gesendet werden soll: **Transaktion** oder **Marketing**

      >[!CAUTION]
      >
      > **Transaktions**-Nachrichten können an Profile gesendet werden, die sich von Marketing-Nachrichten abgemeldet haben. Diese Nachrichten können nur in bestimmten Kontexten gesendet werden, z. B. beim Zurücksetzen des Passworts, beim Bestellstatus oder bei Versandbenachrichtigungen.

   * Wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll. [Weitere Informationen](about-subdomain-delegation.md)
   * Wählen Sie den IP-Pool aus, der mit der Vorgabe verknüpft werden soll. [Weitere Informationen](ip-pools.md)
   * Geben Sie die Header-Parameter für die mit der Vorgabe gesendeten E-Mails ein.

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


1. Konfigurieren der Einstellungen für **Push-Benachrichtigungen**.

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

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Nachrichtenvoreinstellung den Status **[!UICONTROL Aktiv]**. Sie kann nun zum Versand von Nachrichten verwendet werden.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Überwachen von Nachrichtenvorgaben

Alle Ihre Nachrichtenvorgaben werden im Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Nachrichtenvorgaben]** angezeigt. Ihnen stehen Filter zur Verfügung, mit denen Sie die Liste durchsuchen können (Kanaltyp, Benutzer, Status).

![](../assets/preset-filters.png)

Nachrichtenvorgaben können die folgenden Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Nachrichtenvorgabe wurde als Entwurf gespeichert und noch nicht gesendet. Öffnen Sie sie, um die Konfiguration fortzusetzen.
* **[!UICONTROL Verarbeitung]**: Die Nachrichtenvorgabe wurde übermittelt und durchläuft mehrere Überprüfungsschritte.
* **[!UICONTROL Aktiv]**: Die Nachrichtenvorgabe wurde verifiziert und kann zum Erstellen von Nachrichten ausgewählt werden.
* **[!UICONTROL Fehlgeschlagen]**: Eine oder mehrere Prüfungen sind bei der Verifizierung der Nachrichtenvorgabe fehlgeschlagen.
* **[!UICONTROL Deaktiviert]**: Die Nachrichtenvorgabe ist deaktiviert. Sie kann nicht zum Erstellen neuer Nachrichten verwendet werden.

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
   >Deaktivierte Nachrichtenvorgaben können nicht gelöscht werden, um Probleme in Journeys zu vermeiden, die diese Vorgaben zum Senden von Nachrichten verwenden.

## Anleitungsvideo{#video-presets}

Erfahren Sie, wie Sie Nachrichtenvoreinstellungen definieren und verwenden, eine Subdomain zuweisen und einen IP-Pool erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
