---
solution: Journey Optimizer
product: journey optimizer
title: Trigger einer orchestrierten Kampagne mithilfe eines Signals
description: Erfahren Sie, wie Sie einen Trigger für eine orchestrierte Kampagne mit einem -Signal in  [!DNL Adobe Journey Optimizer].
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
source-git-commit: 6bae2fd7d52dd779d272a9a39ba4dfb7e852d4a8
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%

---

# Trigger hat Kampagnen mithilfe eines Signals orchestriert {#trigger-signal}

Sie können einen Trigger für eine orchestrierte Kampagne durchführen, indem Sie ihr ein Signal senden, anstatt sie planmäßig auszuführen. Das Signal wird über einen API-Aufruf von einem externen System oder einer externen Anwendung gesendet. Bei Verwendung eines Signals können Parameter übergeben werden. Sie werden dann in der orchestrierten Kampagne als Ereignisvariablen im Ausführungskontext zur Verwendung bei der Zielgruppenbestimmung, in Bedingungen oder Ausdrücken bereitgestellt.

Die vollständige REST-Spezifikation für den Trigger-Endpunkt (Pfade, Kopfzeilen, Hauptteil, Antworten und Fehler) finden Sie unter [Trigger Orchestered Campaign API](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} in der Adobe Journey Optimizer-API-Dokumentation.

End-to-End-Prozess zum Trigger einer orchestrierten Kampagne mithilfe eines Signals:

1. [Planung der durch ein Signal ausgelösten Kampagne](#set-an-orchestrated-campaign-to-wait-for-a-signal-configure-signal)
1. [Parameter für die Signal-Payload hinzufügen](#add-parameters-for-the-signal-payload-optional-parameters) (optional)
1. [Erstellen und Testen der Kampagne](#build-and-test-the-campaign-build-and-test)
1. [Veröffentlichen und Trigger der Kampagne](#publish-and-trigger-the-campaign-publish)

>[!NOTE]
>
>Um eine orchestrierte Kampagne mithilfe eines Signals Trigger, benötigen Sie die **[!DNL Publish orchestrated campaigns]** (`orchestrated-campaign.publish`). Siehe [Integrierte Berechtigungen](../administration/ootb-permissions.md).

## Planung der durch ein Signal ausgelösten Kampagne {#configure-signal}

Gehen Sie wie folgt vor, um eine orchestrierte Kampagne so einzurichten, dass sie mit einem Signal statt mit einem Zeitplan startet:

1. Öffnen Sie die orchestrierte Kampagne, die Sie mit einem Signal Trigger machen möchten.

1. Öffnen Sie die Zeitplankonfiguration. [Erfahren Sie, wie Sie eine koordinierte Kampagne planen](create-orchestrated-campaign.md#schedule).

1. Wählen Sie **[!UICONTROL Wird durch ein Signal ausgelöst]**, damit die Kampagne auf ein Signal wartet, anstatt nach einem Zeitplan zu laufen.

   ![Menü „Planung“ mit der Option „Ausgelöst durch ein Signal“](assets/triggered-oc-scheduler.png){zoomable="yes"}

## Parameter für die Signal-Payload hinzufügen (optional) {#parameters}

Sie können Parameter im Kampagnensignal übergeben und in Ihrer Trigger im Ausführungskontext verwenden, z. B. bei der Zielgruppenbestimmung, in Bedingungen oder Ausdrücken. Definieren Sie zunächst jeden Parameter in den Zeitplaneinstellungen und übergeben Sie dann beim Aufruf der Trigger-API dessen Wert.

1. Öffnen Sie die Kampagnenplanung und wählen Sie **[!UICONTROL Parameter hinzufügen]** aus.

1. Definieren Sie den Namen und den Datentyp jedes Parameters, der in der Signal-Payload gesendet werden soll. Sie können auch **Testwerte** angeben, die beim Trigger der Kampagne im Testmodus verwendet werden. [Erfahren Sie, wie Sie eine ausgelöste Kampagne testen](#build-and-test).

   ![Parameter hinzufügen, um Payload-Parameter für das Signal zu definieren](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>Wenn Sie im API-Aufruf einen Parameter übergeben, der nicht im Planer definiert wurde, ist der API-Aufruf trotzdem erfolgreich und der Parameter wird weitergegeben, und Sie können ihn in Ausdrücken verwenden. Die orchestrierte Kampagnenschnittstelle hilft Ihnen jedoch nicht bei der Verwendung. Beispielsweise werden in der Testaktivität keine Parameter aufgelistet oder angezeigt, die nicht in der Planung definiert sind.

## Erstellen und Testen der Kampagne {#build-and-test}

Erstellen Sie Ihre Kampagne auf der Arbeitsfläche und testen Sie sie dann optional im Entwurf , indem Sie das Signal über die API auslösen, bevor Sie veröffentlichen.

1. Fügen Sie Aktivitäten (Audience, Zielgruppenbestimmung, Sendungen) auf der Arbeitsfläche hinzu und verbinden Sie sie. [Weitere Informationen zur Orchestrierung von Kampagnenaktivitäten](orchestrate-activities.md)

1. Wenn Sie Parameter im Signal definiert haben, können Sie diese in Ihre Arbeitsflächen-Logik verkabeln (z. B. in Bedingungen oder beim Targeting). In diesem Beispiel wird der Parameter „channel“ als Bedingung in einer &quot;**[!UICONTROL &quot;-]** verwendet.

   ![Kanalparameter, der als Bedingung in der Testaktivität verwendet wird](assets/triggered-oc-use-parameters.png)

   Um einen Signalparameter im Ausdruckseditor zu verwenden (z. B. um eine Abfrage in der Aktivität **[!UICONTROL Zielgruppe aufbauen]**), geben Sie `$(vars/@<parameterName>)` in das Ausdrucksfeld ein. Ersetzen Sie `<parameterName>` durch den im Planer definierten Parameternamen, z. B. `$(vars/@channel)`. [Erfahren Sie mehr über die Arbeit mit dem Ausdruckseditor](edit-expressions.md).

1. Öffnen Sie die Kampagnenplanung, wählen Sie **[!UICONTROL API-Anfrage kopieren]** und das Format aus (cURL- oder HTTP-Anfrage).

   Die kopierten Informationen enthalten die orchestrierte Kampagnen-ID, den Sandbox-Namen, die Organisations-ID und Testwerte für Ihre Parameter, sofern Sie welche hinzugefügt haben.

   ![Option „API-Anfrage kopieren“ in der Zeitplankonfiguration](assets/triggered-oc-copy.png)

   +++Beispielhafte cURL-Anfrage mit einem -Parameter und einem Testwert

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. Klicken Sie **[!UICONTROL Starten]**, um die Kampagne zu starten.

1. Senden Sie den Trigger-API-Aufruf mit der Beispielanfrage, die Sie aus der Planung kopiert haben. Details zu Anfragen und Antworten finden Sie unter [](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} API für orchestrierte Kampagnen in Trigger.

Wenn Sie mit den Testergebnissen zufrieden sind, veröffentlichen [ die Kampagne](#publish).

## Veröffentlichen und Trigger der Kampagne {#publish}

Nachdem Sie [ Kampagne erstellt und getestet haben](#build-and-test) veröffentlichen Sie die Kampagne, damit sie über Ihre Anwendung ausgelöst werden kann.

1. Klicken Sie **[!UICONTROL der Kampagnen]** Arbeitsfläche auf „Veröffentlichen“. Die Kampagne muss veröffentlicht werden, bevor sie von einem externen System ausgelöst werden kann. [Weitere Informationen zum Starten und Überwachen der Kampagne](start-monitor-campaigns.md#publish).

1. Öffnen Sie die Kampagnenplanung, wählen Sie **[!UICONTROL API-Anfrage kopieren]** und das Format aus (cURL- oder HTTP-Anfrage).

   Die kopierten Informationen enthalten die Kennung der orchestrierten Kampagne, den Sandbox-Namen, die Organisations-ID und die Parameter, sofern Sie welche hinzugefügt haben.

   ![Kopieren einer API-Anfrage in der Zeitplankonfiguration](assets/triggered-oc-copy.png)

1. Rufen Sie die Trigger-API von Ihrem System aus auf. Siehe [API für orchestrierte Trigger ](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} für die Live-Endpunktspezifikation.

   >[!IMPORTANT]
   >
   >Bei einer orchestrierten Live-Kampagne erzwingt eine Drosselungsmaßnahme ein **Mindestintervall von einer Stunde** zwischen zwei API-Trigger-Ausführungen. Wenn Sie die API erneut aufrufen, bevor dieses Intervall abgelaufen ist, gibt die API **HTTP 429**-Fehler (zu viele Anfragen) zurück. Diese Schutzmaßnahme wird nicht angewendet, wenn Sie Trigger für eine Entwurfsversion ausführen, um sie zu testen.

   Wenn Sie Parameter zur Signal-Payload hinzugefügt haben, werden die Werte, die Sie im API-Aufruf übergeben, bei der Ausführung der Kampagne als Kampagnenereignisvariablen verfügbar gemacht. Um sie zu überprüfen, öffnen Sie die Kampagnenprotokolle in der Symbolleiste der Kampagnen-Arbeitsfläche. Identifizieren Sie auf **[!UICONTROL Registerkarte]** die Aufgabe, die dem Signal entspricht, und klicken Sie auf das Stiftsymbol, um auf die zugehörigen Ereignisvariablen zuzugreifen. [Erfahren Sie, wie Sie auf Protokolle und Aufgaben zugreifen können](start-monitor-campaigns.md#logs-tasks).

   ![Bildschirm „Protokolle und Aufgaben“, auf dem Kampagnenereignisvariablen verfügbar sind](assets/trigger-events-variables.png){zoomable="yes"}
