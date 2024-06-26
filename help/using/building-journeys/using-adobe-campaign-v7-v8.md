---
solution: Journey Optimizer
product: journey optimizer
title: Aktionen in Adobe Campaign v7/v8
description: Erfahren Sie mehr über Aktionen in Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: Journey, Integration, Campaign, v7, v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 100%

---

# Aktionen in Adobe Campaign v7/v8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Benutzerdefinierte Aktionen"
>abstract="Für Adobe Campaign v7 und v8 ist eine Integration verfügbar. Sie ermöglicht Ihnen das Senden von E-Mails, Push-Benachrichtigungen und SMS mit der Transaktionsnachrichtenfunktion von Adobe Campaign."

Für Adobe Campaign v7 und v8 ist eine Integration verfügbar. Diese ermöglicht Ihnen das Senden von E-Mails, Push-Benachrichtigungen und SMS mit der Transaktionsnachrichtenfunktion von Adobe Campaign.

Die Verbindung zwischen der Journey Optimizer- und der Campaign-Instanz wird bei der Bereitstellung von Adobe hergestellt. Kontaktieren Sie diesbezüglich Adobe.

Damit dies funktioniert, müssen Sie eine dedizierte Aktion konfigurieren. Siehe diesen [Abschnitt](../action/acc-action.md).

In diesem [Abschnitt](../building-journeys/ajo-ac.md) wird ein Anwendungsfall schrittweise beschrieben.

1. Beginnen Sie bei der Erstellung Ihrer Journey mit einem Ereignis. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/journey.md).
1. Wählen Sie im Abschnitt **Aktion** der Palette eine Campaign-Aktion aus und fügen Sie sie zu Ihrer Journey hinzu.
1. Unter **Aktionsparameter** werden alle Felder angezeigt, die in der Nachrichten-Payload erwartet werden. Sie müssen jedes dieser Felder entweder im Ereignis oder der Datenquelle dem zu verwendenden Feld zuordnen. Dies ähnelt benutzerdefinierten Aktionen. Siehe diesen [Abschnitt](../building-journeys/using-custom-actions.md).

![](assets/accintegration2.png)
