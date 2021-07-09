---
title: Administration und Einstellungen
description: Erfahren Sie mehr über Richtlinien zu Administration und Einstellungen
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Anwendungskonfiguration
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 88%

---

# Konfigurieren von Journeys

Um Nachrichten mit Journeys zu senden, müssen Sie **[!UICONTROL Datenquellen]**, **[!UICONTROL Ereignisse]** und **[!UICONTROL Aktionen]** konfigurieren.

![](../assets/admin-menu.png)

## Datenquellen

Mit der Konfiguration von Datenquellen können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung in Ihren Journeys abzurufen. [Weitere Informationen](../../using/datasource/about-data-sources.md)

## Ereignisse

Mit Hilfe von Ereignissen können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten.

In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). [Weitere Informationen](../../using/event/about-events.md)

## Aktionen

Journey Optimizer verfügt über integrierte Nachrichtenfunktionen. Sie müssen nur den Inhalt gestalten und Ihre Nachricht veröffentlichen. Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. [Weitere Informationen](../../using/action/action.md)

## Durchsuchen von Adobe Experience Platform-Feldern {#friendly-names-display}

Bei der Definition von [Ereignis-Payload](../event/about-creating.md#define-the-payload-fields), [Feldergruppen-Payload](../datasource/configure-data-sources.md#define-field-groups) und der Auswahl von Feldern im [Ausdruckseditor](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=de){target=&quot;_blank&quot;} wird der Anzeigename zusätzlich zum Feldnamen angezeigt. Diese Informationen werden aus der Schemadefinition im Experience-Datenmodell abgerufen.

Wenn beim Einrichten von Schemata Deskriptoren wie „xdm:alternateDisplayInfo“ angegeben werden, werden die Anzeigenamen durch benutzerfreundliche Namen ersetzt. Dies ist besonders beim Arbeiten mit „eVars“und generischen Feldern nützlich. Sie können die Deskriptoren für benutzerfreundliche Namen über einen API-Aufruf konfigurieren. Weitere Informationen finden Sie im [Entwicklerhandbuch zur Schema Registry](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=de){target=&quot;_blank&quot;}.

![](../assets/xdm-from-descriptors.png)

Wenn ein benutzerfreundlicher Name verfügbar ist, wird das Feld als `<friendly-name>(<name>)` angezeigt. Ist kein benutzerfreundlicher Name verfügbar, wird der Anzeigename angezeigt, z. B. `<display-name>(<name>)`. Wenn keiner der Namen definiert ist, wird nur der technische Name des Felds `<name>` angezeigt.

>[!NOTE]
>
>Benutzerfreundliche Namen werden nicht abgerufen, wenn Sie Felder aus einer Vereinigungsmenge von Schemas auswählen.