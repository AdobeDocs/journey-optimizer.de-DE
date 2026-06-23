---
product: journey optimizer
title: inSegment
description: Erfahren Sie mehr über die Funktion „inSegment“
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment, Funktion, Ausdruck, Journey
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 33%

---

# inSegment {#inSegment}

Überprüft, ob eine Person zu einer bestimmten Zielgruppe gehört.

>[!NOTE]
>
>Sie können bis zu 100 Zielgruppen abrufen.

Der Zielgruppenname muss eine Zeichenfolgenkonstante sein. Er darf weder ein Feldverweis noch ein Ausdruck sein.

Zielgruppen werden in [Adobe Experience Platform](https://platform.adobe.com/audience/overview) definiert. Der Ausdruckseditor bietet eine automatisch ausgefüllte Zielgruppenliste.

Zielgruppen können zwei Status aufweisen:

* Realisiert: Entität qualifiziert sich für die Segmentdefinition.
* Ausgestiegen: Die Entität verlässt die Segmentdefinition.

Nur Personen mit dem Zielgruppenzugehörigkeitsstatus **Realisiert** werden als Mitglieder der Zielgruppe angesehen. Weitere Informationen zum Auswerten einer Zielgruppe finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/tutorials/evaluate-a-segment#interpret-segment-results).

`inSegment('segmentName') == true` bedeutet, dass Sie eine segmentMembership mit dem Status „eingetreten/vorhanden“ haben.

`inSegment('segmentName') == false` bedeutet, dass Sie über eine segmentMitgliedschaft mit dem Status „beendet“ haben.

## Kategorie

Adobe Experience Platform

## Funktionssyntax

`inSegment(<parameter>)`

## Parameter

| Parameter | Beschreibung | Typ |
|--- |--- |--- |
| Segment | Zielgruppenname | `<string>` |

## Signatur und zurückgegebener Typ

`inSegment(<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`inSegment("men over 50")`

Erklärung:

Die Funktion gibt &quot;**[!UICONTROL &quot; zurück]** wenn die Person in der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe „Männer über 50“ ist, **[!UICONTROL false]** andernfalls.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird die alte `inSegment` dokumentiert, die prüft, ob ein Journey-Profil zu einer benannten Adobe Experience Platform-Zielgruppe gehört, und einen booleschen Wert zurückgibt.

**intents:**
* Überprüfen Sie mithilfe von `inSegment`, ob ein Profil ein aktives Mitglied einer benannten Zielgruppe ist.
* Verwenden Sie `inSegment('name') == true`, um die realisierte (aktive) Zielgruppenzugehörigkeit in einer Journey-Bedingung zu bestätigen
* Verwenden Sie `inSegment('name') == false`, um die beendete (inaktive) Zielgruppenzugehörigkeit zu bestätigen

**Glossar:**
* **Realisiert**: Status der Zielgruppenbeteiligung bedeutet, dass die Entität derzeit für die Segmentdefinition qualifiziert ist *(produktspezifisch)*
* **Ausgetreten**: Status der Zielgruppenbeteiligung, d. h. die Entität verlässt die Segmentdefinition *produktspezifisch)*

**Leitplanken:**
* Auf einer Journey können bis zu 100 Zielgruppen abgerufen werden
* Der Zielgruppenname muss eine Zeichenfolgenkonstante sein. Feldverweise und -ausdrücke werden nicht als Parameter unterstützt

**Terminologie:**
* Kanonischer Name: inSegment — Akronym: none — Varianten: inAudience (aktuelle bevorzugte Funktion)
* Synonyme: „inSegment“ = „Prüfung der Zielgruppenzugehörigkeit“ (veraltet)
* Verwechseln Sie nicht: „inSegment“ (alte/veraltete Funktion) ≠ „inAudience“ (aktuelle empfohlene Funktion)
* Verwechseln Sie nicht: „realized“ (aktives Mitglied) ≠ „exited“ (kein Mitglied mehr)

**FAQ:**
* **F: Was ist der Unterschied zwischen `inSegment` und `inAudience`?** — `inSegment` ist der Name der alten Funktion; `inAudience` ist die derzeit empfohlene Funktion. Beide prüfen die Zugehörigkeit zur Zielgruppe, `inAudience` bietet jedoch eine umfassendere Dokumentation mit Leitplanken und Details zum Propagierungs-Timing.
* **Q: Was bedeutet `inSegment('name') == true`?** — Dies bedeutet, dass das Profil einen „realisierten“ segmentMembership-Status hat, d. h., dass die Person ein aktives Mitglied der Zielgruppe ist.
* **F: Kann ich einen dynamischen Ausdruck als Zielgruppennamen übergeben?** — Nein, der Zielgruppenname muss eine Zeichenfolgenkonstante sein. Feldverweise und -ausdrücke werden nicht unterstützt.
* **F: Wie viele Zielgruppen kann ich auf einer Journey auswerten?** — Auf einer Journey können bis zu 100 Zielgruppen abgerufen werden.

+++
