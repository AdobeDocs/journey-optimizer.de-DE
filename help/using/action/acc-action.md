---
solution: Journey Optimizer
product: journey optimizer
title: Integrieren mit Adobe Campaign v7/v8
description: Erfahren Sie, wie Sie Journey Optimizer mit Adobe Campaign v7/v8 integrieren
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: Kampagne, ACC, Integration
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: cc4ea97f858a212b82ac3b77328e61f59e3bfc27
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Integrieren mit Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Aktionen in Adobe Campaign v7/v8"
>abstract="Diese Integration ist für Adobe Campaign v7 und v8 verfügbar. Sie ermöglicht Ihnen das Senden von E-Mails, Push-Benachrichtigungen und SMS mit der Transaktionsnachrichtenfunktion von Adobe Campaign. Die Verbindung zwischen der Journey Optimizer- und der Campaign-Instanz wird bei der Bereitstellung von Adobe hergestellt."

Diese Integration ist für Adobe Campaign v7/v8 ab Version 7.1 und Adobe Campaign v8 verfügbar.  Sie ermöglicht Ihnen das Senden von E-Mails, Push-Benachrichtigungen und SMS mit der Transaktionsnachrichtenfunktion von Adobe Campaign.

In diesem [Abschnitt](../building-journeys/ajo-ac.md) wird ein Anwendungsfall schrittweise beschrieben.

Für jede konfigurierte Aktion ist eine Aktionsaktivität in der Journey-Designer-Palette verfügbar. Siehe diesen [Abschnitt](../building-journeys/using-adobe-campaign-v7-v8.md).

## Zugriff {#access}

Die Verbindung zwischen den Journey Optimizer- und Campaign-Instanzen wird von Adobe bei der Bereitstellung eingerichtet, falls gewünscht. Wenn Sie die Verbindung zum Bereitstellungszeitpunkt nicht angefordert haben, wenden Sie sich an den Adobe Journey Optimizer-Support und geben Sie die folgenden Informationen an, um die Aktivierung anzufordern:

Was Adobe Journey Optimizer betrifft:

* Organisations-ID (Adobe OrgID)
* Sandbox

Was Adobe Campaign betrifft:

* Campaign-URL
* RT-URL
* Campaign-Version

## Wichtige Hinweise {#important-notes}

* Es gibt keine Drosselung von Nachrichten. Auf der Basis des aktuellen Campaign-SLA begrenzt das System die Anzahl der Nachrichten, die gesendet werden können, auf 4.000 pro 5 Minuten. Aus diesem Grund sollte Journey Optimizer nur in unitären Anwendungsfällen (einzelne Ereignisse, nicht für Zielgruppen) verwendet werden.

* Sie müssen für jede Vorlage, die Sie verwenden möchten, eine Aktion auf der Arbeitsfläche konfigurieren. Sie müssen für jede Vorlage, die Sie von Adobe Campaign verwenden möchten, eine Aktion in Journey Optimizer konfigurieren.

* Es wird empfohlen, eine dedizierte Message Center-Instanz zu verwenden, die für diese Integration gehostet wird, um zu vermeiden, dass andere Campaign-Vorgänge, die Sie vielleicht gerade ausführen, beeinträchtigt werden. Der Marketing-Server kann gehostet oder On-Premise bereitgestellt werden. Der erforderliche Build ist Release Candidate 21.1 oder höher.

* Es wird nicht überprüft, ob die Payload oder Campaign-Nachricht korrekt ist.

* Sie können eine Campaign-Aktion nicht mit einem Zielgruppen-Qualifizierungsereignis verwenden.

## Voraussetzungen {#prerequisites}

Sie müssen in Campaign eine Transaktionsnachricht und das zugehörige Ereignis erstellen und veröffentlichen. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html?lang=de#transactional-messaging){target="_blank"}.

Sie können Ihre JSON-Payload entsprechend jeder Nachricht nach dem folgenden Muster aufbauen. Sie fügen diese Payload dann beim Konfigurieren der Aktion in Journey Optimizer ein (siehe unten)

Siehe folgendes Beispiel:

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **channel**: der für Ihre Campaign-Transaktionsvorlage definierte Kanal
* **eventType**: der interne Namen Ihres Campaign-Ereignisses
* **ctx**: Variable basierend auf der Personalisierung in Ihrer Nachricht.

## Konfigurieren der Aktion {#configure-action}

In Journey Optimizer müssen Sie eine Aktion pro Transaktionsnachricht konfigurieren. Führen Sie folgende Schritte aus:

1. Erstellen Sie eine neue Aktion. Siehe diesen [Abschnitt](../action/action.md).
1. Geben Sie einen Namen und eine Beschreibung ein.
1. Wählen Sie im Feld **Aktionstyp** die Option **Adobe Campaign Classic** aus.
1. Klicken Sie in das Feld **Payload** und fügen Sie ein Beispiel der JSON-Payload ein, die der Campaign-Nachricht entspricht. Wenden Sie sich an Adobe, um diese Payload zu erhalten.
1. Passen Sie die verschiedenen Felder je nach gewünschter Zuordnung auf der Journey-Arbeitsfläche als statisch oder variabel an. Bestimmte Felder, wie z. B. Kanalparameter für E-Mail-Adressen- und Personalisierungsfelder (ctx), sollten wahrscheinlich als Variablen für die Zuordnung im Kontext der Journey definiert werden.
1. Klicken Sie auf **Speichern**.

![](assets/accintegration1.png)