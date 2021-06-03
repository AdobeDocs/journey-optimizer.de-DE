---
title: Nachrichtenvorgaben erstellen
description: Erfahren Sie, wie Sie E-Mail- und Push-Benachrichtigungsvorgaben erstellen
source-git-commit: 4353b8f01bb4e47f6f2384e464341c0ee80ecaf2
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---


# Nachrichtenvorgaben erstellen

Mit [!DNL Journey Optimizer] können Sie Nachrichtenvorgaben einrichten, die alle technischen Parameter definieren, die für E-Mail- und Push-Benachrichtigungen erforderlich sind (E-Mail-Typ, Absender-E-Mail und Name, Mobile Apps usw.).

Je nach den verschiedenen Marken, für die Sie kommunizieren müssen, können Sie beliebig viele Nachrichtenvorgaben einrichten.

Nachdem die Nachrichtenvorgaben konfiguriert wurden, können Sie sie beim Erstellen von Nachrichten aus der Liste **[!UICONTROL Vorgaben]** auswählen.

## Nachrichtenvorgabe {#create-message-preset} erstellen

Gehen Sie wie folgt vor, um eine Nachrichtenvorgabe zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Nachrichtenvorgaben]** auf und klicken Sie dann auf **[!UICONTROL Nachrichtenvorgabe erstellen]**.

   ![](../assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Vorgabe ein und geben Sie dann die Kanäle an, die Sie konfigurieren möchten.

   ![](../assets/preset-general.png)

1. Konfigurieren Sie die Einstellungen für E-Mail- und Push-Benachrichtigungen:

   Geben Sie für den E-Mail-Kanal Folgendes an:

   * Die Art der mit der Vorgabe gesendeten Nachrichten (Transaktions- oder Marketingnachrichten),
   * Die [Subdomain](about-subdomain-delegation.md), die zum Senden der E-Mails verwendet werden soll,
   * Der [IP-Pool](ip-pools.md), der mit der Vorgabe verknüpft werden soll,
   * Die Kopfzeilenparameter, die für die mit der Vorgabe gesendeten E-Mails verwendet werden sollen.

   ![](../assets/preset-email.png)

   Geben Sie für den Push-Benachrichtigungskanal die iOS- und/oder Android-Mobile-Apps an, die für Ihre Nachrichten verwendet werden sollen. Weiterführende Informationen zur Konfiguration Ihrer Umgebung für den Versand von Push-Benachrichtigungen finden Sie in [diesem Abschnitt](../push-configuration.md).

   ![](../assets/preset-push.png)

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]** . Sie können die Nachrichtenvorgabe auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

   ![](../assets/preset-submit.png)

1. Nachdem die Nachrichtenvorgabe erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt.

   Während dieses Schritts werden mehrere Prüfungen durchgeführt, um zu überprüfen, ob die Konfiguration korrekt ist. Die Verarbeitungszeit beträgt ca. 48-72 Stunden und kann bis zu 7-10 Tage dauern.

   Zu diesen Prüfungen gehören Zustellbarkeitstests, die vom Zustellbarkeitsteam der Adobe durchgeführt werden:

   * SPF-Validierung,
   * DKIM-Validierung,
   * MX-Datensatzvalidierung,
   * IP-Adressen auf die Blacklist setzen,
   * Helo-Host-Prüfung,
   * Verifizierung des IP-Pools,
   * A/PTR-Eintrag, Verifizierung der Subdomain von t/m/res.

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