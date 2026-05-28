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
TQID: https://experienceleague.adobe.com/Saqu6Kkm1Rdym10IuwLF88Fj-hT2crAwENajyKBeY5w
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 63%

---

# Aktionen in [!DNL Adobe Campaign] v7/v8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Benutzerdefinierte Aktionen"
>abstract="Für [!DNL Adobe Campaign] v7 und v8 ist eine Integration verfügbar. Diese ermöglicht Ihnen das Senden von E-Mails, Push-Benachrichtigungen und SMS mit der Transaktionsnachrichtenfunktion von [!DNL Adobe Campaign]."

Für [!DNL Adobe Campaign] v7 und v8 ist eine Integration verfügbar. Diese ermöglicht Ihnen das Senden von E-Mails, Push-Benachrichtigungen und SMS mit der Transaktionsnachrichtenfunktion von [!DNL Adobe Campaign].

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
