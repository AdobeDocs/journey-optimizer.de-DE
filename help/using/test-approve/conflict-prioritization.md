---
title: Konfliktmanagement und Priorisierung
description: Erfahren Sie, wie Sie Ihren Inhalt in der Vorschau darstellen und testen können.
feature: Preview, Proofs
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: c609694693f11c77bc61ab31f0e7851262aadcce
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 6%

---


# Konfliktmanagement und Priorisierung {#conflict-prioritization}

>[!AVAILABILITY]
>
>Die Tools zur Konfliktverwaltung und Priorisierung sind derzeit nur ausgewählten Benutzern als Beta-Version verfügbar.

In Journey Optimizer ist die Verwaltung von Umfang und zeitlichem Verlauf von Kampagnen und Journey unverzichtbar, um zu verhindern, dass überwältigende Kunden mit zu vielen Interaktionen auf diese Weise ansprechen. In den folgenden beiden Abschnitten werden Schlüsselwerkzeuge vorgestellt, die Ihnen helfen, ein Gleichgewicht zu wahren und die Kommunikation effektiv zu priorisieren.

## Potenzielle Konflikte in Journey und Kampagnen anzeigen {#conflict}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Konflikt-Viewer in Kampagnen"
>abstract="Mit diesem Tool können Sie Überschneidungen mit anderen Journey, Kampagnen oder Kanalkonfigurationen feststellen. Wenn Sie Überschneidungen bei Zielgruppe, Start- und Enddatum, Kanalkonfiguration, Kanal oder Regelsatz ermitteln möchten, können Sie hier potenzielle Konflikte anzeigen."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Konflikt-Viewer in Journeys"
>abstract="Mit diesem Tool können Sie Überschneidungen mit anderen Journey, Kampagnen oder Kanalkonfigurationen feststellen. Wenn Sie Überschneidungen bei Zielgruppe, Start- und Enddatum, Kanalkonfiguration, Kanal oder Regelsatz ermitteln möchten, können Sie hier potenzielle Konflikte anzeigen."

Wenn Marketing-Experten das Kampagnen- und Journey-Volumen in Journey Optimizer steigern, wird es für Marketing-Experten immer schwieriger zu wissen, ob sie Kunden mit zu vielen Marketinginteraktionen bombardieren. Es ist daher von wesentlicher Bedeutung, einfach festzustellen, wann es Überschneidungen bei Kampagnen und Journey gibt, um sicherzustellen, dass sie das richtige Gleichgewicht zwischen Marketingkommunikation erreichen und gleichzeitig das Risiko der Kundenermüdung verringern.

Die wichtigsten Bereiche, die auf potenzielle Überschneidungen zu überwachen sind:

* **Timeline** (Start- und Enddatum): Laufen zu viele Journey gleichzeitig?
* **Audience**: Welcher Anteil meiner Journey-Audience ist auch Teil anderer Journey?
* **Kanal**: Sind für denselben Zeitraum andere Kommunikationen geplant, und wenn ja, wie viele?
* **Begrenzungsregelsatz**: Welche Journey kann ich begrenzen und gibt es Überschneidungen?
* **Kanalkonfiguration**: Gibt es andere Journey oder Kampagnen, die diese Kanalkonfiguration verwenden, die verhindern könnten, dass diese Kampagne dem Benutzer angezeigt wird?

Mit Journey Optimizer können Sie überprüfen, wann immer Überschneidungen mit anderen Journey oder Kampagnen möglich sind. Gehen Sie dazu wie folgt vor:

1. Klicken Sie zum Zeitpunkt der Erstellung einer Journey oder Kampagne in den Journey- oder Kampagneneigenschaften auf die Schaltfläche **[!UICONTROL Potenzielle Konflikte anzeigen]** .

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >Die Schaltfläche **[!UICONTROL Potenzielle Konflikte anzeigen]** kann ausgewählt werden, sobald Sie eine der folgenden Einstellungen zugewiesen haben: **[!UICONTROL Start-/Enddatum]**, **[!UICONTROL Zielgruppe]**, **[!UICONTROL Kanal]**, **[!UICONTROL Kanalkonfiguration]** und **[!UICONTROL Regelsatz]**.

1. Das Fenster **[!UICONTROL Potenzielle Konflikte]** wird geöffnet und ermöglicht Ihnen die Visualisierung aller Elemente, die sich mit der aktuellen Journey/Kampagne überschneiden.

   Sie können eine sich überschneidende Journey oder Kampagne direkt über diesen Bildschirm öffnen, indem Sie deren Namen auswählen.

   ![](assets/potential-conflicts.png)

>[!NOTE]
>
>Um die Suche nach potenziellen Überschneidungen weiter zu verfeinern, können Sie Ihre Kampagnen- und Journey-Liste nach den relevanten Feldern filtern. Wählen Sie dazu das Filtersymbol in der Lagerbestandsansicht aus. [Erfahren Sie, wie Sie mit Filtern arbeiten](../start/search-filter-categorize.md#filter-lists)

Sobald mögliche Überschneidungen festgestellt wurden, bietet Journey Optimizer mehrere Möglichkeiten, diese zu beheben.

* Passen Sie die **Start-/Enddaten** an, um überlappende Kampagnen oder Journey zu vermeiden.
* Verfeinern Sie das **Zielgruppen-Targeting**, um Überschneidungen zwischen Journey zu minimieren.
* Implementieren Sie **Frequenzobergrenzen** , um zu verhindern, dass Kunden zu viele Nachrichten erhalten.
* Verringern Sie die Anzahl der aktiven Journey **** für eine effektivere Verwaltung des Kundenerlebnisses.
* Legen Sie **Prioritäten** für eingehende Aktionen fest, um sicherzustellen, dass den Kunden die wichtigste Aktion angezeigt wird.

Mithilfe dieser Funktionen können Sie sicherstellen, dass Ihre Marketing-Maßnahmen aufeinander abgestimmt sind und dass Sie bei Ihrer Kommunikationsstrategie das richtige Gleichgewicht wahren.

## Zuweisen von Prioritätsbewertungen zu Journey und Kampagnen {#priority}

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorität"
>abstract="Weisen Sie der Journey einen Prioritätswert von 0 bis 100 zu. Eine höhere Zahl bedeutet eine höhere Priorität. Der hier eingegebene Prioritätswert wird von allen eingehenden Aktionen (wie In-App-Aktionen) übernommen, die in dieser Journey enthalten sind. In Fällen, in denen dieselbe eingehende Kanalkonfiguration in anderen Kampagnen oder Journey verwendet wird, wird dem Empfänger die eingehende Aktion mit der höchsten Priorität angezeigt. Wenn mehrere Journey oder Kampagnen dasselbe Ergebnis aufweisen, wird das Element ausgewählt, das zuletzt geändert wurde."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorität"
>abstract="Weisen Sie der Kampagne einen Prioritätswert von 0 bis 100 zu. Eine höhere Zahl bedeutet eine höhere Priorität. In Fällen, in denen dieselbe eingehende Kanalkonfiguration (z. B. In-App-Konfiguration) in anderen Kampagnen oder Journey verwendet wird, wird dem Empfänger die eingehende Aktion mit der höchsten Priorität angezeigt. Wenn mehrere Journey oder Kampagnen dasselbe Ergebnis aufweisen, wird das Element ausgewählt, das zuletzt geändert wurde."

Mit Journey Optimizer können Sie einer Journey oder Kampagne eine Prioritätsbewertung zuweisen. Die Priorität ist von wesentlicher Bedeutung, um eine Journey, Kampagne oder Aktion zu priorisieren, wenn eine erzwungene Einschränkung vorliegt (z. B. eine Frequenzbegrenzung). Wenn ein Kunde für viele Journey, Kampagnen oder Mitteilungen qualifiziert ist und Sie selektiv sein möchten, in welche Bereiche er eintreten und welche er empfangen soll, sollten Sie dieses Feld nutzen.

>[!NOTE]
>
>Die Prioritätsbewertung ist für eingehende Kanäle verfügbar: Web-, In-App- und code-basierte Kanäle. Unter Journey ist die Prioritätsbewertung nur für den Kanal **in der App** verfügbar.

Die Zuweisung eines Prioritätswerts ist für die eingehende Kommunikation wie Web, Mobile und In-App-Nachrichten von entscheidender Bedeutung. Wenn mehrere Kampagnen dieselbe Kanalkonfiguration verwenden (z. B. ein Banner oben auf Ihrer Webseite), kann dies problematisch sein, da nur Inhalte einer Kampagne angezeigt werden können. In der Prioritätsbewertung legen Sie Ihre Voreinstellung fest, für welche Kampagne angezeigt werden soll, wenn sich der Empfänger für mehr als eine Kampagne qualifizieren kann.

Um einer Journey oder Kampagne eine Prioritätsbewertung zuzuweisen, geben Sie einen numerischen Wert (von 0-100) in das Feld **[!UICONTROL Prioritätsbewertung]** ein, das sich in den Journey- oder Kampagneneigenschaften befindet. Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. Wenn Sie diese Kampagne erstellen und sicherstellen möchten, dass dieser Kampagneninhalt angezeigt wird, erhalten Sie eine Punktzahl von 100.

![](assets/priority-score.png)

In Situationen, in denen zwei Kampagnen dieselbe Prioritätsbewertung aufweisen, wird die zuletzt aktivierte Kampagne angezeigt.
