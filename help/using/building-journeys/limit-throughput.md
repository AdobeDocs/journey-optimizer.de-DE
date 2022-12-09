---
solution: Journey Optimizer
title: Begrenzen des Durchsatzes mit externen Datenquellen und benutzerdefinierten Aktionen
description: Begrenzen des Durchsatzes mit externen Datenquellen und benutzerdefinierten Aktionen
exl-id: 45d6bb82-88ea-4510-a023-a75a82cc6f7b
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Anwendungsfall: den Durchsatz mit externen Datenquellen und benutzerdefinierten Aktionen begrenzen{#limit-throughput}

## Beschreibung des Anwendungsfalls

Mit Adobe Journey Optimizer können Anwender API-Aufrufe über benutzerdefinierte Aktionen und Data Sources an externe Systeme senden.

Dies kann mit folgender Funktion erfolgen:

* **Data Sources**: , um Informationen aus externen Systemen zu sammeln und im Journey-Kontext zu verwenden, z. B. um Wetterinformationen über die Profilstadt zu erhalten und einen dedizierten Journey-Fluss auf dieser Grundlage zu haben.

* **Benutzerdefinierte Aktionen**: , um Informationen an externe Systeme zu senden, z. B. zum Senden von E-Mails über eine externe Lösung mithilfe der Orchestrierungsfunktionen von Journey Optimizer sowie von Profilinformationen, Zielgruppendaten und Journey-Kontext.

Wenn Sie mit externen Datenquellen oder benutzerdefinierten Aktionen arbeiten, sollten Sie Ihre externen Systeme schützen, indem Sie den Journey-Durchsatz einschränken: bis zu 5000 Instanzen/Sekunde für EinzelJourneys und bis zu 20000 Instanzen/Sekunde für segmentgesteuerte. Sie können Begrenzungen auf Endpunktebene definieren, um zu verhindern, dass diese externen Systeme über die Capping-APIs von Journey Optimizer überfordert werden. Alle verbleibenden Anforderungen nach Erreichen des Grenzwerts werden jedoch entfernt.

In diesem Abschnitt finden Sie Problemumgehungen, mit denen Sie Ihren Durchsatz optimieren können. Weiterführende Informationen zur Integration in externe Systeme finden Sie in diesem Abschnitt [page](../configuration/external-systems.md).

## Implementierung

Für **segmentgesteuerte Journeys** können Sie die Drosselungsrate Ihrer Aktivität vom Typ Segment lesen definieren, die sich auf den Journey-Durchsatz auswirkt.  [Mehr dazu](../building-journeys/read-segment.md)

![](assets/limit-throughput-1.png)

Sie können diesen Wert von 500 auf 20 000 Instanzen pro Sekunde ändern. Wenn Sie weniger als 500/s benötigen, können Sie auch Bedingungen für die prozentuale Aufspaltung mit Warteaktivitäten hinzufügen, um Ihre Journey in mehrere Verzweigungen zu unterteilen und sie zu einem bestimmten Zeitpunkt auszuführen.

![](assets/limit-throughput-2.png)

Nehmen wir ein Beispiel für eine **segmentgesteuerte Journeys** mit einer Bevölkerung von **10.000 Profile** und senden Sie Daten an ein externes System, das **100 Anforderungen/Sekunde**.

1. Sie können Ihr Segment &quot;Segment lesen&quot;definieren, um Profile mit einem Durchsatz von 500 Profilen/Sekunde zu lesen. Das bedeutet, dass es 20 Sekunden dauern wird, alle Ihre Profile zu lesen. Am zweiten 1 werden Sie 500 davon lesen, am zweiten 2 500 mehr, usw.

1. Anschließend können Sie eine Bedingungsaktivität mit einer Aufspaltung von 20 % hinzufügen, die bei jeder zweiten Aufspaltung 100 Profile in jedem Zweig enthält.

1. Fügen Sie anschließend in jedem Zweig Warteaktivitäten mit einem bestimmten Timer hinzu. Hier haben wir eine Wartezeit von 30 Sekunden für jeden eingerichtet. Jede Sekunde fließen 100 Profile in jeden Zweig.

   * In Zweig 1 warten sie 30 Sekunden, d. h.:
      * Beim zweiten 1 warten 100 Profile auf den zweiten 31.
      * In der zweiten 2 warten 100 Profile auf die zweite 32 usw.
   * In Zweig 2 warten sie 60 Sekunden, d. h.:
      * Beim zweiten 1 warten 100 Profile auf den zweiten 61 (1&#39;01&#39;&#39;)
      * In der zweiten 2 warten 100 Profile auf die zweite 62 (1&#39;02&#39;&#39;) usw.
   * Da wir erwarten, dass alle Profile maximal 20 Sekunden gelesen werden, gibt es keine Überschneidungen zwischen den einzelnen Zweigen, wobei der zweite Zweig der letzte ist, bei dem Profile in die Bedingung fließen. Zwischen dem zweiten 31. und dem zweiten 51. werden alle Profile in Zweig 1 verarbeitet. Zwischen dem zweiten 61 (1&#39;01&#39;&#39;) und dem zweiten 81 (1&#39;21&#39;&#39;) werden alle Profile in Zweig 2 verarbeitet usw.

   * Als Schutzmaßnahme können Sie auch einen sechsten Zweig hinzufügen, der weniger als 100 Profile pro Zweig enthält, insbesondere wenn Ihr externes System nur 100 Anfragen/Sekunde unterstützt.



>[!IMPORTANT]
>
>Wie bei jeder Problemumgehung sollten Sie diese Lösung gründlich testen, bevor Sie in die Produktion gehen, um sicherzustellen, dass sie das tut, was Sie möchten.

Als zusätzliche Limits können Sie auch Begrenzungsfunktionen verwenden.

>[!NOTE]
>
>Im Gegensatz zu Begrenzungsfunktionen, die einen Endpunkt schützen, indem sie für alle Journeys einer Sandbox global sind, funktioniert diese Problemumgehung nur auf Journey-Ebene. Wenn also mehrere Journeys parallel ausgeführt werden und auf denselben Endpunkt abzielen, müssen Sie dies beim Entwerfen Ihrer Journey berücksichtigen. Diese Problemumgehung ist daher nicht für jeden Anwendungsfall geeignet.
