---
title: Erste Schritte mit APIs für die Angebotsbereitstellung
description: Erfahren Sie mehr über die APIs, die zur Bereitstellung personalisierter Angebote verfügbar sind.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 76661d574ffabf32c4c1db8d88744604e50d7b40
workflow-type: tm+mt
source-wordcount: '430'
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

## Funktionen der Decisioning-API {#decisioning}

Die folgenden Funktionen sind nur mit der Decisioning-API verfügbar. Wenn Sie eine dieser Funktionen benötigen, verwenden Sie die Decisioning-API. Andernfalls empfehlen wir die Verwendung der Edge Decisioning-API.

* **Erlebnisereignisse**: Nutzen Sie Erlebnisereignisse, um Ihre Entscheidungsregeln zu erstellen.
* **Angebotsinhalt und -merkmale**: Sie können festlegen, dass Inhalt und Merkmale eines Angebots nicht über eine eigene Option zurückgegeben werden.
* **Angebotsmetadaten**: Aktivieren Sie eine Option, um die Metadaten eines Angebots zurückzugeben.
* **Zusammenführungsrichtlinie**: Verwenden Sie in Ihrer Anfrage eine andere Zusammenführungsrichtlinie als die Ihrer Sandbox zugeordnete.
* **Entscheidungsereignisse und Frequenzlimitierung**: Hiermit verhindern Sie, dass Entscheidungsereignisse durch eine Frequenzlimitierung gezählt werden.
* **Vorschläge duplizieren**: Aktivieren Sie diese Option, damit Vorschläge nicht dedupliziert werden.
