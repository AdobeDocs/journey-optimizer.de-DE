---
title: Erstellen von Ranking-Formeln
description: Erfahren Sie, wie Sie in Adobe Experience Platform Ranking-Formeln erstellen.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Erstellen von Ranking-Formeln {#create-ranking-formulas}

## Grundlagen zu Ranking-Formeln {#about-ranking-formulas}

**Mithilfe von** Ranking-Formeln können Sie festlegen, welches Angebot für eine bestimmte Platzierung zuerst angezeigt werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Ranking-Formeln werden in **PQL-Syntax** angegeben und können Profil-, Kontextdaten- und Angebot-Attribute nutzen. Weitere Informationen zur Verwendung der PQL-Syntax finden Sie in der [dedizierten Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

Nachdem eine Ranking-Formel erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung zuweisen (früher als Angebot-Aktivität bezeichnet). Weitere Informationen hierzu finden Sie unter [Auswahl der Angebot in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md).

## Erstellen einer Rangformel {#create-ranking-formula}

Gehen Sie wie folgt vor, um eine Rangformel zu erstellen:

* Rufen Sie das Menü **[!UICONTROL Komponenten]** auf und wählen Sie dann die Registerkarte **[!UICONTROL Rankings]**.

* Klicken Sie auf **[!UICONTROL Formel]** erstellen, um eine neue Rangformel zu erstellen.

   ![](../assets/ranking-create-formula.png)

* Geben Sie den Namen, die Beschreibung und die Formel der Rangformel an.

   In diesem Beispiel möchten wir die Priorität aller Angebot mit dem Attribut &quot;heiß&quot;erhöhen, wenn das Wetter heiß ist. Zu diesem Zweck wurde **contextData.weather=hot** im Entscheidungsaufruf übergeben.

   ![](../assets/ranking-syntax.png)

* Klicken Sie auf **[!UICONTROL Speichern]**. Ihre Rangformel wird erstellt. Sie können sie aus der Liste auswählen, um Details abzurufen und sie zu bearbeiten oder zu löschen.

   Es kann jetzt in einer Entscheidung verwendet werden, um förderfähige Angebot für eine Platzierung einzustufen (siehe [Auswahl der Angebote in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md)).

   ![](../assets/ranking-formula-created.png)
