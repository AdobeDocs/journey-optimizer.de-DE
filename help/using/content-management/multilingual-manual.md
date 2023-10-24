---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit mehrsprachigen Inhalten
description: Weitere Informationen zu mehrsprachigen Inhalten in Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: erste Schritte, Start, Inhalt, Experiment
hide: true
hidefromtoc: true
source-git-commit: 90aeb777276e1e72c3099272f00e3700e06c83bf
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 7%

---

# Mehrsprachige Inhalte mit manueller Übersetzung erstellen {#multilingual-manual}

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

* [Erste Schritte mit mehrsprachigen Inhalten](multilingual-gs.md)
* **[Mehrsprachige Inhalte mit manueller Übersetzung erstellen](multilingual-manual.md)**
* [Mehrsprachige Inhalte mit automatisierter Übersetzung erstellen](multilingual-automated.md)
* [Mehrsprachiger Kampagnenbericht](multilingual-report.md)

>[!ENDSHADEBOX]

Mithilfe des manuellen Workflows können Sie Ihren Inhalt mühelos direkt in Ihre E-Mail-, Push-Benachrichtigung- oder SMS-Kampagne übersetzen, wodurch Sie präzise Steuerungsmöglichkeiten und Anpassungsoptionen für Ihre mehrsprachigen Nachrichten erhalten. Darüber hinaus können Sie bereits vorhandene mehrsprachige Inhalte mit der Option HTML importieren einfach importieren.

Führen Sie die folgenden Schritte aus, um mehrsprachige Inhalte mit manueller Übersetzung zu erstellen:

1. [Gebietsschema erstellen](#create-locale).

1. [Spracheinstellungen erstellen](#create-language-settings).

1. [Mehrsprachige Kampagne erstellen](#create-a-multilingual-campaign).

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

Nach der Einrichtung Ihres mehrsprachigen Inhalts können Sie Ihre Kampagne entwerfen und den Inhalt für jedes Ihrer ausgewählten Gebietsschemas anpassen.

1. Erstellen und konfigurieren Sie zunächst Ihre E-Mail-, SMS- oder Push-Benachrichtigungs-Kampagne entsprechend Ihren Anforderungen. [Weitere Informationen](../campaigns/create-campaign.md)

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

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
