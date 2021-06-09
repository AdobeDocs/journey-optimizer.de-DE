---
title: Erstellen von Rangfolgeformeln
description: Erfahren Sie, wie Sie Rangfolgeformeln in Adobe Experience Platform erstellen.
source-git-commit: ea8a3644ecef911a14ea087b03d367976f0c898d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Erstellen von Rangfolgeformeln {#create-ranking-formulas}

## Grundlagen zu Rangfolgeformeln {#about-ranking-formulas}

Mithilfe von **Rangfolgeformeln** können Sie festlegen, welches Angebot für eine bestimmte Platzierung zuerst angezeigt werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Rangfolgeformeln werden in der **PQL-Syntax** angegeben und können Profil-, Kontextdaten- und Angebotsattribute nutzen. Weiterführende Informationen zur Verwendung der PQL-Syntax finden Sie im [entsprechenden Handbuch](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=de).

Sobald eine Rangfolgenformel erstellt wurde, können Sie diese einer Platzierung in einem Angebot (früher Angebotsaktivität) zuweisen. Weitere Informationen finden Sie unter [Auswahl der Angebote in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md).

## Erstellen einer Rangfolgeformel {#create-ranking-formula}

Gehen Sie wie folgt vor, um eine neue Rangfolgeformel zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Komponenten]** auf und wählen Sie dann die Registerkarte **[!UICONTROL Rangfolgen.]** Die Liste der zuvor erstellten Ranglisten wird angezeigt.

   ![](../../assets/rankings-list.png)

1. Klicken Sie auf **[!UICONTROL Rang erstellen]** , um eine neue Rangliste zu erstellen.

   ![](../../assets/ranking-create-formula.png)

1. Geben Sie Namen und die Beschreibung der Rangfolgeformel sowie die Formel selbst an.

   In diesem Beispiel möchten wir die Priorität aller Angebote durch Hinzufügen des Attributs „heiß“ erhöhen, wenn das Wetter heiß ist. Zu diesem Zweck wurde **contextData.weather=hot** im Entscheidungsaufruf übergeben.

   ![](../../assets/ranking-syntax.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**. Ihre Rangfolgeformel wird erstellt. Sie können sie aus der Liste auswählen, um Details abzurufen und sie zu bearbeiten oder zu löschen.

   Sie kann jetzt für eine Entscheidung verwendet werden, um die geeigneten Angebote für eine Platzierung zu sortieren (siehe [Auswahl der Angebote in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)
