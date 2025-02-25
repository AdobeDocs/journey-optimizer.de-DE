---
solution: Journey Optimizer
product: journey optimizer
title: Journey durchsuchen und filtern
description: Durchsuchen und Filtern Ihrer Journey in Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: Journey, erste, Start, Schnellstart, Zielgruppe, Ereignis, Aktion
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 94%

---

# Journey durchsuchen und filtern {#browse-journeys}

## Zugreifen auf Journeys {#journey-access}

### Journey-Dashboard {#dashboard-jo}

Klicken Sie im Menü JOURNEY-MANAGEMENT auf **[!UICONTROL Journeys]**. Zwei Registerkarten sind verfügbar: **[!UICONTROL Übersicht]** und **[!UICONTROL Durchsuchen]**.

* Auf **[!UICONTROL Registerkarte]**&#x200B;Übersicht“ wird ein Dashboard mit Schlüsselmetriken für Ihre Journey angezeigt:

   * **Verarbeitete Profile**: Gesamtzahl der in den letzten 24 Stunden verarbeiteten Profile.
   * **Live-Journeys**: Gesamtzahl der Live-Journeys mit Traffic in den letzten 24 Stunden. Live-Journeys umfassen **unitäre Journeys** (ereignisbasiert) und **Batch-Journeys** (Zielgruppe lesen).
   * **Fehlerrate**: Verhältnis aller fehlerhaften Profile in Bezug auf die Gesamtzahl der in den letzten 24 Stunden eingetretenen Profile.
   * **Verwerfungsrate**: Verhältnis aller verworfenen Profile in Bezug auf die Gesamtzahl der in den letzten 24 Stunden eingetretenen Profile. Ein verworfenes Profil stellt eine Person dar, die nicht zum Eintritt in die Journey berechtigt ist, z. B. aufgrund eines falschen Namespace oder aufgrund von Regeln für den erneuten Eintritt.

  >[!NOTE]
  >
  >Dieses Dashboard berücksichtigt die Journeys mit Traffic in den letzten 24 Stunden. Es werden nur die Journeys angezeigt, auf die Sie zugreifen können. Metriken werden alle 30 Minuten aktualisiert, aber nur dann, wenn neue Daten verfügbar sind.

  ![](assets/journeys-dashboard.png)

* Auf **[!UICONTROL Registerkarte]** Durchsuchen“ wird die Liste der vorhandenen Journey angezeigt. Sie können nach Journeys suchen, Filter verwenden und grundlegende Aktionen für jedes Element ausführen. Sie können Elemente beispielsweise duplizieren oder löschen.

  ![](assets/journeys-browse.png)

### Journey filtern {#filter}

In der Liste der Journeys können Sie verschiedene Filter nutzen, um diese Liste zur besseren Lesbarkeit zu verfeinern.

![](assets/filter-journeys.png)

Folgende Filtervorgänge können Sie durchführen:

Filtern von Journeys nach Status, Typ, Version und zugewiesenen Tags aus den Filtern für **[!UICONTROL Status und Version]**.

Die folgenden Typen sind möglich: **[!UICONTROL Unitäres Ereignis]**, **[!UICONTROL Zielgruppen-Qualifizierung]**, **[!UICONTROL Zielgruppe lesen]** oder **[!UICONTROL Geschäftsereignis]**.

Der Status kann wie folgt lauten:

* **Geschlossen**: Die Journey wurde mithilfe der Schaltfläche **Für neue Eintritte schließen** geschlossen. Die Journey stoppt den Eintritt neuer Personen in die Journey.  Personen, die sich bereits in der Journey befinden, können die Journey wie gewohnt beenden.
* **Entwurf**: Die Journey befindet sich in der ersten Phase. Sie wurde noch nicht veröffentlicht.
* **Entwurf (Test)**: Der Testmodus wurde mit der Schaltfläche **Testmodus** aktiviert.
* **Beendet**: Die Journey wechselt nach der [maximalen globalen Wartezeit](journey-properties.md#global_timeout) von 91 Tagen automatisch in diesen Status.  Profile, die sich bereits in der Journey befinden, beenden die Journey wie gewohnt. Neue Profile können nicht mehr in die Journey eintreten. 
* **Live**: Die Journey wurde mithilfe der Schaltfläche **Veröffentlichen** veröffentlicht.
* **Gestoppt**: Die Journey wurde mit der Schaltfläche **Stoppen** gestoppt. Alle Einzelpersonen verlassen die Journey sofort.

>[!NOTE]
>
>Der Journey-Authoring-Lebenszyklus umfasst auch eine Reihe von Zwischenstatus, die nicht zum Filtern verfügbar sind: „Veröffentlichen“ (zwischen „Entwurf“ und „Live“), „Testmodus aktivieren“ oder „Testmodus deaktivieren“ (zwischen „Entwurf“ und „Entwurf [Test]“) und „Stoppen“ (zwischen „Live“ und „Gestoppt“). Wenn sich eine Journey in einem Zwischenzustand befindet, ist sie schreibgeschützt.

Verwenden Sie die **[!UICONTROL Erstellungsfilter]**, um die Journeys nach ihrem Erstellungsdatum oder der Person, die sie erstellt hat, zu filtern.

Zeigen Sie etwa nur Journeys an, die ein bestimmtes Ereignis, eine bestimmte Feldergruppe oder eine bestimmte Aktion aus den **[!UICONTROL Aktivitätsfiltern]** und **[!UICONTROL Datenfiltern]** verwenden.

Die **[!UICONTROL Veröffentlichungsfilter]** erlauben die Auswahl eines Veröffentlichungsdatum oder einer Person. Sie können beispielsweise auswählen, dass die aktuellen Versionen von Live-Journeys, die gestern veröffentlicht wurden, angezeigt werden sollen.

Um Journeys nach einem bestimmten Datumsbereich zu filtern, wählen Sie aus der Dropdown-Liste **[!UICONTROL Veröffentlicht]** die Option **[!UICONTROL Benutzerdefiniert]** aus.

In den Konfigurationsbereichen für Ereignis, Datenquelle und Aktion zeigt das Feld **[!UICONTROL Verwendet in]** die Zahl der Journeys an, die das betreffende Ereignis, diese Feldergruppe oder diese Aktion verwenden. Sie können auf die Schaltfläche **[!UICONTROL Customer Journeys anzeigen]** klicken, um die Liste der entsprechenden Journeys zu öffnen.

![](assets/journey3bis.png)


## Journey-Versionen {#journey-versions}

In der Liste der Journeys werden alle Journey-Versionen mit der Versionsnummer angezeigt. Wenn Sie nach einer Journey suchen, werden beim ersten Öffnen der Anwendung die neuesten Versionen oben in der Liste angezeigt. Anschließend können Sie die gewünschte Sortierung definieren und die Anwendung behält sie als Benutzerpräferenz bei. Die Version der Journey wird auch oben auf der Journey-Bearbeitungsoberfläche über der Arbeitsfläche angezeigt.

![](assets/journeyversions1.png)

>[!NOTE]
>
>In der Regel kann ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](end-journey.md).

Wenn eine Live-Journey geändert werden muss, bitte eine neue Version der Journey erstellen.

1. Öffnen Sie die neueste Version Ihrer Live-Journey, klicken Sie auf **[!UICONTROL Neue Version erstellen]** und bestätigen Sie.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Sie können eine neue Version nur über die letzte Version einer Journey erstellen.

1. Nehmen Sie Ihre Änderungen vor, klicken Sie auf **[!UICONTROL Veröffentlichen]** und bestätigen Sie.

Ab dem Zeitpunkt der Veröffentlichung der Journey treten Personen in die neueste Version der Journey ein.  Personen, die bereits in einer früheren Version eingetreten sind, bleiben bis zum Ende der Journey darin. Bei einem späteren erneuten Eintritt in dieselbe Journey treten sie in die neueste Version ein.

Journey-Versionen können einzeln angehalten werden. Alle Versionen einer Journey haben denselben Namen.

Wenn Sie eine neue Version einer Journey veröffentlichen, endet die vorherige Version automatisch und wechselt in den Status **Geschlossen**. Es kann kein Eintritt in die Journey stattfinden. Selbst wenn Sie die aktuelle Version stoppen, bleibt die vorherige Version geschlossen.



## Duplizieren einer Journey {#duplicate-a-journey}

Sie können eine vorhandene Journey über die Registerkarte **Durchsuchen** duplizieren. Alle Objekte und Einstellungen werden in der Journey-Kopie dupliziert.

Gehen Sie dazu wie folgt vor:

1. Navigieren Sie zu der Journey, die Sie kopieren möchten, und klicken Sie auf das Symbol **Mehr Aktionen** (die drei Punkte neben dem Journey-Namen).
1. Wählen Sie **Duplizieren** aus.

   ![Duplizieren einer Journey](assets/duplicate-jo.png)

1. Geben Sie den Namen der Journey ein und speichern Sie ihn. Sie können den Namen auch im Bildschirm „Journey-Eigenschaften“ ändern. Standardmäßig lautet der Name wie folgt: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. Die neue Journey wird erstellt und ist in der Journey-Liste verfügbar.

