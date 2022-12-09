---
solution: Journey Optimizer
product: journey optimizer
title: Journeys konfigurieren
description: Erfahren Sie, wie Sie Data Sources, Ereignisse und Aktionen konfigurieren.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Journeys konfigurieren {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="Informationen zur Journey-Konfiguration"
>abstract="Um Nachrichten mit Journeys zu senden, müssen Sie Datenquellen, Ereignisse und Aktionen konfigurieren. Mit Datenquellen können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden, z. B. in Ihren Bedingungen. Ereignisse ermöglichen es Ihnen, Ihre Journeys beim Empfang eines Ereignisses auszulösen. Mit benutzerdefinierten Aktionen können Sie eine Verbindung zu einem Drittanbietersystem herstellen, um Ihre Nachrichten zu senden. Wenn Sie die integrierten Nachrichtenfunktionen von Journey Optimizer verwenden, müssen Sie keine Aktion konfigurieren."

Um Nachrichten mit Journeys senden zu können, müssen Sie **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** und **[!UICONTROL Actions]**.

![](assets/admin-menu.png)

## Data Sources {#data-sources}

Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden. [Weitere Infos](../../using/datasource/about-data-sources.md)

## Veranstaltungen {#events}

Ereignisse ermöglichen es Ihnen, Ihre Journeys unregelmäßig auszulösen, um in Echtzeit Nachrichten an den Kontakt zu senden, der in die Journey gelangt.

In der Ereigniskonfiguration konfigurieren Sie die Ereignisse, die in den Journeys erwartet werden. Die Daten der eingehenden Ereignisse werden nach dem Adobe Experience-Datenmodell (XDM) normalisiert. Ereignisse stammen aus Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). [Weitere Infos](../../using/event/about-events.md)

## Aktionen {#actions}

Die Funktionen von Journey Optimizer-Nachrichten sind integriert: Sie müssen Ihrer Journey nur eine Kanalaktionsaktivität hinzufügen. Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. [Weitere Infos](../../using/action/action.md)

## Durchsuchen von Adobe Experience Platform-Feldern {#friendly-names-display}

Bei der Definition [Ereignis-Payload](../event/about-creating.md#define-the-payload-fields), [Feldgruppen-Payload](../datasource/configure-data-sources.md#define-field-groups) und wählen Sie die Felder im [Ausdruckseditor](../building-journeys/expression/expressionadvanced.md), wird der Anzeigename zusätzlich zum Feldnamen angezeigt. Diese Informationen werden aus der Schemadefinition im Experience-Datenmodell abgerufen.

Wenn beim Einrichten von Schemas Deskriptoren wie &quot;xdm:alternateDisplayInfo&quot;angegeben werden, ersetzen die benutzerfreundlichen Namen die Anzeigenamen. Dies ist besonders bei der Arbeit mit &quot;eVars&quot;und allgemeinen Feldern nützlich. Sie können Deskriptoren für Anzeigenamen über einen API-Aufruf konfigurieren. Weitere Informationen finden Sie unter [Entwicklerhandbuch zur Schema Registry](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target=&quot;_blank&quot;}.

![](assets/xdm-from-descriptors.png)

Wenn ein benutzerfreundlicher Name verfügbar ist, wird das Feld als `<friendly-name>(<name>)`. Wenn kein benutzerfreundlicher Name verfügbar ist, wird der Anzeigename angezeigt, z. B. `<display-name>(<name>)`. Wenn keiner von ihnen definiert ist, wird nur der technische Name des Felds angezeigt `<name>`.

>[!NOTE]
>
>Benutzerfreundliche Namen werden nicht abgerufen, wenn Sie Felder aus einer Vereinigung von Schemas auswählen.
