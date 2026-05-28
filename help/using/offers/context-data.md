---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erste Schritte mit Kontextdaten
description: Erfahren Sie, wie Sie Kontextdaten im Entscheidungs-Management nutzen.
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/aVm2FFqkJWN-k1qngYsp94FgKIZWaLCMUneFd0rVNpA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 100%

---

# Erste Schritte mit Kontextdaten {#context-data}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md)

Daten, die im Rahmen der Entscheidungsanfrage gesendet werden, werden als Kontextdaten betrachtet. Sie können Kontextdaten in der Entscheidungs-Engine nutzen, beispielsweise zum Entwerfen einer Entscheidungsregel, die verlangt, dass das aktuelle Wetter zum Zeitpunkt der Entscheidungsanfrage wärmer als 25 °C sein muss.

Kontextdaten werden in API-Anfragen zwischen **Decisioning** und **Edge Decisioning** unterschiedlich definiert. Für beide Anfragetypen können Kontextdaten in Eignungsregeln oder in Rangfolgeformeln verwendet werden, aber nur Edge Decisioning-API-Anfragen können Kontextdaten verwenden, um Inhalte zu personalisieren.

Bevor Sie beginnen, überprüfen Sie die folgenden Leitlinien und Einschränkungen:

* Aufgrund der unterschiedlichen Art der Kontextübergabe in Decisioning- und Edge Decisioning-Aufrufen sind kontextbasierte Eignungsregeln und Rangfolgeformeln nicht zwischen Decisioning- und Edge Decisioning-Aufrufen austauschbar.
* Tests mit dem Parameter `dryrun` sind nur mit der Decisioning-API möglich. Dies ist mit der Edge Decisioning-API nicht verfügbar. Beachten Sie, dass sich das Festlegen dieses Parameters mit der Decisioning-API auf `true` weder auf Begrenzungen noch auf die Anzahl der Vorschläge auswirkt.

Ausführliche Informationen zur Verwendung von Kontextdaten in den einzelnen APIs finden Sie in den folgenden Abschnitten:

* [Verwenden von Kontextdaten in Edge Decisioning-Anfragen](context-data-edge.md)
* [Verwenden von Kontextdaten in Decisioning-Anfragen](context-data-decisioning.md)
