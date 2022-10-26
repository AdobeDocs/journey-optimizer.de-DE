---
title: Briefpost-Nachricht erstellen
description: Erfahren Sie, wie Sie in Journey Optimizer eine Briefpost-Nachricht erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: fe6fedfd3fb0a8b083f7b047e2879ef6510b041b
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 9%

---

# Briefpost-Nachricht erstellen {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Erstellung von Direkt-Mail"
>abstract="Erstellen Sie Briefpost-Nachrichten in geplanten Kampagnen und entwerfen Sie die Extraktionsdateien, die von Briefpost-Dienstleistern benötigt werden, um E-Mails an Ihre Kunden zu senden."

Briefpost ist ein Offline-Kanal, mit dem Sie die Extraktionsdateien personalisieren und generieren können, die Briefpost-Dienstleister zum Senden von Nachrichten an Ihre Kunden benötigen.

Beim Erstellen einer Briefpost generiert Journey Optimizer eine Datei, die alle Zielgruppenprofile und die ausgewählten Daten enthält (z. B. Postanschrift, Profilattribute). Dann senden Sie diese Datei an Ihren Briefpost-Dienstleister, der den tatsächlichen Versand vornimmt.

Briefpost-Nachrichten können nur im Rahmen geplanter Kampagnen erstellt werden. Sie sind nicht zur Verwendung in API-basierten Kampagnen oder in Journey verfügbar.

>[!IMPORTANT]
>
>Bevor Sie eine Briefpost senden, stellen Sie sicher, dass Sie Folgendes konfiguriert haben:
>* A [Dateirouting-Konfiguration](../configuration/direct-mail-configuration.md#file-routing-configuration) , der den Server angibt, auf den die Extraktionsdatei hochgeladen und gespeichert werden soll,
>* A [Oberfläche für Briefpost-Nachrichten](../configuration/direct-mail-configuration.md#direct-mail-surface) , die auf die Dateirouting-Konfiguration verweist.


## Briefpost-Nachricht erstellen {#create}

Gehen Sie zur Erstellung und zum Versand einer Briefpost-Nachricht wie folgt vor:

1. Erstellen Sie eine neue geplante Kampagne, wählen Sie **[!UICONTROL Briefpost]** und wählen Sie die zu verwendende Nachrichtenoberfläche aus.

   ![](assets/direct-mail-campaign.png)

1. Klicken **[!UICONTROL Erstellen]** Definieren Sie dann grundlegende Informationen zu Ihrer Kampagne (Name, Beschreibung). [Erfahren Sie, wie Sie eine Kampagne konfigurieren](../campaigns/create-campaign.md)

   ![](assets/direct-mail-edit.png)

1. Klicken Sie auf **[!UICONTROL Inhalt bearbeiten]** Schaltfläche zum Konfigurieren der Extraktionsdatei, die an Ihren Briefpost-Dienstleister gesendet werden soll.

1. Definieren Sie den Namen der Extraktionsdatei im **[!UICONTROL Dateiname]** -Feld.

   Hin und wieder müssen Sie vielleicht Informationen am Beginn oder am Ende der Extraktionsdatei hinzufügen. Verwenden Sie dazu die **[!UICONTROL Hinweise]** und geben Sie an, ob die Notiz als Kopf- oder Fußzeile eingefügt werden soll.

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. Definieren Sie im linken Bereich die Informationen, die als Spalten in der Extraktionsdatei angezeigt werden sollen:

   1. Klicken Sie auf **[!UICONTROL Hinzufügen]** um eine neue Spalte hinzuzufügen, und wählen Sie sie dann aus der Liste aus.

   1. Im **[!UICONTROL Formatierung]** einen Titel für die Spalte angeben und dann die Profilattribute definieren, die mit der [Ausdruckseditor](../personalization/personalization-build-expressions.md).

      ![](assets/direct-mail-content.png)

   1. Um die Extraktionsdatei mithilfe der ausgewählten Spalte zu sortieren, können Sie die **[!UICONTROL Sortieren nach]** aktiviert. Die **[!UICONTROL Sortieren nach]** wird dann neben der Spaltenbeschriftung in der Dateistruktur angezeigt.

1. Wiederholen Sie diese Schritte, um so viele Spalten wie nötig hinzuzufügen, um Ihre Extraktionsdatei zu erstellen. Beachten Sie, dass Sie bis zu 50 Spalten hinzufügen können.

   ![](assets/direct-mail-complete.png)

   Sie können eine Spalte jederzeit löschen, indem Sie sie auswählen und auf **[!UICONTROL Entfernen]** -Schaltfläche in der **[!UICONTROL Formatierung]** Abschnitt.

1. Sobald der Inhalt der Briefpost definiert wurde, konfigurieren Sie Ihre Kampagne.

   Wenn die Kampagne gestartet wird, wird die Extraktionsdatei automatisch generiert und auf den in Ihrer [Dateirouting-Konfiguration](../configuration/direct-mail-configuration.md).
