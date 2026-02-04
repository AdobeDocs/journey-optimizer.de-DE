---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Herausforderungen im Zusammenhang mit Treueprogrammen erstellen und verwalten, um ansprechende Treueprogramme zu erstellen.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: e683461c6adbf45cacb30692e23927175685f9fb
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 4%

---


# Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* **Erste Schritte mit den Herausforderungen im Zusammenhang mit der Treue** ◀︎ **Sie sind hier** - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treue aufrufen und verwalten](access-loyalty-challenges.md) - Inventar-, Herausforderungen- und Aufgabenverwaltung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Überblick {#overview}

Herausforderungen im Zusammenhang mit dem Treueprogramm bieten eine Komplettlösung für die Erstellung von Treueprogrammen in großem Umfang, von der Festlegung von Aufgaben und Meilensteinen bis hin zur Bereitstellung von Inhalten und zur kanalübergreifenden Verfolgung der Leistung.

![](assets/challenges-gs.png)

Sie können drei Arten von Herausforderungen erstellen:

* **Standardherausforderungen**: Kunden führen eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus\
  *Beispiel: 3 von 5 verfügbaren Aufgaben abschließen*

* **Streak Challenges**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus\
  *Beispiel: Tätigen Sie einen Kauf an 7 aufeinander folgenden Tagen*

* **Sequenzielle Herausforderungen**: Kunden führen Aufgaben in einer definierten Reihenfolge aus\
  *Beispiel: → erwerben → überprüfen (muss in dieser Reihenfolge ausgefüllt werden)*

Mit Loyalty Challenges können Sie Prämien konfigurieren, Multi-Channel-Benachrichtigungen in wichtigen Lebenszyklusphasen senden und automatisch generierte Journey verwenden - und dabei die Integration in Ihr externes Treueprogramm-Management-System beibehalten.

## Funktionsweise {#how-it-works}

Dieser Workflow ermöglicht das Erstellen und Starten einer Herausforderung zum Treueprogramm:

1. **Datenaufnahme einrichten** - Konfigurieren Sie Experience Platform-Quell-Connectoren (z. B. den [Kapillaren-Connector](https://experienceleague.adobe.com/de/docs/experience-platform/sources/home#loyalty), um Treueprogramm-Ereignisdaten aufzunehmen, mit denen Kundenaktionen und -fortschritt verfolgt werden. Diese Daten ermöglichen das Challenge-Tracking und die Aufgabenerledigung.

1. **Herausforderung erstellen** - Definiert die grundlegenden Eigenschaften der Herausforderung, einschließlich Name, Typ (Standard, Streak oder Sequenziell) und Datumsbereich.

1. **Aufgaben hinzufügen** - Definiert die spezifischen Aktionen, die Kunden durchführen müssen, einschließlich Aufgabentypen (Kauf, Ausgaben), Mengen, Produktfiltern und Belohnungen.

1. **Erstellen von Inhaltskarten** - Erstellen Sie die visuelle Darstellung Ihrer Challenge mit Journey Optimizer-Inhaltskarten, die auf Kundengeräten angezeigt werden. Inhaltskarten zeigen Informationen zu Herausforderungen, Fortschritt und Belohnungen an.

1. **Messaging konfigurieren** (Optional) - Richten Sie Multi-Channel-Nachrichten (In-App, E-Mail, Push) für wichtige Lebenszyklusphasen ein: Start, in Bearbeitung und Abschluss.

1. **Ziel-Audience auswählen** - Definieren Sie, welche Kunden an Ihrer Challenge teilnehmen können, indem Sie eine Audience aus Adobe Experience Platform auswählen.

1. **Journey veröffentlichen** - Journey Optimizer generiert automatisch eine Journey für Ihre Challenge. Navigieren Sie zum Journey-Inventar und veröffentlichen Sie die automatisch generierte Journey, um die Challenge für Kunden verfügbar zu machen.

Detaillierte schrittweise Anweisungen finden Sie unter [Erstellen von Herausforderungen](create-challenges.md).

## Voraussetzungen {#prerequisites}

Bevor Sie Herausforderungen im Zusammenhang mit dem Treueprogramm nutzen, stellen Sie Folgendes sicher:

+++Einrichtung der Datenaufnahme

Herausforderungen im Zusammenhang mit der Kundentreue beruhen auf Daten, die über Experience Platform-Quell-Connectoren aufgenommen werden, um den Kundenfortschritt und den Abschluss von Aufgaben zu verfolgen.

1. **Konfigurieren eines unterstützten Quell-Connectors**: Derzeit ist der Kapillaranschluss verfügbar. Weitere Connectoren sind für zukünftige Versionen geplant. [Erfahren Sie mehr über Quell-Connectoren für Treueprogramme](https://experienceleague.adobe.com/de/docs/experience-platform/sources/home#loyalty).

1. **Validieren der Datenaufnahme**: Stellen Sie sicher, dass Treueereignisse und Kundendaten nach Experience Platform fließen und in Journey Optimizer verfügbar sind. Vergewissern Sie sich, dass das Datenschema die erforderlichen Felder zum Tracking von Kundenaktionen und -fortschritten enthält.

Detaillierte Anweisungen finden Sie unter [Übersicht über Experience Platform-Quellen](https://experienceleague.adobe.com/de/docs/experience-platform/sources/home)

+++

+++Erforderliche Berechtigungen

Um Herausforderungen im Zusammenhang mit der Treue nutzen zu können, benötigen Sie in Journey Optimizer die entsprechenden Berechtigungen. Zu den erforderlichen Berechtigungen gehören:

* Zugriff auf die Funktion **[!UICONTROL Herausforderungen im Zusammenhang mit dem Treueprogramm (Beta]**
* Berechtigungen zum Erstellen und Verwalten von Journey
* Berechtigungen zum Erstellen und Verwalten von Inhaltskarten
* Berechtigungen zum Erstellen und Verwalten von Zielgruppen

Wenden Sie sich an Ihren Administrator, wenn Sie die Funktion nicht nutzen können oder zusätzliche Berechtigungen benötigen.

+++

+++Zielgruppe

Definieren Sie eine Zielgruppe, die angibt, welche Kundinnen und Kunden für die Teilnahme an Ihren Herausforderungen im Zusammenhang mit der Treue infrage kommen. Sie können bestehende Audiences auswählen oder neue Audiences direkt über die Benutzeroberfläche zur Challenge-Erstellung erstellen. [Erfahren Sie, wie Sie mit Audiences arbeiten](../audience/about-audiences.md).

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
    <em>Definieren von Aktionen, die für Herausforderungen abgeschlossen werden sollen</em>
    </p>
  </td>
</tr>
</table>
