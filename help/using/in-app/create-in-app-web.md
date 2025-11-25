---
title: Konfigurieren des Web-In-App-Kanals
description: Erfahren Sie, wie Sie den Web-In-App-Kanal in der Datenerfassung konfigurieren
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: In-App, Nachricht, Erstellung, Starten
exl-id: 5a67177e-a7cf-41a8-9e7d-37f7fe3d34dc
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: ht
source-wordcount: '634'
ht-degree: 100%

---

# Erstellen einer Web-In-App-Nachricht {#create-in-app-web}

## Konfigurieren des Web-In-App-Kanals {#configure-web-inapp}

Gehen Sie wie folgt vor, um Ihren Web-In-App-Kanal einzurichten:

* Installieren Sie die Web SDK-Tag-Erweiterung, um Web-In-App-Nachrichten zu unterstützen. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=de){target="_blank"}

* Passen Sie Ihre Trigger an. Web-In-App-Nachrichten unterstützen zwei Arten von Triggern: „Daten an Platform gesendet“ und „Manuell“. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-in-app-messaging.html?lang=de){target="_blank"}

* Erstellen Sie Ihre Web-In-App-Konfiguration. [Weitere Informationen](inapp-configuration.md)

## Erstellen einer Web-In-App-Nachrichtenkampagne {#create-inapp-web-campaign}

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

1. Wählen Sie den Ausführungstyp Ihrer Kampagne aus: Geplant oder API-ausgelöst. Weitere Informationen zu Kampagnentypen finden Sie auf [dieser Seite](../campaigns/create-campaign.md#campaigntype).

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Aktionen]** die Option **[!UICONTROL In-App-Nachricht]** aus.

   ![](assets/in_app_web_surface_1.png)

1. Wählen oder erstellen Sie Ihre App-Konfiguration. [Weitere Informationen](inapp-configuration.md#channel-prerequisites)

## Definieren der Web-In-App-Nachrichtenkampagne {#configure-inapp}

1. Geben Sie im Abschnitt **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** ein.

1. Um der In-App-Nachricht benutzerdefinierte oder Core-Datennutzungs-Labels zuzuweisen, wählen Sie **[!UICONTROL Zugang verwalten]** aus. [Weitere Informationen](../administration/object-based-access.md).

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen zu definieren. [Weitere Informationen](../audience/about-audiences.md).

   ![](assets/in_app_web_surface_5.png)

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen in der ausgewählten Zielgruppe verwendet werden soll. [Weitere Informationen](../event/about-creating.md#select-the-namespace).

1. Im Menü **[!UICONTROL Aktion]** finden Sie die zuvor unter **[!UICONTROL App-Konfiguration]** konfigurierten Einstellungen. Sie können hier bei Bedarf Änderungen vornehmen oder Ihre Regel aktualisieren, indem Sie auf **[!UICONTROL Regel bearbeiten]** klicken.

1. Klicken Sie auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen und Abwandlungen zu erstellen, deren Performance zu messen und die beste Option für Ihre Zielgruppe zu ermitteln. [Weitere Informationen](../content-management/content-experiment.md)

1. Klicken Sie auf **[!UICONTROL Trigger bearbeiten]**, um die Ereignisse und Kriterien auszuwählen, die Ihre Nachricht auslösen sollen. Mit Rule Builder können Benutzerinnen und Benutzer Kriterien und Werte angeben, die, wenn sie erfüllt sind, eine Reihe von Aktionen auslösen, z. B. das Senden einer In-App-Nachricht.

   1. Klicken Sie auf die Ereignis-Dropdown-Liste, um Ihren Trigger bei Bedarf zu ändern.

      +++Siehe verfügbare Trigger.

      | Paket | Auslöser | Definition |
      |---|---|---|
      | Plattform | Daten an Platform gesendet | Wird ausgelöst, wenn die Mobile App ein Edge-Erlebnisereignis ausgibt, um Daten an die Adobe Experience Platform zu senden. Normalerweise der API-Aufruf [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent){target="_blank"} aus der AEP Edge-Erweiterung. |
      | Manuell | Manueller Trigger | Zwei verknüpfte Datenelemente: ein Schlüssel, bei dem es sich um eine Konstante handelt, die den Datensatz definiert (beispielsweise Geschlecht, Farbe, Preis), und ein Wert, bei dem es sich um eine Variable handelt, die zum Datensatz gehört (z. B. männlich/weiblich, grün, 100). |

      +++

   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Bedingung hinzufügen]**, wenn Sie möchten, dass der Trigger mehrere Ereignisse oder Kriterien berücksichtigt.

   1. Wählen Sie die Bedingung **[!UICONTROL Oder]**, wenn Sie weitere **[!UICONTROL Trigger]** hinzufügen möchten, um Ihre Regel weiter zu erweitern.

      ![](assets/in_app_web_surface_8.png)

   1. Wählen Sie die Bedingung **[!UICONTROL Und]**, wenn Sie ein benutzerdefiniertes **[!UICONTROL Merkmal]** hinzufügen und Ihre Regel besser anpassen möchten.

      +++Siehe verfügbare Merkmale.

      | Paket | Merkmal | Definition |
      |---|---|---|
      | Plattform | XDM-Ereignistyp | Wird ausgelöst, wenn der angegebene Ereignistyp vorliegt. |
      | Plattform | XDM-Wert | Wird ausgelöst, wenn der angegebene XDM-Wert vorliegt. |

      +++

      ![](assets/in_app_web_surface_9.png)

   1. Klicken Sie auf **[!UICONTROL Gruppe erstellen]**, um Trigger zu gruppieren.

1. Wählen Sie die Häufigkeit Ihres Auslösers aus, wenn Ihre In-App-Nachricht aktiv ist. Die folgenden Optionen sind verfügbar:

   * **[!UICONTROL Immer]**: Die Nachricht wird immer angezeigt, wenn die im Dropdown-Menü **[!UICONTROL Mobile-App-Trigger]** ausgewählten Ereignisse eintreten.
   * **[!UICONTROL Einmal anzeigen]**: Die Nachricht wird nur beim ersten Mal angezeigt, wenn die im Dropdown-Menü **[!UICONTROL Mobile-App-Trigger]** ausgewählten Ereignisse eintreten.
   * **[!UICONTROL Bis zu Clickthrough]**: Diese Nachricht wird anzeigt, wenn die im Dropdown-Menü **[!UICONTROL Mobile-App-Trigger]** ausgewählten Ereignisse eintreten, bis vom SDK ein Interaktionsereignis mit der Aktion „Angeklickt“ übermittelt wird.
   * **[!UICONTROL X-mal]**: Diese Nachricht wird X-mal angezeigt.

1. Wählen Sie bei Bedarf aus, an welchem **[!UICONTROL Wochentag]** oder zu welcher **[!UICONTROL Tageszeit]** die In-App-Nachricht angezeigt wird.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/create-campaign.md#schedule), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

   ![](assets/in_app_web_surface_6.png)

1. Sie können jetzt über die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** mit der Erstellung Ihrer Inhalte beginnen. [Weitere Informationen](design-in-app.md)

   ![](assets/in_app_web_surface_7.png)

**Verwandte Themen:**

* [Testen und Senden der In-App-Nachricht](send-in-app.md)
* [In-App-Bericht](../reports/campaign-global-report-cja-inapp.md)
* [In-App-Konfiguration](inapp-configuration.md)
