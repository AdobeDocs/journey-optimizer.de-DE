---
solution: Journey Optimizer
product: journey optimizer
title: Herausforderungen bei der Treue schaffen
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Herausforderungen im Zusammenhang mit Treueprogrammen erstellen und konfigurieren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: c950bee8-4ea9-4b64-810d-91371e8b3e4c
feature_v2: []
subfeature_v2: []
source-git-commit: 2e01cd1880b8527911376d94188d0204f7649541
workflow-type: tm+mt
source-wordcount: 1973
ht-degree: 16%

---

# Herausforderungen schaffen {#create-challenges}

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

[Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Herausforderungen erstellen und verwalten**

* [Zugriff und Verwaltung von Herausforderungen und Aufgaben](access-loyalty-challenges.md)
* **Herausforderungen schaffen** ◀︎ **Sie sind hier**
* [Aufgaben erstellen](create-tasks.md)
* [Überwachen der Leistung beim Treueprogramm](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Konfigurieren und Integrieren**

* [Herausforderungen bei der Treue konfigurieren](loyalty-admin.md)
* [Treuedaten und -datensätze](loyalty-data-and-datasets.md)
* [API-Referenz für Herausforderungen im Treueprogramm](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **privaten Betaversion**. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](../rn/releases.md).

Auf dieser Seite wird der gesamte Prozess zur Erstellung einer Herausforderung für das Treueprogramm behandelt, von der Auswahl des Challenge-Typs und der Konfiguration der Eigenschaften bis hin zur Erstellung und Veröffentlichung der Journey, die die Herausforderung an Ihre Kunden richtet.

## Herausforderung erstellen {#create-the-challenge}

1. Navigieren Sie zu **[!UICONTROL Herausforderungen zum Treueprogramm (Beta]** in Journey Optimizer.

1. Wählen Sie die Registerkarte **[!UICONTROL Herausforderungen]** und wählen Sie **[!UICONTROL Herausforderung erstellen]**.

   ![](assets/challenge-create.png)

1. Wählen Sie den Challenge-Typ:

   * **[!UICONTROL Standard]**: Kunden führen eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus\
     *Beispiel: 3 von 5 verfügbaren Aufgaben abschließen*

   * **[!UICONTROL Streak]**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus\
     *Beispiel: Tätigen Sie einen Kauf an 7 aufeinander folgenden Tagen*

   * **[!UICONTROL Sequenziell]**: Kunden führen Aufgaben in einer definierten Reihenfolge aus\
     *Beispiel: → erwerben → überprüfen (muss in dieser Reihenfolge ausgefüllt werden)*

   * **[!UICONTROL Eigene Daten einbringen]**: Wählen Sie **[!UICONTROL Eigene Daten einbringen]**, wenn Sie möchten, dass das Challenge-Framework, z. B. Aufgaben und Belohnungen, aus Ihrer Loyalty Challenges-Datenintegration zusammengestellt wird. Wenn dieser Typ ausgewählt ist, müssen Sie die Challenge-Struktur nicht konfigurieren. Sie konfigurieren nur **[!UICONTROL Content]**, **[!UICONTROL Messaging]** und **[!UICONTROL Audience]** wie andere Challenges.

     >[!AVAILABILITY]
     >
     >Der Challenge **[!UICONTROL Typ „Eigene Daten]**&quot; steht derzeit einer begrenzten Anzahl von Organisationen zur Verfügung und wird in einer zukünftigen Version breiter verfügbar gemacht.

   Nach Auswahl eines Challenge-Typs wird die Benutzeroberfläche zur Challenge-Erstellung mit mehreren Konfigurations-Registerkarten geöffnet. Beginnen Sie bei allen Typen außer **[!UICONTROL Eigene Daten einbringen]** mit der Konfiguration der Challenge-Struktur.

## Konfiguration der Challenge-Struktur {#structure}

Definieren Sie auf **[!UICONTROL Registerkarte]** Struktur“, wie Ihre Herausforderung organisiert ist: Eigenschaften, Zeitplan, abzuschließende Aufgaben und Belohnungen.

### Definieren der Challenge-Eigenschaften und Verwenden benutzerdefinierter Metadaten {#properties}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_properties"
>title="Challenge-Eigenschaften"
>abstract="Legen Sie im Bereich „Challenge-Eigenschaften“ den Namen und die Beschreibung der Challenge fest und fügen Sie benutzerdefinierte Schlüssel/Wert-Metadaten für das Tracking oder externe Integrationen hinzu."

1. Definieren Sie **[!UICONTROL Bereich &quot;]**&quot; globale Einstellungen für die Herausforderung:

   * **[!UICONTROL Name]**: Geben Sie einen beschreibenden Namen für Ihre Challenge ein. Dieser Name wird im Challenges-Inventar angezeigt.
   * **[!UICONTROL Beschreibung]**: Geben Sie eine Beschreibung ein, die den Zweck und die Ziele der Herausforderung erklärt.

1. Verwenden Sie den Abschnitt **[!UICONTROL Benutzerdefinierte Metadaten]**, um benutzerdefinierte Metadaten mithilfe von Schlüssel/Wert-Paaren hinzuzufügen. Diese Metadaten können für das Tracking oder die Integration mit externen Systemen verwendet werden.

   ![](assets/challenge-create-properties.png)

### Planen der Challenge {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_schedule"
>title="Challenge-Zeitplan"
>abstract="Verwenden Sie den Zeitplan, um festzulegen, wann die Challenge live ist: Legen Sie das Startdatum und die Startzeit fest, wann die Challenge für Kundinnen und Kunden verfügbar sein wird, sowie das Enddatum und die Endzeit, wann keine Abschlüsse mehr angenommen werden. Wählen Sie eine Zeitzone aus und wählen Sie im Abschnitt **[!UICONTROL Fenster zum Abschluss von Aufgaben]** aus, wann Kundinnen und Kunden Aufgaben abschließen können."

Konfigurieren Sie, wann Ihre Challenge ausgeführt wird:

1. Wählen Sie das Symbol **[!UICONTROL Zeitplan öffnen]** aus:

   ![](assets/challenge-create-schedule.png)

1. Konfigurieren Sie die folgenden Planungsoptionen:

   * **[!UICONTROL Startdatum und -uhrzeit]**: Legen Sie fest, wann die Challenge für Kunden verfügbar sein soll.
   * **[!UICONTROL Enddatum und -uhrzeit]**: Legt fest, wann die Challenge abläuft und keine neuen Abschlüsse mehr akzeptiert.
   * **[!UICONTROL Zeitzone]**: Bei der Challenge wird standardmäßig die lokale Zeitzone des Empfängers verwendet.
   * **[!UICONTROL Aufgaben müssen abgeschlossen sein]**: Wählen Sie aus, wann Kunden Aufgaben abschließen können:

      * **[!UICONTROL Jederzeit während der Herausforderung]**: Kunden können Aufgaben jederzeit zwischen dem Start- und dem Enddatum der Herausforderung abschließen.
      * **[!UICONTROL Während bestimmter Tageszeiten:]** Sie den Aufgabenabschluss auf bestimmte tägliche Stunden ein, indem Sie die **[!UICONTROL Startzeit]** und **[!UICONTROL Endzeit“]**.

Der Zeitplan für die Challenge ist jetzt konfiguriert. Fügen Sie als Nächstes die Aufgaben hinzu, die Kunden abschließen müssen.

### Aufgaben hinzufügen {#add-tasks}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_tasks"
>title="Aufgaben"
>abstract="Wählen Sie die Aufgaben aus, die ausgeführt werden sollen, um die Challenge abzuschließen. Konfigurieren Sie anschließend, wie die Challenge abgeschlossen wird. Die verfügbaren Optionen hängen von Ihrem Challenge-Typ ab (Standard, Streak oder Sequenziell)."

Aufgaben definieren die spezifischen Aktionen, die Kunden durchführen müssen, um Belohnungen zu erhalten. Sie können Aufgabentypen (Kauf, Ausgaben oder benutzerspezifisches Ereignis), Mengen, Produktfilter und andere Attribute konfigurieren.

Gehen Sie wie folgt vor, um Ihrer Herausforderung Aufgaben hinzuzufügen:

1. Wählen Sie **[!UICONTROL Abschnitt]** Aufgaben“ **[!UICONTROL Aufgabe hinzufügen]** aus.

   ![](assets/challenge-create-add-task.png)

1. Das **[!UICONTROL Aufgabeninventar]** wird geöffnet. Wählen Sie eine oder mehrere Aufgaben aus der Liste aus und klicken Sie auf **[!UICONTROL Hinzufügen]**. Um eine neue Aufgabe zu erstellen, wählen Sie **[!UICONTROL Neu]** aus. [Erfahren Sie, wie Sie Aufgaben erstellen und konfigurieren](create-tasks.md).

1. Geben Sie an, wann die Herausforderung als abgeschlossen gilt. Die verfügbaren Einstellungen hängen vom Challenge-Typ ab:

   +++Standardmäßige Herausforderungen

   Wählen Sie in **[!UICONTROL Dropdown-Liste]** Anforderung für Aufgabenabschluss“ zwischen:

   * **[!UICONTROL Der Kunde wählt eine zu]** Aufgabe aus *- Kunden können jede einzelne Aufgabe auswählen und abschließen, um Belohnungen zu erhalten*
   * **[!UICONTROL Kunde führt eine bestimmte Anzahl von Aufgaben aus]** - *Kunden müssen eine definierte Anzahl von Aufgaben ausführen. Geben Sie die erforderliche Anzahl von Aufgaben an, die abgeschlossen werden sollen.*

   +++

   +++Herausforderungen meistern

   Wählen **[!UICONTROL in der Dropdown]** Liste „Streak-Typ“ zwischen:

   * **Aufeinander folgend**: Kunden müssen die Aufgabe an aufeinander folgenden Tagen ohne Pausen abschließen. *Beispiel: Kauf am Montag, Dienstag, Mittwoch - ein Tag fehlt, bricht die Serie.*

   * **Nicht fortlaufend**: Kunden können die Aufgabe mit Lücken zwischen den Abschlüssen abschließen. *Beispiel: 7 Käufe über 30 Tage abschließen, wobei Pausen erlaubt sind.*

   Geben **[!UICONTROL im Feld]** an, wie oft die Aufgabe abgeschlossen werden soll. *Beispiel: Für eine „7-tägige Kauf-Stream“ auf 7 festgelegt*

   +++

   +++Sequenzielle Herausforderungen

   Wählen Sie in **[!UICONTROL Dropdown-Liste]** Anforderung für Aufgabenabschluss“ zwischen:

   * **[!UICONTROL Der Kunde wählt eine zu]** Aufgabe aus *- Kunden können jede einzelne Aufgabe auswählen und abschließen, um Belohnungen zu erhalten*
   * **[!UICONTROL Kunde führt eine bestimmte Anzahl von Aufgaben aus]** - *Kunden müssen eine definierte Anzahl von Aufgaben in der von Ihnen definierten Reihenfolge ausführen. Fehlende oder ausgelassene Aufgaben unterbrechen die Sequenz. Geben Sie die erforderliche Anzahl von Aufgaben an, die abgeschlossen werden sollen*

   +++

1. Standardmäßig können Kunden mit standardmäßigen und sequenziellen Herausforderungen Aufgaben über mehrere Transaktionen hinweg ausführen. Wenn alle Aufgaben in einer Transaktion ausgeführt werden sollen, wählen Sie das Symbol **[!UICONTROL Einstellungen]** und aktivieren Sie die folgende Option.

   ![](assets/challenge-create-single-transaction.png)

Nachdem Sie Aufgaben zu Ihrer Challenge hinzugefügt haben, konfigurieren Sie die Belohnungen, die Kunden für den Abschluss erhalten.

### Konfigurieren von Prämien {#rewards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_rewards"
>title="Prämien"
>abstract="Wählen Sie aus, wann Kundinnen und Kunden Punkte sammeln: wenn sie die gesamte Challenge abgeschlossen haben, oder bei einzelnen Meilensteinen im Verlauf der Aufgabe. Wählen Sie Ihren Prämienanbieter aus (Ihre Treuelösung, die Punkte und Prämien verwaltet) und legen Sie dann die Beträge fest: einen Gesamtbetrag für den vollständigen Abschluss oder Werte pro Aufgabe für Meilensteine, wobei Prämien nur für die Aufgaben aktiviert werden, für die Sie eine Auszahlung vornehmen möchten."

Prämien sind die Treuepunkte oder Vorteile, die Kundinnen und Kunden bei der Bewältigung von Herausforderungen erhalten.

So konfigurieren Sie, wann und wie Belohnungen bereitgestellt werden:

1. Wählen Sie im Dropdown **[!UICONTROL Menü]** Belohnungsversand“ aus, wann Belohnungen bereitgestellt werden sollen:

   * **[!UICONTROL Belohnungen nach Abschluss der Herausforderung bereitstellen]**: Belohnungen erhalten, wenn Kunden die gesamte Herausforderung bewältigen\
     *Beispiel: Vergabe von 100 Punkten nach Abschluss aller 5 Aufgaben*

   * **[!UICONTROL Belohnungen bei Meilensteinen zum Abschluss von Aufgaben bereitstellen, sobald der Fortschritt der Herausforderung erreicht wird]**: Belohnungen werden schrittweise verliehen, sobald Kunden einzelne Aufgaben erledigen (nur für Herausforderungen, die mehr als eine Aufgabe erfordern).\
     *Beispiel: Vergabe von 10 Punkten nach Aufgabe 1, 20 Punkten nach Aufgabe 2 und 50 Punkten nach Aufgabe 3*

1. Wählen Sie Ihren Belohnungsanbieter. Dies ist Ihre Treuelösung, mit der Kundenpunkte und -belohnungen verwaltet werden. Belohnungsanbieter werden im Menü **[!UICONTROL Treueprogramm-Administrator]** erstellt, bevor Sie Herausforderungen für Ihre Autoren erstellen. [Erfahren Sie, wie Sie Belohnungsanbieter konfigurieren](loyalty-admin.md#reward-providers)

   ![](assets/challenge-create-reward-type.png)

1. Konfigurieren Sie die Belohnungsbeträge basierend auf Ihrer ausgewählten Versandmethode:

   +++Belohnungen nach Abschluss der Challenge bereitstellen

   Geben Sie den Gesamtbelohnungsbetrag an, der gegeben werden soll, wenn Kunden die gesamte Challenge abschließen.

   *Im folgenden Beispiel erhalten Kunden 100 Punkte, wenn sie die Challenge abschließen.*

   ![](assets/challenge-create-reward-total.png)

   +++

   +++Belohnungen bei Meilensteinen bei Aufgabenabschluss bereitstellen

   Belohnungsbeträge für Meilensteine bei Aufgabenabschluss angeben. Mit dieser Option können Sie progressive Belohnungen schaffen, die die Motivation der Kunden im Laufe der Challenge steigern.

   Schalten Sie für jede Aufgabe, für die Sie eine Belohnung bereitstellen möchten, die Option Belohnung ein und geben Sie an, wie viele Punkte Kunden erhalten sollen, wenn sie diese Aufgabe erfüllen. Sie können festlegen, dass nur bestimmte Aufgabenabschlüsse belohnt werden sollen. Wenn Sie beispielsweise 10 Aufgaben haben, belohnen Sie möglicherweise nur die Aufgaben 1, 5 und 10.

   *Im folgenden Beispiel erhalten Kunden beim Abschluss der ersten Aufgabe 10 Punkte und nach Abschluss der zweiten Aufgabe 50 zusätzliche Punkte.*

   ![](assets/challenge-create-reward-milestones.png)

   +++

Gestalten Sie nach der Konfiguration der Challenge-Struktur mit Aufgaben und Belohnungen die Inhaltskarten, um den Kunden die Challenge anzuzeigen.

## Konfigurieren von Inhaltskarten {#configure-content-cards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_content"
>title="Inhalt"
>abstract="Konfigurieren Sie die Inhaltskarte, die Ihre Challenge auf Kundengeräten darstellt und Informationen, Fortschritt und Prämien für die Challenge anzeigt. Geben Sie einen Namen für die Karte ein, wählen Sie eine Kanalkonfiguration aus, damit beim Versand die richtigen technischen Einstellungen verwendet werden (z. B. Header, Subdomain oder Apps), und wählen Sie dann „Inhalt bearbeiten“ aus, um das Kartenerlebnis zu entwerfen und zu personalisieren."

Inhaltskarten stellen Ihre Herausforderung auf Kundengeräten visuell dar und zeigen Informationen zur Herausforderung, den Fortschritt und die Belohnungen an. [Weitere Informationen zu Inhaltskarten](../content-card/create-content-card.md).

So konfigurieren Sie Inhaltskarten für Ihre Challenge:

1. Navigieren Sie zur Registerkarte **[!UICONTROL Inhalt]** und geben Sie einen **[!UICONTROL Namen]** für die Inhaltskarte ein.

1. Wählen Sie die **[!UICONTROL Kanalkonfiguration]**. Kanalkonfigurationen enthalten alle technischen Parameter zum Senden von Nachrichten, z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Weitere Informationen zu Kanalkonfigurationen](../configuration/channel-surfaces.md).

1. Wählen Sie **[!UICONTROL Inhalt bearbeiten]** aus, um Ihre Inhaltskarte zu entwerfen. [Erfahren Sie, wie Sie Inhaltskarten entwerfen und personalisieren](../content-card/design-content-card.md).

   ![](assets/challenge-create-content.png)

Richten Sie nach der Konfiguration der Inhaltskarte Messaging ein, um Kunden während des gesamten Challenge-Lebenszyklus anzusprechen.

### Konfigurieren von Messaging {#configure-messaging}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_messaging"
>title="Messaging"
>abstract="Messaging unterstützt die Interaktion über den gesamten Challenge-Lebenszyklus hinweg. Fügen Sie auf der Registerkarte „Messaging“ Nachrichten für jeden Schritt hinzu: „Start“ (wenn die Challenge beginnt), „In Bearbeitung“ (Erinnerungen und Fortschrittsaktualisierungen) und „Abschluss“ (Erfolg feiern und Prämien bestätigen). Fügen Sie für jeden Schritt eine Nachricht hinzu, wählen Sie den Kanal aus, wählen Sie eine Kanalkonfiguration aus und klicken Sie dann auf „Bearbeiten“, um den Nachrichteninhalt zu entwerfen."

Richten Sie Multi-Channel-Nachrichten ein, um Kunden in wichtigen Phasen des Challenge-Lebenszyklus anzusprechen. Messaging ist optional, wird aber zur Maximierung der Kundeninteraktion empfohlen.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Messaging]** und konfigurieren Sie Nachrichten für jede Lebenszyklusphase:

   * **Launch**-Nachricht: Kunden benachrichtigen, wenn die Herausforderung beginnt
   * **In Bearbeitung** Nachricht: Halten Sie Kunden mit Erinnerungen und Fortschrittsaktualisierungen in Verbindung
   * **Completion** Nachricht: Erfolg feiern und Zuweisung der Belohnung bestätigen

1. Klicken Sie für jede Phase auf die Schaltfläche Nachricht hinzufügen , um eine Nachricht für diese Phase zu erstellen.

1. Wählen Sie den gewünschten Kanal aus: **[!UICONTROL In-App]**, **[!UICONTROL E-Mail]** oder **[!UICONTROL Push-Benachrichtigung]** und wählen Sie die zugehörige Kanalkonfiguration.

1. Klicken Sie auf das ![](assets/do-not-localize/Smock_More_18_N.svg) und wählen Sie **[!UICONTROL Bearbeiten]** aus, um den Nachrichteninhalt zu entwerfen.

   ![](assets/challenge-create-messaging.png)

In diesen Abschnitten erfahren Sie, wie Sie Nachrichten für bestimmte Kanäle erstellen: [In-App-Nachrichten](../in-app/get-started-in-app.md) - [E-Mail-Nachrichten](../email/get-started-email.md) - [Push-Benachrichtigungen](../push/get-started-push.md)

Legen Sie nach Abschluss der Messaging-Konfiguration fest, welche Kunden für die Teilnahme an der Challenge infrage kommen.

## Auswählen der Zielgruppe für die Challenge {#audience}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_audience"
>title="Zielgruppe"
>abstract="Wählen Sie auf der Registerkarte „Zielgruppe“ aus den verfügbaren Adobe Experience Platform-Zielgruppen aus, wer an der Challenge teilnehmen kann."

Definieren Sie, welche Kundinnen und Kunden an Ihrer Herausforderung der Treue teilnehmen können.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Audience]** und klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**.

   ![](assets/challenge-create-audience.png)

1. Wählen Sie im Dialogfeld für die Zielgruppenauswahl Ihre Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen und wählen Sie **[!UICONTROL Zielgruppe hinzufügen]**. [Erfahren Sie, wie Sie mit Audiences arbeiten](../audience/about-audiences.md).

Ihre Challenge ist jetzt mit Struktur, Inhalt, Messaging und Zielgruppe vollständig konfiguriert. Um ihn zu starten, müssen Sie die Challenge und die zugehörige Journey veröffentlichen.

## Challenge starten {#launch}

Das Starten einer Challenge erfordert **drei Schritte**: (1) Veröffentlichen der Challenge, (2) Generieren der Journey, (3) Veröffentlichen der Journey. Alle drei Punkte müssen erfüllt sein, damit die Herausforderung an die Kunden ausgeliefert werden kann.

1. Überprüfen Sie Ihre Challenge-Konfiguration, um sicherzustellen, dass alle erforderlichen Felder ausgefüllt sind.

1. Klicken Sie auf das Symbol ![](assets/do-not-localize/Smock_More_18_N.svg) und wählen Sie **[!UICONTROL Veröffentlichen]** aus.

   ![](assets/challenge-create-publish.png)

1. Wählen Sie **[!UICONTROL Journey generieren]**, um die Journey zu erstellen, die Ihren Challenge-Versand koordiniert.

   ![](assets/challenge-create-generate-journey.png)

1. Journey Optimizer erstellt automatisch eine Journey im Status „Entwurf“. Die Journey erscheint im Journey-Bestand mit dem Namensformat *&quot;Journey: [Challenge Name]&quot;*. [Erfahren Sie mehr über den Journey-Bestand](../building-journeys/journey-ui.md).

   ![](assets/challenge-create-journey.png)

1. Öffnen Sie die Journey und veröffentlichen Sie sie. Der Journey startet automatisch am angegebenen Startdatum der Challenge und sendet Inhalte und Nachrichten entsprechend Ihrer Konfiguration. [Erfahren Sie, wie Sie eine Journey veröffentlichen](../building-journeys/publish-journey.md).

1. Sobald Ihre Challenge live ist, überwachen Sie Programm-KPIs, Challenge-Ergebnisse und Aufgabenmetriken in den [Treueprogramm-Challenge-Berichten](loyalty-reporting.md). Sie können den Nachrichtenversand auch im Bericht [Journey überwachen](../reports/journey-global-report-cja.md).

>[!NOTE]
>
>Die automatisch generierte Journey kann angepasst werden, um zusätzliche Logik oder Messaging hinzuzufügen. Direkt am Journey vorgenommene Änderungen werden jedoch nicht mit der Challenge-Konfiguration synchronisiert. Wenn Sie die Challenge später bearbeiten, gehen alle Journey-Anpassungen verloren, wenn die Journey neu generiert wird.
