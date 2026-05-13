---
solution: Journey Optimizer
product: journey optimizer
title: Aktivität „Optimieren“
description: Weitere Informationen zur Aktivität „Optimieren“
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Aktivität, Bedingung, Arbeitsfläche, Journey, Optimierung
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/hbDoGEHdCBcOe-e9h06kGY2Rvb129cIzto6jJAuGkX4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 470
ht-degree: 41%

---

# Erste Schritte mit der Aktivität „Optimieren“ {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Aktivität „Optimieren“"
>abstract="Mit der Aktivität **Optimieren** können Sie festlegen, wie Einzelpersonen Ihre Journey durchlaufen, indem Sie mehrere Pfade auf der Grundlage spezifischer Kriterien erstellen, darunter Experimente, Targeting und bestimmte Bedingungen. Beachten Sie, dass **Aktivität „Optimieren** das neue Vehikel zum Erstellen bedingter Pfade in Journey ist. Sie ersetzt die frühere Aktivität **Bedingung**."

>[!IMPORTANT]
>
>Die Aktivität **Optimieren** ist das neue Vehikel zum Erstellen bedingter Pfade in Journey. Sie ersetzt die frühere Aktivität **Bedingung**, die aus der Benutzeroberfläche entfernt wurde. Die gesamte bedingte Logik wird beibehalten und jetzt über die [Bedingungen **der Aktivität** Optimieren](conditions.md) verarbeitet.
>
>Wenn Sie über Journey verfügen, die **[!UICONTROL Bedingungs]**-Aktivitäten verwendet haben, können Sie diese weiterhin wie zuvor verwenden. Sie werden jetzt mit einem neuen Symbol als **[!UICONTROL Optimieren]**-Aktivitäten mit der **[!UICONTROL Bedingung]**-Methode angezeigt, das Verhalten ist jedoch unverändert. Jede benutzerdefinierte Beschriftung, die Sie auf dem Knoten festgelegt hatten, wird beibehalten.

Mit der Aktivität **Optimieren** können Sie festlegen, wie Einzelpersonen Ihre Journey durchlaufen, indem Sie mehrere **Pfade** auf der Grundlage spezifischer Kriterien erstellen, darunter Experimente, Targeting und bestimmte Bedingungen. So gewährleisten Sie ein Höchstmaß an Engagement und Erfolg, um hochgradig personalisierte und effektive Journeys zu erstellen.

![Schaltfläche „Optimieren“ in der Palette „Journey-Aktivität“](assets/journey-optimize.png)

## Was ist ein Journey-Pfad? {#journey-path}

Ein Journey-**Pfad** kann aus beliebigen der folgenden Variablen bestehen: Sequenzierung von Nachrichten, dazwischen liegende Zeit, Anzahl der Nachrichten oder eine beliebige Kombination dieser drei Variablen.

Ein Pfad kann beispielsweise eine E-Mail enthalten, ein anderer zwei SMS-Nachrichten und ein dritter eine E-Mail, einen Knoten, um zwei Stunden zu warten, und dann eine SMS-Nachricht.

## Drei Möglichkeiten zur Optimierung Ihrer Journey {#optimization-methods}

Durch die Aktivität **Optimieren** können Sie die folgenden Aktionen für Ihre Journey-Pfade ausführen:

* [Pfadexperimente ausführen](path-experimentation.md) - Testen Sie verschiedene Pfade basierend auf zufälligen Aufspaltungen, um anhand vordefinierter Erfolgsmetriken (z. B. Konversionsrate, Umsatz, Interaktion) zu bestimmen, welche am besten abschneidet.

* [Nutzen von Zielgruppenregeln](path-targeting.md) - Definieren Sie spezifische Regeln, die erfüllt sein müssen, damit eine Kundin oder ein Kunde auf der Grundlage von Zielgruppensegmenten, Profilattributen oder kontextuellen Daten für die Eingabe eines der Journey-Pfade berechtigt ist. Dadurch wird sichergestellt, dass die richtige Zielgruppe den angegebenen Pfad eingibt.

  >[!AVAILABILITY]
  >
  >Diese Funktion ist derzeit nur eingeschränkt verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern.

* [Bedingungen anwenden](conditions.md) - Erstellen Sie bedingte Pfade basierend auf bestimmten Kriterien wie Datenquellen, Zeit, Datum, Prozentaufspaltungen oder Profilobergrenzen. Dies entspricht der vorherigen Aktivität vom Typ Bedingung .

## Funktionsweise {#how-it-works}

Sobald die Journey live ist, werden die Profile anhand der definierten Kriterien bewertet und basierend auf den passenden Kriterien auf den entsprechenden Pfad der Journey weitergeleitet.

## Nächste Schritte {#next-steps}

Wählen Sie die Optimierungsmethode aus, die am besten zu Ihrem Anwendungsfall passt:

* Möchten Sie testen und erfahren, welcher Pfad am besten funktioniert? → Gehen Sie zu [Pfadexperiment](path-experimentation.md)
* Möchten Sie verschiedene Zielgruppen über bestimmte Pfade senden? → Gehe zu [Pfad-Targeting](path-targeting.md)
* Möchten Sie eine bedingte Logik erstellen (if/then-Szenarien)? → Gehen Sie zu [Bedingungen](conditions.md)
