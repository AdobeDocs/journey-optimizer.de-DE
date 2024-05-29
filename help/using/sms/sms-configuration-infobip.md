---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines Infobip-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten und MMS mit Journey Optimizer mit Infobip konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 99%

---

# Konfigurieren eines Infobip-Anbieters {#sms-configuration-infobip}

Gehen Sie wie folgt vor, um Infobip mit Journey Optimizer zu konfigurieren:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]** aus. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre API-Anmeldedaten, wie unten beschrieben.

   * **[!UICONTROL SMS-Anbieter]**: Infobip.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL API-Basis-URL]** und **[!UICONTROL API-Schlüssel]**: Rufen Sie die Startseite Ihrer Web-Oberfläche oder die Seite zur Verwaltung von API-Schlüsseln auf. Dort finden Sie Ihre Anmeldedaten. Weitere Informationen finden Sie in der [Infobip-Dokumentation](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Opt-in-Keywords]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **[!UICONTROL Opt-in-Nachricht]** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Opt-in-Nachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Ihre **[!UICONTROL Opt-in-Nachricht]** gesendet wird.

   * **[!UICONTROL Opt-out-Keywords]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **[!UICONTROL Opt-out-Nachricht]** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Opt-out-Nachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als **[!UICONTROL Opt-out-Nachricht]** gesendet wird.

   * **[!UICONTROL Hilfe-Keywords]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **Hilfenachricht** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Hilfenachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als **Hilfenachricht** gesendet wird.

   * **[!UICONTROL Double-Opt-in-Suchbegriffe]**: Geben Sie die Suchbegriffe ein, die den Double-Opt-in-Prozess auslösen. Wenn kein Benutzerprofil vorhanden ist, wird es nach erfolgreicher Bestätigung erstellt. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Double-Opt-in-Nachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Antwort auf die Double-Opt-in-Bestätigung gesendet wird.

   * **[!UICONTROL Prinzipalentitäts-ID]**: Geben Sie die Ihnen zugewiesene DLT-Prinzipalentitäts-ID ein.

   * **[!UICONTROL Inhaltsvorlagen-ID]**: Geben Sie Ihre registrierte DLT-Inhaltsvorlagen-ID ein.

   * **[!UICONTROL Gültigkeitszeitraum]**: Geben Sie den Gültigkeitszeitraum der Nachricht in Stunden an. Wenn Nachrichten nicht innerhalb dieses Zeitrahmens zugestellt werden können, unternimmt das System zusätzliche Versuche, sie erneut zu senden. Der standardmäßige Gültigkeitszeitraum beträgt 48 Stunden.

   * **[!UICONTROL Callback-Daten]**: Geben Sie die zusätzlichen Client-Daten ein, die an die Benachrichtigungs-URL gesendet werden.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie nun eine Kanaloberfläche für SMS- und MMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)
