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
source-git-commit: c858d16ec520418148fb28ad2ecec0d3a6377ba9
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 34%

---

# Erstellen von mehrsprachigen Inhalten mit manueller Übersetzung {#multilingual-manual}

>[!IMPORTANT]
>
>Für den manuellen Ablauf müssen Benutzer über die Berechtigung **[!UICONTROL Spracheinstellungen verwalten]** verfügen.

Mithilfe des manuellen Workflows können Sie mühelos Ihre Inhalte direkt in Ihre Kampagnen und Journey übersetzen, wodurch Sie präzise Steuerungsmöglichkeiten und Anpassungsoptionen für Ihre mehrsprachigen Nachrichten erhalten. Darüber hinaus können Sie mit der Option „HTML importieren“ bereits vorhandene mehrsprachige Inhalte ganz einfach importieren.

Führen Sie die folgenden Schritte aus, um mehrsprachige Inhalte mithilfe der manuellen Übersetzung zu erstellen:

1. [Anbieter hinzufügen (optional)](multilingual-provider.md)

1. [Gebietsschemata hinzufügen (optional)](multilingual-locale.md)

1. [Erstellen von Spracheinstellungen](#create-language-settings)

1. [Erstellen von mehrsprachigen Inhalten](#create-a-multilingual-campaign)

## Erstellen von Spracheinstellungen {#language-settings}

In diesem Abschnitt können Sie Ihre unterschiedlichen Gebietsschemata zur Verwaltung Ihrer mehrsprachigen Inhalte festlegen. Sie können auch das Attribut auswählen, mit dem Sie nach Informationen zur Profilsprache suchen möchten

1. Öffnen Sie im Menü **[!UICONTROL Administration]** die Option **[!UICONTROL Kanal]** > **[!UICONTROL Allgemeine Einstellungen]**.

1. Klicken Sie im Menü **[!UICONTROL Spracheinstellungen]** auf **[!UICONTROL Spracheinstellungen erstellen]**.

   ![](assets/language_settings_1.png)

1. Geben Sie den Namen Ihrer **[!UICONTROL Spracheinstellungen]** ein und wählen Sie **[!UICONTROL Manuelle Übersetzung]**.

1. Wählen Sie die mit diesen Einstellungen verknüpften **[!UICONTROL Gebietsschemata]**. Sie können maximal 50 Gebietsschemata hinzufügen.

   Wenn ein **[!UICONTROL Gebietsschema]** fehlt, können Sie es über das Menü **[!UICONTROL Übersetzung]** oder per API manuell im Voraus erstellen. Siehe [Erstellen eines neuen Gebietsschemas](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. Wählen Sie eine **[!UICONTROL Fallback-Voreinstellungen]** aus, um eine Sicherungsoption für den Fall zu definieren, dass ein Profil die für die Inhaltsbereitstellung erforderlichen Kriterien nicht erfüllt.

   Beachten Sie, dass die Kampagne oder Journey nicht gesendet wird, wenn keine Ausweichoption ausgewählt ist.

1. Wählen Sie aus den folgenden Optionen Ihre Versandpräferenz aus:

   * **[!UICONTROL Wählen Sie die Attribute der Sprache der Profilsprache aus]**
   * **[!UICONTROL Erstellen benutzerdefinierter bedingter Regeln]**

1. Wenn Sie &quot;**[!UICONTROL Profilattsprachpräferenzattribute auswählen]**&quot;auswählen, wählen Sie das relevante Attribut aus dem Menü &quot;**[!UICONTROL Profilattribute für Sprachpräferenzen]**&quot;, um nach Informationen zur Profilsprache zu suchen.

   ![](assets/multilingual-settings-3.png)

1. Wenn Sie **[!UICONTROL Benutzerdefinierte bedingte Regeln erstellen]** auswählen, wählen Sie das Gebietsschema aus, für das Sie Bedingungen erstellen möchten. Erstellen Sie dann Regeln basierend auf Faktoren wie Standort des Benutzers, Spracheinstellungen oder anderen kontextbezogenen Elementen.

   ![](assets/multilingual-settings-4.png)

1. Beginnen Sie mit der Erstellung von Bedingungen, indem Sie ein Attribut, ein Ereignis oder eine Zielgruppe hinzufügen, um Ihre Zielgruppe zu definieren.

   >[!IMPORTANT]
   >
   >Kontextdaten sind ausschließlich für die Kanäle Web, In-App, Code-basiertes Erlebnis und Inhaltskarten verfügbar. Wenn die Kampagne bzw. die Journey für die Kanäle E-Mail, SMS, Push-Benachrichtigung oder Briefpost ohne zusätzliche Attribute verwendet wird, wird sie in der Sprache der ersten Listenoption versendet.

   ![](assets/multilingual-settings-6.png)

   +++ Voraussetzungen für die Verwendung kontextbezogener Ereignisse in Ihren Bedingungen

   Wenn Benutzer Ihren Inhalt anzeigen, wird eine Personalisierungsanfrage zusammen mit dem Erlebnisereignis gesendet. Um Kontextdaten in Ihren Bedingungen zu nutzen, müssen Sie zusätzliche Daten an die Payload der Personalisierungsanfrage anhängen. Erstellen Sie dazu in der Adobe Experience Platform-Datenerfassung eine Regel, um Folgendes anzugeben: Wenn eine Personalisierungsanforderung gesendet wird, fügen Sie der Anforderung DANN zusätzliche Daten hinzu und definieren Sie das Attribut, das mit dem Sprachfeld in Ihrem Schema übereinstimmen soll.

   >[!NOTE]
   >
   >Diese Voraussetzungen sind nur für die Kanäle In-App und Inhaltskarten erforderlich.

   1. Rufen Sie in der Adobe Experience Platform-Datenerfassung das Menü **[!UICONTROL Regeln]** auf und erstellen Sie eine neue Regel. Detaillierte Informationen zum Erstellen von Regeln finden Sie in der [!DNL Adobe Experience Platform] [Dokumentation zur Datenerfassung](https://experienceleague.adobe.com/en/docs/experience-platform/collection/e2e#create-a-rule){target="_blank"} .

   2. Fügen Sie im Abschnitt **[!UICONTROL IF]** der Regel ein Ereignis hinzu, das wie folgt konfiguriert wurde:

      ![](assets/multilingual-experience-events-rule-if.png)

      * Wählen Sie die **[!UICONTROL Erweiterung]** aus, mit der Sie arbeiten.
      * Wählen Sie im Feld **[!UICONTROL Ereignistyp]** die Option &quot;AEP-Anforderungsereignis&quot;aus.
      * Wählen Sie im rechten Bereich &quot;XDM Event Type equals personalization.request&quot;
      * Klicken Sie zur Bestätigung auf die Schaltfläche **[!UICONTROL Änderungen beibehalten]** .

   3. Fügen Sie im Abschnitt **[!UICONTROL THEN]** der Regel eine Aktion hinzu, die wie folgt konfiguriert wurde:

      ![](assets/multilingual-experience-events-rule-then.png)

      * Wählen Sie die **[!UICONTROL Erweiterung]** aus, mit der Sie arbeiten.
      * Wählen Sie im Feld **[!UICONTROL Aktionstyp]** die Option &quot;Daten anhängen&quot;aus.
      * Stellen Sie im Abschnitt JSON-Payload sicher, dass das Attribut, mit dem die zu verwendende Sprache abgerufen wird (im Beispiel unter &quot;Sprache&quot;), mit dem Namen des Attributs übereinstimmt, das im Schema angegeben ist, in das Ihr Datenerfassungsdatastream fließt.

        ```JSON
        {
            "xdm":{
                "application":{
                    "_dc":{
                        "language":"{%%Language%%}"
                    }
                }
            }
        }
        ```

      * Klicken Sie auf die Schaltfläche **[!UICONTROL Änderungen beibehalten]** , um Ihre Regel zu bestätigen und zu speichern.

+++

1. Ziehen Sie die Gebietsschemata in den Arbeitsbereich, um sie neu anzuordnen und ihre Priorität in der Liste zu verwalten.

1. Um ein Gebietsschema zu löschen, klicken Sie auf das Papierkorbsymbol.

   ![](assets/multilingual-settings-5.png)

1. Klicken Sie auf **[!UICONTROL Senden]**, um Ihre **[!UICONTROL Spracheinstellungen]** zu erstellen.

Beachten Sie, dass Sie nach der Einrichtung Ihrer Spracheinstellungen nicht mehr die Möglichkeit haben, diese zu bearbeiten.

<!--
1. Access the **[!UICONTROL channel configurations]** menu and create a new channel configuration or select an existing one.


1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Erstellen von mehrsprachigen Inhalten {#create-multilingual-campaign}

Nach der Einrichtung Ihrer mehrsprachigen Inhalte können Sie Ihre Kampagne oder Journey gestalten und die Inhalte für jedes Ihrer ausgewählten Gebietsschemata anpassen.

1. Erstellen und konfigurieren Sie zunächst Ihre E-Mail-, SMS- oder Push-Benachrichtigungs-[Kampagne](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journeys-message.md) entsprechend Ihren Anforderungen.

   >[!IMPORTANT]
   >
   >Wir empfehlen, pro Journey nur ein Übersetzungsprojekt einzuschließen.

1. Erstellen oder importieren Sie Ihren ursprünglichen Inhalt und personalisieren Sie ihn nach Bedarf.

1. Klicken Sie nach der Erstellung des Inhalts auf **[!UICONTROL Speichern]** und gehen Sie zurück zum Konfigurationsbildschirm der Kampagne.

   ![](assets/multilingual-campaign-2.png)

1. Klicken Sie auf **[!UICONTROL Sprachen hinzufügen]** und wählen Sie Ihre zuvor erstellten **[!UICONTROL Spracheinstellungen]** aus. [Weitere Informationen](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Wählen Sie aus dem Dropdown-Menü das gewünschte Gebietsschema aus, das auf den vorhandenen erstellten Inhalt angewendet werden soll.

1. Greifen Sie auf die erweiterten Einstellungen des Menüs **[!UICONTROL Gebietsschemata]** zu und wählen Sie **[!UICONTROL In alle Gebietsschemata kopieren]**.

   ![](assets/multilingual-campaign-4.png)

1. Nachdem Ihr Inhalt nun in den ausgewählten **[!UICONTROL Gebietsschemata]** dupliziert wurde, greifen Sie auf jedes Gebietsschema zu und klicken Sie auf **[!UICONTROL E-Mail-Hauptteil bearbeiten]** , um den Inhalt zu übersetzen.

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
