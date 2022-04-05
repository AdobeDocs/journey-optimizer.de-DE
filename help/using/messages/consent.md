---
title: Verwalten von Opt-out
description: Erfahren Sie, wie Sie Opt-out- und Datenschutzeinstellungen verwalten können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 74%

---

# Einverständnisverwaltung {#consent}

Verwenden Sie [!DNL Journey Optimizer], um das Einverständnis Ihrer Empfänger zur Kommunikation zu erfassen und anhand ihrer Voreinstellungs- und Abonnement-Verwaltung zu ermitteln, wie sie mit Ihrer Marke interagieren möchten.

Gesetzliche Bestimmungen wie die DSGVO verlangen die Erfüllung bestimmter Anforderungen, bevor Sie Informationen von betroffenen Personen verwenden können. Darüber hinaus sollten die betroffenen Personen ihre Einwilligung jederzeit ändern können.

**Warum ist das wichtig?**

* Die Nichtbeachtung dieser Vorschriften birgt rechtliche Risiken für Ihre Marke.
* Auf diese Weise vermeiden Sie das Verschicken unerwünschter Nachrichten an Empfänger, die Ihre Nachrichten als Spam kennzeichnen und Ihrem Ruf schaden könnten.

Weitere Informationen zur Verwaltung der Datenschutzeinstellungen und den geltenden Vorschriften finden Sie in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de){target=&quot;_blank&quot;}.

>[!NOTE]
>
>In [!DNL Journey Optimizer] wird das Einverständnis durch das [Einverständnisschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=de){target=&quot;_blank&quot;} von Experience Platform gehandhabt. Standardmäßig ist der Wert für das Einverständnisfeld leer und gilt als Einverständnis für den Empfang Ihrer Nachrichten. Sie können diesen Standardwert beim Onboarding in einen der möglichen [hier](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=de#choice-values){target=&quot;_blank&quot;} aufgelisteten Werte ändern.

## Opt-out-Verwaltung für E-Mails {#opt-out-management}

Die Möglichkeit für Empfänger, den Empfang von Mitteilungen einer Marke zu kündigen, ist eine gesetzliche Anforderung. Weitere Informationen zu den geltenden Rechtsvorschriften finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=de){target=&quot;_blank&quot;}.

Aus diesem Grund müssen Sie in jeder E-Mail, die an Empfänger gesendet wird, immer einen **Link zur Abmeldung** einfügen:

* Wenn der Empfänger auf diesen Link klickt, wird er auf eine Landingpage weitergeleitet, auf der er die Abmeldung bestätigen muss.
* Nachdem er seine Entscheidung bestätigt hat, werden die Daten des Profils mit dieser Information aktualisiert.

>[!NOTE]
>
>E-Mail-Nachrichten vom Typ Marketing müssen einen Ausschluss-Link enthalten, der für Transaktionsnachrichten nicht erforderlich ist. Die Kategorie der Nachricht (**[!UICONTROL Marketing]** oder **[!UICONTROL Transactional]**) definiert wird unter [Meldungsvoreinstellungsebene](../configuration/message-presets.md#email-type) und wann [Nachricht erstellen](get-started-content.md#create-new-message).

### Externes Opt-out {#opt-out-external-lp}

Hierfür können Sie einen Link zu einer externen Landingpage in eine E-Mail einfügen, damit sich Benutzer vom Erhalt von Nachrichten Ihrer Marke abmelden können.

#### Hinzufügen eines Abmelde-Links {#add-unsubscribe-link}

Zunächst müssen Sie einen Abmelde-Link zu einer Nachricht hinzufügen. Gehen Sie dazu wie folgt vor:

1. Erstellen Sie Ihre eigene Abmeldungs-Landingpage.

1. Hosten Sie sie auf einem Drittanbietersystem Ihrer Wahl.

1. [Erstellen Sie eine Nachricht](get-started-content.md) in [!DNL Journey Optimizer].

1. Wählen Sie Text in Ihrem Inhalt aus und [fügen](../design/message-tracking.md#insert-links) Sie mithilfe der kontextbezogenen Symbolleiste einen Link ein.

   ![](assets/opt-out-insert-link.png)

1. Wählen Sie **[!UICONTROL Externes Opt-out/Abmeldung]** aus der Dropdown-Liste **[!UICONTROL Link-Typ]**.

   ![](assets/opt-out-link-type.png)

1. Fügen Sie im Feld **[!UICONTROL Link]** den Link zu der Landingpage eines Drittanbieters ein.

   ![](assets/opt-out-link-url.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

1. Speichern Sie den Inhalt und [veröffentlichen Sie Ihre Nachricht](publish-manage-message.md).

#### Implementieren eines API-Aufrufs zum Opt-out {#opt-out-api}

Damit sich Ihre Empfänger bei der Auswahl über die Landingpage abmelden können, müssen Sie eine **Abonnement-API-Aufruf** bis [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;}, um die Voreinstellungen der entsprechenden Profile zu aktualisieren.

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

[!DNL Journey Optimizer] verwendet diese Parameter, um die Auswahl des entsprechenden Profils über die [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;} API-Aufruf.

#### Senden der Nachricht mit Abmelde-Link {#send-message-unsubscribe-link}

Nachdem Sie den Abmelde-Link für Ihre Landingpage konfiguriert und den API-Aufruf implementiert haben, kann Ihre Nachricht gesendet werden.

1. Senden Sie die Nachricht mit dem Link über eine [Journey](../building-journeys/journey.md).

1. Wenn der Empfänger nach Erhalt der Nachricht auf den Abmelde-Link klickt, wird die Landingpage angezeigt.

   ![](assets/opt-out-lp-example.png)

1. Wenn der Empfänger das Formular sendet (hier durch Drücken der **Abmelden** -Schaltfläche in Ihrer Landingpage) werden die Profildaten über die [API-Aufruf](#opt-out-api).

1. Der abgemeldete Empfänger wird dann zu einem Bestätigungsbildschirm weitergeleitet, der die erfolgte Abmeldung bestätigt.

   ![](assets/opt-out-confirmation-example.png)

   Ab sofort erhält dieser Benutzer keine weitere Kommunikation von Ihrer Marke, es sei denn, er meldet sich erneut an.

1. Um sich zu vergewissern, dass die Aktualisierung des betreffenden Profils erfolgt ist, öffnen Sie das Profil in Adobe Experience Platform, indem Sie einen Identity-Namespace und einen entsprechenden Identitätswert auswählen. Weitere Informationen finden Sie in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=de#getting-started){target=&quot;_blank&quot;}.

   ![](assets/opt-out-profile-choice.png)

   Auf der Registerkarte **[!UICONTROL Attribute]** sehen Sie, dass der Wert für **[!UICONTROL choice]** auf **[!UICONTROL no]** geändert wurde.

### Opt-out mit einem Klick {#one-click-opt-out}

Da sich viele Kunden einen einfachen Abmeldevorgang wünschen, können Sie auch einen Opt-out-Link mit einem Klick in Ihren E-Mail-Inhalt einfügen. Dieser Link ermöglicht es Ihren Empfängern, sich schnell von Ihren Mitteilungen abzumelden, ohne erst auf eine Landingpage umgeleitet zu werden, auf der sie ihre Wahl bestätigen müssen, was den Abmeldeprozess beschleunigt.

Gehen Sie wie folgt vor, um einen Opt-out-Link zu Ihrer E-Mail hinzuzufügen.

1. [Fügen Sie einen Link ein](../design/message-tracking.md#insert-links) und wählen Sie als Link-Typ **[!UICONTROL Ausschluss mit einem Klick]**.

   ![](assets/message-tracking-opt-out.png)

1. Wählen Sie aus, wie Sie die Abmeldung anwenden möchten: auf Kanal-, Identitäts- oder Abonnementebene.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Kanal]**: Die Abmeldung gilt für künftige Nachrichten, die im aktuellen Kanal an das Ziel des Profils (d. h. die E-Mail-Adresse) gesendet werden. Wenn einem Profil mehrere Ziele zugeordnet sind, gilt die Abmeldung für alle Ziele (d. h. E-Mail-Adressen) im Profil für diesen Kanal.
   * **[!UICONTROL Identität]**: Die Abmeldung gilt für künftige Nachrichten, die an das Ziel (d. h. die E-Mail-Adresse) gesendet werden, das für die aktuelle Nachricht verwendet wird.
   * **[!UICONTROL Abonnement]**: Die Abmeldung gilt für künftige Nachrichten, die mit einer bestimmten Abonnentenliste verbunden sind. Diese Option kann nur ausgewählt werden, wenn die aktuelle Nachricht einer Abonnement-Liste zugeordnet ist.

1. Geben Sie die URL der Landingpage ein, zu der der Benutzer weitergeleitet werden soll, sobald er sich abgemeldet hat. Diese Seite dient nur zur Bestätigung, dass die Abmeldung erfolgreich war.

   >[!NOTE]
   >
   >Wenn Sie die **List-Unsubscribe** auf der Ebene der Nachrichtenvorgabe verwenden, wird diese URL auch verwendet, wenn Benutzer auf den Link zum Abmelden im E-Mail-Header klicken. [Weitere Informationen](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Sie können Ihre Links personalisieren. Weitere Informationen zu personalisierten URLs finden Sie in [diesem Abschnitt](../personalization/personalization-syntax.md).

1. Speichern Sie Ihre Änderungen.

Wenn Ihre Nachricht über eine [Journey](../building-journeys/journey.md) gesendet wurde, wird ein Empfänger, der auf den Abmelde-Link klickt, sofort abgemeldet.

### Abmelde-Link in der Kopfzeile einer Nachricht {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Abmelde-Link zum E-Mail-Header hinzufügen"
>abstract="Aktivieren Sie List-Unsubscribe , um einen Abmelde-Link zum E-Mail-Header hinzuzufügen. Um eine Abmelde-URL festzulegen, fügen Sie einen 1-Klick-Ausschluss-Link in den Inhalt der E-Mail-Nachricht ein."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/consent.html?lang=en#one-click-opt-out" text="Opt-out mit einem Klick"

Wenn die Variable [List-Unsubscribe-Option](../configuration/message-presets.md#list-unsubscribe) auf der Ebene der Nachrichtenvorgabe aktiviert ist, werden die entsprechenden E-Mails mit [!DNL Journey Optimizer] enthält einen Abmelde-Link in den E-Mail-Header.

Der Abmelde-Link wird beispielsweise in Gmail wie folgt angezeigt:

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Um den Abmelde-Link im E-Mail-Header anzuzeigen, muss der E-Mail-Client der Empfänger diese Funktion unterstützen.

Die Abmelde-Adresse ist die Standardeinstellung. **[!UICONTROL Mailto (unsubscribe)]** -Adresse, die in der entsprechenden Nachrichtenvorgabe angezeigt wird. [Weitere Informationen](../configuration/message-presets.md#list-unsubscribe).

Um eine personalisierte Abmelde-URL festzulegen, fügen Sie einen 1-Klick-Abmelde-Link in den Inhalt der E-Mail-Nachricht ein und geben Sie die URL Ihrer Wahl ein. [Weitere Informationen](#one-click-opt-out)

Je nach E-Mail-Client können die folgenden Auswirkungen auftreten, wenn Sie in der Kopfzeile auf den Abmelde-Link klicken:

* Die Abmelde-Anfrage wird an die Standard-Abmelde-Adresse gesendet.

* Der Empfänger wird an die Landingpage-URL weitergeleitet, die Sie beim Hinzufügen des Ausschluss-Links zu Ihrer Nachricht angegeben haben.

   >[!NOTE]
   >
   >Wenn Sie keinen Ausschluss-Link mit einem Klick in Ihren Nachrichteninhalt einfügen, wird keine Landingpage angezeigt.

* Das entsprechende Profil wird sofort abgemeldet und in Experience Platform aktualisiert. Weitere Informationen finden Sie in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

## Push-Opt-out-Verwaltung {#push-opt-out-management}

Push-Empfänger können sich über ihre Geräte selbst abmelden.

Beispielsweise können sie den Versand von Benachrichtigungen beim Herunterladen oder bei der Nutzung Ihrer Mobile App deaktivieren. Ebenso können sie die Benachrichtigungseinstellungen über das mobile Betriebssystem ändern.
