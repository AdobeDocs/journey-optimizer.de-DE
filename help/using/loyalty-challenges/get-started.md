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
source-git-commit: bd98e4dc77a0adde83df6251af749aa6da8c058d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 4%

---


# Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* **Erste Schritte mit den Herausforderungen im Zusammenhang mit der Treue** ◀︎ **Sie sind hier** - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treueprogrammen](access-loyalty-challenges.md) - Inventar und Filterung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren
* [Herausforderungen verwalten](manage-challenges.md) - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Überblick {#overview}

Herausforderungen im Zusammenhang mit dem Treueprogramm bieten eine Komplettlösung für die Erstellung von Treueprogrammen in großem Umfang, von der Festlegung von Aufgaben und Meilensteinen bis hin zur Bereitstellung von Inhalten und zur kanalübergreifenden Verfolgung der Leistung.

Sie können drei Arten von Herausforderungen erstellen:

* **Standardherausforderungen**: Kunden führen eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus
* **Streak Challenges**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus
* **Sequenzielle Herausforderungen**: Kunden führen Aufgaben in einer definierten Reihenfolge aus

Mit den Herausforderungen im Zusammenhang mit dem Treueprogramm können Sie Prämien konfigurieren, Multi-Channel-Benachrichtigungen in wichtigen Lebenszyklusphasen senden und die Leistung mithilfe automatisch generierter Journey überwachen. Dabei bleibt die Integration in Ihr externes Treueprogramm-Management-System erhalten.

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## Funktionsweise {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

Dieser Workflow ermöglicht das Erstellen und Starten einer Herausforderung zum Treueprogramm:

1. **Datenaufnahme einrichten** - Konfigurieren Sie Quell-Connectoren für Experience Platform (z. B. den Kapillaren-Connector), um Treueprogramm-Ereignisdaten aufzunehmen, mit denen Kundenaktionen und -fortschritt verfolgt werden. Diese Daten ermöglichen das Challenge-Tracking und die Aufgabenerledigung.

1. **Herausforderung erstellen** - Definiert die grundlegenden Eigenschaften der Herausforderung, einschließlich Name, Typ (Standard, Streak oder Sequenziell), Zielgruppe und Datumsbereich. Detaillierte [&#x200B; finden Sie &#x200B;](create-challenges.md) „Erstellen von Herausforderungen“.

1. **Aufgaben hinzufügen** - Definieren Sie die spezifischen Aktionen, die Kundinnen und Kunden durchführen müssen, einschließlich Aufgabentypen (Kauf, Ausgaben, Besuch, Interaktion, benutzerdefinierte Ereignisse), Mengen, Produktfilter und Belohnungen. Detaillierte Anweisungen finden [&#x200B; unter &#x200B;](create-tasks.md)Erstellen von Aufgaben“.

1. **Erstellen von Inhaltskarten** - Erstellen Sie die visuelle Darstellung Ihrer Challenge mit Journey Optimizer [Inhaltskarten](../content-card/create-content-card.md) die auf Kundengeräten angezeigt werden. Inhaltskarten zeigen Informationen zu Herausforderungen, Fortschritt und Belohnungen an.

1. **Messaging konfigurieren** (Optional) - Richten Sie Multi-Channel-Nachrichten ([In-App](../in-app/get-started-in-app.md), [Email](../email/get-started-email.md), [Push](../push/get-started-push.md)) für wichtige Lebenszyklusphasen ein: Start, in Bearbeitung und Abschluss.

1. **Überprüfen und veröffentlichen** - Testen Sie Ihre Herausforderung mit [Testprofilen](../test-approve/test-profiles.md) und veröffentlichen Sie sie dann, um sie für Ihre Zielgruppe verfügbar zu machen.

1. **Journey aktivieren** - Wenn Sie eine Challenge veröffentlichen, erstellt Journey Optimizer automatisch eine [Journey](../building-journeys/journey-gs.md) im Entwurfsstatus, die die Bereitstellung und das Messaging von Inhaltskarten koordiniert. Navigieren Sie zum Journey-Inventar, suchen Sie die automatisch generierte Journey (namens „Challenge: [Challenge Name]„) und [aktivieren Sie sie](../building-journeys/publishing-the-journey.md) um die Challenge für Ihre Kunden verfügbar zu machen.

1. **Leistung überwachen** - Verfolgen Sie Teilnahme, Abschlussraten, Belohnungsverteilung und Nachrichteninteraktion durch integrierte Berichte und die Journey-Arbeitsfläche. Siehe [Verwalten von Herausforderungen](manage-challenges.md) für Details zur Überwachung.

## Voraussetzungen {#prerequisites}

Bevor Sie Herausforderungen im Zusammenhang mit dem Treueprogramm nutzen, stellen Sie Folgendes sicher:

+++Einrichtung der Datenaufnahme

Herausforderungen im Zusammenhang mit der Kundentreue beruhen auf Daten, die über Experience Platform-Quell-Connectoren aufgenommen werden, um den Kundenfortschritt und den Abschluss von Aufgaben zu verfolgen.

1. **Konfigurieren eines unterstützten Quell-Connectors**: Derzeit ist der Kapillaranschluss allgemein verfügbar. Weitere Connectoren sind für zukünftige Versionen geplant.

1. **Validieren der Datenaufnahme**: Stellen Sie sicher, dass Treueereignisse und Kundendaten nach Experience Platform fließen und in Journey Optimizer verfügbar sind. Vergewissern Sie sich, dass das Datenschema die erforderlichen Felder zum Tracking von Kundenaktionen und -fortschritten enthält.

Detaillierte Anweisungen finden Sie unter:

* [Dokumentation zu Experience Platform-Quellen](https://experienceleague.adobe.com/de/docs/experience-platform/sources/home)
* [Konfigurieren von Quell-Connectoren in Journey Optimizer](../start/get-started-sources.md)

+++

+++Erforderliche Berechtigungen

Um Herausforderungen im Zusammenhang mit der Treue nutzen zu können, benötigen Sie in Journey Optimizer die entsprechenden Berechtigungen. Zu den erforderlichen Berechtigungen gehören:

* Zugriff auf die Funktion **[!UICONTROL Herausforderungen im Zusammenhang mit]** Treue“
* Berechtigungen zum Erstellen und Verwalten von Journey
* Berechtigungen zum Erstellen und Verwalten von Inhaltskarten
* Berechtigungen zum Erstellen und Verwalten von Zielgruppen

Wenden Sie sich an Ihren Administrator, wenn Sie die Funktion nicht nutzen können oder zusätzliche Berechtigungen benötigen.

+++

+++Zielgruppen

Erstellen Sie Zielgruppen in Experience Platform, bevor Sie Herausforderungen schaffen. Diese Zielgruppen definieren, welche Kundinnen und Kunden für die Teilnahme an Ihren Herausforderungen im Zusammenhang mit der Treue infrage kommen. Weitere Informationen zum Erstellen von Zielgruppen finden Sie unter [Erste Schritte mit Zielgruppen](../audience/about-audiences.md).

+++

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
    </p>
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
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>Aufgaben erstellen</strong></a>
    </div>
    <p>
    <em>Aktionen und Belohnungen für Herausforderungen definieren</em>
    </p>
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
    </p>
  </td>
</tr>
</table>
