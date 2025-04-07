---
solution: Journey Optimizer
product: journey optimizer
title: Opt-out-Verwaltung für E-Mails
description: Erfahren Sie, wie man Opt-outs per E-Mails verwaltet
feature: Email Design, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: Opt-out, E-Mail, Link, Abo stornieren
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 84%

---

# Opt-out-Verwaltung für E-Mails {#email-opt-out}

Beim Versand von Nachrichten von Journeys oder Kampagnen müssen Sie stets sicherstellen, dass sich Kundinnen und Kunden von der künftigen Kommunikation abmelden können.  Nach der Abmeldung werden die Profile automatisch aus der Zielgruppe künftiger Marketing-Nachrichten entfernt.   [Erfahren Sie mehr über Datenschutz und Opt-out-Verwaltung](../privacy/opt-out.md)

>[!NOTE]
>
>Alle Ihre Nachrichten vom Typ Marketing müssen einen Ausschluss-Link enthalten.  Dies ist für Transaktionsnachrichten nicht erforderlich. Die Kategorie der Nachricht (**[!UICONTROL Marketing]** oder **[!UICONTROL Transaktion]**) wird auf Ebene der [Kanalkonfiguration](../configuration/channel-surfaces.md#email-type) und bei der Erstellung der Nachricht definiert.

Um einen Abmelde-Link in Ihren E-Mail-Inhalt einzufügen, haben Sie folgende Möglichkeiten:

* Hinzufügen einer URL zum Abmelden mit einem Klick in der Kopfzeile der E-Mail  Durch Aktivieren der Option **[!UICONTROL Abmelden von der Liste aktivieren]** auf der Ebene der Kanalkonfiguration wird ein Ausschluss-Link in der Kopfzeile der E-Mail hinzugefügt. [Weitere Informationen zum Opt-out finden Sie in der E-Mail-Kopfzeile](#unsubscribe-header)

* Aktivieren Sie den **Ausschluss-Link mit einem Klick** für Ihre E-Mail.  [Informationen dazu, wie man einen Link zum Abmelden mit einem Klick hinzufügt](#one-click-opt-out)

* Fügen Sie einen **Link in eine Landingpage** ein.  [Informationen dazu, wie Sie eine Landingpage zum Abmelden hinzufügen](#opt-out-external-lp)

Wenn ein Empfänger auf den Abmelde-Link klickt, wird seine Abmeldeanfrage entsprechend verarbeitet.

Um sich zu vergewissern, dass die Aktualisierung des entsprechenden Profils erfolgt ist, navigieren Sie zu Experience Platform und [zu diesem Profil](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide#attributes-tab). Auf der Registerkarte **[!UICONTROL Attribute]** sehen Sie, dass der Wert für **[!UICONTROL choice]** auf **[!UICONTROL no]** geändert wurde. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide#browse-identity){target="_blank"}.

![](assets/opt-out-profile-choice.png)

>[!NOTE]
>
>Gelegentlich kann es aufgrund der nachgelagerten Datenverarbeitung länger dauern, bis Ereignisse abgemeldet werden. Warten Sie etwas, bis das System aktualisiert wurde.

## Ausschluss in einem Schritt {#opt-out-one-step}

Mit [!DNL Adobe Journey Optimizer] können Sie Ihre [E-Mail-Konfigurationseinstellungen](email-settings.md#list-unsubscribe) mit einer automatisch generierten URL zum Abmelden mit einem Klick und der Mailto-Adresse in der E-Mail-Kopfzeile konfigurieren oder eine Ein-Klick-Abmelde-URL in Ihren E-Mail-Textkörper einfügen.

### URL zum Abmelden mit einem Klick in der E-Mail-Kopfzeile {#unsubscribe-header}

Die Abmelde-URL mit einem Klick ist ein Abmelde-Link oder eine Schaltfläche neben den E-Mail-Absenderinformationen, über den bzw. die Empfänger Ihre Mailing-Listen sofort mit einem einzigen Klick abmelden können. In diesem Abschnitt erfahren Sie **[!UICONTROL wie Sie die Option]** Abmelden von einer Liste[ verwalten](list-unsubscribe.md).

### Abmelden mit einem Klick über den E-Mail-Inhalt {#one-click-opt-out}

Um eine personalisierte Abmelde-URL einzurichten, fügen Sie einen Link zum Abmelden mit einem Klick in den Inhalt der E-Mail-Nachricht ein und geben Sie die gewünschte URL wie unten beschrieben ein:

1. Greifen Sie auf Ihren E-Mail-Inhalt zu und [fügen Sie einen Link ein](../email/message-tracking.md#insert-links).
1. Wählen Sie **[!UICONTROL Opt-out mit einem Klick]** als Link-Typ aus.

   ![](assets/message-tracking-opt-out.png)

1. Geben Sie die URL der Landingpage ein, zu der Benutzende weitergeleitet werden sollen, sobald sie sich abgemeldet haben.  Diese Seite dient nur Bestätigung, dass die Abmeldung erfolgreich war.

   >[!NOTE]
   >
   >Wenn Sie die Option **[!UICONTROL Von der Liste abmelden]** auf [Ebene der Kanalkonfiguration](email-settings.md#list-unsubscribe) aktiviert und die standardmäßige **[!UICONTROL URL zum Abmelden mit einem Klick]** deaktiviert haben, wird diese Landingpage ebenfalls verwendet, wenn Benutzende in der Kopfzeile der E-Mail auf den Abmelde-Link klicken. [Weitere Informationen](list-unsubscribe.md)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Sie können Ihre Links personalisieren. Weitere Informationen zu personalisierten URLs finden Sie [ (diesem Abschnitt](../personalization/personalization-syntax.md).

1. Wählen Sie aus, wie Sie die Abmeldung anwenden möchten: auf Kanal- oder Identitätsebene.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Kanal]**: Die Abmeldung gilt für künftige Nachrichten, die im aktuellen Kanal an das Ziel des Profils (d. h. die E-Mail-Adresse) gesendet werden. Wenn einem Profil mehrere Ziele zugeordnet sind, gilt die Abmeldung für alle Ziele (d. h. E-Mail-Adressen) im Profil für diesen Kanal.
   * **[!UICONTROL Identität]**: Die Abmeldung gilt für künftige Nachrichten, die an das Ziel (d. h. die E-Mail-Adresse) gesendet werden, das für die aktuelle Nachricht verwendet wird.
     <!--* **[!UICONTROL Subscription]**: The opt-out applies to future messages associated with a specific subscription list. This option can only be selected if the current message is associated with a subscription list.-->

1. Speichern Sie Ihre Änderungen.


## Opt-out in zwei Schritten {#opt-out-external-lp}

Der standardmäßige Opt-out-Mechanismus besteht aus zwei Schritten: Die Abonnentin oder der Abonnent klickt in einer E-Mail auf den Abmelde-Link und wird dann zu einer Opt-out-Landingpage weitergeleitet, um ihre bzw. seine Abmeldung zu bestätigen.

Um diesen Abmeldemodus zu implementieren, müssen Sie eine Opt-out-Landingpage erstellen und veröffentlichen sowie einen Abmelde-Link in Ihren E-Mail-Nachrichten mit einem Link zur Landingpage hinzufügen. Diese Schritte werden nachfolgend beschrieben. 


### Voraussetzungen {#prereq-lp}

Um einen zweischrittigen Opt-out-Mechanismus einzurichten, müssen Sie eigene Abmelde-Landingpages erstellen. Die erste Landingpage wird in Ihrer Nachricht verlinkt und muss eine Aktionsaufruf-Schaltfläche enthalten.  Wenn Benutzende auf die Schaltfläche klicken, sollte eine Bestätigungsmeldung angezeigt werden.

Erfahren Sie auf dieser Seite, wie Sie in Adobe Journey Optimizer eine Landingpage erstellen, um Abmeldungen [ verwalten](../landing-pages/lp-use-cases.md#opt-out).

Sie können auch eine externe Landingpage verwenden. Konfigurieren Sie in diesem Fall die API so, dass die Informationen an Adobe Journey Optimizer gesendet werden, wenn sich eine Empfängerin oder ein Empfänger abgemeldet hat.

+++ Erfahren Sie, wie Sie einen Opt-out-API-Aufruf implementieren

Damit Ihre Empfangenden abgemeldet werden, wenn sie ihre Auswahl über die Landingpage senden, müssen Sie einen **Abonnement-API-Aufruf** über [Adobe Developer](https://developer.adobe.com){target="_blank"} implementieren, um die Voreinstellungen der entsprechenden Profile zu aktualisieren.

Dieser POST-Aufruf sieht wie folgt aus:

Endpunkt: https://platform.adobe.io/journey/imp/consent/preferences

Abfrageparameter:

* **params**: enthält die verschlüsselte Payload
* **pid**: verschlüsselte Profil-ID

Diese beiden Parameter werden in die URL der Drittanbieter-Landingpage eingefügt, die an Ihre Empfängerin oder Ihren Empfänger gesendet wird:

![](assets/opt-out-parameters.png)

Header-Anforderungen:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* Autorisierung (Benutzer-Token Ihres technischen Kontos)

Hauptteil der Anfrage:

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

[!DNL Journey Optimizer] verwendet diese Parameter, um die Auswahl des entsprechenden Profils über den [Adobe Developer](https://developer.adobe.com){target="_blank"}-API-Aufruf zu aktualisieren

+++


### Hinzufügen eines Abmelde-Links {#add-unsubscribe-link}

Zunächst müssen Sie einen Abmelde-Link zu einer Nachricht hinzufügen. Gehen Sie dazu wie folgt vor:

1. Verwenden Sie die kontextbezogene Symbolleiste, um eine Nachricht zu erstellen und einen [Link einzufügen](../email/message-tracking.md#insert-links).

   ![](assets/opt-out-insert-link.png)

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Typ]** die Option **[!UICONTROL Landingpage]** aus und legen Sie Ihre Opt-out-Landingpage im Feld **[!UICONTROL Landingpage]** fest.

   Wenn Sie eine externe Landingpage verwenden, wählen Sie aus der Dropdown-Liste **[!UICONTROL Typ]** die Option **[!UICONTROL Externes Opt-out/Abmeldung]** aus.

   ![](assets/opt-out-link-type.png)

   Fügen Sie im Feld **[!UICONTROL Link]** den Link zu der Landingpage eines Drittanbieters ein.

   ![](assets/opt-out-link-url.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.


### Senden der Nachricht mit Abmelde-Link {#send-message-unsubscribe-link}

Nachdem Sie den Abmelde-Link für Ihre Landingpage konfiguriert haben, können Sie Ihre Nachricht erstellen und senden.

1. Konfigurieren Sie Ihre Nachricht mit einem Abmelde-Link und senden Sie sie an Ihre Abonnentinnen und Abonnenten.

1. Wenn die Empfängerin bzw. der Empfänger nach Erhalt der Nachricht auf den Abmelde-Link klickt, wird die Landingpage angezeigt.

   ![](assets/opt-out-lp-example.png)

1. Wenn die Person das Formular abschickt (in diesem Fall durch Klicken auf die Schaltfläche **[!UICONTROL Abmelden]** auf Ihrer Landingpage), werden die Profildaten durch den API-Aufruf aktualisiert.

1. Der abgemeldete Empfänger wird dann zu einem Bestätigungsbildschirm weitergeleitet, der die erfolgte Abmeldung bestätigt.

   ![](assets/opt-out-confirmation-example.png)

   Ab sofort erhält dieser Benutzer keine weitere Kommunikation von Ihrer Marke, es sei denn, er meldet sich erneut an.

