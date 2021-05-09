---
title: Abmeldeverwaltung verwalten
description: Erfahren Sie, wie Sie Ausschluss- und Datenschutzeinstellungen verwalten können
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Verwalten der Ausschluss-Option {#consent}

![](assets/do-not-localize/badge.png)

Verwenden Sie [!DNL Journey Optimizer], um die Zustimmung Ihrer Empfänger zur Kommunikation zu verfolgen und zu verstehen, wie sie mit Ihrer Marke interagieren möchten, indem sie ihre Präferenzen und Abonnement verwalten. <!--Their preferences and subscriptions are handled through Consent management.-->

Regeln wie GDPR geben an, dass Sie bestimmte Anforderungen erfüllen müssen, bevor Sie Informationen von Datensubjekten verwenden können. Darüber hinaus sollten die betroffenen Personen ihre Einwilligung jederzeit ändern können.

**Warum ist das wichtig?**

* Die Nichteinhaltung dieser Vorschriften birgt rechtliche Risiken für Ihre Marke.
* Dadurch vermeiden Sie unerwünschte Nachrichten an Ihre Empfänger, die Ihre Nachrichten als Spam kennzeichnen und Ihrem Ruf schaden könnten.

Weitere Informationen zur Verwaltung der Privatsphäre und den geltenden Vorschriften finden Sie in der [Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de).

<!--* Recipients should be able to opt-in/opt-out from receiving electronic communication through one or more channel
* Recipients expect the brand to offer preference centre capability that controls how brand should engage with them (example: channel of communication, invasive and non-invasive tracking etc). This helps to fulfil regulatory obligations and also facilitates quality engagement with recipient. 
* The third category is the capability to offer subscription to recipients (newsletter, etc)-->

## Abmeldeverwaltung {#opt-out-management}

Die Bereitstellung der Möglichkeit für Empfänger, sich vom Empfang von Mitteilungen einer Marke abzumelden, ist eine gesetzliche Voraussetzung. Weitere Informationen zu den geltenden Rechtsvorschriften finden Sie in der [Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=en#regulations).

Daher müssen Sie in jeder E-Mail, die an Empfänger gesendet wird, immer einen **Link zum Abmelden** einfügen:
* Wenn Sie auf diesen Link klicken, werden die Empfänger zu einer Landingpage weitergeleitet, die eine Schaltfläche zur Bestätigung der Abmeldung enthält.
* Wenn Sie auf die Schaltfläche zum Ausschluss klicken, wird ein Adobe I/O-Aufruf durchgeführt, um die Profil-Daten mit diesen Informationen zu aktualisieren. [Erfahren Sie mehr darüber](#consent-service-api).

Gehen Sie wie folgt vor, um einen Link zum Abmelden hinzuzufügen:

1. Erstellen Sie Ihre Abmeldung-Landingpage.
1. Hosten Sie Ihre Landingpage auf dem Drittanbietersystem Ihrer Wahl.
1. [Erstellen Sie eine ](../../help/using/create-message.md) Nachricht  [!DNL Journey Optimizer].

   <!--The link to your landing page should contain a static URL and the profile ID.-->

1. Wählen Sie Text in Ihrem Inhalt aus und fügen Sie mithilfe der Kontextsymbolleiste einen Link ein.

   ![](assets/opt-out-insert-link.png)

1. Wählen Sie **[!UICONTROL Link Abmeldung]** aus der Dropdown-Liste **[!UICONTROL Linktyp]**.

   ![](assets/opt-out-link-type.png)

1. Kopieren Sie im Rahmen der URL der Abmeldung **[!UICONTROL den Link in Ihre Landingpage.]**

   ![](assets/opt-out-link-url.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

1. Speichern Sie den Inhalt und [veröffentlichen Sie die Nachricht](../../help/using/publish-manage-message.md).

   >[!NOTE]
   >
   >Ihre Drittanbieter-Landingpage-URL enthält drei Parameter, mit denen die Voreinstellungen der Profile über einen Adobe I/O-Aufruf aktualisiert werden. &#x200B; [Weitere Informationen finden Sie in diesem Abschnitt](#consent-service-api).

1. Senden Sie Ihre Nachricht mit dem Link zu Ihrer Landingpage über eine [Journey](building-journeys/journey.md).

1. Wenn der Empfänger nach Erhalt der Nachricht auf den Link zum Abbestellen klickt, wird Ihre Landingpage angezeigt.

   ![](assets/opt-out-lp-example.png)

1. Wenn der Empfänger in der Landingpage auf die Abmeldeschaltfläche klickt (hier die Schaltfläche **Abmelden**), werden die Profil-Daten über einen [Adobe I/O-Aufruf](#opt-out-api) aktualisiert.

   Der abgelegte Empfänger wird dann zu einem Bestätigungsbildschirm umgeleitet, der angibt, dass die Abmeldung erfolgreich war.

   ![](assets/opt-out-confirmation-example.png)

   Daher erhält dieser Benutzer keine Kommunikation von Ihrer Marke, es sei denn, er hat sich erneut angemeldet.

Um zu überprüfen, ob die Auswahl des entsprechenden Profils aktualisiert wurde, gehen Sie zur Experience Platform und greifen Sie auf das Profil zu, indem Sie einen Identitäts-Namensraum und einen entsprechenden Identitätswert auswählen. Weitere Informationen finden Sie in der [Dokumentation zur Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=en#getting-started).

![](assets/opt-out-profile-choice.png)

Auf der Registerkarte **[!UICONTROL Attribute]** können Sie sehen, dass der Wert für **[!UICONTROL choice]** in **[!UICONTROL no]** geändert wurde.

<!--The opt-out URL is resolved upon each recipient receiving the message. It is then personalized with the relevant encrypted parameters (profile ID, profile name, journey ID, sandbox ID, and message execution ID).-->

## Ausschluss-API-Aufruf {#opt-out-api}

Nachdem der Empfänger sich durch Klicken auf den Link zum Abmelden abgemeldet hat, wird eine Adoben I/O-API <!--Consent service API to capture the encrypted data and-->aufgerufen, um die Voreinstellung des entsprechenden Profils zu aktualisieren.

Dieser Aufruf zur POST der Adobe I/O lautet wie folgt:

Endpunkt: cjm.adobe.io/imp/consent/preferences

Abfrage:
* **params**: enthält die verschlüsselte Nutzlast
* **sig**: signature  <!--which signature?-->
* **pid**: verschlüsselte Profil-ID

Diese Parameter sind über den Link zum Abmelden verfügbar, der an Ihren Empfänger gesendet wird, d. h. die URL, über die Ihre Landingpage eines Drittanbieters für einen bestimmten Empfänger geöffnet wird:

![](assets/opt-out-parameters.png)

<!--QUESTION: How do you get the URL built for each recipient? Do you have to wait until each targeted recipient receives the unsubscribe link or can you deduce it in advance? Is it done automatically upon the API call or do you have to do something manually for each profile? In other words will the LP automatically include the 3 parameters or do you have to insert something manually? Still not completely clear-->

Kopfzeilenanforderungen:
* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* Autorisierung (Benutzertoken aus Ihrem technischen Konto) <!--How do you find this information? And other header elements?-->

Anforderungsgremium:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

<!--The Consent service /-->Adobe Customer Management will <!--decrypt and-->use these parameters to update the corresponding profile's choice. <!--and provide an answer back to the landing page.-->

## Push-Abmeldeverwaltung {#push-opt-out-management}

Push-Empfänger können sich über ihre Geräte selbst abmelden.

Beispielsweise können sie beim Herunterladen oder bei der Verwendung Ihrer App festlegen, dass Benachrichtigungen angehalten werden. Ebenso können sie die Benachrichtigungseinstellungen über das mobile Betriebssystem ändern.
