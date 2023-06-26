---
solution: Journey Optimizer
product: journey optimizer
title: Suchen, Filtern, Organisieren
description: Weitere Informationen zur Benutzeroberfläche von Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 0d09f7d7-d0a4-4831-90e8-8c2062de06b9
source-git-commit: 8da2b22b36a21f95a49f4195c25ccec9b055bbd6
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 100%

---

# Suchen, Filtern, Organisieren {#search-filter-organize}

## Suche{#unified-search}

Sie können auf der gesamten Benutzeroberfläche von Adobe Journey Optimizer die Adobe Experience Cloud-Suche in der Mitte der oberen Leiste verwenden, um Assets, Journeys, Datensätze und mehr in Ihren Sandboxes zu finden.

Beginnen Sie mit der Eingabe von Inhalten, um die wichtigsten Ergebnisse anzuzeigen. In den Ergebnissen werden auch Hilfeartikel zu den eingegebenen Keywords angezeigt.

![](assets/unified-search.png)

Drücken Sie die **Eingabetaste**, um auf alle Ergebnisse zuzugreifen und nach Geschäftsobjekt zu filtern.

![](assets/search-and-filter.png)

## Filterlisten{#filter-lists}

In den meisten Listen können Sie die Suchleiste verwenden, um bestimmte Elemente zu finden und Filterkriterien zu definieren.

Sie können auf die Filter zugreifen, indem Sie auf das Filtersymbol links oben in der Liste klicken. Im Filtermenü können Sie die angezeigten Elemente nach unterschiedlichen Kriterien filtern: Sie können festlegen, dass nur Elemente eines bestimmten Typs oder Status, nur von Ihnen erstellte Elemente oder nur die in den letzten 30 Tagen geänderten Elemente angezeigt werden. Die Optionen unterscheiden sich je nach Kontext.

Darüber hinaus können Sie einheitliche Tags verwenden, um eine Liste nach den einem Objekt zugewiesenen Tags zu filtern. Aktuell sind Tags für Journeys und Kampagnen verfügbar. [Erfahren Sie, wie Sie mit Tags arbeiten.](#tags)

>[!NOTE]
>
>Beachten Sie, dass angezeigte Spalten mithilfe der Konfigurationsschaltfläche oben rechts in den Listen personalisiert werden können. Die Personalisierung wird für jeden Benutzer individuell gespeichert.

In den Listen können Sie für jedes Element grundlegende Aktionen durchführen. Sie können Elemente beispielsweise duplizieren oder löschen.

![](assets/journey4.png)

## Arbeiten mit einheitlichen Tags {#tags}

Mit [einheitlichen Adobe Experience Platform-Tags](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=de) können Sie Ihre Journey Optimizer-Journeys und -Kampagnen einfach klassifizieren, um die Suche über Listen zu verbessern.

>[!AVAILABILITY]
>
>Einheitliche Tags befinden sich derzeit in der Betaversion. Dokumentation und Funktionalitäten können sich ändern.

### Hinzufügen von Tags zu einem Objekt

Über das Feld **Tags** in den [Journey](../building-journeys/journey-gs.md#change-properties)- oder [Kampagnen](../campaigns/create-campaign.md#create)-Eigenschaften können Sie Tags für Ihr Objekt definieren. Sie können entweder ein vorhandenes Tag auswählen oder ein neues erstellen.

Geben Sie den Anfang des Namens des gewünschten Tags ein und wählen Sie es aus der Liste aus. Wenn es nicht verfügbar ist, klicken Sie auf **Erstellen**, um ein neues zu erstellen und hinzuzufügen. Sie können beliebig viele Tags definieren.

![](assets/tags1.png)

Die Liste der definierten Tags wird unter dem Feld **Tags** angezeigt.

>[!NOTE]
>
> Bei Tags wird die Groß-/Kleinschreibung nicht beachtet.
> 
> Wenn Sie eine Journey duplizieren oder eine neue Version einer Journey bzw. Kampagne erstellen, bleiben Tags erhalten.

### Filtern nach Tags

In den Journey- und Kampagnenlisten wird eine spezielle Spalte angezeigt, sodass Sie Ihre Tags einfach visualisieren können.

Es ist auch ein Filter verfügbar, um nur Journeys oder Kampagnen mit bestimmten Tags anzuzeigen.

![](assets/tags2.png)

Sie können Tags zu beliebigen Typen von Journeys oder Kampagnen (Live, Entwurf usw.) hinzufügen oder daraus entfernen. Klicken Sie hierzu auf das Symbol **Mehr Aktionen** neben dem Objekt und wählen Sie **Tags bearbeiten** aus.

![](assets/tags3.png)

### Verwalten von Tags

Admins können Tags löschen und mithilfe des Menüs **Tags** unter **ADMINISTRATION** nach Kategorien organisieren. Weitere Informationen über die Verwaltung von Tags finden Sie in der [Dokumentation zu einheitlichen Tags](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/ui/managing-tags.html?lang=de).

>[!NOTE]
>
> Direkt über das Feld **[!UICONTROL Tags]** in Journey Optimizer erstellte Tags werden automatisch der integrierten Kategorie „Nicht kategorisiert“ hinzugefügt.
