---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer LINE-Nachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine LINE-Nachricht erstellen.
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: a93d4dc9-f0e9-400c-b9a4-6cdac84390fd
TQID: https://experienceleague.adobe.com/OgI9e9LWYpO8nXHQXoDK-y0ys-EpHJzaFRHx9V9pAus
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 8f016fe08e76f896eeb71b96e582e4e7e8fc3c9f
workflow-type: tm+mt
source-wordcount: 782
ht-degree: 94%

---

# Erstellen einer LINE-Nachricht {#create-line}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Fügen Sie einer Journey oder Kampagne eine LINE-Aktion hinzu und erstellen Sie personalisierte Inhalte, von Text und Aufklebern bis hin zu Bildern, Videos, Standorten und Flex-Nachrichten, damit Sie Kundinnen und Kunden über LINE ansprechen können.

>[!ENDSHADEBOX]

## Hinzufügen einer LINE-Nachricht {#create-line-journey-campaign}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_line"
>title="LINE-Aktion"
>abstract="Eine LINE-Kanalaktion sendet eine LINE-Nachricht an Profile, wenn sie diesen Schritt der Journey erreichen. Das Label bezeichnet die Aktivität auf der Journey-Arbeitsfläche und die Aktion verweist auf eine LINE-Konfiguration, die den bereitgestellten Inhalt definiert. Der Abschnitt **Optimierung** kann Inhaltsexperimente oder Targeting-Regeln enthalten, der Abschnitt **Mehrsprachig** kann Inhalte in mehreren Sprachen bereitstellen, und der Abschnitt **Timeout oder Fehler** kann einen alternativen Pfad definieren, wenn die Aktion fehlschlägt."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="Erste Schritte mit Kanalaktionen"

Auf den folgenden Registerkarten finden Sie weitere Informationen dazu, wie Sie eine LINE-Nachricht in einer Kampagne oder Journey hinzufügen.

>[!BEGINTABS]

>[!TAB Hinzufügen einer LINE-Nachricht zu einer Journey]

1. Öffnen Sie Ihre Journey und ziehen Sie eine Aktivität **LINE** per Drag-and-Drop aus dem Abschnitt **Aktionen** der Palette.

   ![](assets/jo-line-1.png)

1. Geben Sie allgemeine Informationen (Label, Beschreibung, Kategorie) zu Ihrer Nachricht ein und wählen Sie dann die zu verwendende Konfiguration aus.

   Weitere Informationen zur Konfiguration der Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

   Das Feld **[!UICONTROL Konfiguration]** ist standardmäßig mit der letzten Konfiguration für den Kanal vorausgefüllt, den die Benutzerin oder der Benutzer verwendet hat.

Sie können jetzt mit der Erstellung des Inhalts Ihrer LINE-Nachricht beginnen, indem Sie auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** klicken, wie unten beschrieben.

>[!TAB Hinzufügen einer LINE-Nachricht zu einer Kampagne]

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

1. Wählen Sie den Typ der Kampagne aus, die Sie ausführen möchten.

   * **Geplant – Marketing**: die Kampagne wird sofort oder an einem bestimmten Datum ausgeführt. Geplante Kampagnen dienen dem Versand von Marketing-Nachrichten. Sie werden über die Benutzeroberfläche konfiguriert und ausgeführt.

   * **API-ausgelöst – Marketing/Transaktion**: die Kampagne wird mithilfe eines API-Aufrufs ausgeführt. API-ausgelöste Kampagnen zielen auf den Versand von Nachrichten des Typs „Marketing“ oder „Transaktion“ ab. Beim Typ „Transaktion“ handelt es sich um Nachrichten, die nach einer von einem Kontakt durchgeführten Aktion verschickt werden: Zurücksetzen des Passworts und Verlassen des Warenkorbs.

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen zu definieren. [Weitere Informationen](../audience/about-audiences.md).

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen in der ausgewählten Zielgruppe verwendet werden soll. [Weitere Informationen](../event/about-creating.md#select-the-namespace).

1. Wählen Sie im Abschnitt **[!UICONTROL Aktionen]** die Option **[!UICONTROL LINE]** und dann eine Konfiguration aus oder erstellen Sie eine neue Konfiguration.

   Auf [dieser Seite](line-configuration.md) erfahren Sie mehr über die LINE-Konfiguration.

   ![](assets/campaign-line-1.png)

1. Klicken Sie auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen und Abwandlungen zu erstellen, deren Performance zu messen und die beste Option für Ihre Zielgruppe zu ermitteln. [Weitere Informationen](../content-management/content-experiment.md)

1. Im Bereich **[!UICONTROL Tracking von Aktionen]** können Sie angeben, ob Sie Klicks auf Links in Ihrer SMS-Nachricht verfolgen möchten.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/create-campaign.md#schedule), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

1. Wählen Sie aus dem Menü **[!UICONTROL Aktions-Trigger]** die **[!UICONTROL Häufigkeit]** Ihrer SMS-Nachricht:

   * Einmal
   * Täglich
   * Wöchentlich
   * Monat

Sie können jetzt mit der Erstellung des Inhalts Ihrer Textnachricht beginnen, indem Sie die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** anklicken, wie unten beschrieben.

>[!ENDTABS]

## Definieren Ihrer LINE-Inhalte{#line-content}

Adobe Journey Optimizer unterstützt die folgenden Nachrichtentypen für LINE:

* **Text**: Senden von einfachen oder formatierten Textnachrichten.
* **Aufkleber**: Integrieren Sie die nativen Aufkleber von LINE, um Charakter und Ausdruckskraft hinzuzufügen.
* **Bilder**: Hängen Sie Bilder an, um die visuelle Attraktivität zu verbessern.
* **Videos**: Geben Sie Videoinhalte für dynamische Kommunikation frei.
* **Standorte**: Senden Sie Standortinformationen mit Karten.
* **Vorlagen**: Verwenden Sie vordefinierte Vorlagen für konsistentes Messaging.
* **Flex-Nachrichten**: Erstellen Sie komplexe Layouts mit Rich-Content mithilfe von JSON-basierten Flex-Nachrichten.

Diese Nachrichtentypen können konfiguriert werden, indem der JSON-Inhalt direkt bearbeitet wird, was dynamische und personalisierte Messaging-Strategien ermöglicht.

Gehen Sie wie folgt vor, um Ihren LINE-Inhalt zu konfigurieren.

1. Klicken Sie auf dem Bildschirm der Journey- oder Kampagnenkonfiguration auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**, um den Inhalt der Textnachricht zu konfigurieren.

1. Klicken Sie auf **[!UICONTROL Code bearbeiten]**, um JSON-Inhalte zu bearbeiten.

1. Verwenden Sie den Personalisierungseditor, um Inhalte zu definieren und Personalisierung sowie dynamischen Inhalt hinzuzufügen. Sie können jedes Attribut verwenden, wie etwa Profilname oder Stadt. Sie können auch bedingte Regeln definieren. Auf den folgenden Seiten erfahren Sie mehr über [Personalisierung](../personalization/personalize.md) und [dynamische Inhalte](../personalization/get-started-dynamic-content.md) im Personalisierungseditor.

1. Klicken Sie auf **[!UICONTROL Speichern]** und überprüfen Sie Ihre Nachricht in der Vorschau.

1. Verwenden Sie **[!UICONTROL Inhalt simulieren]**, um den Inhalt Ihrer LINE-Nachricht und den personalisierten Inhalt in der Vorschau anzuzeigen. [Weitere Informationen](send-line.md)

Sobald Sie Ihre Tests durchgeführt und den Inhalt validiert haben, können Sie Ihre LINE-Nachricht an Ihre Zielgruppe senden. Diese Schritte werden auf [dieser Seite](send-line.md) im Detail beschrieben.

Nach dem Versand können Sie die Wirkung Ihrer LINE-Nachricht in den Kampagnen- oder Journey-Berichten messen. Weiterführende Informationen zum Reporting finden Sie in [diesem Abschnitt](../reports/campaign-global-report-cja.md).
