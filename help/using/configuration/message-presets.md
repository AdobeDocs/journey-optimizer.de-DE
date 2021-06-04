---
title: Nachrichtenvorgaben erstellen
description: Erfahren Sie, wie Sie Nachrichtenvorgaben konfigurieren und überwachen
source-git-commit: 6cabe17f67d0207fc72d3c61498fae0affe5a785
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---


# Nachrichtenvorgaben erstellen

Mit [!DNL Journey Optimizer] können Sie Nachrichtenvorgaben einrichten, die alle technischen Parameter definieren, die für E-Mail- und Push-Benachrichtigungen erforderlich sind: E-Mail-Typ, Absender-E-Mail und Name, mobile Apps und mehr.

>[!CAUTION]
>
> Die Konfiguration von Nachrichtenvorgaben ist auf Journey-Administratoren beschränkt. [Weitere Infos](../administration/ootb-product-profiles.md#journey-administrator)


Nachdem die Nachrichtenvorgaben konfiguriert wurden, können Sie sie beim Erstellen von Nachrichten aus der Liste **[!UICONTROL Vorgaben]** auswählen.

## Nachrichtenvorgabe {#create-message-preset} erstellen

Gehen Sie wie folgt vor, um eine Nachrichtenvorgabe zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Nachrichtenvorgaben]** auf und klicken Sie dann auf **[!UICONTROL Nachrichtenvorgabe erstellen]**.

   ![](../assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Vorgabe ein und wählen Sie dann die zu konfigurierenden Kanäle aus.

   ![](../assets/preset-general.png)


   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A-Z) beginnen. Sie darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen `_`, Punkt`.` und Bindestrich `-` verwenden.

1. Konfigurieren Sie die Einstellungen **email** .

   ![](../assets/preset-email.png)

   * Wählen Sie den Nachrichtentyp aus, der mit der Vorgabe gesendet werden soll: **Transactional** oder **Marketing**

      >[!CAUTION]
      >
      > **** Transaktionsnachrichten können an Profile gesendet werden, die sich von Marketing-Nachrichten abgemeldet haben. Diese Nachrichten können nur in bestimmten Kontexten gesendet werden, z. B. beim Zurücksetzen des Kennworts, beim Bestellstatus oder bei Versandbenachrichtigungen.

   * Wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll. [Weitere Infos](about-subdomain-delegation.md)
   * Wählen Sie den IP-Pool aus, der mit der Vorgabe verknüpft werden soll. [Weitere Infos](ip-pools.md)
   * Geben Sie die Header-Parameter für die mit der Vorgabe gesendeten E-Mails ein.

      >[!NOTE]
      >
      > * Namen müssen mit einem Buchstaben (A-Z) beginnen. Sie darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen `_`, Punkt`.` und Bindestrich `-` verwenden.
         > 
         > 
      * Mit Ausnahme von **Antwort an (Weiterleiten von E-Mails)** muss die E-Mail-Adressen-Domain die aktuelle ausgewählte Subdomain verwenden.



1. Konfigurieren Sie die Einstellungen für **Push-Benachrichtigung**.

   ![](../assets/preset-push.png)

   * Wählen Sie mindestens eine Plattform aus: **iOS** und/oder **Android**

   * Wählen Sie für jede Plattform die zu verwendenden Mobile Apps aus.

      Weiterführende Informationen zur Konfiguration Ihrer Umgebung für den Versand von Push-Benachrichtigungen finden Sie in [diesem Abschnitt](../push-configuration.md).

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]** . Sie können die Nachrichtenvorgabe auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

   ![](../assets/preset-submit.png)

1. Nachdem die Nachrichtenvorgabe erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt.

   Während dieses Schritts werden mehrere Prüfungen durchgeführt, um zu überprüfen, ob die Konfiguration korrekt ist. Die Verarbeitungszeit liegt bei **48h-72h** und kann bis zu **7-10 Tage** dauern.

   Zu diesen Prüfungen gehören Zustellbarkeitstests, die vom Zustellbarkeitsteam der Adobe durchgeführt werden:

   * SPF-Validierung
   * DKIM-Validierung
   * MX-Datensatzvalidierung
   * IP-auf die Blockierungsliste setz überprüfen
   * Helo-Host-Prüfung
   * IP-Poolverifizierung
   * A/PTR-Eintrag, Subdomain-Verifizierung t/m/res

1. Sobald die Prüfungen erfolgreich sind, erhält die Nachrichtenvorgabe den Status **[!UICONTROL Aktiv]** . Es kann zum Versand von Nachrichten verwendet werden.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Überwachen von Nachrichtenvorgaben

Alle Ihre Nachrichtenvorgaben werden im Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Nachrichtenvorgaben]** angezeigt. Es stehen Filter zur Verfügung, mit denen Sie die Liste durchsuchen können (Kanaltyp, Benutzer, Status).

![](../assets/preset-filters.png)

Nachrichtenvorgaben können die folgenden Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Nachrichtenvorgabe wurde als Entwurf gespeichert und wurde noch nicht gesendet. Öffnen Sie es, um die Konfiguration fortzusetzen.
* **[!UICONTROL Verarbeitung]**: Die Nachrichtenvorgabe wurde gesendet und durchläuft mehrere Überprüfungsschritte.
* **[!UICONTROL Aktiv]**: Die Nachrichtenvorgabe wurde überprüft und kann zum Erstellen von Nachrichten ausgewählt werden.
* **[!UICONTROL Fehlgeschlagen]**: Eine oder mehrere Prüfungen sind bei der Überprüfung der Nachrichtenvorgabe fehlgeschlagen.
* **[!UICONTROL Deaktivierung]**: Die Nachrichtenvorgabe ist deaktiviert. Sie kann nicht zum Erstellen neuer Nachrichten verwendet werden.

## Bearbeiten von Nachrichtenvorgaben

Um eine Nachrichtenvorgabe zu bearbeiten, müssen Sie sie zunächst deaktivieren, um sie zum Erstellen neuer Nachrichten nicht verfügbar zu machen (veröffentlichte Nachrichten, die diese Vorgabe verwenden, sind davon nicht betroffen und funktionieren weiterhin). Sie müssen dann die Nachrichtenvorgabe duplizieren, um eine neue Version zu erstellen, mit der Sie neue Nachrichten erstellen:

1. Rufen Sie die Liste der Nachrichtenvorgaben auf und deaktivieren Sie dann die zu bearbeitende Nachrichtenvorgabe.

   ![](../assets/preset-deactivate.png)

1. Duplizieren Sie die deaktivierte Nachrichtenvorgabe. Eine Kopie mit dem Status **[!UICONTROL Entwurf]** wird der Liste automatisch hinzugefügt.

   ![](../assets/preset-duplicated.png)

1. Öffnen Sie die duplizierte Nachrichtenvorgabe, ändern Sie sie entsprechend Ihren Anforderungen und senden Sie dann Ihre Änderungen. Die Nachrichtenvorgabe durchläuft denselben Validierungszyklus wie während des Erstellungsschritts [a1/>.](#create-message-preset)

1. Nach der Validierung erhält es den Status **[!UICONTROL Aktiv]** und kann zum Erstellen neuer Nachrichten verwendet werden.

   >[!NOTE]
   >
   >Deaktivierte Nachrichtenvorgaben können nicht gelöscht werden, um Probleme in Journey zu vermeiden, die diese Vorgaben zum Senden von Nachrichten verwenden.

