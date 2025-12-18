---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erstellen von Sammlungen
description: Erfahren Sie, wie Sie Angebote mithilfe von Sammlungen ordnen
badge: label="Legacy" type="Informative"
feature: Decision Management, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Erstellen von Sammlungen {#create-collections}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="Über Angebotssammlungen"
>abstract="Mit Angebotssammlungen können Sie Ihre Angebote organisieren, indem Sie sie in Kategorien Ihrer Wahl anordnen."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic"
>title="Dynamische Sammlung"
>abstract="Verwenden Sie Sammlungskennzeichner, um Angebote dynamisch für eine Sammlung zu qualifizieren."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static"
>title="Statische Sammlung"
>abstract="Wählen Sie Angebote manuell aus und gruppieren Sie sie mithilfe von Kriterien wie Status, Sammlungskennzeichner, Datum und Kanal."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static_select"
>title="Vorschau der statischen Sammlung"
>abstract="Statische Sammlungen werden durch das manuelle Auswählen einzelner Angebote erstellt, die in die Sammlung aufgenommen werden sollen. Eine solche Sammlung kann nur aktualisiert werden, indem ihr manuell weitere Angebote hinzufügt werden."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic_select"
>title="Vorschau der dynamischen Sammlung"
>abstract="Dynamische Sammlungen erfassen Angebote basierend auf Sammlungskennzeichnern.  Diese Sammlungen werden automatisch aktualisiert. Wenn beispielsweise ein neues Angebot mit dem Sammlungskennzeichner „Sport“ erstellt wird, wird es automatisch der entsprechenden Sammlung hinzugefügt."

Mit Sammlungen können Sie Ihre Angebote organisieren, indem Sie sie in Kategorien Ihrer Wahl anordnen. Sie können beispielsweise eine „Sport“-Sammlung erstellen, die nur sportbezogene Angebote enthält.

➡️ [Funktion im Video kennenlernen](#video).

Die Liste der Angebotssammlungen ist im Menü **[!UICONTROL Angebote]** verfügbar.

![](../assets/collections_list.png)

Sie können zwei Arten von Sammlungen erstellen:

* **Dynamische Sammlungen** sind Sammlungen von Angeboten, die auf Sammlungsqualifizierern (ehemals als „Tags“ bezeichnet) basieren. Diese Sammlungen werden automatisch aktualisiert. Wenn beispielsweise ein neues Angebot mit dem ausgewählten Sammlungsqualifizierer erstellt wird, wird es automatisch der Sammlung hinzugefügt.

* **Statische Kollektionen** sind Sammlungen, die durch manuelles Auswählen einzelner Angebote erstellt werden, die in die Kollektion aufgenommen werden sollen. Eine solche Sammlung kann nur aktualisiert werden, indem ihr manuell weitere Angebote hinzufügt werden.

Gehen Sie wie folgt vor, um eine Sammlung zu erstellen:

1. Gehen Sie zur Registerkarte **[!UICONTROL Sammlungen]** und klicken Sie dann auf **[!UICONTROL Sammlung erstellen]**.

1. Geben Sie den Namen und den Typ der zu erstellenden Sammlung an.

   ![](../assets/collection_create.png)

1. Um eine dynamische Sammlung zu erstellen, wählen Sie im linken Bereich den Sammlungsqualifizierer der Angebote aus, die der Sammlung hinzugefügt werden sollen, und klicken Sie dann auf **[!UICONTROL Speichern]**. Alle Angebote mit dem ausgewählten Sammlungsqualifizierer werden in der Sammlung gespeichert.

   Weiterführende Informationen zur Erstellung von Sammlungsqualifizierern finden Sie unter [Erstellen von Sammlungsqualifizierern](../offer-library/creating-tags.md).

   ![](../assets/dynamic_collection.png)

1. Um eine statische Sammlung zu erstellen, verwenden Sie den linken Bereich zum Filtern der Liste der Angebote (nach Status, Sammlungsqualifizierer, Datum, Kanal, Inhaltstyp) und wählen Sie dann die Angebote aus, die der Sammlung hinzugefügt werden sollen.

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >Statische Sammlungen werden nicht automatisch aktualisiert. Um einer statischen Sammlung Angebote hinzuzufügen, müssen Sie sie bearbeiten und die Angebote manuell hinzufügen.

1. Um einer statischen Sammlung benutzerdefinierte oder Core-Datennutzungs-Labels zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]**. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (Object Level Access Control, OLAC)](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >Die Verwendung von OLAC ist für dynamische Sammlungen nicht verfügbar. Sie muss auf Angebotsebene verwaltet werden. Daher ist es möglich, dass in einer dynamischen Sammlung keine Angebote angezeigt werden, wenn Sie auf keines dieser Angebote Zugriff haben.

1. Nachdem die Sammlung erstellt wurde, wird sie in der Liste angezeigt. Sie können sie zum Bearbeiten oder Löschen auswählen.

   ![](../assets/collection_created.png)

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3411812?captions=ger&quality=12)


