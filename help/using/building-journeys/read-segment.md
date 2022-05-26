---
title: Segment in einer Journey verwenden
description: Erfahren Sie, wie Sie ein Segment in einer Journey verwenden können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 0facae9e7eafc9f6fcbefbdc6d5563322eaf1251
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 97%

---

# Segment in einer Journey verwenden {#segment-trigger-activity}

## Hinzufügen der Aktivität Segment lesen {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Aktivität „Segment lesen“"
>abstract="Mit der Aktivität „Segment-Lesen“ können Sie alle Kontakte, die zu einem Adobe Experience Platform-Segment gehören, in eine Journey eintreten lassen. Der Eintritt in eine Journey kann entweder einmalig oder regelmäßig erfolgen."

Mit der Aktivität „Segment-Lesen“ können Sie alle Kontakte, die zu einem Adobe Experience Platform-Segment gehören, in eine Journey eintreten lassen. Der Eintritt in eine Journey kann entweder einmalig oder regelmäßig erfolgen.

Nehmen wir als Beispiel das Segment „Luma app open and checkout“, das beim Anwendungsfall [Segmente erstellen](../segment/about-segments.md) erstellt wurde. Mit der Aktivität „Segment lesen“ können Sie alle Kontakte, die zu diesem Segment gehören, in eine Journey eintreten lassen und durch individuelle Journeys führen, die alle Journey-Funktionen nutzen: Bedingungen, Timer, Ereignisse, Aktionen.

>[!NOTE]
>
>Das kostenpflichtige Burst-Add-on ermöglicht den schnellen Versand großer Mengen von Push-Benachrichtigungen für einfache Journeys, die die Aktivität „Segment lesen“ und eine einfache Push-Benachrichtigung enthalten. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../building-journeys/journey-gs.md#burst)

### Aktivität konfigurieren {#configuring-segment-trigger-activity}

Die Aktivität „Segment lesen“ wird wie folgt konfiguriert:

1. Erweitern Sie die Kategorie **[!UICONTROL Orchestrierung]** und legen Sie eine Aktivität vom Typ **[!UICONTROL Segment lesen]** auf Ihrer Arbeitsfläche ab.

   Die Aktivität muss als erster Schritt einer Journey positioniert werden.

1. Fügen Sie der Aktivität einen **[!UICONTROL Titel]** hinzu (optional).

1. Wählen Sie im Feld **[!UICONTROL Segment]** das Adobe Experience Platform-Segment aus, das in die Journey eintreten soll, und klicken Sie dann auf **[!UICONTROL Speichern]**.

   Beachten Sie, dass Sie die in der Liste angezeigten Spalten anpassen und sortieren können.

   >[!NOTE]
   >
   >Nur Einzelpersonen mit den Segmentteilnahmestatus **Realisiert** und **Vorhanden** können in die Journey eintreten. Weitere Informationen zum Auswerten eines Segments finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de){target=&quot;_blank&quot;}.

   ![](assets/read-segment-selection.png)

   Nachdem das Segment hinzugefügt wurde, können Sie mit der Schaltfläche **[!UICONTROL Kopieren]** dessen Namen und ID kopieren:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. Wählen Sie im Feld **[!UICONTROL Namespace]** den Namespace aus, der zur Identifizierung der Kontakte verwendet werden soll. [Weitere Informationen über Namespaces](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Kontakte, die zu einem Segment gehören, das nicht die ausgewählte Identität (den ausgewählten Namespace) hat, können nicht in die Journey eintreten.

1. Definieren Sie im Feld **[!UICONTROL Einschränkungsrate]** das Durchsatz-Limit der Aktivität „Segment lesen“.

   Dieser Wert wird in der Payload der Journey-Version gespeichert. Der Standardwert ist 20.000 Nachrichten pro Sekunde. Sie können diesen Wert zwischen 500 und 20.000 Nachrichten pro Sekunde variieren.

   >[!NOTE]
   >
   >Die Gesamteinschränkungsrate pro Sandbox ist auf 20.000 Nachrichten pro Sekunde festgelegt. Daher ergibt die Einschränkungsrate aller gleichzeitig in derselben Sandbox ausgeführten Lesesegmente maximal 20.000 Nachrichten pro Sekunde. Sie können diese Begrenzung nicht ändern.

1. Mit der Aktivität **[!UICONTROL Segment lesen]** können Sie den Zeitpunkt festlegen, zu dem das Segment in die Journey eintreten wird. Klicken Sie dazu auf den Link **[!UICONTROL Journey-Planung bearbeiten]**, um auf die Eigenschaften der Journey zuzugreifen, und konfigurieren Sie dann das Feld **[!UICONTROL Planungstyp]**.

   ![](assets/read-segment-schedule.png)

   Standardmäßig treten Segmente **[!UICONTROL so bald wie möglich]** in die Journey ein. Wenn das Segment zu einem bestimmten Datum/zu einer bestimmten Uhrzeit oder wiederholt in die Journey eintreten soll, wählen Sie den gewünschten Wert aus der Liste aus.

   >[!NOTE]
   >
   >Beachten Sie, dass der Bereich **[!UICONTROL Plan]** nur verfügbar ist, wenn eine **[!UICONTROL Segment lesen]**-Aktivität auf der Arbeitsfläche abgelegt wurde.

   ![](assets/read-segment-schedule-list.png)

   Mit der Option **Inkrementelles Lesen** haben Sie die Möglichkeit, nur die Personen anzusprechen, die seit der letzten Ausführung der Journey in das Segment eingetreten sind. Bei der ersten Ausführung sind immer alle Segmentmitglieder ausgewählt. Diese Option ist nur für wiederkehrende **Segment lesen**-Aktivitäten verfügbar.

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>Journey zum Lesen von Segmenten mit einer Aufnahme wechseln 30 Tage nach der Journey-Ausführung in den Status Abgeschlossen . Bei geplanten Read-Segmenten ist es 30 Tage nach der Ausführung des letzten Vorkommens.

### Testen und Veröffentlichen der Journey {#testing-publishing}

Mit der Aktivität **[!UICONTROL Segment lesen]** können Sie die Journey entweder auf einem unitären Profil oder auf 100 Testprofilen testen, die per Zufallsauswahl aus den für das Segment qualifizierten Profilen entnommen werden.

Aktivieren Sie dazu den Testmodus und wählen Sie dann im linken Bereich die gewünschte Option aus.

![](assets/read-segment-test-mode.png)

Anschließend können Sie den Testmodus wie gewohnt konfigurieren und ausführen. [Erfahren Sie, wie Sie eine Journey testen](testing-the-journey.md).

Sobald der Test ausgeführt wird, können Sie mit der Schaltfläche Protokolle **[!UICONTROL anzeigen]** die Testergebnisse entsprechend der ausgewählten Testoption anzeigen:

* **[!UICONTROL Jeweils ein Einzelprofil]**: Die Testprotokolle zeigen dieselben Informationen an wie bei Verwendung des einheitlichen Testmodus. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Bis zu 100 Profile gleichzeitig]**: Mithilfe der Testprotokolle können Sie den Verlauf des Segmentexports aus Adobe Experience Platform sowie den individuellen Fortschritt aller Personen, die die Journey begonnen haben, verfolgen.

   Beachten Sie, dass beim Testen der Journey mit bis zu 100 Profilen auf einmal der Fortschritt der einzelnen in der Journey enthaltenen Kontakte nicht über den visuellen Verlauf nachverfolgt werden kann.

   ![](assets/read-segment-log.png)

Nach erfolgreichem Abschluss der Tests können Sie Ihre Journey veröffentlichen (siehe [Veröffentlichen der Journey](publishing-the-journey.md)). Kontakte, die zum Segment gehören, treten an dem Datum/zu der Uhrzeit in die Journey ein, das bzw. die im Bereich **[!UICONTROL Planung]** der Eigenschaften der Journey festgelegt ist.

>[!NOTE]
>
>Bei segmentbasierten, wiederkehrenden Journeys wird die Journey automatisch nach der letztmaligen Ausführung geschlossen. Wenn kein Enddatum/keine Endzeit angegeben wurde, müssen Sie die Journey manuell für neue Eintritte schließen, um sie zu beenden.

## Zielgruppenbestimmung bei segmentbasierten Journeys

Segmentbasierte Journeys beginnen immer mit der Aktivität **Segment lesen**, um Personen abzurufen, die einem Adobe Experience Platform-Segment angehören.

Die Audience des Segments wird einmalig oder regelmäßig abgerufen.

Nach Eintritt in die Journey können Sie Anwendungsfälle für die Audience-Orchestrierung erstellen, sodass Einzelpersonen aus dem ersten Segment in verschiedene Zweige der Journey geleitet werden.

**Segmentierung**

Mithilfe der Aktivität **Bedingung** können Sie eine Segmentierung anhand von Bedingungen durchführen. Sie können beispielsweise VIP-Personen auf einen bestimmten Pfad führen und alle übrigen Personen auf einen anderen Pfad.

Die Segmentierung kann basieren auf:

* Daten aus Datenquellen
* Kontext von Ereignissen, die Teil der Journey-Daten sind – Beispiel: Hat eine Person auf die Nachricht geklickt, die sie vor einer Stunde erhalten hat?
* Datum – Beispiel: Sind wir im Juni, wenn eine Person durch die Journey navigiert?
* Tageszeit – Beispiel: Ist es morgens in der Zeitzone der Person?
* Algorithmus, der die in die Journey geführte Audience auf der Basis eines Prozentsatzes aufteilt – Beispiel: 90 % - 10 % für den Ausschluss einer Kontrollgruppe

![](assets/read-segment-audience1.png)

**Ausschluss**

Die selbe Aktivität **Bedingung**, die für die Segmentierung verwendet wird (siehe oben), ermöglicht es Ihnen auch, einen Teil der Population auszuschließen. Sie können beispielsweise VIP-Personen ausschließen, indem Sie diese in einen Zweig mit direkt anschließendem Beenden-Schritt führen.

Dieser Ausschluss kann unmittelbar nach Segmentabruf, zu Zwecken der Populationszählung oder als Teil einer mehrstufigen Journey erfolgen.

![](assets/read-segment-audience2.png)

**Vereinigung**

Journeys erlauben das Erstellen von n Zweigen, die nach einer Segmentierung zusammengeführt werden.

Daher können Sie zwei Audiences zu einem gemeinsamen Erlebnis zurückkehren lassen.

Ein Beispiel: Im Anschluss an ein zehntägiges differenziertes Erlebnis in einer Journey können VIP- und Nicht-VIP-Kunden zum selben Pfad zurückkehren.

Nach einer Vereinigung können Sie die Audience erneut teilen, indem Sie eine Segmentierung oder einen Ausschluss durchführen.

![](assets/read-segment-audience3.png)
