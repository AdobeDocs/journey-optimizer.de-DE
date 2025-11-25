---
product: journey optimizer
title: Funktion „inAudience“
description: Erfahren Sie mehr über die Funktion „inAudience“ von Adobe Experience Platform
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, Funktion, Ausdruck, Journey, Zielgruppe, Segmentierung
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 4f653c0bd3f6998dd54deeae996b7b0427a1744e
workflow-type: ht
source-wordcount: '600'
ht-degree: 100%

---

# Funktion „inAudience“ {#inAudience}

Die Funktion `inAudience` ist eine Adobe Experience Platform-Funktion, mit der Sie überprüfen können, ob ein Kontakt in Ihrer Journey zu einer bestimmten Zielgruppe gehört. Mit dieser leistungsstarken Funktion können Sie personalisierte Journey-Pfade basierend auf der Zielgruppenzugehörigkeit erstellen und ermöglichen dadurch anspruchsvolle Segmentierung und anspruchsvolles Targeting in Ihren Kundenerlebnissen.

Verwenden Sie die Funktion `inAudience`, wenn Sie Folgendes tun müssen:

* Journey-Pfade basierend auf der Zielgruppenzugehörigkeit verzweigen. [Weitere Informationen](../condition-activity.md#using-a-segment)
* Bedingte Logik anwenden, die davon abhängt, ob ein Profil zu einem bestimmten Segment gehört
* Bestimmte Zielgruppen von Kundinnen und Kunden mit personalisierten Erlebnissen ansprechen
* Echtzeit-Zielgruppenbeteiligung unter Journey-Bedingungen auswerten
* Mehrere Zielgruppenprüfungen kombinieren, um komplexe Zielgruppenbestimmungsregeln zu erstellen

Die Funktion wertet die Zielgruppenzugehörigkeit in Echtzeit aus und gibt einen booleschen Wert zurück, wodurch sie sich ideal für Entscheidungsknoten und bedingte Ausdrücke eignet. Zielgruppen werden in [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} definiert und verwaltet (weitere Informationen zum [Arbeiten mit Zielgruppen](../../audience/about-audiences.md) in Journey Optimizer). Der Ausdruckseditor bietet automatische Vervollständigungsvorschläge, um Ihnen eine genaue Referenzierung zu erleichtern.

**Zielgruppenstatus:**

Zielgruppen können zwei Beteiligungsstatus aufweisen:

* **Realisiert**: Der Kontakt qualifiziert sich für die Zielgruppendefinition und ist ein aktives Mitglied
* **Ausgestiegen**: Der Kontakt hat die Zielgruppe verlassen und ist nicht mehr qualifiziert

Nur Kontakte mit dem Status **Realisiert** werden als aktive Zielgruppenmitglieder betrachtet. Wenn die Funktion `true` zurückgibt, bestätigt sie, dass der Kontakt den Status „Realisiert“ hat. Wenn sie `false` zurückgibt, zeigt dies den Status „Ausgestiegen“ an. Weitere Informationen zur Zielgruppenauswertung finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results){target="_blank"}.

+++Syntax

`inAudience(<parameter>)`

+++

+++Parameter

| Parameter | Beschreibung | Typ |
|--- |--- |--- |
| Zielgruppe | Der Zielgruppenname | `<string>` |

**Wichtige Einschränkungen:**

* Der Zielgruppenname muss eine Zeichenfolgenkonstante sein
* Er kann kein Feldverweis oder Ausdruck sein
* Sie können bis zu 100 Zielgruppen in einer einzelnen Journey abrufen

+++

+++Signatur und zurückgegebener Typ

`inAudience(<string>)`

Gibt einen booleschen Wert zurück:
* `true`: Der Kontakt ist Mitglied der Zielgruppe (Status „Realisiert“)

* `false`: Der Kontakt ist kein Mitglied der Zielgruppe (Status „Ausgestiegen“)

+++

+++Beispiele

`inAudience("men over 50")`

Gibt **wahr** zurück, wenn der Kontakt innerhalb der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe „men over 50“ (Männer über 50) ist. Andernfalls wird **falsch** zurückgegeben.

**Praktische Anwendungsfälle:**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## Leitlinien und Einschränkungen {#guardrails}

Beachten Sie bei Verwendung der Funktion `inAudience` in Ihren Journeys die folgenden Leitlinien und Einschränkungen:

**Beschränkung für Zielgruppenabrufe:**
* Sie können bis zu 100 Zielgruppen in einer einzelnen Journey abrufen
* Der Ausdruckseditor stellt eine automatisch vervollständigte Liste verfügbarer Zielgruppen bereit, um Ihnen deren korrekte Referenzierung zu erleichtern

**Parametereinschränkungen:**
* Der Zielgruppenname muss eine Zeichenfolgenkonstante sein
* Feldverweise und Ausdrücke werden nicht als Parameter unterstützt

**Änderungen des Zielgruppennamens:**
* Wenn Sie den Namen einer bestehenden Zielgruppe in Adobe Experience Platform ändern, werden die Verweise auf diese Zielgruppe in Ihren Journey-Ausdrücken nicht automatisch aktualisiert. 
* Wenn Ihr Bedingungsknoten `inAudience('oldAudienceName')` verwendet, müssen Sie den Ausdruck manuell bearbeiten, damit der neue Name verwendet wird.
* Wenn der Zielgruppenname nicht aktualisiert wird, funktioniert die Journey-Bedingung nicht mehr, was zu falschem Journey-Verhalten führen kann

**Überlegungen zur Zusammenführungsrichtlinie:**
* Beim Verwenden mehrerer Zielgruppen mit der Funktion `inAudience` können Inkonsistenzen mit Zusammenführungsrichtlinien zu Fehlern oder Warnhinweisen führen
* Weitere Informationen zum Verhalten von Zusammenführungsrichtlinien finden Sie unter [Journey-Eigenschaften](../journey-properties.md).

## Verwandte Themen

Weitere Informationen zur Verwendung von Zielgruppen in Adobe Journey Optimizer:

* **[Informationen zu Zielgruppen](../../audience/about-audiences.md)**: Erfahren Sie, wie Zielgruppen in Adobe Experience Platform und Journey Optimizer funktionieren, einschließlich ihrer Erstellung und Verwaltung
* **[Aktivität „Zielgruppe lesen“](../read-audience.md)**: Verwenden Sie Zielgruppen, um den Journey-Eintritt auszulösen und alle Mitglieder der Zielgruppe zum Eintritt in eine Journey zu bewegen
* **[Zielgruppenqualifizierungsereignisse](../audience-qualification-events.md)**: Überwachen Sie Zielgruppeneintritte und -austritte von Profilen, um Journey-Aktionen in Echtzeit auszulösen
* **[Verwenden von Zielgruppen in Bedingungen](../condition-activity.md#using-a-segment)**: Erstellen Sie bedingte Journey-Pfade basierend auf der Zielgruppenzugehörigkeit mithilfe der Aktivität „Bedingung“
* **[Journey-Eigenschaften – Zusammenführungsrichtlinien](../journey-properties.md)**: Erfahren Sie, wie Zusammenführungsrichtlinien funktionieren, wenn mehrere Zielgruppen mit der Funktion „inAudience“ verwendet werden

