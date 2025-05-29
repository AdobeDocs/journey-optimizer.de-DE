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
source-git-commit: 60cb5e1ba2b5c8cfd0a306a589c85761be1cf657
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 46%

---

# Integrieren mit Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Aktionen in Adobe Campaign v7/v8"
>abstract="Diese Integration ist für Adobe Campaign v7 und v8 verfügbar. Sie ermöglicht Ihnen das Senden von E-Mails, Push-Benachrichtigungen und SMS mit der Transaktionsnachrichtenfunktion von Adobe Campaign. Die Verbindung zwischen der Journey Optimizer- und der Campaign-Instanz wird bei der Bereitstellung von Adobe hergestellt."

Wenn Sie über Adobe Campaign Classic v7 oder Campaign v8 verfügen, steht in Ihren Journey eine spezifische benutzerdefinierte Aktion zur Verfügung, um Adobe Journey Optimizer und Adobe Campaign zu integrieren. Diese Integration ermöglicht den Versand von E-Mails, Push-Benachrichtigungen und SMS mit der Transaktionsnachrichten-Funktion von Adobe Campaign. Weitere Informationen finden Sie [ diesem End-to-End-Anwendungsfall](../building-journeys/ajo-ac.md).

Für jede konfigurierte Aktion ist [Campaign-Aktionsaktivität](../building-journeys/using-adobe-campaign-v7-v8.md) in der Journey-Designer-Palette verfügbar.

## Activation {#access}

Wenn angefordert, wird die Verbindung zwischen der Journey Optimizer- und der Adobe Campaign-Umgebung zum Zeitpunkt der Bereitstellung von Adobe eingerichtet. Wenn Sie die Verbindung zum Zeitpunkt der Bereitstellung nicht angefordert haben, wenden Sie sich an den Adobe Journey Optimizer-Support, um die Aktivierung anzufordern. Sie müssen die folgenden Details angeben:

>[!BEGINTABS]

>[!TAB Für Adobe Journey Optimizer]

* Organisations-ID (Adobe OrgID)
* Sandbox-Name

>[!TAB Für Adobe Campaign]

* Campaign-Server-URL
* Echtzeit-Server-URL
* Ihre Adobe Campaign-Version

>[!ENDTABS]


## Schutzmechanismen und Einschränkungen {#important-notes}

* Es gibt keine Drosselung von Nachrichten. Auf der Basis des aktuellen Campaign-SLA begrenzt das System die Anzahl der Nachrichten, die gesendet werden können, auf 4.000 pro 5 Minuten. Aus diesem Grund sollte Journey Optimizer nur in unitären Anwendungsfällen (einzelne Ereignisse, nicht für Zielgruppen) verwendet werden.

* Pro Vorlage muss auf der Arbeitsfläche eine Aktion konfiguriert werden. Sie müssen für jede Vorlage, die Sie von Adobe Campaign verwenden möchten, eine Aktion in Journey Optimizer konfigurieren.

* Es wird empfohlen, für diese Integration eine dedizierte Message Center- oder Managed Services-Instanz zu verwenden, um zu vermeiden, dass andere Campaign-Vorgänge, die Sie möglicherweise gerade ausführen, beeinträchtigt werden. Der Marketing-Server kann gehostet oder On-Premise.<!--The build required is 21.1 Release Candidate or greater. -->

* Es wird nicht überprüft, ob die Payload oder Campaign-Nachricht korrekt ist.

* Sie können eine Campaign-Aktion nicht mit einem Zielgruppen-Qualifizierungsereignis verwenden.

## Voraussetzungen {#prerequisites}

In Adobe Campaign müssen Sie eine Transaktionsnachricht und das zugehörige Ereignis erstellen und veröffentlichen. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Campaign](https://experienceleague.adobe.com/de/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}.

Sie können Ihre JSON-Payload entsprechend jeder Nachricht nach dem folgenden Muster aufbauen. Sie fügen diese Payload dann beim Konfigurieren der Aktion in Journey Optimizer ein (siehe unten).

+++ Beispiel

```json
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
* **ctx**: Variable basierend auf der Personalisierung in Ihrer Nachricht

+++

## Konfigurieren der Aktion {#configure-action}

In Journey Optimizer müssen Sie eine Aktion pro Transaktionsnachricht konfigurieren.

Gehen Sie wie folgt vor, um eine Campaign-Aktion zu erstellen:

1. Erstellen Sie eine neue Aktion. [Erfahren Sie, wie Sie benutzerdefinierte Aktionen erstellen](../action/action.md).
1. Geben Sie einen Namen und eine Beschreibung ein.
1. Wählen Sie im Feld **Aktionstyp** die Option **Adobe Campaign Classic** aus.
   ![](assets/accintegration1.png)
1. Klicken Sie in das Feld **Payload** und fügen Sie ein Beispiel der JSON-Payload ein, die der Campaign-Nachricht entspricht. Wenden Sie sich an Adobe, um diese Payload zu erhalten.
1. Legen Sie jedes Feld entweder als statisch oder als Variable fest, je nachdem, ob Sie möchten, dass es auf der Journey-Arbeitsfläche zugeordnet wird. Beispielsweise sollten Felder wie E-Mail-Kanalparameter und Personalisierungsfelder (`ctx`) normalerweise als Variablen festgelegt werden, damit sie sich innerhalb der Journey dynamisch anpassen können.
1. Klicken Sie auf **Speichern**.

