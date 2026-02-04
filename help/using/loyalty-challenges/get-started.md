---
solution: Journey Optimizer
product: journey optimizer
title: Herausforderungen im Zusammenhang mit Treueprogrammen
description: Erfahren Sie mehr über die Funktionen, den Workflow und die Funktionen von Loyalitätsherausforderungen in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 2%

---


# Herausforderungen im Zusammenhang mit Treueprogrammen {#understand-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Über Herausforderungen im Zusammenhang mit der Treue"
>abstract="Mit den Herausforderungen im Zusammenhang mit der Treue können Sie personalisierte Interaktionsangebote erstellen, die Kunden dazu motivieren, bestimmte Aktionen durchzuführen und Belohnungen zu sammeln."

Mit den Herausforderungen im Zusammenhang mit der Kundentreue können Sie personalisierte Interaktionsangebote entwerfen und bereitstellen, die Kunden dazu motivieren, bestimmte Aktionen durchzuführen und Belohnungen zu sammeln.

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit den Herausforderungen im Zusammenhang mit dem Treueprogramm](gs-loyalty-challenges.md) - Kurzübersicht und nächste Schritte
* **Herausforderungen im Zusammenhang mit der Treue verstehen** ◀︎ **Sie sind hier** - Funktionen, Workflow, Voraussetzungen
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* [Herausforderungen verwalten](manage-challenges.md) - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

## Überblick {#overview}

Die Herausforderungen im Zusammenhang mit dem Treueprogramm bieten eine Komplettlösung für die Erstellung von Treueprogrammen in großem Maßstab, von der Definition von Aufgaben und Meilensteinen bis hin zur Bereitstellung von Inhalten und zur kanalübergreifenden Verfolgung der Leistung. Sie können drei Arten von Challenge-Erlebnissen erstellen, Belohnungen konfigurieren, Multi-Channel-Benachrichtigungen in wichtigen Lebenszyklusphasen senden und die Leistung mithilfe automatisch generierter Journey überwachen - und das alles unter Beibehaltung der Integration mit Ihrem externen Treueprogramm-System.

## Funktionsweise {#how-it-works}

Dieser Workflow ermöglicht das Erstellen und Starten einer Herausforderung zum Treueprogramm:

1. **Datenaufnahme einrichten** - Konfigurieren Sie Experience Platform-Quell-Connectoren (wie Kapillare), um Treueprogramm-Ereignisdaten aufzunehmen, mit denen Kundenaktionen und -fortschritt verfolgt werden.

2. **Herausforderung erstellen** - Definiert die grundlegenden Eigenschaften der Herausforderung, einschließlich Name, Typ (Standard, Streak oder Sequenziell), Zielgruppe und Datumsbereich.

3. **Aufgaben hinzufügen** - Definiert die spezifischen Aktionen, die Kunden durchführen müssen, einschließlich Aufgabentypen (Kauf, Ausgaben, Besuch usw.), Mengen, Produktfiltern und Belohnungen.

4. **Erstellen von Inhaltskarten** - Erstellen Sie die visuelle Darstellung Ihrer Challenge mit Journey Optimizer-Inhaltskarten, die auf Kundengeräten angezeigt werden.

5. **Messaging konfigurieren** (Optional) - Richten Sie Multi-Channel-Nachrichten (In-App, E-Mail, Push) für die wichtigsten Phasen ein: Start, in Bearbeitung und Abschluss.

6. **Überprüfen und**: Testen Sie Ihre Herausforderung mit Testprofilen und veröffentlichen Sie sie dann, um sie Ihrer Zielgruppe verfügbar zu machen.

7. **Automatisch erstelltes Journey** - Beim Veröffentlichen erstellt Journey Optimizer automatisch eine Journey, die die Bereitstellung und das Messaging von Inhaltskarten koordiniert.

8. **Journey aktivieren** - Die automatisch generierte Journey wird am Startdatum der Herausforderung aktiviert und verwaltet alle Kundeninteraktionen.

9. **Leistung überwachen** - Verfolgen Sie Teilnahme, Abschlussraten, Belohnungsverteilung und Nachrichteninteraktion durch integrierte Berichte und die Journey-Arbeitsfläche.

>[!NOTE]
>
>Die automatisch generierte Journey wird in Ihrem Journey-Inventar angezeigt und kann bei Bedarf angepasst werden. Direkt am Journey vorgenommene Änderungen werden jedoch nicht mit der Challenge-Konfiguration synchronisiert.

## Wichtigste Funktionen {#key-capabilities}

Herausforderungen im Zusammenhang mit der Treue nutzen, um:

* **Erstellen Sie drei Arten von Herausforderungen**:
   * **Standard**: Kunden führen eine beliebige Anzahl von Aufgaben aus, um Prämien zu erhalten.
   * **Streak**: Kundinnen und Kunden führen dieselbe Aufgabe mehrmals aus.
   * **Sequenziell**: Kunden führen Aufgaben in einer bestimmten Reihenfolge aus.

* **Design Challenge-Inhalte**: Verwenden Sie Journey Optimizer-Inhaltskarten, um die visuelle Darstellung Ihrer Challenge auf Kundengeräten zu erstellen. Auf Inhaltskarten werden die Challenge-Informationen, der Fortschritt und die Belohnungen auf dem Gerät des Kunden angezeigt.

* **Aufgabenanforderungen einrichten** Definieren Sie, was Kunden tun müssen, um Prämien zu verdienen, darunter:
   * Aufgabentypen (Kauf, Ausgabenbetrag, Besuch usw.)
   * Mengenbedarf
   * Produkteinschlüsse/-ausschlüsse mithilfe von SKUs
   * Benutzerdefinierte Attribute und Bedingungen

* **Belohnungen konfigurieren**: Belohnungen definieren, die Kunden entweder bei Aufgabenabschluss oder nach Abschluss der gesamten Challenge erhalten

* **Benachrichtigungen senden**: Versand von Nachrichten über mehrere Kanäle (In-App, E-Mail, Push) in wichtigen Phasen:
   * **Launch**: Wenn die Challenge beginnt
   * **In Bearbeitung**: Wenn Kundinnen und Kunden teilweise durchgekommen sind
   * **Abschließen**: Wenn Kunden die Challenge abgeschlossen haben

* **Performance verfolgen** Überwachen automatisch generierter Journeys und Überprüfen der Challenge-Performance

### Wichtige Einschränkungen {#limitations}

* **Kein Sachkontensystem**: Treueprobleme verfolgen keine Geldwerte oder Punktesalden. Wenn Kundinnen und Kunden eine Challenge abschließen und eine Belohnung erhalten, ruft Journey Optimizer Ihr externes Treueprogramm-Management-System an, um die Punktzuweisung zu bearbeiten.

* **Nur Zielgruppenauswahl**: Sie können vorhandene Zielgruppen auswählen, aber keine neuen Zielgruppen über die Benutzeroberfläche „Herausforderungen im Treueprogramm“ erstellen.

## Voraussetzungen {#prerequisites}

Bevor Sie Herausforderungen im Zusammenhang mit dem Treueprogramm nutzen, stellen Sie Folgendes sicher:

### Einrichtung der Datenaufnahme {#data-ingestion}

Herausforderungen im Zusammenhang mit der Kundentreue beruhen auf Daten, die über Experience Platform-Quell-Connectoren aufgenommen werden, um den Kundenfortschritt und den Abschluss von Aufgaben zu verfolgen.

1. **Konfigurieren eines unterstützten Quell-Connectors**: Derzeit ist der Kapillaranschluss allgemein verfügbar. Weitere Connectoren sind geplant.

2. **Validieren der Datenaufnahme**: Stellen Sie sicher, dass Treueereignisse und Kundendaten nach Experience Platform fließen und in Journey Optimizer verfügbar sind.

Detaillierte Anweisungen finden Sie unter:

* [Dokumentation zu Experience Platform-Quellen](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Konfigurieren von Quell-Connectoren in Journey Optimizer](../start/get-started-sources.md)

### Erforderliche Berechtigungen {#required-permissions}

Um Herausforderungen im Zusammenhang mit der Treue nutzen zu können, benötigen Sie in Journey Optimizer die entsprechenden Berechtigungen. Wenden Sie sich an Ihren Administrator, wenn Sie auf die Funktion nicht zugreifen können.

## Herausforderungen beim Treueprogramm {#access}

So greifen Sie auf Herausforderungen im Zusammenhang mit der Treue zu:

1. Wählen Sie in Adobe Journey Optimizer **[!UICONTROL Navigationsmenü]** Herausforderungen bezüglich der Treue“ aus.

2. Im Inventar der Herausforderungen im Treueprogramm werden alle bestehenden Herausforderungen mit Informationen wie den folgenden angezeigt:
   * Name und Beschreibung der Herausforderung
   * Status (Entwurf, Live, gestoppt usw.)
   * Challenge-Typ (Standard, Streak, sequenziell)
   * Start- und Enddatum
   * Datum der letzten Änderung

3. Wählen Sie **[!UICONTROL Herausforderung erstellen]**, um eine neue Herausforderung zu erstellen.

### Herausforderungen beim Suchen und Filtern {#search-filter}

Verwenden Sie Such- und Filterfunktionen, um bestimmte Herausforderungen schnell zu finden:

* **Suche**: Geben Sie den Namen der Herausforderung oder Schlüsselwörter in das Suchfeld ein
* **Nach Status filtern**: Entwurf, geplant, live, abgeschlossen, gestoppt oder archiviert
* **Nach Typ filtern**: Standard-, Streak- oder sequenzielle Herausforderungen
* **Nach Datum filtern**: Herausforderungen innerhalb eines bestimmten Datumsbereichs
* **Nach Tags filtern**: Herausforderungen bei der Anwendung bestimmter Tags

## Nächste Schritte {#next-steps}

Nachdem Sie sich mit den Herausforderungen im Zusammenhang mit der Treue vertraut gemacht haben, erfahren Sie, wie Sie Ihre erste Herausforderung erstellen:

* [Herausforderungen schaffen](create-challenges.md)
* [Herausforderungen bewältigen](manage-challenges.md)
