---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erste Schritte mit APIs für den Angebotsversand
description: Erfahren Sie mehr über die APIs, die für den Versand personalisierter Angebote verfügbar sind.
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qo18m5-seH1yCaxQPJ7hmXDSkBPex-PgYKMQRsOBhBw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: c132d929-fa62-4271-803e-b823be07b914id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: ed0d8d0e-04b9-4326-be72-a0fbca265377id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 488
ht-degree: 100%

---

# Erste Schritte mit APIs für den Angebotsversand {#about-decisioning-apis}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../experience-decisioning/gs-experience-decisioning.md)

Sie können Angebote entweder mithilfe der **Decisioning**- oder **Edge Decisioning**-API bereitstellen. Darüber hinaus ermöglicht Ihnen die API zur **Batch-Entscheidungsfindung**, Angebote an alle Profile in einer bestimmten Zielgruppe durch einen einzigen Aufruf zu senden. Der Angebotsinhalt für jedes Profil in der Zielgruppe wird in einen Adobe Experience Platform-Datensatz platziert, über den er für benutzerdefinierte Batch-Workflows zur Verfügung steht.

Auf dieser Seite finden Sie Informationen zu spezifischen Funktionen, die mit den **Decisioning**- und **Edge Decisioning**-APIs verfügbar sind. Zwar ermöglichen es Ihnen beide, Ihren Kunden Angebote zu unterbreiten, wir empfehlen jedoch, für eingehende Anwendungsfälle möglichst die **Edge Decisioning**-API zu verwenden, um auf Ihrer Plattform eine bessere Latenz und besseren Durchsatz sicherzustellen.

Weiterführende Informationen zur Verwendung der APIs finden Sie in diesen Abschnitten:

* [Decisioning-API](decisioning-api.md)
* [Edge Decisioning-API](edge-decisioning-api.md)
* [Batch Decisioning-API](batch-decisioning-api.md)

## Funktionen der Edge Decisioning-API {#edge}

**Eindeutige Anfrage für Erlebnisereignisse und Entscheidungsanfragen**

Mit der Edge Decisioning-API können Sie das Erlebnisereignis zusammen mit der Entscheidungsanfrage in einer einzigen Anfrage anstatt zwei verschiedenen Anfragen senden.

Wenn beispielsweise ein Kunde Ihre Website besucht, enthält die Anfrage das Erlebnisereignis (den Besuch des Kunden auf der Website) und gibt ein Angebot zurück, das auf der besuchten Seite erscheint.

**Kontextdatenspeicherung in Adobe Experience Platform**

Kontextdaten sind Daten, die Sie nur zum Zeitpunkt kennen, zu dem Sie ein Angebot anfordern. Beispielsweise die Farbe des gekauften Artikels, das Wetter zum Zeitpunkt des Kaufs usw.

Beim Übermitteln von Kontextdaten mit einer Edge Decisioning-API-Anfrage werden Daten im Adobe Experience Platform-Profil gespeichert, sodass sie später wiederverwendet werden können.

>[!NOTE]
>
>Damit Kontextdaten gespeichert werden können, muss ein dediziertes XDM-Schema konfiguriert sein.

**Aktualisierung des Frequenzbegrenzungszählers**

Wenn für einige Ihrer Angebote die Frequenzbegrenzung aktiviert wurde, um zu definieren, wie oft ihre Begrenzungsanzahl zurückgesetzt wird, wird der Zähler aktualisiert und steht in weniger als 3 Sekunden in einer Entscheidung der Edge Decisioning-API zur Verfügung. [Hinzufügen von Begrenzungen zu einem Angebot](../../offer-library/add-constraints.md)

## Funktionen der Decisioning-API {#decisioning}

Die folgenden Funktionen sind nur mit der Decisioning-API verfügbar. Wenn Sie eine dieser Funktionen benötigen, verwenden Sie die Decisioning-API. Andernfalls empfehlen wir die Verwendung der Edge Decisioning-API.

* **Angebotsinhalt und -merkmale**: Sie können festlegen, dass Inhalt und Merkmale eines Angebots nicht über eine eigene Option zurückgegeben werden.
* **Angebotsmetadaten**: Aktivieren Sie eine Option, um die Metadaten eines Angebots zurückzugeben.
* **Zusammenführungsrichtlinie**: Verwenden Sie in Ihrer Anfrage eine andere Zusammenführungsrichtlinie als die Ihrer Sandbox zugeordnete.
* **Entscheidungsereignisse und Frequenzbegrenzung**: Hiermit verhindern Sie, dass Entscheidungsereignisse durch eine Frequenzbegrenzung gezählt werden.
* **Vorschläge duplizieren**: Aktivieren Sie diese Option, damit Vorschläge nicht dedupliziert werden.
