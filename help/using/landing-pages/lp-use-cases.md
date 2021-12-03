---
title: Anwendungsfälle für Landingpages
description: Die häufigsten Anwendungsfälle für Landingpages in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 27%

---

# Anwendungsfälle für Landingpages

Im Folgenden finden Sie Beispiele für die Verwendung von [!DNL Journey Optimizer] -Landingpages verwenden, damit Ihre Kunden bestimmte oder alle Ihre Nachrichten an- bzw. abmelden können.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Dienstanmeldung {#subscription-to-a-service}

Die wichtigsten Schritte, mit denen Ihre Empfänger einen Dienst abonnieren sollen, sind unten dargestellt.

![](../assets/lp_subscription-uc.png)

Angenommen, Sie organisieren im nächsten Monat eine Veranstaltung und möchten eine Kampagne zur Ereignisregistrierung starten, um interessierte Kunden über diese Veranstaltung auf dem Laufenden zu halten.

1. Erstellen Sie die Abonnementliste der Ereignisregistrierung. Weitere Informationen finden Sie unter [Abonnementlisten](subscription-list.md)

1. [Landingpage erstellen](create-lp.md), damit sich Ihre Empfänger bei Ihrem Ereignis registrieren können.

1. Konfigurieren und gestalten Sie die Anmelde-Landingpage, einschließlich des Links zur Abonnementliste. Weitere Informationen zum Erstellen der [primäre Landingpage](create-lp.md#configure-primary-page)

1. Erstellen Sie eine Dankeseite, die Ihren Empfängern angezeigt wird, sobald sie das Registrierungsformular übermitteln. Weitere Informationen finden Sie unter [Landingpages](create-lp.md#configure-subpages)

1. Erstellen Sie eine E-Mail-Nachricht. Weitere Informationen finden Sie unter [Nachrichten erstellen](../create-message.md)

1. [Link einfügen](../message-tracking.md#insert-links) in Ihrer Nachricht. Auswählen **[!UICONTROL Landingpage]** als **[!UICONTROL Link-Typ]** und wählen Sie die [Landingpage](create-lp.md#configure-primary-page) die Sie für die Registrierung erstellt haben.

   ![](../assets/lp_subscription-uc-link.png)

1. Speichern Sie den Inhalt und [veröffentlichen Sie Ihre Nachricht](../publish-manage-message.md).

1. Senden Sie die Nachricht über eine [Journey](../building-journeys/journey.md) , um die Registrierung anzukündigen, ist nun für Ihr Ereignis geöffnet und ermöglicht Ihnen, den Traffic zur Anmelde-Landingpage zu leiten.

   Wenn Ihre Empfänger nach dem Erhalt der E-Mail auf den Link zur Landingpage klicken, werden sie zur Dankeseite weitergeleitet und auf die Abonnementliste gesetzt.

1. Sie können eine Bestätigungs-E-Mail an die Empfänger senden, die sich für Ihr Ereignis registriert haben. Senden Sie es dazu über eine andere Journey mit der **[!UICONTROL Segmentqualifizierung]** und wählen Sie die Abonnementliste aus, die Sie als Segment erstellt haben.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Abwahl {#opt-out}

Damit sich Ihre Empfänger von Ihrer Nachricht abmelden können, können Sie in Ihre E-Mails einen Link zu einer Opt-out-Landingpage einfügen.

Erfahren Sie mehr über die Verwaltung der Zustimmung Ihrer Empfänger und darüber, warum dies in [diesem Abschnitt](../consent.md).

### Opt-out-Verwaltung {#opt-out-management}

Die Möglichkeit für Empfänger, den Empfang von Mitteilungen einer Marke zu kündigen, ist eine gesetzliche Anforderung. Weitere Informationen zu den geltenden Rechtsvorschriften finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=de){target=&quot;_blank&quot;}.

Aus diesem Grund müssen Sie in jeder E-Mail, die an Empfänger gesendet wird, immer einen **Link zur Abmeldung** einfügen:

* Durch das Klicken auf diesen Link werden die Empfänger zu einer Landingpage mit einer Schaltfläche zur Bestätigung weitergeleitet.
* Nach dem Klicken auf die Opt-out-Schaltfläche werden die Profildaten mit diesen Informationen aktualisiert.

### Konfigurieren des Opt-outs {#configure-opt-out}

Gehen Sie wie folgt vor, um Empfängern einer Nachricht zu ermöglichen, sich über eine Landingpage von Ihrer Nachricht abzumelden.

1. Erstellen Sie Ihre [Landingpage](create-lp.md). Landingpage-spezifisch verwenden **[!UICONTROL Formular]** -Komponente, definieren Sie eine **[!UICONTROL Opt-out]** und wählen Sie die Option **[!UICONTROL Kanal (E-Mail)]**: Das Profil, das das Opt-out-Feld auf Ihrer Landingpage aktiviert, wird von all Ihrer Kommunikation ausgeschlossen. [Weitere Informationen](design-lp.md)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. [Erstellen Sie eine Nachricht](../create-message.md) in [!DNL Journey Optimizer].

1. Wählen Sie Text in Ihrem Inhalt aus und [Link einfügen](../message-tracking.md#insert-links) über die dedizierte Symbolleiste. Sie können auch einen Link auf einer Schaltfläche verwenden.

   ![](../assets/lp_opt-out-insert-link.png)

1. Auswählen **[!UICONTROL Landingpage]** von **[!UICONTROL Link-Typ]** Dropdown-Liste.

1. Wählen Sie die [Landingpage](create-lp.md#configure-primary-page) die Sie für die Abmeldung erstellt haben.

   ![](../assets/lp_opt-out-landing-page.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

1. Speichern Sie den Inhalt und [veröffentlichen Sie Ihre Nachricht](../publish-manage-message.md).

1. Senden Sie die Nachricht über eine [Journey](../building-journeys/journey.md).

1. Wenn der Empfänger nach Erhalt der Nachricht auf den Abmelde-Link klickt, wird Ihre Landingpage angezeigt.

   <!--![](../assets/lp_opt-out-lp-example.png)-->

1. Wenn der Empfänger auf den Abmelde-Link in der Landingpage klickt, werden die Profildaten aktualisiert und erhalten keine Nachrichten von Ihrer Marke, es sei denn, er hat sich erneut angemeldet.

   <!--The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.-->

   <!--![](../assets/lp_opt-out-confirmation-example.png)-->

Um sich zu vergewissern, dass die Aktualisierung des betreffenden Profils erfolgt ist, öffnen Sie das Profil in Adobe Experience Platform, indem Sie einen Identity-Namespace und einen entsprechenden Identitätswert auswählen. Weitere Informationen finden Sie in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=de#getting-started){target=&quot;_blank&quot;}.

![](../assets/lp_opt-out-profile-choice.png)

Auf der Registerkarte **[!UICONTROL Attribute]** sehen Sie, dass der Wert für **[!UICONTROL choice]** auf **[!UICONTROL no]** geändert wurde.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->