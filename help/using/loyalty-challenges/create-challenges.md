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
hidefromtoc: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
source-git-commit: 94b553b19dbb0ba3020979fa710c2c35af237816
workflow-type: tm+mt
source-wordcount: '1501'
ht-degree: 1%

---


# Herausforderungen schaffen {#create-challenges}

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Zugriff und Verwaltung von Herausforderungen und Aufgaben](access-loyalty-challenges.md) - Inventar-, Challenge- und Aufgabenverwaltung
* **Herausforderungen erstellen** ◀︎ **Sie sind hier** - Herausforderungen erstellen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren

>[!ENDSHADEBOX]

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

   Nach Auswahl eines Challenge-Typs wird die Benutzeroberfläche zur Challenge-Erstellung mit mehreren Konfigurations-Registerkarten geöffnet. Beginnen Sie mit der Konfiguration der Challenge-Struktur.

## Konfiguration der Challenge-Struktur {#structure}

Definieren Sie auf **[!UICONTROL Registerkarte]** Struktur“, wie Ihre Herausforderung organisiert ist: Eigenschaften, Zeitplan, abzuschließende Aufgaben und Belohnungen.

### Definieren der Challenge-Eigenschaften und Verwenden benutzerdefinierter Metadaten {#properties}

1. Definieren Sie **[!UICONTROL Bereich &quot;]**&quot; globale Einstellungen für die Herausforderung:

   * **[!UICONTROL Name]**: Geben Sie einen beschreibenden Namen für Ihre Challenge ein. Dieser Name wird im Challenges-Inventar angezeigt.
   * **[!UICONTROL Beschreibung]**: Geben Sie eine Beschreibung ein, die den Zweck und die Ziele der Herausforderung erklärt.

1. Verwenden Sie den Abschnitt **[!UICONTROL Benutzerdefinierte Metadaten]**, um benutzerdefinierte Metadaten mithilfe von Schlüssel/Wert-Paaren hinzuzufügen. Diese Metadaten können für das Tracking oder die Integration mit externen Systemen verwendet werden.

   ![](assets/challenge-create-properties.png)

### Planen der Challenge {#schedule}

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

Aufgaben definieren die spezifischen Aktionen, die Kunden durchführen müssen, um Belohnungen zu erhalten. Sie können Aufgabentypen (Einkauf, Ausgaben), Mengen, Produktfilter und andere Attribute konfigurieren.

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

### Konfigurieren von Belohnungen {#rewards}

Prämien sind die Treuepunkte oder Vorteile, die Kundinnen und Kunden bei der Bewältigung von Herausforderungen erhalten.

So konfigurieren Sie, wann und wie Belohnungen bereitgestellt werden:

1. Wählen Sie im Dropdown **[!UICONTROL Menü]** Belohnungsversand“ aus, wann Belohnungen bereitgestellt werden sollen:

   * **[!UICONTROL Belohnungen nach Abschluss der Herausforderung bereitstellen]**: Belohnungen erhalten, wenn Kunden die gesamte Herausforderung bewältigen\
     *Beispiel: Vergabe von 100 Punkten nach Abschluss aller 5 Aufgaben*

   * **[!UICONTROL Belohnungen bei Meilensteinen zum Abschluss von Aufgaben bereitstellen, sobald der Fortschritt der Herausforderung erreicht wird]**: Belohnungen werden schrittweise verliehen, sobald Kunden einzelne Aufgaben erledigen (nur für Herausforderungen, die mehr als eine Aufgabe erfordern).\
     *Beispiel: Vergabe von 10 Punkten nach Aufgabe 1, 20 Punkten nach Aufgabe 2 und 50 Punkten nach Aufgabe 3*

1. Wählen Sie Ihren Belohnungsanbieter. Dies ist Ihre Treuelösung, mit der Kundenpunkte und -belohnungen verwaltet werden.

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

Inhaltskarten stellen Ihre Herausforderung auf Kundengeräten visuell dar und zeigen Informationen zur Herausforderung, den Fortschritt und die Belohnungen an. [Weitere Informationen zu Inhaltskarten](../content-card/create-content-card.md).

So konfigurieren Sie Inhaltskarten für Ihre Challenge:

1. Navigieren Sie zur Registerkarte **[!UICONTROL Inhalt]** und geben Sie einen **[!UICONTROL Namen]** für die Inhaltskarte ein.

1. Wählen Sie die **[!UICONTROL Kanalkonfiguration]**. Kanalkonfigurationen enthalten alle technischen Parameter zum Senden von Nachrichten, z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Weitere Informationen zu Kanalkonfigurationen](../configuration/channel-surfaces.md).

1. Wählen Sie **[!UICONTROL Inhalt bearbeiten]** aus, um Ihre Inhaltskarte zu entwerfen. [Erfahren Sie, wie Sie Inhaltskarten entwerfen und personalisieren](../content-card/design-content-card.md).

   ![](assets/challenge-create-content.png)

Richten Sie nach der Konfiguration der Inhaltskarte Messaging ein, um Kunden während des gesamten Challenge-Lebenszyklus anzusprechen.

### Konfigurieren von Messaging {#configure-messaging}

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

## Auswählen der Challenge-Audience {#audience}

Definieren Sie, welche Kundinnen und Kunden an Ihrer Herausforderung der Treue teilnehmen können.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Audience]** und klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**.

   ![](assets/challenge-create-audience.png)

1. Wählen Sie im Dialogfeld für die Zielgruppenauswahl Ihre Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen und wählen Sie **[!UICONTROL Zielgruppe hinzufügen]**. [Erfahren Sie, wie Sie mit Audiences arbeiten](../audience/about-audiences.md).

Ihre Challenge ist jetzt mit Struktur, Inhalt, Messaging und Zielgruppe vollständig konfiguriert. Der letzte Schritt besteht darin, die Journey zu generieren und zu veröffentlichen.

## Erstellen und Veröffentlichen der Journey {#review-and-publish}

Generieren Sie nach der Konfiguration aller Challenge-Komponenten die Journey, die Ihren Challenge-Versand koordiniert:

1. Überprüfen Sie Ihre Challenge-Konfiguration, um sicherzustellen, dass alle erforderlichen Felder ausgefüllt sind.

1. Wählen Sie **[!UICONTROL Speichern]**, um Ihre Challenge-Konfiguration zu speichern, und wählen Sie **[!UICONTROL Journey generieren]**.

   ![](assets/challenge-create-generate-journey.png)

1. Journey Optimizer erstellt automatisch eine Journey im Status „Entwurf“. Die automatisch generierte Journey wird in Ihrem Journey-Inventar mit dem Namensformat *&quot;Journey: [Challenge Name]&quot;* angezeigt. [Erfahren Sie mehr über den Journey-Bestand](../building-journeys/journey-ui.md).

   ![](assets/challenge-create-journey.png)

1. Wenn Sie bereit sind, veröffentlichen Sie die Journey, um die Herausforderung für Kunden verfügbar zu machen. Der Journey startet automatisch am angegebenen Startdatum der Challenge und sendet Inhalte und Nachrichten entsprechend Ihrer Konfiguration. [Erfahren Sie, wie Sie eine Journey veröffentlichen](../building-journeys/publish-journey.md).

>[!NOTE]
>
>Die automatisch generierte Journey kann angepasst werden, um zusätzliche Logik oder Messaging hinzuzufügen. Direkt am Journey vorgenommene Änderungen werden jedoch nicht mit der Challenge-Konfiguration synchronisiert. Wenn Sie die Challenge später bearbeiten, gehen alle Journey-Anpassungen verloren, wenn die Journey neu generiert wird.
