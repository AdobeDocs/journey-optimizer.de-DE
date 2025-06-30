---
product: experience platform
solution: Experience Platform
title: Erstellen eines Datensatzes zum Erfassen von Ereignissen
description: Erfahren Sie, wie Sie einen Datensatz erstellen, um Ereignisse zu erfassen.
badge: label="Veraltet" type="Informative"
feature: Ranking, Decision Management, Datasets
role: Data Engineer, Developer
level: Experienced
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 91%

---

# Erstellen eines Datensatzes zum Erfassen von Ereignissen {#create-dataset}

Um Erlebnisereignisse zu erfassen, müssen Sie zunächst einen Datensatz erstellen, in dem diese Ereignisse gesendet werden.

Erstellen Sie zunächst das Schema, das in Ihrem Datensatz verwendet werden soll:

1. Wählen Sie im Menü **[!UICONTROL Daten-Management]** die Option **[!UICONTROL Schema]** aus.

1. Klicken Sie auf **[!UICONTROL Schema erstellen]**, wählen Sie oben rechts die Option **[!UICONTROL Erlebnisereignis]** aus und klicken Sie auf **Weiter**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Weitere Informationen zu XDM-Schemata und Feldergruppen sind in der [Dokumentation zur XDM-Systemübersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"} verfügbar.

1. Geben Sie einen Namen und eine Beschreibung für Ihr Schema ein und klicken Sie auf **Beenden**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. Wählen Sie im Abschnitt **[!UICONTROL Feldergruppen]** auf der linken Seite **[!UICONTROL Hinzufügen]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. Geben Sie im Feld **[!UICONTROL Suche]** „Interaktion mit Vorschlägen“ ein.

1. Wählen Sie die Feldergruppe **[!UICONTROL Erlebnisereignis – Interaktionen mit Vorschlägen]** und klicken Sie auf **[!UICONTROL Feldergruppen hinzufügen]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >Mit dem Schema, das in Ihrem Datensatz verwendet wird, muss die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** verknüpft sein. Andernfalls können Sie es nicht in Ihrem KI-Modell verwenden.

1. Speichern Sie das Schema.

>[!NOTE]
>
>Erfahren Sie mehr über das Erstellen von Schemas in [Grundlagen der Schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de#understanding-schemas){target="_blank"}.

Sie können jetzt einen Datensatz mit diesem Schema erstellen. Gehen Sie dazu wie folgt vor:

1. Wählen Sie aus dem Menü **[!UICONTROL Daten-Management]** die Option **[!UICONTROL Datensätze]** aus und navigieren Sie zur Registerkarte **[!UICONTROL Durchsuchen]**.

1. Klicken Sie auf **[!UICONTROL Datensatz erstellen]** und wählen Sie **[!UICONTROL Datensatz aus Schema erstellen]** aus.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Wählen Sie das soeben erstellte Schema aus der Liste aus und klicken Sie auf **[!UICONTROL Weiter]**.

1. Geben Sie im Feld **[!UICONTROL Name]** einen eindeutigen Namen für den Datensatz ein und klicken Sie auf **[!UICONTROL Beenden]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Der Datensatz kann jetzt ausgewählt werden, um Ereignisdaten zu erfassen, wenn [ein KI-Modell erstellt wird](../ranking/create-ranking-strategies.md).
