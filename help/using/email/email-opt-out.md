---
solution: Journey Optimizer
product: journey optimizer
title: Opt-out-Verwaltung für E-Mails
description: Erfahren Sie, wie man Opt-outs per E-Mails verwaltet
feature: Email Design, Privacy
topic: Content Management
role: User
level: Intermediate
keywords: Opt-out, E-Mail, Link, Abo stornieren
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: fb6a2e29f92e4b7e65eb495a654960e3249f9508
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 32%

---

# Opt-out-Verwaltung für E-Mails {#email-opt-out}

Beim Versand von Nachrichten von Journeys oder Kampagnen müssen Sie stets sicherstellen, dass sich Kunden von der künftigen Kommunikation abmelden können. Nach der Abmeldung werden die Profile automatisch aus der Audience künftiger Marketing-Nachrichten entfernt.  [Erfahren Sie mehr über Datenschutz und Opt-out-Verwaltung](../privacy/opt-out.md)

>[!NOTE]
>
>Alle Ihre Marketing-Nachrichten müssen einen Ausschluss-Link enthalten. Dies ist für Transaktionsnachrichten nicht erforderlich. Die Nachrichtenkategorie - **[!UICONTROL Marketing]** oder **[!UICONTROL Transactional]** - definiert wird im [Kanaloberfläche](../configuration/channel-surfaces.md#email-type) und beim Erstellen der Nachricht.

Um einen Abmelde-Link in Ihren E-Mail-Inhalt einzufügen, haben Sie folgende Möglichkeiten:

* Fügen Sie im E-Mail-Header eine URL zum Abmelden mit einem Klick hinzu. Aktivieren der **[!UICONTROL List-Unsubscribe-Header]** -Option auf der Kanaloberfläche wird ein Ausschluss-Link im E-Mail-Header hinzugefügt. [Weitere Informationen zum Opt-out in der E-Mail-Kopfzeile](#unsubscribe-header)

* Aktivieren Sie die **Ausschluss-Link mit einem Klick** für Ihre E-Mail.  [Erfahren Sie, wie man einen Link zum Abmelden mit einem Klick hinzufügt](#one-click-opt-out)

* Einfügen einer **Link zu einer Landingpage**. [Erfahren Sie, wie Sie eine Landingpage zum Opt-out hinzufügen](#opt-out-external-lp)

## Opt-out in einem Schritt {#opt-out-one-step}

### Ein Klick auf URL abmelden im E-Mail-Header {#unsubscribe-header}

<!--Do not modify - Legal Review Done -->

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Abmelde-URL in E-Mail-Kopfzeile hinzufügen"
>abstract="Aktivieren Sie List-Unsubscribe Header , um eine Abmelde-URL in den E-Mail-Header hinzuzufügen. Um eine Abmelde-URL einzurichten, fügen Sie einen 1-Klick-Ausschluss-Link in den Inhalt der E-Mail ein."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=de#one-click-opt-out" text="Opt-out mit einem Klick"

Die URL zur Abmeldung von einer Liste mit einem Klick ist ein Abmelde-Link oder eine Schaltfläche, der bzw. die neben den Absenderinformationen der E-Mail angezeigt wird und es Empfängern ermöglicht, sich mit einem Klick von Ihren Mailinglisten abzumelden. Wenn in Adobe Journey Optimizer die Variable **List-Unsubscribe aktivieren** aktiviert ist, enthält der E-Mail-Header standardmäßig sowohl ein Mailto als auch eine URL, über die sich Empfänger von Ihrer Mailingliste abmelden können.

Die [List-Unsubscribe aktivieren](email-settings.md#list-unsubscribe) Der Umschalter muss auf der Kanaloberfläche aktiviert sein, damit E-Mails, die diese Oberfläche verwenden, die URL zum Abmelden mit einem Klick in den E-Mail-Header aufnehmen.

>[!NOTE]
>
>Um die URL zur Abmeldung von einem Klick im E-Mail-Header anzuzeigen, muss der E-Mail-Client des Empfängers diese Funktion unterstützen.


Beispielsweise zeigt die 1-Klick-URL zum Abmelden einen Abmelde-Link wie in Gmail an:

![](assets/unsubscribe-header.png)


Mit Adobe Journey Optimizer können Sie Ihre E-Mail-Oberflächeneinstellungen mit einer automatisch generierten 1-Klick-URL für die Abmeldung und die E-Mail-Adresse im E-Mail-Header konfigurieren oder eine 1-Klick-Ausschluss-URL in Ihren E-Mail-Textkörper einfügen: Wenn ein Empfänger auf den 1-Klick-Abmelde-Link klickt, wird die Abmeldeanforderung des Empfängers entsprechend verarbeitet.

>[!AVAILABILITY]
>
>Ab dem 3. Juni 2024 ist in Adobe Journey Optimizer der Header URL abmelden mit einem Klick verfügbar.
>

Je nach E-Mail-Client und [Abmeldeeinstellungen der E-Mail-Oberfläche](email-settings.md#list-unsubscribe)hat das Klicken auf den Abmelde-Link im E-Mail-Header folgende Auswirkungen:

* Wenn die Variable **Mailto (unsubscribe)** aktiviert ist, wird die Abmeldeanforderung an die Standardadresse zur Abmeldung gesendet, die auf der von Ihnen erstellten Subdomain basiert.
* Wenn die Variable **1-Klick-URL abmelden** aktiviert ist - oder wenn Sie eine Abmelde-URL in den Inhalt Ihres E-Mail-Hauptinhalts eingefügt haben -, wird der Empfänger direkt abgemeldet, entweder auf Kanalebene oder auf ID-Ebene (je nachdem, wie die Zustimmung eingerichtet wird), wenn der Empfänger auf die URL zum Abmelden mit einem Klick klickt, die auf der von Ihnen erstellten Subdomain basiert.

In beiden Fällen wird das entsprechende Empfängerprofil sofort abgemeldet und diese Auswahl im Experience Platform aktualisiert. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=de#getting-started){target="_blank"}.

Wenn Sie zum Header &quot;List Unsubscribe&quot;die Option &quot;Enable-In&quot;aktiviert haben, empfehlen wir, beide Funktionen zu aktivieren - Mailto und One-Click&amp;Unsubscribe-URL. Nicht alle E-Mail-Clients unterstützen die HTTP-Methode. Mit der Mailto-List-Unsubscribe-Funktion, die Ihnen als Alternative zur Verfügung gestellt wird, kann Ihre Reputation als Absender besser geschützt werden und alle Empfänger haben wahrscheinlich Zugriff auf die Abmeldefunktion. [Weitere Informationen](email-settings.md#list-unsubscribe)


### Opt-out aus dem E-Mail-Inhalt mit einem Klick {#one-click-opt-out}

Um eine personalisierte Abmelde-URL festzulegen, fügen Sie einen 1-Klick-Abmelde-Link in den Inhalt der E-Mail-Nachricht ein und geben Sie die URL Ihrer Wahl ein, wie unten beschrieben:

1. Zugriff auf E-Mail-Inhalte und [Link einfügen](../email/message-tracking.md#insert-links).
1. Auswählen **[!UICONTROL Opt-out mit einem Klick]** als Typ des Links.

   ![](assets/message-tracking-opt-out.png)

1. Geben Sie die URL der Landingpage ein, auf die der Benutzer nach der Abmeldung weitergeleitet wird. Auf dieser Seite können Sie bestätigen, dass die Abmeldung erfolgreich war.

   >[!NOTE]
   >
   >Wenn Sie die **[!UICONTROL List-Unsubscribe]** -Option am [Kanaloberflächen](email-settings.md#list-unsubscribe) und lassen Sie die standardmäßige Option für die Ausschluss-URL mit einem Klick deaktiviert. Diese URL wird verwendet, wenn Benutzer auf den Link zum Abmelden im E-Mail-Header klicken. [Weitere Informationen](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Sie können Ihre Links personalisieren. Weitere Informationen zu personalisierten URLs finden Sie in [diesem Abschnitt](../personalization/personalization-syntax.md).

1. Wählen Sie aus, wie Sie die Abmeldung anwenden möchten: auf Kanal-, Identitäts- oder Abonnementebene.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Kanal]**: Die Abmeldung gilt für künftige Nachrichten, die im aktuellen Kanal an das Ziel des Profils (d. h. die E-Mail-Adresse) gesendet werden. Wenn einem Profil mehrere Ziele zugeordnet sind, gilt die Abmeldung für alle Ziele (d. h. E-Mail-Adressen) im Profil für diesen Kanal.
   * **[!UICONTROL Identität]**: Die Abmeldung gilt für künftige Nachrichten, die an das Ziel (d. h. die E-Mail-Adresse) gesendet werden, das für die aktuelle Nachricht verwendet wird.
   * **[!UICONTROL Abonnement]**: Die Abmeldung gilt für künftige Nachrichten, die mit einer bestimmten Abonnement-Liste verbunden sind. Diese Option kann nur ausgewählt werden, wenn die aktuelle Nachricht einer Abonnement-Liste zugeordnet ist.

1. Speichern Sie Ihre Änderungen.



## zweistufiger Ausschluss {#opt-out-external-lp}

Der Standard-Abmeldemechanismus besteht aus zwei Schritten: Der Abonnent klickt in einer E-Mail auf den Abmelde-Link und wird dann zu einer Opt-out-Landingpage weitergeleitet, um seine Abmeldung zu bestätigen.

Um diesen Abmeldemodus zu implementieren, müssen Sie eine Opt-out-Landingpage erstellen und veröffentlichen sowie einen Abmelde-Link in Ihren E-Mail-Nachrichten mit einem Link zur Landingpage hinzufügen. Diese Schritte werden nachfolgend beschrieben.


### Voraussetzungen {#prereq-lp}

Um einen zweistufigen Opt-out-Mechanismus einzurichten, müssen Sie eigene Abmelde-Landingpages erstellen. Die erste Landingpage wird von Ihrer Nachricht aus mit einer Aktionsaufruf-Schaltfläche verknüpft. Wenn der Benutzer auf die Schaltfläche klickt, sollte eine Bestätigungsmeldung angezeigt werden.

Erfahren Sie, wie Sie in Adobe Journey Optimizer eine Landingpage erstellen, um Abmeldungen zu verwalten in [diese Seite](../landing-pages/lp-use-cases.md#opt-out).

Sie können auch eine externe Landingpage verwenden. Konfigurieren Sie in diesem Fall die API so, dass die Informationen an Adobe Journey Optimizer gesendet werden, wenn sich ein Empfänger abgemeldet hat.

+++ Erfahren Sie, wie Sie einen Ausschluss-API-Aufruf implementieren

Damit Ihre Empfangenden abgemeldet werden, wenn sie ihre Auswahl über die Landingpage senden, müssen Sie einen **Abonnement-API-Aufruf** über [Adobe Developer](https://developer.adobe.com){target="_blank"} implementieren, um die Voreinstellungen der entsprechenden Profile zu aktualisieren.

Dieser POST-Aufruf sieht wie folgt aus:

Endpunkt: https://platform.adobe.io/journey/imp/consent/preferences

Abfrageparameter:

* **params**: enthält die verschlüsselte Payload
* **pid**: verschlüsselte Profil-ID

Diese drei Parameter werden in die URL der Drittanbieter-Landingpage eingefügt, die an Ihren Empfänger gesendet wird:

![](assets/opt-out-parameters.png)

Header-Anforderungen:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* authorization (Benutzer-Token Ihres technischen Accounts)

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

[!DNL Journey Optimizer] verwendet diese Parameter, um die Auswahl des entsprechenden Profils über die [Adobe Developer](https://developer.adobe.com){target="_blank"} API-Aufruf.

+++


### Hinzufügen eines Abmelde-Links {#add-unsubscribe-link}

Zunächst müssen Sie einen Abmelde-Link zu einer Nachricht hinzufügen. Gehen Sie dazu wie folgt vor:

1. Erstellen Sie eine Nachricht und [Link einfügen](../email/message-tracking.md#insert-links) über die dedizierte Symbolleiste.

   ![](assets/opt-out-insert-link.png)

1. Wählen Sie die **[!UICONTROL Landingpage]** aus dem **[!UICONTROL Typ]** und wählen Sie Ihre Opt-out-Landingpage im **[!UICONTROL Landingpage]** -Feld.

   Wenn Sie eine externe Landingpage verwenden, wählen Sie **[!UICONTROL Externes Opt-out/Abmeldung]** aus dem **[!UICONTROL Typ]** Dropdown-Liste.

   ![](assets/opt-out-link-type.png)

   Fügen Sie im Feld **[!UICONTROL Link]** den Link zu der Landingpage eines Drittanbieters ein.

   ![](assets/opt-out-link-url.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.


### Senden der Nachricht mit Abmelde-Link {#send-message-unsubscribe-link}

Nachdem Sie den Abmelde-Link für Ihre Landingpage konfiguriert haben, können Sie Ihre Nachricht erstellen und senden.

1. Konfigurieren Sie Ihre Nachricht mit einem Abmelde-Link und senden Sie sie an Ihre Abonnenten.

1. Wenn der Empfänger nach Erhalt der Nachricht auf den Abmelde-Link klickt, wird die Landingpage angezeigt.

   ![](assets/opt-out-lp-example.png)

1. Wenn der Empfänger das Formular sendet, klicken Sie hier auf die Schaltfläche **[!UICONTROL Abmelden]** in Ihrer Landingpage - die Profildaten werden über den API-Aufruf aktualisiert.

1. Der abgemeldete Empfänger wird dann zu einem Bestätigungsbildschirm weitergeleitet, der die erfolgte Abmeldung bestätigt.

   ![](assets/opt-out-confirmation-example.png)

   Ab sofort erhält dieser Benutzer keine weitere Kommunikation von Ihrer Marke, es sei denn, er meldet sich erneut an.

1. Um sich zu vergewissern, dass die Aktualisierung des betreffenden Profils erfolgt ist, öffnen Sie das Profil in Adobe Experience Platform, indem Sie einen Identity-Namespace und einen entsprechenden Identitätswert auswählen. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=de#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   Auf der Registerkarte **[!UICONTROL Attribute]** sehen Sie, dass der Wert für **[!UICONTROL choice]** auf **[!UICONTROL no]** geändert wurde.

