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
source-git-commit: e683461c6adbf45cacb30692e23927175685f9fb
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 1%

---


# Herausforderungen schaffen {#create-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treue aufrufen und verwalten](access-loyalty-challenges.md) - Inventar-, Herausforderungen- und Aufgabenverwaltung
* **Herausforderungen erstellen** ◀︎ **Sie sind hier** - Herausforderungen erstellen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

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

## Konfiguration der Challenge-Struktur {#structure}

Definieren Sie auf **[!UICONTROL Registerkarte]** Struktur“, wie Ihre Herausforderung organisiert ist: Eigenschaften, Zeitplan, abzuschließende Aufgaben und Belohnungen.

### Definieren der Challenge-Eigenschaften und Verwenden benutzerdefinierter Metadaten {#properties}

1. Definieren Sie **[!UICONTROL Bereich &quot;]**&quot; globale Einstellungen für die Herausforderung:

   * **[!UICONTROL Name]**: Geben Sie einen beschreibenden Namen für Ihre Challenge ein. Dieser Name wird im Challenges-Inventar angezeigt.
   * **[!UICONTROL Beschreibung]**: Geben Sie eine Beschreibung ein, die den Zweck und die Ziele der Herausforderung erklärt.

   ![](assets/challenge-create-properties.png)

1. Verwenden Sie den Abschnitt **[!UICONTROL Benutzerdefinierte Metadaten]**, um benutzerdefinierte Metadaten mithilfe von Schlüssel/Wert-Paaren hinzuzufügen. Diese Metadaten können für das Tracking oder die Integration mit externen Systemen verwendet werden.

### Planen der Challenge {#schedule}

Konfigurieren Sie, wann Ihre Challenge ausgeführt wird, indem Sie auf das Symbol **[!UICONTROL Zeitplan öffnen]** klicken:

![](assets/challenge-create-schedule.png)

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

   **[!UICONTROL Anforderung zum Abschluss der Aufgabe]** - Wählen Sie zwischen:

   * **[!UICONTROL Der Kunde wählt eine zu]** Aufgabe aus: Der Kunde kann jede einzelne Aufgabe auswählen und abschließen, um Belohnungen zu erhalten
   * **[!UICONTROL Kunde führt bestimmte Aufgaben aus]**: Kunden müssen eine definierte Anzahl von Aufgaben ausführen. Geben Sie die erforderliche Zahl an - *Beispiel: 3 von 5 Aufgaben erledigen*

   +++

   +++Herausforderungen meistern

   * **[!UICONTROL Streak-]**:

      * **Aufeinander**: Kunden müssen die Aufgabe an aufeinander folgenden Tagen ohne Pausen abschließen - *Beispiel: Kauf am Montag, Dienstag, Mittwoch - ein Tag fehlt, bricht die Pause*

      * **Nicht fortlaufend**: Kunden können die Aufgabe mit Lücken zwischen den Abschlüssen abschließen - *Beispiel: 7 Käufe über 30 Tage abschließen, wobei Pausen zulässig sind*

   * **[!UICONTROL Streak-Länge]**: Geben Sie an, wie oft die Aufgabe abgeschlossen werden muss - *Beispiel: Für eine „7-tägige Kauf-Streak“ auf 7 gesetzt*

   +++

   +++Sequenzielle Herausforderungen

   **[!UICONTROL Anforderung zum Abschluss der Aufgabe]** - Wählen Sie zwischen:

   * **[!UICONTROL Der Kunde wählt eine zu]** Aufgabe aus: Der Kunde kann jede einzelne Aufgabe auswählen und abschließen, um Belohnungen zu erhalten
   * **[!UICONTROL Kunde erledigt bestimmte Aufgaben]**: Kunden müssen eine definierte Anzahl von Aufgaben in der von Ihnen definierten Reihenfolge erledigen. Fehlende oder ausgelassene Aufgaben unterbrechen die Sequenz. Geben Sie die erforderliche Zahl an (z. B. 3 von 5 Aufgaben erledigen).

   *Beispiel: Aufgabe 1 (Kauf) → Aufgabe 2 (Überprüfung) → Aufgabe 3 (Freigabe) - muss in dieser Reihenfolge abgeschlossen sein*

   +++

1. Standardmäßig können Kunden mit standardmäßigen und sequenziellen Herausforderungen Aufgaben über mehrere Transaktionen hinweg ausführen. Um alle Aufgaben in einer Transaktion auszuführen, wählen Sie das Symbol ![](assets/do-not-localize/settings-icon.svg)Einstellungen **[!UICONTROL aus]** aktivieren Sie die Option unten.

   ![](assets/challenge-create-single-transaction.png)

Nachdem Sie Aufgaben zu Ihrer Challenge hinzugefügt haben, konfigurieren Sie die Belohnungen, die Kunden für den Abschluss erhalten.

### Konfigurieren von Belohnungen {#rewards}

Prämien sind die Treuepunkte oder Vorteile, die Kundinnen und Kunden bei der Bewältigung von Herausforderungen erhalten. Konfigurieren Sie, wann und wie Belohnungen bereitgestellt werden.

1. Wählen Sie im Dropdown **[!UICONTROL Versand belohnen]** den Zeitpunkt für die Belohnungsversendung aus:

   * **[!UICONTROL Belohnungen nach Abschluss der Herausforderung bereitstellen]**: Belohnungen erhalten, wenn Kunden die gesamte Herausforderung bewältigen\
     *Beispiel: Vergabe von 100 Punkten nach Abschluss aller 5 Aufgaben*

   * **[!UICONTROL Belohnungen bei Meilensteinen zum Abschluss von Aufgaben bereitstellen, sobald der Fortschritt der Herausforderung erreicht wird]**: Belohnungen werden schrittweise verliehen, sobald Kunden einzelne Aufgaben erledigen (nur für Herausforderungen, die mehr als eine Aufgabe erfordern).\
     *Beispiel: Vergabe von 10 Punkten nach Aufgabe 1, 20 Punkten nach Aufgabe 2 und 50 Punkten nach Aufgabe 3*

1. Wählen Sie Ihren Belohnungsanbieter. Dies ist Ihre Treuelösung, mit der Kundenpunkte und -belohnungen verwaltet werden.

1. Konfigurieren Sie die Belohnungsbeträge basierend auf Ihrer ausgewählten Versandmethode:

   +++Belohnungen nach Abschluss der Challenge bereitstellen

   Geben Sie den Gesamtbelohnungsbetrag an, der gegeben werden soll, wenn Kunden die gesamte Challenge abschließen.

   ![](assets/challenge-create-reward-total.png)

   **Beispiel**: Kunden erhalten 100 Punkte, wenn sie die Challenge abschließen.

   +++

   +++Belohnungen bei Meilensteinen bei Aufgabenabschluss bereitstellen

   Belohnungsbeträge für Meilensteine bei Aufgabenabschluss angeben. Mit dieser Option können Sie progressive Belohnungen schaffen, die die Motivation der Kunden im Laufe der Challenge steigern.

   Schalten Sie für jede Aufgabe, für die Sie eine Belohnung bereitstellen möchten, die Option Belohnung ein und geben Sie an, wie viele Punkte Kunden erhalten sollen, wenn sie diese Aufgabe erfüllen. Sie können festlegen, dass nur bestimmte Aufgabenabschlüsse belohnt werden sollen. Wenn Sie beispielsweise 10 Aufgaben haben, belohnen Sie möglicherweise nur die Aufgaben 1, 5 und 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Beispiel**: Kunden erhalten beim Abschluss der ersten Aufgabe 10 Punkte und nach Abschluss der zweiten Aufgabe 50 zusätzliche Punkte, sodass sich nach Abschluss der Aufgabe insgesamt 60 Punkte ergeben.

   >[!TIP]
   >
   >Erwägen Sie, die Belohnungswerte für spätere Aufgaben zu erhöhen, um die Kundeninteraktion während der gesamten Challenge aufrechtzuerhalten.

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

1. Wählen Sie für jede Phase **[!UICONTROL Phase hinzufügen[] Nachricht]** (wobei [Phase] Launch, In Bearbeitung oder Abschluss darstellt), um eine Nachricht für diese Phase zu erstellen.

1. Wählen Sie den gewünschten Kanal aus: **[!UICONTROL In-App]**, **[!UICONTROL E-Mail]** oder **[!UICONTROL Push-Benachrichtigung]** und wählen Sie die zugehörige Kanalkonfiguration.

1. Klicken Sie auf das ![](assets/do-not-localize/Smock_More_18_N.svg) und wählen Sie **[!UICONTROL Bearbeiten]** aus, um den Nachrichteninhalt zu entwerfen.

   ![](assets/challenge-create-messaging.png)

Erfahren Sie, wie Sie Nachrichten für bestimmte Kanäle erstellen:

* [In-App-Nachrichten](../in-app/get-started-in-app.md)
* [E-Mail-Nachrichten](../email/get-started-email.md)
* [Push-Benachrichtigungen ](../push/get-started-push.md)

Legen Sie nach Abschluss der Messaging-Konfiguration fest, welche Kunden für die Teilnahme an der Challenge infrage kommen.

## Auswählen der Challenge-Audience {#audience}

Definieren Sie, welche Kundinnen und Kunden an Ihrer Herausforderung der Treue teilnehmen können.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Audience]** und wählen Sie die Schaltfläche **[!UICONTROL Audience auswählen]** aus.

   ![](assets/challenge-create-audience.png)

1. Wählen Sie Ihre Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen aus. [Erfahren Sie, wie Sie mit Audiences arbeiten](../audience/about-audiences.md).

1. Wählen Sie **[!UICONTROL Zielgruppe hinzufügen]** aus.

Ihre Challenge ist jetzt mit Struktur, Inhalt, Messaging und Zielgruppe vollständig konfiguriert. Der letzte Schritt besteht darin, die Journey zu generieren und zu veröffentlichen.

## Erstellen und Veröffentlichen der Journey {#review-and-publish}

Generieren Sie die Journey, die Ihren Challenge-Versand und die Kundeninteraktionen koordiniert. Wählen Sie dazu **[!UICONTROL Journey generieren]** aus.

![](assets/challenge-create-generate-journey.png)

Journey Optimizer erstellt automatisch eine [Journey](../building-journeys/journey-gs.md) im Entwurfsstatus. Die automatisch generierte Journey wird in Ihrem Journey-Inventar mit dem Namensformat „Challenge: [Challenge Name]&quot; angezeigt.

![](assets/challenge-create-journey.png)

Überprüfen Sie bei Bedarf die Journey-Konfiguration und veröffentlichen Sie dann die Journey, um die Herausforderung für Kunden verfügbar zu machen. [Erfahren Sie, wie Sie eine Journey veröffentlichen](../building-journeys/publish-journey.md).

Der Journey startet automatisch am angegebenen Startdatum der Challenge und sendet Inhalte und Nachrichten entsprechend Ihrer Konfiguration.

>[!NOTE]
>
>Die automatisch generierte Journey kann angepasst werden, um zusätzliche Logik oder Messaging hinzuzufügen. Direkt am Journey vorgenommene Änderungen werden jedoch nicht mit der Challenge-Konfiguration synchronisiert. Wenn Sie die Challenge später bearbeiten, gehen alle Journey-Anpassungen verloren, wenn die Journey neu generiert wird.
