---
solution: Journey Optimizer
product: journey optimizer
title: Leitplanken und Einschränkungen von Journey Optimizer
description: Weitere Informationen zu Leitplanken bei Journey Optimizer
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 2
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2: id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 493d9822091427d03c012f7f9c72d0650ce625ee
workflow-type: tm+mt
source-wordcount: 4463
ht-degree: 71%

---


# Leitlinien und Einschränkungen {#limitations}

Unten finden Sie Leitlinien und Einschränkungen bei der Verwendung von [!DNL Adobe Journey Optimizer].

Berechtigungen, Produkteinschränkungen und Performance-Leitlinien sind auf der Seite [Adobe Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} aufgeführt.

>[!CAUTION]
>
>* [Leitlinien für Echtzeit-Kundenprofildaten und Segmentierung](https://experienceleague.adobe.com/de/docs/experience-platform/profile/guardrails){target="_blank"} gelten auch für Adobe Journey Optimizer.
>
>* Siehe auch [Leitlinien für die Datenaufnahme im Echtzeit-Kundenprofil](https://experienceleague.adobe.com/de/docs/experience-platform/ingestion/guardrails){target="_blank"}


## System und Plattform {#system-platform}

### Unterstützte Browser {#browsers}

Die Benutzeroberfläche von Adobe [!DNL Journey Optimizer] wurde für eine optimale Funktionsweise in der neuesten Version von Google Chrome entwickelt. Bei der Verwendung bestimmter Funktionen in älteren Versionen oder anderen Browsern können Probleme auftreten.

### Leitlinien für Datensätze {#datasets-guardrails}

Ab Februar 2025 werden in **neuen Sandboxes und neuen Organisationen** für systemgenerierte Journey Optimizer-Datensätze als Schutzmechanismen die folgenden Limits für die Time-to-Live (TTL) eingeführt:

* **90 Tage** für Daten im Profilspeicher
* **13 Monate** für Daten im Data Lake

Diese Änderung wird in einer nachfolgenden Phase in **bestehende Kunden-Sandboxes** integriert. [Weitere Informationen zu Limits für die Time-to-Live (TTL) als Schutzmechanismen für Datensätze](../data/datasets-ttl.md)

## Journeys {#journeys-guardrails}

In diesem Abschnitt werden Leitlinien und Einschränkungen für Journeys beschrieben, einschließlich allgemeiner Journey-Einschränkungen, Journey-Komponenten (Aktionen, Ereignisse, Datenquellen), Journey-Aktivitäten und spezifischer Funktionen wie benutzerdefinierten Aktionen und Ausdruckseditor.

### Allgemeine Limits für Journey {#journeys-guardrails-journeys}

* Die Anzahl der Aktivitäten in einer Journey ist auf **50%**. Die Anzahl der Aktivitäten wird im oberen linken Bereich der Journey-Arbeitsfläche angezeigt.

  Da die Journey sich diesem Grenzwert nähern, kann die Bearbeitungs- und Veröffentlichungsleistung beeinträchtigt sein und es können Speicher- oder Validierungsfehler auftreten. Wenn dies eintritt, teilen Sie Ihren Journey mithilfe von „Sprungaktivitäten[ in kleinere Unterversionen auf ](../building-journeys/jump.md) erstellen Sie ihn in einer neuen Journey. Das Aktivitätslimit kann nicht erhöht werden.

* Standardmäßig ist die Anzahl der Live-/Pausen-/Probelauf-Journey auf einmal auf **100** begrenzt. Die aktuelle Anzahl der Journeys wird über der Journey-Arbeitsfläche angezeigt.

  Während Sie Journeys veröffentlichen, skalieren und passen wir sie automatisch an, um maximalen Durchsatz und maximale Stabilität zu gewährleisten. Wenn Sie den Meilenstein von 100 Live-Journeys gleichzeitig erreichen, wird in der UI eine Benachrichtigung zu dieser Leistung angezeigt. Wenn Sie diese Benachrichtigung sehen, aber die Notwendigkeit besteht, Ihre Journey über 100 Live-Journeys hinaus zu erweitern, erstellen Sie bitte ein Ticket für die Kundenunterstützung, und wir helfen Ihnen bei der Erreichung Ihrer Ziele.

* Bei Verwendung einer Zielgruppen-Qualifizierungsaktivität auf einer Journey kann es bis zu **10 Minuten dauern, bis diese Zielgruppen-Qualifizierungsaktivität** ist und Profile überwacht werden, die in die Zielgruppe eintreten oder diese verlassen.

* Eine Journey-Instanz für ein Profil hat eine Maximalgröße von **1 MB**. Alle Daten, die im Rahmen der Journey-Ausführung gesammelt wurden, werden in dieser Journey-Instanz gespeichert. Daher werden Daten aus einem eingehenden Ereignis, aus Adobe Experience Platform abgerufene Profilinformationen, Antworten auf benutzerdefinierte Aktionen usw. in dieser Journey-Instanz gespeichert und wirken sich auf die Journey-Größe aus. Es wird empfohlen, beim Start eines Journey mit einem Ereignis die maximale Größe dieser Ereignis-Payload (z. B. unter **800 KB**) zu begrenzen, um zu vermeiden, dass dieser Grenzwert nach einigen Aktivitäten bei der Journey-Ausführung erreicht wird. Wenn dieses Limit erreicht ist, befindet sich das Profil im Fehlerstatus und wird von der Journey ausgeschlossen.

* Für jede Profil- und Journey-Version speichert die Journey-Laufzeitumgebung eine interne Warteschlange von bis zu **10 ausstehenden**, während ein Ereignis verarbeitet wird. Wenn dieses Limit erreicht ist, werden zusätzliche Ereignisse mit dem Grund `maxInstanceStackEventsReached` verworfen, bis wieder Plätze im Stapel frei sind. Weitere Informationen finden Sie unter [Aufgrund von blockierter Journey-Instanz verworfene Ereignisse](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached).

* Zusätzlich zum in den Journey-Aktivitäten verwendeten Timeout gibt es auch einen globalen Journey-Timeout, der nicht auf der Benutzeroberfläche angezeigt wird und nicht geändert werden kann. Dieser globale Timeout stoppt den Fortschritt von Kontakten in der Journey **91 Tage** nach ihrem Eintritt. [Weitere Informationen](../building-journeys/journey-properties.md#global_timeout)

>[!TIP]
>
>**Was dies für Sie bedeutet:** Das **50-Aktivitätslimit** und **100-live-Journey-Limit** sind die beiden Leitplanken, auf die die meisten Teams als erste beim Skalieren stoßen. Planen Sie die Journey-Aufteilung frühzeitig und verteilen Sie die Startzeiten für „Zielgruppe lesen“ im Abstand von mindestens 5-10 Minuten, um Sandbox-Durchsatzkonflikte zu vermeiden.

#### Validieren der Journey-Payload-Größe {#journey-payload-size}

Beim Speichern oder Veröffentlichen einer Journey validiert Journey Optimizer die gesamte Journey-Payload-Größe, um Stabilität und Leistung zu erhalten.

| Szenario | Schwellenwert | Verhalten |
|---|---|---|
| Payload &lt; 90 % des Limits | Warnhinweis unten | Journey speichert und veröffentlicht erfolgreich. Keine Warnungen oder Fehler angezeigt. |
| Payload 90-99 % des Limits | Warnung (weich) | Journey speichert und veröffentlicht mit einem Warnhinweis: **Warnung** Die Größe der Journey-Payload liegt nahe am Grenzwert. Größter Knoten: „[Name des Knotens]“ (Typ: „[Typ des Knotens]“, Größe: [N] Byte). |
| Payload ≥ 100 % des Limits | **Fehler (hart)** | Speichern oder Veröffentlichen ist blockiert. Gibt **HTTP 413-Anfrageentität zu groß** zurück. Fehler: Journey-Payload überschreitet das Limit. Größter Knoten: „[Name des Knotens]“ (Typ: „[Typ des Knotens]“, Größe: [N] Byte). |

**Standardkonfiguration**

* **Standardmäßige maximale Anfragengröße**: **2 MB** (2.000.000 Byte). Einige Organisationen verfügen möglicherweise über benutzerdefinierte Limits, die von Adobe konfiguriert werden.
* **Warnhinweisschwelle:** 90 % des Limits.
* **Fehlerschwelle:** 100 % des Limits.

**Fehlerbehebung und Empfehlungen**

* Überprüfen Sie den größten Knoten, der im Warnhinweis oder in der Fehlermeldung angegeben ist.
* Vereinfachen Sie Bedingungen, reduzieren Sie Datenzuordnungen und entfernen Sie unnötige Schritte oder Parameter.
* Erwägen Sie bei Bedarf, die Journey in kleinere Journeys aufzuteilen.
* Wenn Sie der Meinung sind, dass Ihr Unternehmen ein höheres Limit benötigt, wenden Sie sich an den Adobe-Support.

Um die aktuelle Payload-Größe des Journey vor der Veröffentlichung zu überwachen, verwenden Sie die Anzeige **[!UICONTROL Aktuelle Journey-Payload-]**&quot; im Bedienfeld &quot;Journey-Eigenschaften“. [Erfahren Sie, wie Sie die Größe Ihrer Journey-Payload überprüfen](../building-journeys/journey-properties.md#journey-payload-size)

### Vergleich von Lizenzpaketen {#select-package-limitations}

>[!NOTE]
>
>Die folgenden Paketeinschränkungen auswählen gelten nicht für Journey vom Typ „Zielgruppe lesen“ oder „Geschäftsereignis“. Wenn Sie eine komplexere Journey-Logik mit mehreren Aktionen, Bedingungen oder Warteaktivitäten benötigen, sollten Sie ein Upgrade Ihres Lizenzpakets in Erwägung ziehen oder gegebenenfalls Journeys vom Typ „Zielgruppe lesen“ verwenden.

Für Kunden, die das **Select**-Lizenzpaket verwenden, gelten die folgenden zusätzlichen Einschränkungen speziell für unitäre Journey (Journey, die mit einer Veranstaltung oder einer Zielgruppen-Qualifizierung beginnen):

| Einschränkung | Fehler-Code | Beschreibung |
|---|---|---|
| Nur eine Aktion zulässig | `ERR_PKG_SELECT_8` | Einzelne Journey können nur **eine** Aktionsaktivität enthalten. Mehrere E-Mail-, Push-, SMS- oder andere Aktionsaktivitäten sind innerhalb derselben Journey nicht zulässig. |
| Keine Bedingungen zulässig | `ERR_PKG_SELECT_7` | Bedingungsaktivitäten können nicht in unitären Journey verwendet werden. Die Journey muss einem einzigen, linearen Pfad ohne Verzweigungslogik folgen. |
| Keine Warteaktivitäten | `ERR_PKG_SELECT_6` | Warteaktivitäten können nicht zu einheitlichen Journey hinzugefügt werden. Aktionen müssen sofort und ohne Verzögerungen ausgeführt werden. |
| Die Zeitüberschreitungs-/Fehlerübergänge müssen zum Endknoten gehen. | `ERR_PKG_SELECT_2` | Wenn Sie Zeitüberschreitung oder Fehlerübergänge für eine Aktion (z. B. eine E-Mail-Aktion) konfigurieren, müssen diese Pfade direkt auf einen Endknoten verweisen. Sie können keine Verbindung zu anderen Aktivitäten oder Aktionen in der Journey herstellen. |

>[!TIP]
>
>**Was dies für Sie bedeutet:** Wenn Sie das Paket „Auswählen“ verwenden und Verzweigungslogik, Warteaktivitäten oder mehrere Aktionen benötigen, müssen Sie stattdessen eine „Zielgruppe lesen“-Journey verwenden oder sich an den Adobe-Support wenden, um ein Upgrade für Ihr Paket durchzuführen.

### Journey-Versionen {#journey-versions-g}

Für [Journey-Versionen](../start/user-interface.md) gelten die folgenden Schutzmechanismen:

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einem **Zielgruppen-Qualifizierungsereignis** beginnen.
* Eine Journey, die in Version 1 mit einer Aktivität vom Typ **Zielgruppen-Qualifizierung** beginnt, muss in weiteren Versionen immer mit einer **Zielgruppen-Qualifizierung** beginnen.
* Die Zielgruppe und der Namespace, die unter **Zielgruppen-Qualifizierung** (dem ersten Knoten) ausgewählt wurden, können in neuen Versionen nicht geändert werden.
* Die Regel für den erneuten Eintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit **Zielgruppe lesen** beginnt, kann in Folgeversionen nicht mit einem anderen Ereignis beginnen.
* Sie können keine neue Version einer „Zielgruppe lesen“-Journey mit inkrementellem Lesen erstellen. Sie müssen die Journey duplizieren.

### Journeys und Profilerstellung {#journeys-limitation-profile-creation}

In Adobe Experience Platform gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenz ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von **20K Anfragen pro Sekunde (RPS)**.

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um Adobe Experience Platform ausreichend Zeit zu geben, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

### Ereignisse {#events-g}

Für [Ereignisse](../event/about-events.md) in Ihren Journeys gelten die folgenden Schutzmechanismen:

* Journey Optimizer unterstützt ein Spitzenvolumen von **5.000 eingehenden Journey-Ereignissen pro Sekunde** über alle Sandboxes hinweg. Weitere Informationen zu dieser Einschränkung finden Sie [auf dieser Seite](../event/about-events.md#event-thoughput).
* Die Verarbeitung der ersten Aktion auf der Journey kann bis zu **5 Minuten**, bis ereignisausgelöste Journey-Aktionen ausgeführt werden.
* Für systemgenerierte Ereignisse müssen Streaming-Daten, die zum Starten einer Customer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.
* Geschäftsereignisse können nicht zusammen mit unitären Ereignissen oder Zielgruppen-Qualifizierungaktivitäten verwendet werden.
* Unitäre Journeys (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung) enthalten einen Schutzmechanismus, der verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profileintritt wird standardmäßig **5 Minuten lang vorübergehend blockiert**. Wenn also beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres Ereignis verzeichnet wird (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.
* Journey Optimizer erfordert, dass Ereignisse an den Data Collection Core Service (DCCS) gestreamt werden, damit eine Journey ausgelöst werden kann. In Batches aufgenommene Ereignisse, über den **Abfrage-Service** eingefügte Ereignisse oder Ereignisse aus internen Journey Optimizer-Datensätzen (Nachrichten-Feedback, E-Mail-Tracking usw.) können nicht zum Auslösen einer Journey verwendet werden. Für Anwendungsfälle, bei denen Sie keine Streaming-Ereignisse empfangen können, müssen Sie stattdessen eine auf diesen Ereignissen basierende Zielgruppe erstellen und die Aktivität **Zielgruppe lesen** verwenden. Die Zielgruppenqualifizierung kann zwar theoretisch verwendet werden, wird jedoch nicht empfohlen, da sie aufgrund der verwendeten Aktionen zu nachgelagerten Problemen führen kann.

### Datenquellen {#data-sources-g}

Für [Datenquellen](../datasource/about-data-sources.md) in Ihren Journeys gelten die folgenden Schutzmechanismen:

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.
* Interne Adobe-Adressen (`.adobe.*`) sind in URLs und APIs nicht zulässig.

>[!NOTE]
>
>Da die Antworten jetzt unterstützt werden, sollten Sie für Anwendungsfälle mit externen Datenquellen benutzerdefinierte Aktionen anstelle von Datenquellen verwenden.

### Allgemeine Aktionen {#general-actions-g}

Für [Aktionen](../building-journeys/about-journey-activities.md) in Ihren Journeys gelten die folgenden Schutzmechanismen:

* Im Falle eines Fehlers werden systematisch drei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung einstellen. Mit Ausnahme von HTTP 401, 403 und 404 werden weitere Zustellversuche für alle HTTP-Fehler durchgeführt.
* Mit dem integrierten Ereignis **Reaktion** können Sie auf vorkonfigurierte Aktionen reagieren. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/reaction-events.md). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wird, müssen Sie ein spezielles Ereignis konfigurieren.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.
* Ein Profil kann nicht mehrmals zur gleichen Zeit in derselben Journey für alle aktiven [Journey-Versionen](../building-journeys/publish-journey.md#journey-create-new-version) vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](../building-journeys/end-journey.md)

### Benutzerdefinierte Aktionen {#custom-actions-g}

Für [benutzerdefinierte Aktionen](../action/action.md) in Ihren Journeys gelten die folgenden Schutzmechanismen:

* Eine Begrenzung von **300.000 Aufrufen über eine Minute** wird für alle benutzerdefinierten Aktionen pro Host und pro Sandbox definiert. Diese Begrenzung wird als bewegliches Fenster pro Sandbox und pro Endpunkt für Endpunkte mit Antwortzeiten von weniger als 0,75 Sekunden erzwungen. Für Endpunkte mit Antwortzeiten von mehr als 0,75 Sekunden gilt eine separate Begrenzung von **150.000 Aufrufen pro 30** (ebenfalls ein gleitendes Fenster).
* Die URL einer benutzerdefinierten Aktion unterstützt keine dynamischen Parameter.
* POST-, PUT- und GET-Aufrufmethoden werden unterstützt.
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit „.“ oder &quot;$&quot;.
* IP-Adressen sind in URLs nicht zulässig. Hostnamen verwenden.
* Interne Adobe-Adressen (`.adobe.*`) sind in URLs und APIs nicht zulässig.
* Integrierte benutzerdefinierte Aktionen können nicht entfernt werden.
* Benutzerdefinierte Aktionen unterstützen das JSON-Format nur bei Verwendung von Anfrage- oder Antwort-Payloads. Weitere Informationen finden Sie auf [dieser Seite](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Jeder Endpunkt, auf den eine benutzerdefinierte Aktion abzielt, muss mindestens **200 TPS** unterstützen. Vorsicht: Eine Drosselungskonfiguration darf nicht unter 200 TPS liegen. Je nach erwartetem Durchsatz kann sich eine hohe Reaktionszeit auf den tatsächlichen Durchsatz auswirken.

>[!TIP]
>
>**Was das für Sie bedeutet:** Die standardmäßige Begrenzung auf 300.000 Aufrufe/Min. schützt Ihre externen Endpunkte davor, durch den Journey-Durchsatz überlastet zu werden. Wenn Ihr Endpunkt mehr Last verarbeiten kann, können Sie diese Grenze mit der [Begrenzungs-API](../configuration/capping.md) oder der [Drosselungs-API](../configuration/throttling.md) erhöhen. Einen umfassenden Überblick darüber, wie Journey Optimizer eine Verbindung zu externen Systemen herstellt, finden Sie [dieser Seite](../configuration/external-systems.md). Wenden Sie sich an den Adobe-Support-Mitarbeiter, wenn Sie ein höheres organisatorisches Limit benötigen.

### Zusätzliche Kennungen {#supplemental}

Für die Verwendung zusätzlicher Kennungen in Journeys gelten spezifische Leitlinien. Sie sind auf [dieser Seite](../building-journeys/supplemental-identifier.md#guardrails) aufgeführt.

### Ausdruckseditor {#expression-editor}

Für den [Journey-Ausdruckseditor](../building-journeys/expression/expressionadvanced.md) gelten die folgenden Leitlinien:

* Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einer Aktivität vom Typ „Zielgruppe lesen“, „Zielgruppen-Qualifizierung“ oder „Geschäftsereignis“ beginnen. Sie müssen eine neue Zielgruppe erstellen und eine `inaudience`-Bedingung in der Journey verwenden.
* `timeSeriesEvents`-Attribute können nicht im Ausdruckseditor verwendet werden. Um auf Erlebnisereignisse auf Profilebene zuzugreifen, erstellen Sie eine neue Feldergruppe basierend auf einem `XDM ExperienceEvent`-Schema.

### Journey-Aktivitäten {#activities}

#### Aktivität des Typs „Zielgruppen-Qualifizierung“ {#audience-qualif-g}

Für die Journey-Aktivität [Zielgruppen-Qualifizierung](../building-journeys/audience-qualification-events.md) gilt der folgende Schutzmechanismus:

* Die Aktivität „Zielgruppen-Qualifizierung“ kann nicht mit Adobe Campaign-Aktivitäten verwendet werden.
* Zusätzliche Kennungen werden für Journeys des Typs „Zielgruppen-Qualifizierung“ nicht unterstützt.

Weitere Informationen zu Journey-Verarbeitungsraten und Durchsatzbeschränkungen finden Sie in [diesem Abschnitt](../building-journeys/entry-management.md#journey-processing-rate).

Weitere Leitplanken - einschließlich Empfehlungen zu Streaming vs. Batch-Zielgruppen und Einschränkungen bei der Komposition von Zielgruppen - sind auf [ Seite ](../building-journeys/audience-qualification-events.md#audience-qualification-guardrails).

#### Kampagnenaktivitäten {#ac-g}

Für die Aktivitäten **[!UICONTROL Campaign v7/v8]** und **[!UICONTROL Campaign Standard]** gelten die folgenden Schutzmechanismen:

* Adobe Campaign-Aktivitäten können nicht mit der Aktivität „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ verwendet werden.
* **[!UICONTROL Campaign Standard]**-Aktivitäten können nicht mit den anderen Kanalaktivitäten verwendet werden: Karte, Code-basiertes Erlebnis, E-Mail, Push, SMS, In-App-Nachrichten, Web.
* **[!UICONTROL Campaign v7/v8]**-Aktivitäten können zusammen mit nativen Kanalaktivitäten in derselben Journey verwendet werden.

#### Reaktionsereignisse {#reaction-events-g}

Spezifische Leitplanken gelten für **[!UICONTROL Reaktion]**-Ereignisse, einschließlich der Anforderung, die Aktivität unmittelbar nach einer Kanalaktion zu platzieren, und der Unfähigkeit, Nachrichten zu verfolgen, die auf einer anderen Journey gesendet werden. Sie sind auf [dieser Seite](../building-journeys/reaction-events.md#guardrails-limitations) aufgeführt.

#### In-App-Aktivität {#in-app-activity-limitations}

Für die Aktion **[!UICONTROL In-App-Nachrichten]** gelten die folgenden Schutzmechanismen: Weitere Informationen zu In-App-Nachrichten finden Sie auf [dieser Seite](../in-app/create-in-app.md).

* Diese Funktion ist derzeit nicht für Kundinnen und Kunden im Gesundheitswesen verfügbar.

* Personalisierung kann nur Profilattribute enthalten.

* Die In-App-Aktivität kann nicht mit **[!UICONTROL Campaign Standard]**-Aktivitäten verwendet werden.

* Die In-App-Anzeige ist an die Journey-Lebensdauer gebunden, d. h. wenn die Journey für ein Profil endet, werden alle In-App-Nachrichten innerhalb dieser Journey nicht mehr für dieses Profil angezeigt. Daher ist es nicht möglich, eine In-App-Nachricht direkt von einer Journey-Aktivität aus zu stoppen. Stattdessen müssen Sie die gesamte Journey beenden, damit die In-App-Nachrichten nicht mehr im Profil angezeigt werden.

* Im Testmodus hängt die In-App-Anzeige von der Journey-Lebensdauer ab. Um zu verhindern, dass die Journey während des Tests zu früh endet, passen Sie den **[!UICONTROL Wartezeit]**-Wert für Ihre **[!UICONTROL Warten]**-Aktivitäten an.

* **[!UICONTROL Reaktion]**-Aktivitäten können nicht verwendet werden, um auf ein Öffnen oder Klicken in der App zu reagieren.

* Es kann eine Aktivierungsverzögerung zwischen dem Zeitpunkt auftreten, zu dem ein Benutzerprofil eine In-App-Aktivität auf der Arbeitsfläche erreicht, und dem Zeitpunkt, zu dem es diese In-App-Nachricht zu sehen beginnt.

* Die Größe des Inhalts von In-App-Nachrichten ist auf **2 MB** beschränkt. Das Einschließen großer Bilder kann den Veröffentlichungsprozess behindern.

#### Aktivität „Inhaltsentscheidung“ {#content-decision-g}

Spezifische Leitplanken gelten für die Aktivität **[!UICONTROL Inhaltsentscheidung]**, einschließlich einer 48-stündigen Verzögerung, bevor aktualisierte Einverständnisrichtlinien in Entscheidungsrichtlinien wirksam werden. Sie sind auf [dieser Seite](../building-journeys/content-decision.md#guardrails) aufgeführt.

#### Aktivität „Springen“ {#jump-g}

Für die Aktivität **[!UICONTROL Springen]** gelten spezifische Schutzmechanismen. Sie sind auf [dieser Seite](../building-journeys/jump.md#jump-limitations) aufgeführt.

#### Aktivität des Typs „Zielgruppe lesen“ {#read-segment-g}

Für die Journey-Aktivität [Zielgruppe lesen](../building-journeys/read-audience.md) gelten die folgenden Schutzmechanismen:

* Streaming-Zielgruppen sind immer auf dem neuesten Stand, Batch-Zielgruppen werden jedoch zum Zeitpunkt des Abrufs nicht berechnet. Sie werden nur jeden Tag zum Zeitpunkt der täglichen Batch-Auswertung berechnet.
* Beim Journey-Eintritt verwenden Profile Attributwerte aus dem Snapshot der Batch-Zielgruppe. Wenn ein Profil jedoch eine Aktivität vom Typ **Warten** erreicht, aktualisiert die Journey Profilattribute automatisch, indem sie die neuesten Daten aus dem einheitlichen Profildienst (UPS) abruft. Dies bedeutet, dass sich Profilattribute während der Journey-Ausführung ändern können.
* Die Aktivität **Zielgruppe lesen** kann nicht mit Adobe Campaign-Aktivitäten verwendet werden.
* Die Aktivität **Zielgruppe lesen** kann nur als erste Aktivität in einer Journey oder nach einer Aktivität vom Typ „Geschäftsereignis“ verwendet werden.
* Eine Journey kann nur über eine Aktivität **Zielgruppe lesen** verfügen.
* Die Aktivität **Zielgruppe lesen** kann nur eine Zielgruppe pro Journey ansprechen. Wenn mehrere Zielgruppen erforderlich sind, führen Sie sie zuerst zu einer einzigen Zielgruppe zusammen. [Erfahren Sie mehr zum Kombinieren von Zielgruppen mithilfe von Kompositions-Workflows](../audience/get-started-audience-orchestration.md).
* Jede Organisation kann bis zu **5****Zielgruppe lesen**-Instanzen gleichzeitig ausführen (geplant oder durch ein Geschäftsereignis ausgelöst), und zwar in allen Sandboxes und Journey. Vermeiden Sie es, dass mehr als fünf Journeys des Typs **Zielgruppe lesen** zum exakt gleichen Zeitpunkt beginnen. Planen Sie die Startzeiten im Abstand von 5 bis 10 Minuten voneinander. Weitere Informationen zu Journey-Verarbeitungsraten finden Sie in [diesem Abschnitt](../building-journeys/entry-management.md#journey-processing-rate).
* Sandbox-Durchsatz: Das System verwaltet die Verarbeitung pro Sandbox mit maximal **20.000 Profilen pro Sekunde** die für alle Aktivitäten des Typs **Zielgruppe lesen** freigegeben sind. Einzelne Aktivitäten können mit zwischen **500 und 20.000 Profilen pro Sekunde konfiguriert**. Wenn Sandbox-Limits erreicht werden, können Aufträge in die Warteschlange gestellt werden.
* Maximale Wartezeit bei der Auftragsverarbeitung: **Zielgruppe lesen** Aufträge, die nicht innerhalb von **12 Stunden verarbeitet werden können** werden automatisch bereinigt und werden nicht ausgeführt.
* Wiederholungsversuche werden beim Abrufen des Exportvorgangs standardmäßig auf zielgruppenausgelöste Journey angewendet. Wenn bei der Erstellung des Exportvorgangs ein Fehler auftritt, werden weitere Zustellversuche alle 10 Minuten unternommen, maximal **1 Stunde**. Danach gilt die Journey als fehlgeschlagen und kann daher bis zu 1 Stunde nach der geplanten Zeit ausgeführt werden.
* Bei Journey, die zusätzliche IDs verwenden, ist die Leserate der Aktivität **Zielgruppe lesen** für jede Journey-Instanz auf maximal **500 Profile pro Sekunde** beschränkt.

>[!TIP]
>
>**Was dies für Sie bedeutet:** Das Limit für 5 gleichzeitige Instanzen ist eine feste Obergrenze für Ihr gesamtes Unternehmen. Wenn Sie mehrere Teams haben, die die Journey zum Lesen von Zielgruppen planen, sollten Sie die Startzeiten sorgfältig koordinieren. Aufträge, bei denen das 12-Stunden-Verarbeitungsfenster verpasst wird, werden im Hintergrund gelöscht. Bestätigen Sie die erfolgreiche Ausführung immer in den Journey-Protokollen.

Weitere Informationen zur Aktivität „Zielgruppe lesen“ finden Sie unter [Empfehlungen und Konfiguration](../building-journeys/read-audience.md#must-read).

#### Profilaktivität aktualisieren {#update-profile-g}

Für die Aktivität **[!UICONTROL Profil aktualisieren]** gelten spezifische Schutzmechanismen. Sie sind auf [dieser Seite](../building-journeys/update-profiles.md) aufgeführt.

#### Journey Pause {#pause-g}

Spezifische Leitplanken gelten für **pausierende Journey**, einschließlich einer maximalen Pausendauer von **14 Tagen** und einer **10 Millionen Profilbegrenzung** für alle pausierten Journey in Ihrem Unternehmen. Sie sind auf [dieser Seite](../building-journeys/journey-pause.md#journey-pause-guardrails) aufgeführt.

#### Journey-Probelauf {#dry-run-g}

Spezifische Leitplanken gelten für den **Journey-Probelauf** einschließlich der Zählung für kontaktierbare Profil- und Live-Journey-Kontingente. Sie sind auf [dieser Seite](../building-journeys/journey-dry-run.md#journey-dry-run-limitations) aufgeführt.

#### Journey Fragments {#fragments-journey-g}

Spezifische Leitplanken gelten für **Journey-Fragmente**, einschließlich maximal **20 Knoten pro Fragment** und **200 aktive Fragmente pro Sandbox**. Sie sind auf [dieser Seite](../building-journeys/journey-fragments.md#guardrails) aufgeführt.

#### Versenden in Schüben {#waves-g}

Spezifische Leitplanken gelten für **Wellenversand in Journey**, einschließlich eines Wellenbereichs von 2-10 und eines **30-minütigen**. Sie sind auf [dieser Seite](../building-journeys/send-using-waves.md#limitations-guardrails) aufgeführt.

#### Journey-Simulation {#simulation-g}

Spezifische Leitplanken gelten für die **Journey-Simulation**. Sie sind auf [dieser Seite](../building-journeys/simulate-journey.md#limitations) aufgeführt.

## Zielgruppen und Profile {#audiences-profiles}

In diesem Abschnitt werden Leitlinien für die Verwaltung von Zielgruppen, die Behandlung von Profilen und Überlegungen zu ansprechbaren Profilen behandelt.

### Leitlinien für Zielgruppen und Profile {#audience}

* Sie können bis zu **10 Audience-Kompositionen** einer Sandbox veröffentlichen. Wenn Sie diesen Schwellenwert erreicht haben, müssen Sie eine Komposition löschen, um Speicherplatz freizumachen, und eine neue veröffentlichen.

  Weitere Informationen zu Zielgruppenkompositionen finden Sie auf [dieser Seite](../audience/get-started-audience-orchestration.md).

* Bei der Datenaufnahme wird bei E-Mails die Groß- und Kleinschreibung beachtet. Das bedeutet, dass möglicherweise doppelte Profile erstellt (z. B. ein Profil für John.Greene@luma.com und ein anderes Profil für john.greene@luma.com) und beim Targeting der entsprechenden Person in Ihren [!DNL Journey Optimizer]-Journeys und Kampagnen verwendet werden.

* Wenn pseudonyme Profile (nicht authentifizierte Besuchende) mit Inbound-Kanälen angesprochen werden, sollten Sie eine Time-to-Live (TTL) für die automatische Profillöschung festlegen, um die Anzahl der ansprechbaren Profile und die damit verbundenen Kosten zu verwalten. [Weitere Informationen](#profile-management-inbound)

## Kanäle und Messaging {#channel-guardrails}

Dieser Abschnitt behandelt die Leitlinien für alle Kommunikationskanäle, einschließlich E-Mail, SMS, eingehenden Kanälen (Web, In-App, Code-basiert, Inhaltskarten) sowie Transaktionsnachrichten.

>[!NOTE]
>
>In seltenen Fällen können temporäre Ausfälle in einer bestimmten Region dazu führen, dass gültige Profile von Journeys ausgeschlossen werden oder dass E-Mails fälschlicherweise als Bounces markiert werden. Sobald die Services wiederhergestellt sind, überprüfen Sie die Journey-Protokolle erneut, verifizieren Sie die Einverständnisprofilfelder und veröffentlichen Sie die Journey bei Bedarf erneut. [In diesem Abschnitt](../configuration/manage-suppression-list.md#remove-from-suppression-list) erfahren Sie, wie Sie im Falle eines ISP-Ausfalls Profile aus der Unterdrückungsliste entfernen.

### Schutzmechanismen für E-Mails {#message-guardrails}

Für den [E-Mail-Kanal](../email/get-started-email.md) gelten die folgenden Schutzmechanismen:

* Es kann nicht dieselbe Versand-Domain zum Senden von Nachrichten von [!DNL Adobe Journey Optimizer] und einem anderen Produkt, z. B. [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage], verwendet werden.

Beim Entwerfen von E-Mail-Nachrichten sucht das System nach wichtigen Einstellungen und zeigt Warnungen (Empfehlungen und Best Practices) und Fehler (Blockierungsprobleme, die Tests oder die Aktivierung verhindern) an. Weitere Informationen zu E-Mail-Warnhinweisen und Validierungsanforderungen finden Sie in [diesem Abschnitt](../email/create-email.md#check-email-alerts).

#### Größe des Nachrichteninhalts für die Veröffentlichung einer Journey {#message-content-size}

Beim Veröffentlichen von Journey mit E-Mail-Nachrichten darf die Gesamtgröße des Nachrichteninhalts nach der Backend-Verarbeitung **2 MB** nicht überschreiten. Während der Veröffentlichung verarbeitet das System automatisch Nachrichteninhalte, indem es Links und Bilder patcht und Transformationen anwendet, wodurch die Payload-Größe über die Größe des erstellten Inhalts hinaus erhöht wird.

>[!CAUTION]
>
>Wenn der endgültige verarbeitete Nachrichteninhalt **2 MB** überschreitet, schlägt die Journey-Veröffentlichung fehl. Halten Sie den Inhalt der erstellten Nachricht deutlich unter 2 MB - idealerweise unter **1 MB** -, um einen Puffer von 300-400 KB für den Verarbeitungsaufwand im Backend zu ermöglichen.

**Best Practices zur Vermeidung von Veröffentlichungsfehlern:**

* Erstellte E-Mail-Inhalte unter 1 **speichern**
* Minimieren Sie die Anzahl der Inhaltsvarianten
* Optimieren und komprimieren Sie Bilder, bevor Sie sie zu Nachrichten hinzufügen
* Entfernen Sie nicht verwendete Assets und unnötige HTML-Elemente
* Testen Sie die Nachrichtengröße, bevor Sie Journeys in der Produktionsumgebung veröffentlichen

Wenn die Veröffentlichung einer Journey aufgrund der Inhaltsgröße fehlschlägt, reduzieren Sie den Inhalt Ihrer Nachricht und veröffentlichen Sie die Journey erneut.

### Leitlinien für SMS {#sms-guardrails}

Für den [SMS-Kanal](../mobile/get-started-mobile.md) gelten die folgenden Schutzmechanismen:

* Mediendateien für MMS können über eine unterstützte URL eingeschlossen werden. Bitte stellen Sie sicher, dass die Mediendatei separat hochgeladen wird.
* Die Synchronisierung von Nachrichten-Feedback ist derzeit nicht für MMS verfügbar.
* Die Einverständnisverwaltung erfolgt auf SMS-Kanalebene für MMS.

### Leitlinien für eingehende Kanäle {#inbound-guardrails}

* Damit Sie Aktionen für [Code-basierte Erlebnisse](../code-based/get-started-code-based.md) in [!DNL Journey Optimizer] verwenden und eine Payload mit Code-Inhalten bereitstellen können, die von Ihren Anwendungen genutzt werden kann, müssen die auf [dieser Seite](../code-based/code-based-prerequisites.md) beschriebenen Voraussetzungen erfüllt sein.

* Um in der Benutzeroberfläche von [!DNL Journey Optimizer] auf [Web-Seiten](../web/get-started-web.md) zuzugreifen oder sie dort zu erstellen, erfüllen Sie die Voraussetzungen auf [dieser Seite](../web/web-prerequisites.md).

* Um In-App-Nachrichten in Ihren Journeys und Kampagnen mit [!DNL Journey Optimizer] zu senden, erfüllen Sie die Versandvoraussetzungen auf [dieser Seite](../in-app/inapp-configuration.md).

* Damit Adobe Journey Optimizer Inhaltskarten korrekt anzeigt, müssen Sie die Adobe Experience Platform-Einstellungen auf [dieser Seite](../content-card/content-card-configuration-prereq.md) konfigurieren:

* Journey Optimizer unterstützt ein Spitzenvolumen von **5.000 eingehenden Anfragen pro Sekunde**. Diese Leitlinie gilt für alle eingehenden Anfragen, die von jedem der von Journey Optimizer unterstützten eingehenden Kanäle stammen können ([Web](../web/get-started-web.md), [In-App](../in-app/get-started-in-app.md), [Code-basierte Erlebnisse](../code-based/get-started-code-based.md), [Inhaltskarten](../../rp_landing_pages/content-card-landing-page.md)).

* **Journey Optimizer unterstützt zu jedem** maximal 500 aktive eingehende Aktionen. Diese eingehenden Aktionen werden gezählt, wenn sie Teil einer Live-Kampagne sind oder wenn sie ein Knoten sind, der in einer Live-Journey verwendet wird. Sobald diese Anzahl erreicht ist, müssen Sie ältere Kampagnen oder Journeys deaktivieren, die eingehende Aktionen verwenden, bevor neue gestartet werden können.

#### Profil-Management mit Inbound-Kanälen {#profile-management-inbound}

Inbound-Kanäle in [!DNL Journey Optimizer] können pseudonyme Profile ansprechen, d. h. Profile, die nicht authentifiziert oder noch nicht bekannt sind, weil sie zuvor noch nicht über andere Kanäle kontaktiert wurden. Dies ist beispielsweise der Fall, wenn das Targeting aller Besuchenden oder Zielgruppen auf der Grundlage temporärer IDs wie ECID erfolgt.

Dadurch erhöht sich die Gesamtzahl der kontaktierbaren Profile. Dies kann sich auf die Kosten auswirken, wenn die im Vertrag festgelegte Anzahl der von Ihnen erworbenen kontaktierbaren Profile überschritten wird. Lizenzmetriken für jedes Paket finden Sie auf der Seite [Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Sie können die Anzahl der kontaktierbaren Profile im [Dashboard zur Lizenznutzung](../audience/license-usage.md) überprüfen.

Um die Reichweite Ihrer ansprechbaren Profile auf ein vertretbares Maß zu begrenzen, empfiehlt Adobe, eine Time-to-Live (TTL) festzulegen, damit pseudonyme Profile automatisch aus dem Echtzeit-Kundenprofil gelöscht werden, wenn sie innerhalb eines bestimmten Zeitfensters nicht angezeigt oder angesprochen wurden. Adobe empfiehlt, den TTL-Wert auf **14 Tage** festzulegen, damit er mit der aktuellen Edge-Profil-TTL übereinstimmt.

>[!NOTE]
>
>Weitere Informationen zum Konfigurieren des Ablaufs von Daten für pseudonyme Profile finden Sie in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

### Leitlinien für Transaktionsnachrichten {#transactional-message-guardrails}

Journey Optimizer unterstützt in Kampagnen ein Spitzenvolumen von **500 Transaktionsnachrichten pro**.

## Inhalte und Assets {#content-assets}

Dieser Abschnitt enthält Leitlinien für die Erstellung und Verwaltung von Inhalten, einschließlich Landingpages, Subdomains und Fragmenten.

### Leitplanken des KI-Assistenten {#ai-assistant-g}

Leitplanken und Einschränkungen für die **KI-Assistenten zur Inhaltserstellung** - einschließlich unterstützter Kanäle (E-Mail, Push, Web, SMS) und Einschränkungen des Personalisierungseditors - sind auf [dieser Seite](../content-management/gs-generative.md#generative-guardrails) aufgeführt.

### Schutzmechanismen für Landingpages {#lp-guardrails}

Für [Landingpages](../landing-pages/get-started-lp.md) gelten die folgenden Schutzmechanismen:

* Es kann nur eine einzige **Formular**-Komponente auf einer einzelnen primären Seite verwendet werden.
* Die **Formular**-Komponente kann nicht in Unterseiten verwendet werden.
* Sie können keine Preheader zu einer Landingpage hinzufügen.
* Sie können die Option **Eigene Codierung** nicht auswählen, wenn Sie eine primäre Landingpage entwerfen.

### Leitlinien für Subdomains {#subdomain-guardrails}

Die Leitlinien und Einschränkungen für die Delegierung von Subdomains in Journey Optimizer werden auf [dieser Seite](../configuration/delegate-subdomain.md#guardrails) beschrieben.

### Schutzmechanismen für Fragmente {#fragments-guardrails}

Für [Fragmente](../content-management/fragments.md) gelten die folgenden Schutzmechanismen:

* Zum Erstellen, Bearbeiten, Archivieren und Veröffentlichen von Fragmenten benötigen Sie die Berechtigungen **[!DNL Manage library items]** und **[Fragment veröffentlichen]**, die im Produktprofil des **[!DNL Content Library Manager]** enthalten sind. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager)
* Visuelle Fragmente sind nur für den E-Mail-Kanal verfügbar.
* Ausdrucksfragmente sind nicht für den In-App-Kanal verfügbar.
* Visuelle Fragmente dürfen 100 **nicht überschreiten**. Ausdrucksfragmente dürfen nicht größer als **200 KB** sein.
* Damit ein Fragment in einer Journey oder Kampagne verwendet werden kann, muss es sich im Status **Live** befinden.
* [Kontextuelle Attribute](../personalization/personalization-build-expressions.md) werden in Fragmenten nicht unterstützt.
* Visuelle Fragmente sind zwischen den Modi „Designs verwenden“ und „Manuelle Formatierung“ nicht kreuzkompatibel. Um ein Fragment in einem Inhalt verwenden zu können, auf den Sie ein Design anwenden möchten, muss dieses Fragment im Modus „Designs verwenden“ erstellt werden. [Weitere Informationen zu Designs](../email/apply-email-themes.md)
* Wenn in einer Journey oder Kampagne das Tracking aktiviert ist und Sie Links zu einem Fragment hinzufügen, das in einer Nachricht verwendet wird, werden diese Links ebenso wie alle anderen in der Nachricht enthaltenen Links nachverfolgt. [Weitere Informationen über Links und Tracking](../email/message-tracking.md)

## Entscheidungs-Management {#decision-management}

### Leitlinien für die Entscheidungsfindung und das Entscheidungs-Management {#decisioning-guardrails}

Leitlinien und Einschränkungen, die Sie bei der Arbeit mit der Entscheidungsfindung oder dem Entscheidungs-Management beachten sollten, werden in den folgenden Abschnitten zur Entscheidungsfindung und dem Entscheidungs-Management beschrieben:

* [Leitlinien und Einschränkungen für die Entscheidungsfindung](../experience-decisioning/decisioning-guardrails.md)
* [Schutzmechanismen und Einschränkungen für das Entscheidungs-Management](../offers/decision-management-guardrails.md)

## Kampagnenorchestrierung {#campaign-orchestration}

### Leitlinien für die Kampagnenorchestrierung {#orchestration-guardrails}

Die bei der Kampagnenorchestrierung zu beachtenden Leitlinien und Einschränkungen werden in diesem Abschnitt beschrieben: [Leitlinien und Einschränkungen](../orchestrated/guardrails.md).
