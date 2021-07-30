---
title: Rangfolgeformeln erstellen
description: Erfahren Sie, wie Sie Rangfolgeformeln in Adobe Experience Platform erstellen.
feature: Angebote
topic: Integrationen
role: User
level: Intermediate
source-git-commit: 70d3bdaeec2a7a8f282b0e1a79bc751f7f837663
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 100%

---

# Rangfolgeformeln erstellen {#create-ranking-formulas}

## Grundlagen zu Rangfolgeformeln {#about-ranking-formulas}

Mithilfe von **Rangfolgeformeln** können Sie festlegen, welches Angebot für eine bestimmte Platzierung zuerst angezeigt werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Rangfolgeformeln werden in der **PQL-Syntax** angegeben und können Profil-, Kontextdaten- und Angebotsattribute nutzen. Weiterführende Informationen zur Verwendung der PQL-Syntax finden Sie im [entsprechenden Handbuch](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=de).

Nachdem eine Rangfolgenformel erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung (früher als Angebotsaktivität bezeichnet) zuweisen. Weitere Informationen dazu finden Sie unter [Auswahl der Angebote in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md).

## Erstellen einer Rangfolgeformel {#create-ranking-formula}

Gehen Sie wie folgt vor, um eine neue Rangfolgeformel zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Komponenten]** auf und wählen Sie dann die Registerkarte **[!UICONTROL Rangfolgen]**. Die Liste der zuvor erstellten Rangfolgen wird angezeigt.

   ![](../../assets/rankings-list.png)

1. Klicken Sie auf **[!UICONTROL Rangfolge erstellen]**, um eine neue Rangfolgeformel zu erstellen.

   ![](../../assets/ranking-create-formula.png)

1. Geben Sie Namen und die Beschreibung der Rangfolgeformel sowie die Formel selbst an.

   In diesem Beispiel möchten wir die Priorität aller Angebote durch Hinzufügen des Attributs „heiß“ erhöhen, wenn das Wetter heiß ist. Zu diesem Zweck wurde **contextData.weather=hot** im Entscheidungsaufruf übergeben.

   ![](../../assets/ranking-syntax.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**. Ihre Rangfolgeformel wird erstellt. Sie können sie aus der Liste auswählen, um Details abzurufen und sie zu bearbeiten oder zu löschen.

   Sie kann jetzt in einer Entscheidung verwendet werden, um die geeigneten Angebote für eine Platzierung zu reihen (siehe [Auswahl der Angebote in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)
