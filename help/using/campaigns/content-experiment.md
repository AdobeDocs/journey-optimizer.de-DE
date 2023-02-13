---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen eines Inhaltsexperiments
description: Erfahren Sie, wie Sie in Ihren Kampagnen ein Inhaltsexperiment erstellen
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: Inhalt, Experiment, mehrere, Audience, Behandlung
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 08d842a877ed52349eef5a901aaf9c75187c69d3
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 77%

---

# Erstellen eines Inhaltsexperiments {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Inhaltsexperiment"
>abstract="Der Versandinhalt, der Betreff oder der Absender kann abgeändert werden, um mehrere Abwandlungen des Versands zu definieren und die beste Kombination für die Audiences zu ermitteln."

>[!AVAILABILITY]
>
>Die Funktion für **Inhaltsexperimente** ist derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie beim Adobe-Support.

Mit dem Journey Optimizer Content Experiment können Sie mehrere Bereitstellungsbehandlungen definieren, um zu messen, welche die beste Leistung für Ihre Zielgruppe erzielt. Sie haben die Möglichkeit, Inhalt, Betreff oder Absender des Versands zu variieren. Die Zielgruppe wird nach dem Zufallsprinzip jeder Behandlung zugeordnet, um zu bestimmen, welche die angegebene Metrik am besten verwendet.

>[!NOTE]
>
>Bevor Sie mit dem Inhaltsexperiment beginnen, stellen Sie sicher, dass die Berichtskonfiguration für Ihre benutzerdefinierten Datensätze definiert ist. Weiterführende Informationen finden Sie in [diesem Abschnitt](reporting-configuration.md).

Im nachstehenden Beispiel wurde die Zielgruppe des Versands in zwei Gruppen aufgeteilt, die jeweils 45 % der Zielpopulation repräsentieren, und eine neutrale Gruppe von 10 %, die den Versand nicht erhalten wird.

Jede Person in der Audience erhält eine Version der E-Mail mit einer der beiden folgenden Betreffzeilen:

* In einer wird direkt ein 10-%-Angebot für die neue Kollektion beworben. Sie enthält außerdem ein Bild.
* In der anderen wird nur für ein Sonderangebot ohne Angabe des 10-%-Rabatts geworben. Sie enthält kein Bild.

Das Ziel besteht nun darin zu beobachten, welche Empfänger mit welcher E-Mail-Variante interagieren. Wir wählen daher in diesem Inhaltsexperiment **[!UICONTROL Geöffnete E-Mails]** als primäre Zielmetrik aus.

![](assets/content_experiment.png)

## Erstellen der Kampagne {#campaign-experiment}

1. Klicken Sie auf der Seite **[!UICONTROL Kampagnen]** auf **[!UICONTROL Kampagne erstellen]**.

   ![](assets/content_experiment_1.png)

1. Wählen Sie Ihren Kanal und dann **[!UICONTROL Oberfläche]** Sie möchten für diesen Versand verwenden und klicken Sie auf **[!UICONTROL Erstellen]**. Weiterführende Informationen dazu finden Sie auf der Seite [Kanaloberflächen](../configuration/channel-surfaces.md).

   ![](assets/content_experiment_2.png)

1. Richten Sie die **[!UICONTROL Eigenschaften]** Ihres Versands ein:
   * **[!UICONTROL Name]**
   * **[!UICONTROL Beschreibung]**

1. Definieren Sie die anzusprechende Audience. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Liste der verfügbaren Adobe Experience Platform-Segmente anzuzeigen. [Weitere Informationen zu Segmenten](../segment/about-segments.md)

   Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll. [Weitere Informationen](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. Geben Sie im Bereich **[!UICONTROL Aktions-Tracking]** an, ob Sie verfolgen möchten, wie Ihre Empfänger(innen) auf Ihren Versand reagieren: Sie können Klicks und/oder Öffnungen verfolgen.

   Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar.

1. Um Ihre Kampagne an einem bestimmten Datum oder in regelmäßigen Abständen auszuführen, konfigurieren Sie den Abschnitt **[!UICONTROL Zeitplan]**. [Weitere Informationen](create-campaign.md)

1. Klicken **[!UICONTROL Inhalt bearbeiten]** , um mit der Personalisierung Ihres Versands zu beginnen. [Weitere Informationen](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. Aus dem **[!UICONTROL Inhalt bearbeiten]** Beginn der Personalisierung der Behandlung A.

   Für diese Behandlung wird das Sonderangebot direkt in der Betreffzeile spezifiziert und eine Personalisierung hinzugefügt.

   ![](assets/content_experiment_5.png)

## Konfigurieren des Inhaltsexperiments {#configure-experiment}

1. Wenn Ihr Versand personalisiert wurde, klicken Sie auf der Übersichtsseite der Kampagne auf **[!UICONTROL Experiment erstellen]** , um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen.

   ![](assets/content_experiment_3.png)

1. Wählen Sie die **[!UICONTROL Erfolgsmetrik]** Sie möchten für Ihr Experiment festlegen.

   Für unser Experiment wählen wir **[!UICONTROL Geöffnete E-Mails]**, um zu testen, ob Empfänger ihre E-Mails öffnen, wenn sich das Angebot in der Betreffzeile befindet.

   ![](assets/content_experiment_11.png)

1. Klicken **[!UICONTROL Behandlung hinzufügen]** um so viele neue Behandlungsmöglichkeiten wie nötig zu schaffen.

   ![](assets/content_experiment_8.png)

1. Ändern Sie den **[!UICONTROL Titel]** Ihrer Variante, um die einzelnen Varianten besser unterscheiden zu können.

1. Wählen Sie aus, dass eine **[!UICONTROL neutrale]** Gruppe zu Ihrem Versand hinzugefügt werden soll. Diese Gruppe erhält keine Inhalte aus dieser Kampagne.

   Wenn Sie den Umschalter aktivieren, werden für diese Gruppe automatisch 10 % Ihrer Population genommen. Sie können diesen Prozentsatz bei Bedarf aber auch anpassen.

   ![](assets/content_experiment_12.png)

1. Sie können dann jeder **[!UICONTROL Variante]** einen bestimmten Prozentsatz zuweisen oder einfach den Umschalter **[!UICONTROL Gleichmäßig verteilen]** aktivieren.

   ![](assets/content_experiment_13.png)

1. Klicken **[!UICONTROL Erstellen]** wenn Ihre Konfiguration festgelegt ist.

## Behandlungen entwerfen {#treatment-experiment}

1. Aus dem **[!UICONTROL Inhalt bearbeiten]** auswählen, wählen Sie Ihre Behandlung B aus, um den Inhalt zu ändern.

   In dieser Variante wird das Angebot nicht in der **[!UICONTROL Betreffzeile]** angegeben.

   ![](assets/content_experiment_18.png)

1. Klicken **[!UICONTROL Bearbeiten des E-Mail-Hauptteils]** zur weiteren Personalisierung Ihrer Behandlung B.

   ![](assets/content_experiment_9.png)

1. Klicken Sie nach der Konzeption Ihrer Behandlungen auf **[!UICONTROL Mehr Aktionen]** für den Zugriff auf Optionen für Ihre Behandlungen: **[!UICONTROL Umbenennen]**, **[!UICONTROL Duplizieren]** und **[!UICONTROL Löschen]**.

   ![](assets/content_experiment_7.png)

1. Greifen Sie bei Bedarf auf die **[!UICONTROL Experimenteinstellungen]** Menü, um die Konfiguration Ihrer Behandlungen zu ändern.

   ![](assets/content_experiment_19.png)

1. Nachdem der Nachrichteninhalt definiert wurde, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** zur Steuerung des Renderings Ihres Versands und zur Überprüfung der Personalisierungseinstellungen mit Testprofilen. [Weitere Informationen](../email/preview.md)

1. Wenn Ihr Inhaltsexperiment fertig ist, können Sie auf Ihrer Kampagnenzusammenfassungs-Seite auf **[!UICONTROL Aktivieren]** um eine Zusammenfassung der Kampagne anzuzeigen. Warnhinweise werden angezeigt, wenn Parameter falsch sind oder fehlen.

   ![](assets/content_experiment_15.png)

1. Vergewissern Sie sich, dass Ihre Kampagne korrekt konfiguriert ist, und klicken Sie dann auf **[!UICONTROL Aktivieren]**, um sie zu starten.

   ![](assets/content_experiment_14.png)

Nach der Konfiguration Ihrer Experimente und Kampagnen können Sie mit dem Kampagnenbericht den Erfolg Ihres Versands verfolgen.

## Zielsetzungsbericht {#objectives-global}

>[!AVAILABILITY]
>
>Die Funktion für Inhaltsexperimente ist derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie beim Adobe-Support.

![](assets/performance_report.gif)

Auf der Registerkarte **[!UICONTROL Ziele]** im Campaign-Bericht können Sie die Berichte Ihrer Sendungen besser anpassen, indem Sie auf eine bestimmte Kennzahl abzielen.

Die aufgeführten **[!UICONTROL Ziele]** sind mit **[!UICONTROL Datensätzen]** verbunden, die eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen. Eine Liste mit integrierten **[!UICONTROL Zielen]** ist verfügbar, Sie können jedoch Ihre eigenen hinzufügen, indem Sie einen neuen **[!UICONTROL Datensatz]** hinzufügen. Weiterführende Informationen finden Sie in diesem [Abschnitt](reporting-configuration.md).

Nach Auswahl der Ziele, die Sie in Angriff nehmen möchten, bieten die beiden Widgets für **[!UICONTROL Leistungsübersicht]** und **[!UICONTROL Kampagnenziel]** eine detaillierte Zusammenfassung Ihrer Versandleistung.

Mit dem Widget **[!UICONTROL Kampagnenziel]** können Sie auch Ihr Hauptziel mit einer anderen Metrik vergleichen.

Beachten Sie, dass jedes Widget bei Bedarf in der Größe verändert und gelöscht werden kann. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/global-report.md#modify-dashboard).

## Experimentieren Bericht {#experimentation-global}

>[!AVAILABILITY]
>
>Die Funktion für Inhaltsexperimente ist derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie beim Adobe-Support.

![](assets/experimentation_report_3.png)

Die Registerkarte **[!UICONTROL Experimentieren]** in Ihrem **[!UICONTROL globalen Bericht]** in Campaign enthält die wichtigsten Informationen bezüglich der Leistung der einzelnen Varianten und auch dazu, ob es eine Leistung gibt, die besonders positiv heraussticht.

Beachten Sie, dass es ein wenig dauern kann, um die beste Leistung zu ermitteln. Sie wird durch das Symbol ![](assets/experimentation_report_1.png) gekennzeichnet.

Die Widget **[!UICONTROL Experimentergebnis]** liefert Details zur Leistung der einzelnen Varianten. Sie können Ihre Grundlinie ändern, indem Sie eine der Behandlungen aus der Dropdown-Liste **[!UICONTROL Grundlinie]** auswählen. Die beste Behandlung wird mit einem Sternsymbol gekennzeichnet.

Die Tabelle enthält die folgenden Metriken:

* **[!UICONTROL Profile]**: Anzahl der für diese Behandlung ausgewählten Profile.

* **[!UICONTROL Ausgehende Einzelklicks]**: Gesamtanzahl der Klicks in allen ausgehenden Kanälen.

* **[!UICONTROL Anzahl pro Profil]**: Gesamtwert der Experimentziel-Metrik dividiert durch die Anzahl der Profile.

* **[!UICONTROL Konfidenzintervall]**: prozentualer Leistungsunterschied zwischen der Grundlinie und der Behandlung mit der besten Leistung. [Weitere Informationen](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Durchschnittlicher Anstieg]**: prozentuale Verbesserung der Konversionsrate einer bestimmten Behandlung im Vergleich zur Grundlinie. [Weitere Informationen](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Behandlung mit der Grundlinienbehandlung identisch ist. [Weitere Informationen](../campaigns/experiment-calculations.md#understand-confidence)

Einen tiefen Einblick in diese Ergebnisse und ihre Interpretation finden Sie auf [dieser Seite](../campaigns/get-started-experiment.md#interpret-results).
