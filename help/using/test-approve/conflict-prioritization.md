---
title: Konflikt-Management und Priorisierung
description: Erfahren Sie, wie Sie Ihren Inhalt in der Vorschau darstellen und testen können.
feature: Preview, Proofs
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '1187'
ht-degree: 100%

---


# Konflikt-Management und Priorisierung {#conflict-prioritization}

>[!AVAILABILITY]
>
>Die Tools für Konflikt-Management und Priorisierung sind derzeit nur für ausgewählte Benutzende als Beta-Version verfügbar.

In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kunden mit zu vielen Interaktionen überfordert werden. In den folgenden beiden Abschnitten werden wichtige Tools vorgestellt, die Ihnen dabei helfen, ein Gleichgewicht zu wahren und die Kommunikation effektiv zu priorisieren

## Identifizieren von potenziellen Konflikten in Journeys und Kampagnen {#conflict}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Konflikt-Viewer in Kampagnen"
>abstract="Mit diesem Tool können Sie Überschneidungen mit anderen Journeys, Kampagnen oder Kanalkonfigurationen ermitteln. Wenn Sie Überschneidungen bei Zielgruppe, Start- und Enddatum, Kanalkonfiguration, Kanal oder Regelsatz identifizieren möchten, können Sie hier potenzielle Konflikte anzeigen."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Konflikt-Viewer in Journeys"
>abstract="Mit diesem Tool können Sie Überschneidungen mit anderen Journeys, Kampagnen oder Kanalkonfigurationen ermitteln. Wenn Sie Überschneidungen bei Zielgruppe, Start- und Enddatum, Kanalkonfiguration, Kanal oder Regelsatz identifizieren möchten, können Sie hier potenzielle Konflikte anzeigen."

Da Marketing-Fachleute das Volumen von Kampagnen und Journeys in Journey Optimizer erhöhen, wird es für sie immer schwieriger zu erfahren, ob sie Ihre Kundschaft mit zu vielen Marketing-Interaktionen bombardieren. Daher ist es wichtig, dass Sie leicht erkennen können, wann es zu Überschneidungen von Kampagnen und Journeys kommt, um sicherzustellen, das richtige Gleichgewicht in der Marketing-Kommunikation zu finden und gleichzeitig das Risiko einer Ermüdung der Kundschaft zu minimieren.

Wichtige Bereiche, die auf mögliche Überschneidungen hin überwacht werden sollten, sind:

* **Timeline** (Start- und Enddatum): Laufen zu viele Journeys gleichzeitig?
* **Zielgruppe**: Wie viel Prozent meiner Journey-Zielgruppe sind auch Teil anderer Journeys?
* **Kanal**: Sind für denselben Zeitraum weitere Kommunikationsmaßnahmen geplant, und wenn ja, wie viele?
* **Regelwerk für Begrenzungen**: Welche Arten von Journeys werden von mir begrenzt und kommt es innerhalb dieser zu Überschneidungen?
* **Kanalkonfiguration**: Gibt es andere Journeys oder Kampagnen, die eine Kanalkonfiguration verwenden, die in derselben Journey oder Kampagne verwendet wird, was dazu führen könnte, dass die Journey oder Kampagne den Endbenutzenden nicht angezeigt wird?

### So erkennt Journey Optimizer Konflikte {#detection}

Nachfolgend finden Sie eine Zusammenfassung darüber, wie Journey Optimizer potenzielle Konflikte für Journeys und Kampagnen identifiziert:

* **Umfang der Konfliktidentifizierung**: Konflikte werden nur für aktive oder geplante Kampagnen und Journeys angezeigt.
* **Unitäre Journeys**: Wenn die ausgewählte Journey unitär ist, werden andere Journeys angezeigt, die mit demselben Ereignis beginnen, da dieses Ereignis alle diese Journeys auslöst.
* **Zielgruppenqualifikation und die Journeys „Zielgruppe lesen“/„Geschäftsereignis lesen“**: Wenn es sich bei der ausgewählten Journey entweder um eine Zielgruppenqualifikation oder die Journey „Zielgruppe lesen“ oder „Geschäftsereignis lesen“ handelt, werden alle anderen Journeys desselben Typs mit einer gültigen Zielgruppe angezeigt, da es Überschneidungen zwischen den Zielgruppen geben kann.
* **Kampagnen**: Da alle Kampagnen auf Zielgruppen ausgerichtet sind und es kein Konzept für Ereignisse gibt, können alle Kampagnen potenziell mit segmentgesteuerten Journeys (beginnend mit der Aktivität „Zielgruppe lesen“) in Konflikt stehen.
* **Live-/Geplante Kampagnen**: Live- und geplante Kampagnen können aufgrund möglicher Überschneidungen bei den Zielgruppen miteinander in Konflikt stehen. Für jede beliebige Kampagne werden alle Live- oder geplanten Kampagnen in der Konfliktansicht aufgelistet.

### Anzeigen von erkannten Konflikten für eine bestimmte Journey oder Kampagnen {#view}

Wenn Sie eine Journey oder Kampagne erstellen, können Sie mit Journey Optimizer überprüfen, ob es zu Überschneidungen mit anderen Journeys oder Kampagnen kommen kann. Gehen Sie dazu wie folgt vor:

1. Klicken Sie beim Erstellen einer Journey oder Kampagne in den Eigenschaften der Journey oder Kampagne auf die Schaltfläche **[!UICONTROL Potenzielle Konflikte anzeigen]**.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >Die Schaltfläche **[!UICONTROL Potenzielle Konflikte anzeigen]** wird verfügbar, sobald Sie eine der folgenden Einstellungen zugewiesen haben: **[!UICONTROL Start-/Enddatum]**, **[!UICONTROL Zielgruppe]**, **[!UICONTROL Kanal]**, **[!UICONTROL Kanalkonfiguration]** und **[!UICONTROL Regelsatz]**. Stellen Sie sicher, dass Sie nach dem Zuweisen dieser Einstellungen **[!UICONTROL Speichern]** auswählen, da die Schaltfläche erst ausgewählt werden kann, wenn die Änderungen gespeichert wurden.

1. Es öffnet sich das Fenster **[!UICONTROL Potenzielle Konflikte]**, in dem Sie alle Elemente sehen können, die sich mit der aktuellen Journey/Kampagne überschneiden.

   Sie können eine sich überschneidende Journey oder Kampagne direkt über diesen Bildschirm öffnen, indem Sie deren Namen auswählen.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >Bei neu veröffentlichten Kampagnen kann es aufgrund der implementierten Zwischenspeicherung bis zu 5 Minuten dauern, bis sie in der Konfliktanzeige angezeigt werden

Um die Suche nach potenziellen Überschneidungen weiter zu verfeinern, können Sie Ihre Liste der Kampagnen und Journeys nach den relevanten Feldern filtern. Wählen Sie dazu das Filtersymbol in der Ansicht „Sammlungsbestand“ aus. [Erfahren Sie, wie Sie mit Filtern arbeiten](../start/search-filter-categorize.md#filter-lists)

### Lösen von Konflikten {#resolve}

Hier sind einige Tipps, um potenzielle Konflikte zu reduzieren, sobald sie erkannt wurden:

* Passen Sie die **Start-/Enddaten** an, um überlappende Kampagnen oder Journey zu vermeiden.
* Verfeinern Sie das **Zielgruppen-Targeting**, um Überschneidungen zwischen Journeys zu minimieren.
* Implementieren Sie **Begrenzungen der Häufigkeit**, um zu verhindern, dass die Kundschaft zu viele Mitteilungen erhält.
* Reduzieren Sie die Anzahl der **aktiven Journeys**, um das Erlebnis für Ihre Kundschaft effektiver zu gestalten.
* Setzen Sie **Prioritäten** für eingehende Aktionen, um sicherzustellen, dass Ihrer Kundschaft die wichtigste Aktion angezeigt wird.

Mithilfe dieser Funktionen können Sie sicherstellen, dass Ihre Marketing-Maßnahmen aufeinander abgestimmt sind und dass Sie in Ihrer Kommunikationsstrategie das richtige Gleichgewicht wahren.

## Zuweisen von Prioritätswerten zu Journeys und Kampagnen {#priority}

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorität"
>abstract="Weisen Sie der Journey einen Prioritätswert von 0 bis 100 zu. Eine höhere Zahl bedeutet eine höhere Priorität. Der hier eingegebene Prioritätswert wird von allen eingehenden Aktionen übernommen (beispielsweise In-App-Aktionen), die in dieser Journey enthalten sind. In Fällen, in denen dieselbe eingehende Kanalkonfiguration in anderen Kampagnen oder Journeys verwendet wird, wird der Empfängerin bzw. dem Empfänger die eingehende Aktion mit der höchsten Priorität angezeigt. Wenn mehrere Journeys oder Kampagnen denselben Wert aufweisen, wird das Element ausgewählt, das zuletzt geändert wurde."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorität"
>abstract="Weisen Sie der Kampagne einen Prioritätswert von 0 bis 100 zu. Eine höhere Zahl bedeutet eine höhere Priorität. In Fällen, in denen dieselbe eingehende Kanalkonfiguration (beispielsweise In-App-Konfiguration) in anderen Kampagnen oder Journeys verwendet wird, wird der Empfängerin bzw. dem Empfänger die eingehende Aktion mit der höchsten Priorität angezeigt. Wenn mehrere Journeys oder Kampagnen denselben Wert aufweisen, wird das Element ausgewählt, das zuletzt geändert wurde."

Mit Journey Optimizer können Sie einer Journey oder Kampagne einen Prioritätswert zuweisen. Die Priorität ist von wesentlicher Bedeutung, um eine Journey, Kampagne oder Aktion zu priorisieren, wenn eine erzwungene Begrenzung vorliegt (z. B. eine Häufigkeittsbegrenzung). In Situationen, in denen Ihre Kundschaft für viele Journeys, Kampagnen oder Mitteilungen infrage kommt und Sie selektiv auswählen möchten, welche sie betreten und erhalten soll, sollten Sie dieses Feld verwenden.

>[!NOTE]
>
>Der Prioritätswert ist für eingehende Kanäle verfügbar: Web-, In-App- und Code-basierte Kanäle. In Journeys ist der Prioritätswert nur für die Kanäle **In-App** und **Code-basiert** verfügbar.

Die Zuweisung eines Prioritätswerts ist für eingehende Kommunikation wie Web, Mobile und In-App entscheidend. Wenn Sie mehrere Kampagnen haben, die dieselbe Kanalkonfiguration verwenden (z. B. ein Banner oben auf Ihrer Webseite), könnte dies problematisch sein, da nur Inhalte aus einer Kampagne angezeigt werden können. Bei dem Prioritätswert geben Sie an, welche Kampagne angezeigt werden soll, wenn die empfangende Person für mehr als eine Kampagne infrage kommt.

Um einer Journey oder Kampagne einen Prioritätswert zuzuweisen, geben Sie einen numerischen Wert (von 0 bis 100) in das Feld **[!UICONTROL Prioritätswert]** ein, das sich in den Journey- oder Kampagneneigenschaften befindet. Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn Sie diese Kampagne erstellen und sicherstellen möchten, dass der Inhalt dieser Kampagne angezeigt wird, sollten Sie ihr den Wert 100 geben.

![](assets/priority-score.png)

Wenn zwei Kampagnen die gleiche Priorität haben, wird die Kampagne angezeigt, die zuerst aktiviert wurde.
