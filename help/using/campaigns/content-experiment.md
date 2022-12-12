---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen eines Inhaltsexperiments
description: Erfahren Sie, wie Sie in Ihren Kampagnen ein Inhaltsexperiment erstellen
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: ef838945e0c3595de8ad920203b278bb51671d16
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# Erstellen eines Inhaltsexperiments {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Inhaltsexperiment"
>abstract="Sie können den Versandinhalt, den Betreff oder den Absender variieren, um mehrere Versandbehandlungen zu definieren und die beste Kombination für Ihre Zielgruppen zu bestimmen."

>[!AVAILABILITY]
>
>Die **Inhaltstest** ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrem Adobe-Support-Mitarbeiter.

Verwenden Sie das Journey Optimizer-Inhaltsexperiment, um mehrere Bereitstellungsbehandlungen zu definieren. Die Zielgruppe wird nach dem Zufallsprinzip jeder Behandlung zugeordnet, um festzustellen, welche die beste Leistung in Bezug auf die Zielmetrik erzielt. Sie können den Versandinhalt, den Betreff oder den Absender variieren.

>[!NOTE]
>
>Bevor Sie mit Content Experiment beginnen, stellen Sie sicher, dass Ihre Berichtskonfiguration für Ihre benutzerdefinierten Datensätze festgelegt ist. Weitere Informationen finden Sie unter [diesem Abschnitt](reporting-configuration.md).

Im folgenden Beispiel wurde die Zielgruppe in zwei Gruppen unterteilt, von denen jeweils 45 % der Zielgruppe und 10 % der Zielpopulation ausmachen, die den Versand nicht erhalten.

Jede Person in der Zielgruppe erhält eine Version einer E-Mail mit einer Betreffzeile, die einer der beiden folgenden ist:

* ein direktes Bewerben eines 10 %-Angebots für die neue Sammlung und ein Bild.
* das andere nur ein spezielles Angebot bewerben, ohne die 10% Rabatt ohne Bild anzugeben.

Das Ziel besteht hier darin zu sehen, ob Empfänger je nach dem empfangenen Experiment mit der E-Mail interagieren. Wir werden daher **[!UICONTROL Email Opens]** als primäre Zielmetrik in diesem Inhaltsexperiment.

![](assets/content_experiment.png)

## Kampagne erstellen {#campaign-experiment}

1. Aus dem **[!UICONTROL Campaigns]** Seite, klicken Sie auf **[!UICONTROL Create campaign]**.

   ![](assets/content_experiment_1.png)

1. Wählen Sie Ihren Kanal und dann **[!UICONTROL Surface]** Sie möchten für diesen Versand verwenden. Weitere Informationen hierzu finden Sie im Abschnitt [Kanaloberflächen](../configuration/channel-surfaces.md) Seite.

   ![](assets/content_experiment_2.png)

1. Klicken **[!UICONTROL Create]**.

1. Richten Sie die **[!UICONTROL Properties]** Ihres Versands:
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. Um Ihr Inhaltsexperiment zu starten, schalten Sie die **[!UICONTROL Content experiment]** -Option. Die **[!UICONTROL Content experiment]** angezeigt.

   ![](assets/content_experiment_3.png)

1. Definieren Sie die Zielgruppe. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Select audience]** -Schaltfläche, um die Liste der verfügbaren Adobe Experience Platform-Segmente anzuzeigen. [Weitere Informationen zu Segmenten](../segment/about-segments.md)

   Im **[!UICONTROL Identity namespace]** wählen Sie den Namespace aus, der verwendet werden soll, um die Kontakte aus dem ausgewählten Segment zu identifizieren. [Weitere Infos](get-started-experiment.md#content-experiment-work)

1. Um Ihre Kampagne an einem bestimmten Datum oder in regelmäßigen Abständen auszuführen, konfigurieren Sie den Abschnitt Planung . [Weitere Infos](create-campaign.md)

1. Klicken **[!UICONTROL Edit content]** zur Personalisierung Ihrer anderen **[!UICONTROL Treatments]**.

   ![](assets/content_experiment_4.png)

## Erstellen von Behandlungen {#treatment-experiment}

1. Aus dem **[!UICONTROL Edit content]** Beginn der Personalisierung Ihrer Behandlung A.

   Für diese Behandlung wird das Sonderangebot direkt in der Betreffzeile angegeben.

   ![](assets/content_experiment_5.png)

1. Nach der Konzeption Ihrer ersten Behandlung, **[!UICONTROL More actions]** Schaltfläche, klicken Sie auf **[!UICONTROL Duplicate]**.

   Sie können auch eine neue Behandlung starten, indem Sie auf die **[!UICONTROL Content experiment]** button ![](assets/content_experiment_16.png) um auf die erweiterten Optionen zuzugreifen, **[!UICONTROL Add treatment]**.

   ![](assets/content_experiment_7.png)

1. Ändern Sie die **[!UICONTROL Title]** Ihrer Behandlung, um sie besser zu differenzieren.

   ![](assets/content_experiment_8.png)

1. Personalisieren Sie Ihre zweite Behandlung nach Bedarf.

   Im vorliegenden Beispiel soll das Angebot nicht im **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_9.png)

Sobald Ihre Behandlungen personalisiert wurden, können Sie mit der Konfiguration Ihres Inhaltsexperiments beginnen.

## Konfigurieren des Inhaltsexperiments {#configure-experiment}

1. Wenn beide Sendungen personalisiert sind, wird im **[!UICONTROL Edit content]** auswählen **[!UICONTROL Configure content experiment]**.

   ![](assets/content_experiment_10.png)

1. Wählen Sie die Ziele aus, die Sie für Ihr Experiment festlegen möchten.

   Für unser Experiment wählen wir **[!UICONTROL Email open]** , um zu testen, ob Empfänger ihre E-Mails öffnen, wenn sich der Angebotscode in der Betreffzeile befindet.

   ![](assets/content_experiment_11.png)

1. Wählen Sie zum Hinzufügen einer **[!UICONTROL Holdout]** zu Ihrem Versand hinzugefügt. Diese Gruppe erhält keine Inhalte von dieser Kampagne.

   Das Umschalten auf die Umschalter-Leiste nimmt automatisch 10 % Ihrer Population in Anspruch. Sie können diesen Prozentsatz bei Bedarf anpassen.

   ![](assets/content_experiment_12.png)

1. Anschließend können Sie festlegen, jedem **[!UICONTROL Treatment]** oder schalten Sie einfach die **[!UICONTROL Distribute evenly]** Leiste ein/aus.

   ![](assets/content_experiment_13.png)

1. Klicken **[!UICONTROL Save]** wenn Ihre Konfiguration festgelegt ist.

1. Wenn Ihr Inhaltsexperiment fertig ist, können Sie auf **[!UICONTROL Review to activate]** um eine Zusammenfassung der Kampagne anzuzeigen. Warnhinweise werden angezeigt, wenn ein Parameter falsch ist oder fehlt.

   ![](assets/content_experiment_15.png)

1. Vergewissern Sie sich, dass Ihre Kampagne korrekt konfiguriert ist, und klicken Sie dann auf **[!UICONTROL Activate]** , um es zu starten.

   ![](assets/content_experiment_14.png)

Nach der Konfiguration Ihrer Experimente und Kampagnen können Sie dem Erfolg Ihres Versands mit dem Kampagnenbericht folgen.

## Zielgruppenbericht {#objectives-global}

>[!AVAILABILITY]
>
>Die Funktion für Inhaltsexperimente ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrem Adobe-Support-Mitarbeiter.

![](assets/performance_report.gif)

Die **[!UICONTROL Objectives]** im Kampagnenbericht können Sie die Berichte Ihrer Sendungen durch Targeting einer bestimmten Metrik besser anpassen.

Die **[!UICONTROL Objectives]** aufgeführt sind, die **[!UICONTROL Datasets]** die eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen. Eine Liste der integrierten **[!UICONTROL Objectives]** ist verfügbar, Sie können jedoch Ihre eigene hinzufügen, indem Sie neue **[!UICONTROL Dataset]**. Eine detaillierte Anleitung finden Sie in diesem Abschnitt [Abschnitt](reporting-configuration.md).

Nach Auswahl der Ziele, für die Sie die Zielgruppe bestimmen möchten, werden die beiden **[!UICONTROL Performance overview]** und **[!UICONTROL Campaign objective]** -Widgets bieten eine detaillierte Zusammenfassung Ihrer Versandleistung.

Mit dem **[!UICONTROL Campaign objective]** -Widget, können Sie auch Ihr Hauptziel mit einer anderen Metrik vergleichen.

Beachten Sie, dass jedes Widget bei Bedarf in der Größe angepasst und gelöscht werden kann. Weitere Informationen hierzu finden Sie in diesem Abschnitt [Abschnitt](../reports/global-report.md#modify-dashboard).

## Experimentationsbericht {#experimentation-global}

>[!AVAILABILITY]
>
>Die Funktion für Inhaltsexperimente ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrem Adobe-Support-Mitarbeiter.

![](assets/experimentation_report_3.png)

In Ihrer Kampagne **[!UICONTROL Global report]**, die **[!UICONTROL Experimentation]** im Tab werden die wichtigsten Informationen bezüglich der Leistung der einzelnen Varianten und der bestmöglichen Leistung aufgeführt.

Beachten Sie, dass das Definieren des besten Leisters einige Zeit in Anspruch nehmen kann. Es wird durch dieses Symbol dargestellt ![](assets/experimentation_report_1.png).

Die **[!UICONTROL Experiment result]** Widget erläutert die Leistung der einzelnen Varianten. Sie können Ihre Ausgangswerte ändern, indem Sie eine der Behandlungen aus der **[!UICONTROL Baseline]** die Dropdown-Liste. Die beste Behandlung wird mit einem Sternsymbol dargestellt.

Die Tabelle enthält die folgenden Metriken:

* **[!UICONTROL Profiles]**: Anzahl der für diese Behandlung ausgewählten Profile.

* **[!UICONTROL Unique outbound clicks]**: Gesamtanzahl der Klicks in allen ausgehenden Kanälen.

* **[!UICONTROL Count per profile]**: Gesamtwert der Metrik Experimentziel dividiert durch die Anzahl der Profile.

* **[!UICONTROL Confidence interval]**: Prozentualer Leistungsunterschied zwischen dem Ausgangswert und der Behandlung mit der besten Performance. [Weitere Infos](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Average lift]**: Prozentuale Verbesserung der Konversionsrate einer bestimmten Behandlung im Vergleich zum Ausgangswert. [Weitere Infos](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confidence]**: Belege dafür, dass eine bestimmte Behandlung mit der Ausgangsbehandlung identisch ist. [Weitere Infos](../campaigns/experiment-calculations.md#understand-confidence)

Einen tiefen Einblick in diese Ergebnisse und ihre Interpretation finden Sie unter [diese Seite](../campaigns/get-started-experiment.md#interpret-results).
