---
solution: Journey Optimizer
product: journey optimizer
title: Entwerfen einer Journey
description: Erfahren Sie, wie Sie Ihre Journey entwerfen
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Design, Arbeitsfläche, Journey, Benutzeroberfläche, ziehen, ablegen
exl-id: 1998f6fc-60fd-4038-8669-39cd55bc02d1
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Mn8oR-jsUTbkXoohAgCulA-SBY8xRVy75z6H7j9ETvE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
  - id: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 300b4c714f797971749706e0269f61174d1fe91e
workflow-type: tm+mt
source-wordcount: 2469
ht-degree: 66%

---

# Entwerfen einer Journey {#design-your-journey}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mit der Arbeitsfläche und Palette des Journey-Designers Ereignisse, Orchestrierungs- und Aktionsaktivitäten per Drag-and-Drop in einen sequenziellen Fluss ziehen können, aus dem Ihr Journey besteht.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] enthält eine Arbeitsfläche für die Omni-Channel-Orchestrierung, mit der Marketing-Experten Marketing-Maßnahmen mit Eins-zu-eins-Kundeninteraktionen aufeinander abstimmen können. Die Benutzeroberfläche ermöglicht es, Aktivitäten einfach von der Palette in die Arbeitsfläche zu ziehen, um eine Journey zu erstellen. Sie können auch auf eine Aktivität doppelklicken, um sie im nächsten verfügbaren Schritt der Arbeitsfläche hinzuzufügen.

Ereignisse, Orchestrierungs- und Aktionsaktivitäten haben eine bestimmte Rolle und einen bestimmten Platz im Prozess. Die Aktivitäten finden der Reihe nach statt: Nach Beendigung einer Aktivität wird der Fluss fortgesetzt und die nächste Aktivität wird verarbeitet usw.

## Erste Schritte beim Entwerfen von Journeys {#gs-journey-design}

Die **Palette** befindet sich auf der linken Bildschirmseite. Alle verfügbaren Aktivitäten sind in verschiedene Kategorien unterteilt: [Ereignisse](#jo-event), [Orchestrierung](#jo-orch) und [Aktionen](#jo-actions). Sie können die verschiedenen Kategorien erweitern/reduzieren, indem Sie auf ihren Namen klicken. Um eine Aktivität in Ihrer Journey zu verwenden, ziehen Sie sie per Drag-and-Drop aus der Palette in Ihre Arbeitsfläche.

Beim Erstellen einer neuen Journey werden Elemente ausgeblendet, die nicht als erster Schritt auf der Arbeitsfläche abgelegt werden können. Dies betrifft alle Aktionen, die Bedingungsaktivität, die Wartezeit und die Reaktion.

![Benutzeroberfläche des Journey-Designers mit Palette, Arbeitsfläche und Eigenschaftenbereich](assets/journey38.png)

Mit dem Symbol **[!UICONTROL Elemente filtern]** oben links können Sie die folgenden Filter anzeigen:

* **Nur verfügbare Elemente anzeigen**: Blenden Sie nicht verfügbare Elemente in der Palette ein oder aus, z. B. die Ereignisse, die einen anderen Namespace verwenden als die in der Journey verwendeten. Standardmäßig werden nicht verfügbare Elemente ausgeblendet. Wenn Sie sie anzeigen lassen, werden sie grau dargestellt.

* **Nur aktuelle Elemente anzeigen**: Mit diesem Filter können Sie neben den nativen auch die letzten fünf Ereignisse und Aktionen anzeigen. Dies ist benutzerspezifisch. Standardmäßig werden alle Elemente angezeigt.

Sie können auch das Feld **[!UICONTROL Suche]** verwenden. Es werden nur Ereignisse und Aktionen gefiltert.

Die **Arbeitsfläche** ist der zentrale Bereich im Journey-Designer. In diesem Bereich können Sie Ihre Aktivitäten ablegen und konfigurieren. Klicken Sie auf eine Aktivität auf der Arbeitsfläche, um sie zu konfigurieren. Dadurch wird der Konfigurationsbereich für die Aktivität auf der rechten Seite geöffnet.

![Journey-Arbeitsfläche mit geöffnetem Konfigurationsbereich für Aktivitäten auf der rechten Seite](assets/journey39.png)

Die **Symbolleiste** oben rechts auf der Arbeitsfläche ermöglicht es Ihnen, das Raster ein- und auszublenden, ein- und auszuzoomen und einen Screenshot der Arbeitsfläche herunterzuladen. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/journey-properties.md#timeout_and_error).

<!--and show/hide timeout and error paths-->

![Journey-Symbolleiste mit Steuerelementen für Zoomen, Raster und Screenshots](assets/toolbar.png){width="70%"}

Der **Konfigurationsbereich für die Aktivität** wird angezeigt, wenn Sie auf eine Aktivität in der Palette klicken. Füllen Sie die erforderlichen Felder aus. Klicken Sie auf das Symbol **[!UICONTROL Löschen]**, um die Aktivität zu löschen. Klicken Sie auf **[!UICONTROL Abbrechen]**, um die Änderungen zu ignorieren, oder auf **[!UICONTROL OK]**, um sie zu bestätigen. Um Aktivitäten zu löschen, können Sie auch eine Aktivität (oder mehrere) auswählen und die Rücktaste drücken. Durch Drücken der Esc-Taste wird der Konfigurationsbereich für die Aktivität geschlossen.

Standardmäßig sind schreibgeschützte Felder ausgeblendet. Um sie anzuzeigen, klicken Sie auf das Symbol **Schreibgeschützte Felder anzeigen** oben links im Konfigurationsbereich für die Aktivitäten. Diese Einstellung gilt für alle Aktivitäten in allen Journeys.

![Konfigurationsbereich für Aktivitäten mit der Option „Schreibgeschützte Felder anzeigen“](assets/journey59bis.png)

Abhängig vom Status der Journey können Sie mithilfe der verfügbaren Schaltflächen oben rechts verschiedene Aktionen für Ihre Journey ausführen: **[!UICONTROL Veröffentlichen]**, **[!UICONTROL Duplizieren]**, **[!UICONTROL Löschen]**, **[!UICONTROL Testmethode]**, **[!UICONTROL Zugriff verwalten]**, **[!UICONTROL Warnhinweise]**. Diese Schaltflächen werden angezeigt, wenn keine Aktivität ausgewählt ist. Einige Schaltflächen werden kontextuell angezeigt. Die Schaltfläche für das Testmodusprotokoll wird angezeigt, wenn der Testmodus aktiviert ist.

![Schaltflächen für Journey-Aktionen: „Veröffentlichen“, „Duplizieren“, „Löschen“, „Testmodus“, „Zugriff verwalten“, „Warnhinweise“](assets/journey41.png)

## Neue Journey-Benutzeroberfläche {#canvas-capabilities}

Eine **neue Benutzeroberfläche** ist für die Journey-Arbeitsfläche verfügbar, die speziell für Ihre komplexesten Anwendungsfälle entwickelt wurde:

* **Performance** - Verarbeitet große Journey mit vielen Schritten und Verzweigungen effizient.
* **Automatisches Layout** - Organisiert automatisch Aktivitäten, um die Lesbarkeit zu verbessern.
* **Geführtes Authoring** - Bietet ein strukturiertes Authoring-Erlebnis, mit dem Sie mühelos und effizient Journey erstellen können.

![](assets/journey-new-canvas.png)

Um zum neuen Erlebnis zu wechseln, klicken Sie auf die Schaltfläche **[!UICONTROL Neues Erlebnis]** auf der Journey-Arbeitsfläche. Nach dem Wechsel wird diese Einstellung auf Journey-Ebene gespeichert, sodass die Journey bei nachfolgenden Besuchen standardmäßig in der neuen -Version geöffnet wird. Klicken Sie auf die Schaltfläche **[!UICONTROL Altes Erlebnis]**, um es wiederherzustellen.

![](assets/journey-new-experience-switch.png){width="50%" align="center" zoomable="yes"}


## Starten der Journey {#start-your-journey}

Wenn Sie Ihre Journey entwerfen, stellen Sie sich als Erstes die Frage, wie Profile in die Journey eintreten werden.

Es gibt zwei Möglichkeiten:

1. **Beginn mit einem Ereignis**: Wenn eine Journey so eingestellt ist, dass sie auf Ereignisse wartet, treten Personen **einheitlich** in Echtzeit in die Journey ein. Nachrichten, die in Ihrer Journey enthalten sind, werden an die Person gesendet, die gerade in die Journey kommt. [Weitere Informationen zu Ereignissen](../event/about-events.md)

1. **Mit „Zielgruppe lesen** beginnen: Sie können Ihren Journey so einstellen, dass er auf [!DNL Adobe Experience Platform] Zielgruppen wartet. In diesem Fall treten alle der angegebenen Zielgruppe angehörenden Personen in die Journey ein. Die in Ihrer Journey enthaltenen Nachrichten werden an die der Zielgruppe angehörenden Personen gesendet. Weitere Informationen zur Aktivität [Zielgruppe lesen](read-audience.md). Weitere Informationen zum Generieren und Ansprechen von Zielgruppen in Journey Optimizer finden Sie [in diesem Abschnitt](../audience/about-audiences.md).

## Definieren der nächsten Schritte{#define-next-steps}

Nach dem ersten Ereignis oder „Zielgruppe lesen“ können Sie die verschiedenen Aktivitäten kombinieren, um mehrstufige Cross-Channel-Szenarien zu erstellen. Wählen Sie in der Palette die gewünschten Schritte aus.

### Ereignisse{#jo-event}

Ereignisse sind Auslöser personalisierter Journeys, z. B. eines Online-Kaufs. Wenn eine Person in eine Journey eintritt, durchläuft sie sie als Individuum. Jede Person bewegt sich in einer anderen Geschwindigkeit und auf einem anderen Pfad.

Wenn Sie Ihre Journey mit einem Ereignis beginnen, wird die Journey ausgelöst, sobald das Ereignis eintritt. Jede Person in der Journey folgt dann einzeln den nächsten Schritten, die in Ihrer Journey definiert sind.

Sie können **mehrere Ereignisse** in Ihrer Journey hinzufügen, sofern sie denselben Namespace verwenden. Die Ereignisse werden zuvor konfiguriert. [Weitere Informationen zu Journey-Ereignissen](about-journey-activities.md#event-activities)

Sie können nach einer Nachricht auch ein **Reaktions**-Ereignis hinzufügen, um auf Tracking-Daten im Zusammenhang mit der Nachricht zu reagieren. So können Sie z. B. eine weitere Nachricht senden, wenn der Kontakt die vorherige Nachricht geöffnet oder in ihr auf etwas geklickt hat. [Weitere Informationen zu Reaktionsereignissen](reaction-events.md).

Verwenden Sie **Ereignisaktivität** Zielgruppen-Qualifizierung), um Personen auf der Grundlage [!DNL Adobe Experience Platform] Zielgruppen-Ein- und -Ausstiege zu veranlassen, in eine Journey einzutreten oder in einer CD fortzufahren. Sie können alle neuen Silber-Kunden dazu bringen, in eine Journey einzutreten und ihnen personalisierte Nachrichten senden. Weiterführende Informationen finden Sie in diesem [Abschnitt](audience-qualification-events.md).

### Orchestrierung{#jo-orch}

Orchestrierungsaktivitäten sind Bedingungen, die beim Bestimmen des nächsten Schritts der Journey helfen.

In den Orchestrierungsaktivitäten können Sie die Aktivität **Zielgruppe lesen** verwenden, um Ihren Journey so einzustellen, dass er auf eine [!DNL Adobe Experience Platform] Zielgruppe wartet. [Erfahren Sie mehr zur Aktivität „Zielgruppe lesen“](read-audience.md).

Verwenden Sie **Journey-Fragmente** um wiederverwendbare Sätze vordefinierter Journey-Knoten direkt in die Arbeitsfläche einzufügen. Fragmente helfen Teams dabei, konsistent zu bleiben und schneller zu arbeiten, indem sie die Neuerstellung derselben Logik vermeiden - z. B. Eignungsprüfungen, Kanalrouting oder Begrüßungssequenzen - von Grund auf vermeiden. [Weitere Informationen zum Journey von Fragmenten](journey-fragments.md).

Die anderen Aktivitäten ermöglichen es Ihnen, Bedingungen zu Ihrer Journey hinzuzufügen, um mehrere Pfade zu definieren, eine Wartezeit festzulegen, bevor Sie die nächste Aktivität ausführen, oder Ihre Journey zu beenden. [Weitere Informationen zu Orchestrierungsaktivitäten](about-journey-activities.md#orchestration-activities).

### Aktionen{#jo-actions}

Aktionen sind das Ergebnis eines Auslösers, wie das Senden einer Nachricht. Sie sind die Teile der Journey, die der Kunde bzw. die Kundin wahrnimmt. Dabei kann es sich um eine E-Mail-, SMS- oder Push-Nachricht oder um eine Drittanbieteraktion handeln, z. B. um eine Slack-Nachricht.

Mit den Kanalaktionsaktivitäten können Sie eine Nachricht einfügen, die in [!DNL Journey Optimizer] entworfen wurde. [Weitere Informationen zu Kanalaktionsaktivitäten](journey-action.md)

Verwenden Sie in den Aktionsaktivitäten benutzerdefinierte Aktionen, um Nachrichten mit Drittanbietersystemen zu senden. [Weitere Informationen zu benutzerdefinierten Aktionen](about-journey-activities.md#action-activities).

## Hinzufügen alternativer Pfade {#paths}

Für den Fall eines Fehlers oder einer Zeitüberschreitung können Sie eine Ausweichaktion für die folgenden Journey-Aktivitäten definieren: **[!UICONTROL Bedingung]** und **[!UICONTROL Aktion]**.

Um eine Ausweichaktion für eine Aktivität hinzuzufügen, wählen Sie das Feld **[!UICONTROL Alternativen Pfad im Fall einer Zeitüberschreitung oder eines Fehlers hinzufügen]** in den Eigenschaften der Aktivität aus. Nach der Aktivität wird dadurch ein weiterer Pfad hinzugefügt. Die Zeitüberschreitungsdauer wird von Admin-Benutzern in den [Journey-Eigenschaften](../building-journeys/journey-properties.md) festgelegt. Wenn beispielsweise der Versand einer E-Mail zu lange dauert oder ein Fehler dabei auftritt, können Sie sich für den Versand einer Push-Benachrichtigung entscheiden.

![Option „Alternativen Pfad hinzufügen, falls eine Zeitüberschreitung oder ein Fehler auftritt“](assets/journey42.png)

Verschiedene Aktivitäten (Ereignis, Aktion, Warten) ermöglichen es Ihnen, nach der Aktivität mehrere Pfade hinzuzufügen. Setzen Sie dazu den Cursor auf die Aktivität und klicken Sie auf das „+“-Symbol. Nur Ereignis- und Warteaktivitäten können parallel festgelegt werden. Wenn mehrere Ereignisse parallel festgelegt werden, wird der Pfad des Ereignisses ausgewählt, das zuerst stattfindet.

Wir empfehlen, beim Überwachen eines Ereignisses nicht auf unbestimmte Zeit auf das Ereignis zu warten. Dies ist nicht obligatorisch, sondern nur eine Best Practice. Wenn Sie ein oder mehrere Ereignisse nur während einer bestimmten Zeit überwachen möchten, platzieren Sie ein oder mehrere Ereignisse und eine Warteaktivität parallel. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/general-events.md#events-specific-time).

Um den Pfad zu löschen, platzieren Sie den Cursor darauf und klicken Sie auf das Symbol **[!UICONTROL Pfad löschen]**.

![Symbol „Pfad löschen“ zum Entfernen eines alternativen Pfads](assets/journey42ter.png)

Wenn zwei Aktivitäten auf der Arbeitsfläche getrennt werden, wird eine Warnung angezeigt. Platzieren Sie den Cursor auf das Warnsymbol, um die entsprechende Fehlermeldung anzuzeigen. Um das Problem zu beheben, verschieben Sie einfach die getrennte Aktivität und verbinden Sie sie mit der vorherigen Aktivität.

![Symbol „Warnung“ mit getrennten Aktivitäten auf der Arbeitsfläche](assets/canvas-disconnected.png)

## Kopieren und Einfügen von Aktivitäten {#copy-paste}

Sie können eine oder mehrere Aktivitäten einer Journey kopieren und entweder in derselben oder einer anderen Journey einfügen. So sparen Sie Zeit, wenn Sie verschiedene Aktivitäten wiederverwenden möchten, die bereits in einer vorherigen Journey konfiguriert wurden.

**Wichtige Hinweise**

* Sie können über verschiedene Tabs und Browser hinweg kopieren und einfügen. Sie können Aktivitäten nur innerhalb derselben Instanz kopieren/einfügen.
* Sie können ein Ereignis nicht kopieren/einfügen, wenn die Ziel-Journey über ein Ereignis verfügt, das einen anderen Namespace verwendet.
* Eingefügte Aktivitäten können auf Daten verweisen, die in der Ziel-Journey nicht vorhanden sind, z. B. wenn Sie Daten in verschiedene Sandboxes kopieren/einfügen. Führen Sie stets eine Fehlerprüfung durch und nehmen Sie die erforderlichen Anpassungen vor.
* Beachten Sie, dass sich eine Aktion nicht rückgängig machen lässt. Um eingefügte Aktivitäten zu löschen, müssen Sie sie auswählen und löschen. Wählen Sie also vor dem Kopieren ausschließlich benötigte Aktivitäten aus.
* Sie können Aktivitäten aus beliebigen Journeys kopieren, auch aus solchen, die schreibgeschützt sind.
* Sie können beliebige Aktivitäten auswählen, auch solche, die nicht verknüpft sind. Verknüpfte Aktivitäten bleiben nach dem Einfügen verknüpft.

Im Folgenden werden die Schritte zum Kopieren/Einfügen von Aktivitäten beschrieben:

1. Öffnen Sie eine Journey.
1. Wählen Sie die Aktivitäten aus, die Sie kopieren möchten, indem Sie die Maus darüber bewegen und klicken. Alternativ können Sie auf die einzelnen Aktivitäten klicken, während Sie die **Strg-/Befehlstaste** gedrückt halten. Verwenden Sie **Strg/Befehl + A**, wenn Sie alle Aktivitäten auswählen möchten.
   ![Auswählen mehrerer Aktivitäten in Journey zum Kopieren](assets/copy-paste1.png)
1. Drücken Sie **Strg/Befehl+C**.
Wenn Sie nur eine Aktivität kopieren möchten, können Sie darauf klicken und oben links im Konfigurationsbereich für die Aktivität das Symbol **Kopieren** verwenden.
   ![Symbol „Kopieren“ im Konfigurationsbereich für Aktivitäten](assets/copy-paste2.png)
1. Drücken Sie in einer beliebigen Journey die **Strg-/Befehlstaste + V**, um die Aktivitäten einzufügen, ohne sie mit einem vorhandenen Knoten zu verknüpfen. Eingefügte Aktivitäten werden in derselben Reihenfolge angeordnet. Nach dem Einfügen bleiben Aktivitäten ausgewählt, damit Sie sie einfach verschieben können. Sie können den Cursor auch auf einen leeren Platzhalter setzen und **Strg/Befehl+V** drücken. Eingefügte Aktivitäten werden mit dem Knoten verknüpft.
   ![Eingefügte Aktivitäten auf der Journey-Arbeitsfläche, die verbunden werden können](assets/copy-paste3.png)

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird die Arbeitsfläche des Journey Optimizer Journey-Designers vorgestellt und erläutert, wie mehrstufige Journey erstellt werden, indem Ereignisse, Orchestrierungs- und Aktionsaktivitäten aus der Palette gezogen und abgelegt werden.

**intents:**

* Navigieren in der Benutzeroberfläche des Journey-Designers (Palette, Arbeitsfläche, Symbolleiste, Konfigurationsbereich für Aktivitäten)
* Hinzufügen von Ereignissen, Orchestrierungsaktivitäten und Aktionsaktivitäten zu einer Journey-Arbeitsfläche
* Konfigurieren eines alternativen Fallback-Pfads für Bedingungs- und Aktionsaktivitäten bei Zeitüberschreitung oder Fehler
* Kopieren und Einfügen von Aktivitäten innerhalb derselben Journey oder über verschiedene Journey hinweg in derselben Instanz
* Starten einer Journey mit einem Ereignis-Trigger oder einem Einstiegspunkt für „Zielgruppe lesen“

**Glossar:**

* **Palette**: Das Bedienfeld auf der linken Seite im Journey-Designer, in dem alle verfügbaren Ereignisse, Orchestrierungs- und Aktionsaktivitäten für das Ziehen und Ablegen auf die Arbeitsfläche aufgelistet sind *(produktspezifisch)*
* **Canvas**: Der zentrale Designbereich des Journey-Designers, in dem Aktivitäten platziert, verbunden und konfiguriert werden *(produktspezifisch)*
* **Konfigurationsbereich für die Aktivität**: Der rechte Bereich, der geöffnet wird, wenn eine Aktivität auf der Arbeitsfläche ausgewählt wird. Dieser Bereich wird zum Ausfüllen der Aktivitätseinstellungen verwendet *produktspezifisch)*
* **Journey-Fragmente**: Wiederverwendbare Sätze vordefinierter Journey-Knoten, die direkt in die Arbeitsfläche eingefügt werden können, um zu vermeiden, dass gängige *(produktspezifisch) neu erstellt werden*
* **Reaktionsereignis**: Eine Ereignisaktivität, die nach einer Nachricht platziert wird, um die Journey auf der Grundlage von Empfängerverfolgungsinteraktionen (Öffnen, Klicken) zu verzweigen *(produktspezifisch)*

**Leitplanken:**

* Aktionen, Bedingungen, Warteaktivitäten und Reaktionsereignisse können nicht als erster Schritt in einer neuen Journey platziert werden.
* Kopieren/Einfügen wird nur innerhalb derselben Instanz unterstützt, instanzübergreifendes Kopieren/Einfügen wird nicht unterstützt.
* Sie können ein Ereignis nicht in eine Ziel-Journey kopieren, die einen anderen Namespace verwendet.
* Eingefügte Aktivitäten aus einer anderen Sandbox verweisen möglicherweise auf Daten, die auf der Ziel-Journey nicht vorhanden sind.
* Nur Ereignis- und Warteaktivitäten können parallel festgelegt werden. Andere Aktivitätstypen können nicht parallel ausgeführt werden.
* Alternative Pfade (Zeitüberschreitung/Fehler-Fallback) sind nur für Bedingungs- und Aktionsaktivitäten verfügbar.

**Terminologie:**

* Kanonischer Name: Journey Designer — Akronym: none — Varianten: Journey Canvas, Orchestrierung Canvas
* Synonyme: „Palette“ = „Aktivitäts-Bedienfeld“; „Arbeitsfläche“ = „Design-Bereich“
* Verwechseln Sie nicht: „events“ (Trigger-Journey-Eintrag oder Verzweigung) ≠ „actions“ (was passiert mit dem Kunden, z. B. eine Nachricht senden)

**FAQ:**

* **F: Wie gelangen Profile auf eine Journey?** - Profile geben entweder einheitlich in Echtzeit ein, wenn ein konfiguriertes Ereignis empfangen wird, oder im Batch, wenn die Aktivität „Zielgruppe lesen“ die Journey Trigger.
* **F: Kann ich mehrere Events zu einer Journey hinzufügen?** — Ja, Sie können mehrere Ereignisse hinzufügen, sofern sie alle denselben Namespace verwenden.
* **F: Wie kann ich ein Fallback definieren, wenn eine Aktion fehlschlägt?** — Aktivieren Sie in den Aktivitätseigenschaften die Option „Alternativen Pfad im Falle einer Zeitüberschreitung oder eines Fehlers hinzufügen“, um nach der Aktivität einen Fallback-Pfad hinzuzufügen.
* **F: Kann ich Aktivitäten von einer schreibgeschützten Journey kopieren?** — Ja, Sie können Aktivitäten von jeder Journey kopieren, unabhängig vom Status, aber Sie können nur innerhalb derselben Instanz einfügen.
* **F: Was ist ein Journey Fragment?** - Ein wiederverwendbarer Satz vordefinierter Journey-Knoten (z. B. Eignungsprüfungen, Begrüßungssequenzen), die direkt in die Arbeitsfläche eingefügt werden können, um zu vermeiden, dass die allgemeine Logik von Grund auf neu erstellt wird.

+++
