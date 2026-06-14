---
solution: Journey Optimizer
product: journey optimizer
title: Überprüfen und Testen Ihrer WhatsApp-Nachrichten
description: Erfahren Sie, wie Sie Ihre WhatsApp-Nachrichten in Journey Optimizer überprüfen und senden können.
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 31acb095-de90-495f-8e8c-43a78dedfa06
TQID: https://experienceleague.adobe.com/u2OevVu38fPdytpuTmHeSdEx3Wvpih7ifk-j88rhDFI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b8df23d2-98a2-4406-86cc-2babe8728d36
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 01105f4dc3f6b52598c634373988570cf6916406
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 42%

---

# Überprüfen und Senden Ihrer WhatsApp-Nachrichten {#send-whatsapp}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Sie Ihre WhatsApp-Nachricht in der Vorschau anzeigen, validieren und senden und dann die zurückgegebenen Interaktionsdaten analysieren, um sicherzustellen, dass Ihre Nachricht vor dem Versand korrekt ist, und um zu messen, wie Empfängerinnen und Empfänger damit interagieren.

>[!ENDSHADEBOX]

## Anzeigen einer Vorschau Ihrer WhatsApp-Nachricht {#preview-whatsapp}

Sobald der Nachrichteninhalt definiert wurde, können Sie den Inhalt mit einer der beiden Simulationsmethoden in der Vorschau anzeigen:

* Klicken Sie **[!UICONTROL Inhalt simulieren]**, um Inhaltsvarianten mit Beispieleingabedaten oder automatischer KI-Generierung zu testen. [Informationen zum Simulieren von Inhaltsvarianten](../test-approve/simulate-sample-input.md)
* Klicken Sie auf **[!UICONTROL Inhalt simulieren]** und wählen Sie dann **[!UICONTROL Inhalt simulieren (AEP-Profile)]** aus der Dropdown-Liste aus, um eine Vorschau mit Testprofilen anzuzeigen.

Detaillierte Informationen zur Vorschau und zum Test des Inhalts finden Sie im Abschnitt [Content-Management](../content-management/preview-test.md).

## Validieren Ihres Inhalts {#whatsapp-validate}

Sie müssen die Warnmeldungen im oberen Bereich des Editors überprüfen. Einige davon sind einfache Warnungen, aber andere können Sie daran hindern, die Nachricht zu senden. Es gibt zwei Arten von Warnungen: Warnungen und Fehler.

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. So wird beispielsweise eine Warnmeldung angezeigt, wenn Ihre Textnachricht leer ist.

* **Fehler** hindern Sie daran, die Journey zu testen oder zu aktivieren oder die Kampagne zu veröffentlichen, bis sie behoben sind. Eine Fehlermeldung warnt Sie zum Beispiel, wenn die Betreffzeile fehlt.

## Senden Ihrer WhatsApp-Nachrichten {#whatsapp-send}

>[!IMPORTANT]
>
> Wenn Ihre Kampagne einer Genehmigungsrichtlinie unterliegt, müssen Sie eine Genehmigung anfordern, um Ihre Textnachrichten senden zu können. [Weitere Informationen](../test-approve/gs-approval.md)

Wenn Ihre WhatsApp-Nachricht fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/publish-journey.md) oder [Kampagne](../campaigns/review-activate-campaign.md), um sie zu versenden.

## WhatsApp-Interaktionen analysieren {#whatsapp-channel-context}

Journey Optimizer erfasst zusätzliche Interaktionsdaten, die vom WhatsApp-Kanal zurückgegeben werden, und speichert sie im **AJO-E-Mail-Tracking-Erlebnisereignis** Datensatz unter der `whatsAppChannelContext` Feldergruppe. Verwenden Sie diese Felder, um [Zielgruppen](../audience/about-audiences.md) zu erstellen, [Abfragen](../data/get-started-queries.md) auszuführen und die WhatsApp-Interaktion zu analysieren. [Weitere Informationen zu Systemdatensätzen](../data/get-started-datasets.md#system-datasets).

Die folgenden Felder werden erfasst:

| Feld | Beschreibung |
|-|-|
| `messageType` | WhatsApp-Nachrichtentyp (z. B. `templateBased`, `response`). |
| `inboundMessage` | Inhalt eingehender Antworten (z. B. `stop`, `start`, `subscribe`) |
| `inboundNumber` | Absender-ID, bei der die eingehende Nachricht empfangen wurde. |
| `channelType` | Kanal-Kategorie (`Utility`, `Marketing` oder `Promotional`). |
| `profileNumber` | Telefonnummer, von der die eingehende Nachricht empfangen wurde. |
| `origTimestamp` | Ursprünglicher Zeitstempel aus Meta/WhatsApp. |
| `status` | Versandstatus einschließlich standardisiertem Provider-Feedback (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` oder `unknown`) und der rohen Provider-Statusmeldung. |
| `reactionEvent` | Inhalt der Benutzerantwort: Emoji für Reaktionen oder Nachrichtentext für Antworten auf eine bestimmte Nachricht. |
| `reactionMessageID` | ID der ursprünglichen Nachricht, auf die geantwortet wird. |
| `reactionActionName` | Typ der Antwortaktion (`react`, `unreact` oder `reply`). |
| `interactiveSelectedTitle` | Vom Benutzer ausgewählter Titel aus einer interaktiven WhatsApp-Nachricht. |
| `interactiveType` | Interaktiver Nachrichtentyp (`list reply`, `button reply` oder `button`). |
| `interactiveSelectedDescription` | Beschreibung der ausgewählten interaktiven WhatsApp-Option. |
| `interactiveSelectedID` | Kennung der gewählten Option aus WhatsApp. |

Um diesen Datensatz abzufragen, verwenden Sie die `ajo_email_tracking_experience_event_dataset` im Abfrage-Service. Informationen zu Abfragemustern und zugehörigen Anwendungsfällen finden Sie unter [Beispiele für Datensatzabfragen](../data/datasets-query-examples.md).
