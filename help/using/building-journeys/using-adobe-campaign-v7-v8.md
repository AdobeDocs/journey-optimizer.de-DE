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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 24%

---

# Aktionen in [!DNL Adobe Campaign] v7/v8 {#using_campaign_v7-v8}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mit der Integration von Adobe Campaign v7 und v8 E-Mails, Push-Benachrichtigungen und SMS von Ihren Journey-Mitgliedern über Transaktionsnachrichten in Campaign senden können.

>[!ENDSHADEBOX]

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

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird erläutert, wie Sie Adobe Campaign v7/v8 als Aktion in Journey Optimizer Journey verwenden können, um E-Mails, Push-Benachrichtigungen und SMS über Transaktionsnachrichten in Campaign zu senden.

**intents:**

* Hinzufügen einer Campaign v7/v8-Aktion zu einer Journey, um Transaktionsnachrichten zu senden
* Journey-Ereignis- oder Datenquellenfelder den Payload-Parametern der Campaign-Nachricht zuordnen
* Campaign v7/v8-Aktionen mit nativen Journey Optimizer-Kanalaktionen auf derselben Journey kombinieren
* Konfigurieren der dedizierten Aktion, die für die Integration von Campaign v7/v8 erforderlich ist

**Glossar:**

* **Transaktionsnachrichten in Campaign**: Funktion von Adobe Campaign v7/v8 zum Senden von ausgelösten Nachrichten (E-Mail, SMS, Push) über eine dedizierte Aktion, die in Journey Optimizer *integriert ist (produktspezifisch)*
* **Aktionsparameter**: Felder im Journey-Aktivitätsbereich, die Journey-Daten der erwarteten Campaign-Nachrichten-Payload zuordnen *(produktspezifisch)*

**Leitplanken:**

* Die Verbindung zwischen Journey Optimizer und der Campaign-Instanz wird von Adobe zur Bereitstellungszeit eingerichtet. Wenden Sie sich an Adobe, um sie zu aktivieren.
* Es muss eine dedizierte Aktion konfiguriert werden, bevor Campaign v7/v8-Aktionen in der Journey-Palette verfügbar sind.
* Campaign v7/v8-Aktionen können nicht mit Aktivitäten vom Typ „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ verwendet werden.
* Voraussetzungen sind der Zugriff auf Campaign-Transaktionsnachrichten und die erforderlichen Berechtigungen in Campaign.

**Terminologie:**

* Kanonischer Name: Adobe Campaign v7/v8 — Akronym: ACC — Varianten: Campaign v7, Campaign v8, Campaign Classic
* Verwechseln Sie nicht: „Campaign v7/v8-Aktionen“ (kann zusammen mit nativen Aktionen verwendet werden) ≠ &quot;Campaign Standard-Aktionen“ (kann nicht mit nativen Aktionen auf derselben Journey kombiniert werden)

**FAQ:**

* **F: Wer stellt die Verbindung zwischen Journey Optimizer und Campaign v7/v8 her?** - Adobe richtet die Verbindung zum Zeitpunkt der Bereitstellung ein. Sie müssen sich zur Konfiguration an Adobe wenden.
* **F: Können Campaign v7/v8-Aktionen mit nativen Journey Optimizer-Kanalaktionen auf derselben Journey kombiniert werden?** — Ja, Campaign v7/v8-Aktionen können zusammen mit nativen Kanalaktionen verwendet werden. Dies ist bei Campaign Standard-Aktionen nicht der Fall.
* **F: Können Campaign v7/v8-Aktionen mit Aktivitäten vom Typ „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ verwendet werden?** — Nein, Campaign v7/v8-Aktionen können nicht mit Aktivitäten vom Typ „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ verwendet werden.
* **F: Wie mappe ich Journey-Daten zur Campaign-Nachrichten-Payload?** - Ordnen Sie im Bereich Aktionsparameter jedes erwartete Payload-Feld dem entsprechenden Feld aus dem Journey-Ereignis oder der Datenquelle zu, genauso wie bei benutzerdefinierten Aktionen.

+++
