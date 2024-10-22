---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von mehrsprachigen Inhalten mit manueller Übersetzung
description: Erfahren Sie, wie Sie in Journey Optimizer mehrsprachige Inhalte mit manueller Übersetzung erstellen.
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: erste Schritte, Starten, Inhalt, Experiment
exl-id: 6244d717-fbd6-468e-9164-60451d0d62f0
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 8fecd0d4812ba875dba1d47bc32ab08178a13f2c
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 95%

---

# Erstellen von mehrsprachigen Inhalten mit manueller Übersetzung {#multilingual-manual}

>[!AVAILABILITY]
>
>Mehrsprachige Inhalte sind derzeit nur für eine Gruppe von ausgewählten Organisationen verfügbar (begrenzte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.

Mithilfe des manuellen Flusses können Sie Inhalte mühelos direkt in Ihrer E-Mail-, Push-Benachrichtigung- oder SMS-Kampagne und Journey übersetzen. So erhalten Sie präzise Steuerungsmöglichkeiten und Anpassungsoptionen für Ihre mehrsprachigen Nachrichten. Darüber hinaus können Sie mit der Option „HTML importieren“ bereits vorhandene mehrsprachige Inhalte ganz einfach importieren.

Führen Sie die folgenden Schritte aus, um mehrsprachige Inhalte mithilfe der manuellen Übersetzung zu erstellen:

1. [Erstellen Sie Ihr Gebietsschema](#create-locale).

1. [Erstellen Sie Spracheinstellungen](#create-language-settings).

1. [Erstellen von mehrsprachigen Inhalten](#create-a-multilingual-campaign).

## Erstellen eines Gebietsschemas {#create-locale}

Wenn bei der Konfiguration der Spracheinstellungen, wie im Abschnitt [Erstellen von Spracheinstellungen](#language-settings) beschrieben, ein bestimmtes Gebietsschema für mehrsprachige Inhalte nicht verfügbar ist, können Sie über das Menü **[!UICONTROL Übersetzung]** beliebig viele Gebietsschemata erstellen.

1. Greifen Sie im Menü **[!UICONTROL Content Management]** auf **[!UICONTROL Übersetzung]** zu.

1. Klicken Sie in der Registerkarte **[!UICONTROL Gebietsschema-Wörterbuch]** auf **[!UICONTROL Gebietsschema hinzufügen]**.

   ![](assets/locale_1.png)

1. Wählen Sie Ihren Gebietsschema-Code aus der Liste **[!UICONTROL Sprache]** sowie die zugehörige **[!UICONTROL Region]** aus.

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihr Gebietsschema zu erstellen.

   ![](assets/locale_2.png)

## Erstellen von Spracheinstellungen {#language-settings}

In diesem Abschnitt können Sie Ihre Primärsprache und die zugehörigen Gebietsschemata zur Verwaltung Ihrer mehrsprachigen Inhalte festlegen. Sie können auch das Attribut auswählen, mit dem Sie nach Informationen zur Profilsprache suchen möchten

1. Öffnen Sie im Menü **[!UICONTROL Administration]** die Option **[!UICONTROL Kanal]** > **[!UICONTROL Allgemeine Einstellungen]**.

1. Klicken Sie im Menü **[!UICONTROL Spracheinstellungen]** auf **[!UICONTROL Spracheinstellungen erstellen]**.

   ![](assets/language_settings_1.png)

1. Geben Sie den Namen Ihrer **[!UICONTROL Spracheinstellungen]** ein.

1. Wählen Sie die mit diesen Einstellungen verknüpften **[!UICONTROL Gebietsschemata]**. Sie können maximal 50 Gebietsschemata hinzufügen.

   Wenn ein **[!UICONTROL Gebietsschema]** fehlt, können Sie es über das Menü **[!UICONTROL Übersetzung]** oder per API manuell im Voraus erstellen. Siehe [Erstellen eines neuen Gebietsschemas](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. Wählen Sie im Menü **[!UICONTROL Versandvoreinstellung]** das Attribut aus, mit dem Sie nach Informationen zu Profilsprachen suchen möchten.

   ![](assets/multilingual-settings-3.png)

1. Klicken Sie neben Ihrem **[!UICONTROL Gebietsschema]** auf **[!UICONTROL Bearbeiten]**, um es weiter zu personalisieren und **[!UICONTROL Profilvoreinstellungen]** hinzuzufügen.

   ![](assets/multilingual-settings-4.png)

1. Wählen Sie andere **[!UICONTROL Gebietsschemata]** aus der Dropdown-Liste „Profileinstellungen“ und klicken Sie auf **[!UICONTROL Profile hinzufügen]**.

1. Öffnen Sie das erweiterte Menü Ihres **[!UICONTROL Gebietsschemas]**, um Ihr **[!UICONTROL primäres Gebietsschema]** festzulegen, d. h. die Standardsprache, wenn das Profilattribut nicht angegeben ist.

   Sie können Ihr Gebietsschema über dieses erweiterte Menü auch löschen.

   ![](assets/multilingual-settings-5.png)

1. Klicken Sie auf **[!UICONTROL Senden]**, um Ihre **[!UICONTROL Spracheinstellungen]** zu erstellen.

<!--
1. Access the **[!UICONTROL channel configurations]** menu and create a new channel configuration or select an existing one.


1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Erstellen von mehrsprachigen Inhalten {#create-multilingual-campaign}

Nach der Einrichtung Ihrer mehrsprachigen Inhalte können Sie Ihre Kampagne oder Journey gestalten und die Inhalte für jedes Ihrer ausgewählten Gebietsschemata anpassen.

1. Erstellen und konfigurieren Sie zunächst Ihre E-Mail-, SMS- oder Push-Benachrichtigungs-[Kampagne](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journeys-message.md) entsprechend Ihren Anforderungen.

   >[!AVAILABILITY]
   >
   >Wir empfehlen, pro Journey nur ein Übersetzungsprojekt einzuschließen.

1. Erstellen oder importieren Sie Ihren ursprünglichen Inhalt und personalisieren Sie ihn nach Bedarf.

1. Nachdem der Hauptinhalt erstellt wurde, klicken Sie auf **[!UICONTROL Speichern]** und gehen Sie zurück zum Kampagnenkonfigurationsbildschirm.

   ![](assets/multilingual-campaign-2.png)

1. Klicken Sie auf **[!UICONTROL Sprachen hinzufügen]** und wählen Sie Ihre zuvor erstellten **[!UICONTROL Spracheinstellungen]** aus. [Weitere Informationen](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Öffnen Sie die erweiterten Einstellungen des Menüs **[!UICONTROL Gebietsschemata]** und wählen Sie **[!UICONTROL Hauptinhalt in alle Gebietsschemata kopieren]**.

   ![](assets/multilingual-campaign-4.png)

1. Nachdem Sie Ihren Hauptinhalt in alle ausgewählten **[!UICONTROL Gebietsschemata]**, dupliziert haben, öffnen Sie die einzelnen Gebietsschemata und klicken Sie auf **[!UICONTROL E-Mail-Text bearbeiten]**, um Ihren Inhalt zu übersetzen.

   ![](assets/multilingual-campaign-5.png)

1. Sie können Gebietsschemata über das Menü **[!UICONTROL Weitere Aktionen]** des ausgewählten Gebietsschemas aktivieren und deaktivieren.

   ![](assets/multilingual-campaign-6.png)

1. Um Ihre mehrsprachige Konfiguration zu deaktivieren, klicken Sie auf **[!UICONTROL Sprachen hinzufügen]** und wählen Sie die Sprache aus, die Sie als Landessprache beibehalten möchten.

   ![](assets/multilingual-campaign-7.png)

1. Klicken Sie auf **[!UICONTROL Zum Aktivieren überprüfen]**, um eine Zusammenfassung der Kampagne anzuzeigen.

   In der Zusammenfassung können Sie die Kampagne bei Bedarf ändern und überprüfen, ob ein Parameter falsch ist oder fehlt.

1. Durchsuchen Sie Ihre mehrsprachigen Inhalte, um das Rendering in den einzelnen Sprachen anzuzeigen.

   ![](assets/multilingual-campaign-8.png)

Jetzt können Sie Ihre Kampagne oder Journey aktivieren. Nach dem Versand können Sie die Wirkung Ihrer mehrsprachigen Journey oder Kampagnen in den Berichten ermitteln.

>[!IMPORTANT]
>
> Wenn Ihre Kampagne einer Validierungsrichtlinie unterliegt, müssen Sie eine Validierung anfordern, um Ihre mehrsprachige Kampagne oder Journey senden zu können. [Weitere Informationen](../test-approve/gs-approval.md)

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
