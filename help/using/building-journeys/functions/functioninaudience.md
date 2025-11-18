---
product: journey optimizer
title: inAudience-Funktion
description: Erfahren Sie mehr über die Funktion "Adobe Experience Platform inAudience“
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, Funktion, Ausdruck, Journey, Zielgruppe, Segmentierung
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 4f653c0bd3f6998dd54deeae996b7b0427a1744e
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 4%

---

# inAudience-Funktion {#inAudience}

Die `inAudience` ist eine Adobe Experience Platform-Funktion, mit der Sie überprüfen können, ob ein Kontakt in Ihrem Journey zu einer bestimmten Zielgruppe gehört. Mit dieser leistungsstarken Funktion können Sie personalisierte Journey-Pfade erstellen, die auf der Zielgruppenzugehörigkeit basieren, und so eine ausgefeilte Segmentierung und Zielgruppenbestimmung in Ihren Kundenerlebnissen ermöglichen.

Verwenden Sie die `inAudience`, wenn Sie Folgendes tun müssen:

* Verzweigen Sie Journey-Pfade basierend auf der Zielgruppenzugehörigkeit. [Weitere Informationen](../condition-activity.md#using-a-segment)
* Anwenden einer bedingten Logik, die davon abhängt, ob ein Profil zu einem bestimmten Segment gehört
* Targeting bestimmter Kundengruppen mit personalisierten Erlebnissen
* Auswerten der Echtzeit-Zielgruppenbeteiligung unter Journey-Bedingungen
* Kombinieren Sie mehrere Zielgruppenprüfungen, um komplexe Zielgruppenbestimmungsregeln zu erstellen

Die Funktion bewertet die Zielgruppenzugehörigkeit in Echtzeit und gibt einen booleschen Wert zurück, was sie ideal für Entscheidungsknoten und bedingte Ausdrücke macht. Zielgruppen werden in [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} definiert und verwaltet (weitere Informationen zum [Arbeiten mit Zielgruppen](../../audience/about-audiences.md) in Journey Optimizer), und der Ausdruckseditor bietet Vorschläge für die automatische Vervollständigung, damit Sie sie genau referenzieren können.

**Zielgruppenstatus:**

Zielgruppen können zwei Teilnahmestatus haben:

* **Realisiert**: Der Kontakt qualifiziert sich für die Zielgruppendefinition und ist ein aktives Mitglied
* **Ausgetreten**: Der Kontakt hat die Zielgruppe verlassen und ist nicht mehr qualifiziert

Nur Personen mit dem **Realisiert**-Status werden als aktive Zielgruppenmitglieder betrachtet. Wenn die Funktion `true` zurückgibt, bestätigt sie, dass die Person einen realisierten Status hat. Wenn sie `false` zurückgibt, zeigt sie den Status „Beendet“ an. Weitere Informationen zur Auswertung von Audiences finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results){target="_blank"}.

+++Syntax

`inAudience(<parameter>)`

+++

+++Parameter

| Parameter | Beschreibung | Typ |
|--- |--- |--- |
| Zielgruppe | Zielgruppenname | `<string>` |

**Wichtige Einschränkungen:**

* Der Zielgruppenname muss eine Zeichenfolgenkonstante sein
* Es kann sich nicht um einen Feldverweis oder einen Ausdruck handeln
* Sie können auf einer Journey bis zu 100 Zielgruppen abrufen

+++

+++Signatur und zurückgegebener Typ

`inAudience(<string>)`

Gibt einen booleschen Wert zurück:
* `true`: Der Kontakt ist Mitglied der Zielgruppe (realisierter Status)

* `false`: Der Kontakt ist kein Mitglied der Zielgruppe (Status „beendet„)

+++

+++Beispiele

`inAudience("men over 50")`

Gibt **true** zurück, wenn die Person in der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe „Männer über 50“ ist, **false** andernfalls.

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

Beachten Sie bei Verwendung der `inAudience` in Ihren Journey die folgenden Leitplanken und Einschränkungen:

**Limit für Zielgruppenabrufe:**
* Sie können in einem Journey bis zu 100 Zielgruppen abrufen
* Der Ausdruckseditor bietet eine automatisch vervollständigte Liste der verfügbaren Zielgruppen, damit Sie sie korrekt referenzieren können

**Parameterbegrenzungen:**
* Der Zielgruppenname muss eine Zeichenfolgenkonstante sein
* Feldverweise und -ausdrücke werden nicht als Parameter unterstützt

**Änderungen am Zielgruppennamen:**
* Durch das Ändern des Namens einer bestehenden Zielgruppe in Adobe Experience Platform werden Verweise auf diese Zielgruppe in Ihren Journey-Ausdrücken nicht automatisch aktualisiert
* Wenn Ihr Bedingungsknoten `inAudience('oldAudienceName')` verwendet, müssen Sie den Ausdruck manuell bearbeiten, um den neuen Namen zu verwenden
* Wenn der Zielgruppenname nicht aktualisiert wird, funktioniert die Journey-Bedingung nicht mehr, was zu falschem Journey-Verhalten führen kann

**Überlegungen zur Zusammenführungsrichtlinie:**
* Bei Verwendung mehrerer Zielgruppen mit der `inAudience`-Funktion können Inkonsistenzen mit Zusammenführungsrichtlinien zu Fehlern oder Warnhinweisen führen
* Siehe [Journey-Eigenschaften](../journey-properties.md) für weitere Informationen zum Verhalten von Zusammenführungsrichtlinien

## Verwandte Themen

Weitere Informationen zur Verwendung von Zielgruppen in Adobe Journey Optimizer:

* **[Über Zielgruppen](../../audience/about-audiences.md)** - Erfahren Sie, wie Zielgruppen in Adobe Experience Platform und Journey Optimizer funktionieren, einschließlich ihrer Erstellung und Verwaltung
* **[Aktivität „Zielgruppe lesen](../read-audience.md)** - Zielgruppen verwenden, um einen Journey-Eintrag zu Triggern und alle Mitglieder der Zielgruppe zum Eintritt in eine Journey zu bewegen
* **[Zielgruppen-Qualifizierungsereignisse](../audience-qualification-events.md)** - Überwachen von Profileintritten und -austritten aus Zielgruppen in Trigger-Journey-Aktionen in Echtzeit
* **[Verwenden von Zielgruppen in Bedingungen](../condition-activity.md#using-a-segment)** - Erstellen bedingter Journey-Pfade basierend auf der Zielgruppenzugehörigkeit mithilfe der Aktivität „Bedingung“
* **[Journey-Eigenschaften - Zusammenführungsrichtlinien](../journey-properties.md)** - Erfahren Sie, wie Zusammenführungsrichtlinien funktionieren, wenn mehrere Zielgruppen mit der inAudience-Funktion verwendet werden

