---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 2dfcbd1631c7fefccaf02782a3218c9a1c1dc7aa
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 29%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats im [Versionshinweise](release-notes.md).

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise vom März 2024 {#e-2024}

**Veröffentlichungsdatum**: 19.-20. März 2024

### Neue Funktion {#e-features}

Mit dieser Version wird die neue Funktion im Folgenden beschrieben.

<table>
<thead>
<tr>
<th><strong>Codebasierte Erlebnisse</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem neuen code-basierten Erlebniskanal können Sie mit Adobe Journey Optimizer eine erweiterte Personalisierung und Tests für Ihre eingehenden Eigenschaften durchführen, um eine nahtlose Bereitstellung maßgeschneiderter Erlebnisse für verschiedene Touchpoints wie Web-Apps, mobile Apps, Desktop-Apps, Videokonsolen, TV-verbundene Geräte, Smart-TVs, Kiosks, ATMs, IoT-Geräte und mehr zu ermöglichen.</p>
<P>Die wichtigsten Funktionen ermöglichen Folgendes:</p>
<ul><li> Universelle Personalisierung: Erweiterung personalisierter Erlebnisse über alle Touchpoints hinweg, sodass eine kohärente und maßgeschneiderte Journey für Benutzer gewährleistet ist</li>
<li>Präzise Bearbeitungsgenauigkeit: Bearbeiten Sie bestimmte Inhalte an einzelnen Stellen in Ihren Apps oder Webseiten</li>
<li>Vielseitige Implementierung: Unterstützung für serverseitige, API-basierte oder SDK-basierte Implementierungsmethoden zur nahtlosen Integration in Ihre Entwicklungsumgebung.</li></ul></p>
<p>Weitere Informationen finden Sie in der <a href="../code-based/get-started-code-based.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Inhaltsvorlagen**

* **Miniaturen** - A **Rasteransicht** ist jetzt für Inhaltsvorlagen verfügbar und zeigt Miniaturansichten an, um den visuellen Zugriff zu verbessern. Derzeit werden nur E-Mail-HTML-Vorlagen unterstützt. [Weitere Informationen](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Diese Funktion wird mit begrenzter Verfügbarkeit (Limited Availability, LA) für eine kleine Gruppe von Kundinnen und Kunden veröffentlicht.

**Journeys**

Dem Journey-Authoring-Lebenszyklus wurden neue Zwischenstatus hinzugefügt:

* **Publishing** Status zwischen **Entwurf** und **Live** status
* **Anhalten** Status zwischen **Live** und **Angehalten** status
* **Aktivieren des Testmodus** oder **Deaktivieren des Testmodus** Status zwischen den **Entwurf** und **Entwurf (Test)** status

Wenn eine Journey in einem Zwischenzustand ist, ist sie schreibgeschützt.