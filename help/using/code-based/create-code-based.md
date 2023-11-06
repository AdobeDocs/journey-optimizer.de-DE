---
title: Erstellen von Code-basierten Erlebnissen
description: Informationen zum Erstellen von Code-basierten Erlebnissen in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 100%

---

# Erstellen von Code-basierten Erlebnissen {#create-code-based}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit dem Code-basierten Kanal](get-started-code-based.md)
* [Code-basierte Voraussetzungen](code-based-prerequisites.md)
* [Code-basierte Implementierungsbeispiele](code-based-implementation-samples.md)
* **[Erstellen von Code-basierten Erlebnissen](create-code-based.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Dieser Code-basierte Kanal ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

## Erstellen einer Code-basierten Kampagne {#create-code-based-campaign}

Führen Sie die folgenden Schritte aus, um Ihr Code-basiertes Erlebnis durch eine Kampagne zu erstellen.

>[!CAUTION]
>
>Derzeit können Code-basierte Erlebnisse in [!DNL Journey Optimizer] nur mithilfe von **Kampagnen** erstellt werden.

1. Erstellen einer Kampagne. [Weitere Informationen](../campaigns/create-campaign.md)

1. Wählen Sie die Aktion **[!UICONTROL Code-basiertes Erlebnis (Beta)]** aus.

1. Geben Sie die Oberfläche des Code-basierten Erlebnisses ein. [Weitere Informationen](#surface-definition)

   ![](assets/code-based-campaign-surface.png)

   >[!CAUTION]
   >
   >Stellen Sie sicher, dass der in Ihrer Code-basierten Kampagne verwendete Oberflächen-URI mit dem in Ihrer eigenen Implementierung verwendeten übereinstimmt. Andernfalls werden die Änderungen nicht bereitgestellt.

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

1. Führen Sie die Schritte zum Erstellen einer Kampagne aus, z. B. die Kampagneneigenschaften, [Zielgruppe](../audience/about-audiences.md) und [Zeitplan](../campaigns/create-campaign.md#schedule).

   >[!NOTE]
   >
   >Weitere Informationen zur Konfiguration Ihrer Kampagne finden Sie auf [dieser Seite](../campaigns/get-started-with-campaigns.md).

1. Bearbeiten Sie den Inhalt wie gewünscht mit dem Ausdruckseditor. [Weitere Informationen](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## Bearbeiten des Code-Inhalts {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="Verwenden des Ausdruckseditors"
>abstract="Fügen Sie den Code ein, den Sie als Teil dieser Code-basierten Erlebnisaktion bereitstellen möchten, und bearbeiten Sie ihn."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html?lang=de" text="Erste Schritte mit dem Ausdruckseditor"

1. Wählen Sie auf dem Bildschirm zur Kampagnenbearbeitung die Option **[!UICONTROL Code bearbeiten]**.

   ![](assets/code-based-campaign-edit-code.png)

1. Der [Ausdruckseditor](../personalization/personalization-build-expressions.md) wird geöffnet. Es handelt sich dabei um eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen, mit der Code erstellt werden kann.

1. Der Authoring-Modus kann von HTML auf JSON umgestellt werden und umgekehrt.

   >[!CAUTION]
   >
   >Das Ändern des Authoring-Modus führt zum Verlust des gesamten aktuellen Codes. Stellen Sie daher sicher, dass Sie den Modus wechseln, bevor Sie mit dem Authoring beginnen.

1. Geben Sie Ihren Code nach Bedarf ein. Der [!DNL Journey Optimizer] Ausdruckseditor kann mit allen Personalisierungs- und Bearbeitungsfunktionen genutzt werden. [Weitere Informationen](../personalization/personalization-build-expressions.md)

   ![](assets/code-based-campaign-code-editor.png)

1. In Code-basierten Kampagnen kann die Entscheidungsfunktion für Erlebnisse verwendet werden. Wählen Sie das Symbol **[!UICONTROL Entscheidungen]** in der linken Leiste und klicken Sie auf **[!UICONTROL Entscheidung erstellen]**. [Weitere Informationen](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >Die Offer Decisioning-Funktion ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar.

1. Klicken Sie auf **[!UICONTROL Speichern und Schließen]**, um Ihre Änderungen zu bestätigen.

Sobald Ihre Entwicklungspersonen nun einen API- oder SDK-Aufruf zum Abrufen von Inhalten für die ausgewählte Oberfläche starten, werden die Änderungen auf die Web-Seite oder App angewendet.

## Testen der Code-basierten Kampagne {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Vorschau des Code-basierten Erlebnisses"
>abstract="Eine Simulation, die zeigt, wie das Code-basierte Erlebnis aussehen wird."

Führen Sie die folgenden Schritte aus, um eine Vorschau des geänderten Code-basierten Erlebnisses anzuzeigen. Detaillierte Informationen zur Auswahl von Testprofilen und zur Vorschau Ihres Inhalts finden Sie auf der Seite [Vorschau und Test Ihrer Inhalte](../content-management/preview-test.md).

>[!CAUTION]
>
>Sie müssen über Testprofile verfügen, um simulieren zu können, welche Angebote an sie gesendet werden. Hier erfahren Sie, wie Sie [Testprofile erstellen](../audience/creating-test-profiles.md).

1. Wählen Sie entweder im Ausdruckseditor oder auf dem Bildschirm zur Inhaltsbearbeitung die Option **[!UICONTROL Inhalt simulieren]** aus.

   ![](assets/code-based-campaign-simulate.png)

1. Klicken Sie auf **[!UICONTROL Testprofile verwalten]**, um ein oder mehrere Testprofile auszuwählen.

1. Es wird eine Vorschau des geänderten Code-basierten Erlebnisses angezeigt.

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## Aktivieren der Code-basierten Kampagne {#activate-code-based-campaign}

Sobald Sie Ihre Code-basierte Kampagne definiert und Ihren Inhalt wie gewünscht mit dem [Code-basierten Editor](#edit-code) bearbeitet haben, können Sie sie überprüfen und aktivieren. Führen Sie dazu folgende Schritte durch.

>[!NOTE]
>
>Außerdem kann vor der Aktivierung eine Vorschau des Kampagneninhalts angezeigt werden. [Weitere Informationen](#test-code-based-campaign)

1. Wählen Sie in Ihrer Code-basierten Kampagne die Option **[!UICONTROL Zur Aktivierung überprüfen]**.

   ![](assets/code-based-campaign-review.png)

1. Überprüfen und bearbeiten Sie bei Bedarf Inhalt, Eigenschaften, Oberfläche, Audience und Zeitplan.

1. Wählen Sie **[!UICONTROL Aktivieren]** aus.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Nachdem Sie auf **[!UICONTROL Aktivieren]** geklickt haben, kann es bis zu 1 Minute dauern, bis Änderungen an Code-basierten Kampagnen an Ihrem Standort live sind.

Die Code-basierte Kampagne geht in den **[!UICONTROL Live]**-Status über und ist nun für die ausgewählte Zielgruppe sichtbar. Jede Empfängerin und jeder Empfänger der Kampagne kann die Änderungen sehen.

>[!NOTE]
>
>Wenn ein Zeitplan für die Code-basierte Kampagne definiert wurde, hat sie den Status **[!UICONTROL Geplant]**, bis das Startdatum und die Startzeit erreicht werden.
>
>Wenn Sie eine Code-basierte Kampagne aktivieren, die sich auf dieselben Standorte auswirkt wie eine andere bereits aktive Kampagne, werden alle Änderungen auf die Standorte angewendet.

Weitere Informationen zur Aktivierung von Kampagnen finden Sie in [diesem Abschnitt](../campaigns/review-activate-campaign.md).

## Stoppen einer Code-basierten Kampagne {#stop-code-based-campaign}

Wenn eine Code-basierte Kampagne live ist, kann sie gestoppt werden, um zu verhindern, dass Änderungen für eine Zielgruppe sichtbar werden. Führen Sie dazu folgende Schritte durch.

1. Wählen Sie eine Live-Kampagne aus der Liste aus.

1. Wählen Sie im oberen Menü **[!UICONTROL Kampagne stoppen]** aus.

   ![](assets/code-based-campaign-stop.png)

1. Die hinzugefügten Änderungen sind dann für die von Ihnen definierte Audience nicht mehr sichtbar.

>[!NOTE]
>
>Nachdem eine Code-basierte Kampagne gestoppt wurde, kann sie nicht mehr bearbeitet oder wieder aktiviert werden. Sie können sie nur duplizieren und dann die duplizierte Kampagne aktivieren.

## Code-basierte Kampagnenberichte

Über den Bildschirm Kampagnenzusammenfassung kann auf Code-basierte Kampagnenberichte zugegriffen werden.

Globale Berichte zeigen Ereignisse an, die vor mindestens zwei Stunden aufgetreten sind, und decken Ereignisse über einen ausgewählten Zeitraum ab. Im Vergleich dazu konzentrieren sich Live-Berichte auf Ereignisse, die innerhalb der letzten 24 Stunden stattgefunden haben. Der Zeitraum ab dem Auftreten des Ereignisses beträgt mindestens zwei Minuten.

### Code-basierter Live-Bericht {#live-report-code-based}

Im **[!UICONTROL Live-Bericht]** der Kampagne werden auf der Registerkarte **[!UICONTROL Code-basierte Erlebnisse]** die wichtigsten Informationen zu Ihren Apps oder Web-Seiten aufgeführt. [Weitere Informationen zu Live-Berichten](../reports/campaign-live-report.md)

+++Weitere Informationen zu verschiedenen Metriken und Widgets, die für den Code-basierten Erlebnisbericht verfügbar sind.

Die KPIs der **[!UICONTROL Code-basierten Erlebnisleistung]** geben die wichtigsten Informationen bezüglich der Interaktion der Besucherinnen und Besucher mit den Code-basierten Erlebnissen an, z. B.:

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzenden bereitgestellten Erlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit der App/Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

Der Graph **[!UICONTROL Code-basierte Erlebnis-Zusammenfassung]** zeigt die Entwicklung der Erlebnisse (Impressions, eindeutige Impressions und Interaktionen) für die letzten 24 Stunden an.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### Code-basierter globaler Bericht {#global-report-code-based}

Über die Schaltfläche **[!UICONTROL Bericht anzeigen]** ist der direkte Zugriff in einer Kampagne auf den globalen Bericht der Code-basierten Kampagne möglich. [Weitere Informationen zum globalen Bericht](../reports/campaign-global-report.md)

Im **[!UICONTROL globalen Bericht]** der Kampagne werden auf der Registerkarte **[!UICONTROL Code-basierte Erlebnisse]** die wichtigsten Informationen zu Ihren Apps oder Web-Seiten aufgeführt.

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++Weitere Informationen zu verschiedenen Metriken und Widgets, die für den Code-basierten Erlebnisbericht verfügbar sind.

Die KPIs der **[!UICONTROL Code-basierten Erlebnisleistung]** geben die wichtigsten Informationen bezüglich der Interaktion der Besucherinnen und Besucher mit den Erlebnissen an, z. B.:

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Benutzenden, denen das Erlebnis bereitgestellt wurde.

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzenden bereitgestellten Erlebnisse.

* **[!UICONTROL Interaktionen]**: Prozentsatz der Interaktionen mit der App/Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

Der Graph **[!UICONTROL Code-basierte Erlebnis-Zusammenfassung]** zeigt die Entwicklung der Erlebnisse (eindeutige Impressions, Impressions und Interaktionen) für den betreffenden Zeitraum an.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
