---
solution: Journey Optimizer
product: journey optimizer
title: Integrieren von Journey Optimizer mit externen Systemen
description: Best Practices bei der Integration von Journey Optimizer mit externen Systemen
role: User
level: Beginner
keywords: extern, API, Optimizer, Begrenzung
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 40afc1c0e0ae55dfbec45ff0b22170d6345a8e46
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 61%

---

# Integration mit externen Systemen {#external-systems}

Auf dieser Seite werden die verschiedenen Leitplanken vorgestellt, die Journey Optimizer für die Integration eines externen Systems bietet. Zusätzlich erhalten Sie Best Practices dazu, wie Sie den Schutz Ihres externen Systems mithilfe der Begrenzungs-API optimieren können, wie Journey-Zeitüberschreitungen konfiguriert werden und wie erneute Versuche funktionieren.

Mit Journey Optimizer können Sie Verbindungen zu externen Systemen über benutzerdefinierte Datenquellen und Aktionen konfigurieren. Auf diese Weise können Sie beispielsweise Ihre Journeys mit Daten aus einem externen Reservierungssystem anreichern oder Nachrichten mithilfe eines Drittanbietersystems wie Epsilon oder Facebook versenden.

Bei der Integration eines externen Systems können mehrere Probleme auftreten: Das System kann langsam sein, nicht mehr reagieren oder es kann möglicherweise nicht in der Lage sein, große Datenmengen zu verarbeiten. Journey Optimizer bietet verschiedene Schutzmechanismen, um Ihr System vor Überlastung zu schützen.

Alle externen Systeme unterscheiden sich hinsichtlich ihrer Leistung. Sie müssen die Konfiguration deshalb an Ihre Anwendungsfälle anpassen.

Wenn Journey Optimizer einen Aufruf an eine externe API ausführt, werden die technischen Schutzmechanismen wie folgt eingesetzt:

1. Begrenzungs- oder Einschränkungsregeln werden angewendet: Wenn die maximale Rate erreicht wird, werden die verbleibenden Aufrufe verworfen oder in die Warteschlange gestellt.

2. Zeitüberschreitung und erneuter Versuch: Wenn die Begrenzungsregel erfüllt wird, versucht Journey Optimizer, den Aufruf auszuführen, bis das Ende der Zeitüberschreitungsdauer erreicht ist.

## Begrenzung und Drosselungs-APIs {#capping}

### Über Begrenzungs- und Einschränkungs-APIs

Beim Konfigurieren einer Datenquelle oder einer Aktion stellen Sie eine Verbindung zu einem System her, um entweder zusätzliche Informationen abzurufen, die in Ihren Journey verwendet werden, oder Nachrichten oder API-Aufrufe zu senden.

Journey-APIs unterstützen bis zu 5.000 Ereignisse pro Sekunde, einige externe Systeme oder APIs weisen jedoch möglicherweise keinen gleichwertigen Durchsatz auf. Um eine Überlastung dieser Systeme zu vermeiden, können Sie die **Begrenzung** und **Einschränken** APIs zur Begrenzung der Anzahl der pro Sekunde gesendeten Ereignisse.

Jedes Mal, wenn Journey einen API-Aufruf ausführen, wird er über die API-Engine weitergeleitet. Wenn das in der API festgelegte Limit erreicht wird, wird der Aufruf entweder abgelehnt, wenn Sie die Capping-API verwenden, oder bis zu sechs Stunden lang in die Warteschlange gestellt und so bald wie möglich in der Reihenfolge verarbeitet, in der sie empfangen wurden, wenn Sie die Throttling-API verwenden.

Nehmen wir beispielsweise an, Sie haben eine Begrenzungs- oder Einschränkungsregel von 100 Aufrufen pro Sekunde für Ihr externes System definiert. Eine benutzerdefinierte Aktion führt in 10 verschiedenen Journeys Aufrufe an Ihr System aus. Wenn eine Journey 200 Aufrufe pro Sekunde erhält, werden die 100 verfügbaren Slots verwendet und die 100 verbleibenden Slots verworfen oder in die Warteschlange gestellt. Da die Höchstrate überschritten wurde, sind für die anderen 9 Journeys keine Slots mehr übrig. Durch diese Granularität ist das externe System vor Überlastung und Abstürzen geschützt.

>[!IMPORTANT]
>
>**Begrenzungsregeln** werden auf Sandbox-Ebene für einen bestimmten Endpunkt (die URL genannt) konfiguriert, aber global für alle Journey dieser Sandbox.
>
>**Einschränkungsregeln** werden nur für Produktions-Sandboxes konfiguriert, für einen bestimmten Endpunkt, aber global für alle Journey über alle Sandboxes hinweg. Pro Organisation kann nur eine Einschränkungskonfiguration verwendet werden.

Weiterführende Informationen zur Verwendung der APIs finden Sie in diesen Abschnitten:

* [Capping-API](capping.md)
* [Einschränkungs-API](throttling.md)

Eine ausführliche Beschreibung der APIs finden Sie unter [Dokumentation zu Adobe Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Kapazität von Datenquellen und benutzerdefinierten Aktionen {#capacity}

Für **externe Datenquellen** festgelegt ist, ist die maximale Anzahl von Anrufen pro Sekunde auf 15 beschränkt. Wenn diese Grenze überschritten wird, werden alle zusätzlichen Aufrufe je nach verwendeter API entweder verworfen oder in die Warteschlange gestellt. Es ist möglich, diesen Grenzwert für private externe Datenquellen zu erhöhen, indem Sie sich an die Adobe wenden, um den Endpunkt in die Zulassungsliste aufzunehmen. Dies ist jedoch keine Option für öffentliche externe Datenquellen. * [Erfahren Sie, wie Sie Datenquellen konfigurieren](../datasource/about-data-sources.md).

>[!NOTE]
>
>Wenn eine Datenquelle eine benutzerdefinierte Authentifizierung mit einem anderen Endpunkt als dem verwendet, der für die Datenquelle verwendet wird, müssen Sie sich an Adobe wenden, um diesen Endpunkt ebenfalls in die Zulassungsliste aufzunehmen.

Für **benutzerdefinierte Aktionen** müssen Sie die Kapazität Ihrer externen API bewerten. Wenn Journey Optimizer beispielsweise 1000 Aufrufe pro Sekunde sendet und Ihr System nur 100 Aufrufe pro Sekunde unterstützen kann, müssen Sie eine Begrenzungs- oder Drosselkonfiguration definieren, damit Ihr System nicht überfordert wird. [Erfahren Sie, wie Sie Aktionen konfigurieren](../action/action.md)

## Zeitüberschreitung und erneute Versuche{#timeout}

Wenn die Begrenzungs- oder Einschränkungsregel erfüllt ist, wird die Timeout-Regel angewendet.

Sie können in jeder Journey eine Zeitüberschreitungsdauer festlegen. Auf diese Weise können Sie für den Aufruf eines externen Systems eine maximale Dauer festlegen. Die Zeitüberschreitungsdauer wird in den Eigenschaften einer Journey konfiguriert. Mehr dazu erfahren Sie auf [dieser Seite](../building-journeys/journey-gs.md#timeout_and_error).

Diese Zeitüberschreitung gilt für alle externen Aufrufe (externe API-Aufrufe in benutzerdefinierten Aktionen und Datenquellen). Standardmäßig ist dieser Zeitraum mit 30 Sekunden festgelegt.

Während der definierten Zeitüberschreitungsdauer versucht Journey Optimizer, das externe System aufzurufen. Nach dem ersten Aufruf können bis zum Ende der Zeitüberschreitungsdauer maximal drei weitere Versuche unternommen werden. Die Anzahl weiterer Versuche kann nicht geändert werden.

Bei jedem erneuten Versuch wird ein Slot verwendet. Wenn Sie eine Begrenzung von 100 Aufrufen pro Sekunde haben und jeder Ihrer Aufrufe zwei weitere Versuche erfordert, sinkt die Rate auf 30 Aufrufe pro Sekunde (jeder Aufruf verwendet drei Slots: den ersten Aufruf und zwei weitere Versuche).

Der Wert für die Zeitüberschreitungsdauer hängt vom Anwendungsfall ab. Wenn Sie Ihre Nachricht schnell senden möchten, z. B. wenn ein Kunde das Geschäft betritt, ist es nicht sinnvoll, eine lange Zeitüberschreitung einzurichten. Je länger die Zeitüberschreitung ist, desto mehr Elemente werden in die Warteschlange gestellt. Dies kann die Leistung erheblich beeinträchtigen. Wenn Journey Optimizer 1.000 Aufrufe pro Sekunde ausführt, kann das System durch fünf oder 15 Sekunden lange Datenflüsse schnell überlastet werden.

Sehen wir uns ein Beispiel einer Zeitüberschreitung von fünf Sekunden an.

* Der erste Aufruf dauert weniger als fünf Sekunden: Der Aufruf ist erfolgreich und es wird kein erneuter Versuch unternommen.
* Der erste Aufruf dauert länger als fünf Sekunden: Der Aufruf wird abgebrochen und es wird kein erneuter Versuch unternommen. In Berichten wird dies als Zeitüberschreitungsfehler gezählt.
* Der erste Aufruf schlägt nach zwei Sekunden fehl (das externe System gibt einen Fehler zurück): drei Sekunden bleiben für weitere Versuche, wenn Begrenzungs-Slots verfügbar sind.
   * Wenn einer der drei weiteren Versuche vor Ablauf der fünf Sekunden erfolgreich ist, wird der Aufruf durchgeführt und es wird kein Fehler ausgegeben.
   * Wenn während der erneuten Versuche das Ende der maximalen Wartezeit erreicht wird, wird der Aufruf abgebrochen und in Berichten als Zeitüberschreitungsfehler gezählt.

## Häufig gestellte Fragen{#faq}

**Wie kann ich eine Begrenzungs- oder Einschränkungsregel konfigurieren? Gibt es eine Standardregel?**

Standardmäßig gibt es keine Begrenzungs- oder Einschränkungsregel. Regeln werden auf Sandbox-Ebene für einen bestimmten Endpunkt (die URL genannt) mithilfe der Capping- oder Throttling-API definiert. Weitere Informationen finden Sie in [diesem Abschnitt](../configuration/external-systems.md#capping).

**Wie viele weitere Versuche werden unternommen? Kann ich die Anzahl der weiteren Versuche ändern oder eine Mindestwartezeit zwischen den Versuchen definieren?**

Pro Aufruf können nach dem ersten Aufruf maximal drei weitere Versuche durchgeführt werden, bis das Ende der Zeitüberschreitungsdauer erreicht ist. Die Anzahl weiterer Versuche und die Zeit zwischen den einzelnen Versuchen können nicht geändert werden. Weitere Informationen finden Sie in [diesem Abschnitt](../configuration/external-systems.md#timeout).

**Wo kann ich die Zeitüberschreitung konfigurieren? Gibt es einen Maximalwert?**

Sie können in jeder Journey eine Zeitüberschreitungsdauer festlegen. Die Zeitüberschreitungsdauer wird in den Eigenschaften einer Journey konfiguriert. Die Zeitüberschreitungsdauer muss zwischen 1 Sekunde und 30 Sekunden liegen. Weitere Informationen finden Sie in [diesem Abschnitt](../configuration/external-systems.md#timeout) und auf [dieser Seite](../building-journeys/journey-gs.md#timeout_and_error).