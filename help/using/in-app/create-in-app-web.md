---
title: Web-In-App-Kanal konfigurieren
description: Erfahren Sie, wie Sie den Web-In-App-Kanal in der Datenerfassung konfigurieren
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: In-App, Nachricht, Erstellung, Starten
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 58%

---

# Web-In-App-Nachricht erstellen {#create-in-app-web}

## Web-In-App-Kanal konfigurieren {#configure-web-inapp}

Gehen Sie wie folgt vor, um Ihren Web-In-App-Kanal einzurichten:

* Installieren Sie die Web SDK-Tag-Erweiterung, um Web-In-App-Nachrichten zu unterstützen. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

* Passen Sie Ihre Trigger an. Web In-App Messaging unterstützt zwei Arten von Triggern: Daten an Platform-Trigger und manuelle Nachrichten. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-in-app-messaging.html)

## Erstellen einer Web-In-App-Nachrichtenkampagne {#create-inapp-web-campaign}

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

1. Wählen Sie im Abschnitt **[!UICONTROL Eigenschaften]** den Ausführungstyp der Kampagne aus: Geplant oder API-ausgelöst. Weitere Informationen zu Kampagnentypen finden Sie auf [dieser Seite](../campaigns/create-campaign.md#campaigntype).

1. Im **[!UICONTROL Aktionen]** wählen Sie die **[!UICONTROL In-App-Nachricht]**. Aus dem **[!UICONTROL Senden an]** Dropdown-Liste wählen Sie Web aus.

   ![](assets/in_app_web_surface_1.png)

1. Definieren Sie eine App-Oberfläche. Sie haben zwei Möglichkeiten, Änderungen vorzunehmen:

   * Sie können entweder **[!UICONTROL Seiten-URL]** , um Änderungen auf eine bestimmte Seite anzuwenden.

   * Sie können eine Regel erstellen, um mehrere URLs als Ziel festzulegen, die demselben Muster entsprechen.

+++ So erstellen Sie eine Seitenvergleichsregel.

      1. Auswählen **[!UICONTROL Seitenübereinstimmungsregel]** als App-Oberfläche.
      1. Klicks **[!UICONTROL Regel erstellen]**.

         ![](assets/in_app_web_surface_3.png)

      1. Im **[!UICONTROL Oberflächenregel bearbeiten]** definieren Sie Ihre Kriterien für die **[!UICONTROL Domäne]** und **[!UICONTROL Seite]** -Felder.
      1. Personalisieren Sie Ihre Kriterien in den Dropdown-Listen Bedingung weiter.

         Wenn Sie hier beispielsweise Elemente bearbeiten möchten, die auf allen Verkaufsproduktseiten Ihrer Luma-Website angezeigt werden, wählen Sie Domäne > Starts mit > Luma und Seite > Enthält > Vertrieb.

         ![](assets/in_app_web_surface_4.png)

      1. Speichern Sie Ihre Änderungen. Die Regel wird auf dem Bildschirm **[!UICONTROL Kampagne erstellen]** angezeigt.

+++

   ![](assets/in_app_web_surface_2.png)

1. Nachdem Sie die Oberfläche Ihrer App ausgewählt und konfiguriert haben, klicken Sie auf **[!UICONTROL Erstellen]**.

## Definieren der Web-In-App-Nachrichtenkampagne {#configure-inapp}

1. Geben Sie im Abschnitt **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** ein.

1. Um der In-App-Nachricht benutzerdefinierte oder Core-Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugang verwalten]** aus. [Weitere Informationen](../administration/object-based-access.md).

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen zu definieren. [Weitere Informationen](../audience/about-audiences.md).

   ![](assets/in_app_web_surface_5.png)

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen in der ausgewählten Zielgruppe verwendet werden soll. [Weitere Informationen](../event/about-creating.md#select-the-namespace).

1. Im **[!UICONTROL Aktion]** Menü, können Sie die zuvor konfigurierten Einstellungen wie **[!UICONTROL Anwendungsoberfläche]**. Sie können hier bei Bedarf Änderungen vornehmen oder Ihre Regel aktualisieren, indem Sie auf **[!UICONTROL Regel bearbeiten]**.

1. Klicken Sie auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen und Abwandlungen zu erstellen, deren Performance zu messen und die beste Option für Ihre Zielgruppe zu ermitteln. [Weitere Informationen](../campaigns/content-experiment.md)

1. Klicken Sie auf **[!UICONTROL Trigger bearbeiten]**, um die Ereignisse und Kriterien auszuwählen, die Ihre Nachricht auslösen sollen. Mit Rule Builder können Benutzerinnen und Benutzer Kriterien und Werte angeben, die, wenn sie erfüllt sind, eine Reihe von Aktionen auslösen, z. B. das Senden einer In-App-Nachricht.

   1. Klicken Sie auf die Ereignis-Dropdown-Liste, um Ihren Trigger bei Bedarf zu ändern.

      +++Siehe verfügbare Trigger.

      | Paket | Auslöser | Definition |
      |---|---|---|
      | Plattform | Daten an Platform gesendet | Wird ausgelöst, wenn die Mobile App ein Edge-Erlebnisereignis ausgibt, um Daten an die Adobe Experience Platform zu senden. Normalerweise der API-Aufruf [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) aus der AEP Edge-Erweiterung. |
      | Manuell | Manueller Trigger | Zwei verknüpfte Datenelemente: ein Schlüssel, bei dem es sich um eine Konstante handelt, die den Datensatz definiert (z. B. Geschlecht, Farbe, Preis), und ein Wert, bei dem es sich um eine Variable handelt, die zum Datensatz gehört (z. B. männlich/weiblich, grün, 100). |

+++

   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Bedingung hinzufügen]**, wenn Sie möchten, dass der Trigger mehrere Ereignisse oder Kriterien berücksichtigt.

   1. Wählen Sie die Bedingung **[!UICONTROL Oder]**, wenn Sie weitere **[!UICONTROL Trigger]** hinzufügen möchten, um Ihre Regel weiter zu erweitern.

      ![](assets/in_app_web_surface_8.png)

   1. Wählen Sie die **[!UICONTROL und]** -Bedingung, wenn Sie eine benutzerdefinierte **[!UICONTROL Eigenschaft]** und passen Sie Ihre Regel besser an.

      +++Sehen Sie sich die verfügbaren Merkmale an.

      | Paket | Merkmal | Definition |
      |---|---|---|
      | Plattform | XDM-Ereignistyp | Wird ausgelöst, wenn der angegebene Ereignistyp erfüllt ist. |
      | Plattform | XDM-Wert | Wird ausgelöst, wenn der angegebene XDM-Wert erfüllt ist. |
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
* [In-App-Bericht](../reports/campaign-global-report.md#inapp-report)
* [In-App-Konfiguration](inapp-configuration.md)