---
title: Personalisierte Angebote erstellen
description: Hier erfahren Sie, wie Sie in Adobe Experience Platform personalisierte Angebote erstellen.
feature: Angebote
topic: Integrationen
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 94%

---

# Personalisierte Angebote erstellen {#creating-personalized-offers}

Vor der Erstellung eines Angebots sollten Sie Folgendes erstellt haben:

* Eine **Platzierung**, in der das Angebot angezeigt wird. Siehe [.Erstellen von Platzierungen](../offer-library/creating-placements.md)
* Eine **Entscheidungsregel**, die die Bedingung für die Unterbreitung des Angebots definiert. Weitere Informationen finden Sie unter [Entscheidungsregeln erstellen](../offer-library/creating-decision-rules.md).
* Ein oder mehrere **Tags**, die Sie mit dem Angebot verknüpfen möchten. Weitere Informationen finden Sie unter [Tags erstellen](../offer-library/creating-tags.md).

➡️ [Entdecken Sie diese Funktion im Video](#video)

Die Liste der personalisierten Angebote ist im Menü **[!UICONTROL Angebote]** verfügbar.

![](../../assets/offers_list.png)

## Angebot erstellen {#create-offer}

Gehen Sie wie folgt vor, um ein **Angebot** zu erstellen:

1. Klicken Sie auf **[!UICONTROL Angebot erstellen]** und wählen Sie dann **[!UICONTROL Personalisiertes Angebot]** aus.

   ![](../../assets/create_offer.png)

1. Geben Sie den Namen des Angebots sowie sein Anfangs- und Enddatum sowie die entsprechende Uhrzeit an. Sie können dem Angebot auch ein oder mehrere Tags zuordnen, damit Sie die Angebotsbibliothek leichter durchsuchen und organisieren können.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >Im Abschnitt **[!UICONTROL Angebotsattribute]** können Sie für Berichterstellungs- und Analysezwecke Schlüsselwertpaare mit dem Angebot verknüpfen.

## Darstellungen des Angebots konfigurieren {#representations}

1. Fügen Sie mithilfe der Schaltfläche **[!UICONTROL Darstellung hinzufügen]** eine oder mehrere Darstellungen für Ihr Angebot hinzu.

   >[!NOTE]
   >
   >Ein Angebot kann in einer Nachricht an verschiedenen Stellen angezeigt werden: in einem oberen Banner mit einem Bild, als Text in einem Absatz, als HTML-Block usw. Je mehr Darstellungen ein Angebot hat, desto mehr Möglichkeiten gibt es, das Angebot in verschiedenen Platzierungskontexten zu verwenden.

1. Geben Sie für jede Darstellung den **[!UICONTROL Kanal]** und die **[!UICONTROL Platzierung]** an, an der das Angebot angezeigt werden soll.

   ![](../../assets/channel-placement.png)

   Mit der Schaltfläche **[!UICONTROL Durchsuchen]** können Sie verfügbare Platzierungen filtern und nach ihrem Kanal und/oder Inhaltstyp filtern.

   ![](../../assets/browse-placements.png)

1. Fügen Sie jeder Darstellung Inhalte hinzu, die aus der Adobe Experience Cloud Assets-Bibliothek oder von einem externen öffentlichen Speicherort stammen. 

   * Um Inhalte aus der Adobe Experience Cloud Assets-Bibliothek hinzuzufügen, ziehen Sie diese aus dem linken Bereich in den Darstellungsbereich und geben Sie dann im Feld **[!UICONTROL Ziel-Link]** die URL an, die mit dem Inhalt verknüpft werden soll.

      >[!NOTE]
      >
      >Inhalte können nur aus der Asset-Auswahl im linken Panel gezogen und abgelegt werden. Es sind nur Inhalte verfügbar, die dem Inhaltstyp der Platzierung entsprechen.

      ![](../../assets/offer_drag_content.png)

   * Um Inhalte von einem externen öffentlichen Speicherort hinzuzufügen, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt hinzufügen]** und geben Sie dann den Namen, die URL und den Ziel-Link des hinzuzufügenden Inhalts an.

      Vergewissern Sie sich, dass der Inhalt, den Sie hinzufügen, dem Inhaltstyp der ausgewählten Platzierung entspricht.

      ![](../../assets/offer_add_content.png)

   * Sie können auch Textinhalte einfügen. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Inhalt hinzufügen]** und wählen Sie dann die Option **[!UICONTROL Eigener Text]**. Geben Sie im Feld **[!UICONTROL Text]** den Text ein, der im Angebot angezeigt werden soll.

      >[!NOTE]
      >
      >Bei Platzierungen vom Typ „Bild“ ist diese Option nicht verfügbar.

      ![](../../assets/offer_text_content.png)

## Eignungsregeln und Einschränkungen hinzufügen {#eligibility}

Mit Eignungsregeln und Einschränkungen können Sie festlegen, unter welchen Bedingungen ein Angebot angezeigt werden soll.

1. Konfigurieren Sie die **[!UICONTROL Angebotseignung]**. Standardmäßig ist die Entscheidungsregel **[!UICONTROL Alle Besucher]** aktiviert, d. h. jedes Profil ist dazu geeignet, das Angebot angezeigt zu bekommen.

   Sie können die Präsentation eines Angebots auf die Mitglieder eines oder mehrerer Adobe Experience Platform-Segmente einschränken. Aktivieren Sie dazu die Option **[!UICONTROL Besucher, die zu mindestens einem Segment passen]**, fügen Sie dann ein oder mehrere Segmente aus dem linken Bereich hinzu und kombinieren Sie sie mit den logischen Operatoren **[!UICONTROL Und]** / **[!UICONTROL Oder]**.

   Weitere Informationen zum Arbeiten mit Segmenten finden Sie auf [dieser Seite](../../segment/about-segments.md).

   ![](../../assets/offer-eligibility-segment.png)

   Wenn Sie eine bestimmte Entscheidungsregel mit dem Angebot verknüpfen möchten, wählen Sie **[!UICONTROL Nach definierter Entscheidungsregel]** aus und ziehen Sie die gewünschte Regel dann aus dem linken Bereich in den Bereich **[!UICONTROL Entscheidungsregel]**. Weiterführende Informationen zur Verwendung einer Entscheidungsregel finden Sie in [diesem Abschnitt](../offer-library/creating-decision-rules.md).

   ![](../../assets/offer_rule.png)

1. Definieren Sie die **[!UICONTROL Priorität]** des Angebots gegenüber anderen, wenn der Benutzer für mehr als ein Angebot geeignet ist. Je höher die Priorität eines Angebots ist, desto höher ist seine Priorität gegenüber anderen Angeboten.

1. Geben Sie die **[!UICONTROL Begrenzung]** des Angebots an, d. h. wie oft das Angebot insgesamt für alle Benutzer angezeigt wird. Wenn das Angebot allen Benutzern so oft bereitgestellt wurde, wie Sie es in diesem Feld angegeben haben, wird der Versand beendet.

   >[!NOTE]
   >
   >Die Häufigkeit, mit der ein Angebot vorgeschlagen wird, wird zum Zeitpunkt der E-Mail-Vorbereitung berechnet. Wenn Sie z. B. eine E-Mail mit mehreren Angeboten vorbereiten, wird diese Anzahl dem Begrenzungswert angerechnet, unabhängig davon, ob die E-Mail gesendet wird oder nicht.
   >
   >Wenn ein E-Mail-Versand gelöscht oder die Vorbereitung vor dem Senden erneut vorgenommen wird, wird der Begrenzungswert für das Angebot automatisch aktualisiert.

   ![](../../assets/offer_capping.png)

   Im obigen Beispiel:

   * Die Priorität des Angebots ist mit „50“ festgelegt, d. h. das Angebot wird vor Angeboten mit einer Priorität zwischen 1 und 49 und nach Angeboten mit einer Priorität von mindestens 51 unterbreitet.
   * Das Angebot wird nur bei Benutzern berücksichtigt, die die Entscheidungsregel „Gold-Treuekunden“ erfüllen.
   * Das Angebot wird nur einmal pro Benutzer unterbreitet.

## Angebot überprüfen {#review}

Sobald Eignungsregeln und Einschränkungen definiert wurden, wird eine Zusammenfassung der Angebotseigenschaften angezeigt. Wenn alles ordnungsgemäß konfiguriert ist und Ihr Angebot bereit ist, den Benutzern präsentiert zu werden, klicken Sie auf **[!UICONTROL Beenden]** und wählen Sie **[!UICONTROL Speichern und genehmigen]**.

Sie können das Angebot auch als Entwurf speichern, um es später zu bearbeiten und zu genehmigen.

![](../../assets/offer_review.png)

Das Angebot wird in der Liste mit dem Status **[!UICONTROL Live]** oder **[!UICONTROL Entwurf]** angezeigt, je nachdem, ob Sie es im vorherigen Schritt genehmigt haben oder nicht.

Es kann jetzt Benutzern unterbreitet werden. Sie können das Angebot auswählen, um seine Eigenschaften anzuzeigen und um es zu bearbeiten oder zu unterdrücken.

![](../../assets/offer_created.png)

Nachdem ein Angebot erstellt wurde, können Sie auf seinen Namen in der Liste klicken, um auf detaillierte Informationen zuzugreifen und alle Änderungen zu überwachen, die an ihm vorgenommen wurden, indem Sie den Tab **[!UICONTROL Änderungsprotokoll]** verwenden. [Weitere Informationen](../get-started/user-interface.md#monitoring-changes).

## Tutorial {#video}

>[!NOTE]
>
>Dieses Video bezieht sich auf den auf Adobe Experience Platform aufbauenden Programm-Service Offer Decisioning. Es enthält allgemeine Leitlinien für die Verwendung von Angeboten im Kontext von Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
