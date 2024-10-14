---
title: Potenzielle Konflikte in Journey und Kampagnen identifizieren
description: Erfahren Sie, wie Sie potenzielle Konflikte in Journey und Kampagnen identifizieren können.
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 3%

---


# Potenzielle Konflikte in Journey und Kampagnen erkennen {#conflict}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit Konfliktmanagement und Priorisierung](gs-conflict-prioritization.md)
* **[Potenzielle Konflikte in Journey und Kampagnen erkennen](conflicts.md)**
* [Zuweisen von Prioritätswerten zu Journeys und Kampagnen](priority-scores.md)
* [Journey-Begrenzung und Schlichtung](journey-capping.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Die Tools zur Konfliktverwaltung und Priorisierung sind derzeit nur für ausgewählte Benutzer verfügbar, da sie nur über eingeschränkte Verfügbarkeit verfügen.

Wenn Marketing-Experten das Kampagnen- und Journey-Volumen in Journey Optimizer steigern, wird es für Marketing-Experten immer schwieriger zu wissen, ob sie Kunden mit zu vielen Marketinginteraktionen bombardieren. Es ist daher von wesentlicher Bedeutung, einfach festzustellen, wann es Überschneidungen bei Kampagnen und Journey gibt, um sicherzustellen, dass sie das richtige Gleichgewicht zwischen Marketingkommunikation erreichen und gleichzeitig das Risiko der Kundenermüdung verringern.

Die wichtigsten Bereiche, die auf potenzielle Überschneidungen zu überwachen sind:

* **Timeline** (Start- und Enddatum): Laufen zu viele Journey gleichzeitig?
* **Audience**: Welcher Anteil meiner Journey-Audience ist auch Teil anderer Journey?
* **Kanal**: Sind für denselben Zeitraum andere Kommunikationen geplant, und wenn ja, wie viele?
* **Begrenzungsregelsatz**: Welche Journey kann ich begrenzen und gibt es Überschneidungen?
* **Kanalkonfiguration**: Gibt es andere Journey oder Kampagnen, die eine Kanalkonfiguration verwenden, die in derselben Journey oder Kampagne verwendet wird, die verhindern könnte, dass dem Endbenutzer die Journey oder Kampagne angezeigt wird?

## So erkennt Journey Optimizer Konflikte {#detection}

Nachstehend finden Sie eine Zusammenfassung dazu, wie Journey Optimizer potenzielle Konflikte für Journey und Kampagnen identifiziert:

* **Perimeter zur Identifizierung von Konflikten**: Konflikte werden nur für Live- oder geplante Kampagnen und Journey angezeigt.
* **Eindeutige Journey**: Wenn die ausgewählte Journey unitär ist, werden andere Journey angezeigt, die mit demselben Ereignis beginnen, da dieses Ereignis alle diese Journey Trigger.
* **Zielgruppenqualifizierung und Journey Lesen von Zielgruppen-/Geschäftsereignissen**: Wenn es sich bei der ausgewählten Journey um eine Zielgruppenqualifikation oder eine Journey zum Lesen von Zielgruppen-/Geschäftsereignissen handelt, werden alle anderen Journey desselben Typs mit einer gültigen Zielgruppe angezeigt, da es zu Überschneidungen zwischen den Zielgruppen kommen kann.
* **Kampagnen**: Da alle Kampagnen auf Zielgruppen ausgerichtet sind und kein Ereigniskonzept existiert, kollidieren alle Kampagnen möglicherweise mit segmentausgelösten Journey (angefangen mit der Aktivität Audience lesen ).
* **Live-/Geplante Kampagnen**: Live- und geplante Kampagnen können aufgrund möglicher Zielgruppenüberschneidungen miteinander in Konflikt geraten. Für jede Kampagne werden alle Live- oder geplanten Kampagnen in der Konfliktanzeige aufgelistet.

## Identifizierte Konflikte für bestimmte Journey oder Kampagnen anzeigen {#view}

Bei der Erstellung einer Journey oder Kampagne können Sie mit Journey Optimizer überprüfen, wann immer Überschneidungen mit anderen Journey oder Kampagnen möglich sind. Gehen Sie dazu wie folgt vor:

1. Klicken Sie zum Zeitpunkt der Erstellung einer Journey oder Kampagne in den Journey- oder Kampagneneigenschaften auf die Schaltfläche **[!UICONTROL Potenzielle Konflikte anzeigen]** .

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >Die Schaltfläche **[!UICONTROL Potenzielle Konflikte anzeigen]** steht zur Auswahl, sobald Sie eine der folgenden Einstellungen zugewiesen haben: **[!UICONTROL Start-/Enddatum]**, **[!UICONTROL Zielgruppe]**, **[!UICONTROL Kanal]**, **[!UICONTROL Kanalkonfiguration]** und **[!UICONTROL Regelsatz]**. Stellen Sie sicher, dass Sie nach dem Zuweisen dieser Einstellungen **[!UICONTROL Speichern]** auswählen, da die Schaltfläche erst ausgewählt werden kann, wenn die Änderungen gespeichert wurden.

1. Das Fenster **[!UICONTROL Potenzielle Konflikte]** wird geöffnet und ermöglicht Ihnen die Visualisierung aller Elemente, die sich mit der aktuellen Journey/Kampagne überschneiden.

   Sie können eine sich überschneidende Journey oder Kampagne direkt über diesen Bildschirm öffnen, indem Sie deren Namen auswählen.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >Die Anzeige neu veröffentlichter Kampagnen im Konflikt-Viewer kann bis zu 5 Minuten dauern, da die Zwischenspeicherung implementiert ist

Um die Suche nach potenziellen Überschneidungen weiter zu verfeinern, können Sie Ihre Kampagnen- und Journey-Liste nach den relevanten Feldern filtern. Wählen Sie dazu das Filtersymbol in der Lagerbestandsansicht aus. [Erfahren Sie, wie Sie mit Filtern arbeiten](../start/search-filter-categorize.md#filter-lists)

## Konflikte lösen {#resolve}

Im Folgenden finden Sie einige Tipps zur Reduzierung möglicher Konflikte, sobald diese erkannt wurden:

* Passen Sie die **Start-/Enddaten** an, um überlappende Kampagnen oder Journey zu vermeiden.
* Verfeinern Sie das **Zielgruppen-Targeting**, um Überschneidungen zwischen Journey zu minimieren.
* Implementieren Sie **Frequenzobergrenzen** , um zu verhindern, dass Kunden zu viele Nachrichten erhalten.
* Verringern Sie die Anzahl der aktiven Journey **** für eine effektivere Verwaltung des Kundenerlebnisses.
* Legen Sie **Prioritäten** für eingehende Aktionen fest, um sicherzustellen, dass den Kunden die wichtigste Aktion angezeigt wird.

Mithilfe dieser Funktionen können Sie sicherstellen, dass Ihre Marketing-Maßnahmen aufeinander abgestimmt sind und dass Sie bei Ihrer Kommunikationsstrategie das richtige Gleichgewicht wahren.
