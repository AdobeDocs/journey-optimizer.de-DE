---
title: Decisioning- und Edge Decisioning-APIs
description: Entscheidungs-Management ist eine Sammlung von Services und Benutzeroberflächenprogrammen, mit denen Marketing-Experten personalisierte Angebotserlebnisse für Endbenutzer erstellen und bereitstellen können – über verschiedene Kanäle und Anwendungen hinweg und unter Verwendung von Business-Logik und Entscheidungsregeln.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: dc56f2dc461a11c9706b3572ccd4b9e0feb6f055
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 8%

---

# Decisioning- und Edge Decisioning-APIs {#about-decisioning-apis}

Sie können Angebote entweder mithilfe der **Entscheidungsfindung** oder **Edge Decisioning** API.

Auf dieser Seite finden Sie Informationen zu spezifischen Funktionen, die in den einzelnen APIs verfügbar sind. Beide ermöglichen es Ihnen, Ihren Kunden Angebote zu unterbreiten. Wir empfehlen jedoch, die Variable **Edge Decisioning** wann immer möglich, für eingehende Anwendungsfälle und um eine bessere Latenz und Durchsatz auf Ihrer Plattform sicherzustellen.

|  | Anforderungen/Sek. | Latenz |
|---|---|---|
| Decisioning API | 2.000 | &lt;500ms |
| Edge Decisioning-API | 5.000 | &lt;250ms |

Weiterführende Informationen zur Verwendung der APIs finden Sie in diesen Abschnitten:
* [Decisioning API](decisioning-api.md)
* [Edge Decisioning-API](edge-decisioning-api.md)

## Funktionen der Edge Decisioning API {#edge}

**Eindeutige Anforderung für Erlebnisereignisse und Entscheidungsanforderungen**

Mit der Edge Decisioning-API können Sie das Erlebnisereignis zusammen mit der Entscheidungsanfrage in einer einzigen Anfrage senden, anstatt zwei verschiedene Anfragen zu haben.

Wenn beispielsweise ein Kunde Ihre Website besucht, enthält die Anfrage das Erlebnisereignis (den Besuch des Kunden auf der Seite) und ein Angebot, das zum Ausfüllen der besuchten Seite zurückgegeben wird.

**Kontextdatenspeicherung in Adobe Experience Platform**

Kontextdaten beziehen sich auf Daten, die Sie nur zum Zeitpunkt der Angebotsrückgabe kennen. Beispielsweise die Farbe des gekauften Artikels, das Wetter zum Zeitpunkt des Kaufs usw.

Beim Übergeben von Kontextdaten mit einer Edge Decisioning API-Anfrage werden Daten im Adobe Experience Platform-Profil gespeichert, sodass sie später wiederverwendet werden können.

>[!NOTE]
>
>Damit die Kontextdaten gespeichert werden können, muss ein dediziertes XDM-Schema konfiguriert sein.

## Decisioning API-Funktionen {#decisioning}

Die folgenden Funktionen sind nur mit der Decisioning API verfügbar. Verwenden Sie die Decisioning-API, wenn Sie eine davon nutzen müssen, um Ihre Anforderungen zu erfüllen. Andernfalls empfehlen wir die Verwendung der Edge Decisioning-APIs.

* **Erlebnisereignisse**: Nutzen Sie Erlebnisereignisse, um Ihre Entscheidungsregeln zu erstellen.
* **Angebotsinhalt und -merkmale**: Sie können festlegen, dass Inhalt und Merkmale eines Angebots nicht über eine dedizierte Option zurückgegeben werden.
* **Angebotsmetadaten**: Aktivieren Sie eine Option, um die Metadaten eines Angebots zurückzugeben.
* **Zusammenführungsrichtlinie**: verwenden in Ihrer Anfrage eine andere Zusammenführungsrichtlinie als die Ihrer Sandbox zugeordnete.
* **Entscheidungsereignisse und Frequenzlimitierung**: blockieren, dass Entscheidungsereignisse durch eine beliebige Frequenzbegrenzung gezählt werden.
* **Vorschläge duplizieren**: Aktivieren Sie die Option, die Vorschläge nicht zu deduplizieren.
