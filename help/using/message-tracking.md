---
title: Verfolgen von Nachrichten
description: Erfahren Sie, wie Sie Links hinzufügen und gesendete Nachrichten verfolgen können.
feature: Überwachung
topic: Content-Management
role: User
level: Intermediate
source-git-commit: f5a6a9b6c786b39b492a177de0b19a54b81729f7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 72%

---

# Links hinzufügen und Nachrichten verfolgen {#tracking}

Verwenden Sie [!DNL Journey Optimizer], um Links zu Ihrem Inhalt hinzuzufügen und die gesendeten Nachrichten zu verfolgen, um das Verhalten Ihrer Empfänger zu überwachen.

## Tracking aktivieren {#enable-tracking}

Sie können das Tracking auf Nachrichtenebene aktivieren, indem Sie die Optionen **[!UICONTROL Tracking der Öffnungen bei E-Mails]** und/oder **[!UICONTROL Tracking der Klicks bei E-Mails]** beim [Erstellen Ihrer Nachricht](create-message.md) markieren.

![](assets/message-tracking.png)

>[!NOTE]
>
>Beide Optionen sind standardmäßig aktiviert.

Auf diese Weise können Sie das folgende Verhalten Ihrer Empfänger verfolgen:
* **[!UICONTROL Tracking der Öffnungen bei E-Mails]**: Nachrichten, die geöffnet wurden.
* **[!UICONTROL Tracking der Klicks bei E-Mails]**: Klicks auf Links in einer E-Mail.

## Links einfügen {#insert-links}

Beim Entwerfen einer Nachricht können Sie Links zu Ihren Inhalten hinzufügen.

>[!NOTE]
>
>Wenn das [Tracking aktiviert ist](#enable-tracking), werden alle im Nachrichteninhalt enthaltenen Links verfolgt.

Gehen Sie wie folgt vor, um Links in Ihren E-Mail-Inhalt einzufügen:

1. Wählen Sie zuerst ein Element aus und danach in der dedizierten Symbolleiste die Option **[!UICONTROL Link einfügen]**.

   ![](assets/message-tracking-insert-link.png)

1. Wählen Sie den gewünschten Link-Typ aus.

   * **[!UICONTROL Externer Link]**: Fügen Sie einen Link auf eine externe URL ein.

   * **[!UICONTROL Abmelde-Link]**: Fügen Sie einen Link ein, über den man sich vom Erhalt von Nachrichten Ihrer Marke abmelden kann. Weitere Informationen zur Opt-out-Verwaltung finden Sie in [diesem Abschnitt](consent.md#opt-out-management).

   * **[!UICONTROL Mirrorseite]**: Fügen Sie einen Link ein, um den E-Mail-Inhalt in einem Webbrowser anzuzeigen. Weiterführende Informationen finden Sie in diesem [Abschnitt](#mirror-page).

   ![](assets/message-tracking-links.png)

1. Sie können Ihre Links personalisieren, indem Sie nur einen einfachen Ausdruck verwenden. Weitere Informationen zur Personalisierung finden Sie in [diesem Abschnitt](personalization/personalization-syntax.md).

1. Speichern Sie Ihre Änderungen.

1. Sie können auch nach dem Erstellen des Links noch Änderungen im Bereich der **[!UICONTROL Komponenteneinstellungen]** auf der rechten Seite vornehmen.

   * Klicken Sie auf das Stiftsymbol, um den Link zu bearbeiten.
   * Sie können den Link unterstreichen oder nicht unterstreichen, indem Sie die entsprechende Option markieren.

   ![](assets/message-tracking-link-settings.png)

## Link zu einer Mirrorseite {#mirror-page}

Die Mirrorseite ist eine HTML-Seite, auf die online über einen Webbrowser zugegriffen werden kann. Der Inhalt entspricht dem Inhalt Ihrer E-Mail.

Um einen Link zu einer Mirrorseite zu Ihrer E-Mail hinzuzufügen, fügen Sie [einen Link](#insert-links) ein und wählen Sie **[!UICONTROL Mirrorseite]** als Link-Typ aus.

![](assets/message-tracking-mirror-page.png)

Die Mirrorseite wird automatisch erstellt.

>[!NOTE]
>
>Der automatisch generierte Link kann nicht bearbeitet werden.

Wenn die Empfänger nach dem Versand der E-Mail auf den Mirrorseiten-Link klicken, wird der Inhalt der E-Mail in ihrem Standard-Webbrowser angezeigt.

>[!NOTE]
>
>Im an die Testprofile gesendeten [Testversand](preview.md#send-proofs) ist der Link zur Mirrorseite nicht aktiv. Er wird erst in den endgültigen Nachrichten aktiviert.

Die Aufbewahrungsfrist für eine Mirrorseite beträgt 60 Tage. Nach dieser Verzögerung ist die Mirrorseite nicht mehr verfügbar.

## Tracking verwalten {#manage-tracking}

Mit [Email Designer](create-email-content.md) können Sie die verfolgten URLs verwalten, z. B. den Tracking-Typ für jeden Link bearbeiten.

1. Klicken Sie auf das Symbol **[!UICONTROL Links]** im linken Bereich, um die Liste aller URLs Ihres Inhalts, die verfolgt werden sollen, anzuzeigen.

   Diese Liste bietet einen guten Überblick und ermöglicht das Auffinden aller im E-Mail-Inhalt vorhandenen URLs.

1. Um einen Link zu bearbeiten, wählen Sie das entsprechende Stiftsymbol aus.

   ![](assets/message-tracking-edit-links.png)

1. Sie können den **[!UICONTROL Tracking-Typ]** bei Bedarf ändern:


   ![](assets/message-tracking-edit-a-link.png)

   Für jede verfolgte URL können Sie einen der folgenden Tracking-Modi festlegen:

   * **[!UICONTROL Verfolgt]**: Aktiviert das Tracking dieser URL.
   * **[!UICONTROL Opt-out]**: Diese URL wird als Opt-out- oder Abmelde-URL behandelt.
   * **[!UICONTROL Mirrorseite]**: Diese URL wird als Mirror-Seite behandelt.
   * **[!UICONTROL Nie]**: Das Tracking dieser URL wird nie aktiviert. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Die Anzahl der geöffneten Nachrichten und der angeklickten Links sind auf der Registerkarte [Ausführungen](message-monitoring.md) aufgeführt.

Das Reporting zu Öffnungen und Klicks ist im [E-Mail-Live-Bericht](reports/email-live-report.md) und im [Globalen E-Mail-Bericht](reports/email-global-report.md) verfügbar.


