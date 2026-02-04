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
source-git-commit: e978d075efbbcb42e7500d921bd8cc3ed1eee890
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 1%

---


# Herausforderungen schaffen {#create-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treueprogrammen](access-loyalty-challenges.md) - Inventar und Filterung
* **Herausforderungen erstellen** ◀︎ **Sie sind hier** - Herausforderungen erstellen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren
* [Herausforderungen verwalten](manage-challenges.md) - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Funktionsweise {#how-it-works}

Dieser Workflow ermöglicht das Erstellen und Starten einer Herausforderung zum Treueprogramm:

1. **[Challenge erstellen](#create-the-challenge)** - Wählen Sie den Challenge-Typ (Standard, Streak oder Sequential) aus, der Ihren Zielen im Treueprogramm am besten entspricht.

1. **[Konfiguration der Challenge-Struktur](#structure)** - Definieren Sie die Challenge-Eigenschaften, den Zeitplan, die Aufgaben, die Kundinnen und Kunden abschließen müssen, und die Belohnungen, die sie sammeln werden.

1. **[Konfigurieren von Inhaltskarten](#configure-content-cards)** - Entwerfen Sie Inhaltskarten, um Ihre Herausforderung auf Kundengeräten visuell darzustellen und Challenge-Informationen, Fortschritt und Belohnungen anzuzeigen.

1. **[Messaging konfigurieren](#configure-messaging)** (Optional) - Richten Sie Multi-Channel-Nachrichten (In-App, E-Mail, Push) für die wichtigsten Phasen ein: Start, in Bearbeitung und Abschluss.

1. **[Zielgruppe der Challenge auswählen](#audience)** - Festlegen, welche Kunden für die Challenge geeignet sind.

1. **[Journey generieren und aktivieren](#review-and-publish)** - Generieren Sie die zugehörige Journey und aktivieren Sie sie, um die Challenge für Ihre Audience verfügbar zu machen.

## Herausforderung erstellen {#create-the-challenge}

1. Navigieren Sie zu **[!UICONTROL Herausforderungen zum Treueprogramm (Beta]** in Journey Optimizer.

1. Wählen Sie die Registerkarte **[!UICONTROL Herausforderungen]** und wählen Sie **[!UICONTROL Herausforderung erstellen]**.

   ![](assets/challenge-create.png)

1. Wählen Sie den Challenge-Typ:

   * **[!UICONTROL Standard]**: Kunden führen eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus
   * **[!UICONTROL Streak]**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus
   * **[!UICONTROL Sequenziell]**: Kunden führen Aufgaben in einer definierten Reihenfolge aus

## Konfiguration der Challenge-Struktur {#structure}

Definieren Sie auf der Registerkarte Struktur , wie Ihre Herausforderung organisiert ist: Eigenschaften, Zeitplan, abzuschließende Aufgaben und Belohnungen.

### Definieren der Challenge-Eigenschaften und Verwenden benutzerdefinierter Metadaten {#properties}

1. Definieren Sie im Bereich Challenge-Eigenschaften die Challenge-Einstellungen:

   ![](assets/challenge-create-properties.png)

   **Name**: Geben Sie einen beschreibenden Namen für Ihre Challenge ein. Dieser Name wird im Challenges-Inventar angezeigt.

   **Beschreibung**: Geben Sie eine Beschreibung ein, in der der Zweck und die Ziele der Herausforderung erläutert werden.

1. Verwenden Sie den Abschnitt **[!UICONTROL Benutzerdefinierte Metadaten]**, um benutzerdefinierte Metadaten mithilfe von Schlüssel/Wert-Paaren hinzuzufügen. Diese Metadaten können für das Tracking, die Segmentierung oder die Integration mit externen Systemen verwendet werden.

### Planen der Challenge {#schedule}

Konfigurieren Sie, wann Ihre Challenge ausgeführt wird, indem Sie auf das ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Zeitplan öffnen]** klicken:

* **Startdatum und -uhrzeit**: Festlegen, wann die Challenge für Kunden verfügbar sein soll

* **Enddatum und -uhrzeit**: Legt fest, wann die Challenge abläuft und keine neuen Abschlüsse mehr akzeptiert

* **Zeitzone**: Die Challenge verwendet standardmäßig die lokale Zeitzone des Empfängers

* **Aufgaben müssen abgeschlossen sein**: Wählen Sie aus, wann Kunden Aufgaben abschließen können:

   * **[!UICONTROL Zu jeder Zeit während der Herausforderung]**: Kunden können Aufgaben jederzeit zwischen dem Start- und dem Enddatum der Herausforderung abschließen
   * **[!UICONTROL Während bestimmter Tageszeiten:]** Sie den Aufgabenabschluss auf bestimmte tägliche Stunden ein, indem Sie die Zeiten **[!UICONTROL Startzeit]** und **[!UICONTROL Endzeit“]**

Der Zeitplan für die Challenge ist jetzt konfiguriert. Sie können jetzt die Aufgaben hinzufügen, die Kunden abschließen müssen.

### Aufgaben hinzufügen {#add-tasks}

Aufgaben definieren die spezifischen Aktionen, die Kunden durchführen müssen, um Belohnungen zu erhalten. Sie können Aufgabentypen (Einkauf, Ausgaben), Mengen, Produktfilter und andere Attribute konfigurieren.

Je nach Challenge-Typ führen Kundinnen und Kunden Aufgaben unterschiedlich aus:

* **Standardherausforderungen**: Führen Sie eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus\
  *Beispiel: 3 von 5 Aufgaben erledigen - einen Kauf tätigen, eine Bewertung schreiben, einen Freund verweisen, in sozialen Medien teilen oder Profil aktualisieren*

* **Streak Challenges**: Dieselbe Aufgabe mehrmals hintereinander ausführen\
  *Beispiel: Tätigen Sie einen Kauf an 7 aufeinander folgenden Tagen, um Bonusprämien zu erhalten*

* **Sequenzielle Herausforderungen**: Aufgaben in einer definierten Reihenfolge erledigen\
  *Beispiel: Zuerst einen Kauf tätigen, dann eine Bewertung schreiben und dann in den sozialen Medien teilen - Aufgaben müssen in dieser exakten Reihenfolge erledigt sein*

Gehen Sie wie folgt vor, um Ihrer Herausforderung Aufgaben hinzuzufügen:

1. Wählen Sie **[!UICONTROL Abschnitt]** Aufgaben“ **[!UICONTROL Aufgabe hinzufügen]** aus.

   ![](assets/challenge-create-add-task.png)

1. Das Aufgabeninventar wird geöffnet. Wählen Sie eine oder mehrere Aufgaben aus der Liste aus und klicken Sie auf **[!UICONTROL Hinzufügen]**. Um eine neue Aufgabe zu erstellen, wählen Sie **[!UICONTROL Neu]** aus.

   [Erfahren Sie, wie Sie Aufgaben erstellen und konfigurieren](create-tasks.md).

1. Geben Sie im Abschnitt **[!UICONTROL Anforderung für Aufgabenabschluss]** an, wann die Herausforderung als abgeschlossen gilt:

   * **[!UICONTROL Der Kunde wählt eine zu]** Aufgabe aus: Der Kunde kann jede einzelne Aufgabe auswählen und abschließen, um Belohnungen zu erhalten
   * **[!UICONTROL Kunde führt bestimmte Aufgaben aus]**: Kunden müssen eine definierte Anzahl von Aufgaben ausführen. Geben Sie die erforderliche Zahl an.

1. Herausforderungen ermöglichen es Kunden standardmäßig, Aufgaben über mehrere Transaktionen hinweg auszuführen. Um alle Aufgaben in einer Transaktion auszuführen, wählen Sie das Symbol ![](assets/do-not-localize/settings-icon.svg)**[!UICONTROL Einstellungen]** und schalten Sie die Option **[!UICONTROL Einzelne Transaktion]** um.

   ![](assets/challenge-create-single-transaction.png)

### Konfigurieren von Belohnungen {#rewards}

Prämien sind die Treuepunkte oder Vorteile, die Kundinnen und Kunden bei der Bewältigung von Herausforderungen erhalten. Konfigurieren Sie, wann und wie Belohnungen bereitgestellt werden.

1. Wählen Sie im Dropdown **[!UICONTROL Versand belohnen]** den Zeitpunkt für die Belohnungsversendung aus:

   * **[!UICONTROL Belohnungen nach Abschluss der Herausforderung bereitstellen]**: Belohnungen erhalten, wenn Kunden die gesamte Herausforderung bewältigen
   * **[!UICONTROL Belohnungen bei Meilensteinen zum Abschluss von Aufgaben bereitstellen, sobald der Fortschritt der Herausforderung erreicht wird]**: Belohnungen werden schrittweise verliehen, sobald Kunden einzelne Aufgaben erledigen (nur für Herausforderungen, die mehr als eine Aufgabe erfordern).

1. Wählen Sie Ihren **[!UICONTROL Belohnungsanbieter]** aus dem Dropdown-Menü aus. Dies ist Ihre Treuelösung, mit der Kundenpunkte und -belohnungen verwaltet werden.

1. Konfigurieren Sie die Belohnungsbeträge basierend auf Ihrer ausgewählten Versandmethode:

   +++Belohnungen nach Abschluss der Challenge bereitstellen

   Geben Sie im Feld **Anzahl der [Treuepunkte] bei Abschluss der** den Gesamtbelohnungsbetrag an, der gegeben werden soll, wenn die Kundinnen und Kunden die gesamte Herausforderung abschließen.

   Der Feldname zeigt den Namen Ihrer Treuepunkte wie im ausgewählten Anbieter definiert an. Wenn Ihr Provider beispielsweise „Luma-Punkte“ verwendet, wird im Feld „Anzahl der Luma-Punkte nach Abschluss der Herausforderung“ angezeigt.

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

>[!NOTE]
>
>Die Herausforderungen bezüglich der Treue umfassen kein integriertes Sachkontensystem zur Verfolgung von Belohnungssalden. Stellen Sie sicher, dass Ihr ausgewählter Belohnungsanbieter Punktverfolgung und -einlösung übernimmt.

Die Challenge-Struktur ist jetzt mit Aufgaben und Belohnungen konfiguriert. Sie können jetzt die Inhaltskarten entwerfen, um den Kunden die Herausforderung anzuzeigen.

## Konfigurieren von Inhaltskarten {#configure-content-cards}

Inhaltskarten stellen Ihre Herausforderung auf Kundengeräten visuell dar und zeigen Informationen zur Herausforderung, den Fortschritt und die Belohnungen an. [Weitere Informationen zu Inhaltskarten](../content-card/create-content-card.md).

So konfigurieren Sie Inhaltskarten für Ihre Challenge:

1. Navigieren Sie zur Registerkarte **[!UICONTROL Inhalt]** .

1. Geben Sie **[!UICONTROL Inhaltskarte]** Name“ ein.

1. Wählen Sie die **[!UICONTROL Kanalkonfiguration]**. Kanalkonfigurationen enthalten alle technischen Parameter zum Senden der Nachricht, z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Weitere Informationen zu Kanalkonfigurationen](../configuration/channel-surfaces.md).

1. Wählen Sie **[!UICONTROL Inhalt bearbeiten]** aus, um Ihre Inhaltskarte zu entwerfen.

   ![](assets/challenge-create-content.png)

[Erfahren Sie, wie Sie Inhaltskarten entwerfen und personalisieren](../content-card/design-content-card.md).

Die Inhaltskarte ist jetzt konfiguriert. Sie können jetzt Messaging einrichten, um Kunden während des gesamten Challenge-Lebenszyklus anzusprechen.

### Konfigurieren von Messaging {#configure-messaging}

Richten Sie Multi-Channel-Nachrichten ein, um Kunden in wichtigen Phasen des Challenge-Lebenszyklus anzusprechen. Messaging ist optional, wird aber zur Maximierung der Kundeninteraktion empfohlen.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Messaging]**.

1. Konfigurieren Sie Nachrichten für jede Lebenszyklusphase:

   ![](assets/challenge-create-messaging.png)

   * **Launch**-Nachricht: Kunden benachrichtigen, wenn die Herausforderung beginnt
   * **In Bearbeitung** Nachricht: Halten Sie Kunden mit Erinnerungen und Fortschrittsaktualisierungen in Verbindung
   * **Completion** Nachricht: Erfolg feiern und Zuweisung der Belohnung bestätigen

1. Wählen Sie für jede Phase **[!UICONTROL Phase hinzufügen *Nachricht* aus,]** eine Nachricht für diese Phase zu erstellen.

1. Wählen Sie den gewünschten Kanal aus: **[!UICONTROL In-App]**, **[!UICONTROL E-Mail]** oder **[!UICONTROL Push-Benachrichtigung]** und wählen Sie die zugehörige Kanalkonfiguration.

1. Klicken Sie auf das ![](assets/do-not-localize/Smock_More_18_N.svg) und wählen Sie **[!UICONTROL Bearbeiten]** aus, um den Nachrichteninhalt zu entwerfen.

   Erfahren Sie, wie Sie Nachrichten für bestimmte Kanäle erstellen:

   * [Erfahren Sie, wie Sie In-App-Nachrichten erstellen](../in-app/get-started-in-app.md)
   * [Erfahren Sie, wie Sie E-Mail-Nachrichten erstellen](../email/get-started-email.md)
   * [Erfahren Sie, wie Sie Push-Benachrichtigungen erstellen.](../push/get-started-push.md)

1. Wiederholen Sie diese Schritte für jede Phase und jeden Kanal nach Bedarf.

Die Messaging-Konfiguration ist jetzt abgeschlossen. Jetzt können Sie festlegen, welche Kunden für die Teilnahme an der Challenge infrage kommen.

## Auswählen der Challenge-Audience {#audience}

Definieren Sie, welche Kundinnen und Kunden an Ihrer Herausforderung der Treue teilnehmen können.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Audience]** und wählen Sie **[!UICONTROL Audience auswählen]** aus.

   ![](assets/challenge-create-audience.png)

1. Wählen Sie Ihre Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen aus.

1. Wählen Sie **[!UICONTROL Zielgruppe hinzufügen]** aus.

Ihre Challenge-Konfiguration ist jetzt abgeschlossen. Sie können jetzt die Journey generieren, die den Challenge-Versand koordiniert.

## Journey erzeugen und aktivieren {#review-and-publish}

Wenn Ihre Challenge-Konfiguration abgeschlossen ist, generieren Sie die zugehörige Journey, die den Challenge-Versand und die Kundeninteraktionen koordiniert. Wählen Sie dazu **[!UICONTROL Journey generieren]** aus.

![](assets/challenge-create-generate-journey.png)

Journey Optimizer erstellt automatisch eine [Journey](../building-journeys/journey-gs.md) im Entwurfsstatus. Die automatisch generierte Journey wird in Ihrem Journey-Inventar mit dem Namensformat „Challenge: [Challenge Name]&quot; angezeigt.

Überprüfen Sie bei Bedarf die Journey-Konfiguration und [&#x200B; Sie dann die Journey &#x200B;](../building-journeys/publish-journey.md), um die Herausforderung für Kunden verfügbar zu machen.

Der Journey startet automatisch am angegebenen Startdatum der Challenge und sendet Inhalte und Nachrichten entsprechend Ihrer Konfiguration.

>[!NOTE]
>
>Die automatisch generierte Journey kann angepasst werden, um zusätzliche Logik oder Messaging hinzuzufügen. Direkt am Journey vorgenommene Änderungen werden jedoch nicht mit der Challenge-Konfiguration synchronisiert. Wenn Sie die Challenge später bearbeiten, gehen alle Journey-Anpassungen verloren, wenn die Journey neu generiert wird.

## Nächste Schritte {#next-steps}

* [Herausforderungen verwalten](manage-challenges.md) - Herausforderungen bearbeiten, überwachen und optimieren
