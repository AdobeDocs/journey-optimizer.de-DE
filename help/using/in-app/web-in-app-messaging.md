---
title: Konfigurieren der Web-In-App-Messaging-Unterstützung in Web SDK
description: Erfahren Sie, wie Sie die Tag-Erweiterung „Web SDK" konfigurieren, um Web-In-App-Nachrichten zu unterstützen.
feature: In App
topic: Content Management
role: Developer
level: Intermediate
keywords: In-App, Nachricht, Web SDK, Konfiguration
source-git-commit: 4a7f98ce24af02658620485840d11190c0954c09
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 1%

---

# Konfigurieren der Web-In-App-Messaging-Unterstützung in Web SDK

In-App-Nachrichten sind Benachrichtigungen, die Sie an Benutzer innerhalb Ihrer Web-Anwendung senden können und sie zu bestimmten Punkten von Interesse führen.

Sie können diese Benachrichtigungen für verschiedene Zwecke verwenden, z. B. zur Förderung neuer Funktionen, zur Präsentation von Sonderangeboten oder zur Erleichterung des Onboardings von Benutzenden.

Mithilfe von In-App-Nachrichten können Sie effektiv mit Ihrer Zielgruppe interagieren und sie auf wichtige Aspekte Ihrer Anwendung lenken.

## Voraussetzungen {#prerequisites}

### Web SDK-Tag-Erweiterungsversion {#extension-version}

Für die Web-In-App-Messaging-Funktion ist die neueste Version der Tag-Erweiterung von Web SDK erforderlich.

### Konfigurieren eines CSP für Web-In-App-Messaging {#csp}

Beim Konfigurieren von Web-In-App-Nachrichten müssen Sie die folgende Anweisung in Ihren CSP aufnehmen:

```
default-src  blob:;
```

Weitere Informationen zur Konfiguration eines CSP finden Sie unter [Datenerfassungsdokumentation](https://experienceleague.adobe.com/docs/experience-platform/edge/use-cases/configuring-a-csp.html?lang=de){target="_blank"}.

## Konfigurieren von Web-In-App-Nachrichten mit der Tag-Erweiterung „Web SDK&quot; {#tag-extension}

Auf der Seite [Konfiguration von Web SDK-Tag-Erweiterungen](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=de){target="_blank"} erfahren Sie, wo Sie die unten beschriebenen Einstellungen finden.

Nachdem Sie die Tag[Erweiterung &quot;](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=de#install-the-web-sdk-tag-extension){target="_blank"}&quot; installiert haben, führen Sie die folgenden Schritte aus, um die Erweiterung für Web-In-App-Nachrichten zu konfigurieren.

Aktivieren Sie im Abschnitt **[!UICONTROL Personalization]** die Option **[!UICONTROL Personalisierungsspeicher aktivieren]**. Mit dieser Option kann Web SDK verfolgen, welche Erlebnisse der Benutzer über Seitenladevorgänge hinweg gesehen hat.

![Bild, das die Speicheroption „Personalisierung“ auf der Seite „Tag-Erweiterungskonfiguration“ zeigt.](assets/enable-personalization-storage.png)

Web-In-App-Messaging unterstützt zwei Typen von Triggern:

* [Senden von Daten an Experience Platform](#send-data-platform)
* [Manuelles Auslösen der Nachrichten](#manual-trigger)

Anhand der folgenden Abschnitte können Sie die Tag-Erweiterung „Web SDK&quot; entsprechend den gewünschten Triggern konfigurieren.

### Konfigurationsschritte für den Trigger **[!UICONTROL Daten an Experience Platform senden]** {#send-data-platform}

1. Wählen Sie die Tag-Eigenschaft aus, die Ihre Web SDK-Erweiterung enthält, und [erstellen Sie eine neue Regel](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/managing-resources/rules.html#create-a-rule){target="_blank"} mit den folgenden Einstellungen:

   * **[!UICONTROL Erweiterung]**: [!UICONTROL Core]
   * **[!UICONTROL Ereignistyp]**: [!UICONTROL Bibliothek geladen (Seitenanfang)]

   ![Bild mit dem Bildschirm für die Ereigniskonfiguration.](assets/rule-configuration.png)

1. Wählen **[!UICONTROL Änderungen beibehalten]**, um die Ereigniskonfiguration zu speichern.

1. Fügen Sie nun zu der von Ihnen erstellten Regel eine Aktion hinzu. Wählen Sie im Abschnitt [!DNL Actions] die Option **[!UICONTROL Hinzufügen]** aus.

   Verwenden Sie die folgenden **[!UICONTROL Action]**-Einstellungen:

   * **[!UICONTROL Erweiterung]**: [!UICONTROL Adobe Experience Platform Web SDK]
   * **[!UICONTROL Aktionstyp]**: [!UICONTROL Ereignis senden]

   ![Bild mit dem Bildschirm „Regel bearbeiten“](assets/add-action.png)

1. Aktivieren Sie auf der rechten Bildschirmseite im Abschnitt **[!UICONTROL Personalization]** die Option **[!UICONTROL Visuelle Personalisierungsentscheidungen rendern]**.

   ![Bild mit dem Bildschirm für die Personalisierungskonfiguration.](assets/render-visual-personalization.png)

1. Definieren Sie rechts im Bildschirm im Abschnitt **[!UICONTROL Entscheidungskontext]** die **[!UICONTROL Schlüssel]**/**[!UICONTROL Wert]**-Paare, die Sie in Ihrer Kampagnenkonfiguration verwendet haben, um sich für die In-App-Nachricht zu qualifizieren.

   ![Bild mit dem Bildschirm für die Personalisierungskonfiguration.](assets/decision-context.png)

1. Wählen **[!UICONTROL Änderungen beibehalten]** um Ihre Konfiguration zu speichern.

1. Als Nächstes müssen Sie die neu erstellte Regel zur Tag-Eigenschaftsbibliothek hinzufügen. Navigieren Sie dazu zu **[!UICONTROL Veröffentlichungsfluss]** und wählen Sie die zuvor erstellte Regel aus.

   ![Bild, das den Bibliotheksbildschirm anzeigt.](assets/add-rule-to-library.png)

1. Nachdem Sie die Regel zur Bibliothek hinzugefügt haben, wählen Sie **[!UICONTROL Speichern und in Entwicklung erstellen]** aus.

   ![Bild mit dem Bildschirm für die Personalisierungskonfiguration.](assets/publish-flow.png)

Der Konfigurationsprozess ist jetzt abgeschlossen und Ihre Nachricht kann den Benutzern angezeigt werden.

### Konfigurationsschritte zur Verwendung von manuellen Triggern {#manual-trigger}

1. Wählen Sie die Tag-Eigenschaft aus, die Ihre Web SDK-Erweiterung enthält, und [Erstellen einer neuen Regel](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/managing-resources/rules.html#create-a-rule){target="_blank"} mit den folgenden Einstellungen:

   * **[!UICONTROL Erweiterung]**: [!UICONTROL Core]
   * **[!UICONTROL Ereignistyp]**: [!UICONTROL Klick]

1. Legen Sie den Trigger für ein bestimmtes Seitenelement fest, das durch einen von Ihnen ausgewählten CSS-Selektor identifiziert wird.

   ![Bild mit dem Bildschirm für die Ereigniskonfiguration.](assets/event-configuration-manual.png)

1. Sie müssen der von Ihnen erstellten Regel eine Aktion hinzufügen. Wählen Sie im Abschnitt [!DNL Actions] die Option **[!UICONTROL Hinzufügen]** aus und verwenden Sie die folgenden Einstellungen **[!UICONTROL Aktion]**:

   * **[!UICONTROL Erweiterung]**: [!UICONTROL Adobe Experience Platform Web SDK]
   * **[!UICONTROL Aktionstyp]**: [!UICONTROL Regelsätze auswerten]

   ![Bild mit dem Bildschirm „Regel bearbeiten“](assets/add-action.png)

1. Aktivieren Sie auf der rechten Bildschirmseite die Option **[!UICONTROL Visuelle Personalisierungsentscheidungen rendern]**.

   ![Bild mit dem Bildschirm für die Personalisierungskonfiguration.](assets/manual-trigger-render.png)

1. Definieren Sie rechts im Bildschirm im Abschnitt **[!UICONTROL Entscheidungskontext]** die **[!UICONTROL Schlüssel]**/**[!UICONTROL Wert]**-Paare, die Sie in Ihrer Kampagnenkonfiguration verwendet haben, um sich für die In-App-Nachricht zu qualifizieren.

   ![Bild mit dem Bildschirm für die Personalisierungskonfiguration.](assets/manual-trigger-decision-context.png)

1. Wählen **[!UICONTROL Änderungen beibehalten]** um Ihre Konfiguration zu speichern.

1. Fügen Sie die neu erstellte Regel zur Tag-Eigenschaftsbibliothek hinzu. Navigieren Sie dazu zu **[!UICONTROL Veröffentlichungsfluss]** und wählen Sie die zuvor erstellte Regel aus.

   ![Bild, das den Bibliotheksbildschirm anzeigt.](assets/add-rule-to-library.png)

1. Nachdem Sie die Regel zur Bibliothek hinzugefügt haben, wählen Sie **[!UICONTROL Speichern und in Entwicklung erstellen]** aus.

   ![Bild mit dem Bildschirm für die Personalisierungskonfiguration.](assets/publish-flow.png)

Der Konfigurationsprozess ist jetzt abgeschlossen und Ihre Nachricht kann den Benutzern angezeigt werden.

## Konfigurieren von Web-In-App-Nachrichten mithilfe der Web SDK JavaScript-Bibliothek {#js-library}

Als Alternative zur Verwendung der Tag-Erweiterung „Web SDK&quot; können Sie Web-In-App-Nachrichten auch direkt über die Web SDK JavaScript-Bibliothek konfigurieren.

Sie können Web-In-App-Nachrichten von Adobe Journey Optimizer auf zwei Arten anzeigen.

### Methode 1: Automatisches Abrufen des Personalisierungsinhalts {#automatic}

Damit Web SDK den Personalisierungsinhalt beim Laden der Seite automatisch abruft, verwenden Sie den Befehl `sendEvent` , wie im folgenden Beispiel gezeigt.

```js
  alloy("sendEvent", {
      renderDecisions: true,
      personalization: {
          surfaces: ['#welcome']
      }
  });
```

### Methode 2: Manuelles Abrufen des Personalisierungsinhalts basierend auf der Benutzeraktion {#manual}

Um den Personalisierungsinhalt erst anzuzeigen, nachdem der Benutzer eine bestimmte Aktion ausgeführt hat, verwenden Sie den Befehl `evaluateRulesets` wie im folgenden Beispiel gezeigt.

In diesem Beispiel wird der Personalisierungsinhalt angezeigt, wenn ein Benutzer auf die Schaltfläche „Jetzt **[!UICONTROL &quot;]** Ihrer Website klickt.

```js
 alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
         decisionContext: {
             "userAction": "buy_now"
         }
     }
 });
```

### Personalisierungsspeicher konfigurieren {#personalization-storage}

Sie können festlegen, dass In-App-Nachrichten Benutzern für eine bestimmte Anzahl von Malen oder jedes Mal, wenn sie eine Seite besuchen, über die `personalizationStorageEnabled` angezeigt werden.

Legen [&#x200B; in der Konfiguration &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de){target="_blank"}Web-SDK&quot; die Option &quot;`personalizationStorageEnabled`&quot; entsprechend Ihren Anforderungen fest:

* `personalizationStorageEnabled: true` Trigger die In-App-Nachricht mit der Häufigkeit, die Sie in Ihrer [Kampagne) &#x200B;](create-in-app-web.md#configure-inapp).
* `personalizationStorageEnabled: false` Trigger die In-App-Nachricht bei jedem Laden der Seite.
