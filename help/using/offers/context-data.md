---
product: experience platform
solution: Experience Platform
title: Erste Schritte mit Kontextdaten
description: Erfahren Sie, wie Sie Kontextdaten im Entscheidungs-Management nutzen.
badge: label="Legacy" type="Informative"
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: ht
source-wordcount: '210'
ht-degree: 100%

---

# Erste Schritte mit Kontextdaten {#context-data}

Daten, die im Rahmen der Entscheidungsanfrage gesendet werden, werden als Kontextdaten betrachtet. Sie können Kontextdaten in der Entscheidungs-Engine nutzen, beispielsweise zum Entwerfen einer Entscheidungsregel, die verlangt, dass das aktuelle Wetter zum Zeitpunkt der Entscheidungsanfrage wärmer als 25 °C sein muss.

Kontextdaten werden in API-Anfragen zwischen **Decisioning** und **Edge Decisioning** unterschiedlich definiert. Für beide Anfragetypen können Kontextdaten in Eignungsregeln oder in Rangfolgeformeln verwendet werden, aber nur Edge Decisioning-API-Anfragen können Kontextdaten verwenden, um Inhalte zu personalisieren.

Bevor Sie beginnen, überprüfen Sie die folgenden Leitlinien und Einschränkungen:

* Aufgrund der unterschiedlichen Art der Kontextübergabe in Decisioning- und Edge Decisioning-Aufrufen sind kontextbasierte Eignungsregeln und Rangfolgeformeln nicht zwischen Decisioning- und Edge Decisioning-Aufrufen austauschbar.
* Tests mit dem Parameter `dryrun` sind nur mit der Decisioning-API möglich. Dies ist mit der Edge Decisioning-API nicht verfügbar. Beachten Sie, dass sich das Festlegen dieses Parameters mit der Decisioning-API auf `true` weder auf Begrenzungen noch auf die Anzahl der Vorschläge auswirkt.

Ausführliche Informationen zur Verwendung von Kontextdaten in den einzelnen APIs finden Sie in den folgenden Abschnitten:

* [Verwenden von Kontextdaten in Edge Decisioning-Anfragen](context-data-edge.md)
* [Verwenden von Kontextdaten in Decisioning-Anfragen](context-data-decisioning.md)
