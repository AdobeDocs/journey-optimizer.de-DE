---
solution: Journey Optimizer
product: journey optimizer
title: Aktivität „Inhaltsentscheidung“
description: Erfahren Sie mehr über die Aktivität zur Inhaltsentscheidung
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Aktivität, Entscheidungsfindung, Inhaltsentscheidung, Entscheidungsrichtlinie, Arbeitsfläche, Journey
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 5%

---

# Aktivität „Inhaltsentscheidung“ {#content-decision}

>[!AVAILABILITY]
>
>Diese Funktion ist nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.

Mit [!DNL Journey Optimizer] können Sie über die dedizierte Aktivität **Inhaltsentscheidung“ auf der Journey-** Angebote in Ihre Journey einbeziehen. Anschließend können Sie Ihren Journey weitere Aktivitäten (wie [benutzerdefinierte Aktionen](../action/about-custom-action-configuration.md) hinzufügen, um Ihre Zielgruppen mit diesen personalisierten Angeboten anzusprechen.

>[!NOTE]
>
>Die Ausgabe einer Inhaltsentscheidungsaktivität kann nicht in nativen Kanalaktivitäten verwendet werden.

Um diese Funktion zu nutzen, erstellen Sie einen Journey, in dem Sie eine [Inhaltsentscheidungsaktivität](#add-content-decision-activity) hinzufügen, um die Angebote zu definieren, die Sie den geeigneten Profilen unterbreiten möchten.

Sie können dann die Ausgabe der Aktivität Inhaltsentscheidung in folgenden Bereichen verwenden:

* eine [Bedingungsaktivität](#add-condition-activity), um Profile basierend auf den abgerufenen Angeboten in bestimmte Pfade zu verschieben;

* Eine [benutzerdefinierte Aktion](#add-custom-action), mit der Sie diese Angebote an externe Systeme senden können.

## Konfigurieren einer Inhaltsentscheidungsaktivität {#add-content-decision-activity}

Mit der Aktivität Inhaltsentscheidung können Sie eine Entscheidungsrichtlinie definieren, mit der Sie die besten Elemente aus [!DNL Journey Optimizer] Decisioning auswählen und sie für die richtige Zielgruppe bereitstellen können.

<!--Their goal is to select the best offers for each profile, while the campaign/journey authoring allows you to indicate how the selected decision items should be presented, including which item attributes to be included in the message.-->

Gehen Sie wie folgt vor, um **[!UICONTROL Aktivität]** Inhaltsentscheidung“ zu konfigurieren.

1. Erweitern Sie die Kategorie **[!UICONTROL Orchestrierung]** und legen Sie eine Aktivität **[!UICONTROL Inhaltsentscheidung]** auf Ihrer Arbeitsfläche ab.

   ![Fügen Sie der Journey eine Inhaltsentscheidung hinzu](assets/journey-content-decision.png){width=100%}

1. Fügen Sie optional einen Titel und eine Beschreibung zur Aktivität hinzu.

1. Klicken Sie **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**. [Weitere Informationen zu Entscheidungsrichtlinien](../experience-decisioning/create-decision.md)

   >[!NOTE]
   >
   >Entscheidungsberechtigungen sind erforderlich, um eine Entscheidungsrichtlinie zu erstellen. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md#steps)

1. Wählen Sie die Anzahl der Elemente, die zurückgegeben werden sollen. Wenn Sie beispielsweise „2“ auswählen, werden die besten zwei geeigneten Angebote angezeigt. Klicken Sie auf **[!UICONTROL Weiter]**.

1. Wählen **[!UICONTROL im Abschnitt]** die Entscheidungselemente und/oder Auswahlstrategien aus, die mit der Entscheidungsrichtlinie angezeigt werden sollen. [Weitere Informationen](../experience-decisioning/create-decision.md#select)

1. Ordnen Sie die Auswertungsreihenfolge nach Bedarf an.

   Beim Hinzufügen mehrerer Entscheidungselemente und/oder Strategien werden diese in sequenzieller Reihenfolge ausgewertet, wobei die Zahlen links von jedem Objekt oder jeder Objektgruppe angezeigt werden. Die Objekte und/oder Gruppen können nach Bedarf per Drag-and-Drop verschoben werden, um die Standardsequenz zu ändern.  [Weitere Informationen](../experience-decisioning/create-decision.md#evaluation-order)

1. Fügen Sie optional ein Fallback-Angebot hinzu. [Weitere Informationen](../experience-decisioning/create-decision.md#fallback)

1. Überprüfen und speichern Sie Ihre Entscheidungsrichtlinie.

   ![Zusammenfassung der Entscheidungsrichtlinie](assets/journey-content-decision-policy.png){width=70%}<!--reshoot or change screen-->

Sie können jetzt die Ausgabe dieser Inhaltsentscheidungsaktivität in Ihrem Journey nutzen.

## Verwenden der Ausgabe der Inhaltsentscheidungsaktivität {#use-content-decision-output}

Die Ausgabe einer Inhaltsentscheidung kann in mehreren Journey-Aktivitäten verwendet werden. Sie können beispielsweise eine Aktivität vom Typ [Bedingung](#add-condition-activity) verwenden, um Profile basierend auf der Anzahl der für sie abgerufenen Angebote in bestimmte Verzweigungen Ihres Journey zu verschieben.

Sie können Ihrer Journey auch eine [benutzerdefinierte Aktion](#add-custom-action) hinzufügen, um die Angebote aus der Inhaltsentscheidungsaktivität für ein externes System freizugeben.

### In einer Bedingungsaktivität {#add-condition-activity}

Um die Ausgabe einer Inhaltsentscheidungsaktivität zu nutzen, können Sie eine Bedingung zu Ihrem Journey hinzufügen, in der Sie Ausdrücke definieren, um Profile mithilfe von Daten aus diesen Angeboten in bestimmte Pfade zu verschieben. Führen Sie dazu folgende Schritte durch.

1. Ziehen Sie aus der Kategorie **[!UICONTROL Orchestrierung]** eine Aktivität **[!UICONTROL Bedingung]** auf Ihre Arbeitsfläche. [Weitere Informationen](condition-activity.md#add-condition-activity)

1. Optional können Sie **[!UICONTROL Path1]**, der dem ersten Ausdruck entspricht, den Sie definieren, in eine relevantere Bezeichnung umbenennen.

1. Klicken Sie für diesen ersten Pfad in das Feld **[!UICONTROL Ausdruck]** oder verwenden Sie das Symbol Bearbeiten , um einen Ausdruck hinzuzufügen.

   ![Bedingung hinzufügen und Ausdruck bearbeiten](assets/journey-content-decision-condition.png){width=80%}

1. Wechseln Sie im sich öffnenden Popup-Fenster in den **[!UICONTROL Erweiterter Modus]**, um den [erweiterten Ausdruckseditor“ ](expression/expressionadvanced.md).

   >[!CAUTION]
   >
   >Die Ausgabe eines Inhaltsentscheidungsknotens ist nur im **[!UICONTROL erweiterten Modus“]**.

1. Erweitern Sie den **[!UICONTROL Kontext]**-Knoten und navigieren Sie zu Ihrer Entscheidungsrichtlinie, um alle im [Angebotskatalogschema“ verfügbaren Attribute ](../experience-decisioning/catalogs.md#access-catalog-schema).

   ![Bedingung hinzufügen und Ausdruck bearbeiten](assets/journey-content-decision-context.png)

   >[!NOTE]
   >
   >Eine eingeschränkte Beschriftung, die für ein Attribut definiert wird, entweder in einem Journey-Erlebnisereignis, das in einer Entscheidungsregel (als Kontextdaten) oder im [Angebotsschema](../experience-decisioning/catalogs.md#access-catalog-schema) verwendet wird, führt nicht zu einem Richtlinienverstoß für die DULE oder das Einverständnis. Weitere Informationen zu Data-Governance-Richtlinien finden Sie [ diesem Abschnitt](../action/action-privacy.md)

1. Um zu überprüfen, ob für die Profile, die die Journey betreten, ein Angebot zurückgegeben wurde, verwenden Sie die [listSize](functions/functionlistsize.md) mit der folgenden Syntax: `listSize(@decision{ContentdecisionName.items})>0`

   >[!NOTE]
   >
   >In diesem Beispiel ist `Name` der Titel der Inhaltsentscheidung, die Sie Ihrem Journey hinzugefügt haben.

   ![Bedingung mit Liste hinzufügen](assets/journey-content-decision-condition-list.png)

1. Klicken Sie auf **[!UICONTROL OK]**.

1. Fügen Sie weitere Pfade hinzu, um ggf. weitere Bedingungen zu definieren.

   Sie können auch einen anderen Pfad für Profile erstellen, die die erste Bedingung nicht erfüllen, indem Sie die Option **[!UICONTROL Pfad für andere Fälle als die obigen zeigen]** aktivieren<!--These profiles will then exit the journey if no other activity is added in that path.-->

1. Speichern Sie die Aktivität Bedingung .

### In einer benutzerdefinierten Aktion {#add-custom-action}

Um die Ausgabe einer Inhaltsentscheidungsaktivität zu nutzen, können Sie eine benutzerdefinierte Aktion zu Ihrem Journey hinzufügen, in der Sie die von Ihnen definierten Angebote für ein externes System freigeben. Führen Sie dazu folgende Schritte durch.

1. Fügen Sie eine benutzerdefinierte Aktion zu Ihrem Journey hinzu. [Weitere Informationen](../action/about-custom-action-configuration.md)

1. Geben Sie einen Titel für Ihre Aktion ein.

1. Wählen **[!UICONTROL Abschnitt Anforderungsparameter]** den Parameter aus, den Sie Attributen aus den abgerufenen Angeboten zuordnen möchten.

   Klicken Sie in das bearbeitbare Textfeld und wählen Sie aus den abgerufenen Angeboten einen beliebigen Parameter aus, den Sie Attributen zuordnen möchten.

   ![Bearbeiten der Anfrageparameter der benutzerdefinierten Aktion](assets/journey-content-decision-custom-action-param.png)

1. Wechseln Sie **[!UICONTROL Popup]** Fenster, das sich öffnet, in den „Erweiterten Modus“. Erweitern Sie im [erweiterten Ausdruckseditor](expression/expressionadvanced.md) den Knoten **[!UICONTROL Kontext]**, um alle Entscheidungsrichtlinienelemente anzuzeigen.

   >[!CAUTION]
   >
   >Die Ausgabe eines Inhaltsentscheidungsknotens ist nur im **[!UICONTROL erweiterten Modus“]**.

1. Durchsuchen Sie das [Angebotskatalogschema](../experience-decisioning/catalogs.md#access-catalog-schema) mithilfe des `items`. Verwenden Sie beispielsweise die `itemName` des ersten abgerufenen Angebots und die `itemName` des zweiten abgerufenen Angebots.

   ![Anfrageparameter der benutzerdefinierten Aktion, einschließlich der Entscheidungsrichtlinie](assets/journey-content-decision-custom-action-param-ex.png)

1. Klicken Sie auf **[!UICONTROL OK]**, um Ihren Ausdruck zu speichern.

1. **[!UICONTROL Speichern]** Ihre benutzerdefinierte Aktionskonfiguration.

### Beispiel für eine vollständige Implementierung {#use-case}

Nachfolgend finden Sie ein vollständiges Beispiel für einen Journey mit einer Inhaltsentscheidungsaktivität in Kombination mit einer Bedingungsaktivität und einer benutzerdefinierten Aktion, wie oben beschrieben.

![Vollständige Journey](assets/journey-content-decision-full-journey.png)

<!--When all activities are properly configured and saved, [publish](publishing-the-journey.md) your journey.-->

Sobald die Journey [aktiviert](publishing-the-journey.md):

<!--* Profiles who enter the journey and are eligible for at least one offer are targeted by the custom action.

* If no offer is returned for a profile, they are excluded from the custom action.-->

1. Jedes Mal, wenn sich ein Profil für diese Zielgruppe qualifiziert, gelangt es auf die Journey.

1. Über die Aktivität Inhaltsentscheidung ruft [!DNL Journey Optimizer] die für jedes Profil relevanten Angebote ab.

1. Nur Profile, für die mindestens ein Angebot abgerufen wurde, setzen die Journey fort (über den Pfad „Berechtigte Profile„).

1. Wenn die Bedingung erfüllt ist, werden die entsprechenden Angebote über die benutzerdefinierte Aktion an ein externes System gesendet.