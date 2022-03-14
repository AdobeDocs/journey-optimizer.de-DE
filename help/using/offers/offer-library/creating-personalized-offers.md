---
title: Erstellen von personalisierten Angeboten
description: Erfahren Sie, wie Sie Ihre Angebote erstellen, konfigurieren und verwalten können
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: ht
source-wordcount: '1565'
ht-degree: 100%

---

# Personalisierte Angebote erstellen {#create-personalized-offers}

Vor der Erstellung eines Angebots sollten Sie Folgendes erstellt haben:

* Eine **Platzierung**, in der das Angebot angezeigt wird. Siehe [Platzierungen erstellen](../offer-library/creating-placements.md)
* Wenn Sie eine Eignungsbedingung hinzufügen möchten: eine **Entscheidungsregel** definiert die Bedingung, unter der das Angebot unterbreitet wird. Weitere Informationen finden Sie unter [Erstellen von Entscheidungsregeln](../offer-library/creating-decision-rules.md).
* Ein oder mehrere **Tags**, die Sie mit dem Angebot verknüpfen möchten. Weitere Informationen finden Sie unter [Erstellen von Tags](../offer-library/creating-tags.md).

➡️ [Entdecken Sie diese Funktion im Video](#video).

Die Liste der personalisierten Angebote ist im Menü **[!UICONTROL Angebote]** verfügbar.

![](../assets/offers_list.png)

## Angebot erstellen {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="Info zu Angebotsattributen"
>abstract="Mit Angebotsattributen können Sie für Reporting- und Analysezwecke Schlüssel-Wert-Paare mit dem Angebot verknüpfen."
>additional-url="https://video.tv.adobe.com/v/329375?captions=ger" text="Demovideo ansehen"

Gehen Sie wie folgt vor, um ein **Angebot** zu erstellen:

1. Klicken Sie auf **[!UICONTROL Angebot erstellen]** und wählen Sie dann **[!UICONTROL Personalisiertes Angebot]** aus.

   ![](../assets/create_offer.png)

1. Geben Sie den Namen des Angebots sowie sein Anfangs- und Enddatum sowie die entsprechende Uhrzeit an. Sie können dem Angebot auch ein oder mehrere Tags zuordnen, damit Sie die Angebotsbibliothek leichter durchsuchen und organisieren können.

   ![](../assets/offer_details.png)

   >[!NOTE]
   >
   >Im Abschnitt **[!UICONTROL Angebotsattribute]** können Sie für Reporting- und Analysezwecke Schlüssel-Wert-Paare mit dem Angebot verknüpfen.

## Darstellungen des Angebots konfigurieren {#representations}

Ein Angebot kann in einer Nachricht an verschiedenen Stellen angezeigt werden: in einem oberen Banner mit einem Bild, als Text in einem Absatz, als HTML-Block usw. Je mehr Darstellungen ein Angebot hat, desto mehr Möglichkeiten gibt es, das Angebot in verschiedenen Platzierungskontexten zu verwenden.

Gehen Sie wie folgt vor, um eine oder mehrere Darstellungen zu Ihrem Angebot hinzuzufügen und sie zu konfigurieren.

1. Wählen Sie für die erste Darstellung zunächst den zu verwendenden **[!UICONTROL Kanal]** aus.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Nur die verfügbaren Platzierungen für den ausgewählten Kanal werden in der Dropdown-Liste **[!UICONTROL Platzierung]** angezeigt.


1. Wählen Sie eine Platzierung aus der Liste aus.

   Sie können auch den Button neben der Dropdown-Liste **[!UICONTROL Platzierung]** verwenden, um alle Platzierungen zu durchsuchen.

   ![](../assets/browse-button-placements.png)

   Dort können Sie die Platzierungen nach Kanal und/oder Content-Typ filtern. Wählen Sie eine Platzierung aus und klicken Sie auf **[!UICONTROL Auswahl]**.

   ![](../assets/browse-placements.png)

1. Fügen Sie für Ihre Darstellung Inhalte hinzu. Mehr dazu erfahren Sie in [diesem Abschnitt](#content).

1. Wenn Sie Inhalte wie ein Bild oder eine URL hinzufügen, können Sie einen **[!UICONTROL Ziel-Link]** angeben: Die Benutzer, die auf das Angebot klicken, werden zur entsprechenden Seite weitergeleitet.

   ![](../assets/offer-destination-link.png)

1. Wählen Sie abschließend eine Sprache, um zu bestimmen, welche Inhalte den Benutzern angezeigt werden sollen.

1. Um eine weitere Darstellung hinzuzufügen, verwenden Sie die Schaltfläche **[!UICONTROL Darstellung hinzufügen]** und fügen Sie beliebig viele Darstellungen hinzu.

   ![](../assets/offer-add-representation.png)

1. Nachdem Sie alle Darstellungen hinzugefügt haben, klicken Sie auf **[!UICONTROL Weiter]**.

## Inhalte für Ihre Darstellungen definieren {#content}

Sie können einer Darstellung verschiedene Inhaltstypen hinzufügen.

>[!NOTE]
>
>Es sind nur Inhalte verfügbar, die dem Content-Typ der Platzierung entsprechen.

### Bilder hinzufügen {#images}

Wenn es sich bei der ausgewählten Platzierung um einen Bildtyp handelt, können Sie Inhalte aus der **Adobe Experience Cloud Assets**-Bibliothek hinzufügen, einem zentralen Repository mit Assets, das von [!DNL Adobe Experience Manager Assets Essentials] bereitgestellt wird.

>[!NOTE]
>
> Um [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=de){target=&quot;_blank&quot;} verwenden zu können, müssen Sie [!DNL Assets Essentials] für Ihr Unternehmen bereitstellen und sicherstellen, dass die Benutzer Teil der Produktprofile **Assets Essentials Consumer Users** und/oder **Assets Essentials Users** sind. Weitere Informationen finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=de){target=&quot;_blank&quot;}.

1. Wählen Sie die Option **[!UICONTROL Assets-Bibliothek]** aus.

1. Klicken Sie auf **[!UICONTROL Durchsuchen]**.

   ![](../assets/offer-browse-asset-library.png)

1. Durchsuchen Sie die Assets, um das Bild Ihrer Wahl auszuwählen.

1. Klicken Sie auf **[!UICONTROL Auswählen]**.

   ![](../assets/offer-select-asset.png)

### URLs hinzufügen {#urls}

Um Inhalte von einem externen öffentlichen Speicherort hinzuzufügen, klicken Sie auf **[!UICONTROL URL]** und geben Sie dann die URL-Adresse des hinzuzufügenden Inhalts ein.

![](../assets/offer-content-url.png)

### Hinzufügen von benutzerdefiniertem Text {#custom-text}

Sie können auch Textinhalte einfügen, wenn Sie eine kompatible Platzierung auswählen.

1. Wählen Sie die Option **[!UICONTROL Benutzerdefiniert]** aus und klicken Sie auf **[!UICONTROL Inhalt hinzufügen]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Bei Platzierungen vom Typ „Bild“ ist diese Option nicht verfügbar.

1. Geben Sie den Text ein, der im Angebot angezeigt werden soll.

   ![](../assets/offer-text-content.png)

   Sie können Ihren Inhalt mit dem Ausdruckseditor personalisieren. Erfahren Sie mehr zur [Personalisierung](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Nur die Quellen **[!UICONTROL Profilattribute]**, **[!UICONTROL Segmentzugehörigkeiten]** und **[!UICONTROL Helper-Funktionen]** sind für das Entscheidungs-Management verfügbar.

## Eignungsregeln und Einschränkungen hinzufügen {#eligibility}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="Informationen zu Angebotseinschränkungen"
>abstract="Mit Einschränkungen können Sie angeben, wie das Angebot priorisiert und dem Benutzer im Vergleich zu anderen Angeboten angezeigt wird."
>additional-url="https://video.tv.adobe.com/v/329375?captions=ger" text="Demovideo ansehen"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="Informationen zur Eignung von Angeboten"
>abstract="In diesem Abschnitt können Sie mithilfe von Entscheidungsregeln bestimmen, welche Benutzer für das Angebot geeignet sind."
>additional-url="https://video.tv.adobe.com/v/329373?captions=ger" text="Demovideo ansehen"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="Informationen zur Angebotspriorität "
>abstract="In diesem Feld können Sie die Prioritätseinstellungen für das Angebot festlegen. Die Priorität ist eine Zahl, die verwendet wird, um Angebote, die alle Einschränkungen wie Berechtigung, Datum und Begrenzungen erfüllen, in eine Rangfolge zu bringen."
>additional-url="https://video.tv.adobe.com/v/329375?captions=ger" text="Demovideo ansehen"

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Informationen zur Begrenzung von Angeboten"
>abstract="In diesem Feld können Sie angeben, wie oft das Angebot für alle Benutzer angezeigt werden kann."
>additional-url="https://video.tv.adobe.com/v/329375?captions=ger" text="Demovideo ansehen"

Mit Eignungsregeln und Einschränkungen können Sie festlegen, unter welchen Bedingungen ein Angebot angezeigt werden soll.

1. Konfigurieren Sie die **[!UICONTROL Angebotseignung]**.

   * Standardmäßig ist die Entscheidungsregel **[!UICONTROL Alle Besucher]** aktiviert, d. h. jedes Profil ist dazu geeignet, das Angebot angezeigt zu bekommen.

   * Sie können die Präsentation eines Angebots auf die Mitglieder eines oder mehrerer Adobe Experience Platform-Segmente einschränken. Aktivieren Sie dazu die Option **[!UICONTROL Besucher, die zu mindestens einem Segment passen]**, fügen Sie dann ein oder mehrere Segmente aus dem linken Bereich hinzu und kombinieren Sie sie mit den logischen Operatoren **[!UICONTROL Und]** / **[!UICONTROL Oder]**.

      Weitere Informationen zum Arbeiten mit Segmenten finden Sie auf [dieser Seite](../../segment/about-segments.md).

      ![](../assets/offer-eligibility-segment.png)

   * Wenn Sie eine bestimmte Entscheidungsregel mit dem Angebot verknüpfen möchten, wählen Sie **[!UICONTROL Nach definierter Entscheidungsregel]** aus und ziehen Sie die gewünschte Regel dann aus dem linken Bereich in den Bereich **[!UICONTROL Entscheidungsregel]**. Weiterführende Informationen zum Erstellen einer Entscheidungsregel finden Sie in [diesem Abschnitt](../offer-library/creating-decision-rules.md).

      ![](../assets/offer_rule.png)

      >[!CAUTION]
      >
      >Ereignisbasierte Angebote werden derzeit in [!DNL Journey Optimizer] nicht unterstützt. Wenn Sie eine Entscheidungsregel basierend auf einem [Ereignis](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=de#events){target=&quot;_blank&quot;} erstellen, können Sie sie in einem Angebot nicht nutzen.
   Weitere Informationen zur Verwendung von Segmenten versus Entscheidungsregeln finden Sie in [diesem Abschnitt](../offer-activities/create-offer-activities.md#segments-vs-decision-rules).

1. Definieren Sie die **[!UICONTROL Priorität]** des Angebots gegenüber anderen, wenn der Benutzer für mehr als ein Angebot geeignet ist. Je höher die Priorität eines Angebots ist, desto höher ist seine Priorität gegenüber anderen Angeboten.

1. Geben Sie die **[!UICONTROL Begrenzung]** des Angebots an, d. h. wie oft das Angebot insgesamt für alle Benutzer angezeigt wird. Wenn das Angebot allen Benutzern so oft bereitgestellt wurde, wie Sie es in diesem Feld angegeben haben, wird der Versand beendet.

   >[!NOTE]
   >
   >Die Häufigkeit, mit der ein Angebot vorgeschlagen wird, wird zum Zeitpunkt der E-Mail-Vorbereitung berechnet. Wenn Sie z. B. eine E-Mail mit mehreren Angeboten vorbereiten, wird diese Anzahl dem Begrenzungswert angerechnet, unabhängig davon, ob die E-Mail gesendet wird oder nicht.
   >
   >Wenn ein E-Mail-Versand gelöscht oder die Vorbereitung vor dem Senden erneut vorgenommen wird, wird der Begrenzungswert für das Angebot automatisch aktualisiert.

   ![](../assets/offer_capping.png)

   Im obigen Beispiel:

   * Die Priorität des Angebots ist mit „50“ festgelegt, d. h. das Angebot wird vor Angeboten mit einer Priorität zwischen 1 und 49 und nach Angeboten mit einer Priorität von mindestens 51 unterbreitet.
   * Das Angebot wird nur bei Benutzern berücksichtigt, die die Entscheidungsregel „Gold-Treuekunden“ erfüllen.
   * Das Angebot wird nur einmal pro Benutzer unterbreitet.

## Angebot überprüfen {#review}

Sobald Eignungsregeln und Begrenzungen definiert wurden, wird eine Zusammenfassung der Angebotseigenschaften angezeigt.

1. Stellen Sie sicher, dass alles ordnungsgemäß konfiguriert ist.

1. Wenn Ihr Angebot bereit ist, den Benutzern präsentiert zu werden, klicken Sie auf **[!UICONTROL Beenden]**.

1. Wählen Sie **[!UICONTROL Speichern und genehmigen]** aus.

   ![](../assets/offer_review.png)

   Sie können das Angebot auch als Entwurf speichern, um es später zu bearbeiten und zu genehmigen.

Das Angebot wird in der Liste mit dem Status **[!UICONTROL Genehmigt]** oder **[!UICONTROL Entwurf]** angezeigt, je nachdem, ob Sie es im vorherigen Schritt genehmigt haben oder nicht.

Es kann jetzt Benutzern unterbreitet werden.

![](../assets/offer_created.png)

## Angebotsliste {#offer-list}

Sie können aus der Angebotsliste das Angebot auswählen, dessen Eigenschaften angezeigt werden sollen. Sie können das Angebot auch bearbeiten, seinen Status (**Entwurf**, **Genehmigt**, **Archiviert**) ändern, es duplizieren oder löschen.

![](../assets/offer_created.png)

Wählen Sie die Schaltfläche **[!UICONTROL Bearbeiten]** aus, um zum Bearbeitungsmodus für Angebote zurückzukehren. Dort können Sie die [Details](#create-offer) und [Darstellungen](#representations) des Angebots ändern und die [Eignungsregeln und Begrenzungen](#eligibility) bearbeiten.

Wählen Sie ein genehmigtes Angebot aus und klicken Sie auf **[!UICONTROL Genehmigung rückgängig machen]**, um den Angebotsstatus wieder auf **[!UICONTROL Entwurf]** zu setzen.

Um den Status erneut auf **[!UICONTROL Genehmigt]** zu setzen, wählen Sie die entsprechende Schaltfläche aus, die jetzt angezeigt wird.

![](../assets/offer_approve.png)

Die Schaltfläche **[!UICONTROL Weitere Aktionen]** aktiviert die unten beschriebenen Aktionen.

![](../assets/offer_more-actions.png)

* **[!UICONTROL Duplizieren]**: erstellt ein Angebot mit denselben Eigenschaften, Darstellungen, Eignungsregeln und Begrenzungen. Standardmäßig weist das neue Angebot den Status **[!UICONTROL Entwurf]** auf.
* **[!UICONTROL Löschen]**: entfernt das Angebot aus der Liste.

   >[!CAUTION]
   >
   >Auf das Angebot und seinen Inhalt kann nicht mehr zugegriffen werden. Diese Aktion kann nicht rückgängig gemacht werden.
   >
   >Wenn das Angebot in einer Kollektion oder Entscheidung verwendet wird, kann es nicht gelöscht werden. Sie müssen das Angebot zuerst aus allen Objekten entfernen.

* **[!UICONTROL Archivieren]**: setzt den Angebotsstatus auf **[!UICONTROL Archiviert]**. Das Angebot ist weiterhin in der Liste verfügbar, Sie können seinen Status jedoch nicht auf **[!UICONTROL Entwurf]** oder **[!UICONTROL Genehmigt]** zurücksetzen. Sie können es nur duplizieren oder löschen.

Sie können auch den Status mehrerer Angebote gleichzeitig löschen oder ändern, indem Sie die entsprechenden Checkboxen auswählen.

![](../assets/offer_multiple-selection.png)

Wenn Sie den Status mehrerer Angebote mit unterschiedlichen Status ändern möchten, werden nur die relevanten Status geändert.

![](../assets/offer_change-status.png)

Nachdem ein Angebot erstellt wurde, können Sie in der Liste auf seinen Namen klicken.

![](../assets/offer_click-name.png)

Auf diese Weise können Sie auf detaillierte Informationen zu diesem Angebot zugreifen. Wählen Sie die Registerkarte **[!UICONTROL Protokoll ändern]** aus, um [alle Änderungen zu überwachen](../get-started/user-interface.md#monitoring-changes), die am Angebot vorgenommen wurden.

![](../assets/offer_information.png)

## Anleitungsvideo {#video}

>[!NOTE]
>
>Dieses Video bezieht sich auf den auf Adobe Experience Platform aufbauenden Anwendungsdienst Offer Decisioning. Es enthält allgemeine Leitlinien für die Verwendung von Angeboten im Kontext von Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
