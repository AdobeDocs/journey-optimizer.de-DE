---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Unterstützte Funktionen im Personalisierungseditor
description: Erfahren Sie, welche Funktionen des Personalisierungseditors bei der Personalisierung von Angebotsinhalten im Entscheidungs-Management (Offer Decisioning) unterstützt werden.
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: c4df41a2-d740-437c-acc3-957508c4a1c0
source-git-commit: c15bae97ea52243d65aa59fdd4e924dc4e1852d8
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 36%

---

# Unterstützte Funktionen im Personalisierungseditor {#personalization-editor-supported-functions}

Im Entscheidungs-Management verwenden Sie den **Personalisierungseditor** wenn Sie [Darstellungen hinzufügen](add-representations.md) und **Angebotsinhalte)** Bilder, Text, Links in Ihren Angeboten) personalisieren.

Das Offer Decisioning-Backend unterstützt bei **Personalisierung nur eine** der im Personalisierungseditor verfügbaren Funktionen. Auf dieser Seite werden alle Funktionen aufgelistet, die Sie sicher im Editor für Angebotsinhalte verwenden können. Erweitern Sie jeden Abschnitt, um die unterstützten Operatoren, Helper und Funktionen anzuzeigen.

>[!NOTE]
>
>Diese Funktionsliste gilt **nur für die Personalisierung von Angebotsinhalten** (Darstellungen). Entscheidungsregeln und Rangfolgeformeln verwenden verschiedene Editoren und sind nicht auf diese Untergruppe beschränkt.

## Liste der unterstützten Funktionen {#supported-functions-list}

+++ Operatoren

* Arithmetisch: `+` `-` `*` `/` `%`
* Logisch: `and` `or` `!`
* Vergleich: `=` `!=` `>` `>=` `<` `<=`

+++

+++ Helper

* Jeweils
* Mit
* Wenn
* Außer
* Zulassen
* Standardwert für Fallback
* Fragment
* datasetLookup
* externalDataLookup (Alpha)
* Inline
* URL
* Ausführungsmetadaten
* valueAtPath

+++

+++ Zeichenfolgen-Funktionen

| Anzeigename | Interner Name |
|--------------|---------------|
| Kleinbuchstaben | Kleinbuchstaben |
| Großbuchstaben | Großbuchstaben |
| Camel Case | Binnenmajuskel |
| Title Case | titleCase |
| Kürzen | trim |
| Links kürzen | leftTrim |
| Rechts kürzen | RightTrim |
| Ist leer | isEmpty |
| Gleich ohne Groß-/Kleinschreibung | equalsIgnoreCase |
| Entspricht nicht (Groß-/Kleinschreibung ignorieren) | notEqualWithIgnoreCase |
| Ersetzen | replace |
| Alle ersetzen | replaceAll |
| Verknüpfen | concat |
| Aufspaltung | split |
| Encode64 | Encode64 |
| Länge | length |
| MD5 | md5 |
| SHA256 | SHA256 |
| Ist wie | ist wie |
| Beginnt mit | startsWith |
| Beginnt nicht mit | doesNotStartWith |
| Endet mit | endet mit |
| Endet nicht mit | doesNotEndWith |
| Enthält | enthält |
| Enthält nicht | doesNotContains |
| Gleich | ist gleich |
| Ungleich | notEqualTo |
| Stimmt überein mit | „matches“ |
| Gruppe regelmäßiger Ausdrücke | RegexGroup |
| Zeichenfolge zu Zahl | stringToNumber |
| Zeichenfolge zu Datum | stringToDate |
| Zu Uhrzeit-/Datumsangabe | toDateTime |
| Nur zu Datums-/Uhrzeitangabe | toDateTimeOnly |
| E-Mail-Domain extrahieren | extractEmailDomain |
| E-Mail-Benutzernamen extrahieren | extractEmailUsername |
| Ist nicht leer | isNotEmpty |
| Index von | indexOf |
| Letzter Index von | lastIndexOf |
| Teilzeichenfolge | substr |
| Zu booleschem Wert | toBool |
| Zeichenfolge zu Ganzzahl | string_to_integer |
| Maskieren | Maske |
| Formatwährung abrufen | formatCurrency |
| Unicode-Zeichenwert abrufen | charCodeAt |
| QR-Code für beliebigen Text abrufen | qrCode |

+++

+++ Array-, Listen- und Set-Funktionen

| Anzeigename | Interner Name |
|--------------|---------------|
| Eindeutig | distinct |
| Enthalten | in |
| Nicht enthalten | notIn |
| Schnittmengen | überschneidet |
| Teilmenge von | subsetOf |
| Übergeordnete Gruppe von | Obermenge |
| Umfasst | Umfasst |
| Sortieren und Abrufen der ersten N im Array | topN |
| Sortieren und Abrufen der letzten N im Array | bottomN |
| Erstes Element | anführen |
| Anzahl | count |
| Summe | sum |
| Durchschnittlicher | Durchschnitt |
| Minimum | min |
| Maximum | max |

+++

+++ Zuordnungsfunktionen

| Anzeigename | Interner Name |
|--------------|---------------|
| Abrufen | get |
| Schlüssel | Schlüssel |
| Werte | Werte |

+++

+++ Objektfunktionen

| Anzeigename | Interner Name |
|--------------|---------------|
| Ist null | isNull |
| Ist nicht null | isNotNull |

+++

+++ Mathematische Funktionen

| Anzeigename | Interner Name |
|--------------|---------------|
| Zu Prozentwert | toPercentage |
| Aufrunden | aufrunden |
| Abrunden | abgerundet |
| Zu Präzision | toPrecision |
| Absolut | absolut |
| Zufällig | random |
| zu hexadezimal | toHexString |
| Zahl zum Gebietsschema abrufen | formatNumber |
| Zu Zeichenfolge | toString |
| To Int | toInt |
| Zu lang | toLong |

+++

+++ Datums-/Uhrzeitfunktionen

| Anzeigename | Interner Name |
|--------------|---------------|
| Jetzt | now |
| CurrentZonedDateTime abrufen | getCurrentZonedDateTime |
| Bis Datum | toDate |
| To Time | toTime |
| Zu Uhrzeit-/Datumsangabe | toDateTime |
| Nur zu Datums-/Uhrzeitangabe | toDateTimeOnly |
| Nur bis zum | toDateOnly |
| Nur zu Zeit | toTimeOnly |
| In Zeitzone | toTimeZone |
| Datum formatieren | formatDate |
| Datum/Uhrzeit formatieren | formatDateTime |
| Uhrzeit formatieren | formatTime |
| Datum analysieren | parseDate |
| Uhrzeit des Analysedatums | parseDateTime |
| Analysezeit | parseTime |
| Tage hinzufügen | Tage hinzufügen |
| Monate hinzufügen | AddMonths |
| Jahre hinzufügen | Jahre hinzufügen |
| Stunden hinzufügen | Stunden hinzufügen |
| Minuten hinzufügen | Minuten hinzufügen |
| Sekunden hinzufügen | addSecond |
| Tage subtrahieren | substrahierenTage |
| Monate abziehen | SubtractMonths |
| Jahre abziehen | subtrahierenJahre |
| Stunden subtrahieren | subtractHours |
| Minuten subtrahieren | subtractMinutes |
| Sekunden subtrahieren | subtractSeconds |
| Unterschied in Tagen | Tage vergleichen |
| Differenz in Monaten | diffMonths |
| Jahresdifferenz | diffYears |
| Stundenunterschied | Stunden vergleichen |
| Unterschied in Minuten | diffMinutes |
| Unterschied in Sekunden | diffSeconds |
| Tagesbeginn | startOfDay |
| Tagesende | endOfDay |
| Ist vor | isBefore |
| Ist nach | isAfter |

+++

+++ URL-Funktionen

| Anzeigename | Interner Name |
|--------------|---------------|
| URL kodieren | encodeUrl |
| URL decodieren | decodeUrl |
| URL-Abfrageparameter abrufen | getUrlQueryParam |
| URL-Protokoll abrufen | getUrlProtocol |
| URL-Host abrufen | getUrlHost |

+++

>[!NOTE]
>
>Wenn Sie bei der Personalisierung von Angebotsinhalten eine Funktion verwenden, die nicht in der obigen Liste aufgeführt ist, kann der Ausdruck zur Laufzeit fehlschlagen oder unerwartete Ergebnisse hervorrufen. Alle in [!DNL Journey Optimizer] Personalisierung verfügbaren Funktionen finden Sie unter [Liste der Helper-Funktionen](../../personalization/functions/functions.md). Nur die auf dieser Seite dokumentierte Teilmenge wird für die Personalisierung von Inhalten in Offer Decisioning unterstützt.
