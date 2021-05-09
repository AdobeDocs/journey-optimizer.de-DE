---
title: Entscheidungen erstellen
description: Erfahren Sie, wie Sie Entscheidungen erstellen
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Entscheidungen erstellen {#create-offer-activities}

Entscheidungen (früher als Angebot-Aktivitäten bezeichnet) sind Container für Ihre Angebot, die die Angebot-Entscheidungsmaschine nutzen, um das beste Angebot auszuwählen, das je nach Zielgruppe des Versands bereitgestellt werden soll.

![](../assets/do-not-localize/how-to-video.png) [Funktion im Video kennenlernen](#video).

Die Liste der Entscheidungen steht auf der Registerkarte **[!UICONTROL Angebot]** / **[!UICONTROL Entscheidungen]** zur Verfügung. Es stehen Filter zur Verfügung, mit denen Sie Entscheidungen nach Status, Beginn und Enddatum abrufen können.

![](../assets/activities-list.png)

Bevor Sie eine Entscheidung erstellen, stellen Sie sicher, dass die folgenden Komponenten in der Angebot-Bibliothek erstellt wurden:

* [Platzierungen](../offer-library/creating-placements.md),
* [Kollektionen](../offer-library/creating-collections.md),
* [Personalisierte Angebote](../offer-library/creating-personalized-offers.md)
* [Fallback-Angebote](../offer-library/creating-fallback-offers.md)

## Entscheidung {#create-activity} erstellen

1. Greifen Sie auf die Liste der Entscheidungen zu und klicken Sie dann auf **[!UICONTROL Aktivität erstellen]**.

1. Geben Sie den Namen der Entscheidung sowie Beginn und Enddatum und -zeit ein und klicken Sie dann auf **[!UICONTROL Weiter]**.

   ![](../assets/activities-name.png)

## hinzufügen Entscheidungen {#add-decisions}

1. Ziehen Sie eine Platzierung per Drag &amp; Drop aus der Liste, um sie der Entscheidung hinzuzufügen, und klicken Sie dann auf **[!UICONTROL Hinzufügen Sammlung]**.

   ![](../assets/activities-placement.png)

1. Wählen Sie die Kollektion aus, die die zu berücksichtigenden Angebote enthält, und klicken Sie auf **[!UICONTROL Hinzufügen]**.

   ![](../assets/activities-collection.png)

1. Die ausgewählten Angebote werden der Platzierung hinzugefügt. In diesem Beispiel haben wir zwei Angebote ausgewählt, die in einer JSON-Platzierung angezeigt werden, um Angebote in einer Callcenter-Lösung zu präsentieren.

   ![](../assets/offers-added.png)

1. Wenn mehrere Angebot für diese Platzierung infrage kommen, werden die Angebot mit der höchsten Priorität standardmäßig an den Kunden geliefert.

   Wenn Sie mit einer bestimmten Formel festlegen möchten, welches geeignete Angebot bereitgestellt werden soll, wählen Sie eine Rangformel aus der Dropdown-Liste **[!UICONTROL Rank-Angebot nach]**. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../offer-activities/configure-offer-selection.md).

1. Das Feld **[!UICONTROL Constraint]** schränkt die Auswahl der Angebot für diese Platzierung ein. Diese Einschränkung kann mithilfe einer Entscheidungsregel oder eines oder mehrerer Adobe Experience Platform-Segmente angewendet werden.

   Um die Auswahl der Angebot auf die Mitglieder eines Adobe Experience Platform-Segments zu beschränken, wählen Sie **[!UICONTROL Segmente]** und klicken Sie dann auf **[!UICONTROL Hinzufügen Segmente]**.

   ![](../assets/activity_constraint_segment.png)

   hinzufügen Sie eines oder mehrere Segmente aus dem linken Bereich, kombinieren Sie sie mit den logischen Operatoren **[!UICONTROL und]** / **[!UICONTROL Oder]** und klicken Sie dann auf **[!UICONTROL Wählen Sie]**, um dies zu bestätigen.

   Weitere Informationen zum Arbeiten mit Segmenten finden Sie in der Dokumentation zum [Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

   ![](../assets/activity_constraint_segment2.png)

   Wenn Sie eine Auswahlbeschränkung für diese Platzierung mithilfe einer Entscheidungsregel hinzufügen möchten, wählen Sie die Option **[!UICONTROL Entscheidungsregel]** und ziehen Sie dann die gewünschte Regel aus dem linken Bereich in den Bereich **[!UICONTROL Entscheidungsregel]**. Weiterführende Informationen zur Verwendung einer Entscheidungsregel finden Sie in [diesem Abschnitt](../offer-library/creating-decision-rules.md).

   ![](../assets/activity_constraint_rule.png)

## hinzufügen eines Fallback-Angebots {#add-fallback}

Wählen Sie das Fallback-Angebot aus, das Kunden, die nicht den Regeln der Angebotsbedingung und den Einschränkungen entsprechen, in letzter Instanz angezeigt wird, und klicken Sie dann auf **[!UICONTROL Weiter]**.

![](../assets/add-fallback-offer.png)

## Überprüfen und speichern Sie die Entscheidung {#review}

Wenn alles korrekt konfiguriert ist und Ihre Entscheidung verwendet werden kann, um Angebot Kunden vorzustellen, klicken Sie auf **[!UICONTROL Fertig stellen]** und wählen Sie **[!UICONTROL Speichern und aktivieren]**.

Sie können die Entscheidung auch als Entwurf speichern, um sie später zu bearbeiten und zu aktivieren.

![](../assets/save-activities.png)

Die Entscheidung wird in der Liste mit dem Status **[!UICONTROL Live]** oder **[!UICONTROL Entwurf]** angezeigt, je nachdem, ob Sie sie im vorherigen Schritt aktiviert haben oder nicht.

Sie ist jetzt bereit, für das Senden von Angeboten an Kunden genutzt zu werden. Sie können das Tag auswählen, um seine Eigenschaften anzuzeigen und zu bearbeiten oder zu unterdrücken.

Weitere Informationen zur Bereitstellung von Angeboten finden Sie in den folgenden Abschnitten:

* [hinzufügen personalisierter Angebot in Nachrichten](../../deliver-personalized-offers.md)
* [Bereitstellen von Angeboten mithilfe von APIs](../api-reference/decisions-api/deliver-offers.md)

![](../assets/activities-created.png)

>[!NOTE]
>
>Nachdem eine Entscheidung erstellt wurde, können Sie in der Liste auf ihren Namen klicken, um auf detaillierte Informationen zuzugreifen und alle daran vorgenommenen Änderungen mithilfe der Registerkarte **[!UICONTROL Änderungsprotokoll]** zu überprüfen (siehe [Änderungsprotokoll](../get-started/user-interface.md#changes-log) für Angebot und Entscheidungen).

## tutorial {#video}

>[!NOTE]
>
>Dieses Video bezieht sich auf den auf Adobe Experience Platform aufbauenden Offer decisioning-Anwendungsdienst. Sie enthält jedoch allgemeine Leitlinien für die Verwendung von Angebot im Kontext von Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
