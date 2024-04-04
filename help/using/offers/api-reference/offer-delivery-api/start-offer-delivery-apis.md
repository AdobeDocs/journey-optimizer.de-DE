---
title: Erste Schritte mit APIs für die Angebotsbereitstellung
description: Erfahren Sie mehr über die APIs, die zur Bereitstellung personalisierter Angebote verfügbar sind.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 2ef555bd10d7b8fa32c1324b201d55d2a4b1aec7
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 100%

---

# Erste Schritte mit APIs für die Angebotsbereitstellung {#about-decisioning-apis}

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
