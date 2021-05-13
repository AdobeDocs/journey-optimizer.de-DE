---
title: Erstellen von Rangfolgeformeln
description: Erfahren Sie, wie Sie Rangfolgeformeln in Adobe Experience Platform erstellen.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 72%

---

# Erstellen von Rangfolgeformeln {#create-ranking-formulas}

## Grundlagen zu Rangfolgeformeln {#about-ranking-formulas}

Mithilfe von **Rangfolgeformeln** können Sie festlegen, welches Angebot für eine bestimmte Platzierung zuerst angezeigt werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Rangfolgeformeln werden in der **PQL-Syntax** angegeben und können Profil-, Kontextdaten- und Angebotsattribute nutzen. Weiterführende Informationen zur Verwendung der PQL-Syntax finden Sie im [entsprechenden Handbuch](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=de).

Nachdem eine Ranking-Formel erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung zuweisen (früher als Angebot-Aktivität bezeichnet). Weitere Informationen hierzu finden Sie unter [Auswahl der Angebot in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md).

## Erstellen einer Rangfolgeformel {#create-ranking-formula}

Gehen Sie wie folgt vor, um eine neue Rangfolgeformel zu erstellen:

* Rufen Sie das Menü **[!UICONTROL Komponenten]** auf und wählen Sie dann die Registerkarte **[!UICONTROL Rankings]**.

* Klicken Sie auf **[!UICONTROL Formel erstellen]**, um eine neue Rangfolgeformel zu erstellen.

   ![](../../assets/ranking-create-formula.png)

* Geben Sie Namen und die Beschreibung der Rangfolgeformel sowie die Formel selbst an.

   In diesem Beispiel möchten wir die Priorität aller Angebote durch Hinzufügen des Attributs „heiß“ erhöhen, wenn das Wetter heiß ist. Zu diesem Zweck wurde **contextData.weather=hot** im Entscheidungsaufruf übergeben.

   ![](../../assets/ranking-syntax.png)

* Klicken Sie auf **[!UICONTROL Speichern]**. Ihre Rangfolgeformel wird erstellt. Sie können sie aus der Liste auswählen, um Details abzurufen und sie zu bearbeiten oder zu löschen.

   Es kann jetzt in einer Entscheidung verwendet werden, um förderfähige Angebot für eine Platzierung einzustufen (siehe [Auswahl der Angebote in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)
