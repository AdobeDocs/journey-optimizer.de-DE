---
title: Entscheidungselemente
description: Erfahren Sie, wie Sie mit Entscheidungselementen arbeiten.
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 97%

---

# Entscheidungselemente {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="Verwalten von Entscheidungselementen"
>abstract="Mit Journey Optimizer können Sie Marketing-Angebote, die als Entscheidungselemente bezeichnet werden, erstellen und in einem zentralen Katalog und in Sammlungen organisieren. Derzeit sind alle erstellten Entscheidungselemente in einem einzigen „Angebote“-Katalog konsolidiert. Über diesen Bildschirm können Sie auch mithilfe der Schaltfläche **Schema bearbeiten** auf das Schema des Katalogs zugreifen und benutzerdefinierte Attribute für Ihre Entscheidungselemente erstellen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html?lang=de" text="Konfigurieren des Elementkatalogs"

>[!BEGINSHADEBOX &quot;Was Sie in diesem Handbuch finden werden&quot;]

* [Erste Schritte mit Offer Decisioning](gs-experience-decisioning.md)
* Verwalten Sie Ihre Entscheidungselemente: [Konfigurieren des Elementkatalogs](catalogs.md) - **[Erstellen von Entscheidungselementen](items.md)** - [Verwalten von Elementsammlungen](collections.md)
* Konfigurieren der Elementauswahl: [Entscheidungsregeln erstellen](rules.md) - [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Erstellen von Entscheidungsrichtlinien](create-decision.md)

>[!ENDSHADEBOX]

Mit Journey Optimizer können Sie Marketing-Angebote, die als Entscheidungselemente bezeichnet werden, erstellen und in einem zentralen Katalog und in Sammlungen organisieren. Sie bestehen aus standardmäßigen und benutzerdefinierten Attributen, die genau auf Ihre Bedürfnisse abgestimmt sind. Darüber hinaus enthalten sie Profileinschränkungen, mit denen Sie definieren können, wem ein Entscheidungselement angezeigt werden kann.

Bevor Sie ein Entscheidungselement erstellen, stellen Sie sicher, dass Sie eine **Entscheidungsregel** erstellt haben, wenn Sie Bedingungen festlegen möchten, um zu bestimmen, wem das Entscheidungselement angezeigt werden kann. [Erfahren Sie, wie Sie Entscheidungsregeln erstellen können](rules.md).

## Erstellen Ihres ersten Entscheidungselements

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="Definieren der Priorität des Entscheidungselements"
>abstract="Wenn ein Profil für mehrere Elemente geeignet ist, ermöglicht die Priorität den Vergleich dieses Entscheidungselements mit anderen. Eine höhere Priorität gewährt dem Element Vorrang vor anderen."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="Definieren der benutzerdefinierten Attribute"
>abstract="Benutzerdefinierte Attribute sind spezifische Attribute, die auf Ihre Anforderungen zugeschnitten sind und die Sie einem Entscheidungselement zuweisen können. Sie werden im Katalogschema der Entscheidungselemente erstellt. Dieser Abschnitt wird nur angezeigt, wenn Sie dem Katalogschema mindestens ein benutzerdefiniertes Attribut hinzugefügt haben."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html?lang=de" text="Konfigurieren des Elementkatalogs"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="Hinzufügen von Zielgruppen oder Entscheidungsregeln"
>abstract="Standardmäßig sind alle Profile berechtigt, das Entscheidungselement zu erhalten. Sie können jedoch Zielgruppen oder Regeln verwenden, um das Element auf bestimmte Profile zu beschränken."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html?lang=de" text="Verwenden von Zielgruppen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html?lang=de" text="Verwenden von Entscheidungsregeln"

Gehen Sie wie folgt vor, um eine Entscheidungsregel zu erstellen:

1. Navigieren Sie zu **[!UICONTROL Offer Decisioning]** > **[!UICONTROL Elemente]**.

1. Definieren Sie die Standardattribute des Entscheidungselements:

   1. Geben Sie einen Namen und eine Beschreibung ein.
   1. Geben Sie Start- und Enddatum an. Das Element wird von der Entscheidungs-Engine nur innerhalb dieser Daten berücksichtigt.
   1. Legen Sie die **[!UICONTROL Priorität]** des Entscheidungselements im Vergleich zu anderen fest, wenn ein Profil für mehrere Elemente qualifiziert ist. Eine höhere Priorität gewährt dem Element Vorrang vor anderen.

   ![](assets/item-attributes.png)

   >[!NOTE]
   >
   >Die Priorität ist ein ganzzahliger Datentyp. Alle Attribute, bei denen es sich um ganzzahlige Datentypen handelt, sollten ganzzahlige Werte (ohne Dezimalstellen) enthalten.

1. Benutzerdefinierte Attribute sind spezifische Attribute, die auf Ihre Anforderungen zugeschnitten sind und die Sie einem Entscheidungselement zuweisen können. Sie werden im Katalogschema der Entscheidungselemente definiert. [Erfahren Sie, wie Sie mit Vorlagen arbeiten](catalogs.md)

1. Sobald die Attribute des Entscheidungspunkts definiert sind, klicken Sie auf **[!UICONTROL Weiter]**, um Profileinschränkungen für das Element festzulegen.

   Standardmäßig sind alle Profile berechtigt, das Entscheidungselement zu erhalten. Sie können jedoch Zielgruppen oder Regeln verwenden, um das Element auf bestimmte Profile zu beschränken, wobei die beiden Lösungen unterschiedlichen Verwendungszwecken entsprechen. Erweitern Sie den folgenden Abschnitt, um weitere Informationen zu erhalten:

   +++Verwenden von Zielgruppen im Vergleich zu Entscheidungsregeln

   Grundsätzlich liefert eine Zielgruppe eine Liste von Profilen, während es sich bei einer Entscheidungsregel um eine Funktion handelt, die während des Entscheidungsprozesses bei Bedarf für ein einzelnes Profil ausgeführt wird.

   * **Zielgruppen**: Zielgruppen sind Adobe Experience Platform-Profile, die basierend auf Profilattributen und Erlebnisereignissen einer bestimmten Logik entsprechen. Jedoch wird beim Offer Decisioning-Prozess die Zielgruppe nicht neu berechnet, weshalb sie zum Zeitpunkt der Angebotsunterbreitung möglicherweise nicht aktuell ist.

   * **Entscheidungsregeln**: Dagegen basiert eine Entscheidungsregel auf in Adobe Experience Platform verfügbaren Daten und bestimmt, wem ein Angebot angezeigt werden kann. Nachdem die Entscheidungsregel in einem Angebot oder einer Entscheidung für eine bestimmte Platzierung ausgewählt wurde, wird sie bei jedem Entscheidungsvorgang erneut ausgeführt. Dadurch wird jedem Profil immer ein aktuelles, optimales Angebot angezeigt.

+++

   ![](assets/item-constraints.png)

   * Um die Präsentation des Entscheidungselements auf die Mitglieder einer oder mehrerer Adobe Experience Platform-Zielgruppen zu beschränken, wählen Sie die Option **[!UICONTROL Besucherinnen und Besucher, die zu mindestens einer Zielgruppe passen]** aus, fügen Sie dann eine oder mehrere Zielgruppen aus dem linken Bereich hinzu und kombinieren Sie sie mithilfe der logischen Operatoren **[!UICONTROL Und]**/**[!UICONTROL Oder]**. [Weitere Informationen zu Zielgruppen](../audience/about-audiences.md).

   * Um eine bestimmte Entscheidungsregel mit dem Entscheidungselement zu verknüpfen, wählen Sie **[!UICONTROL Nach Regel]** aus und ziehen Sie dann die gewünschte Regel aus dem linken Bereich in den zentralen Bereich. [Erfahren Sie mehr über Entscheidungsregeln](rules.md),

   Wenn Sie Zielgruppen oder Entscheidungsregeln auswählen, können Sie Informationen zur geschätzten Anzahl der qualifizierten Profile sehen. Klicken Sie auf **[!UICONTROL Aktualisieren]**, um diese Daten zu aktualisieren.

   >[!NOTE]
   >
   >Profilschätzungen sind nicht verfügbar, wenn Regelparameter Daten enthalten, die nicht im Profil enthalten sind, z. B. Kontextdaten. Beispielsweise eine Eignungsregel, für die die aktuelle Temperatur höher als 25 °C sein muss.

1. Sobald die Einschränkungen des Entscheidungselements definiert sind, klicken Sie auf **[!UICONTROL Weiter]**, um das Element zu überprüfen und zu speichern.

1. Das Entscheidungselement wird jetzt in der Liste angezeigt und hat den Status **[!UICONTROL Entwurf]**. Wenn es bereit ist, in Profilen präsentiert zu werden, klicken Sie auf die Schaltfläche mit den drei Punkten und wählen Sie **[!UICONTROL Genehmigen]** aus.

   ![](assets/item-approve.png)

## Verwalten von Entscheidungselementen

In der Liste der Entscheidungselemente können Sie ein Entscheidungselement bearbeiten und seinen Status ändern (**Entwurf**, **Genehmigt**, **Archiviert**), es duplizieren oder löschen.

Um ein Entscheidungselement zu ändern, öffnen Sie es, nehmen Sie Ihre Änderungen vor und speichern Sie es.

Wenn Sie ein Entscheidungselement auswählen oder auf die Schaltfläche mit den drei Punkten klicken, werden die unten beschriebenen Aktionen aktiviert.

* **[!UICONTROL Genehmigen]**: Setzt den Status des Entscheidungselements auf „Genehmigt“.
* **[!UICONTROL Genehmigung rückgängig machen]**: Setzt den Status des Entscheidungselements zurück auf **[!UICONTROL Entwurf]**.
* **[!UICONTROL Duplizieren]**: Erstellt ein Entscheidungselement mit identischen Attributen und Einschränkungen. Standardmäßig weist das neue Element den Status **[!UICONTROL Entwurf]** auf.
* **[!UICONTROL Löschen]**: Entfernt die Entscheidung aus der Liste.

  >[!IMPORTANT]
  >
  >Nach dem Löschen sind das Entscheidungselement und sein Inhalt nicht mehr verfügbar. Diese Aktion kann nicht rückgängig gemacht werden. Wenn das Angebot in einer Sammlung oder Entscheidung verwendet wird, kann es nicht gelöscht werden. Sie müssen das Entscheidungselement zuerst aus allen Objekten entfernen.

* **[!UICONTROL Archivieren]**: Setzt den Entscheidungsstatus auf **[!UICONTROL Archiviert]**. Das Entscheidungselement ist weiterhin in der Liste verfügbar, Sie können seinen Status jedoch nicht auf **[!UICONTROL Entwurf]** oder **[!UICONTROL Genehmigt]** zurücksetzen. Sie können es nur duplizieren oder löschen.
