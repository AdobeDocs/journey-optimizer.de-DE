---
title: Segmentnutzung in einer Journey
description: Erfahren Sie, wie Sie ein Segment in einer Journey verwenden
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 0%

---

# Segment in einer Journey verwenden{#segment-trigger-activity}

![](../assets/do-not-localize/badge.png)

## Über die Aktivität „Segment lesen“ {#about-segment-trigger-actvitiy}

Mit der Aktivität „Segment-Lesen“ können Sie alle Kontakte, die zu einem Adobe Experience Platform-Segment gehören, in eine Journey eintreten lassen. Der Eintritt in eine Journey kann entweder einmalig oder regelmäßig erfolgen.

Nehmen wir als Beispiel das Segment &quot;Luma app open and checkout&quot;, das im Anwendungsfall [Build segmente](../segment/about-segments.md) erstellt wurde. Mit der Aktivität zum Lesen von Segmenten können Sie alle zu diesem Segment gehörenden Personen in eine Journey einbinden und sie in individuelle Journey umwandeln, die alle Journey-Funktionen nutzen: Bedingungen, Timer, Ereignisse, Aktionen.

>[!NOTE]
>
>Es ist nicht möglich, eine segmentbasierte Journey innerhalb eines kürzeren Zeitrahmens als 1 Stunde Trigger.

### Aktivität {#configuring-segment-trigger-activity} konfigurieren

Die Aktivität zum Lesen der Segmente wird wie folgt konfiguriert:

1. Erweitern Sie die Kategorie **[!UICONTROL Orchestrierung]** und legen Sie eine Aktivität vom Typ **[!UICONTROL Segment lesen]** auf Ihrer Arbeitsfläche ab.

   Die Aktivität muss als erster Schritt einer Journey positioniert werden.

1. Fügen Sie der Aktivität einen **[!UICONTROL Titel]** hinzu (optional).

1. Wählen Sie im Feld **[!UICONTROL Segment]** das Adobe Experience Platform-Segment, das die Journey eingibt, und klicken Sie dann auf **[!UICONTROL Speichern]**.

   Beachten Sie, dass Sie die in der Liste angezeigten Spalten anpassen und sortieren können.

   >[!NOTE]
   >
   >Nur Personen mit den Segmentteilnahmestatus **Realized** und **Vorhandene** werden in die Journey aufgenommen. Weitere Informationen zum Auswerten eines Segments finden Sie in der [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results).

   ![](../assets/read-segment-selection.png)

   Nachdem das Segment hinzugefügt wurde, können Sie mit der Schaltfläche **[!UICONTROL Kopieren]** dessen Namen und ID kopieren:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](../assets/read-segment-copy.png)

1. Wählen Sie im Feld **[!UICONTROL Namespace]** den Namespace aus, der zur Identifizierung der Einzelanwender verwendet werden soll. [Erfahren Sie mehr über Namensraum](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Kontakte, die zu einem Segment gehören, das nicht die ausgewählte Identität (den ausgewählten Namespace) hat, können nicht in die Journey eintreten.

1. Mit der Aktivität **[!UICONTROL Segment lesen]** können Sie den Zeitpunkt festlegen, zu dem das Segment in die Journey eintreten wird. Klicken Sie dazu auf den Link **[!UICONTROL Journey-Planung bearbeiten]**, um auf die Eigenschaften der Journey zuzugreifen, und konfigurieren Sie dann das Feld **[!UICONTROL Planungstyp]**.

   ![](../assets/read-segment-schedule.png)

   Standardmäßig treten Segmente **[!UICONTROL so bald wie möglich]** in die Journey ein, d. h. eine Stunde nach der Veröffentlichung der Journey. Wenn das Segment zu einem bestimmten Datum/zu einer bestimmten Uhrzeit oder wiederholt in die Journey eintreten soll, wählen Sie den gewünschten Wert aus der Liste aus.

   >[!NOTE]
   >
   >Beachten Sie, dass der Bereich **[!UICONTROL Plan]** nur verfügbar ist, wenn eine **[!UICONTROL Segment lesen]**-Aktivität auf der Arbeitsfläche abgelegt wurde.

   ![](../assets/read-segment-schedule-list.png)

### Testen und Veröffentlichen der Journey {#testing-publishing}

Mit der Aktivität **[!UICONTROL Segment lesen]** können Sie die Journey entweder auf einem unitären Profil oder auf 100 Testprofilen testen, die per Zufallsauswahl aus den für das Segment qualifizierten Profilen entnommen werden.

Aktivieren Sie dazu den Testmodus und wählen Sie dann im linken Bereich die gewünschte Option aus.

![](../assets/read-segment-test-mode.png)

Anschließend können Sie den Testmodus wie gewohnt konfigurieren und ausführen. [Erfahren Sie, wie Sie eine Journey](testing-the-journey.md) testen.

Sobald der Test ausgeführt wird, können Sie mit der Schaltfläche Protokolle **[!UICONTROL anzeigen]** die Testergebnisse entsprechend der ausgewählten Testoption anzeigen:

* **[!UICONTROL Jeweils ein Einzelprofil]**: Die Testprotokolle zeigen dieselben Informationen an wie bei Verwendung des einheitlichen Testmodus. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Bis zu 100 Profile gleichzeitig]**: Mithilfe der Testprotokolle können Sie den Verlauf des Segmentexports aus Adobe Experience Platform sowie den individuellen Fortschritt aller Personen, die die Journey begonnen haben, verfolgen.

   Beachten Sie, dass beim Testen der Journey mit bis zu 100 Profilen auf einmal der Fortschritt der einzelnen in der Journey enthaltenen Kontakte nicht über den visuellen Verlauf nachverfolgt werden kann.

   ![](../assets/read-segment-log.png)

Nach erfolgreichem Abschluss der Tests können Sie Ihre Journey veröffentlichen (siehe [Veröffentlichen der Journey](publishing-the-journey.md)). Kontakte, die zum Segment gehören, treten an dem Datum/zu der Uhrzeit in die Journey ein, das bzw. die im Bereich **[!UICONTROL Planung]** der Eigenschaften der Journey festgelegt ist.

>[!NOTE]
>
>Wenn eine segmentbasierte Journey ausgeführt wird, die nicht wiederholt auftritt (&quot;sobald wie möglich starten&quot;oder &quot;einmal&quot;), wird der Status automatisch in &quot;geschlossen&quot;geändert.
>
>Bei wiederholten segmentbasierten Journey wird die Journey automatisch geschlossen, sobald das letzte Vorkommen ausgeführt wird. Wenn kein Enddatum/keine Endzeit angegeben wurde, müssen Sie die Journey an neuen Eingängen manuell schließen, um sie zu beenden.


## Audiencen-Targeting in segmentbasierten Journey

Segmentbasierte Journey verwenden immer einen Beginn mit der Aktivität **Read segment**, um Personen abzurufen, die zu einem Adobe Experience Platform-Segment gehören.

Die Audience des Segments wird ein- oder regelmäßig abgerufen.

Nach der Eingabe der Journey können Sie Anwendungsfälle für die Audience-Orchestrierung erstellen, sodass Einzelpersonen aus dem ersten Segment in verschiedene Zweige der Journey fließen.

**Segmentierung**

Sie können Bedingungen verwenden, um mithilfe der Aktivität **Bedingung** eine Segmentierung durchzuführen. Sie können beispielsweise VIP Personen einen bestimmten Pfad und nicht VIP Fluss in einem anderen Pfad einschlagen lassen.

Die Segmentierung kann auf Folgendem basieren:

* Datenquellendaten
* der Kontext von Ereignissen Teil der Journey-Daten, z. B.: Hat eine Person auf die Nachricht geklickt, die sie vor einer Stunde erhalten hat?
* ein Datum, z. B.: Sind wir im Juni, wenn eine Person durch die Journey geht?
* eine Zeit, z. B.: Ist es Morgen in der Zeitzone der Person?
* ein Algorithmus, der die in der Journey fließende Audience auf Grundlage eines Prozentsatzes aufteilt, z. B.: 90 % - 10 % für den Ausschluss einer Kontrollgruppe

![](../assets/read-segment-audience1.png)

**Ausschluss**

Die gleiche **Bedingung**-Aktivität, die für die Segmentierung verwendet wird (siehe oben), ermöglicht es Ihnen auch, einen Teil der Population auszuschließen. Sie können beispielsweise VIP Personen ausschließen, indem Sie sie mit einem Endschritt direkt danach in eine Zweigniederlassung leiten lassen.

Dieser Ausschluss kann unmittelbar nach Segmentabruf, zu Zwecken der Bevölkerungszählung oder entlang einer mehrstufigen Journey erfolgen.

![](../assets/read-segment-audience2.png)

**Vereinigung**

Mit Journey können Sie N Zweige erstellen und nach einer Segmentierung zusammenführen.

Daher können Sie zwei Audiencen zu einem allgemeinen Erlebnis zurückkehren lassen.

Wenn Sie beispielsweise während zehn Tagen in einer Journey einem anderen Erlebnis folgen, können VIP und Nicht-VIP zum gleichen Pfad zurückkehren.

Nach einer Vereinigung können Sie die Audience erneut teilen, indem Sie eine Segmentierung oder einen Ausschluss durchführen.

![](../assets/read-segment-audience3.png)
