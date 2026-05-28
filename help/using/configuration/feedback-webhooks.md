---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von Feedback-Webhooks für durch API ausgelöste Kampagnen in Journey Optimizer
description: Erfahren Sie, wie Sie Feedback-Webhooks für durch API ausgelöste Kampagnen in Journey Optimizer erstellen.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
exl-id: a46f29a4-5115-4feb-8b2c-751765be2b36
TQID: https://experienceleague.adobe.com/RPopgwZfOcaw-uHvqVnforixMTAH57urwF2ViaZQemQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 302
ht-degree: 100%

---

# Erstellen von Feedback-Webhooks für durch API ausgelöste Kampagnen {#webhooks}

Feedback-Webhooks ermöglichen es Ihnen, Statusaktualisierungen in Echtzeit für Nachrichten zu erhalten, die über durch API ausgelöste Transaktions-Kampagnen gesendet werden. Durch die Konfiguration eines Webhooks können Sie automatisch Versandergebnisse direkt in Ihren Systemen empfangen, was Monitoring, Protokollierung und automatisierte Verarbeitung ermöglicht.

Sie können Webhook-Konfigurationen über das Menü **[!UICONTROL Administration]**/**[!UICONTROL Kanäle]**/**[!UICONTROL Feedback-Webhook-Einstellungen]** verwalten.

![](assets/webhook-list.png)

>[!NOTE]
>Pro Kombination aus **Organisation und Sandbox** ist nur eine Webhook-Konfiguration zulässig.

## Erstellen eines Feedback-Webhooks

Gehen Sie wie folgt vor, um einen Webhook zu erstellen:

1. Navigieren Sie zu **[!UICONTROL Administration]**/**[!UICONTROL Kanäle]**/**[!UICONTROL Feedback Webhook-Einstellungen]**.

1. Klicken Sie auf **Feedback-Webhook erstellen**.

1. Geben Sie im Abschnitt **[!UICONTROL Grundkonfiguration]** die folgenden Details an:

   ![](assets/webhook-config.png)

   * **Webhook-Name**: Geben Sie einen beschreibenden Namen zur Identifizierung des Webhooks ein.
   * **Kanäle**: Wählen Sie die Kanäle aus, für die dieser Webhook Feedback erhalten soll (E-Mail und/oder SMS).
   * **Webhook-URL**: Geben Sie den HTTPS-Endpunkt an, an den Feedback-Ereignisse gesendet werden sollen.

1. Wählen Sie im Abschnitt **[!UICONTROL Authentifizierung]** die Authentifizierungsmethode aus.

   ![](assets/webhook-authentication.png)

   * **Keine Authentifizierung**: Es werden keine Authentifizierungs-Header hinzugefügt.
   * **JWT-Authentifizierung**: Geben Sie die erforderlichen Details an, wenn Ihr Endpunkt eine JWT-Authentifizierung erfordert.

1. Im Abschnitt **[!UICONTROL Header-Parameter]** können Sie zusätzliche benutzerdefinierte Header konfigurieren, die mit jeder Webhook-Anfrage gesendet werden sollen.

   ![](assets/webhook-header.png)

1. Klicken Sie auf **[!UICONTROL Senden]**, um die Konfiguration zu speichern.

>[!NOTE]
>
>Sie können einen Webhook jederzeit bearbeiten. Öffnen Sie ihn dazu im Inventar und klicken Sie auf die Schaltfläche **[!UICONTROL Bearbeiten]**.

## Webhook-Payload-Struktur

Nach der Ausführung einer Nachricht sendet **[!DNL Journey Optimizer]** die folgende Payload an den konfigurierten Endpunkt.

```
{
  "requestId": "8NoByJneShCdCGRnrGS1t1m3CdA73dhR",
  "imsOrg": "myImsOrg",
  "sandbox": {
    "id": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "name": "prod"
  },
  "channel": "email",
  "eventType": "message.feedback",
  "messageExecution": {
    "messageExecutionID": "HUMA-26362805",
    "messageType": "transactional",
    "campaignID": "16f24a15-7e21-477c-848a-d5695ca7f137",
    "campaignVersionID": "2ca10c10-56dd-4505-87cd-fa5da84e7a5d"
  },
  "messageDeliveryFeedback": {
    "feedbackStatus": {
      "value": "bounce"
    },
    "offers": null,
    "messageExclusion": null,
    "messageFailure": {
      "category": "sync",
      "type": "Ignored",
      "code": "25",
      "reason": "Admin Failure"
    },
    "retryCount": 0
  },
  "identityMap": {
    "email": [
      {
        "id": "john.doe@luma.com",
        "primary": true
      }
    ]
  }
}
```

Der Webhook kann die folgenden Ereignisse erfassen:

* Gesendet
* zugestellt
* Bounce (siehe obiges Beispiel)
* Fehler

Jede eingehende Anfrage enthält auch eine eindeutige requestId, die an den Webhook zurückgesendet wird.

## Nächste Schritte {#next}

Nachdem ein Feedback-Webhook erstellt wurde, können Sie ihn bei der Konfiguration einer Zielgruppe von **durch API ausgelösten Transaktionskampagnen** aktivieren. Weitere Informationen finden Sie in diesem Abschnitt: [Aktivieren von Webhooks](../campaigns/api-triggered-campaign-audience.md#webhook)
