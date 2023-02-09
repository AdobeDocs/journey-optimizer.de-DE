---
solution: Journey Optimizer
product: journey optimizer
title: Opt-out-Verwaltung für E-Mails
description: Erfahren Sie, wie man Opt-outs per E-Mails verwaltet
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Opt-out, E-Mail, Link, Abo stornieren
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 100%

---

# Opt-out-Verwaltung für E-Mails {#email-opt-out}

Um Empfängern die Möglichkeit zu geben, sich vom Erhalt von E-Mail-Nachrichten abzumelden, muss jede E-Mail, die an Empfänger gesendet wird, einen **Abmelde-Link** enthalten. [Weitere Informationen zu Datenschutz und Opt-out-Verwaltung](../privacy/opt-out.md)

Dafür haben Sie folgende Möglichkeiten:

* Fügen Sie einen **Link zu einer externen Landingpage** in eine E-Mail ein, damit sich Benutzende vom Erhalt von Nachrichten von Ihrer Marke abmelden können. [Erfahren Sie, wie man einen externen Ausschluss-Link hinzufügt](#opt-out-external-lp)

* Fügen Sie in Ihren E-Mail-Inhalt einen **Link zum Abmelden mit einem Klick** ein. Dieser Link ermöglicht es Ihren Empfängern, sich schnell von Ihren Mitteilungen abzumelden, ohne erst auf eine Landingpage umgeleitet zu werden, auf der sie ihre Wahl bestätigen müssen, was den Abmeldeprozess beschleunigt. [Erfahren Sie, wie man einen Link zum Abmelden mit einem Klick hinzufügt](#one-click-opt-out)

Wenn die Option **[!UICONTROL Listen-Abonnement kündigen]** auf der Ebene der Kanaloberfläche aktiviert ist, sollten die entsprechenden E-Mails, die mit Journey Optimizer gesendet werden, außerdem einen Abmelde-Link in der E-Mail-Kopfzeile enthalten. [Weitere Informationen zum Opt-out in der E-Mail-Kopfzeile](#unsubscribe-header)

>[!NOTE]
>
>E-Mail-Nachrichten vom Typ Marketing müssen einen Ausschluss-Link enthalten, während dies für Transaktionsnachrichten nicht erforderlich ist. Die Kategorie der Nachricht (**[!UICONTROL Marketing]** oder **[!UICONTROL Transaktion]**) wird auf Ebene der [Kanaloberfläche](../configuration/channel-surfaces.md#email-type) (d. h. Nachrichtenvoreinstellung) und bei der Erstellung der Nachricht definiert).

## Externes Opt-out {#opt-out-external-lp}

### Hinzufügen eines Abmelde-Links {#add-unsubscribe-link}

Zunächst müssen Sie einen Abmelde-Link zu einer Nachricht hinzufügen. Gehen Sie dazu wie folgt vor:

1. Erstellen Sie Ihre eigene Abmeldungs-Landingpage.

1. Hosten Sie sie auf einem Drittanbietersystem Ihrer Wahl.

1. Erstellen Sie eine Nachricht in einer Journey.

1. Wählen Sie Text in Ihrem Inhalt aus und fügen Sie mithilfe der kontextuellen Symbolleiste einen [Link ein](../email/message-tracking.md#insert-links).

   ![](assets/opt-out-insert-link.png)

1. Wählen Sie **[!UICONTROL Externes Opt-out/Abmeldung]** aus der Dropdown-Liste **[!UICONTROL Link-Typ]**.

   ![](assets/opt-out-link-type.png)

1. Fügen Sie im Feld **[!UICONTROL Link]** den Link zu der Landingpage eines Drittanbieters ein.

   ![](assets/opt-out-link-url.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

### Implementieren eines API-Aufrufs zum Opt-out {#opt-out-api}

Damit Ihre Empfangenden abgemeldet werden, wenn sie ihre Auswahl über die Landingpage senden, müssen Sie einen **Abonnement-API-Aufruf** über [Adobe Developer](https://developer.adobe.com/){target="_blank"} implementieren, um die Voreinstellungen der entsprechenden Profile zu aktualisieren.

Dieser POST-Aufruf sieht wie folgt aus:

Endpunkt: platform.adobe.io/journey/imp/consent/preferences

Abfrageparameter:

* **params**: enthält die verschlüsselte Payload
* **sig**: Signatur
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

[!DNL Journey Optimizer] verwendet diese Parameter, um die Auswahl des entsprechenden Profils über den API-Aufruf von [Adobe Developer](https://developer.adobe.com){target="_blank"} zu aktualisieren

### Senden der Nachricht mit Abmelde-Link {#send-message-unsubscribe-link}

Nachdem Sie den Abmelde-Link für Ihre Landingpage konfiguriert und den API-Aufruf implementiert haben, kann Ihre Nachricht gesendet werden.

1. Senden Sie die Nachricht mit dem Link über eine [Journey](../building-journeys/journey.md).

1. Wenn der Empfänger nach Erhalt der Nachricht auf den Abmelde-Link klickt, wird die Landingpage angezeigt.

   ![](assets/opt-out-lp-example.png)

1. Wenn der Empfänger das Formular abschickt (in diesem Fall durch Klicken auf die Schaltfläche **Abmelden** auf Ihrer Landingpage), werden die Profildaten durch den [API-Aufruf](#opt-out-api) aktualisiert.

1. Der abgemeldete Empfänger wird dann zu einem Bestätigungsbildschirm weitergeleitet, der die erfolgte Abmeldung bestätigt.

   ![](assets/opt-out-confirmation-example.png)

   Ab sofort erhält dieser Benutzer keine weitere Kommunikation von Ihrer Marke, es sei denn, er meldet sich erneut an.

1. Um sich zu vergewissern, dass die Aktualisierung des betreffenden Profils erfolgt ist, öffnen Sie das Profil in Adobe Experience Platform, indem Sie einen Identity-Namespace und einen entsprechenden Identitätswert auswählen. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=de#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   Auf der Registerkarte **[!UICONTROL Attribute]** sehen Sie, dass der Wert für **[!UICONTROL choice]** auf **[!UICONTROL no]** geändert wurde.

## Opt-out mit einem Klick {#one-click-opt-out}

Gehen Sie wie folgt vor, um einen Opt-out-Link zu Ihrer E-Mail hinzuzufügen.

1. [Fügen Sie einen Link ein](../email/message-tracking.md#insert-links) und wählen Sie als Link-Typ **[!UICONTROL Ausschluss mit einem Klick]**.

   ![](assets/message-tracking-opt-out.png)

1. Wählen Sie aus, wie Sie die Abmeldung anwenden möchten: auf Kanal-, Identitäts- oder Abonnementebene.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Kanal]**: Die Abmeldung gilt für künftige Nachrichten, die im aktuellen Kanal an das Ziel des Profils (d. h. die E-Mail-Adresse) gesendet werden. Wenn einem Profil mehrere Ziele zugeordnet sind, gilt die Abmeldung für alle Ziele (d. h. E-Mail-Adressen) im Profil für diesen Kanal.
   * **[!UICONTROL Identität]**: Die Abmeldung gilt für künftige Nachrichten, die an das Ziel (d. h. die E-Mail-Adresse) gesendet werden, das für die aktuelle Nachricht verwendet wird.
   * **[!UICONTROL Abonnement]**: Die Abmeldung gilt für künftige Nachrichten, die mit einer bestimmten Abonnentenliste verbunden sind. Diese Option kann nur ausgewählt werden, wenn die aktuelle Nachricht einer Abonnement-Liste zugeordnet ist.

1. Geben Sie die URL der Landingpage ein, zu der der Benutzer weitergeleitet werden soll, sobald er sich abgemeldet hat. Diese Seite dient nur zur Bestätigung, dass die Abmeldung erfolgreich war.

   >[!NOTE]
   >
   >Wenn Sie die Option zum **Abmelden von einer Liste** auf der Ebene der Kanaloberfläche aktiviert haben, wird diese URL auch verwendet, wenn jemand auf den Abmelde-Link in der E-Mail-Kopfzeile klickt. [Weitere Informationen](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Sie können Ihre Links personalisieren. Weitere Informationen zu personalisierten URLs finden Sie in [diesem Abschnitt](../personalization/personalization-syntax.md).

1. Speichern Sie Ihre Änderungen.

Wenn Ihre Nachricht über eine [Journey](../building-journeys/journey.md) gesendet wurde, wird ein Empfänger, der auf den Abmelde-Link klickt, sofort abgemeldet.

## Abmelde-Link in der Kopfzeile einer E-Mail {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Hinzufügen eines Abmelde-Links zur E-Mail-Kopfzeile"
>abstract="Aktivieren Sie „Abmelden von einer Liste“, um einen Abmelde-Link zur E-Mail-Kopfzeile hinzuzufügen. Um eine Abmelde-URL einzurichten, fügen Sie einen 1-Klick-Ausschluss-Link in den Inhalt der E-Mail ein."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=de#one-click-opt-out" text="Opt-out mit einem Klick"

Wenn die Option zum [Abmelden von einer Liste](../configuration/channel-surfaces.md#list-unsubscribe) auf der Ebene der Kanaloberfläche aktiviert ist, enthalten die entsprechenden E-Mails, die mit [!DNL Journey Optimizer] gesendet werden, einen Abmelde-Link in der Kopfzeile.

Der Abmelde-Link wird beispielsweise in Gmail wie folgt angezeigt:

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Um den Abmelde-Link in der E-Mail-Kopfzeile anzuzeigen, muss der E-Mail-Client der Empfänger diese Funktion unterstützen.

Die Abmelde-Adresse ist die Standardadresse **[!UICONTROL Mailto (unsubscribe)]**, die in der entsprechenden Kanaloberfläche angezeigt wird. [Weitere Informationen](../configuration/channel-surfaces.md#list-unsubscribe).

Um eine personalisierte Abmelde-URL einzurichten, fügen Sie einen 1-Klick-Abmelde-Link in den Inhalt der E-Mail-Nachricht ein und geben Sie die gewünschte URL ein. [Weitere Informationen](#one-click-opt-out)

Je nach E-Mail-Client hat das Klicken auf den Abmelde-Link in der Kopfzeile eine der folgenden Auswirkungen:

* Die Abmelde-Anfrage wird an die Standard-Abmeldeadresse gesendet.

* Der Empfänger wird an die Landingpage-URL weitergeleitet, die Sie beim Hinzufügen des Abmelde-Links zu Ihrer Nachricht angegeben haben.

   >[!NOTE]
   >
   >Wenn Sie keinen 1-Klick-Abmelde-Link in Ihren Nachrichteninhalt einfügen, wird keine Landingpage angezeigt.

* Das entsprechende Profil wird sofort abgemeldet und in Experience Platform aktualisiert. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=de#getting-started){target="_blank"}.
