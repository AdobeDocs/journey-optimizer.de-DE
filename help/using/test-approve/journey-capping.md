---
title: Journey-Begrenzung und Schlichtung
description: Erfahren Sie, wie Sie Begrenzungsregeln für Ihre Journey erstellen und Journey-Eintritte vermitteln.
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 2%

---


# Journey-Begrenzung und Schlichtung {#journey-capping}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit Konfliktmanagement und Priorisierung](gs-conflict-prioritization.md)
* [Potenzielle Konflikte in Journey und Kampagnen erkennen](conflicts.md)
* [Zuweisen von Prioritätswerten zu Journeys und Kampagnen](priority-scores.md)
* **[Journey-Capping und Schlichtung](journey-capping.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Die Tools zur Konfliktverwaltung und Priorisierung sind derzeit nur für ausgewählte Benutzer verfügbar, da sie nur über eingeschränkte Verfügbarkeit verfügen.

Mit der Journey-Begrenzung können Sie die Anzahl der Journey einschränken, in die sich ein Profil eintragen kann, wodurch eine Kommunikationsüberlastung verhindert wird. In Journey Optimizer können Sie zwei Arten von Begrenzungsregeln festlegen:

* **Einstiegsbegrenzung** begrenzt die Anzahl der Einstiege in eine Journey über einen bestimmten Zeitraum für ein Profil.
* **Parallele Begrenzungen** beschränken, wie viele Journey ein Profil gleichzeitig eingeschrieben werden kann. Diese Art der Begrenzung nutzt Journey-Prioritätsbewertungen, um Einträge zu schlichten, wenn Profile für mehrere Journey gleichzeitig während eines bestimmten Zeitraums berechtigt sind.

## Erstellen einer Journey-Begrenzungsregel {#create-rule}

Gehen Sie wie folgt vor, um eine Journey-Begrenzungsregel zu erstellen:

1. Navigieren Sie zum Menü **[!UICONTROL Geschäftsregeln (Beta)]** , um auf den Regelsatzbestand zuzugreifen.

1. Wählen Sie den Regelsatz aus, dem Sie die Begrenzungsregel hinzufügen möchten, oder erstellen Sie einen neuen Regelsatz:

   * Um einen vorhandenen Regelsatz zu verwenden, wählen Sie ihn aus der Liste aus. Journey-Begrenzungsregeln können nur zu Regelsätzen mit der Domäne &quot;Journey&quot;hinzugefügt werden. Sie können diese Informationen in den Regelsatzlisten in der Spalte **[!UICONTROL Domäne]** überprüfen.

     ![](assets/journey-capping-list.png)

   * Um die Begrenzungsregel in einem neuen Regelsatz zu erstellen, klicken Sie auf **[!UICONTROL Regelsatz erstellen]**, geben Sie einen eindeutigen Namen für den Regelsatz an und wählen Sie &quot;Journey&quot;aus der Dropdown-Liste **[!UICONTROL Regelsatzdomäne]** aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

     ![](assets/journey-capping-rule-set.png)

1. Klicken Sie im Regelsatzbildschirm auf die Schaltfläche **[!UICONTROL Regel hinzufügen]** und konfigurieren Sie dann die Regel entsprechend Ihren Anforderungen:

   ![](assets/journey-capping-concurrency.png)

   * Geben Sie einen eindeutigen Namen für die Regel an.

   * Geben Sie in der Dropdownliste **[!UICONTROL Regeltyp]** den Begrenzungstyp für die Regel an.

      * **[!UICONTROL Journey Entry Cap]**: Beschränkt die Anzahl der Einträge in die Journey über einen bestimmten Zeitraum für ein Profil.
      * **[!UICONTROL Journey Concurrency Cap]**: Beschränkt, wie viele Journey ein Profil gleichzeitig eingeschrieben werden kann.

   * Erweitern Sie die folgenden Abschnitte, um zu erfahren, wie Sie die einzelnen Begrenzungstypen konfigurieren:

     +++Journey-Einstiegsbegrenzungsregel konfigurieren

      1. Legen Sie im Feld **[!UICONTROL Begrenzung]** fest, wie oft ein Profil maximal auf die Journey zugreifen darf.
      1. Definieren Sie im Feld **[!UICONTROL Dauer]** den zu berücksichtigenden Zeitraum.

     In diesem Beispiel möchten wir verhindern, dass Profile diese Journey mehr als &quot;5&quot;-mal im Monat aufrufen.

     ![](assets/journey-capping-entry-example.png)

+++

     +++Journey-Begrenzungsregel konfigurieren

      1. Legen Sie im Feld **[!UICONTROL Begrenzung]** die maximale Anzahl von Journey fest, an denen ein Profil gleichzeitig angemeldet werden kann.
      1. Verwenden Sie das Feld **[!UICONTROL Priorization look ahead]** , um Journey-Einträge basierend auf Prioritätsbewertungen über einen ausgewählten Zeitraum (z. B. 1 Tag, 7 Tage, 30 Tage) zu schlichten. Dies hilft bei der Priorisierung der Eingabe in Journey mit höherem Wert, wenn ein Profil für mehrere Journey qualifiziert ist.

     In diesem Beispiel möchten wir die Eingabe von Profilen auf die Journey beschränken, wenn diese bereits für eine andere Journey angemeldet sind. Wenn eine weitere Journey innerhalb der nächsten sieben Tage eine höhere Priorität hat, wird das Profil diese Journey eingeben.

     ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

+++

1. Wenn die Begrenzungsregel für die Anwendung auf Journey bereit ist, aktivieren Sie sie, indem Sie auf die Schaltfläche mit Auslassungspunkten neben ihrem Namen klicken.

   ![](assets/journey-capping-activate-rule.png)

1. Aktivieren Sie den gesamten Regelsatz, indem Sie in der oberen rechten Ecke des Bildschirms auf die Suchschaltfläche neben der Schaltfläche Regel hinzufügen klicken.

   ![](assets/journey-capping-activate-rule-set.png){width="50%" zommable="yes"}

## Begrenzungsregeln auf Journey anwenden {#apply-capping}

Um eine Begrenzungsregel auf eine Journey anzuwenden, greifen Sie auf die Journey zu und öffnen Sie die zugehörigen Eigenschaften. Wählen Sie in der Dropdown-Liste **[!UICONTROL Begrenzungsregeln]** den relevanten Regelsatz aus.
Sobald die Journey aktiviert ist, werden die im Regelsatz definierten Begrenzungsregeln wirksam.

![](assets/journey-capping-apply.png)
