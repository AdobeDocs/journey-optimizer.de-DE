---
title: Personalisierte Angebote erstellen
description: Hier erfahren Sie, wie Sie in Adobe Experience Platform personalisierte Angebote erstellen.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 0%

---

# Personalisierte Angebote erstellen {#creating-personalized-offers}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="Informationen zu Angebot-Einschränkungen"
>abstract="Mit Einschränkungen können Sie angeben, wie das Angebot priorisiert und dem Benutzer im Vergleich zu anderen Angeboten angezeigt wird."
>additional-url="https://video.tv.adobe.com/v/329375" text="Demovideo ansehen"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="Informationen zur Angebot-Berechtigung"
>abstract="In diesem Abschnitt können Sie mithilfe von Entscheidungsregeln bestimmen, welche Benutzer für das Angebot berechtigt sind."
>additional-url="https://experienceleague.adobe.com/docs/offer-decisioning/using/managing-offers-in-the-offer-library/creating-decision-rules.html" text="Entscheidungsregeln erstellen"
>additional-url="https://video.tv.adobe.com/v/329373" text="Demovideo ansehen"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="Informationen zur Priorität Angebot"
>abstract="In diesem Feld können Sie die Prioritätseinstellungen für das Angebot festlegen. Priorität ist eine Zahl, die verwendet wird, um Angebot einzustufen, die alle Einschränkungen wie Förderfähigkeit, Daten und Deckelung erfüllen."
>additional-url="https://video.tv.adobe.com/v/329375" text="Demovideo ansehen"

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Informationen zur Angebot-Deckelung"
>abstract="In diesem Feld können Sie angeben, wie oft das Angebot für alle Benutzer angezeigt werden kann."
>additional-url="https://video.tv.adobe.com/v/329375" text="Demovideo ansehen"

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="Info zu Angebot-Attributen"
>abstract="Mit Angebot-Attributen können Sie Schlüsselwertpaare zu Berichte- und Analysen mit dem Angebot verknüpfen."
>additional-url="https://video.tv.adobe.com/v/329375" text="Demovideo ansehen"

Vor der Erstellung eines Angebots sollten Sie Folgendes erstellt haben:

* Eine **Platzierung**, in der das Angebot angezeigt wird. Siehe [Erstellen von Platzierungen](../offer-library/creating-placements.md)
* Eine **Entscheidungsregel**, die die Bedingung für die Unterbreitung des Angebots definiert. Weitere Informationen finden Sie unter [Entscheidungsregeln erstellen](../offer-library/creating-decision-rules.md).
* Ein oder mehrere **Tags**, die Sie mit dem Angebot verknüpfen möchten. Weitere Informationen finden Sie unter [Tags erstellen](../offer-library/creating-tags.md).

![](../assets/do-not-localize/how-to-video.png) [Funktion im Video kennenlernen](#video).

Die Liste personalisierter Angebot ist im Menü **[!UICONTROL Angebot]** verfügbar.

![](../assets/offers_list.png)

## Angebot {#create-offer} erstellen

Gehen Sie wie folgt vor, um ein **Angebot** zu erstellen:

1. Klicken Sie auf **[!UICONTROL Angebot erstellen]** und wählen Sie **[!UICONTROL Personalisiertes Angebot]**.

   ![](../assets/create_offer.png)

1. Geben Sie den Namen des Angebots sowie sein Anfangs- und Enddatum sowie die entsprechende Uhrzeit an. Sie können dem Angebot auch ein oder mehrere Tags zuordnen, damit Sie die Angebotsbibliothek leichter durchsuchen und organisieren können.

   ![](../assets/offer_details.png)

   >[!NOTE]
   >
   >Im Abschnitt **[!UICONTROL Angebotsattribute]** können Sie für Berichterstellungs- und Analysezwecke Schlüsselwertpaare mit dem Angebot verknüpfen.

## Konfigurieren der Darstellungen des Angebots {#representations}

1. Fügen Sie mithilfe der Schaltfläche **[!UICONTROL Darstellung hinzufügen]** eine oder mehrere Darstellungen für Ihr Angebot hinzu.

   >[!NOTE]
   >
   >Ein Angebot kann in einer Nachricht an verschiedenen Stellen angezeigt werden: in einem oberen Banner mit einem Bild, als Text in einem Absatz, als HTML-Block usw. Je mehr Darstellungen ein Angebot hat, desto mehr Möglichkeiten gibt es, das Angebot in verschiedenen Platzierungskontexten zu verwenden.

1. Geben Sie für jede Darstellung den **[!UICONTROL Kanal]** und die **[!UICONTROL Platzierung]** an, an der das Angebot angezeigt werden soll.

   ![](../assets/channel-placement.png)

   Mit der Schaltfläche **[!UICONTROL Durchsuchen]** können Sie verfügbare Platzierungen filtern und nach ihrem Kanal und/oder Inhaltstyp filtern.

   ![](../assets/browse-placements.png)

1. Fügen Sie jeder Darstellung Inhalte hinzu, die aus der Adobe Experience Cloud Assets-Bibliothek oder von einem externen öffentlichen Speicherort stammen. 

   * Um Inhalte aus der Adobe Experience Cloud Assets-Bibliothek hinzuzufügen, ziehen Sie diese aus dem linken Bereich in den Darstellungsbereich und geben Sie dann im Feld **[!UICONTROL Ziel-Link]** die URL an, die mit dem Inhalt verknüpft werden soll.

      >[!NOTE]
      >
      >Inhalte können nur aus der Asset-Auswahl im linken Bereich gezogen und abgelegt werden. Es sind nur Inhalte verfügbar, die dem Inhaltstyp der Platzierung entsprechen.

      ![](../assets/offer_drag_content.png)

   * Um Inhalte von einem externen öffentlichen Speicherort hinzuzufügen, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt hinzufügen]** und geben Sie dann den Namen, die URL und den Ziel-Link des hinzuzufügenden Inhalts an.

      Vergewissern Sie sich, dass der Inhalt, den Sie hinzufügen, dem Inhaltstyp der ausgewählten Platzierung entspricht.

      ![](../assets/offer_add_content.png)

   * Sie können auch Textinhalte einfügen. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Inhalt hinzufügen]** und wählen Sie dann die Option **[!UICONTROL Eigener Text]**. Geben Sie im Feld **[!UICONTROL Text]** den Text ein, der im Angebot angezeigt werden soll.

      >[!NOTE]
      >
      >Bei Platzierungen vom Typ „Bild“ ist diese Option nicht verfügbar.

      ![](../assets/offer_text_content.png)

## hinzufügen Eignungsregeln und Einschränkungen {#eligibility}

Mit Eignungsregeln und Einschränkungen können Sie festlegen, unter welchen Bedingungen ein Angebot angezeigt werden soll.

1. Konfigurieren Sie die **[!UICONTROL Angebot-Berechtigung]**. Standardmäßig ist die Entscheidungsregel **[!UICONTROL Alle Besucher]** aktiviert, d. h. jedes Profil ist dazu geeignet, das Angebot angezeigt zu bekommen.

   Sie können die Präsentation des Angebots auf die Mitglieder eines oder mehrerer Adobe Experience Platform-Segmente beschränken. Aktivieren Sie dazu die Option **[!UICONTROL Besucher, die in ein oder mehrere Segmente]** fallen, fügen Sie dann ein oder mehrere Segmente aus dem linken Bereich hinzu und kombinieren Sie sie mit den logischen Operatoren **[!UICONTROL Und]** / **[!UICONTROL Oder]**.

   Weitere Informationen zum Arbeiten mit Segmenten finden Sie in der Dokumentation zum [Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

   ![](../assets/offer-eligibility-segment.png)

   Wenn Sie eine bestimmte Entscheidungsregel mit dem Angebot verknüpfen möchten, wählen Sie **[!UICONTROL Nach definierter Entscheidungsregel]** und ziehen Sie dann die gewünschte Regel aus dem linken Bereich in den Bereich **[!UICONTROL Decision rule]**. Weiterführende Informationen zur Verwendung einer Entscheidungsregel finden Sie in [diesem Abschnitt](../offer-library/creating-decision-rules.md).

   ![](../assets/offer_rule.png)

1. Definieren Sie die **[!UICONTROL Priority]** des Angebots im Vergleich zu anderen, wenn der Benutzer mehr als ein Angebot beansprucht. Je höher die Priorität eines Angebots ist, desto höher wird seine Priorität im Vergleich zu anderen Angeboten sein

1. Geben Sie die **[!UICONTROL Begrenzung]** des Angebots an, d. h., wie oft das Angebot insgesamt für alle Benutzer angezeigt wird. Wenn das Angebot in der Anzahl der in diesem Feld angegebenen Bereitstellungen für alle Benutzer bereitgestellt wurde, wird der Versand beendet.

   >[!NOTE]
   >
   >Die Häufigkeit, mit der ein Angebot vorgeschlagen wird, wird zum Zeitpunkt der E-Mail-Vorbereitung berechnet. Wenn Sie z. B. eine E-Mail mit einer Reihe von Angeboten vorbereiten, werden die entsprechenden Zahlen auf die maximale Begrenzung angerechnet, unabhängig davon, ob die E-Mail gesendet wird oder nicht.
   >
   >Wenn ein E-Mail-Versand gelöscht oder die Vorbereitung vor dem Senden erneut vorgenommen wird, wird der Begrenzungswert für das Angebot automatisch aktualisiert.

   ![](../assets/offer_capping.png)

   Im obigen Beispiel:

   * Die Priorität des Angebots ist mit „50“ festgelegt, d. h. das Angebot wird vor Angeboten mit einer Priorität zwischen 1 und 49 und nach Angeboten mit einer Priorität von mindestens 51 unterbreitet.
   * Das Angebot wird nur bei Benutzern berücksichtigt, die die Entscheidungsregel „Gold-Treuekunden“ erfüllen.
   * Das Angebot wird nur einmal pro Benutzer unterbreitet.

## Überprüfen Sie das Angebot {#review}

Sobald Eignungsregeln und Einschränkungen definiert wurden, wird eine Zusammenfassung der Angebotseigenschaften angezeigt. Wenn alles korrekt konfiguriert ist und Ihr Angebot für die Anzeige für Benutzer bereit ist, klicken Sie auf **[!UICONTROL Fertig stellen]** und wählen Sie **[!UICONTROL Speichern und genehmigen]**.

Sie können das Angebot auch als Entwurf speichern, um es später zu bearbeiten und zu genehmigen.

![](../assets/offer_review.png)

Das Angebot wird in der Liste mit dem Status **[!UICONTROL Live]** oder **[!UICONTROL Entwurf]** angezeigt, je nachdem, ob Sie es im vorherigen Schritt genehmigt haben oder nicht.

Es kann jetzt an Benutzer geliefert werden. Sie können das Tag auswählen, um seine Eigenschaften anzuzeigen und zu bearbeiten oder zu unterdrücken.

![](../assets/offer_created.png)

Nachdem ein Angebot erstellt wurde, können Sie in der Liste auf seinen Namen klicken, um auf detaillierte Informationen zuzugreifen und alle daran vorgenommenen Änderungen mithilfe der Registerkarte **[!UICONTROL Änderungsprotokoll]** zu überwachen (siehe [Überwachungsänderungen an Angeboten und Entscheidungen](../get-started/user-interface.md#monitoring-changes)).

## tutorial {#video}

>[!NOTE]
>
>Dieses Video bezieht sich auf den auf Adobe Experience Platform aufbauenden Offer decisioning-Anwendungsdienst. Sie enthält jedoch allgemeine Leitlinien für die Verwendung von Angebot im Kontext von Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
