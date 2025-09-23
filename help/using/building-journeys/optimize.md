---
solution: Journey Optimizer
product: journey optimizer
title: Optimierungaktivität
description: Informationen zur Aktivität „Optimieren“
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Aktivität, Bedingung, Arbeitsfläche, Journey, Optimierung
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
source-git-commit: c472ce00623b810dea60dd5d9e34ca4d516447ad
workflow-type: tm+mt
source-wordcount: '1298'
ht-degree: 38%

---

# Optimierungaktivität {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Optimierungaktivität"
>abstract="Mit der Aktivität **Optimieren** können Sie festlegen, wie Einzelpersonen Ihre Journey durchlaufen, indem Sie mehrere Pfade auf der Grundlage spezifischer Kriterien erstellen, darunter Experimente, Targeting und bestimmte Bedingungen."

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.

Mit der Aktivität **Optimieren** können Sie festlegen, wie Einzelpersonen Ihre Journey durchlaufen, indem Sie mehrere **Pfade** auf der Grundlage spezifischer Kriterien erstellen, darunter Experimente, Targeting und bestimmte Bedingungen. So gewährleisten Sie ein Höchstmaß an Engagement und Erfolg, um hochgradig personalisierte und effektive Journeys zu erstellen.

Ein Journey **Pfad** kann aus einer der folgenden Variablen bestehen: Sequenzierung der Kommunikation, dazwischen liegende Zeit, Anzahl der Kommunikationen oder eine beliebige Kombination dieser drei Variablen.

Ein Pfad kann beispielsweise eine E-Mail enthalten, ein anderer zwei SMS-Nachrichten und ein dritter eine E-Mail, einen Warteknoten von zwei Stunden und dann eine SMS-Nachricht.

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

Durch die Aktivität **Optimieren** können Sie die folgenden Aktionen für die resultierenden Pfade ausführen:

* [Pfadexperimente](#experimentation) durchführen
* [Targeting](#targeting)-Regeln in jedem Journey-Pfad nutzen
* [Bedingungen](#conditions) auf Ihre Pfade anwenden

![](assets/journey-optimize.png)

Sobald die Journey live ist, werden die Profile anhand der definierten Kriterien bewertet und basierend auf den passenden Kriterien auf den entsprechenden Pfad der Journey weitergeleitet.

## Verwenden von Experimenten {#experimentation}

>[!CONTEXTUALHELP]
>id="ajo_path_experiment_success_metric"
>title="Erfolgsmetrik"
>abstract="Die Erfolgsmetrik wird verwendet, um die Abwandlung mit der besten Leistung in einem Experiment zu verfolgen und zu bewerten."

Mit Experimenten können Sie verschiedene Pfade auf der Grundlage einer zufälligen Aufteilung testen, um anhand vordefinierter Erfolgsmetriken zu ermitteln, welcher Pfad am besten funktioniert.

Gehen Sie wie folgt vor, um Pfadexperimente auf einer Journey einzurichten.

Angenommen, Sie möchten drei Pfade vergleichen:

* einen Pfad mit einer E-Mail,
* einen zweiten Pfad mit einem **[!UICONTROL Warte]**-Knoten von zwei Tagen und einer E-Mail;
* einen dritten Pfad mit einer E-Mail und dann einer SMS-Nachricht.

1. Ziehen Sie aus dem Abschnitt **[!UICONTROL Orchestrierung]** die Aktivität **[!UICONTROL Optimieren]** per Drag-and-Drop auf die Journey-Arbeitsfläche.

1. Fügen Sie eine optionale Beschriftung hinzu, die nützlich sein kann, um die Aktivität in Reporting- und Testmodusprotokollen zu identifizieren.

1. Wählen Sie **[!UICONTROL Experiment]** aus der Dropdown-Liste **[!UICONTROL Methode]** aus.

   ![](assets/journey-optimize-experiment.png){width=65%}

1. Klicken Sie **[!UICONTROL Experiment erstellen]**.

1. Wählen Sie **[!UICONTROL Erfolgsmetrik]**, die Sie für Ihr Experiment festlegen möchten. Weitere Informationen zu den verfügbaren Metriken und zur Konfiguration der Liste finden [ in diesem Abschnitt](success-metrics.md).

   <!--Need to have the list of all default metrics + a description for each.
    Explain why the metric selection is important.
    Are there custom metrics? If so explain.
    If possible, add best practices and examples for each metrics (could even be a dedicated section).
    Consider adding an example in this step: For this example, select this metric to test xxx.
    -->

   ![](assets/journey-optimize-experiment-metrics.png){width=80%}

1. Sie können eine &quot;**[!UICONTROL &quot;-]** zu Ihrem Versand hinzufügen. Diese Gruppe gibt keinen Pfad aus diesem Experiment ein.

   >[!NOTE]
   >
   >Wenn Sie den Umschalter aktivieren, werden automatisch 10 % Ihrer Population übernommen. Sie können diesen Prozentsatz bei Bedarf anpassen.

   <!--
    DOES THIS APPLY TO PATH EXPERIMENT?
    IMPORTANT: When a holdout group is used in an action for path experimentation, the holdout assignment only applies to that specific action. After the action is completed, profiles in the holdout group will continue down the journey path and can receive messages from other actions. Therefore, ensure that any subsequent messages do not rely on the receipt of a message by a profile that might be in a holdout group. If they do, you may need to remove the holdout assignment.-->

1. Sie können jeder **[!UICONTROL Variante“ einen bestimmten Prozentsatz zuweisen]** einfach den Umschalter **[!UICONTROL Gleichmäßig verteilen]** aktivieren.

   ![](assets/journey-optimize-experiment-treatments.png){width=80%}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Definieren Sie die gewünschten Elemente für jede Verzweigung, die aus dem Experiment resultiert, z. B.:

   * Ziehen Sie eine [E-Mail](../email/create-email.md)-Aktivität auf den ersten Zweig (**Abwandlung A**).

   * Ziehen Sie eine [Warten](wait-activity.md)-Aktivität von zwei Tagen auf den ersten Zweig, gefolgt von einer [E-Mail](../email/create-email.md)-Aktivität (**Behandlung B**).

   * Ziehen Sie eine Aktivität [E-Mail](../email/create-email.md) auf den dritten Zweig, gefolgt von einer Aktivität [SMS](../sms/create-sms.md) (**Abwandlung C**).

   ![](assets/journey-optimize-experiment-ex.png){width=100%}

1. Verwenden Sie optional den **[!UICONTROL Alternativen Pfad hinzufügen, falls eine Zeitüberschreitung oder ein Fehler auftritt]** um eine Ausweichaktion zu definieren. [Weitere Informationen](using-the-journey-designer.md#paths)

1. Wählen Sie eine Kanalaktion aus und verwenden Sie die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**, um auf die Design-Tools zuzugreifen.

   ![](assets/journey-optimize-experiment-edit-content.png){width=70%}

1. Von dort aus können Sie mithilfe des linken Bereichs zwischen den verschiedenen Inhalten für jede Aktion in Ihrem Experiment navigieren. Wählen Sie jeden Inhalt aus und entwerfen Sie ihn nach Bedarf.

   ![](assets/journey-optimize-experiment-content.png){width=100%}

1. [Veröffentlichen](publishing-the-journey.md) Ihres Journey.

Sobald die Journey live ist, werden die Benutzenden nach dem Zufallsprinzip zugewiesen, um verschiedene Pfade zu durchlaufen. [!DNL Journey Optimizer] verfolgt, welcher Pfad am besten funktioniert, und liefert verwertbare Einblicke.

Verfolgen Sie den Erfolg Ihres Journey mit dem Journey-Pfad-Experimentbericht. [Weitere Informationen](../reports/journey-global-report-cja-experimentation.md)

### Anwendungsfälle für Experimente {#uc-experiment}

Die folgenden Beispiele zeigen, wie Sie mit der Aktivität **[!UICONTROL Optimieren]** zusammen mit der Methode **[!UICONTROL Experiment]** ermitteln, welcher Pfad insgesamt am besten funktioniert.

+++Kanaleffektivität

Testen Sie, ob das Senden der ersten Nachricht per E-Mail oder per SMS zu höheren Konversionen führt.

➡️ Verwenden Sie die Konversionsrate als Erfolgsmetrik (z. B.: Käufe, Anmeldungen).

![](assets/journey-optimize-experiment-uc-channel.png)

+++

+++Nachrichtenfrequenz

Führen Sie ein Experiment durch, um zu überprüfen, ob der Versand einer E-Mail im Vergleich zu drei E-Mails pro Woche zu mehr Käufen führt.

➡️ Verwenden Sie Käufe oder die Abmelderate als Erfolgsmetrik.

![](assets/journey-optimize-experiment-uc-frequency.png)

+++

+++Wartezeit zwischen Nachrichten

Vergleichen Sie eine Wartezeit von 24 Stunden mit einer Wartezeit von 72 Stunden vor einem Nachfassen, um zu ermitteln, welcher Zeitraum die Interaktion maximiert.

➡️ Verwenden Sie die Clickthrough-Rate oder den Umsatz als Erfolgsmetrik.

![](assets/journey-optimize-experiment-uc-wait.png)

+++

## Nutzen von Targeting {#targeting}

>[!CONTEXTUALHELP]
>id="ajo_path_targeting_fallback"
>title="Was ist ein Fallback-Pfad?"
>abstract="Mit Fallback-Pfaden kann Ihre Zielgruppe einen alternativen Pfad beschreiten, falls keine der Targeting-Regeln erfüllt wird. </br>Wenn Sie diese Option nicht aktivieren, werden Zielgruppen, die sich für keine Targeting-Regel qualifizieren, nicht in den Fallback-Pfad aufgenommen. Zudem wird die Journey beendet."

Mit Targeting-Regeln können Sie bestimmte Regeln oder Qualifikationen festlegen, die eine Kundin oder ein Kunde basierend auf bestimmten Zielgruppensegmenten erfüllen muss, um für den Eintritt in einen der Journey-Pfade berechtigt zu <!-- depending on profile attributes or contextual attributes-->.

Im Gegensatz zu Experimenten, bei denen es sich um eine zufällige Zuweisung eines bestimmten Pfads handelt, ist das Targeting deterministisch, da sichergestellt wird, dass die richtige Zielgruppe oder das richtige Profil in den angegebenen Pfad eintritt.

<!--With targeting, specific rules can be defined based on:

* **User profile attributes** such as location (eg. geo-targeting), age, or preferences. For example, users in the US receive a "Golden Gate" promotion, while users in France receive an "Eiffel Tower" promotion.

* **Contextual data** such as device type (eg. device-targeting), time of day, or session details. For example, desktop users receive desktop-optimized content, while mobile users receive mobile-optimized content.

* **Audiences** which can be used to include or exclude profiles that have a particular audience membership.-->

Gehen Sie folgendermaßen vor, um das Targeting in einer Journey einzurichten.

1. Ziehen Sie aus dem Abschnitt **[!UICONTROL Orchestrierung]** die Aktivität **[!UICONTROL Optimieren]** per Drag-and-Drop auf die Journey-Arbeitsfläche.

1. Fügen Sie eine optionale Beschriftung hinzu, die nützlich sein kann, um die Aktivität in Reporting- und Testmodusprotokollen zu identifizieren.

1. Wählen **[!UICONTROL Zielgruppenbestimmungsregel]** aus der Dropdown **[!UICONTROL Liste]** Methode“ aus.

   ![](assets/journey-optimize-targeting.png){width=60%}

1. Klicken Sie auf **[!UICONTROL Targeting-Regel erstellen]**.

1. Verwenden Sie den Regel-Builder, um Ihre Kriterien festzulegen. Definieren Sie beispielsweise eine Regel für Gold-Mitglieder des Treueprogramms (`loyalty.status.equals("Gold", false)`) und eine Regel für die anderen Mitglieder (`loyalty.status.notEqualTo("Gold", false)`).

   ![](assets/journey-targeting-rule.png)

1. Wählen Sie bei **[!UICONTROL die Option]** Fallback-Pfad aktivieren“ aus. Diese Aktion erstellt einen Fallback-Pfad für die Zielgruppe, der keiner der oben definierten Zielgruppenbestimmungsregeln entspricht.

   >[!NOTE]
   >
   >Wenn Sie diese Option nicht auswählen, gibt jede Zielgruppe, die sich nicht für eine Zielgruppenbestimmungsregel qualifiziert, den Fallback-Pfad nicht ein und beendet die Journey.

1. Klicken Sie **[!UICONTROL Erstellen]** um Ihre Einstellungen für die Zielgruppenregel zu speichern.

1. Kehren Sie zur Journey zurück und fügen Sie bestimmte Aktionen hinzu, um jeden Pfad anzupassen. Erstellen Sie beispielsweise eine E-Mail mit personalisierten Angeboten für Mitglieder des Treueprogramms Gold und eine SMS-Erinnerung für alle anderen Mitglieder.

   ![](assets/journey-targeting-paths.png)

1. Wenn Sie bei der Definition der **[!UICONTROL die Option]** Fallback-Inhalt aktivieren“ ausgewählt haben, definieren Sie eine oder mehrere Aktionen für den automatisch hinzugefügten Fallback-Pfad.

   ![](assets/journey-targeting-fallback.png){width=70%}

1. Verwenden Sie optional den **[!UICONTROL Alternativen Pfad hinzufügen, falls eine Zeitüberschreitung oder ein Fehler auftritt]** um eine alternative Aktion zu definieren, falls Probleme auftreten. [Weitere Informationen](using-the-journey-designer.md#paths)

1. Entwerfen Sie geeignete Inhalte für jede Aktion, die jeder durch Ihre Zielgruppenregeleinstellungen definierten Gruppe entspricht. Sie können für jede Aktion nahtlos zwischen den verschiedenen Inhalten navigieren.

   ![](assets/journey-targeting-design.png)

   In diesem Beispiel entwerfen Sie eine E-Mail mit Sonderangeboten für Gold-Mitglieder und einer SMS-Erinnerung für die anderen Mitglieder.

1. [Veröffentlichen](publishing-the-journey.md) Ihres Journey.

Sobald die Journey live ist, wird der für jedes Segment angegebene Pfad verarbeitet, sodass Gold-Mitglieder den Pfad mit den E-Mail-Angeboten eingeben, während die anderen Mitglieder den Pfad mit der SMS-Erinnerung eingeben.

Verfolgen Sie den Erfolg Ihres Journey mit dem Journey-Bericht. [Weitere Informationen](../reports/journey-global-report-cja.md#targeting)

### Anwendungsfälle für Targeting-Regeln {#uc-targeting}

Die folgenden Beispiele zeigen, wie die Aktivität **[!UICONTROL Optimieren]** mit der Methode **[!UICONTROL Targeting-Regel]** verwendet wird, um Pfade für verschiedene Unterzielgruppen zu personalisieren.

+++Segmentspezifische Kanäle

Mitglieder des Treueprogramms mit Gold-Status können personalisierte Angebote per E-Mail erhalten, während alle anderen Mitglieder zu SMS-Erinnerungen weitergeleitet werden.

<!--➡️ Use the revenue per profile or conversion rate as the optimization metric.-->

![](assets/journey-optimize-targeting-uc-segment.png)

+++

+++Verhaltensbasiertes Targeting

Kundinnen und Kunden, die eine E-Mail geöffnet, aber nicht geklickt haben, können eine Push-Benachrichtigung erhalten, während diejenigen, die sie überhaupt nicht geöffnet haben, eine SMS erhalten.

<!--➡️ Use the click-through rate or downstream conversions as the optimization metric.-->

![](assets/journey-optimize-targeting-uc-behavior.png)

+++

+++Zielgruppenbestimmung bezüglich des Kaufverlaufs

Kundinnen und Kunden, die kürzlich gekauft haben, können in einen kurzen „Danke + Crosssell“-Pfad eintreten, während Kundinnen und Kunden ohne Kaufhistorie eine längere Nurturing-Journey durchlaufen.

<!--➡️ Use the repeat purchase rate or engagement rate as the optimization metric.-->

![](assets/journey-optimize-targeting-uc-purchase.png)

+++

### Hinzufügen einer Bedingung {#conditions}

Bedingungen sind eine Art von [Targeting](#targeting)-Regeln, mit denen Sie festlegen können, wie sich Personen durch Ihren Journey bewegen, indem Sie mehrere Pfade auf der Grundlage bestimmter Kriterien erstellen.

![](assets/journey-condition.png)

Erfahren Sie in [diesem Abschnitt](conditions.md), wie Sie eine Bedingung definieren.

Folgende Bedingungstypen sind verfügbar:

* [Datenquellenbedingung](condition-activity.md#data_source_condition)
* [Bedingung für die Uhrzeit](condition-activity.md#time_condition)
* [Prozentuale Aufspaltung](condition-activity.md#percentage_split)
* [Bedingung für das Datum](condition-activity.md#date_condition)
* [Profilbegrenzung](condition-activity.md#profile_cap)
