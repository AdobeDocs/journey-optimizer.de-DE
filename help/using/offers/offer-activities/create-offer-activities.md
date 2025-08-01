---
title: Erstellen von Entscheidungen
description: Erfahren Sie, wie Sie Entscheidungen erstellen
badge: label="Legacy" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: fb036e910431a4ce9709b394c93484e6b76bf8f8
workflow-type: tm+mt
source-wordcount: '2549'
ht-degree: 96%

---

# Erstellen von Entscheidungen {#create-offer-activities}

Entscheidungen sind Container für Ihre Angebote, die die Offer-Decisioning-Engine nutzen, um das beste Angebot auszuwählen, das je nach Zielgruppe des Versandes unterbreitet werden kann.

➡️ [In diesem Video erfahren Sie, wie Sie Angebotsaktivitäten erstellen](#video)

Die Liste der Entscheidungen ist im Menü **[!UICONTROL Angebote]** auf der Registerkarte **[!UICONTROL Entscheidungen]** verfügbar. Es gibt Filter, mit denen Sie Entscheidungen anhand von Status oder Anfangs- und Enddatum abrufen können.

![](../assets/activities-list.png)

Bevor Sie eine Entscheidung erstellen, prüfen Sie, ob die folgenden Komponenten in der Angebotsbibliothek erstellt wurden:

* [Platzierungen](../offer-library/creating-placements.md)
* [Sammlungen](../offer-library/creating-collections.md)
* [Personalisierte Angebote](../offer-library/creating-personalized-offers.md)
* [Fallback-Angebote](../offer-library/creating-fallback-offers.md)

## Erstellen einer Entscheidung {#create-activity}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_details"
>title="Details zur Angebotsentscheidung"
>abstract="Geben Sie den Namen der Entscheidung ein und legen Sie bei Bedarf ein Start- und Enddatum fest. Um der Entscheidung benutzerdefinierte oder Core-Datennutzungs-Labels zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]**."

1. Rufen Sie die Entscheidungsliste auf und klicken Sie dann auf **[!UICONTROL Entscheidung erstellen]**.

1. Geben Sie den Namen der Entscheidung an.

1. Legen Sie gegebenenfalls ein Start- und Enddatum sowie eine Uhrzeit fest und klicken Sie dann auf **[!UICONTROL Weiter]**.

   ![](../assets/activities-name.png)

1. Um der Entscheidung benutzerdefinierte oder Core-Datennutzungs-Labels zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]**. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (Object Level Access Control, OLAC)](../../administration/object-based-access.md)

## Definieren von Entscheidungsumfängen {#add-decision-scopes}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_scopes"
>title="Entscheidungsumfänge"
>abstract="Konfigurieren Sie einen oder mehrere Umfänge für die Angebotsentscheidung, um festzulegen, welche Angebote angezeigt werden. Wählen Sie hierzu eine Platzierung und ein zugehöriges Auswertungskriterium für diese Platzierung aus."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_placement"
>title="Platzierung"
>abstract="Platzierung wählen, in der die Angebote unterbreitet werden sollen."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_evaluation"
>title="Auswertungskriterien"
>abstract="Auswertungskriterien bestehen aus einer Angebotssammlung, die mit einer Eignungsbegrenzung verknüpft ist, und einer Ranking-Methode, mit der die in der Platzierung anzuzeigenden Angebote bestimmt werden.  Die Abfolge der Auswertungskriterien bestimmt, welche Sammlung zuerst bewertet wird. Es ist mindestens ein Auswertungskriterium erforderlich."

1. Wählen Sie eine Platzierung aus der Dropdown-Liste aus. Sie wird zum ersten Entscheidungsumfang in Ihrer Entscheidung hinzugefügt.

   ![](../assets/activities-placement.png)

1. Klicken Sie auf **[!UICONTROL Hinzufügen]**, um Auswertungskriterien für diese Platzierung auszuwählen.

   ![](../assets/activities-evaluation-criteria.png)

   Jedes Kriterium besteht aus einer Angebotssammlung, die mit einer Eignungsbegrenzung verknüpft ist, und einer Ranking-Methode, mit der die in der Platzierung anzuzeigenden Angebote bestimmt werden.

   >[!NOTE]
   >
   >Es ist mindestens ein Auswertungskriterium erforderlich.

1. Wählen Sie die Angebotssammlung aus, die die zu berücksichtigenden Angebote enthält, und klicken Sie anschließend auf **[!UICONTROL Hinzufügen]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >Sie können auf den Link **[!UICONTROL Angebotskollektionen öffnen]** klicken, um die Liste der Sammlungen in einer neuen Registerkarte anzuzeigen, wo Sie die Sammlungen und die darin enthaltenen Angebote durchsuchen können.

   Die ausgewählte Sammlung wird den Kriterien hinzugefügt.

   ![](../assets/activities-collection-added.png)

1. Verwenden Sie das Feld **[!UICONTROL Eignung]**, um die Auswahl der Angebote für diese Platzierung zu beschränken.

   Diese Einschränkung kann mithilfe einer **Entscheidungsregel** oder einer oder mehrerer **Adobe Experience Platform-Zielgruppen** angewendet werden. Beides wird in [diesem Abschnitt](../offer-library/add-constraints.md#segments-vs-decision-rules) genauer beschrieben.

   * Um die Auswahl der Angebote auf die Mitglieder einer Experience Platform-Zielgruppe zu beschränken, wählen Sie **[!UICONTROL Zielgruppen]** aus und klicken Sie dann auf **[!UICONTROL Zielgruppen hinzufügen]**.

     ![](../assets/activity_constraint_segment.png)

     Fügen Sie eine oder mehrere Zielgruppen aus dem linken Bereich hinzu und kombinieren Sie diese mithilfe der logischen Operatoren **[!UICONTROL Und]**/**[!UICONTROL Oder]**.

     ![](../assets/activity_constraint_segment2.png)

     Weitere Informationen zum Arbeiten mit Zielgruppen finden Sie in [diesem Abschnitt](../../audience/about-audiences.md).

   * Wenn Sie eine Auswahlbegrenzung mit einer Entscheidungsregel hinzufügen möchten, verwenden Sie die Option **[!UICONTROL Entscheidungsregel]** und wählen Sie die gewünschte Regel aus.

     ![](../assets/activity_constraint_rule.png)

     Weiterführende Informationen zum Erstellen einer Entscheidungsregel finden Sie in [diesem Abschnitt](../offer-library/creating-decision-rules.md).

1. Wenn Sie Zielgruppen oder Entscheidungsregeln auswählen, können Sie Informationen zur geschätzten Anzahl der qualifizierten Profile sehen. Klicken Sie auf **[!UICONTROL Aktualisieren]**, um diese Daten zu aktualisieren.

   >[!NOTE]
   >
   >Profilschätzungen sind nicht verfügbar, wenn Regelparameter Daten enthalten, die nicht im Profil enthalten sind, z. B. Kontextdaten. Beispielsweise eine Eignungsregel, für die die aktuelle Temperatur höher als 25 °C sein muss.

   ![](../assets/activity_constraint-estimate.png)

1. Definieren Sie die Rangfolgenmethode, die Sie zur Auswahl des besten Angebots für jedes Profil verwenden möchten. [Weitere Informationen](../offer-activities/configure-offer-selection.md).

   ![](../assets/activity_ranking-method.png)

   * Wenn mehrere Angebote für diese Platzierung infrage kommen, verwendet die Methode **[!UICONTROL Angebotspriorität]** den in den Angeboten definierten Wert: Das Angebot mit der höchsten Priorität wird an die Benutzerin oder den Benutzer gesendet.

   * Wenn Sie ein bestimmtes berechnetes Ergebnis verwenden möchten, um zu entscheiden, welches geeignete Angebot geliefert werden soll, wählen Sie **[!UICONTROL Formel]** oder **[!UICONTROL KI-Modell]**. [Weitere Informationen](../offer-activities/configure-offer-selection.md).

1. Klicken Sie auf **[!UICONTROL Hinzufügen]**, um weitere Kriterien für dieselbe Platzierung zu definieren.

   ![](../assets/activity_add-collection.png)

1. Wenn Sie mehrere Kriterien hinzufügen, werden diese in einer bestimmten Reihenfolge ausgewertet. Die erste Sammlung, die der Sequenz hinzugefügt wurde, wird zuerst ausgewertet usw. [Weitere Informationen](#evaluation-criteria-order)

   Um die Standardsequenz neu anzuordnen, können Sie die Sammlungen per Drag-and-drop nach Bedarf verschieben.

   ![](../assets/activity_reorder-collections.png)

1. Sie können außerdem mehrere Kriterien gleichzeitig auswerten. Ziehen Sie dazu die Kollektion per Drag-and-drop auf eine andere Sammlung.

   ![](../assets/activity_move-collection.png)

   Sie haben nun denselben Rang und werden daher gleichzeitig ausgewertet. [Weitere Informationen](#evaluation-criteria-order)

   ![](../assets/activity_same-rank-collections.png)

   >[!CAUTION]
   >
   >* Bei der Verwendung eines [KI-Modells](../ranking/ai-models.md) in einer Gruppe von Bewertungskriterien müssen alle Bewertungskriterien in dieser Gruppe die KI-Rangfolgenmethode und dasselbe spezifische KI-Modell verwenden.
   >
   >* Nur eine der Bewertungskriterien-Gruppen kann das KI-Modell verwenden. Alle anderen Gruppen innerhalb eines Entscheidungsumfangs müssen andere Ranglistenmethoden verwenden (Priorität oder Formel). [Weitere Informationen zu Ranglistenmethoden](../offer-activities/configure-offer-selection.md)

1. Um im Rahmen dieser Entscheidung eine weitere Platzierung für Ihre Angebote hinzuzufügen, verwenden Sie die Schaltfläche **[!UICONTROL Neuer Umfang]**. Wiederholen Sie für jeden Entscheidungsumfang die obigen Schritte.

   ![](../assets/activity_new-scope.png)

   >[!NOTE]
   >
   >Beim Hinzufügen mehrerer Entscheidungsumfänge wird die Reihenfolge der Auswertungskriterien beeinflusst. [Weitere Informationen](#multiple-scopes)

### Reihenfolge der Auswertungskriterien {#evaluation-criteria-order}

Wie oben beschrieben bestehen Auswertungskriterien aus einer Sammlung, Eignungsbegrenzungen und einer Ranking-Methode. Sie können die sequenzielle Reihenfolge festlegen, in der die Auswertungskriterien angewendet werden sollen. Sie können aber auch mehrere Auswertungskriterien kombinieren, sodass sie zusammen und nicht getrennt angewendet werden.

#### Mit nur einem Umfang {#one-scope}

Innerhalb eines einzigen Entscheidungsumfangs bestimmen mehrere Kriterien und ihre Gruppierung die Priorität der Kriterien und die Rangfolge der geeigneten Angebote. Das erste Kriterium hat die höchste Priorität und die Kriterien, die in derselben „Gruppe“ zusammengefasst sind, haben die gleiche Priorität.

Sie haben beispielsweise zwei Sammlungen – eine im Auswertungskriterium A und eine im Auswertungskriterien B. Die Anfrage sieht die Rücksendung von zwei Angeboten vor. Angenommen, es gibt zwei geeignete Angebote nach Auswertungskriterium A und drei geeignete Angebote nach Auswertungskriterium B.

* Wenn die beiden Auswertungskriterien **nicht kombiniert** und/oder in sequenzieller Reihenfolge (1 und 2) sind, werden die beiden geeignetsten Angebote aus den Auswertungskriterien in der ersten Zeile angezeigt. Gibt es für das erste Auswertungskriterium keine zwei geeigneten Angebote, geht die Entscheidungs-Engine zum nächsten Auswertungskriterium in der Reihenfolge über, um so viele Angebote zu finden, wie noch benötigt werden, und gibt schließlich bei Bedarf ein Fallback zurück.

  ![](../assets/activity_consecutive-rank-collections.png)

* Werden die beiden Sammlungen **gleichzeitig bewertet**, da es zwei geeignete Angebote nach Bewertungskriterien A und drei geeignete Angebote nach Bewertungskriterien B gibt, werden die fünf Angebote auf der Grundlage des von den jeweiligen Bewertungsmethoden ermittelten Wertes alle gemeinsam in eine Rangfolge gebracht. Es werden zwei Angebote angefordert, so dass von diesen fünf Angeboten die beiden geeignetsten zurückgegeben werden.

  ![](../assets/activity_same-rank-collections.png)

+++ **Beispiel mit mehreren Kriterien**

Betrachten wir nun ein Beispiel, bei dem mehrere Kriterien für einen einzelnen Umfang in verschiedene Gruppen unterteilt sind.

Sie haben drei Kriterien definiert. Die Kriterien 1 und 2 befinden sich beide in Gruppe 1, während Kriterium 3 unabhängig ist (Gruppe 2).

Die geeigneten Angebote für jedes Kriterium und ihre Priorität (die bei der Auswertung der Ranglistenfunktion verwendet wird) sind wie folgt:

* Gruppe 1:
   * Kriterium 1 – (Angebot 1, Angebot 2, Angebot 3) – Priorität 1
   * Kriterium 2 – (Angebot 3, Angebot 4, Angebot 5) – Priorität 1

* Gruppe 2:
   * Kriterium 3 – (Angebot 5, Angebot 6) – Priorität 0

Die Angebote mit der höchsten Priorität werden zuerst ausgewertet und der Ranking-Liste der Angebote hinzugefügt.

**Iteration 1:**

Angebote mit Kriterium 1 und Kriterium 2 werden gemeinsam ausgewertet (Angebot 1, Angebot 2, Angebot 3, Angebot 4, Angebot 5). Nehmen wir an, das Ergebnis lautet:

Angebot 1 - 10
Angebot 2 - 20
Angebot 3 - 30 aus Kriterium 1, 45 aus Kriterium 2. Der höchste Wert von beiden wird berücksichtigt, also 45.
Angebot 4 - 40
Angebot 5 - 50

Die Rangfolge der Angebote ist nun wie folgt: Angebot 5, Angebot 3, Angebot 4, Angebot 2, Angebot 1.

**Iteration 2:**

Angebote mit Kriterium 3 werden ausgewertet (Angebot 5, Angebot 6). Nehmen wir an, das Ergebnis lautet:

* Angebot 5 - wird nicht ausgewertet, da es bereits im obigen Ergebnis enthalten ist.
* Angebot 6 - 60

Die Rangfolge der Angebote ist nun wie folgt: Angebot 5, Angebot 3, Angebot 4, Angebot 2, Angebot 1, Angebot 6.

+++

#### Mit mehreren Umfängen {#multiple-scopes}

**Wenn die Duplizierung deaktiviert ist**

Wenn Sie einer Entscheidung mehrere Entscheidungsumfänge hinzufügen und keine Duplizierung zwischen Platzierungen zulässig ist, werden die geeigneten Angebote nacheinander in der Reihenfolge der Entscheidungsumfänge in der Anfrage ausgewählt.

>[!NOTE]
>
>Der Parameter **[!UICONTROL Duplikate über Platzierungen hinweg zulassen]** wird auf der Platzierungsebene festgelegt. Wenn die Duplizierung bei einer Platzierung in einer Entscheidungsanfrage auf „false“ gesetzt ist, übernehmen alle Platzierungen in der Anfrage die Einstellung „false“. [Weitere Informationen zu Duplizierungsparametern](../offer-library/creating-placements.md)

Nehmen wir ein Beispiel, in dem Sie zwei Entscheidungsumfänge hinzugefügt haben, z. B.:

* Umfang 1: Es gibt vier geeignete Angebote (Angebot 1, Angebot 2, Angebot 3, Angebot 4) und die Anfrage lautet, dass zwei Angebote zurückgeschickt werden sollen.
* Umfang 2: Es gibt vier geeignete Angebote (Angebot 1, Angebot 2, Angebot 3, Angebot 4) und die Anfrage lautet, dass zwei Angebote zurückgeschickt werden sollen.

+++ **Beispiel 1**

Die findet folgendermaßen statt:

1. Die zwei geeigneten Angebote aus Umfang 1 werden zurückgegeben (Angebot 1, Angebot 2).
1. Die verbleibenden zwei geeigneten Angebote aus Umfang 2 werden zurückgegeben (Angebot 3, Angebot 4).

+++

+++ **Beispiel 2**

In diesem Beispiel erreichte Angebot 1 das Frequenzlimit. [Weitere Informationen zur Frequenzbegrenzung](../offer-library/add-constraints.md#capping)

Die findet folgendermaßen statt:

1. Die verbleibenden zwei geeigneten Angebote aus Umfang 1 werden zurückgegeben (Angebot 2, Angebot 3).
1. Das verbleibende geeignete Angebot aus Umfang 2 wird zurückgegeben (Angebot 4).

+++

+++ **Beispiel 3**

In diesem Beispiel haben Angebot 1 und Angebot 3 ihr Frequenzlimit erreicht. [Weitere Informationen zur Frequenzbegrenzung](../offer-library/add-constraints.md#capping)

Die findet folgendermaßen statt:

1. Die verbleibenden zwei geeigneten Angebote aus Umfang 1 werden zurückgegeben (Angebot 2, Angebot 4).
1. Es gibt keine verbleibenden geeigneten Angebote für Umfang 2. Daher wird das [Fallback-Angebot](#add-fallback) zurückgegeben.

+++

**Wenn die Duplizierung aktiviert ist**

Wenn Duplizierungen für alle Platzierungen zulässig sind, kann dasselbe Angebot mehrmals für verschiedene Platzierungen vorgeschlagen werden. Wenn diese Option aktiviert ist, berücksichtigt das System dasselbe Angebot für mehrere Platzierungen. [Weitere Informationen zu Duplizierungsparametern](../offer-library/creating-placements.md)

Nehmen wir dasselbe Beispiel wie oben, in dem Sie zwei Entscheidungsumfänge hinzugefügt haben, z. B.:

* Umfang 1: Es gibt vier geeignete Angebote (Angebot 1, Angebot 2, Angebot 3, Angebot 4) und die Anfrage lautet, dass zwei Angebote zurückgeschickt werden sollen.
* Umfang 2: Es gibt vier geeignete Angebote (Angebot 1, Angebot 2, Angebot 3, Angebot 4) und die Anfrage lautet, dass zwei Angebote zurückgeschickt werden sollen.

+++ **Beispiel 1**

Die findet folgendermaßen statt:

1. Die zwei geeigneten Angebote aus Umfang 1 werden zurückgegeben (Angebot 1, Angebot 2).
1. Die beiden geeigneten Angebote aus Umfang 2 werden zurückgegeben (Angebot 1, Angebot 2).

+++

+++ **Beispiel 2**

In diesem Beispiel erreichte Angebot 1 das Frequenzlimit. [Weitere Informationen zur Frequenzbegrenzung](../offer-library/add-constraints.md#capping)

Die findet folgendermaßen statt:

1. Die verbleibenden zwei geeigneten Angebote aus Umfang 1 werden zurückgegeben (Angebot 2, Angebot 3).

1. Dieselben beiden verbleibenden geeigneten Angebote aus Umfang 2 werden zurückgegeben (Angebot 2, Angebot 3).

+++

+++ **Beispiel 3**

In diesem Beispiel haben Angebot 1 und Angebot 3 ihr Frequenzlimit erreicht. [Weitere Informationen zur Frequenzbegrenzung](../offer-library/add-constraints.md#capping)

Die findet folgendermaßen statt:

1. Die verbleibenden zwei geeigneten Angebote aus Umfang 1 werden zurückgegeben (Angebot 2, Angebot 4).

1. Dieselben beiden verbleibenden geeigneten Angebote aus Umfang 2 werden zurückgegeben (Angebot 2, Angebot 4).

+++

## Hinzufügen eines Fallback-Angebots {#add-fallback}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_fallback"
>title="Hinzufügen eines Fallback-Angebots"
>abstract="Nachdem Sie die Entscheidungsumfänge definiert haben, legen Sie das Fallback-Angebot fest, das Kunden, die nicht den Eignungsregeln und Einschränkungen des Angebots entsprechen, angezeigt wird."

Nachdem Sie die Entscheidungsumfänge definiert haben, definieren Sie das [Fallback-Angebot](../offer-library/creating-fallback-offers.md), das Kunden, die nicht den Eignungsregeln und Einschränkungen des Angebots entsprechen, als letztes Mittel angezeigt wird.

Wählen Sie dazu das Fallback-Angebot aus der Liste der verfügbaren Fallback-Angebote für die in der Entscheidung definierten Platzierungen aus.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>Fallback-Angebote sollten alle in einer Entscheidung verwendeten Darstellungen enthalten. Wenn eine Entscheidung beispielsweise fünf Angebote umfasst und jedes davon eine andere Darstellung hat, sollten fünf Darstellungen in das Fallback-Angebot aufgenommen werden.

Klicken Sie nach der Auswahl auf **[!UICONTROL Weiter]**.

Sie können auf den Link **[!UICONTROL Angebotsbibliothek öffnen]** klicken, um die Liste der Angebote in einer neuen Registerkarte anzuzeigen.

## Entscheidung überprüfen und speichern {#review}

Wenn alles ordnungsgemäß konfiguriert ist, wird eine Zusammenfassung der Entscheidungseigenschaften angezeigt.

1. Überprüfen Sie, ob die Entscheidung für die Präsentation von Angeboten für Kunden bereit ist. Alle Entscheidungsumfänge und das darin enthaltene Fallback-Angebot werden angezeigt.

   ![](../assets/review-decision.png)

1. Sie können jede Platzierung erweitern oder reduzieren. Sie können für jede Platzierung eine Vorschau der verfügbaren Angebote, der Eignung und der Rangfolgedetails anzeigen. Sie können auch Informationen zu den geschätzten qualifizierten Profilen anzeigen. Klicken Sie auf **[!UICONTROL Aktualisieren]**, um diese Daten zu aktualisieren.

   ![](../assets/review-decision-details.png)

1. Klicken Sie auf **[!UICONTROL Fertigstellen]**.
1. Wählen Sie die Option **[!UICONTROL Speichern und aktivieren]** aus.

   ![](../assets/save-activities.png)

   Sie können die Entscheidung auch als Entwurf speichern, um sie später zu bearbeiten und zu aktivieren.

Die Entscheidung wird in der Liste mit dem Status **[!UICONTROL Live]** oder **[!UICONTROL Entwurf]** angezeigt, je nachdem, ob Sie sie im vorherigen Schritt aktiviert haben oder nicht.

Sie ist jetzt bereit, für das Senden von Angeboten an Kunden genutzt zu werden.

## Entscheidungsliste {#decision-list}

In der Entscheidungsliste können Sie die Entscheidung auswählen, deren Eigenschaften angezeigt werden sollen. Dort können Sie sie auch bearbeiten, ihren Status ändern (**Entwurf**, **Live**, **Abgeschlossen**, **Archiviert**), die Entscheidung duplizieren oder löschen.

![](../assets/decision_created.png)

Wählen Sie die Schaltfläche **[!UICONTROL Bearbeiten]** aus, um zum Entscheidungsbearbeitungsmodus zurückzukehren. Dort können Sie die [Details](#create-activity), [Entscheidungsumfänge](#add-decision-scopes) und das [Fallback-Angebot](#add-fallback) der Entscheidung ändern.

>[!IMPORTANT]
>
>Wenn Änderungen an einer Angebotsentscheidung vorgenommen werden, die in einer Journey-Nachricht verwendet wird, müssen Sie die Veröffentlichung der Journey aufheben und sie dann erneut veröffentlichen.  Dadurch wird sichergestellt, dass die Änderungen in die Journey aufgenommen werden und die Nachricht den neuesten Aktualisierungen entspricht.

Wählen Sie eine Live-Entscheidung aus und klicken Sie auf **[!UICONTROL Deaktivieren]**, um den Entscheidungsstatus wieder auf **[!UICONTROL Entwurf]** zu setzen.

Um den Status erneut auf **[!UICONTROL Live]** zu setzen, wählen Sie die Schaltfläche **[!UICONTROL Aktivieren]** aus, die jetzt angezeigt wird.

![](../assets/decision_activate.png)

Die Schaltfläche **[!UICONTROL Weitere Aktionen]** aktiviert die unten beschriebenen Aktionen.

![](../assets/decision_more-actions.png)

* **[!UICONTROL Abschließen]**: setzt den Status der Entscheidung auf **[!UICONTROL Abgeschlossen]**, was bedeutet, dass die Entscheidung nicht mehr aufgerufen werden kann. Diese Aktion steht nur für aktivierte Entscheidungen zur Verfügung. Die Entscheidung ist weiterhin in der Liste verfügbar, Sie können ihren Status jedoch nicht auf **[!UICONTROL Entwurf]** oder **[!UICONTROL Genehmigt]** zurücksetzen. Sie können sie nur duplizieren, löschen oder archivieren.

* **[!UICONTROL Duplizieren]**: erstellt eine Entscheidung mit denselben Eigenschaften, Entscheidungsumfängen und Fallback-Angebot. Standardmäßig hat die neue Entscheidung den Status **[!UICONTROL Entwurf]**.

* **[!UICONTROL Löschen]**: entfernt die Entscheidung aus der Liste.

  >[!CAUTION]
  >
  >Die Entscheidung und ihr Inhalt sind nicht mehr zugänglich. Diese Aktion kann nicht rückgängig gemacht werden.
  >
  >Wenn die Entscheidung in einem anderen Objekt verwendet wird, kann sie nicht gelöscht werden.

* **[!UICONTROL Archivieren]**: setzt den Entscheidungsstatus auf **[!UICONTROL Archiviert]**. Die Entscheidung ist weiterhin in der Liste verfügbar, Sie können ihren Status jedoch nicht auf **[!UICONTROL Entwurf]** oder **[!UICONTROL Genehmigt]** zurücksetzen. Sie können es nur duplizieren oder löschen.

Sie können auch den Status mehrerer Entscheidungen gleichzeitig löschen oder ändern, indem Sie die entsprechenden Checkboxen auswählen.

![](../assets/decision_multiple-selection.png)

Wenn Sie den Status mehrerer Entscheidungen mit unterschiedlichen Status ändern möchten, werden nur die relevanten Status geändert.

![](../assets/decision_change-status.png)

Nachdem eine Entscheidung erstellt wurde, können Sie in der Liste auf ihren Namen klicken.

![](../assets/decision_click-name.png)

Dadurch können Sie auf detaillierte Informationen zu dieser Entscheidung zugreifen. Wählen Sie die Registerkarte **[!UICONTROL Protokoll ändern]**, um [alle Änderungen zu überwachen](../get-started/user-interface.md#changes-log), die an der Entscheidung vorgenommen wurden.

![](../assets/decision_information.png)

## Anleitungsvideo{#video}

Erfahren Sie, wie Sie im Entscheidungs-Management Angebotsaktivitäten erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/3411813?quality=12&captions=ger)


