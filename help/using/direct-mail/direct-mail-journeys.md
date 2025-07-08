---
title: Senden von Briefpostnachrichten mit Journeys
description: Erfahren Sie, wie Sie mit Journey Briefpostnachrichten erstellen und senden.
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
robots: noindex
googlebot: noindex
keywords: Direkt-Mail, Nachricht, Kampagne
source-git-commit: 114f712984b946bba30841a1d79be8870f9e3f07
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 39%

---


# Senden von Briefpostnachrichten mit Journeys {#direct-mail-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_direct_mail"
>title="Endaktivität"
>abstract="Direkt-Mail ist ein Offline-Kanal, mit dem Sie die Extraktionsdateien personalisieren und generieren können, die Direkt-Mail-Drittanbieter zum Senden von Nachrichten an Ihre Kunden und Kundinnen benötigen."

Direkt-Mail ist ein Offline-Kanal, mit dem Sie die Extraktionsdateien personalisieren und generieren können, die Direkt-Mail-Drittanbieter zum Senden von Nachrichten an Ihre Kunden und Kundinnen benötigen.

Beim Erstellen einer Briefpostnachricht generiert [!DNL Journey Optimizer] automatisch eine Datei, die alle Zielgruppenprofile und die ausgewählten Daten enthält, z. B. Postanschriften und Profilattribute. Diese Datei wird an den Server Ihrer Wahl gesendet, sodass der von Ihnen gewählte Direkt-Mail-Anbieter darauf zugreifen kann, der den eigentlichen Mailing-Prozess für Sie übernimmt.

Sie müssen ggf. mit Ihrem ausgewählten Direkt-Mail-Drittanbieter zusammenarbeiten, um die erforderliche Zustimmung von Ihren Kundinnen und Kunden zu erhalten, damit diese E-Mails von Ihnen erhalten können.

Ihre Nutzung von Mailing-Services unterliegt zusätzlichen Bedingungen des jeweiligen Drittanbieters für Briefpost. Adobe hat keine Kontrolle über die Produkte von Drittanbietern und ist nicht für Ihre Nutzung dieser Produkte verantwortlich. Wenden Sie sich bei Problemen oder Anfragen zur Unterstützung im Zusammenhang mit dem Versand Ihrer Briefpostnachricht an Ihren ausgewählten Drittanbieter.

>[!NOTE]
>
>Auf dieser Seite wird der Prozess zum Erstellen und Senden von Briefpostnachrichten mit Journey beschrieben. Weiterführende Informationen zum Briefpost-Kanal und zum Erstellen von Briefpostkampagnen finden Sie in diesem Abschnitt: [Erste Schritte mit Briefpost](../direct-mail/get-started-direct-mail.md).

## Erstellen einer Datei-Routing-Konfiguration

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_frequency"
>title="Auswählen der AWS-Region"
>abstract="Wenn Ihre Datei-Routing-Konfiguration mit Journeys gesendet wird, können Sie die Häufigkeit festlegen, mit der die Datei an den Server gesendet wird."

Bevor Sie eine Briefpostnachricht erstellen, stellen Sie sicher, dass Sie eine Datei-Routing-Konfiguration konfiguriert haben, die den Server angibt, auf den die Extraktionsdatei hochgeladen und gespeichert werden soll. Gehen Sie dazu wie folgt vor:

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Direkt-Mail-Einstellungen]** > **[!UICONTROL Datei-Routing]** auf und klicken Sie auf **[!UICONTROL Routing-Konfiguration erstellen]**.

1. Definieren Sie die Eigenschaften der Datei-Routing-Konfiguration wie beispielsweise den Namen und den Typ des zu verwendenden Servers. Detaillierte Informationen zum Einrichten einer Datei-Routing-Konfiguration finden Sie im Abschnitt [Briefpostkonfiguration](../direct-mail/direct-mail-configuration.md#file-routing-configuration).

   Wenn Ihre Datei-Routing-Konfiguration mit Journeys gesendet wird, können Sie die Häufigkeit festlegen, mit der die Datei an den Server gesendet wird.

   ![](assets/file-routing-journey.png)

1. Klicken Sie **[!UICONTROL Senden]**, um die Erstellung der Datei-Routing-Konfiguration zu bestätigen. Die Konfiguration wird mit dem Status **[!UICONTROL Aktiv]** erstellt. Sie kann jetzt in einer Briefpost-Konfiguration referenziert werden.

## Erstellen einer Direkt-Mail-Konfiguration {#direct-mail-surface}

Eine Direkt-Mail-Konfiguration enthält die Formatierungseinstellungen der Datei, die die Daten der anvisierten Zielgruppe enthält und vom Direkt-Mail-Anbieter verwendet wird. Sie müssen auch festlegen, wohin die Datei exportiert werden soll. Wählen Sie dazu die entsprechende Datei-Routing-Konfiguration aus.

Detaillierte Informationen zum Erstellen einer Briefpostkonfiguration finden Sie im Abschnitt [Briefpostkonfiguration](../direct-mail/direct-mail-configuration.md#file-routing-configuration).

Sobald Ihre Briefpost-Konfiguration fertig ist, können Sie eine Briefpost-Aktion erstellen und zu Ihrem Journey hinzufügen.

## Hinzufügen einer Briefpost-Aktion zu Ihrem Journey

Gehen Sie wie folgt vor, um eine Briefpost-Aktion zu einer Journey hinzuzufügen:

1. Öffnen Sie den Journey und ziehen Sie eine Aktivität **[!UICONTROL Briefpost]** aus dem Bereich **Aktionen** der Palette.

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenkonfiguration aus. Das Feld **[!UICONTROL Konfiguration]** ist standardmäßig mit der letzten Konfiguration für den Kanal vorausgefüllt, den die Benutzerin oder der Benutzer verwendet hat.

   Weitere Informationen zur Konfiguration der Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

1. Sie können jetzt die Extraktionsdatei konfigurieren, die an Ihren Briefpostanbieter gesendet werden soll. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**.

   ![](assets/direct-mail-add-journey.png)

1. Passen Sie die Eigenschaften der Extraktionsdatei an, z. B. den Dateinamen oder die anzuzeigenden Spalten. Weitere Informationen zum Konfigurieren der Eigenschaften der Extraktionsdatei finden Sie in diesem Abschnitt. [Erstellen einer Briefpostnachricht](../direct-mail/create-direct-mail.md#extraction-file)

   ![](assets/direct-mail-journey-content.png)

1. Sobald der Inhalt der Extraktionsdatei definiert wurde, können Sie Testprofile verwenden, um sie in der Vorschau anzuzeigen. Wenn Sie personalisierten Inhalt eingefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie dieser Inhalt in der Nachricht angezeigt wird.

   Klicken Sie dazu auf **[!UICONTROL Inhalt simulieren]** und fügen Sie dann ein Testprofil hinzu, um zu überprüfen, wie die Extraktionsdatei mithilfe der Testprofildaten gerendert wird.

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

   Detaillierte Informationen zur Auswahl von Testprofilen und zur Vorschau Ihres Inhalts finden Sie im Abschnitt [Content-Management](../content-management/preview-test.md).

Wenn Ihre Extraktionsdatei bereit ist, schließen Sie zum Senden die Konfiguration Ihrer [Journey](../building-journeys/journey-gs.md) ab.
