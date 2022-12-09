---
solution: Journey Optimizer
product: journey optimizer
title: Integration mit Adobe Campaign v7/v8
description: Erfahren Sie, wie Sie die Integration mit Adobe Campaign v7/v8 durchführen.
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Integration mit Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Aktionen in Adobe Campaign v7/v8"
>abstract="Diese Integration ist für Adobe Campaign Classic v7 und v8 verfügbar. Sie ermöglicht den Versand von E-Mails, Push-Benachrichtigungen und SMS mithilfe von Transaktionsnachrichten in Adobe Campaign. Die Verbindung zwischen der Journey Optimizer- und der Campaign-Instanz wird von Adobe zur Bereitstellungszeit eingerichtet."

Diese Integration ist für Adobe Campaign Classic v7 ab Version 7.1 und Adobe Campaign v8 verfügbar. Sie ermöglicht den Versand von E-Mails, Push-Benachrichtigungen und SMS mithilfe von Transaktionsnachrichten in Adobe Campaign.

Die Verbindung zwischen der Journey Optimizer- und der Campaign-Instanz wird von Adobe zur Bereitstellungszeit eingerichtet.

Ein durchgängiges Anwendungsbeispiel wird in diesem Abschnitt vorgestellt [Abschnitt](../building-journeys/ajo-ac.md).

Für jede konfigurierte Aktion ist in der Palette &quot;Journey-Designer&quot;eine Aktionsaktivität verfügbar. Siehe hierzu [Abschnitt](../building-journeys/using-adobe-campaign-classic.md).

## Wichtige Hinweise {#important-notes}

* Es gibt keine Drosselung von Nachrichten. Das System begrenzt die Anzahl der Nachrichten, die basierend auf der aktuellen Campaign-SLA über 5 Minuten an 4000 gesendet werden können. Aus diesem Grund sollte Journey Optimizer nur in Einzelanwendungsfällen verwendet werden (einzelne Ereignisse, keine Segmente).

* Sie müssen für jede zu verwendende Vorlage eine Aktion auf der Arbeitsfläche konfigurieren. Sie müssen für jede Vorlage, die Sie in Adobe Campaign verwenden möchten, eine Aktion in Journey Optimizer konfigurieren.

* Es wird empfohlen, eine dedizierte Message-Center-Instanz zu verwenden, die für diese Integration gehostet wird, um mögliche andere Campaign-Vorgänge nicht zu beeinträchtigen. Der Marketing-Server kann gehostet oder On-Premise verwendet werden. Der erforderliche Build ist Release-Kandidat 21.1 oder höher.

* Es gibt keine Überprüfung, ob die Payload- oder die Campaign-Nachricht korrekt ist.

* Sie können keine Kampagnenaktion mit einem Segmentqualifikationsereignis verwenden.

## Voraussetzungen {#prerequisites}

In Campaign müssen Sie eine Transaktionsnachricht und das zugehörige Ereignis erstellen und veröffentlichen. Siehe Abschnitt [Dokumentation zu Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target=&quot;_blank&quot;}.

Sie können Ihre JSON-Nutzlast entsprechend den folgenden Mustern für jede Nachricht erstellen. Sie fügen diese Payload dann bei der Konfiguration der Aktion in Journey Optimizer ein (siehe unten).

Im Folgenden finden Sie ein Beispiel:

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

* **channel**: den für Ihre Campaign-Transaktionsvorlage definierten Kanal
* **eventType**: den internen Namen Ihres Campaign-Ereignisses
* **ctx**: -Variable basierend auf der Personalisierung, die Sie in Ihrer Nachricht haben.

## Konfiguration der Aktion {#configure-action}

In Journey Optimizer müssen Sie eine Aktion pro Transaktionsnachricht konfigurieren. Führen Sie die folgenden Schritte aus:

1. Erstellen Sie eine neue Aktion. Siehe hierzu [Abschnitt](../action/action.md).
1. Geben Sie einen Namen und eine Beschreibung ein.
1. Im **Aktionstyp** Feld, wählen Sie **Adobe Campaign Classic**.
1. Klicken Sie in **Nutzlast** und fügen Sie ein Beispiel der JSON-Payload ein, das der Campaign-Nachricht entspricht. Wenden Sie sich an Adobe, um diese Payload zu erhalten.
1. Passen Sie die verschiedenen Felder an, die statisch oder variabel sein sollen, je nachdem, ob Sie sie auf der Journey-Arbeitsfläche zuordnen möchten. Bestimmte Felder, wie z. B. Kanalparameter für E-Mail-Adressen- und Personalisierungsfelder (ctx), sollten Sie wahrscheinlich als Variablen für die Zuordnung im Kontext der Journey definieren.
1. Klicken **Speichern**.

![](assets/accintegration1.png)
