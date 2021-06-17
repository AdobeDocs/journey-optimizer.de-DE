---
title: Verfolgen von Nachrichten
description: Erfahren Sie, wie Sie gesendete Nachrichten verfolgen können
feature: Überwachung
topic: Content Management
role: User
level: Intermediate
source-git-commit: e27472cc6186cf7cb25fdb93d15720fc837c58bb
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 20%

---

# Nachrichten-Tracking {#tracking}

Verwenden Sie [!DNL Journey Optimizer], um die gesendeten Nachrichten und das Verhalten Ihrer Empfänger zu verfolgen.

## Tracking aktivieren {#enable-tracking}

Sie können das Tracking auf Meldungsebene aktivieren, indem Sie die Optionen **[!UICONTROL Tracking für E-Mail öffnen]** und/oder **[!UICONTROL Auf Tracking für E-Mail]** klicken, wenn [Ihre Nachricht erstellen](create-message.md).

![](assets/message-tracking.png)

>[!NOTE]
>
>Beide Optionen sind standardmäßig aktiviert.

Auf diese Weise können Sie das Verhalten Ihrer Empfänger verfolgen:
* **[!UICONTROL Öffnen Sie Tracking für E-Mail]**: Nachrichten, die geöffnet wurden.
* **[!UICONTROL Klicken Sie für E-Mail]** auf Tracking . Klicks auf Links in einer E-Mail.

## Links einfügen {#insert-links}

Beim Erstellen einer Nachricht können Sie Links zu Ihrem Inhalt hinzufügen.

>[!NOTE]
>
>Wenn die [Verfolgung aktiviert ist](#enable-tracking), werden alle im Nachrichteninhalt enthaltenen Links verfolgt.

Gehen Sie wie folgt vor, um Links in Ihren E-Mail-Inhalt einzufügen:

1. Wählen Sie zuerst ein Element aus und danach in der dedizierten Symbolleiste die Option **[!UICONTROL Link einfügen]**.

   ![](assets/message-tracking-insert-link.png)

1. Wählen Sie den gewünschten Linktyp aus.

   * **[!UICONTROL Externer Link]**: Fügen Sie einen Link zu einer externen URL ein.

   * **[!UICONTROL Abmelde-Link]**: Fügen Sie einen Link ein, um sich vom Erhalt von Nachrichten Ihrer Marke abzumelden. Weitere Informationen zur Opt-out-Verwaltung finden Sie in [diesem Abschnitt](consent.md#opt-out-management).

   * **[!UICONTROL Mirrorseite]**: Fügen Sie einen Link ein, um den E-Mail-Inhalt in einem Webbrowser anzuzeigen.

   ![](assets/message-tracking-links.png)

1. Sie können Ihre Links nur mithilfe eines einfachen Ausdrucks personalisieren. Weitere Informationen zur Personalisierung finden Sie in [diesem Abschnitt](personalization/personalization-syntax.md).

1. Speichern Sie Ihre Änderungen.

1. Nachdem der Link erstellt wurde, können Sie ihn weiterhin im Bereich **[!UICONTROL Komponenteneinstellungen]** auf der rechten Seite ändern.

   * Klicken Sie auf das Stiftsymbol, um den Link zu bearbeiten.
   * Sie können den Link unterstreichen oder nicht, indem Sie die entsprechende Option aktivieren.

   ![](assets/message-tracking-link-settings.png)

## Tracking verwalten {#manage-tracking}

Mit [Email Designer](create-email-content.md) können Sie die getrackten URLs verwalten, z. B. den Tracking-Typ für jeden Link bearbeiten.

1. Klicken Sie im linken Bereich auf das Symbol **[!UICONTROL Links]** , um die Liste aller URLs Ihres Inhalts anzuzeigen, die verfolgt werden sollen.

   Diese Liste bietet einen guten Überblick und ermöglicht das Auffinden aller im E-Mail-Inhalt vorhandenen URLs.

1. Um einen Link zu bearbeiten, wählen Sie das entsprechende Stiftsymbol aus.

   ![](assets/message-tracking-edit-links.png)

1. Sie können den **[!UICONTROL Tracking-Typ]** bei Bedarf ändern:


   ![](assets/message-tracking-edit-a-link.png)

   Für jede getrackte URL können Sie den Tracking-Modus auf einen der folgenden Werte einstellen:

   * **[!UICONTROL Getrackt]**: Aktiviert das Tracking dieser URL.
   * **[!UICONTROL Opt-out]**: Betrachtet diese URL als Ausschluss- oder Abmelde-URL.
   * **[!UICONTROL Mirrorseite]**: betrachtet diese URL als Mirrorseiten-URL.
   * **[!UICONTROL Nie]**: Aktiviert nie das Tracking dieser URL.  <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Die Anzahl der geöffneten Meldungen und die Anzahl der angeklickten Links sind auf der Registerkarte [Ausführungen](message-monitoring.md) aufgeführt.

Die Berichterstellung zu Öffnungen und Klicks ist im [E-Mail-Live-Bericht](reports/email-live-report.md) und im [E-Mail-Global-Bericht](reports/email-global-report.md) verfügbar.


