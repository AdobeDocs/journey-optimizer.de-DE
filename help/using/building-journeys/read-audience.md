---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden einer Zielgruppe in einer Journey
description: Erfahren Sie, wie Sie die Aktivität „Zielgruppe lesen“ konfigurieren und verwenden, damit Personen aus - [!DNL Adobe Experience Platform]  in Journeys eintreten.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: Aktivität, Journey, Zielgruppe lesen, Zielgruppe, Segment, Batch, Einstiegspunkt, Trigger, Zeitplan, Zielgruppen-Qualifizierung
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
version: Journey Orchestration
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '3620'
ht-degree: 67%

---

# Verwenden einer Zielgruppe in einer Journey {#segment-trigger-activity}

Verwenden Sie die Aktivität Zielgruppe lesen , um Journey mit definierten Zielgruppen zu starten. Wählen Sie die Zielgruppe und den Zeitpunkt der Ausführung aus. Personalisieren Sie dann den Pfad jedes Profils mithilfe von Bedingungen, Timern und Aktionen.

## Über die Aktivität „Zielgruppe lesen“ {#about-segment-trigger-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Aktivität „Zielgruppe lesen“"
>abstract="Fügen Sie alle qualifizierten Profile einer ausgewählten [!DNL Adobe Experience Platform] Zielgruppe zu dieser Journey hinzu. Einmal oder nach Zeitplan ausführen."

Die **Zielgruppe lesen**-Aktivität ist die Journey-Einstiegspunktaktivität, die alle Profile aus einer ausgewählten [!DNL Adobe Experience Platform] Zielgruppe zu einer Journey hinzufügt. Sie können den Eintritt einmal oder nach einem wiederkehrenden Zeitplan ausführen. In -APIs und technischen Referenzen wird diese Aktivität auch als segmentbasierter oder zielgruppenbasierter Journey-Trigger bezeichnet.

**Verwendung von „Zielgruppe lesen“ vs. Zielgruppen-Qualifizierung**

| Verwenden Sie **Zielgruppe lesen** wenn | Verwenden **[Zielgruppen-Qualifizierung](audience-qualification-events.md)** wenn |
|----------------------------|-----------------------------------------------------------------------|
| Sie möchten eine Journey einmal oder nach einem Zeitplan (Batch) ausführen. | Sie benötigen Profile, um die Journey in Echtzeit aufrufen zu können, da sie sich qualifizieren. |
| Ihre Zielgruppe wird per Batch ausgewertet (z. B. täglicher Schnappschuss). | Ihre Zielgruppe streamt oder ereignisbasiert. |
| Sie können mit einer Verzögerung zwischen der Zielgruppenauswertung und dem Journey-Eintrag einverstanden sein. | Sie müssen sofort eintreten, wenn ein Profil qualifiziert ist. |

**Schlüsselbeschränkungen:** eine „Zielgruppe lesen“ pro Journey (muss die erste Aktivität sein); eine Zielgruppe pro Aktivität; bis zu fünf gleichzeitige „Zielgruppe lesen“-Ausführungen pro Organisation; 20.000 Profile pro Sekunde pro Sandbox; 12-Stunden-Job-Timeout. Ausführliche Informationen finden Sie unter [Leitplanken und Empfehlungen](#must-read).

**Voraussetzungen:** Eine [!DNL Adobe Experience Platform] Zielgruppe, die erstellt und ausgewertet wird (realisierter Status), ein personenbasierter Identity-Namespace, der für die Journey ausgewählt wird, und - bei wiederkehrenden Ausführungen - ein Verständnis von [Zeitplan und Durchsatzbeschränkungen](#must-read).

Beispielsweise kann die im Anwendungsfall `Luma app opening and checkout`Zielgruppen erstellen[&#x200B; erstellte &#x200B;](../audience/about-audiences.md)-Zielgruppe als Einstiegspunkt verwendet werden. Alle qualifizierten Profile treten in die Journey ein und durchlaufen personalisierte Pfade, in denen Bedingungen, Timer, Ereignisse und Aktionen verwendet werden.

➡️ [Funktion im Video kennenlernen](#video)


>[!CAUTION]
>
>* Bevor Sie mit der Verwendung der Aktivität „Zielgruppe lesen“ beginnen, [lesen Sie die Informationen zu Leitlinien und Einschränkungen](#must-read).

## Konfigurieren der Aktivität {#configuring-segment-trigger-activity}

Sie legen Folgendes fest: **Audience** (obligatorisch), **Namespace** (obligatorisch), **Leserate** (obligatorisch, Standard 5.000/s) und **Zeitplan** (wenn die Journey ausgeführt wird). Fügen Sie optional eine **Bezeichnung** und **Zusätzliche Kennung** hinzu. Die folgenden Schritte führen Sie durch die einzelnen Einstellungen.

### Aktivität hinzufügen und Zielgruppe auswählen {#add-activity-and-select-audience}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_label"
>title="Label"
>abstract="Optionaler Titel zur Identifizierung dieser Aktivität in Reporting- und Testmodusprotokollen."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_audience"
>title="Zielgruppe"
>abstract="Wählen Sie die [!DNL Adobe Experience Platform] Zielgruppe aus, deren Profile auf diese Journey zugreifen werden."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_namespace"
>title="Namespace"
>abstract="Wählen Sie aus, welche Identität (z. B. E-Mail, ECID) zur Identifizierung der Personen verwendet wird, die die Journey betreten. Wählen Sie die erste Option in der Liste aus, um die bestmögliche Kompatibilität mit Geschäftsregeln und Begrenzungen zu erzielen."

1. Erweitern Sie die Kategorie **[!UICONTROL Orchestrierung]** und legen Sie eine Aktivität vom Typ **[!UICONTROL Zielgruppe lesen]** auf Ihrer Arbeitsfläche ab.

   Die Aktivität muss als erster Schritt einer Journey positioniert werden.

1. Fügen Sie **[!UICONTROL Aktivität einen]** Titel“ hinzu (optional). Eine optionale Beschriftung hilft Ihnen, die Aktivität in Berichten und in Testmodus-Protokollen zu identifizieren.

1. Wählen Sie im Feld **[!UICONTROL Zielgruppe]** die [!DNL Adobe Experience Platform]-Zielgruppe aus, die in die Journey eintreten soll, und klicken Sie dann auf **[!UICONTROL Speichern]**. Sie können eine beliebige [!DNL Adobe Experience Platform]-Zielgruppe auswählen, die mit [Segmentdefinitionen](../audience/creating-a-segment-definition.md) generiert wurde.

   >[!NOTE]
   >
   >Darüber hinaus können Sie [!DNL Adobe Experience Platform] Zielgruppen ansprechen, die mithilfe von [Zielgruppenkompositionen](../audience/get-started-audience-orchestration.md) erstellt wurden.
   >Sie können auch Zielgruppen auswählen [aus einer CSV-Datei hochgeladen](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=de#import-audience){target="_blank"}.
   >[Weitere Informationen zum Generieren und Ansprechen von Zielgruppen in Journey Optimizer](../audience/about-audiences.md).

   Beachten Sie, dass Sie die in der Liste angezeigten Spalten anpassen und sortieren können.

   ![Benutzeroberfläche zur Zielgruppenauswahl mit verfügbaren [!DNL Adobe Experience Platform] Zielgruppen](assets/read-segment-selection.png)

   Nachdem die Zielgruppe hinzugefügt wurde, können Sie mit der Schaltfläche **[!UICONTROL Kopieren]** deren Namen und ID kopieren:

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![Schaltfläche „Kopieren“ zum Kopieren von Zielgruppenname und -ID im JSON-Format](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >Nur Personen mit dem Zielgruppenzugehörigkeitsstatus **Realisiert** können in die Journey eintreten. Weitere Informationen zum Auswerten einer Zielgruppe finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/tutorials/evaluate-a-segment#interpret-segment-results){target="_blank"}.

1. Wählen Sie im Feld **[!UICONTROL Namespace]** den Namespace aus, der zur Identifizierung der Kontakte verwendet werden soll. Standardmäßig ist das Feld mit dem zuletzt verwendeten Namespace vorausgefüllt. [Weitere Informationen über Namespaces](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Personen, die zu einer Zielgruppe ohne die ausgewählte Identität (den ausgewählten Namespace) gehören, können nicht in die Journey eintreten. Sie können nur einen personenbasierten Identity-Namespace auswählen. Wenn Sie einen Namespace für eine Suchtabelle definiert haben (z. B.: Produkt-ID-Namespace für eine Produktsuche), ist er nicht in der Dropdown-Liste **Namespace** verfügbar.

### Zusatzkennung {#read-audience-supplemental-id}

Optional können Sie **Zusätzliche Kennung verwenden** aktivieren, um die Journey zusätzlich zur Profil-ID im Kontext einer sekundären Kennung (z. B. einer Auftrags-ID oder Buchungs-ID) auszuführen. Dies ermöglicht mehrere Eintritte desselben Profils, wenn die zusätzliche Kennung unterschiedlich ist.

[Erfahren Sie, wie Sie zusätzliche Kennungen in Journey verwenden](supplemental-identifier.md). Bei Journey des Typs „Zielgruppe lesen“ muss die zusätzliche Kennung ein Profilattribut sein. Die Leserate ist auf 500 Profile pro Sekunde beschränkt, wenn eine zusätzliche ID verwendet wird.

### Leitlinien und Empfehlungen {#must-read}

* In einer Journey kann nur eine Aktivität **[!UICONTROL Zielgruppe lesen]** verwendet werden. Dies muss die erste Aktivität auf der Arbeitsfläche sein.

* Die Aktivität **[!UICONTROL Zielgruppe lesen]** kann nur eine Zielgruppe ansprechen. Wenn mehrere Zielgruppen erforderlich sind, sollten Sie diese Zielgruppen vor der Verwendung zu einer Zielgruppe zusammenführen. [Informationen zum Kombinieren von Zielgruppen mithilfe von Kompositions-Workflows](../audience/get-started-audience-orchestration.md)

* Für Journeys, die eine Aktivität vom Typ **Zielgruppe lesen** verwenden, gibt es eine maximale Anzahl von Journeys, die genau zur gleichen Zeit beginnen können. Weitere Zustellversuche werden vom System durchgeführt. Vermeiden Sie jedoch, dass mehr als fünf Journeys (mit **Zielgruppe lesen**, geplant oder „so bald wie möglich“ beginnend) genau zur selben Zeit starten. Es empfiehlt sich, sie über einen bestimmten Zeitraum zu verteilen, z. B. mit Abständen zwischen 5 und 10 Minuten.

* Erlebnisfeldgruppen können nicht in Journeys verwendet werden, die mit einer **Zielgruppe lesen**-Aktivität, einer **[Zielgruppenqualifizierung](audience-qualification-events.md)**-Aktivität oder einer Geschäftsereignis-Aktivität beginnen.

* Als Best Practice wird empfohlen, in einer Aktivität **Zielgruppe lesen** nur Batch-Zielgruppen zu verwenden. Dies ermöglicht eine zuverlässige und konsistente Zählung der in einer Journey verwendeten Zielgruppen. „Zielgruppe lesen“ wurde für Batch-Anwendungsfälle entwickelt. Wenn Ihr Anwendungsfall Echtzeitdaten benötigt, verwenden Sie bitte die Aktivität **[Zielgruppenqualifizierung](audience-qualification-events.md)**.

* Zielgruppen,[&#x200B; die aus einer CSV-Datei importiert wurden](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=de#import-audience) oder aus [Kompositions-Workflows](../audience/get-started-audience-orchestration.md) stammen, können in der Aktivität **Zielgruppe lesen** ausgewählt werden. Diese Zielgruppen sind in der Aktivität **Zielgruppen-Qualifizierung** nicht verfügbar.

* Beschränkung der gleichzeitigen Ausführung des Typs „Zielgruppe lesen“ pro Organisation: Jede Organisation kann bis zu fünf Instanzen des Typs „Zielgruppe lesen“ gleichzeitig ausführen. Dies umfasst sowohl geplante Ausführungen als auch solche, die durch Geschäftsereignisse ausgelöst werden. Das Limit gilt für alle Sandboxes und Journeys. Diese Beschränkung wird durchgesetzt, um eine faire und ausgewogene Ressourcenzuordnung zwischen allen Organisationen zu gewährleisten.

* Sandbox-Durchsatzverwaltung: Das System verwaltet den Verarbeitungsdurchsatz pro Sandbox dynamisch, mit einer maximalen Begrenzung von 20.000 Profilen pro Sekunde, die zwischen allen Aktivitäten des Typs „Zielgruppe lesen“ geteilt werden. Einzelne Aktivitäten vom Typ „Zielgruppe lesen“ können mit einer Mindestrate von 500 Profilen pro Sekunde konfiguriert werden. Wenn Durchsatz-Limits auf Sandbox-Ebene erreicht werden, können Aufträge in die Warteschlange gestellt werden, um eine faire Ressourcenzuweisung sicherzustellen.

* Timeout bei der Auftragsverarbeitung: Aufträge vom Typ „Zielgruppe lesen“, die aufgrund von Begrenzungen von Leitlinien nicht innerhalb von 12 Stunden verarbeitet werden können, werden automatisch bereinigt und nie ausgeführt. Dadurch wird eine Akkumulation von Aufträgen verhindert und die Systemstabilität gewährleistet.

* Stellen Sie bei der Verwendung von Batch-Segmenten sicher, dass Ihre Aufnahme und tägliche Snapshot-Updates lange vor dem Start der Journey abgeschlossen sind. Ziehen Sie eine zusätzliche Wartezeit in Betracht, wenn Segmente Daten widerspiegeln müssen, die am selben Tag aufgenommen wurden. Wenn die sofortige Profilaktualisierung wichtig ist, verwenden Sie einen ereignisbasierten oder Streaming-Ansatz anstelle von täglichen Batches. Alternativ können Sie einen Wartemechanismus einfügen, damit aktualisierte Daten vor der Journey-Auswertung übertragen werden können.

Leitlinien im Zusammenhang mit der Aktivität **Zielgruppe lesen** sind auf [dieser Seite](../start/guardrails.md#read-segment-g) aufgeführt.

>[!CAUTION]
>
>[Leitlinien für Echtzeit-Kundenprofildaten und Segmentierung](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=de){target="_blank"} gelten auch für [!DNL Adobe Journey Optimizer].

**Weiter** Legen Sie die [Leserate](#profile-entry-and-reading-rate) und [Zeitplan](#schedule) fest und dann [testen und veröffentlichen](#testing-publishing).

### Profileingabe und Leserate {#profile-entry-and-reading-rate}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_reading_rate"
>title="Lesegeschwindigkeit"
>abstract="Maximale Anzahl von Profilen, die pro Sekunde auf die Journey gelangen (500-20.000). Der Standardwert ist 5.000."

Legen Sie die **[!UICONTROL Ableserate]** fest (obligatorisch). Dies ist die maximale Anzahl von Profilen, die pro Sekunde in die Journey eintreten können. Diese Rate gilt nur für diese und keine andere Aktivitäten in der Journey. Wenn Sie beispielsweise eine Einschränkungsrate für benutzerdefinierte Aktionen definieren möchten, müssen Sie die Einschränkungs-API verwenden. Mehr dazu erfahren Sie auf [dieser Seite](../configuration/throttling.md).

Dieser Wert wird in der Payload der Journey-Version gespeichert. Der Standardwert ist 5.000 Profile pro Sekunde. Sie können diesen Wert zwischen 500 und 20.000 Profile pro Sekunde variieren.

>[!NOTE]
>
>Die Gesamtleserate pro Sandbox ist auf 20.000 Profile pro Sekunde festgelegt. Daher ergibt die Leserate aller gleichzeitig in derselben Sandbox ausgeführten Aktivitäten „Zielgruppe lesen“ maximal 20.000 Profile pro Sekunde. Sie können diese Begrenzung nicht ändern. Weitere Informationen zu Journey-Verarbeitungsraten und -Durchsatz finden Sie in [diesem Abschnitt](entry-management.md#journey-processing-rate).

### Planen der Journey {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_start_date"
>title="Startdatum/Uhrzeit"
>abstract="Legen Sie fest, wann diese Journey gestartet werden soll."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_until"
>title="Wiederholen bis"
>abstract="Enddatum für wiederkehrende Ausführungen definieren."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_every"
>title="Wiederholen alle"
>abstract="Wie oft die Journey läuft (z. B. täglich, wöchentlich)."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_incremental_read"
>title="Inkrementelles Lesen"
>abstract="Nach dem ersten Durchlauf geben nur neue Profile, die der Audience hinzugefügt wurden, die Journey ein."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_force_reentrance"
>title="Wiedereintritt erzwingen"
>abstract="Löschen Sie alle Teilnehmer von der Journey, bevor jede neue Zielgruppe gelesen wird."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience"
>title="Nach Auswertung der Batch-Zielgruppe auslösen"
>abstract="Führen Sie die Journey erst aus, nachdem die Batch-Zielgruppe neu ausgewertet wurde."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience_wait_time"
>title="Wartezeit für neue Zielgruppenauswertung"
>abstract="Wie lange die Journey auf neue Zielgruppendaten wartet (1-6 Stunden, in Minuten oder Stunden)."

Standardmäßig sind Journeys so konfiguriert, dass sie nur einmal ausgeführt werden. Führen Sie die nachfolgenden Schritte aus, um ein bestimmtes Datum/eine bestimmte Uhrzeit und eine bestimmte Häufigkeit für die Journey-Ausführung zu definieren.

>[!NOTE]
>
>Einmalige „Zielgruppe lesen“-Journeys wechseln 91 Tage nach der Ausführung der Journey in den Status **Beendet** ([globaler Timeout der Journey](journey-properties.md#global_timeout)).  Folgt die Aktivität „Zielgruppe lesen“ einem Zeitplan, wird sie 91 Tage nach dem letzten Auftreten beendet.

1. Wählen Sie in den Eigenschaften der Aktivität **[!UICONTROL Zielgruppe lesen]** die Option **[!UICONTROL Journey-Plan bearbeiten]** aus.

   ![Schaltfläche zum Bearbeiten des Journey-Zeitplans in den Eigenschaften der Aktivität „Zielgruppe lesen“](assets/read-segment-schedule.png)

1. Die Eigenschaften der Journey werden angezeigt. Wählen Sie in der Dropdown-Liste **[!UICONTROL Planungstyp]** die Häufigkeit aus, mit der die Journey ausgeführt werden soll.

   ![Dropdown-Liste „Planungstyp“ mit Häufigkeitsoptionen: einmal, täglich, wöchentlich, monatlich](assets/read-segment-schedule-list.png)

>[!TIP]
>
>Um ausgehende Nachrichten in Batches über einen bestimmten Zeitraum statt alle gleichzeitig zu versenden, können Sie den Wellenversand im Journey-Zeitplan konfigurieren. [Erfahren Sie, wie Sie mithilfe von Schüben in Journey senden](send-using-waves.md)

Für wiederkehrende Journeys stehen spezifische Optionen zur Verfügung, mit denen Sie den Eintritt der Profile in die Journey verwalten können. Erweitern Sie die folgenden Abschnitte, um weitere Informationen zu den einzelnen Optionen zu erhalten.

![Wiederholungsoptionen für „Zielgruppe lesen“: Inkrementelles Lesen, erzwungener Wiedereintritt, nach Batch auslösen](assets/read-audience-options.png)

+++**[!UICONTROL Inkrementelles Lesen]**

Wenn eine Journey mit einer wiederkehrenden Aktivität **Zielgruppe lesen** zum ersten Mal ausgeführt wird, treten alle Profile in der Zielgruppe in die Journey ein. Mit dieser Option haben Sie die Möglichkeit, nach dem ersten Auftreten nur die Personen anzusprechen, die seit der letzten Journey-Ausführung in die Zielgruppe eingetreten sind.

Bei Verwendung dieser Option blickt das System **24 Stunden** vom Zeitpunkt des letzten Zielgruppenauswertungsauftrags zurück, der vom Segmentierungs-Service von [!DNL Adobe Experience Platform] ausgeführt wurde.

Nach Abschluss der Segmentierung beginnt ein Exportauftrag für Profil-Snapshots, mit dem Journey Optimizer neue Profile erkennen und verarbeiten kann. Wenn die Journey zwischen diesen beiden Aufträgen geplant ist, werden beim inkrementellen Lesen keine Profile erfasst, die seit der letzten Ausführung der Journey Mitglieder der Zielgruppe wurden.

So minimieren Sie das Risiko fehlender Profile:
* Aktivieren Sie die Option **[!UICONTROL Nach Batch-Zielgruppenauswertung auslösen]**, um den Lookback-Zeitraum auf den Zeitpunkt der letzten erfolgreichen Journey-Ausführung zu verlängern, unabhängig davon, wie lange er zurückliegt
* Planen Sie die Ausführung der Journey nach Abschluss der täglichen Batch-Segmentierungsaufträge (in der Regel 2–3 Std. Puffer)
* Bei zeitkritischen Anwendungsfällen, die eine sofortige Profileinbindung erfordern, sollten Sie stattdessen Aktivitäten zur [Zielgruppen-Qualifizierung](audience-qualification-events.md) mit Streaming-Zielgruppen verwenden

>[!CAUTION]
>
>Wenn Sie eine [benutzerdefinierte Upload-Zielgruppe](../audience/about-audiences.md#about-segments) auf Ihrem Journey ansprechen, werden Profile nur bei der ersten Wiederholung abgerufen, wenn diese Option auf einer wiederkehrenden Journey aktiviert ist. Diese Zielgruppen sind unveränderlich.

+++

+++**[!UICONTROL Bei wiederholter Ausführung erneuten Eintritt erzwingen]**

Mit dieser Option können Sie alle noch in der Journey vorhandenen Profile bei der nächsten Ausführung automatisch austreten lassen. 

Wenn Sie beispielsweise eine Wartezeit von 2 Tagen auf einer täglich wiederkehrenden Journey haben, werden Profile bei Aktivierung dieser Option zur nächsten Journey-Ausführung verschoben. Dies geschieht am darauffolgenden Tag, unabhängig davon, ob sie sich in der Zielgruppe der nächsten Ausführung befinden oder nicht.

Wenn die Lebensdauer Ihrer Profile in dieser Journey länger als die Häufigkeit der Intervalle sein kann, aktivieren Sie diese Option nicht. So stellen Sie sicher, dass die Profile ihre Journey abschließen können.

+++

+++**[!UICONTROL Nach Batch-Zielgruppenauswertung auslösen]**

Für täglich geplante Journeys und zum Targeting von Batch-Zielgruppen können Sie ein Zeitfenster von bis zu 6 Stunden definieren, damit die Journey auf neue Zielgruppendaten aus Batch-Segmentierungsaufträgen wartet. Wenn der Segmentierungsauftrag innerhalb des Zeitfensters abgeschlossen wird, wird die Journey ausgelöst. Andernfalls wird die Journey bis zum nächsten Auftreten übersprungen. Diese Option stellt sicher, dass Journeys mit genauen und aktuellen Zielgruppendaten ausgeführt werden.

Wenn beispielsweise eine Journey für täglich 18 Uhr geplant ist, können Sie angeben, wie viele Minuten oder Stunden gewartet werden soll, bevor die Journey ausgeführt wird. Wenn die Journey um 18 Uhr aktiv wird, sucht sie nach einer neuen Zielgruppe, d. h. nach einer Zielgruppe, die neuer ist als die aus der vorherigen Journey-Ausführung. Während des angegebenen Zeitfensters wird die Journey ausgeführt, sobald die neue Zielgruppe erkannt wird. Wenn keine neue Zielgruppe erkannt wird, wird die Journey-Ausführung für diesen Tag übersprungen.

+++

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

## Testen und Veröffentlichen der Journey {#testing-publishing}

Mit der Aktivität **[!UICONTROL Zielgruppe lesen]** können Sie die Journey anhand eines einheitlichen Profils testen.

Dazu muss der Testmodus aktiviert werden.

![Benutzeroberfläche des Testmodus für die Aktivität „Zielgruppe lesen“ mit Testprofilauswahl](assets/read-segment-test-mode.png)

Konfigurieren Sie den Testmodus und führen Sie ihn wie gewohnt aus. [Erfahren Sie, wie Sie eine Journey testen](testing-the-journey.md).

Sobald der Test ausgeführt wird, können mit der Schaltfläche **[!UICONTROL Protokolle anzeigen]** die Testergebnisse angezeigt werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](testing-the-journey.md#viewing_logs)

![Testprotokolle mit Ergebnissen der Zielgruppenausführung und dem Profilfluss](assets/read-segment-log.png)

Nach erfolgreichem Abschluss der Tests können Sie Ihre Journey veröffentlichen (siehe [Veröffentlichen der Journey](../building-journeys/publish-journey.md)). Personen, die zur Zielgruppe gehören, treten zu dem Datum und der Uhrzeit in die Journey ein, die im Abschnitt **[!UICONTROL Planung]** der Journey-Eigenschaften festgelegt sind.

>[!NOTE]
>
>Bei zielgruppenbasierten wiederkehrenden Journeys wird die Journey automatisch nach dem letzten Auftreten geschlossen. Wenn kein Enddatum/-zeitpunkt angegeben wurde, müssen Sie die Journey manuell für neue Eintritte schließen, um sie zu beenden.

## Zielgruppen-Targeting in Journey

Zielgruppenbasierte Journey beginnen immer mit der Aktivität **Zielgruppe lesen** um Personen abzurufen, die zu einer [!DNL Adobe Experience Platform] Zielgruppe gehören. Diese Profile werden einmal oder in einem wiederkehrenden Zeitplan gelesen.

Nach dem Eintritt in die Journey orchestrieren Sie sie mithilfe **Bedingung** Aktivitäten: Nach Attributen oder Verhalten segmentieren, einen Teil der Population ausschließen oder Zweige wieder zusammenführen (Vereinigung). In den folgenden Abschnitten werden die einzelnen Muster beschrieben.

**Segmentierung**

Mithilfe der Aktivität **Bedingung** können Sie eine Segmentierung anhand von Bedingungen durchführen. Sie können beispielsweise VIP-Personen auf einen bestimmten Pfad führen und alle übrigen Personen auf einen anderen Pfad.

Die Segmentierung kann basieren auf:

* Daten aus Datenquellen
* Kontext von Ereignissen, die Teil der Journey-Daten sind – Beispiel: Hat eine Person auf die Nachricht geklickt, die sie vor einer Stunde erhalten hat?
* Datum – Beispiel: Ist es Juni, wenn eine Person durch die Journey navigiert?
* Tageszeit – Beispiel: Ist es in der Zeitzone der Person morgens?
* Algorithmus, der die in die Journey geführte Zielgruppe auf der Basis eines Prozentsatzes aufteilt – Beispiel: 90 %–10 % für den Ausschluss einer Kontrollgruppe

![Bedingungsaktivität zur Zielgruppensegmentierung in Pfade für VIP- und Nicht-VIP-Profile](assets/read-segment-audience1.png)

>[!NOTE]
>
>Bei Verwendung des Planungstyps „Täglich“ mit der Aktivität **[!UICONTROL Zielgruppe lesen]** können Sie ein Zeitfenster definieren, in dem die Journey auf neue Zielgruppendaten warten soll. Dadurch wird eine präzise Zielgruppenbestimmung sichergestellt. Außerdem werden Probleme durch Verzögerungen bei Batch-Segmentierungsaufträgen vermieden. [Informationen zum Planen einer Journey](#schedule)

**Ausschluss**

Die selbe Aktivität **Bedingung**, die für die Segmentierung verwendet wird (siehe oben), ermöglicht es Ihnen auch, einen Teil der Population auszuschließen. Sie können beispielsweise VIP-Personen ausschließen, indem Sie diese in einen Zweig mit direkt anschließendem Beenden-Schritt führen.

Dieser Ausschluss kann unmittelbar nach Zielgruppenabruf, zu Zwecken der Populationszählung oder als Teil einer mehrstufigen Journey erfolgen.

![Journey-Pfad mit Ausschlussverzweigung mit der Aktivität „Ende“](assets/read-segment-audience2.png)

**Vereinigung**

Journeys erlauben das Erstellen von N Verzweigungen, die nach einer Segmentierung zusammengeführt werden. Daher können Sie zwei Zielgruppen zu einem gemeinsamen Erlebnis zurückkehren lassen.

Ein Beispiel: Im Anschluss an ein zehntägiges differenziertes Erlebnis in einer Journey können Kundinnen und Kunden mit und ohne VIP-Status zum selben Pfad zurückkehren. Nach einer Vereinigung können Sie die Zielgruppe erneut teilen, indem Sie eine Segmentierung oder einen Ausschluss durchführen.

![Journey-Pfade werden nach der Segmentierung durch Vereinigung wieder zusammengeführt](assets/read-segment-audience3.png)

## Fehlerbehebung {#audience-count-mismatch}

In diesem Abschnitt erfahren Sie, wie Sie **Zielgruppengröße-Inkongruenzen** (weniger oder mehr Profile eintreten als erwartet), **keine Profile verarbeitet** (Zielgruppen-Warnhinweis lesen oder keine Einträge) und **verzögerte oder fehlende Einträge** (Timing und Datenübertragung) beheben können.

>[!NOTE]
>
>Wenn die Aktivität „Zielgruppe lesen“ ausgeführt wird, generiert das System interne Ereignisse (sogenannte `segmentExportJob`-Ereignisse), um den Lebenszyklus des Vorgangs des Zielgruppenexports zu verfolgen. Diese Ereignisse werden auf Aktivitätsebene und nicht pro einzelnem Profil aufgezeichnet und können zu Monitoring- und Fehlerbehebungszwecken abgefragt werden. Erfahren Sie mehr über das [Abfragen von Ereignissen des Typs „Zielgruppe lesen“](../reports/query-examples.md#read-segment-queries).

**Problem suchen:**

| Symptom | Gehe zu |
|---------|--------|
| Weniger (oder mehr) Profile als die Zielgruppengröße eingegeben | [Timing und Datenweitergabe](#timing-and-data-propagation), [Datenvalidierung und -überwachung](#data-validation-and-monitoring) |
| Zielgruppe lesen hat null Profile verarbeitet; Warnhinweis ausgelöst | [Keine Profile verarbeitet](#zero-profiles-processed) |
| Einträge für Batch-Zielgruppen verzögert oder fehlen | [Timing und Datenweitergabe](#timing-and-data-propagation) |
| Segmentauftragsstatus oder Namespace müssen überprüft werden | [Datenvalidierung und -überwachung](#data-validation-and-monitoring) |

### Keine Profile verarbeitet {#zero-profiles-processed}

Wenn die Aktivität **Zielgruppe lesen** kein Profil verarbeitet hat (z. B. wird die Warnung [Zielgruppe lesen](../reports/alerts.md#alert-read-audiences) angezeigt):

1. **Überprüfen, ob die Zielgruppe leer ist** - Überprüfen Sie in [!DNL Adobe Experience Platform] die Zielgruppengröße und, ob sich Profile im Status **Realisiert** befinden. Eine leere oder noch nicht ausgewertete Zielgruppe führt zu null Einträgen.
2. **Namespace überprüfen** - Der in der Aktivität „Zielgruppe lesen“ ausgewählte Namespace muss in den Profilen in Ihrer Zielgruppe vorhanden sein. Profile ohne diese Identität können nicht auf die Journey zugreifen. [Weitere Informationen über Namespaces](../event/about-creating.md#select-the-namespace).
3. **Warnungen und erneute Versuche überprüfen** - Fehler werden in &quot;**&quot;**. Das System versucht, die Erstellung von Exportvorgängen alle 10 Minuten für bis zu 1 Stunde erneut auszuführen. [Erfahren Sie mehr über weitere Zustellversuche und Warnhinweise](#read-audience-retry).

Wenn das Problem nach diesen Prüfungen weiterhin besteht, finden Sie unter [Timing und Datenweitergabe](#timing-and-data-propagation) und [Datenvalidierung und -überwachung](#data-validation-and-monitoring) Informationen zu Ursachen für Batch- und Konfigurationen.

### Timing und Datenpropagierung {#timing-and-data-propagation}

* **Abschluss des Batch-Segmentierungsauftrags**: Stellen Sie für Batch-Zielgruppen sicher, dass der tägliche Batch-Segmentierungsauftrag abgeschlossen ist und Momentaufnahmen aktualisiert werden, bevor die Journey ausgeführt wird. Batch-Zielgruppen sind etwa **2 Stunden** nach Abschluss des Segmentierungsauftrags einsatzbereit. Weitere Informationen zu [Methoden zur Zielgruppenauswertung](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de#evaluate-segments){target="_blank"}.

* **Zeitpunkt der Datenaufnahme**: Stellen Sie sicher, dass die Profildatenaufnahme vor der Journey-Ausführung vollständig abgeschlossen wurde. Wenn Profile kurz vor dem Start der Journey aufgenommen wurden, werden sie möglicherweise noch nicht in der Zielgruppe angezeigt. Weitere Informationen zu [Datenaufnahme in [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=de){target="_blank"}.

* **Option „Nach Batch-Zielgruppenauswertung auslösen“ verwenden**: Bei täglich geplanten Journeys, die Batch-Zielgruppen verwenden, sollten Sie die Option **[!UICONTROL Nach Batch-Zielgruppenauswertung auslösen]** aktivieren. Dadurch wird sichergestellt, dass die Journey vor der Ausführung auf neue Zielgruppendaten wartet (bis zu 6 Stunden). [Weitere Informationen zur Planung](#schedule)

* **Warteaktivität hinzufügen**: Für Streaming-Zielgruppen mit kürzlich aufgenommenen Daten sollten Sie am Anfang der Journey eine Aktivität des Typs **Warten** hinzufügen, um Zeit für die Datenpropagierung und Profilqualifizierung zu gewähren. [Weitere Informationen zur Aktivität „Warten“](wait-activity.md)

### Datenvalidierung {#data-validation-and-monitoring}

* **Status des Segmentierungsauftrags überprüfen** Überwachen der Abschlusszeiten von Batch-Segmentierungsaufträgen im [!DNL Adobe Experience Platform]Überwachungs[Dashboard](https://experienceleague.adobe.com/docs/experience-platform/dataflows/ui/monitor-segments.html?lang=de){target="_blank"}. Verwenden Sie sie, um zu überprüfen, wann Zielgruppendaten bereit sind.

* **Zusammenführungsrichtlinien prüfen**: Stellen Sie sicher, dass die für Ihre Zielgruppe konfigurierte Zusammenführungsrichtlinie dem erwarteten Verhalten für die Kombination von Profildaten aus verschiedenen Quellen entspricht. Weitere Informationen zu [Zusammenführungsrichtlinien in [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/overview.html?lang=de){target="_blank"}.

* **Segmentdefinitionen prüfen**: Prüfen Sie, ob Segmentdefinitionen korrekt konfiguriert sind, und schließen Sie alle erwarteten Qualifikationskriterien ein. Weitere Informationen zum [Erstellen von Zielgruppen](../audience/creating-a-segment-definition.md). Achten Sie besonders auf Folgendes:
   * Zeitbasierte Bedingungen, die Profile basierend auf Ereignis-Zeitstempeln ausschließen können
   * Attributqualifikationen, die von kürzlich aktualisierten Daten abhängen
   * Streaming- vs. Batch-Auswertungsmethoden

* **Namespace-Konfiguration validieren**: Stellen Sie sicher, dass der in der Aktivität **Zielgruppe lesen** ausgewählte Namespace mit der primären Identität übereinstimmt, die von Profilen in Ihrer Zielgruppe verwendet wird. Profile ohne den ausgewählten Namespace treten nicht in die Journey ein. Erfahren Sie mehr über [Identity-Namespaces](../event/about-creating.md#select-the-namespace).

### Best Practices

* **Journeys nach der Segmentierung planen**: Planen Sie die Journey-Ausführung für Batch-Zielgruppen für frühestens 2–3 Stunden nach der typischen Abschlusszeit des Batch-Segmentierungsauftrags. [Weitere Informationen zur Journey-Planung](#schedule)

* **Streaming-Zielgruppen für Echtzeit-Anwendungsfälle verwenden**: Wenn Profilqualifizierung und Journey-Eintritt sofort erfolgen sollen, verwenden Sie Aktivitäten des Typs [Zielgruppen-Qualifizierung](audience-qualification-events.md) mit Streaming-Zielgruppen anstelle des Typs **Zielgruppe lesen** mit Batch-Zielgruppen.

* **Zuerst mit kleineren Zielgruppen testen**: Bevor Sie große Journeys starten, testen Sie sie mit einer kleineren Teilmenge, um zu prüfen, ob die Anzahl der Profile den Erwartungen entspricht. [Weitere Informationen zum Testen einer Journey](testing-the-journey.md)

* **Regelmäßig überwachen**: Richten Sie eine regelmäßige Überwachung der Zielgruppengrößen und Journey-Eintrittsmetriken ein, um Diskrepanzen frühzeitig zu erkennen. Weitere Informationen zu [Journey-Verarbeitungsraten und zur Eintrittsverwaltung](entry-management.md).

### Kontaktaufnahme mit dem Support

Wenn nach den oben genannten Schritten weiterhin Inkongruenzen bei der Zählung oder Nullprofilausführungen auftreten, wenden Sie sich an den Adobe-Support. Halten Sie bereit: Zielgruppenname/ID, Journey-Name/ID, geplante Laufzeit(en), Sandbox und eine kurze Beschreibung der Diskrepanz (z. B. „Zielgruppe zeigt 10K realisiert an, nur 2K ist am [Datum] auf die Journey gelangt).

## Weitere Zustellversuche {#read-audience-retry}

Beim Abrufen des Exportauftrags werden standardmäßig weitere Versuche bei zielgruppenseitig ausgelösten Journeys durchgeführt (beginnend mit der Aktivität **Zielgruppe lesen** oder einem **Geschäftsereignis**). Tritt bei der Erstellung des Exportauftrags ein Fehler auf, werden alle 10 Minuten, aber höchstens eine Stunde lang, weitere Versuche unternommen. Danach wird von einem Fehler ausgegangen. Diese Journey-Typen können daher bis zu einer Stunde nach der geplanten Zeit ausgeführt werden.

Erfolglose **Zielgruppe lesen**-Trigger werden erfasst und in **Warnhinweisen** angezeigt. Der Warnhinweis **Zielgruppe lesen** warnt Sie, wenn eine Aktivität **Zielgruppe lesen** 10 Minuten nach der geplanten Ausführungszeit kein Profil verarbeitet hat. Dieser Fehler kann durch technische Probleme oder eine leere Zielgruppe verursacht werden. Wenn der Fehler auf technische Probleme zurückzuführen ist, können je nach Problemtyp weiterhin weitere Zustellversuche unternommen werden. Wenn die Erstellung des Exportvorgangs beispielsweise fehlschlägt, versuchen wir alle 10 Minuten bis zu 1 Stunde erneut. [Weitere Informationen](../reports/alerts.md#alert-read-audiences)

## Verwandte Themen

* [Erstellen von Zielgruppen](../audience/about-audiences.md)
* [Aktivität des Typs „Zielgruppenqualifizierung“](audience-qualification-events.md)
* [Verwenden zusätzlicher Kennungen in Journeys](supplemental-identifier.md)
* [Journey-Eigenschaften und -Leitlinien](../start/guardrails.md#read-segment-g)
* [Journey-Verarbeitungsraten und Eingabemanagement](entry-management.md)
* [Testen einer Journey](testing-the-journey.md)
* [Veröffentlichen einer Journey](../building-journeys/publish-journey.md)

## Anleitungsvideo {#video}

Machen Sie sich mit den relevanten Anwendungsfällen für eine Journey vertraut, die durch die Aktivität „Zielgruppe lesen“ ausgelöst wird. Erfahren Sie, wie Sie Batch-basierte Journeys erstellen und welche Best Practices anzuwenden sind.

>[!VIDEO](https://video.tv.adobe.com/v/3424997?quality=12)
