---
product: experience platform
solution: Experience Platform
title: Erste Schritte mit Kontextdaten
description: Erfahren Sie, wie Sie Kontextdaten im Entscheidungs-Management nutzen.
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Erste Schritte mit Kontextdaten {#context-data}

Daten, die im Rahmen der Entscheidungsanfrage gesendet werden, werden als Kontextdaten betrachtet. Sie können Kontextdaten in der Entscheidungs-Engine nutzen, um z. B. eine Entscheidungsregel zu entwerfen, für die das aktuelle Wetter zum Zeitpunkt der Entscheidungsanfrage ≥80 Grad betragen muss.

Kontextdaten werden zwischen {**}- und {**}Edge Decisioning **-API-Anfragen unterschiedlich definiert.** Für beide Anfragetypen können Kontextdaten in Eignungsregeln oder in Rangfolgeformeln verwendet werden, aber nur Edge Decisioning-API-Anfragen können Kontextdaten verwenden, um Inhalte zu personalisieren.

Bevor Sie beginnen, überprüfen Sie die folgenden Leitplanken und Einschränkungen:

* Aufgrund der unterschiedlichen Art der Kontextübergabe zwischen Decisioning- und Edge Decisioning-Aufrufen sind kontextbasierte Eignungsregeln und Rangfolgeformeln zwischen Decisioning- und Edge Decisioning-Aufrufen nicht austauschbar.
* Tests mit dem `dryrun` Parameter sind nur mit der Decisioning-API möglich. Sie ist nicht mit der Edge Decisioning-API verfügbar. Beachten Sie, dass sich die Festlegung dieses Parameters auf `true` mit der Decisioning-API nicht auf Obergrenzen und die Anzahl der Vorschläge auswirkt.

Ausführliche Informationen zur Verwendung von Kontextdaten in den einzelnen APIs finden Sie in den folgenden Abschnitten:

* [Verwenden von Kontextdaten in Edge Decisioning-Anfragen](context-data-edge.md)
* [Verwenden von Kontextdaten in Entscheidungsanfragen](context-data-decisioning.md)

