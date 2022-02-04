---
title: Anwendungsfälle für Landingpages
description: Entdecken Sie die häufigsten Anwendungsfälle für Landingpages in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 100%

---

# Anwendungsfälle für Landingpages {#lp-use-cases}

Im Folgenden finden Sie einige Beispiele für die Verwendung von [!DNL Journey Optimizer]-Landingpages zum kundenseitigen Opt-in/Opt-out für bestimmte oder alle Ihre Nachrichten.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Abonnement eines Services {#subscription-to-a-service}

Einer der häufigsten Anwendungsfälle besteht darin, Ihre Kunden über eine Landingpage zum [Abonnieren eines Services](subscription-list.md) (z. B. eines Newsletters oder einer Veranstaltung) aufzufordern. Die wichtigsten Schritte werden im unten stehenden Diagramm dargestellt:

![](../assets/lp_subscription-uc.png)

Angenommen, Sie organisieren im nächsten Monat eine Veranstaltung und möchten eine Kampagne zur Veranstaltungsregistrierung starten<!--to keep your customers that are interested updated on that event-->. Senden Sie dazu eine E-Mail mit einem Link zu einer Landingpage, über die sich Ihre Empfänger für diese Veranstaltung registrieren können. Die Benutzer, die sich registrieren, werden zur Abonnementliste hinzugefügt, die Sie zu diesem Zweck erstellt haben.

### Einrichten einer Landingpage {#set-up-lp}

1. Erstellen Sie die Abonnementliste für die Veranstaltungsregistrierung, in der die registrierten Benutzer gespeichert werden. [Hier](subscription-list.md#define-subscription-list) erfahren Sie, wie Sie eine Abonnementliste erstellen.

   ![](../assets/lp_subscription-uc-list.png)

1. [Erstellen Sie eine Landingpage](create-lp.md), damit sich Ihre Empfänger für Ihre Veranstaltung registrieren können.

1. Konfigurieren Sie die [primäre Landingpage](create-lp.md#configure-primary-page) für die Registrierung.

1. Wählen Sie beim Entwerfen der [Landingpage-Inhalte](design-lp.md) die von Ihnen erstellte Abonnementliste aus, um sie mit den Profilen zu aktualisieren, die das Registrierungs-Kontrollkästchen anklicken.

   ![](../assets/lp_subscription-uc-lp-list.png)

1. Erstellen Sie eine „Danke“-Seite, die Ihren Empfängern angezeigt wird, sobald sie das Registrierungsformular übermitteln. [Hier](create-lp.md#configure-subpages) erfahren Sie, wie Sie Unterseiten für die Landingpage konfigurieren.

   ![](../assets/lp_subscription-uc-thanks.png)

1. [Veröffentlichen](create-lp.md#publish) Sie die Landingpage.

1. [Erstellen Sie eine E-Mail-Nachricht](../messages/create-message.md), um anzukündigen, dass die Registrierung für die Veranstaltung nun eröffnet ist.

1. [Fügen Sie einen Link](../messages/message-tracking.md#insert-links) in Ihren Nachrichteninhalt ein. Wählen Sie **[!UICONTROL Landingpage]** als **[!UICONTROL Link-Typ]** und wählen Sie die [Landingpage](create-lp.md#configure-primary-page) aus, die Sie für die Registrierung erstellt haben.

   ![](../assets/lp_subscription-uc-link.png)

1. Speichern Sie den Inhalt und [veröffentlichen Sie Ihre Nachricht](../messages/publish-manage-message.md).

1. Senden Sie die Nachricht über eine [Journey](../building-journeys/journey.md), um den Traffic zur Landingpage zur Registrierung zu leiten.

   ![](../assets/lp_subscription-uc-journey.png)

   Wenn Ihre Empfänger nach dem Erhalt der E-Mail auf den Link zur Landingpage klicken, werden sie zur „Danke-Seite“ weitergeleitet und auf die Abonnementliste gesetzt.

### Senden einer Bestätigungs-E-Mail {#send-confirmation-email}

Zusätzlich können Sie eine Bestätigungs-E-Mail an die Empfänger senden, die sich für Ihre Veranstaltung registriert haben. Gehen Sie dazu wie folgt vor.

1. Erstellen Sie eine weitere [Journey](../building-journeys/journey.md). Sie können dies direkt über die Landingpage tun, indem Sie auf die Schaltfläche **[!UICONTROL Journey erstellen]** klicken. [Hier](create-lp.md#configure-primary-page) erhalten Sie weitere Informationen.

   ![](../assets/lp_subscription-uc-create-journey.png)

1. Erweitern Sie die Kategorie **[!UICONTROL Ereignisse]** und legen Sie eine Aktivität vom Typ **[!UICONTROL Segmentqualifikation]** in Ihrer Arbeitsfläche ab. [Hier](../building-journeys/segment-qualification-events.md) erhalten Sie weitere Informationen.

1. Klicken Sie in das Feld **[!UICONTROL Segment]** und wählen Sie die von Ihnen erstellte Abonnementliste aus.

   ![](../assets/lp_subscription-uc-confirm-journey.png)

1. Wählen Sie die gewünschte Bestätigungs-E-Mail aus und senden Sie sie über die Journey.

   ![](../assets/lp_subscription-uc-confirm-email.png)

Alle Benutzer, die sich für Ihre Veranstaltung registriert haben, erhalten die Bestätigungs-E-Mail.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Ausschluss (Opt-out) {#opt-out}

Damit Ihre Empfänger das Abonnement stornieren können, können Sie in Ihre E-Mails einen Link zu einer Ausschluss-Landingpage einfügen.

In [diesem Abschnitt](../messages/consent.md) erfahren Sie mehr über die Verwaltung des Einverständnisses Ihrer Empfänger und darüber, warum dies wichtig ist.

### Opt-out-Verwaltung {#opt-out-management}

Die Möglichkeit für Empfänger, den Empfang von Mitteilungen einer Marke zu kündigen, ist eine gesetzliche Anforderung. Weitere Informationen zu den geltenden Rechtsvorschriften finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=de){target=&quot;_blank&quot;}.

Aus diesem Grund müssen Sie in jeder E-Mail, die an Empfänger gesendet wird, immer einen **Link zur Abmeldung** einfügen:

* Durch das Klicken auf diesen Link werden die Empfänger zu einer Landingpage mit einer Schaltfläche zur Bestätigung weitergeleitet.
* Nach dem Klicken auf die Ausschluss-Schaltfläche werden die Profildaten mit diesen Informationen aktualisiert.

### Konfigurieren des Ausschlusses {#configure-opt-out}

Gehen Sie wie folgt vor, um Empfängern einer Nachricht zu ermöglichen, dieses Abonnement über eine Landingpage zu stornieren.

1. Erstellen Sie Ihre Landingpage. [Weitere Informationen](create-lp.md)

1. Definieren Sie die Primärseite. [Weitere Informationen](create-lp.md#configure-primary-page)

1. [Gestaltung](design-lp.md) des primären Seiteninhalts: Verwenden Sie die Landingpage-spezifische **[!UICONTROL Formular]**-Komponente, definieren Sie ein Kontrollkästchen zum **[!UICONTROL Opt-out]** und wählen Sie die Aktualisierung von **[!UICONTROL Kanal (E-Mail)]**. Jetzt wird jedes Profil, das auf Ihrer Landingpage das Opt-out-Kästchen ankreuzt, von Ihrer gesamten Kommunikation ausgeschlossen.

   ![](../assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. Fügen Sie eine [Unterseite](create-lp.md#configure-subpages) zur Bestätigung hinzu, die den Nutzern angezeigt wird, die das Formular übermitteln.

   ![](../assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >Referenzieren Sie die Unterseite im Abschnitt **[!UICONTROL Call to Action]** der **[!UICONTROL Formular]**-Komponente der Primärseite. [Weitere Informationen](design-lp.md)

1. Nachdem Sie den Inhalt Ihrer Seiten konfiguriert und definiert haben, können Sie die Landingpage [veröffentlichen](create-lp.md#publish).

   ![](../assets/lp_opt-out-publish.png)

1. [Erstellen Sie eine E-Mail-Nachricht](../messages/create-message.md) in [!DNL Journey Optimizer].

1. Wählen Sie Text in Ihrem Inhalt aus und [fügen Sie mithilfe der kontextbezogenen Symbolleiste einen Link ](../messages/message-tracking.md#insert-links) ein. Auch ein Link auf einer Schaltfläche kann verwendet werden.

   ![](../assets/lp_opt-out-insert-link.png)

1. Wählen Sie **[!UICONTROL Landingpage]** aus der Dropdown-Liste **[!UICONTROL Link-Typ]** und wählen Sie die [Landingpage](create-lp.md#configure-primary-page), die Sie für das Opt-out erstellt haben.

   ![](../assets/lp_opt-out-landing-page.png)

1. Speichern Sie den Inhalt und [veröffentlichen Sie Ihre Nachricht](../messages/publish-manage-message.md).

1. Senden Sie eine Nachricht über eine Journey. [Weitere Informationen](../building-journeys/journey.md).

1. Wenn ein Empfänger nach Erhalt der Nachricht auf den Abmelde-Link in der E-Mail klickt, wird Ihre Landingpage angezeigt.

   ![](../assets/lp_opt-out-submit-form.png)

   Wenn der Empfänger das Kästchen aktiviert und das Formular absendet:

   * Der abgemeldete Empfänger wird zum Bestätigungsbildschirm weitergeleitet.

   * Die Profildaten werden aktualisiert und erhalten keine Nachrichten mehr von Ihrer Marke, es sei denn, das Profil meldet sich erneut an.

Um sich zu vergewissern, dass die Aktualisierung des betreffenden Profils erfolgt ist, öffnen Sie das Profil in Adobe Experience Platform, indem Sie einen Identity-Namespace und einen entsprechenden Identitätswert auswählen. Weitere Informationen finden Sie in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=de#getting-started){target=&quot;_blank&quot;}.

![](../assets/lp_opt-out-profile-choice.png)

Auf der Registerkarte **[!UICONTROL Attribute]** sehen Sie, dass der Wert für **[!UICONTROL choice]** auf **[!UICONTROL no]** geändert wurde.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../messages/message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../messages/consent.md#unsubscribe-email)
-->
