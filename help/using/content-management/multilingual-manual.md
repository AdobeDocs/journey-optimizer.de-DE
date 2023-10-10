---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit mehrsprachigen Inhalten
description: Weitere Informationen zu mehrsprachigen Inhalten in Journey Optimizer
feature: Multilingual
topic: Content Management
role: User
level: Beginner
keywords: erste Schritte, Start, Inhalt, Experiment
hide: true
hidefromtoc: true
source-git-commit: 3b1acd7ada0637ce22e360e6e1bb35921dde2315
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 15%

---

# Mehrsprachige Inhalte erstellen {#multilingual}

Die mehrsprachige Funktion ermöglicht es Ihnen, mühelos Inhalte in mehreren Sprachen innerhalb einer Kampagne zu erstellen. Mit dieser Funktion können Sie bei der Bearbeitung Ihrer Kampagne zwischen Sprachen wechseln, den gesamten Bearbeitungsvorgang optimieren und Ihre Fähigkeit zur effizienten Verwaltung mehrsprachiger Inhalte verbessern.

## Gebietsschema erstellen {#create-locale}

Beim Konfigurieren der Spracheinstellungen, wie im Abschnitt [Spracheinstellungen erstellen](#language-settings) Wenn für Ihre mehrsprachigen Inhalte kein bestimmtes Gebietsschema verfügbar ist, können Sie mit der Variablen **[!UICONTROL Übersetzung]** Menü.

1. Aus dem **[!UICONTROL Administration]** Menü, Zugriff **[!UICONTROL Kanal]**.

   Im Menü Übersetzungen können Sie auf die Liste der aktivierten Gebietsschemata zugreifen.

1. Aus dem **[!UICONTROL Gebietsschema-Wörterbuch]** Registerkarte, klicken **[!UICONTROL Gebietsschema hinzufügen]**.

   ![](assets/locale_1.png)

1. Wählen Sie Ihren Gebietsschema-Code aus der **[!UICONTROL Sprache]** und der zugehörigen **[!UICONTROL Region]**.

1. Klicks **[!UICONTROL Speichern]** , um Ihr Gebietsschema zu erstellen.

   ![](assets/locale_2.png)

## Spracheinstellungen erstellen {#language-settings}

In diesem Abschnitt können Sie Ihre Primärsprache und die zugehörigen Gebietsschemata zur Verwaltung Ihrer mehrsprachigen Inhalte festlegen. Sie können auch das Attribut auswählen, mit dem Sie Informationen zur Profilsprache nachschlagen möchten

1. Aus dem **[!UICONTROL Administration]** Menü, Zugriff **[!UICONTROL Kanal]**.

1. Im **[!UICONTROL Spracheinstellungen]** Menü, klicken **[!UICONTROL Spracheinstellungen erstellen]**.

   ![](assets/multilingual-settings-1.png)

1. Geben Sie den Namen Ihrer **[!UICONTROL Spracheinstellungen]**.

1. Wählen Sie die **[!UICONTROL Gebietsschemata]** mit diesen Einstellungen verknüpft sind. Sie können maximal 50 Gebietsschemata hinzufügen.

   Wenn eine **[!UICONTROL Gebietsschema]** fehlt, können Sie es manuell im Voraus erstellen über **[!UICONTROL Übersetzung]** Menü oder nach API. Siehe Abschnitt [Neues Gebietsschema erstellen](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. Aus dem **[!UICONTROL Versandpräferenz]** wählen Sie das Attribut aus, nach dem Sie nach Informationen zu Profilsprachen suchen möchten.

   ![](assets/multilingual-settings-3.png)

1. Klicks **[!UICONTROL Bearbeiten]** neben **[!UICONTROL Gebietsschema]** , um sie weiter zu personalisieren und hinzuzufügen **[!UICONTROL Profilvoreinstellungen]**.

   ![](assets/multilingual-settings-4.png)

1. Andere auswählen **[!UICONTROL Gebietsschemata]** Wählen Sie aus der Dropdown-Liste Profileinstellungen und klicken Sie auf **[!UICONTROL Profile hinzufügen]**.

1. Greifen Sie auf das erweiterte Menü Ihrer **[!UICONTROL Gebietsschema]** , um **[!UICONTROL Primäres Gebietsschema]**, d. h. die Standardsprache, wenn das Profilattribut nicht angegeben ist.

   Sie können Ihr Gebietsschema auch über dieses erweiterte Menü löschen.

   ![](assets/multilingual-settings-5.png)

1. Klicks **[!UICONTROL Einsenden]** , um **[!UICONTROL Spracheinstellungen]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Mehrsprachige Kampagne erstellen {#create-multilingual-campaign}

1. Erstellen und konfigurieren Sie zunächst Ihre Kampagne entsprechend Ihren Anforderungen. [Weitere Informationen](../campaigns/create-campaign.md)

1. Navigieren Sie zum **[!UICONTROL Aktionen]** und wählen Sie **[!UICONTROL Inhalt bearbeiten]**.

   ![](assets/multilingual-campaign-1.png)

1. Erstellen oder importieren Sie Ihren ursprünglichen Inhalt und personalisieren Sie ihn nach Bedarf.

1. Nachdem der Hauptinhalt erstellt wurde, klicken Sie auf **[!UICONTROL Speichern]** und gehen Sie zurück zum Kampagnenkonfigurationsbildschirm.

   ![](assets/multilingual-campaign-2.png)

1. Klicks **[!UICONTROL Sprachen hinzufügen]** und wählen Sie die zuvor erstellte **[!UICONTROL Spracheinstellungen]**. [Weitere Informationen](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Greifen Sie auf die erweiterten Einstellungen der **[!UICONTROL Gebietsschemata]** Menü und wählen Sie **[!UICONTROL Primär in alle Gebietsschemata kopieren]**.

   ![](assets/multilingual-campaign-4.png)

1. Jetzt, da Ihr Hauptinhalt in Ihrem ausgewählten  **[!UICONTROL Gebietsschemata]**, öffnen Sie jedes Gebietsschema und klicken Sie auf **[!UICONTROL Bearbeiten des E-Mail-Hauptteils]** , um Ihren Inhalt zu übersetzen.

   ![](assets/multilingual-campaign-5.png)

1. Sie können Gebietsschemata mit dem **[!UICONTROL Mehr Aktionen]** des ausgewählten Gebietsschemas.

   ![](assets/multilingual-campaign-6.png)

1. Um Ihre mehrsprachige Konfiguration zu deaktivieren, klicken Sie auf **[!UICONTROL Sprachen hinzufügen]** und wählen Sie die Sprache aus, die Sie als Landessprache beibehalten möchten.

   ![](assets/multilingual-campaign-7.png)

1. Klicks **[!UICONTROL Aktivieren]** um eine Zusammenfassung der Kampagne anzuzeigen.

   In der Zusammenfassung können Sie die Kampagne bei Bedarf ändern und überprüfen, ob ein Parameter falsch ist oder fehlt.

1. Durchsuchen Sie Ihre mehrsprachigen Inhalte, um das Rendering in den einzelnen Sprachen anzuzeigen.

   ![](assets/multilingual-campaign-8.png)

1. Vergewissern Sie sich, dass Ihre Kampagne korrekt konfiguriert ist, und klicken Sie dann auf **[!UICONTROL Aktivieren]**.

Ihre Kampagne ist jetzt aktiviert. Die in der Kampagne konfigurierte Nachricht wird sofort oder am angegebenen Datum gesendet. Beachten Sie, dass Ihre Kampagne, sobald sie live ist, nicht mehr geändert werden kann. Um Inhalte wiederzuverwenden, können Sie Ihre Kampagne duplizieren.

Nach dem Versand können Sie die Wirkung Ihrer Kampagnen in den Kampagnenberichten messen.

## Mehrsprachiger Kampagnenbericht {#multilingual-campaign-report}

Globale Berichte, auf die über das **Ganzzeit** -Registerkarte Ereignisse anzeigen, die mindestens vor zwei Stunden aufgetreten sind, und Ereignisse über einen ausgewählten Zeitraum abdecken. Über die Schaltfläche **[!UICONTROL Bericht anzeigen]** ist der direkte Zugriff in einer Campaign-Instanz auf den globalen Bericht in Campaign möglich.

Weitere Informationen zu den im Campaign-Bericht verfügbaren Daten finden Sie unter [diese Seite](../reports/campaign-global-report.md).

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für Ihren mehrsprachigen Inhalt verfügbar sind.

![](assets/report_multilingual.png)

Die **[!UICONTROL Versandstatistiken von E-Mails nach Sprachen]** Widget erläutert den Erfolg Ihres Versands in Abhängigkeit von Ihrer **[!UICONTROL Gebietsschemata]**:

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

Die **[!UICONTROL Statistiken des E-Mail-Trackings nach Sprachen]** Widget enthält die für die Empfängeraktivität für Ihren Versand verfügbaren Daten. **[!UICONTROL Gebietsschemata]**:

* **[!UICONTROL Abmeldungen]**: Anzahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der Nachricht.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt.
+++


<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

# Translation project/ Create translation project:

1. From the Translation projects menu, click Create project.
1. Type-in a Name and Description.
1. Select the Source locale.
1. Click Add language to access the menu and define the languages for your translation project.
1. Select from the list your Target locale(s) and choose which Translation provider you want to use.
1. Click Add language when you finished linking your Target locale with the correct Translation provider.
1. Click Save.
1. From the Advanced menu of your Translation project, you can choose to Edit, deactive or delete it.
-->
