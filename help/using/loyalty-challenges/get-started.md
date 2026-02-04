---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Herausforderungen im Zusammenhang mit dem Treueprogramm erstellen und verwalten, um ansprechende Treueprogramme zu erstellen.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 4%

---


# Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* **Erste Schritte mit den Herausforderungen im Zusammenhang mit der Treue** ◀︎ **Sie sind hier** - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treueprogrammen](access-loyalty-challenges.md) - Inventar und Filterung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* [Herausforderungen verwalten](manage-challenges.md) - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Über Herausforderungen im Zusammenhang mit der Treue"
>abstract="Mit den Herausforderungen im Zusammenhang mit der Treue können Sie personalisierte Interaktionsangebote erstellen, die Kunden dazu motivieren, bestimmte Aktionen durchzuführen und Belohnungen zu sammeln."

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

## Überblick {#overview}

Die Herausforderungen im Zusammenhang mit dem Treueprogramm bieten eine Komplettlösung für die Erstellung von Treueprogrammen in großem Maßstab, von der Definition von Aufgaben und Meilensteinen bis hin zur Bereitstellung von Inhalten und zur kanalübergreifenden Verfolgung der Leistung. Sie können drei Arten von Challenge-Erlebnissen erstellen, Belohnungen konfigurieren, Multi-Channel-Benachrichtigungen in wichtigen Lebenszyklusphasen senden und die Leistung mithilfe automatisch generierter Journey überwachen - und das alles unter Beibehaltung der Integration mit Ihrem externen Treueprogramm-System.

## Wichtigste Funktionen {#key-capabilities}

Herausforderungen im Zusammenhang mit der Treue nutzen, um:

* **Erstellen Sie drei Arten von Herausforderungen**:
   * **Standard**: Kunden führen eine beliebige Anzahl von Aufgaben aus, um Prämien zu erhalten
   * **Streak**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus
   * **Sequenziell**: Kunden führen Aufgaben in einer bestimmten Reihenfolge aus

* **Design Challenge-Inhalte**: Verwenden Sie Journey Optimizer-Inhaltskarten, um die visuelle Darstellung Ihrer Challenge auf Kundengeräten zu erstellen. Inhaltskarten zeigen Informationen zur Herausforderung, den Fortschritt und die Belohnungen an.

* **Aufgabenanforderungen einrichten** Definieren Sie, was Kunden tun müssen, um Prämien zu verdienen, darunter:
   * Aufgabentypen (Kauf, Ausgabenbetrag, Besuch, Interaktion, benutzerdefinierte Ereignisse)
   * Mengenbedarf
   * Produkteinschlüsse/-ausschlüsse mithilfe von SKUs, Kategorien oder Attributen
   * Benutzerdefinierte Attribute und Bedingungen

* **Belohnungen konfigurieren**: Belohnungen definieren, die Kunden entweder bei Aufgabenabschluss (progressive Belohnungen) oder nach Abschluss der gesamten Challenge (endgültige Belohnungen) erhalten.

* **Multi-Channel-Benachrichtigungen senden**: Versand von Nachrichten über mehrere Kanäle (In-App, E-Mail, Push) in wichtigen Phasen:
   * **Launch**: Wenn die Challenge beginnt
   * **In Bearbeitung**: Wenn Kundinnen und Kunden teilweise durchgekommen sind
   * **Abschließen**: Wenn Kunden die Challenge abgeschlossen haben

* **Performance verfolgen** Überwachen automatisch generierter Journeys und Überprüfen der Challenge-Performance mithilfe integrierter Berichte.

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

### Zielgruppen {#target-audiences}

Erstellen Sie Zielgruppen in Experience Platform, bevor Sie Herausforderungen schaffen. Sie können vorhandene Zielgruppen auswählen, aber keine neuen Zielgruppen über die Benutzeroberfläche „Herausforderungen im Zusammenhang mit dem Treueprogramm“ erstellen.

## Wichtige Einschränkungen {#limitations}

* **Kein Sachkontensystem**: Treueprobleme verfolgen keine Geldwerte oder Punktesalden. Wenn Kundinnen und Kunden eine Challenge abschließen und eine Belohnung erhalten, ruft Journey Optimizer Ihr externes Treueprogramm-Management-System an, um die Punktzuweisung zu bearbeiten.

* **Nur Zielgruppenauswahl**: Sie können vorhandene Zielgruppen auswählen, aber keine neuen Zielgruppen über die Benutzeroberfläche „Herausforderungen im Treueprogramm“ erstellen.

## Nächste Schritte {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Zugriff auf Herausforderungen im Zusammenhang mit Treue</strong></a>
    </div>
    <p>
    <em>Erfahren Sie, wie Sie auf die Herausforderungen im Zusammenhang mit der Bestandsaufnahme und der Filterung zugreifen können</em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>Herausforderungen schaffen</strong></a>
    </div>
    <p>
    <em>Erstellen und konfigurieren Sie Ihre erste Herausforderung bezüglich der Treue</em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>Verwalten von Herausforderungen</strong></a>
    </div>
    <p>
    <em>Herausforderungen bearbeiten, überwachen und optimieren</em>
    <p>
  </td>
</tr>
</table>
