---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen Ihrer ersten Journey
description: Wichtige Schritte zum Erstellen Ihrer ersten Journey mit Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: Journey, erste, Start, Schnellstart, Zielgruppe, Ereignis, Aktion
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 619bcbc16b4117c29c482c85323603a4281298e0
workflow-type: ht
source-wordcount: '1244'
ht-degree: 100%

---

# Erstellen Ihrer ersten Journey{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Erstellen von Journeys"
>abstract="Erstellen Sie mit **Adobe Journey Optimizer** anhand von in Ereignissen oder Datenquellen gespeicherten kontexbezogenen Daten Echtzeit-Orchestrierungsfälle."


## Voraussetzungen{#start-prerequisites}

Um Nachrichten mit Journeys zu senden, sind folgende Konfigurationen notwendig:

1. **Ereignis konfigurieren**: Wenn Sie Ihre Journeys beim Empfang eines Ereignisses unitär triggern möchten, müssen Sie zunächst ein Ereignis konfigurieren. Sie definieren die erwarteten Informationen sowie deren Verarbeitungsmethode. Dieser Schritt wird von einem **technischen Anwender** ausgeführt. [Mehr dazu](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Zielgruppe erstellen**: Ihre Journey kann auch Adobe Experience Platform-Zielgruppen überwachen, um Nachrichten als Batch an einen bestimmten Satz von Profilen zu senden. Dazu müssen Sie Zielgruppen erstellen. [Weitere Informationen](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **Konfigurieren einer Datenquelle**: Sie können eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung bei Ihren Journeys abzurufen (z. B. in Ihren Bedingungen). Außerdem wird zur Bereitstellungszeit eine integrierte Adobe Experience Platform-Datenquelle konfiguriert. Dieser Schritt ist nicht erforderlich, wenn Sie ausschließlich Daten aus den Ereignissen Ihrer Journey nutzen. Dieser Schritt wird von einem **technischen Anwender** ausgeführt. [Mehr dazu](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Konfigurieren einer Aktion**: Wenn Sie für den Versand Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../action/action.md). Dieser Schritt wird von einem **technischen Anwendenden** ausgeführt. Wenn Sie integrierte Nachrichtenfunktionen von Journey Optimizer verwenden, müssen Sie lediglich eine Kanalaktion zu Ihrer Journey hinzufügen und Inhalte entwerfen.

   ![](assets/custom2.png)

## Zugreifen auf Journeys {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Journeys"
>abstract="Entwerfen Sie Customer Journeys, um Ihren Kundinnen und Kunden personalisierte, kontextuelle Erlebnisse zu bieten. Mit Journey Optimizer können Sie anhand von in Ereignissen oder Datenquellen gespeicherten kontextbezogenen Daten Echtzeit-Orchestrierungsfälle erstellen. In der Registerkarte **Übersicht** wird ein Dashboard mit Schlüsselmetriken zu Ihren Journeys angezeigt. Auf der Registerkarte **Durchsuchen** wird eine Liste der vorhandenen Journeys angezeigt."

### Schlüsselmetriken und Journey-Liste {#access-metrics}

Klicken Sie im Menü JOURNEY-MANAGEMENT auf **[!UICONTROL Journeys]**. Zwei Registerkarten sind verfügbar:

**Überblick**: Auf dieser Registerkarte wird ein Dashboard mit Schlüsselmetriken für Ihre Journeys angezeigt:

* **Verarbeitete Profile**: Gesamtzahl der in den letzten 24 Stunden verarbeiteten Profile.
* **Live-Journeys**: Gesamtzahl der Live-Journeys mit Traffic in den letzten 24 Stunden. Live-Journeys umfassen **unitäre Journeys** (ereignisbasiert) und **Batch-Journeys** (Zielgruppe lesen).
* **Fehlerrate**: Verhältnis aller fehlerhaften Profile in Bezug auf die Gesamtzahl der in den letzten 24 Stunden eingetretenen Profile.
* **Verwerfungsrate**: Verhältnis aller verworfenen Profile in Bezug auf die Gesamtzahl der in den letzten 24 Stunden eingetretenen Profile. Ein verworfenes Profil stellt eine Person dar, die nicht zum Eintritt in die Journey berechtigt ist, z. B. aufgrund eines falschen Namespace oder aufgrund von Regeln für den erneuten Eintritt.

>[!NOTE]
>
>Dieses Dashboard berücksichtigt die Journeys mit Traffic in den letzten 24 Stunden. Es werden nur die Journeys angezeigt, auf die Sie zugreifen können. Metriken werden alle 30 Minuten aktualisiert, aber nur dann, wenn neue Daten verfügbar sind.

![](assets/journeys-dashboard.png)

**Durchsuchen**: Auf dieser Registerkarte wird die Liste der vorhandenen Journeys angezeigt. Sie können nach Journeys suchen, Filter verwenden und grundlegende Aktionen für jedes Element ausführen. Sie können Elemente beispielsweise duplizieren oder löschen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../start/user-interface.md#filter-lists).

![](assets/journeys-browse.png)

### Filtern von Journeys {#filter}

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

## Erstellen Ihrer Journey {#jo-build}

Entwerfen Sie Journeys, um Ihren Kundinnen und Kunden personalisierte, kontextuelle Erlebnisse zu bieten. Mit [!DNL Journey Optimizer] können Sie Anwendungsfälle für die Orchestrierung in Echtzeit erstellen und dabei kontextuelle Daten nutzen, die in Ereignissen oder Datenquellen gespeichert sind. Erstellen Sie mehrstufige fortgeschrittene Szenarien mit folgenden Funktionen:

* Führen Sie einen **unitären Versand** in Echtzeit aus, ausgelöst durch den Empfang eines Ereignisses, oder **als Batch** unter Verwendung von Adobe Experience Platform-Zielgruppen.

* Nutzen Sie **kontextuelle Daten** aus Ereignissen, Informationen aus Adobe Experience Platform oder Daten aus API-Services von Drittanbietern.

* Verwenden Sie die **integrierten Kanalaktionen** (E-Mail, SMS, Push-Benachrichtigung) zum Senden von in [!DNL Journey Optimizer] entworfenen Nachrichten oder erstellen Sie **benutzerdefinierte Aktionen**, wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden.

* Erstellen Sie mit dem **Journey-Designer** mehrstufige Anwendungsfälle: Ziehen Sie einfach per Drag-and-Drop ein Eintrittsereignis oder eine Aktivität vom Typ „Zielgruppe lesen“ in die Benutzeroberfläche, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

➡️ [Entdecken Sie diese Funktion im Video](journey.md#video)

Die Schritte zum Senden von Nachrichten durch Journeys sind unten aufgeführt:

1. Klicken Sie auf der Registerkarte **Durchsuchen** auf **[!UICONTROL Journey erstellen]**, um eine neue Journey zu erstellen.

1. Bearbeiten Sie im Konfigurationsbereich auf der rechten Seite die Eigenschaften der Journey. Informationen zum Festlegen der Eigenschaften Ihrer Journey finden Sie auf [dieser Seite](journey-properties.md).

   ![](assets/jo-properties.png)

1. Ziehen Sie zuerst ein Ereignis oder die Aktivität **Zielgruppe lesen** per Drag-and-Drop aus der Palette in die Arbeitsfläche. Weitere Informationen zum Entwerfen von Journeys finden Sie in [diesem Abschnitt](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Ziehen Sie die nächsten Schritte, die der Kontakt ausführen soll, per Drag-and-Drop. Sie können beispielsweise eine Bedingung und anschließend eine Kanalaktion hinzufügen. Weitere Informationen zu Aktivitäten finden Sie in [diesem Abschnitt](using-the-journey-designer.md).

1. Testen Sie Ihre Journey mit Testprofilen. Weitere Informationen finden Sie in diesem [Abschnitt](testing-the-journey.md)

1. Veröffentlichen Sie Ihre Journey, um sie zu aktivieren. Weitere Informationen finden Sie in diesem [Abschnitt](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Überwachen Sie Ihre Journey mithilfe der dedizierten Reporting-Tools, um die Effektivität Ihrer Journey zu messen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)


## Duplizieren einer Journey {#duplicate-a-journey}

Sie können eine vorhandene Journey über die Registerkarte **Durchsuchen** duplizieren. Alle Objekte und Einstellungen werden in der Journey-Kopie dupliziert.

Gehen Sie dazu wie folgt vor:

1. Navigieren Sie zu der Journey, die Sie kopieren möchten, und klicken Sie auf das Symbol **Mehr Aktionen** (die drei Punkte neben dem Journey-Namen).
1. Wählen Sie **Duplizieren** aus.

   ![Duplizieren einer Journey](assets/duplicate-jo.png)

1. Geben Sie den Namen der Journey ein und speichern Sie ihn. Sie können den Namen auch im Bildschirm „Journey-Eigenschaften“ ändern. Standardmäßig lautet der Name wie folgt: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. Die neue Journey wird erstellt und ist in der Journey-Liste verfügbar.
