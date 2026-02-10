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
version: Journey Orchestration
source-git-commit: 339285cbc82d5b30b221feb235ed8425a66f8802
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 46%

---

# [!DNL Adobe Campaign] v7/v8-Aktionen {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Benutzerdefinierte Aktionen"
>abstract="Eine Integration ist verfügbar, wenn Sie über [!DNL Adobe Campaign] v7 oder v8 verfügen. Sie ermöglicht den Versand von E-Mails, Push-Benachrichtigungen und SMS mit [!DNL Adobe Campaign] Transaktionsnachrichten-Funktionen."

Eine Integration ist verfügbar, wenn Sie über [!DNL Adobe Campaign] v7 oder v8 verfügen. Sie ermöglicht den Versand von E-Mails, Push-Benachrichtigungen und SMS mit [!DNL Adobe Campaign] Transaktionsnachrichten-Funktionen.

Die Verbindung zwischen der Journey Optimizer- und der Campaign-Instanz wird bei der Bereitstellung von Adobe hergestellt. Kontaktieren Sie diesbezüglich Adobe.

**Verwendungszeitpunkt**: Verwenden Sie Campaign v7/v8-Aktionen, wenn Ihr Messaging auf Campaign-Transaktionsvorlagen, kampagnenspezifischen Datenmodellen oder vorhandenen Versand-Workflows von Campaign basiert.

**Voraussetzungen**

* Ihre [!DNL Adobe Campaign] v7/v8-Instanz wird von Adobe bereitgestellt und mit Journey Optimizer verbunden.
* Sie haben Zugriff auf Campaign-Transaktionsnachrichten und die erforderlichen Berechtigungen.

Damit dies funktioniert, müssen Sie eine dedizierte Aktion konfigurieren. Siehe diesen [Abschnitt](../action/acc-action.md).

In diesem [Abschnitt](../building-journeys/ajo-ac.md) wird ein Anwendungsfall schrittweise beschrieben.

1. Beginnen Sie bei der Erstellung Ihrer Journey mit einem Ereignis. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/journey.md).
1. Wählen Sie im Abschnitt **Aktion** der Palette eine Campaign-Aktion aus und fügen Sie sie zu Ihrer Journey hinzu.
1. Unter **Aktionsparameter** werden alle Felder angezeigt, die in der Nachrichten-Payload erwartet werden. Sie müssen jedes dieser Felder entweder im Ereignis oder der Datenquelle dem zu verwendenden Feld zuordnen. Dies ähnelt benutzerdefinierten Aktionen. Siehe diesen [Abschnitt](../building-journeys/using-custom-actions.md).

>[!NOTE]
>
>* Campaign v7/v8-Aktionen können zusammen mit nativen Kanalaktionen auf derselben Journey verwendet werden. Dies gilt nicht für Campaign Standard-Aktionen. Siehe [Leitplanken für Kampagnenaktivitäten](../start/guardrails.md#ac-g).
>* Campaign v7/v8-Aktionen können nicht mit Aktivitäten vom Typ „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ verwendet werden. Weitere Informationen finden Sie auf der Seite Leitplanken unter Lesen von Leitplanken für Zielgruppen- und Zielgruppen-Qualifizierung .

![[!DNL Adobe Campaign] v7/v8-Aktionskonfiguration und Integrationseinstellungen](assets/accintegration2.png)
