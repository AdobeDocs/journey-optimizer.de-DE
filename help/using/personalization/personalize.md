---
title: Personalisieren von Inhalten in Journey Optimizer
description: Erste Schritte bei der Personalisierung
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 7be83409f7a594747963c5b125f3bf96c0b4f8b6
workflow-type: ht
source-wordcount: '691'
ht-degree: 100%

---

# Erste Schritte bei der Personalisierung{#add-personalization}

Erkunden Sie die Personalisierungs-Funktionen von [!DNL Adobe Journey Optimizer], um Ihre Nachrichten an jeden einzelnen Empfänger anhand der vorhandenen Daten anzupassen. Dabei kann es sich z. B. um den Vornamen des Empfängers, seine Interessen, seinen Wohnort oder zuvor gekaufte Artikel handeln.

➡️ [In diesen Videos erfahren Sie, wie Sie eine Nachricht personalisieren](#video-perso)

[!DNL Journey Optimizer] verwendet eine einfache **Inline**-Personalisierungssyntax, die auf Handlebars basiert. Damit können Sie Ausdrücke mit Inhalten erstellen, die von geschweiften Klammern **{{}}** eingeschlossen sind. Sie können ohne Einschränkungen mehrere Ausdrücke in demselben Inhalt oder Feld hinzufügen. Weitere Informationen finden Sie unter [Personalisierungssyntax](personalization-syntax.md).

Die Personalisierung basiert auf den Profildaten, die von dem in Adobe Experience Platform definierten Schema **Individuelles XDM-Profil** verwaltet werden. Weitere Informationen finden Sie in der [Dokumentation zum Adobe Experience Platform-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target=&quot;_blank&quot;}.

>[!CAUTION]
>Das Schema **Individuelles XDM-Profil** ist das einzige, das Sie zum Personalisieren von Inhalten in [!DNL Journey Optimizer] verwenden können.

**Beispiele:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Bei der Verarbeitung der Nachricht (E-Mail und Push-Benachrichtigung) ersetzt Journey Optimizer den Ausdruck durch die in der Experience Cloud Platform-Datenbank enthaltenen Daten: `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wird zu „Hallo, Max Mustermann“.


## Personalisierungskontexte{#personalization-areas}

Es gibt verschiedene Möglichkeiten, um den Inhalt und die Darstellung von Nachrichten in [!DNL Journey Optimizer] zu personalisieren.

In allen Feldern mit dem Editor-Symbol können Sie den Personalisierungseditor (auch Ausdruckseditor genannt) öffnen und die Personalisierung definieren.

![](assets/perso_icon.png)

### E-Mails personalisieren

Wenn Sie eine E-Mail erstellen, können Sie im Fenster **[!UICONTROL Betreffzeile]** der Nachricht eine Personalisierung hinzufügen.

![](assets/perso_subject.png)

In Email Designer können Sie den Inhalt personalisieren:

* In der **Nachricht**: Klicken Sie in einen Textblock, klicken Sie auf das Symbol **Personalisieren** in der kontextbezogenen Symbolleiste und wählen Sie **Personalisierungfeld einfügen** aus. Weiterführende Informationen zur Benutzeroberfläche von Email Designer finden Sie in [diesem Abschnitt](../design-emails.md).

   ![](assets/perso_insert.png)

* Für einen **Link**: Wählen Sie Text oder ein Bild in einem Textblock aus und klicken Sie in der kontextbezogenen Symbolleiste auf das Symbol **Link einfügen**. Im Fenster können Sie einen Personalisierungsblock hinzufügen, indem Sie auf das Symbol **Personalisierung hinzufügen** klicken.

   ![](assets/perso_link.png)

In beiden Fällen greifen Sie auf den Personalisierungseditor zu.

![](assets/perso_ee.png)

### Push-Benachrichtigungen personalisieren

Sie können **Push-Benachrichtigungen** auch in den folgenden Feldern personalisieren:

* **Titel**
* **Textkörper**
* **Benutzerdefinierter Benachrichtigungston**
* **Badges**
* **Benutzerspezifische Daten**

![](assets/perso_push.png)

Weitere Informationen zur Konfiguration von Push-Benachrichtigungen finden Sie in [diesem Abschnitt](../push-gs.md).

### Angebote personalisieren {#personalize-offers}

Sie können auch auf den Personalisierungs-Editor zugreifen, wenn Sie den Angebotsdarstellungen Inhalte vom Typ Text hinzufügen.

Weitere Informationen zur Verwaltung von Inhalten mit dem Entscheidungs-Management finden Sie in [diesem Abschnitt](../offers/offer-library/creating-personalized-offers.md#custom-text).

## Ausdruckseditor verwenden {#use-expression-editor}

Der Ausdruckseditor ist das Herzstück der Personalisierung in [!DNL Journey Optimizer].

Er ist in jedem Kontext verfügbar, in dem Sie eine Personalisierung definieren müssen, wie z. B. E-Mails, Push-Benachrichtigungen und Angebote.

In der Benutzeroberfläche des Ausdruckseditors können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen.

![](assets/perso_ee1.png)

Im linken Bildschirmbereich wird ein Domain-Selektor angezeigt, mit dem Sie die Quelle für die Personalisierung auswählen können.

![](assets/perso_ee3.png)

Verfügbare Quellen sind:

* **[!UICONTROL Profilattribute]**: Listet alle Verweise auf, die mit dem Profilschema verknüpft sind, das in der [Dokumentation des Adobe Experience Platform-Datenmodells (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target=&quot;_blank&quot;} beschrieben wird.
* **[!UICONTROL Segmentzugehörigkeit]**: Listet alle im Segmentierungs-Service von Adobe Experience Platform erstellten Segmente auf. Weitere Informationen zur Segmentierung finden Sie [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de){target=&quot;_blank&quot;}.
* **[!UICONTROL Angebotsentscheidungen]**: Listet alle Angebote auf, die mit einer bestimmten Platzierung verbunden sind. Wählen Sie die Platzierung aus und fügen Sie dann die Angebote in den Inhalt ein. Eine vollständige Dokumentation zum Verwalten von Angeboten finden Sie in [diesem Abschnitt](../deliver-personalized-offers.md).
* **[!UICONTROL Kontextuelle Attribute]**: Wenn die Aktivität **Nachricht** in einer Journey verwendet wird, stehen in diesem Menü kontextbezogene Journey-Felder zur Verfügung. Weiterführende Informationen finden Sie in diesem [Abschnitt](personalization-use-case.md).
* **[!UICONTROL Hilfsfunktionen]**: listet alle Hilfsfunktionen auf, die für die Durchführung von Datenoperationen wie Berechnungen, Datenformatierungen oder -konvertierungen, Bedingungen und die Bearbeitung von Daten im Rahmen der Personalisierung verfügbar sind. Weiterführende Informationen finden Sie in diesem [Abschnitt](functions/functions.md).

Bei der Auswahl wird die Referenz im Editor hinzugefügt.

>[!NOTE]
>
>Das Infosymbol neben dem Symbol „+“ öffnet eine QuickInfo mit weiteren Details zu jeder Variablen.

Im folgenden Beispiel können Sie mit dem Ausdruckseditor die Profile auswählen, die heute Geburtstag haben, und dann die Anpassung vervollständigen, indem Sie ein spezifisches Angebot einfügen, das zu diesem Tag passt.

![](assets/perso_ee2.png)

## Anleitungsvideos{#video-perso}

Erfahren Sie, wie Sie kontextbezogene Ereignisinformationen aus einer Journey verwenden können, um eine Nachricht zu personalisieren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Erfahren Sie, wie Sie kontextbezogene Ereignisinformationen aus einer Journey verwenden können, um eine Nachricht zu personalisieren.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
