---
title: Journey-Begrenzung und -Steuerung
description: Informationen zum Erstellen von Begrenzungsregeln für Ihre Journeys und zur Steuerung des Journey-Eintritts
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: 4c0ee178-81fb-41ae-b7f5-22da995e6fc6
source-git-commit: 0a6fa748aca04f544954089d2dfdd8e9a3afdd97
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 89%

---

# Journey-Begrenzung und -Steuerung {#journey-capping}

>[!AVAILABILITY]
>
>Die Funktionen für Konflikte und Priorisierung stehen derzeit einer ausgewählten Kundengruppe nur eingeschränkt zur Verfügung. Sie werden in Zukunft schrittweise für weitere Benutzende eingeführt. Wenden Sie sich an Ihr Accountteam, wenn Sie auf die Warteliste für diese Funktionen gesetzt werden möchten.

Mit der Journey-Begrenzung können Sie die Anzahl der Journeys einschränken, an denen ein Profil teilnehmen kann, wodurch eine Kommunikationsüberlastung verhindert wird. In Journey Optimizer können Sie zwei Arten von Begrenzungsregeln festlegen:

* **Begrenzung für Eintritte**: Beschränkt die Anzahl der Eintritte in die Journey für ein Profil über einen bestimmten Zeitraum.
* **Begrenzung gleichzeitiger Journeys**: Beschränkt, an wie vielen Journeys ein Profil gleichzeitig teilnehmen kann.

Beide Arten von Journey-Begrenzungen nutzen Prioritätswerte, um Eintritte zu steuern.

>[!AVAILABILITY]
>
>**Journey** Domain-Regelsätze sind nur für eine begrenzte Benutzergruppe verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.

➡️ [Entdecken Sie diese Funktion im Video](#video)

## Erstellen einer Journey-Begrenzungsregel {#create-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_set_concurrency_prioritization"
>title="Vorschau der Priorisierung"
>abstract=" Wenn eine Journey mit höherer Priorität innerhalb des hier angegebenen Zeitraums geplant ist, wird der Eintritt der Kundin bzw. des Kunden in die Journey unterbunden. Für Situationen, in denen der Journey-Eintritt nach dem Windhundverfahren erfolgen soll, wird empfohlen, den täglichen Vorschauzeitraum auszuwählen und sicherzustellen, dass der Prioritätswert aller anderen Journeys an diesem Tag unter dem Prioritätswert für die Journey liegt. Wenn eine Journey einen Prioritätswert von 100 erhält, würde das ebenfalls einen Eintritt in die Journey sicherstellen."

>[!CONTEXTUALHELP]
>id="ajo_rule_set_rule_type"
>title="Regeltyp"
>abstract="Geben Sie den Begrenzungstyp für die Regel an. Die **[!UICONTROL Begrenzung für Journey-Eintritte]** begrenzt für ein Profil die Anzahl der Eintritte in die Journey über einen bestimmten Zeitraum, während die **[!UICONTROL Begrenzung gleichzeitiger Journeys]** eingrenzt, in wie viele Journeys ein Profil gleichzeitig eingetreten sein kann."

Gehen Sie wie folgt vor, um eine Journey-Begrenzungsregel zu erstellen:

1. Navigieren Sie zum Menü **[!UICONTROL Geschäftsregeln]**, um auf das Regelsatzinventar zuzugreifen.

1. Wählen Sie den Regelsatz aus, dem Sie die Begrenzungsregel hinzufügen möchten, oder erstellen Sie einen neuen Regelsatz:

   * Um einen vorhandenen Regelsatz zu verwenden, wählen Sie ihn aus der Liste aus. Journey-Begrenzungsregeln können nur zu Regelsätzen mit der Domain „Journey“ hinzugefügt werden. Sie können diese Informationen in den Regelsatzlisten in der Spalte **[!UICONTROL Domain]** überprüfen.

     ![](assets/journey-capping-list.png)

   * Um die Begrenzungsregel in einem neuen Regelsatz zu erstellen, klicken Sie auf **[!UICONTROL Regelsatz erstellen]**, geben Sie einen eindeutigen Namen für den Regelsatz an und wählen Sie in der Dropdown-Liste **[!UICONTROL Domain des Regelsatzes]** die Option „Journey“ aus. Klicken Sie anschließend auf **[!UICONTROL Speichern]**.

     ![](assets/journey-capping-rule-set.png)

1. Klicken Sie auf dem Bildschirm „Regelsatz“ auf die Schaltfläche **[!UICONTROL Regel hinzufügen]** und konfigurieren Sie dann die Regel entsprechend Ihren Anforderungen:

   ![](assets/journey-capping-concurrency.png)

   * Geben Sie einen eindeutigen Namen für die Regel an.

   * Geben Sie in der Dropdown-Liste **[!UICONTROL Regeltyp]** den Begrenzungstyp für die Regel an.

      * **[!UICONTROL Begrenzung für Journey-Eintritte]**: Beschränkt für ein Profil die Anzahl der Eintritte in die Journey über einen bestimmten Zeitraum.
      * **[!UICONTROL Begrenzung gleichzeitiger Journeys]**: Beschränkt, an wie vielen Journeys ein Profil gleichzeitig teilnehmen kann.

   * Erweitern Sie die folgenden Abschnitte, um zu erfahren, wie jeder Begrenzungstyp konfiguriert wird:

     +++Konfigurieren einer Begrenzungsregel für Journey-Eintritte

      1. Legen Sie im Feld **[!UICONTROL Begrenzung]** die maximale Anzahl von Journeys fest, in die ein Profil eintreten kann.
      1. Legen Sie im Feld **[!UICONTROL Dauer]** den zu berücksichtigenden Zeitraum fest. Bitte beachten Sie, dass die Dauer auf der UTC-Zeitzone basiert. Zum Beispiel wird die tägliche Begrenzung um Mitternacht UTC zurückgesetzt.

     >[!AVAILABILITY]
     >
     >Die „tägliche“ Dauer ist nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.

     In diesem Beispiel möchten wir Profile so einschränken, dass sie in einem Monat in nicht mehr als „5“ Journeys eintreten können.

     ![](assets/journey-capping-entry-example.png)

     >[!NOTE]
     >
     >Das System berücksichtigt die Priorität bevorstehender geplanter Journeys, auf die dieselbe Regel angewendet wird.
     >
     >Wenn die Marketing-Fachkraft in diesem Beispiel bereits vier Journeys eingegeben hat und in diesem Monat eine weitere geplante Journey mit höherer Priorität ansteht, wird die Kundschaft daran gehindert, in die Journey mit der niedrigeren Priorität einzutreten.

+++

     +++Konfigurieren einer Regel für die Begrenzung gleichzeitiger Journeys

      1. Legen Sie im Feld **[!UICONTROL Begrenzung]** die maximale Anzahl von Journeys fest, an denen ein Profil gleichzeitig teilnehmen kann.

      1. Verwenden Sie das Feld **[!UICONTROL Vorschau der Priorisierung]**, um Journey-Eintritte basierend auf Prioritätswerten über einen ausgewählten Zeitraum (z. B. 1 Tag, 7 Tage, 30 Tage) zu steuern. Dies hilft bei der Priorisierung des Eintritts in Journeys mit einem höheren Wert, wenn ein Profil für mehrere Journeys qualifiziert ist.

     In diesem Beispiel möchten wir Profile so einschränken, dass sie nicht in die Journey eintreten können, wenn sie bereits an einer Journey mit demselben Regelsatz teilnehmen. Wenn eine weitere Journey innerhalb der nächsten sieben Tage einen höheren Prioritätswert hat, tritt das Profil nicht in diese Journey ein.

     ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

+++

1. Wenn die Begrenzungsregel für die Anwendung auf Journeys bereit ist, aktivieren Sie sie, indem Sie auf die Schaltfläche mit Auslassungspunkten neben ihrem Namen klicken.

   ![](assets/journey-capping-activate-rule.png)

1. Aktivieren Sie den gesamten Regelsatz, indem Sie oben rechts im Bildschirm auf die Schaltfläche mit den Auslassungspunkten neben der Schaltfläche „Regel hinzufügen“ klicken.

   ![](assets/journey-capping-activate-rule-set.png)

## Anwenden von Begrenzungsregeln auf Journeys {#apply-capping}

>[!CONTEXTUALHELP]
>id="ajo_journey_capping_rule"
>title="Anwenden des Regelsatzes auf Journeys"
>abstract="Regelsatz anwenden, damit ein Teil der Zielgruppe anhand von Regeln zur Frequenzbegrenzung von dieser Journey ausgeschlossen wird."

Um eine Begrenzungsregel auf eine Journey anzuwenden, greifen Sie auf die Journey zu und öffnen Sie die zugehörigen Eigenschaften. Wählen **[!UICONTROL in der Dropdown]** Liste Begrenzungsregeln den entsprechenden Regelsatz aus. Sobald die Journey aktiviert ist, werden die im Regelsatz definierten Begrenzungsregeln wirksam.

![](assets/journey-capping-apply.png)

>[!IMPORTANT]
>
>Wenn eine Journey sofort aktiviert wird, kann es bis zu 20 Minuten dauern, bis das System beginnt, Kundinnen und Kunden zu unterdrücken. Sie können Ihre Journey so planen, dass sie mindestens 20 Minuten in der Zukunft beginnt, um dies zu verhindern.

Sobald die Journey live ist, können Sie in der Tabelle **[!UICONTROL Journey-Ausschlüsse} im Journey-Bericht überprüfen, ob der Regelsatz zu einem Ausschluss von der Journey]**. [Erfahren Sie, wie Sie mit Journey-Berichten arbeiten](../reports/journey-global-report-cja.md)

![](assets/journey-report.png)

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435530?quality=12)
