---
title: Erstellen eines Inhaltsexperiments
description: Erfahren Sie, wie Sie in Ihren Kampagnen ein Inhaltsexperiment erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---

# Erstellen eines Inhaltsexperiments {#content-experiment}

Mit der Funktion für Inhaltsexperimente können Sie mehrere Versandbehandlungen definieren. Die Zielgruppe wird nach dem Zufallsprinzip jeder Behandlung zugeordnet, um festzustellen, welche die beste Leistung in Bezug auf die Zielmetrik erzielt. Sie können den Inhalt, den Betreff oder den Absender der E-Mail variieren.

Im folgenden Beispiel wurde die Zielgruppe in zwei Gruppen unterteilt, von denen jeweils 45 % der Zielgruppe und 10 % der Zielpopulation ausmachen, die den Versand nicht erhalten.

Jede Person in der Zielgruppe erhält eine Version der E-Mail mit einer Betreffzeile, die einer der beiden folgenden ist:

* ein direktes Bewerben eines 10 %-Angebots für die neue Sammlung und ein Bild.
* das andere nur ein spezielles Angebot bewerben, ohne die 10% Rabatt ohne Bild anzugeben.

Das Ziel besteht hier darin zu sehen, ob Empfänger je nach dem empfangenen Experiment mit der E-Mail interagieren. Wir werden daher **[!UICONTROL E-Mail wird geöffnet]** als primäre Zielmetrik in diesem Inhaltsexperiment.

![](assets/content_experiment.png)

## Erstellen Ihrer Kampagne {#campaign-experiment}

1. Aus dem **[!UICONTROL Kampagnen]** Seite, klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

   ![](assets/content_experiment_1.png)

1. Auswählen **[!UICONTROL Email]** dann die **[!UICONTROL Oberfläche]** Sie möchten für diesen Versand verwenden. Weitere Informationen hierzu finden Sie im Abschnitt [Kanaloberflächen](../configuration/channel-surfaces.md) Seite.

   ![](assets/content_experiment_2.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Richten Sie die **[!UICONTROL Eigenschaften]** Ihres Versands:
   * **[!UICONTROL Titel]**
   * **[!UICONTROL Beschreibung]**
   * **[!UICONTROL Kategorie]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. Um Ihr Inhaltsexperiment zu starten, schalten Sie die **[!UICONTROL Inhaltsexperiment]** -Option. Die **[!UICONTROL Inhaltsexperiment]** wird angezeigt.

   ![](assets/content_experiment_3.png)

1. Richten Sie die **[!UICONTROL Zielgruppe]** und **[!UICONTROL Zeitplan]** Versandparameter. [Weitere Informationen](create-campaign.md)

1. Klicken **[!UICONTROL Inhalt bearbeiten]** zur Personalisierung Ihrer anderen **[!UICONTROL Behandlung]**.

   ![](assets/content_experiment_4.png)

## Erstellen von Behandlungen {#treatment-experiment}

1. Aus dem **[!UICONTROL Inhalt bearbeiten]** -Fenster, fügen Sie die **[!UICONTROL Betreff]** für Ihre Behandlung Eine E-Mail und klicken Sie auf **[!UICONTROL Speichern]**.

   Für diese Behandlung wird das Angebot direkt in der Betreffzeile angegeben.

   ![](assets/content_experiment_5.png)

1. Klicken **[!UICONTROL Email Designer]** , um Ihre Sendungen zu personalisieren.

   ![](assets/content_experiment_6.png)

1. Klicken Sie nach dem Erstellen Ihrer E-Mail auf **[!UICONTROL Speichern]** und kehren zur **[!UICONTROL Inhalt bearbeiten]** Fenster zur Erstellung von Behandlung B.

1. Aus dem **[!UICONTROL Mehr Aktionen]** Schaltfläche, klicken Sie auf **[!UICONTROL Duplizieren]**.

   Sie können auch eine neue Behandlung starten, indem Sie auf die **[!UICONTROL Inhaltsexperiment]** -Schaltfläche, um auf die erweiterten Optionen zuzugreifen, und **[!UICONTROL Behandlung hinzufügen]**.

   ![](assets/content_experiment_7.png)

1. Ändern Sie die **[!UICONTROL Titel]** Ihrer Behandlung, um sie besser zu differenzieren.

   ![](assets/content_experiment_8.png)

1. Wählen Sie den mit Ihrem neu erstellten E-Mail-Versand verknüpften **[!UICONTROL Behandlung]**.

1. Fügen Sie die **[!UICONTROL Betreff]** für Ihren Versand.

   Für diese Behandlung legen wir das Angebot nicht im **[!UICONTROL Betreff]**.

   ![](assets/content_experiment_9.png)

1. Klicken **[!UICONTROL Email Designer]** , um bei Bedarf den Versand von Behandlung B weiter zu personalisieren.

Sobald Ihre Behandlungen personalisiert wurden, können Sie mit der Konfiguration Ihres Inhaltsexperiments beginnen.

## Konfigurieren des Inhaltsexperiments {#configure-experiment}

1. Wenn beide Sendungen personalisiert sind, wird im **[!UICONTROL Inhalt bearbeiten]** auswählen **[!UICONTROL Konfigurieren des Inhaltsexperiments]**.

   ![](assets/content_experiment_10.png)

1. Wählen Sie die Ziele aus, die Sie für Ihr Experiment festlegen möchten.

   Für unser Experiment wählen wir **[!UICONTROL Email open]** , um zu testen, ob Empfänger ihre E-Mails öffnen, wenn sich der Angebotscode in der Betreffzeile befindet.

   ![](assets/content_experiment_11.png)

1. Wählen Sie zum Hinzufügen einer **[!UICONTROL Holdout]** zu Ihrem Versand hinzugefügt. Diese Gruppe erhält keine Inhalte von dieser Kampagne.

   Das Umschalten auf die Umschalter-Leiste nimmt automatisch 10 % Ihrer Population in Anspruch. Sie können diesen Prozentsatz bei Bedarf anpassen.

   ![](assets/content_experiment_12.png)

1. Anschließend können Sie festlegen, jedem **[!UICONTROL Behandlung]** oder schalten Sie einfach die **[!UICONTROL Gleichmäßig verteilen]** Leiste ein/aus.

   ![](assets/content_experiment_13.png)

1. Klicken **[!UICONTROL Speichern]** wenn Ihre Konfiguration festgelegt ist.

1. Wenn Ihr Inhaltsexperiment fertig ist, können Sie auf **[!UICONTROL Aktivieren]** um eine Zusammenfassung der Kampagne anzuzeigen. Warnhinweise werden angezeigt, wenn ein Parameter falsch ist oder fehlt.

   ![](assets/content_experiment_15.png)

1. Vergewissern Sie sich, dass Ihre Kampagne korrekt konfiguriert ist, und klicken Sie dann auf **[!UICONTROL Aktivieren]** , um es zu starten.

   ![](assets/content_experiment_14.png)

