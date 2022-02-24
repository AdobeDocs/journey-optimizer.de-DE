---
title: Arbeiten mit gespeicherten Ausdrücken
description: Erfahren Sie, wie Sie mit gespeicherten Ausdrücken aus dem [!DNL Journey Optimizer] -Bibliothek.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 163211f95436a37dee7deffea9ced1a3fa09dc34
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Arbeiten mit gespeicherten Ausdrücken {#expression-library}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Über die Ausdrucksbibliothek"
>abstract="[!DNL Journey Optimizer] bietet eine Bibliothek, in der Sie auf gespeicherte Personalisierungsausdrücke zugreifen können, die von Admin-Benutzern konfiguriert wurden. "

[!DNL Journey Optimizer] bietet eine Bibliothek, in der Sie auf zuvor gespeicherte Personalisierungsausdrücke zugreifen können, die von Admin-Benutzern hinzugefügt wurden.

1. Um auf die gespeicherten Ausdrücke zuzugreifen, klicken Sie auf die **[!UICONTROL Bibliothek]** im linken Bereich. Die Liste enthält alle Ausdrücke, die von Admin-Benutzern gespeichert wurden (siehe [Speichern von Ausdrücken in der Bibliothek](#save-expressions)).

   >[!NOTE]
   >
   >Über die Infoschaltfläche erhalten Sie weitere Informationen zum Inhalt eines gespeicherten Ausdrucks. Wenn Sie über die entsprechenden Berechtigungen zum Verwalten von Bibliothekselementen verfügen, wird die Informationsschaltfläche im Menü mit Auslassungspunkten angezeigt.

   ![](assets/library-list.png)

1. Klicken Sie auf + , um den Ausdruck in den Editor einzufügen. Anschließend können Sie Ihren Personalisierungsinhalt wie gewohnt anpassen und validieren. [Weitere Informationen](../personalization/personalization-build-expressions.md)

   ![](assets/library-add.png)

## Speichern eines Ausdrucks in der Bibliothek {#save-expressions}

[!DNL Journey Optimizer] ermöglicht es Admin-Benutzern, Personalisierungsausdrücke in der Bibliothek zu speichern. Diese Ausdrücke stehen dann allen Benutzern zur Verfügung, um Personalisierungsinhalte zu erstellen.

Gehen Sie wie folgt vor, um einen Ausdruck in der Bibliothek zu speichern:

1. Erstellen Sie in der Editor-Oberfläche den Ausdruck und klicken Sie auf **[!UICONTROL Bibliothek hinzufügen]**.

   >[!NOTE]
   >
   >Wenn die Schaltfläche nicht sichtbar ist, überprüfen Sie in der Admin Console, dass Sie über die erforderlichen Berechtigungen verfügen (siehe [Berechtigungsebenen](../administration/high-low-permissions.md)).

   ![](assets/library-save.png)

1. Geben Sie im rechten Bereich einen Titel und eine Beschreibung für den Ausdruck ein, damit Benutzer ihn leichter finden können. Klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

   ![](assets/add-expression.png)

1. Der Ausdruck wird der Bibliothek hinzugefügt. Benutzer können sie nun verwenden, um ihren Personalisierungsinhalt zu erstellen.


>[!NOTE]
>
>* Sie speichern bis zu 40 Ausdrücke in der Bibliothek.
>
>* Ausdrücke dürfen 200 KB nicht überschreiten.
>
>* Gespeicherte Ausdrücke werden nach Erstellungsdatum sortiert: Der kürzlich hinzugefügte Ausdruck wird zuerst in der Liste angezeigt.



Um einen vorhandenen Ausdruck zu bearbeiten, fügen Sie ihn zum Editor hinzu und ändern Sie ihn dann entsprechend Ihren Anforderungen. Klicken **[!UICONTROL Bibliothek hinzufügen]** , um die Syntax zu überprüfen und den Ausdruck zu speichern.

Um einen Ausdruck zu löschen, klicken Sie auf die Schaltfläche mit den Auslassungszeichen und anschließend auf **[!UICONTROL Löschen]**.
