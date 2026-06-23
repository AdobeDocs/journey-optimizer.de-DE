---
solution: Journey Optimizer
product: journey optimizer
title: Bedingte Anweisung (if, then, else)
description: Erfahren Sie mehr über die bedingte Anweisung
feature: Journeys
role: Developer
level: Experienced
keywords: erweitert, Bedingung, Aktion, Journey
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 29%

---

# Bedingte Anweisung (if, then, else) {#conditional-instruction}

Die bedingte Anweisung (if, then, else) wird im erweiterten Editor unterstützt. Sie ermöglicht die Definition komplexerer Ausdrücke. Sie umfasst die folgenden Elemente:

* **[!UICONTROL if]**: die Bedingung, die zuerst ausgewertet werden soll.
* **[!UICONTROL then]**: der auszuwertende Ausdruck, falls das Ergebnis der Auswertung der Bedingung wahr ist.
* **[!UICONTROL else]**: der auszuwertende Ausdruck, falls das Ergebnis der Auswertung der Bedingung falsch ist.

>[!NOTE]
>
>Alle Ausdrücke müssen in Klammern gesetzt werden.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` muss einen booleschen Wert (**boolean**) zurückgeben.

`<expression2>` und `<expression3>` müssen denselben Typ oder kompatible Typen aufweisen. Folgende Signaturen und zurückgegebene Typen werden unterstützt:

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**Verwendung**

Mit der bedingten Anweisung können Sie den Workflow der Journey optimieren, indem Sie die Anzahl der Bedingungsaktivitäten reduzieren. Beispielsweise können Sie innerhalb derselben Aktionsaktivität zwei Alternativen für eine Felddefinition angeben, wobei nur ein Bedingungsausdruck verwendet wird.

Beispiel für eine Aktionsaktivität (für ein Feld, das eine Zeichenfolge als Ergebnis der bedingten Anweisung erwartet):

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden die `if / then / else` Bedingungsanweisungen erläutert, die im erweiterten Ausdruckseditor von Journey verfügbar sind, einschließlich Syntaxregeln, unterstützter Typkombinationen und eines praktischen Anwendungsbeispiels.

**intents:**

* Schreiben Sie einen bedingten Ausdruck mit `if`, `then` und `else`, um auf der Grundlage einer booleschen Bedingung verschiedene Werte zurückzugeben
* Verringern Sie die Anzahl der Bedingungsaktivitäten in einem Journey durch Einbetten einer Bedingungslogik in eine einzelne Aktionsaktivität
* Bestimmen, welche Datentypkombinationen für die `then` und `else` Verzweigungen gültig sind
* Wenden Sie die bedingte Anweisung an, um Push-Benachrichtigungs-Token je nach Gerätemodell entweder an APNS oder an FCM zu leiten

**Glossar:**

* **Bedingte Anweisung**: Ein `if / then / else` Ausdruckskonstrukt im erweiterten Editor, das einen booleschen Wert auswertet und einen von zwei Ausdrücken zurückgibt *(produktspezifisch)*
* **Erweiterter Ausdruckseditor**: Die Journey Optimizer-Oberfläche zum Schreiben komplexer Ausdrücke, die in Bedingungen, Warteaktivitäten und der Zuordnung von Aktionsparametern verwendet werden *(produktspezifisch)*

**Leitplanken:**

* Um alle Ausdrücke in den `if`-, `then`- und `else` sind Klammern erforderlich
* Die `if` (`<expression1>`) muss einen booleschen Typ zurückgeben
* Die `then`- und `else`-Ausdrücke (`<expression2>` und `<expression3>`) müssen vom gleichen Typ oder von kompatiblen Typen sein (z. B. sind `decimal` und `integer` kompatibel, `string` und `integer` nicht)
* Nicht alle Typkombinationen werden unterstützt - nur die in der Tabelle Unterstützte Signaturen aufgeführten Paare sind gültig

**Terminologie:**

* Kanonische Bezeichnung: Bedingte Anweisung — Akronym: none — Varianten: if/then/else, ternäre Bedingung
* Synonyme: „Bedingte Anweisung“ = „Inline-Bedingung“ = „if-then-else Ausdruck“
* Nicht verwechseln: Bedingte Anweisung (Inline-Ausdruck) ≠ Bedingungsaktivität (ein Journey-Arbeitsflächenknoten)

**FAQ:**

* **F: Muss die `if`-Klausel in Klammern eingeschlossen werden?** — Ja, um alle Ausdrücke einschließlich der Bedingung in der `if`-Klausel sind Klammern erforderlich.
* **F: Kann ich `if / then / else` verwenden, um eine Zahl aus einer Verzweigung und eine Zeichenfolge aus einer anderen Verzweigung zurückzugeben?** — Nein; `<expression2>` und `<expression3>` müssen dieselben oder kompatible Typen aufweisen.
* **F: Wie reduziert die bedingte Anweisung die Komplexität des Journey?** - Damit können Sie zwei Feldwertalternativen innerhalb einer einzelnen Aktionsaktivität mit einem Ausdruck angeben, wobei ein separater Aktivitätsknoten für Bedingungen auf der Arbeitsfläche vermieden wird.
* **F: Welchen Typ gibt die bedingte Anweisung zurück, wenn beide Verzweigungen Zeichenfolgen sind?** — Gibt einen `string` zurück.
* **F: Kann `if / then / else` verwendet werden, um einen Push-Benachrichtigungskanal auszuwählen?** — Ja. Beispielsweise kann das Gerätemodell evaluiert werden, um `'apns'` für Apple-Geräte oder `'fcm'` für andere zurückzugeben.

+++
