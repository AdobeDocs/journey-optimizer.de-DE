---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer Briefpostnachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine Direkt-Mail-Nachricht erstellen
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: Direkt-Mail, Nachricht, Kampagne
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
TQID: https://experienceleague.adobe.com/vn-PhvuksTX-ALADGGwGlvtp7-dTgjFVsIVvucAjLa8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 675606750af67b398f18646dddf901778625fb30
workflow-type: tm+mt
source-wordcount: 1232
ht-degree: 66%

---

# Erstellen einer Briefpostnachricht {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Erstellung von Briefpost"
>abstract="Erstellen Sie Direkt-Mail-Nachrichten in geplanten Kampagnen und Journeys und erstellen Sie die von Direkt-Mail-Anbietern benötigten Extraktionsdateien, um E-Mails an Ihre Kundinnen und Kunden zu senden."

>[!CONTEXTUALHELP]
>id="ajo_journey_direct_mail"
>title="Endaktivität"
>abstract="Direkt-Mail ist ein Offline-Kanal, mit dem Sie die Extraktionsdateien personalisieren und generieren können, die Direkt-Mail-Drittanbieter zum Senden von Nachrichten an Ihre Kunden und Kundinnen benötigen."

Erstellen Sie zum Erstellen von Briefpostnachrichten eine geplante Kampagne oder eine Journey und konfigurieren Sie die Extraktionsdatei. Diese Datei wird von Briefpost-Dienstleistern benötigt, um E-Mails an Ihre Kundinnen bzw. Kunden zu senden.

>[!IMPORTANT]
>
>Bevor Sie eine Briefpostnachricht senden, stellen Sie sicher, dass Sie Folgendes konfiguriert haben:
>
>1. Eine [Dateirouting-Konfiguration](../direct-mail/direct-mail-configuration.md#file-routing-configuration), die den Server angibt, auf den die Extraktionsdatei hochgeladen und gespeichert werden soll,
>1. Eine [Konfiguration für Direkt-Mail-Nachrichten](../direct-mail/direct-mail-configuration.md#direct-mail-surface), die auf die Datei-Routing-Konfiguration verweist.

## Hinzufügen einer Briefpostnachricht {#create-dm-campaign}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_direct_mail"
>title="Briefpost-Aktion"
>abstract="Eine Briefpost-Kanalaktion generiert den Briefpost-Inhalt für Profile, wenn sie diesen Schritt des Journey erreichen. Die Bezeichnung identifiziert die Aktivität auf der Journey-Arbeitsfläche und die Aktion verweist auf eine Briefpostkonfiguration, die den bereitgestellten Inhalt definiert. Der Abschnitt **Optimierung** kann Inhaltsexperimente oder Zielgruppenbestimmungsregeln enthalten, der Abschnitt **Mehrsprachig** kann Inhalte in mehreren Sprachen bereitstellen, und der Abschnitt **Zeitüberschreitung oder Fehler** kann einen alternativen Pfad definieren, wenn die Aktion fehlschlägt."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="Erste Schritte mit Kanalaktionen"

Auf den folgenden Registerkarten erfahren Sie, wie Sie eine Briefpostnachricht zu einer Kampagne oder einer Journey hinzufügen.

>[!BEGINTABS]

>[!TAB Hinzufügen einer Briefpostnachricht zu einer Journey]

1. Öffnen Sie Ihre Journey und ziehen Sie eine Aktivität **[!UICONTROL Direkt-Mail]** per Drag-and-Drop aus dem Abschnitt **Aktionen** der Palette.

1. Geben Sie allgemeine Informationen (Label, Beschreibung, Kategorie) zu Ihrer Nachricht ein und wählen Sie dann die zu verwendende Konfiguration aus. Das Feld **[!UICONTROL Konfiguration]** ist standardmäßig vorab mit der letzten Konfiguration für den Kanal ausgefüllt, den die Benutzerin oder der Benutzer verwendet hat. Weitere Informationen zur Konfiguration einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

1. Konfigurieren Sie die Extraktionsdatei, die an Ihren Direkt-Mail-Anbieter gesendet werden soll. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**.

   ![Die Briefpost-Aktivität wurde einer Journey über die Palette „Aktionen“ hinzugefügt](assets/direct-mail-add-journey.png)

1. Passen Sie die Eigenschaften der Extraktionsdatei an, z. B. den Dateinamen oder die anzuzeigenden Spalten. Weitere Informationen zum Konfigurieren der Eigenschaften der Extraktionsdatei finden Sie in diesem Abschnitt: [Erstellen einer Direkt-Mail-Nachricht](../direct-mail/create-direct-mail.md#extraction-file).

   ![Inhaltseditor für die Extraktionsdatei für eine Briefpost-Journey-Aktivität](assets/direct-mail-journey-content.png)

1. Nachdem der Inhalt der Extraktionsdatei definiert wurde, können Sie ihn mit „Inhalt simulieren **[!UICONTROL in der Vorschau]**. [Erfahren Sie, wie Sie Inhalte in der Vorschau anzeigen und testen können](../content-management/preview-test.md)

   ![Inhaltsvorschau für eine Briefpost-Extraktionsdatei simulieren](assets/direct-mail-simulate.png){width="800" align="center"}

Wenn Ihre Push-Benachrichtigung bereit ist, schließen Sie zum Versenden die Konfiguration Ihrer [Journey](../building-journeys/journey-gs.md) ab.

>[!TAB Hinzufügen einer Briefpostnachricht zu einer Kampagne]

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

1. Wählen Sie den Kampagnentyp **Geplant – Marketing** aus.

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Um Ihre Zielgruppe zu definieren, klicken Sie auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]** und wählen Sie aus den verfügbaren Adobe Experience Platform-Zielgruppen aus. [Weitere Informationen](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >Derzeit ist die Zielgruppenauswahl auf 3 Millionen Profile beschränkt. Diese Einschränkung kann auf Anfrage von Ihrer Adobe-Support-Mitarbeitenden aufgehoben werden.

1. Wählen Sie im **[!UICONTROL Identity-Namespace]** den entsprechenden Namespace aus, um Kontakte innerhalb der ausgewählten Zielgruppe zu identifizieren. [Weitere Informationen](../event/about-creating.md#select-the-namespace).

1. Wählen Sie im Abschnitt **[!UICONTROL Aktionen]** die Option **[!UICONTROL Direkt-Mail]** aus.

1. Wählen Sie eine **[!UICONTROL Direkt-Mail-Konfiguration]** aus oder erstellen Sie eine neue Konfiguration. [Erfahren Sie, wie Sie eine Direkt-Mail-Konfiguration erstellen](direct-mail-configuration.md#direct-mail-surface).

   ![Briefpost-Aktion, die in einer geplanten Marketing-Kampagne konfiguriert ist](assets/direct-mail-campaign.png){width="800" align="center"}

   >[!AVAILABILITY]
   >
   >Briefpost unterstützt die **Holdout**-Funktion, unterstützt aber derzeit nicht **Behandlungen**. [Erfahren Sie, wie Sie mit Experimenten arbeiten](../content-management/get-started-experiment.md)

1. Kampagnen können für ein bestimmtes Datum geplant oder in regelmäßigen Abständen wiederholt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/campaign-schedule.md), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

Jetzt können Sie mit der Konfiguration der Extraktionsdatei beginnen, die an Ihren Briefpost-Dienstleister gesendet werden soll.

>[!ENDTABS]

## Konfigurieren der Extraktionsdatei {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="Datenfelder"
>abstract="Fügen Sie die Spalten und die Informationen hinzu, die in der Extraktionsdatei angezeigt werden sollen, die von Briefpostanbietern benötigt wird, um E-Mails an Ihre Kundinnen und Kunden zu senden, und konfigurieren Sie sie. Sie können bis zu 50 Spalten hinzufügen."

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="Formatieren der Extraktionsdatei"
>abstract="Geben Sie mit dem Personalisierungseditor für jedes Feld ein Label und die Informationen an, die angezeigt werden sollen. <br/><br/> Die Option <b>Sortieren nach</b> ermöglicht es Ihnen, die Spalten der Extraktionsdatei mithilfe des ausgewählten Felds zu sortieren."

Die Extraktionsdatei wird von Briefpost-Dienstleistern benötigt, um E-Mails an Ihre Kundinnen bzw. Kunden zu senden. Gehen Sie wie folgt vor, um die Konfiguration der Extraktionsdatei zu definieren:

1. Klicken Sie im Konfigurationsbildschirm der Kampagne oder des Journey auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**, um den Inhalt der Extraktionsdatei zu konfigurieren.

1. Um Ihrer Briefpostnachricht Entscheidungsrichtlinien hinzuzufügen, wählen Sie eine Spalte im Abschnitt **[!UICONTROL Datenfelder]** aus und öffnen Sie den Personalisierungseditor mithilfe des ![](../experience-decisioning/assets/do-no-localize/editor-icon.svg). Navigieren Sie zum Menü **[!UICONTROL Entscheidungsrichtlinien]**, um eine Entscheidungsrichtlinie zu erstellen und einzufügen. Anschließend können Sie Entscheidungselementattribute als Spaltendaten in der Extraktionsdatei verwenden.

   >[!AVAILABILITY]
   >
   >Experience Decisioning in Briefpost ist eine neue Funktion. Zuvor konnten Briefpost-Extraktionsdateien die Decisioning-Engine nicht verwenden. Sie können jetzt Entscheidungsrichtlinien hinzufügen und Entscheidungsattributen als Spaltendaten in den Export einschließen.

   [Erfahren Sie, wie Sie eine Entscheidungsrichtlinie in Briefpost hinzufügen](../experience-decisioning/create-decision-policy.md#add). Informationen zu Batch-Entscheidungs-Workflows und Beispielen (personalisierte Briefpost oder Export in nachgelagerte Systeme) finden Sie unter [Batch-Entscheidung in Briefpost](../experience-decisioning/batch-decisioning-direct-mail.md).

1. Passen Sie die Eigenschaften der Extraktionsdatei an:

   1. Geben Sie in das Feld **[!UICONTROL Dateiname]** einen Namen für die Extraktionsdatei an.

      >[!NOTE]
      >
      >Standardmäßig wird die Datei in das Stammverzeichnis des Servers geschrieben. Das Feld **[!UICONTROL Dateiname]** akzeptiert auch das Format „/Hier/Ihr/Pfad/Dateiname.csv“, wobei der angegebene Pfad dem Zielverzeichnis auf dem ausgewählten Server entspricht. <!--TBC if for SFTP and Azure only, or for all servers including S3-->

   1. Optional können Sie den **[!UICONTROL Zeitstempel an den Dateinamen des Exports anhängen]**, wenn Sie dem angegebenen Dateinamen einen automatischen Zeitstempel hinzufügen möchten.

   1. Hin und wieder müssen Sie vielleicht Informationen am Beginn oder am Ende der Extraktionsdatei hinzufügen. Verwenden Sie dazu das Feld **[!UICONTROL Hinweise]** und geben Sie an, ob der Hinweis als Kopf- oder Fußzeile eingefügt werden soll.

      ![Eigenschaften der Extraktionsdatei einschließlich Dateiname, Zeitstempel und Kopf- oder Fußzeilenhinweisen](assets/direct-mail-properties.png){width="800" align="center"}

1. Konfigurieren Sie die Spalten und die Informationen, die in der Extraktionsdatei angezeigt werden sollen:

   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Hinzufügen]**, um eine neue Spalte zu erstellen.

   1. Der Bereich **[!UICONTROL Formatierung]** wird auf der rechten Seite angezeigt, sodass Sie die ausgewählte Spalte einrichten können. Geben Sie ein **[!UICONTROL Label]** für die Spalte an.

   1. Wählen Sie im Feld **[!UICONTROL Daten]** mit dem [Personalisierungseditor](../personalization/personalization-build-expressions.md) die Profilattribute aus, die angezeigt werden sollen.

   1. Um die Extraktionsdatei mithilfe einer Spalte zu sortieren, wählen Sie die Spalte aus und schalten Sie die Option **[!UICONTROL Sortieren nach]** ein. Das Symbol **[!UICONTROL Sortieren nach]** wird neben dem Spalten-Label im Abschnitt **[!UICONTROL Datenfelder]** angezeigt.

      ![Datenfelder und Spaltenformatierung im Editor für die Briefpost-Extraktionsdatei](assets/direct-mail-content.png){width="800" align="center"}

   1. Wiederholen Sie diese Schritte, um so viele Spalten wie nötig hinzuzufügen, um Ihre Extraktionsdatei zu erstellen. Beachten Sie, dass Sie bis zu 50 Spalten hinzufügen können.

      Um die Position einer Spalte zu ändern, ziehen Sie sie an die gewünschte Position im Abschnitt **[!UICONTROL Datenfeld]**. Um eine Spalte zu löschen, wählen Sie sie aus und klicken Sie auf die Schaltfläche **[!UICONTROL Entfernen]** im Bereich **[!UICONTROL Formatierung]**.

Jetzt können Sie Ihre Briefpost-Nachricht testen und an Ihre Zielgruppe senden. [Erfahren Sie, wie Sie Briefpost-Nachrichten testen und senden.](test-send-direct-mail.md)

## Verwandte Themen {#related-topics}

* [Erste Schritte mit Direkt-Mail](get-started-direct-mail.md)
* [Konfigurieren des Briefpostkanals](direct-mail-configuration.md)
* [Testen und Senden von Briefpost](test-send-direct-mail.md)
* [Vorschau und Testinhalt](../content-management/preview-test.md)

Häufige Fragen zu Briefpost finden Sie unter [Erste Schritte mit Briefpost](get-started-direct-mail.md).
