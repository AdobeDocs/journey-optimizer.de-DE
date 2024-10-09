---
title: Konflikt-Management und Priorisierung
description: Erfahren Sie, wie Sie Ihren Inhalt in der Vorschau darstellen und testen können.
feature: Preview, Proofs
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: ff529c9319a6eb5fe6762f30b739f2c39c3d5685
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 22%

---


# Konflikt-Management und Priorisierung {#conflict-prioritization}

>[!AVAILABILITY]
>
>Die Tools zur Konfliktverwaltung und Priorisierung sind derzeit nur ausgewählten Benutzern als Beta-Version verfügbar.

In Journey Optimizer ist die Verwaltung von Umfang und zeitlichem Verlauf von Kampagnen und Journey unverzichtbar, um zu verhindern, dass überwältigende Kunden mit zu vielen Interaktionen auf diese Weise ansprechen. In den folgenden beiden Abschnitten werden Schlüsselwerkzeuge vorgestellt, mit denen Sie ein ausgewogenes Verhältnis gewährleisten und die Kommunikation effektiv priorisieren können

## Potenzielle Konflikte in Journey und Kampagnen identifizieren {#conflict}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Konflikt-Viewer in Kampagnen"
>abstract="Mit diesem Tool können Sie Überschneidungen mit anderen Journeys, Kampagnen oder Kanalkonfigurationen ermitteln. Wenn Sie Überschneidungen bei Zielgruppe, Start- und Enddatum, Kanalkonfiguration, Kanal oder Regelsatz identifizieren möchten, können Sie hier potenzielle Konflikte anzeigen."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Konflikt-Viewer in Journeys"
>abstract="Mit diesem Tool können Sie Überschneidungen mit anderen Journeys, Kampagnen oder Kanalkonfigurationen ermitteln. Wenn Sie Überschneidungen bei Zielgruppe, Start- und Enddatum, Kanalkonfiguration, Kanal oder Regelsatz identifizieren möchten, können Sie hier potenzielle Konflikte anzeigen."

Wenn Marketing-Experten das Kampagnen- und Journey-Volumen in Journey Optimizer steigern, wird es für Marketing-Experten immer schwieriger zu wissen, ob sie Kunden mit zu vielen Marketinginteraktionen bombardieren. Es ist daher von wesentlicher Bedeutung, einfach festzustellen, wann es Überschneidungen bei Kampagnen und Journey gibt, um sicherzustellen, dass sie das richtige Gleichgewicht zwischen Marketingkommunikation erreichen und gleichzeitig das Risiko der Kundenermüdung verringern.

Die wichtigsten Bereiche, die auf potenzielle Überschneidungen zu überwachen sind:

* **Timeline** (Start- und Enddatum): Laufen zu viele Journey gleichzeitig?
* **Audience**: Welcher Anteil meiner Journey-Audience ist auch Teil anderer Journey?
* **Kanal**: Sind für denselben Zeitraum andere Kommunikationen geplant, und wenn ja, wie viele?
* **Begrenzungsregelsatz**: Welche Journey kann ich begrenzen und gibt es Überschneidungen?
* **Kanalkonfiguration**: Gibt es andere Journey oder Kampagnen, die eine Kanalkonfiguration verwenden, die in derselben Journey oder Kampagne verwendet wird, die verhindern könnte, dass dem Endbenutzer die Journey oder Kampagne angezeigt wird?

### So erkennt Journey Optimizer Konflikte {#detection}

Nachstehend finden Sie eine Zusammenfassung dazu, wie Journey Optimizer potenzielle Konflikte für Journey und Kampagnen identifiziert:

* **Perimeter zur Identifizierung von Konflikten**: Konflikte werden nur für Live- oder geplante Kampagnen und Journey angezeigt.
* **Eindeutige Journey**: Wenn die ausgewählte Journey unitär ist, werden andere Journey angezeigt, die mit demselben Ereignis beginnen, da dieses Ereignis alle diese Journey Trigger.
* **Zielgruppenqualifizierung und Journey Lesen von Zielgruppen-/Geschäftsereignissen**: Wenn es sich bei der ausgewählten Journey um eine Zielgruppenqualifikation oder eine Journey zum Lesen von Zielgruppen-/Geschäftsereignissen handelt, werden alle anderen Journey desselben Typs mit einer gültigen Zielgruppe angezeigt, da es zu Überschneidungen zwischen den Zielgruppen kommen kann.
* **Kampagnen**: Da alle Kampagnen auf Zielgruppen ausgerichtet sind und kein Ereigniskonzept existiert, kollidieren alle Kampagnen möglicherweise mit segmentausgelösten Journey (angefangen mit der Aktivität Audience lesen ).
* **Live-/Geplante Kampagnen**: Live- und geplante Kampagnen können aufgrund möglicher Zielgruppenüberschneidungen miteinander in Konflikt geraten. Für jede Kampagne werden alle Live- oder geplanten Kampagnen in der Konfliktanzeige aufgelistet.

### Identifizierte Konflikte für bestimmte Journey oder Kampagnen anzeigen {#view}

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

### Konflikte lösen {#resolve}

Im Folgenden finden Sie einige Tipps zur Reduzierung möglicher Konflikte, sobald diese erkannt wurden:

* Passen Sie die **Start-/Enddaten** an, um überlappende Kampagnen oder Journey zu vermeiden.
* Verfeinern Sie das **Zielgruppen-Targeting**, um Überschneidungen zwischen Journey zu minimieren.
* Implementieren Sie **Frequenzobergrenzen** , um zu verhindern, dass Kunden zu viele Nachrichten erhalten.
* Verringern Sie die Anzahl der aktiven Journey **** für eine effektivere Verwaltung des Kundenerlebnisses.
* Legen Sie **Prioritäten** für eingehende Aktionen fest, um sicherzustellen, dass den Kunden die wichtigste Aktion angezeigt wird.

Mithilfe dieser Funktionen können Sie sicherstellen, dass Ihre Marketing-Maßnahmen aufeinander abgestimmt sind und dass Sie bei Ihrer Kommunikationsstrategie das richtige Gleichgewicht wahren.

## Zuweisen von Prioritätswerten zu Journeys und Kampagnen {#priority}

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorität"
>abstract="Weisen Sie der Journey einen Prioritätswert von 0 bis 100 zu. Eine höhere Zahl bedeutet eine höhere Priorität. Der hier eingegebene Prioritätswert wird von allen eingehenden Aktionen übernommen (beispielsweise In-App-Aktionen), die in dieser Journey enthalten sind. In Fällen, in denen dieselbe eingehende Kanalkonfiguration in anderen Kampagnen oder Journeys verwendet wird, wird der Empfängerin bzw. dem Empfänger die eingehende Aktion mit der höchsten Priorität angezeigt. Wenn mehrere Journeys oder Kampagnen denselben Wert aufweisen, wird das Element ausgewählt, das zuletzt geändert wurde."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorität"
>abstract="Weisen Sie der Kampagne einen Prioritätswert von 0 bis 100 zu. Eine höhere Zahl bedeutet eine höhere Priorität. In Fällen, in denen dieselbe eingehende Kanalkonfiguration (beispielsweise In-App-Konfiguration) in anderen Kampagnen oder Journeys verwendet wird, wird der Empfängerin bzw. dem Empfänger die eingehende Aktion mit der höchsten Priorität angezeigt. Wenn mehrere Journeys oder Kampagnen denselben Wert aufweisen, wird das Element ausgewählt, das zuletzt geändert wurde."

Mit Journey Optimizer können Sie einer Journey oder Kampagne eine Prioritätsbewertung zuweisen. Die Priorität ist von wesentlicher Bedeutung, um eine Journey, Kampagne oder Aktion zu priorisieren, wenn eine erzwungene Einschränkung vorliegt (z. B. eine Frequenzbegrenzung). Wenn ein Kunde für viele Journey, Kampagnen oder Mitteilungen qualifiziert ist und Sie selektiv sein möchten, in welche Bereiche er eintreten und welche er empfangen soll, sollten Sie dieses Feld nutzen.

>[!NOTE]
>
>Die Prioritätsbewertung ist für eingehende Kanäle verfügbar: Web-, In-App- und code-basierte Kanäle. Unter Journey ist die Prioritätsbewertung nur für die Kanäle **in der App** und **code-basiert** verfügbar.

Die Zuweisung eines Prioritätswerts ist für die eingehende Kommunikation wie Web, Mobile und In-App-Nachrichten von entscheidender Bedeutung. Wenn mehrere Kampagnen dieselbe Kanalkonfiguration verwenden (z. B. ein Banner oben auf Ihrer Webseite), kann dies problematisch sein, da nur Inhalte einer Kampagne angezeigt werden können. In der Prioritätsbewertung legen Sie Ihre Voreinstellung fest, für welche Kampagne angezeigt werden soll, wenn sich der Empfänger für mehr als eine Kampagne qualifizieren kann.

Um einer Journey oder Kampagne eine Prioritätsbewertung zuzuweisen, geben Sie einen numerischen Wert (von 0-100) in das Feld **[!UICONTROL Prioritätsbewertung]** ein, das sich in den Journey- oder Kampagneneigenschaften befindet. Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn Sie diese Kampagne erstellen und sicherstellen möchten, dass dieser Kampagneninhalt angezeigt wird, erhalten Sie eine Punktzahl von 100.

![](assets/priority-score.png)

In Situationen, in denen zwei Kampagnen dieselbe Prioritätsbewertung aufweisen, wird die zuvor aktivierte Kampagne angezeigt.
