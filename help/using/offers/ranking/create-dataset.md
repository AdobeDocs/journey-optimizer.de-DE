---
product: experience platform
solution: Experience Platform
title: Erstellen eines Datensatzes zum Erfassen von Ereignissen
description: Erfahren Sie, wie Sie einen Datensatz erstellen, um Ereignisse zu erfassen.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 17d37da6e6325d36df0f63122fa37f416e3f2c4c
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 100%

---

# Erstellen eines Datensatzes zum Erfassen von Ereignissen {#create-dataset}

Bevor Sie ein KI-Modell erstellen, müssen Sie einen Datensatz erstellen, in dem Konversionsereignisse erfasst werden. Erstellen Sie zunächst das Schema, das in Ihrem Datensatz verwendet werden soll:

1. Wählen Sie im Menü **[!UICONTROL Daten-Management]** die Option **[!UICONTROL Schema]** aus, wechseln Sie zur Registerkarte **[!UICONTROL Durchsuchen]** und klicken Sie auf **[!UICONTROL Schema erstellen]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Wählen Sie **[!UICONTROL XDM ExperienceEvent]** aus.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    Weitere Informationen zu XDM-Schemas und Feldergruppen finden Sie in der [Dokumentation zur XDM-Systemübersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de).


1. Geben Sie im Feld **[!UICONTROL Suche]** „Interaktion mit Vorschlägen“ ein und wählen Sie die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** aus.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    Mit dem Schema, das in Ihrem Datensatz verwendet wird, muss die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** verknüpft sein. Andernfalls können Sie es nicht in Ihrer Rangfolgestrategie verwenden.

1. Klicken Sie auf **[!UICONTROL Feldergruppen hinzufügen]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Die Feldergruppen wurden früher als Mixins bezeichnet.

1. Geben Sie einen Namen ein und speichern Sie das Schema.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    Erfahren Sie mehr über das Erstellen von Schemas in [Grundlagen der Schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de#understanding-schemas).

Sie können jetzt einen Datensatz unter Verwendung dieses Schemas erstellen. Gehen Sie dazu wie folgt vor:

1. Wählen Sie im Menü **[!UICONTROL Daten-Management]** die Option **[!UICONTROL Datensätze]** aus, wechseln Sie zur Registerkarte **[!UICONTROL Durchsuchen]** und klicken Sie auf **[!UICONTROL Datensatz erstellen]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Wählen Sie **[!UICONTROL Datensatz aus Schema erstellen]** aus.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Wählen Sie das soeben erstellte Schema aus der Liste aus.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Klicken Sie auf **[!UICONTROL Weiter]**.

1. Geben Sie im Feld **[!UICONTROL Name]** einen eindeutigen Namen für den Datensatz ein und klicken Sie auf **[!UICONTROL Beenden]**.

   ![](../assets/ai-ranking-dataset-name.png)

Der Datensatz kann jetzt ausgewählt werden, um Ereignisdaten zu erfassen, wenn [eine Rangfolgestrategie erstellt wird](#create-ranking-strategy).
