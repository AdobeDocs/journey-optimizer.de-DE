---
title: Erstellen einer Briefpostnachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine Briefpostnachricht erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: Direkt-Mail, Nachricht, Kampagne
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: d8ae894cc303237f5b2257afd8da5b2d0cf1b7a6
workflow-type: ht
source-wordcount: '560'
ht-degree: 100%

---

# Erstellen einer Briefpostnachricht {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Erstellung von Briefpost"
>abstract="Erstellen Sie Briefpostnachrichten in geplanten Kampagnen und entwerfen Sie die Extraktionsdateien, die von Briefpostanbietern benötigt werden, um E-Mails an Ihre Kunden zu senden."

Um Briefpost-Nachrichten zu erstellen, erstellen Sie eine geplante Kampagne und konfigurieren Sie die Extraktionsdatei. Diese Datei wird von Briefpost-Dienstleistern benötigt, um E-Mails an Ihre Kundinnen bzw. Kunden zu senden.

>[!IMPORTANT]
>
>Bevor Sie eine Briefpostnachricht senden, stellen Sie sicher, dass Sie Folgendes konfiguriert haben:
>
>1. Eine [Dateirouting-Konfiguration](../direct-mail/direct-mail-configuration.md#file-routing-configuration), die den Server angibt, auf den die Extraktionsdatei hochgeladen und gespeichert werden soll,
>1. Eine [Oberfläche für Briefpostnachrichten](../direct-mail/direct-mail-configuration.md#direct-mail-surface), die auf die Datei-Routing-Konfiguration verweist.


## Erstellen einer Briefpost-Kampagne{#create-dm-campaign}

Um eine Briefpost-Kampagne zu erstellen, gehen Sie folgendermaßen vor:

1. Erstellen Sie eine neue geplante Kampagne und wählen Sie **[!UICONTROL Briefpost]** als Aktion aus.

1. Wählen Sie die **[!UICONTROL Briefpost-Oberfläche]**, die verwendet werden soll, und klicken Sie auf **[!UICONTROL Erstellen]**. [Erfahren Sie, wie Sie eine Briefpost-Oberfläche erstellen](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Um Ihre Zielgruppe zu definieren, klicken Sie auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]** und wählen Sie aus den verfügbaren Adobe Experience Platform-Zielgruppen aus. [Weitere Informationen](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >Derzeit ist die Zielgruppenauswahl auf 3 Millionen Profile beschränkt. Diese Einschränkung kann auf Anfrage von Ihrer Adobe-Support-Mitarbeitenden aufgehoben werden.

1. Wählen Sie im **[!UICONTROL Identitäts-Namespace]** den entsprechenden Namespace aus, um Kontakte innerhalb der ausgewählten Zielgruppe zu identifizieren. [Weitere Informationen](../event/about-creating.md#select-the-namespace).

   ![](assets/direct-mail-campaign-properties.png){width="800" align="center"}

1. Kampagnen können für ein bestimmtes Datum geplant oder in regelmäßigen Abständen wiederholt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/create-campaign.md#schedule), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

Jetzt können Sie mit der Konfiguration der Extraktionsdatei beginnen, die an Ihren Briefpost-Dienstleister gesendet werden soll.

## Konfigurieren der Extraktionsdatei {#extraction-file}

Die Extraktionsdatei wird von Briefpost-Dienstleistern benötigt, um E-Mails an Ihre Kundinnen bzw. Kunden zu senden. Gehen Sie wie folgt vor, um die Konfiguration der Extraktionsdatei zu definieren:

1. Klicken Sie zum Konfigurieren des Inhalts der Push-Benachrichtigung im Konfigurationsbildschirm der Kampagne auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**.

1. Passen Sie die Eigenschaften der Extraktionsdatei an:

   1. Geben Sie den gewünschten **[!UICONTROL Dateiname]** für die Extraktionsdatei an.

   1. Optional können Sie den **[!UICONTROL Zeitstempel an den Dateinamen des Exports anhängen]**, wenn Sie dem angegebenen Dateinamen einen automatischen Zeitstempel hinzufügen möchten.

   1. Hin und wieder müssen Sie vielleicht Informationen am Beginn oder am Ende der Extraktionsdatei hinzufügen. Verwenden Sie dazu das Feld **[!UICONTROL Hinweise]** und geben Sie an, ob der Hinweis als Kopf- oder Fußzeile eingefügt werden soll.

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. Konfigurieren Sie die Spalten und die Informationen, die in der Extraktionsdatei angezeigt werden sollen:

   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Hinzufügen]**, um eine neue Spalte zu erstellen.

   1. Der Bereich **[!UICONTROL Formatierung]** wird auf der rechten Seite angezeigt, sodass Sie die ausgewählte Spalte einrichten können. Geben Sie einen **[!UICONTROL Titel]** für die Spalte an.

   1. Wählen Sie im Feld **[!UICONTROL Daten]** mit dem [Ausdruckseditor](../personalization/personalization-build-expressions.md) die Profilattribute aus, die angezeigt werden sollen.

   1. Um die Extraktionsdatei mithilfe einer Spalte zu sortieren, wählen Sie die Spalte aus und schalten Sie die Option **[!UICONTROL Sortieren nach]** ein. Das Symbol **[!UICONTROL Sortieren nach]** wird neben der Spaltenbeschriftung im Abschnitt **[!UICONTROL Datenfelder]** angezeigt.

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. Wiederholen Sie diese Schritte, um so viele Spalten wie nötig hinzuzufügen, um Ihre Extraktionsdatei zu erstellen. Beachten Sie, dass Sie bis zu 50 Spalten hinzufügen können.

      Um die Position einer Spalte zu ändern, ziehen Sie sie an die gewünschte Position im Abschnitt **[!UICONTROL Datenfeld]**. Um eine Spalte zu löschen, wählen Sie sie aus und klicken Sie auf die Schaltfläche **[!UICONTROL Entfernen]** im Bereich **[!UICONTROL Formatierung]**.

Jetzt können Sie Ihre Briefpost-Nachricht testen und an Ihre Zielgruppe senden. [Erfahren Sie, wie Sie Briefpost-Nachrichten testen und senden.](test-send-direct-mail.md)
