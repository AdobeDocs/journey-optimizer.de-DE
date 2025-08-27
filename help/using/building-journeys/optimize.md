---
solution: Journey Optimizer
product: journey optimizer
title: Aktivität „Bedingung“
description: Erfahren Sie mehr über Bedingungsaktivitäten
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Aktivität, Bedingung, Arbeitsfläche, Journey, Optimierung
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: a770cbc1736e7add7e25f2cc8210d81bd8b2e375
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 5%

---

# Aktivität optimieren {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Aktivität optimieren"
>abstract="Mit **Aktivität „Optimieren** können Sie festlegen, wie Kontakte über Ihren Journey fortschreiten, indem Sie mehrere Pfade auf der Grundlage bestimmter Kriterien wie Experimentieren, Targeting und bestimmter Bedingungen erstellen."

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.

Mit der Aktivität **Optimieren** können Sie festlegen, wie Kontakte über Ihren Journey voranschreiten, indem Sie mehrere **Pfade** basierend auf bestimmten Kriterien erstellen, einschließlich Experimentieren, Targeting und bestimmten Bedingungen. So stellen Sie ein Höchstmaß an Interaktion und Erfolg sicher, um hochgradig angepasste und effektive Journey zu erstellen.

Ein **Journey-Pfad** kann aus einem der folgenden Elemente bestehen:

* Sequenzierung der Kommunikation;
* Zeit zwischen ihnen;
* Anzahl der Mitteilungen;
* oder eine beliebige Kombination dieser drei Variablen.

Ein Pfad kann beispielsweise eine E-Mail enthalten, ein anderer zwei SMS-Nachrichten und ein dritter eine E-Mail, einen [Warte](wait-activity.md)-Knoten mit zwei Stunden und dann eine SMS-Nachricht.

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

Mit der Aktivität **Optimieren** können Sie:

* Ausführen [Pfadexperimenten](#experimentation)
* Nutzen [Targeting](#targeting)-Regeln in jedem Journey-Pfad
* Anwenden [Bedingungen](#conditions) auf Ihre Pfade

![](assets/journey-optimize.png)

Sobald die Journey live ist, werden die Profile anhand der definierten Kriterien bewertet. Anhand übereinstimmender Kriterien werden sie dann vom Journey in den entsprechenden Pfad weitergeleitet.

## Experimentieren verwenden {#experimentation}

Mit Experimenten können Sie verschiedene Pfade auf der Grundlage einer zufälligen Aufspaltung testen, um anhand vordefinierter Erfolgsmetriken zu bestimmen, welche am besten abschneidet.

Gehen Sie wie folgt vor, um das Experimentieren auf einer Journey einzurichten.

Angenommen, Sie möchten drei Pfade vergleichen:

* ein Pfad mit einer E-Mail;
* einen zweiten Pfad mit einem Warteknoten von zwei Tagen und einer E-Mail;
* einem dritten Pfad mit einer E-Mail-Adresse und einer SMS-Nachricht.

1. Ziehen Sie die Aktivität **[!UICONTROL Optimieren]** in die Arbeitsfläche Journey.

1. Fügen Sie eine optionale Beschriftung hinzu, um die Aktivität in den Reporting- und Testmodusprotokollen zu identifizieren.

1. Wählen Sie **[!UICONTROL Experiment]** aus der **[!UICONTROL Methode]** Dropdown-Liste aus.

   ![](assets/journey-optimize-experiment.png){width=85%}

1. Klicken Sie auf **[!UICONTROL Experimenteinstellungen]**.

1. Entwerfen und konfigurieren Sie Ihr Experiment nach Bedarf. [Weitere Informationen](../content-management/content-experiment.md)

   <!--
    ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}
    Replace with appropriate screenshot
    The experiment applies to all the activities in the journey.TBC
   -->

Sobald die Journey live ist, werden die Benutzenden nach dem Zufallsprinzip zugewiesen, verschiedene Pfade zu durchlaufen. [!DNL Journey Optimizer] verfolgt, welcher Pfad zu mehr Käufen führt, und bietet umsetzbare Einblicke.

<!--Follow the success of your journey with the [Experimentation journey report](../reports/campaign-global-report-cja-experimentation.md). Is there a report specific to experimentation in journey?-->

### Anwendungsfälle mit Experiment {#uc-experiment}

Die folgenden Beispiele zeigen, wie Sie mit der Aktivität **[!UICONTROL Optimieren]** mit der Methode **[!UICONTROL Experiment]** ermitteln, welcher Pfad insgesamt am besten funktioniert.

**Kanaleffektivität**

Testen Sie, ob das Senden der ersten Nachricht per E-Mail oder SMS zu höheren Konversionen führt.

* Konversionsrate als Optimierungsmetrik verwenden (z. B.: Käufe, Anmeldungen).

![](assets/journey-optimize-experiment-uc.png)

**Nachrichtenfrequenz**

Führen Sie ein Experiment durch, um zu überprüfen, ob der Versand einer E-Mail im Vergleich zu drei E-Mails pro Woche zu mehr Käufen führt.

* Verwenden Sie Käufe oder die Abmelderate als Optimierungsmetrik.

**Wartezeit zwischen Nachrichten**

Vergleich einer Wartezeit von 24 Stunden mit einer Wartezeit von 72 Stunden vor einer Nachbeobachtung, um zu bestimmen, welcher Zeitpunkt die Interaktion maximiert.

* Verwenden Sie die Clickthrough-Rate oder den Umsatz als Optimierungsmetrik.

## Verwenden von Targeting {#targeting}

Beim Targeting können Sie auf der Grundlage bestimmter Zielgruppensegmente bestimmte Regeln oder Qualifikationen festlegen, die erfüllt sein müssen, damit eine Kundin oder ein Kunde für den Eintritt in einen der Journey-Pfade berechtigt ist<!-- depending on profile attributes or contextual attributes-->.

Im Gegensatz zu Experimenten, bei denen es sich um eine zufällige Zuweisung eines bestimmten Pfads handelt, ist die Zielgruppenbestimmung deterministisch, indem sichergestellt wird, dass die richtige Zielgruppe oder das richtige Profil in den angegebenen Pfad eintritt.

Beim Targeting können spezifische Regeln definiert werden, die auf Folgendem basieren:

* **Benutzerprofilattribute** wie Speicherort (z. B. Geotargeting), Alter oder Voreinstellungen. In den USA wird beispielsweise eine „Golden Gate“-Promotion angeboten, in Frankreich hingegen eine „Eiffelturm“-Promotion.

* **Kontextdaten** wie Gerätetyp (z. B. Geräte-Targeting), Tageszeit oder Sitzungsdetails. Desktop-Benutzer erhalten beispielsweise Desktop-optimierte Inhalte, während mobile Benutzer Mobile-optimierte Inhalte erhalten.

* **Zielgruppen** mit denen Profile mit einer bestimmten Zielgruppenzugehörigkeit ein- oder ausgeschlossen werden können.

Gehen Sie wie folgt vor, um das Targeting auf einer Journey einzurichten.

1. Ziehen Sie die Aktivität **[!UICONTROL Optimieren]** in die Arbeitsfläche Journey.

1. Fügen Sie eine optionale Beschriftung hinzu, um die Aktivität in den Reporting- und Testmodusprotokollen zu identifizieren.

1. Wählen Sie **[!UICONTROL Targeting]** aus **[!UICONTROL Dropdown-Liste]** Methode“ aus.

   ![](assets/journey-optimize-targeting.png){width=85%}

1. Klicken Sie **[!UICONTROL Zielgruppenregel erstellen]**.

1. Verwenden Sie den Regel-Builder, um Ihre Kriterien zu definieren. Definieren Sie beispielsweise eine Regel für in den USA ansässige Personen, eine Regel für in Frankreich ansässige Personen und eine Regel für in Indien ansässige Personen.

   ![](assets/journey-targeting-rule.png)

1. Wählen Sie **[!UICONTROL Fallback-Inhalt aktivieren]** nach Bedarf aus. Mit Fallback-Inhalten kann Ihre Zielgruppe Standardinhalte empfangen, wenn keine Targeting-Regeln qualifiziert sind. Wenn Sie diese Option nicht auswählen, gibt jede Zielgruppe, die sich nicht für eine der oben definierten Zielgruppenbestimmungsregeln qualifiziert, keinen Fallback-Pfad ein.

1. Speichern Sie Ihre Einstellungen für die Zielgruppenregel.

1. Legen Sie bestimmte Aktionen auf der Journey ab, um jeden Pfad anzupassen. Sie können beispielsweise eine bestimmte E-Mail für US-Bürger, eine andere für in Frankreich ansässige Personen usw. erstellen.

   ![](assets/journey-targeting-paths.png)

1. Entwerfen Sie geeignete Inhalte für jede Gruppe, die durch die Einstellungen Ihrer Zielgruppenbestimmungsregeln definiert wird. Sie können nahtlos zwischen den verschiedenen Pfaden navigieren.

   ![](assets/journey-targeting-design.png)

   In diesem Beispiel entwerfen Sie einen bestimmten Pfad für US-Einwohner, einen anderen Pfad für französische Einwohner und einen anderen Pfad für Inder.

Sobald die Journey live ist, wird der für jedes Segment angegebene Pfad verarbeitet, sodass US-Bürger einen bestimmten Pfad eingeben, Frankreich-Bürger einen anderen Pfad eingeben usw.

### Anwendungsfälle mit Targeting {#uc-targeting}

Die folgenden Beispiele zeigen, wie die Aktivität **[!UICONTROL Optimieren]** mit der Methode **[!UICONTROL Targeting]** verwendet wird, um Pfade für verschiedene Unterzielgruppen zu personalisieren.

**Segmentspezifische Kanäle**

Mitglieder des Treueprogramms mit Gold-Status können personalisierte Angebote per E-Mail erhalten, während alle anderen Mitglieder zu SMS-Erinnerungen weitergeleitet werden.

* Verwenden Sie die Metrik Umsatz pro Profil oder Konversionsrate als Optimierungsmetrik.

![](assets/journey-optimize-targeting-uc.png)

**Verhaltensbasiertes Targeting**

Kunden, die eine E-Mail geöffnet, aber nicht geklickt haben, können eine Push-Benachrichtigung erhalten, während diejenigen, die überhaupt nicht geöffnet haben, eine SMS erhalten.

* Verwenden Sie die Clickthrough-Rate oder nachgelagerte Konversionen als Optimierungsmetrik.

**Zielgruppenbestimmung bezüglich des Kaufverlaufs**

Kunden, die kürzlich gekauft haben, können einen kurzen „Danke + Crosssell“-Weg einschlagen, während Kunden ohne Kaufhistorie eine längere Pflege-Journey erhalten.

* Verwenden Sie die Wiederholungskaufrate oder Interaktionsrate als Optimierungsmetrik.

## Hinzufügen einer Bedingung {#conditions}

Sie können eine Bedingung hinzufügen, um zu definieren, wie Kontakte durch Ihren Journey voranschreiten, indem Sie mehrere Pfade auf der Grundlage bestimmter Kriterien erstellen. Sie können auch einen alternativen Pfad konfigurieren, um mit Timeouts oder Fehlern umzugehen und so ein nahtloses Erlebnis sicherzustellen.

![](assets/journey-condition.png)

Erfahren Sie in ([ Abschnitt), wie Sie eine Bedingung ](conditions.md).

Folgende Bedingungstypen sind verfügbar:

* [Bedingung der Datenquelle](condition-activity.md#data_source_condition)
* [Bedingung für die Uhrzeit](condition-activity.md#time_condition)
* [Prozentuale Aufspaltung](condition-activity.md#percentage_split)
* [Bedingung für das Datum](condition-activity.md#date_condition)
* [Profilbegrenzung](condition-activity.md#profile_cap)
