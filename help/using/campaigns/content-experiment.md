---
title: Erstellen eines Inhaltsexperiments
description: Erfahren Sie, wie Sie in Ihren Kampagnen ein Inhaltsexperiment erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 28380dbadf485ba05f7ef6788a50253876718441
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 65%

---

# Erstellen eines Inhaltsexperiments {#content-experiment}

>[!AVAILABILITY]
>
>Die Funktion für Inhaltsexperimente ist derzeit nur für eine Reihe von ausgewählten Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie bei Ihrer Adobe-Support-Person.

>[!NOTE]
>
>Bevor Sie Inhaltsexperimente verwenden, stellen Sie sicher, dass Ihre Berichtskonfiguration für Ihre benutzerdefinierten Datensätze festgelegt ist. Weiterführende Informationen finden Sie in [diesem Abschnitt](reporting-configuration.md).

Mit der Funktion für Inhaltsexperimente können Sie mehrere Versandbehandlungen definieren. Die geplante Audience wird jeder Variante nach dem Zufallsprinzip zugeordnet, um festzustellen, welche die beste Leistung in Bezug auf die Zielmetrik erzielt. Sie haben die Möglichkeit, Inhalt, Betreff oder Absender der E-Mail zu variieren.

Im nachstehenden Beispiel wurde die Zielgruppe des Versands in zwei Gruppen aufgeteilt, die jeweils 45 % der Zielpopulation repräsentieren, und eine neutrale Gruppe von 10 %, die den Versand nicht erhalten wird.

Jede Person in der Audience erhält eine Version der E-Mail mit einer der beiden folgenden Betreffzeilen:

* In einer wird direkt ein 10-%-Angebot für die neue Kollektion beworben. Sie enthält außerdem ein Bild.
* In der anderen wird nur für ein Sonderangebot ohne Angabe des 10-%-Rabatts geworben. Sie enthält kein Bild.

Das Ziel besteht nun darin zu beobachten, welche Empfänger mit welcher E-Mail-Variante interagieren. Wir wählen daher in diesem Inhaltsexperiment **[!UICONTROL Geöffnete E-Mails]** als primäre Zielmetrik aus.

![](assets/content_experiment.png)

## Erstellen der Kampagne {#campaign-experiment}

1. Klicken Sie auf der Seite **[!UICONTROL Kampagnen]** auf **[!UICONTROL Kampagne erstellen]**.

   ![](assets/content_experiment_1.png)

1. Wählen Sie **[!UICONTROL E-Mail]** und dann die **[!UICONTROL Oberfläche]**, die Sie für diesen Versand verwenden möchten. Weiterführende Informationen dazu finden Sie auf der Seite [Kanaloberflächen](../configuration/channel-surfaces.md).

   ![](assets/content_experiment_2.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Richten Sie die **[!UICONTROL Eigenschaften]** Ihres Versands ein:
   * **[!UICONTROL Titel]**
   * **[!UICONTROL Beschreibung]**
   * **[!UICONTROL Kategorie]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transaktion]**

1. Um Ihr Inhaltsexperiment zu starten, aktivieren Sie die Option **[!UICONTROL Inhaltsexperiment]**. Das Menü **[!UICONTROL Inhaltsexperiment]** wird angezeigt.

   ![](assets/content_experiment_3.png)

1. Konfigurieren Sie die Parameter **[!UICONTROL Audience]** und **[!UICONTROL Zeitplan]** für die Sendungen. [Weitere Informationen](create-campaign.md)

1. Klicken Sie auf **[!UICONTROL Inhalt bearbeiten]**, um mit der Personalisierung Ihrer anderen **[!UICONTROL Varianten]** zu beginnen.

   ![](assets/content_experiment_4.png)

## Erstellen der Varianten {#treatment-experiment}

1. Fügen Sie im Fenster **[!UICONTROL Inhalt bearbeiten]** die **[!UICONTROL Betreffzeile]** für Ihre E-Mail mit der Variante A hinzu und klicken Sie auf **[!UICONTROL Speichern]**.

   Diese Variante wird so konfiguriert, dass das Angebot direkt in der Betreffzeile angezeigt wird.

   ![](assets/content_experiment_5.png)

1. Klicken Sie auf **[!UICONTROL Email Designer]**, um mit der Personalisierung Ihrer Sendungen zu beginnen.

   ![](assets/content_experiment_6.png)

1. Nachdem Sie Ihre E-Mail erstellt haben, klicken Sie auf **[!UICONTROL Speichern]** und kehren Sie zum Fenster **[!UICONTROL Inhalt bearbeiten]** zurück, um Variante B zu erstellen.

1. Klicken Sie zuerst auf die Schaltfläche **[!UICONTROL Weitere Aktionen]** und danach auf **[!UICONTROL Duplizieren]**.

   Sie können auch eine völlig neue Variante erstellen, indem Sie auf die Schaltfläche **[!UICONTROL Inhaltsexperiment]** klicken, um auf die erweiterten Optionen zuzugreifen, und dann auf **[!UICONTROL Variante hinzufügen]** klicken.

   ![](assets/content_experiment_7.png)

1. Ändern Sie den **[!UICONTROL Titel]** Ihrer Variante, um die einzelnen Varianten besser unterscheiden zu können.

   ![](assets/content_experiment_8.png)

1. Wählen Sie den E-Mail-Versand aus, der mit Ihrer neu erstellten **[!UICONTROL Variante]** verknüpft ist.

1. Fügen Sie die **[!UICONTROL Betreffzeile]** für Ihren Versand hinzu.

   In dieser Variante wird das Angebot nicht in der **[!UICONTROL Betreffzeile]** angegeben.

   ![](assets/content_experiment_9.png)

1. Klicken Sie auf **[!UICONTROL Email Designer]**, um den Versand von Variante B bei Bedarf weiter zu personalisieren.

Nachdem Ihre Varianten personalisiert wurden, können Sie mit der Konfiguration Ihres Inhaltsexperiments beginnen.

## Konfigurieren des Inhaltsexperiments {#configure-experiment}

1. Wenn beide Varianten personalisiert sind, wählen Sie im Fenster **[!UICONTROL Inhalt bearbeiten]** die Option **[!UICONTROL Inhaltsexperiment konfigurieren]**.

   ![](assets/content_experiment_10.png)

1. Wählen Sie die Ziele aus, die Sie für Ihr Experiment festlegen möchten.

   Für unser Experiment wählen wir **[!UICONTROL Geöffnete E-Mails]**, um zu testen, ob Empfänger ihre E-Mails öffnen, wenn sich das Angebot in der Betreffzeile befindet.

   ![](assets/content_experiment_11.png)

1. Wählen Sie aus, dass eine **[!UICONTROL neutrale]** Gruppe zu Ihrem Versand hinzugefügt werden soll. Diese Gruppe erhält keine Inhalte aus dieser Kampagne.

   Wenn Sie den Umschalter aktivieren, werden für diese Gruppe automatisch 10 % Ihrer Population genommen. Sie können diesen Prozentsatz bei Bedarf aber auch anpassen.

   ![](assets/content_experiment_12.png)

1. Sie können dann jeder **[!UICONTROL Variante]** einen bestimmten Prozentsatz zuweisen oder einfach den Umschalter **[!UICONTROL Gleichmäßig verteilen]** aktivieren.

   ![](assets/content_experiment_13.png)

1. Klicken Sie nach der Konfiguration auf **[!UICONTROL Speichern]**.

1. Wenn Ihr Inhaltsexperiment bereit ist, können Sie auf **[!UICONTROL Zum Aktivieren überprüfen]** klicken, um eine Zusammenfassung der Kampagne anzuzeigen. Warnhinweise werden angezeigt, wenn Parameter falsch sind oder fehlen.

   ![](assets/content_experiment_15.png)

1. Vergewissern Sie sich, dass Ihre Kampagne korrekt konfiguriert ist, und klicken Sie dann auf **[!UICONTROL Aktivieren]**, um sie zu starten.

   ![](assets/content_experiment_14.png)

Nach der Konfiguration Ihrer Experimente und Kampagnen können Sie dem Erfolg Ihres Versands mit dem Kampagnenbericht folgen.

## Zielgruppenbericht {#objectives-global}

>[!AVAILABILITY]
>
>Die Funktion für Inhaltsexperimente ist derzeit nur für eine Reihe von ausgewählten Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie bei Ihrer Adobe-Support-Person.

![](assets/performance_report.gif)

Die **[!UICONTROL Ziele]** im Kampagnenbericht können Sie die Berichte Ihrer Sendungen durch Targeting einer bestimmten Metrik besser anpassen.

Die **[!UICONTROL Ziele]** aufgeführt sind, die **[!UICONTROL Datensätze]** die eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen. Eine Liste der integrierten **[!UICONTROL Ziele]** ist verfügbar, Sie können jedoch Ihre eigene hinzufügen, indem Sie neue **[!UICONTROL Datensatz]**. Eine detaillierte Anleitung finden Sie in diesem Abschnitt [Abschnitt](reporting-configuration.md).

Nach Auswahl der Ziele, für die Sie die Zielgruppe bestimmen möchten, werden die beiden **[!UICONTROL Leistungsübersicht]** und **[!UICONTROL Kampagnenziel]** -Widgets bieten eine detaillierte Zusammenfassung Ihrer Versandleistung.

Mit dem **[!UICONTROL Kampagnenziel]** -Widget, können Sie auch Ihr Hauptziel mit einer anderen Metrik vergleichen.

Beachten Sie, dass jedes Widget bei Bedarf in der Größe angepasst und gelöscht werden kann. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/global-report.md#modify-dashboard).

## Experimentationsbericht {#experimentation-global}

>[!AVAILABILITY]
>
>Die Funktion für Inhaltsexperimente ist derzeit nur für eine Reihe von ausgewählten Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie bei Ihrer Adobe-Support-Person.

![](assets/experimentation_report_3.png)

In Ihrer Kampagne **[!UICONTROL Gesamtbericht]**, die **[!UICONTROL Experimentieren]** im Tab werden die wichtigsten Informationen bezüglich der Leistung der einzelnen Varianten und der bestmöglichen Leistung aufgeführt.

Beachten Sie, dass das Definieren des besten Leisters einige Zeit in Anspruch nehmen kann. Es wird durch dieses Symbol dargestellt ![](assets/experimentation_report_1.png).

Die **[!UICONTROL Experimentergebnis]** Widget erläutert die Leistung der einzelnen Varianten. Sie können Ihre Ausgangswerte ändern, indem Sie eine der Behandlungen aus der **[!UICONTROL Grundlinie]** die Dropdown-Liste. Die beste Behandlung wird mit einem Sternsymbol dargestellt.

Die Tabelle enthält die folgenden Metriken:

* **[!UICONTROL Profile]**: Anzahl der für diese Behandlung ausgewählten Profile.

* **[!UICONTROL Ausgehende Einzelklicks]**: Gesamtanzahl der Klicks in allen ausgehenden Kanälen.

* **[!UICONTROL Anzahl pro Profil]**: Gesamtwert der Metrik Experimentziel dividiert durch die Anzahl der Profile.

* **[!UICONTROL Konfidenzintervall]**: Prozentualer Leistungsunterschied zwischen dem Ausgangswert und der Behandlung mit der besten Performance. [Weitere Informationen](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Durchschnittliche Steigerung]**: Prozentuale Verbesserung der Konversionsrate einer bestimmten Behandlung im Vergleich zum Ausgangswert. [Weitere Informationen](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Behandlung mit der Ausgangsbehandlung identisch ist. [Weitere Informationen](../campaigns/experiment-calculations.md#understand-confidence)

Einen tiefen Einblick in diese Ergebnisse und ihre Interpretation finden Sie unter [diese Seite](../campaigns/get-started-experiment.md#interpret-results).
