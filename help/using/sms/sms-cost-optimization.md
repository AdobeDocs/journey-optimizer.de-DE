---
solution: Journey Optimizer
product: journey optimizer
title: Best Practices für SMS zur Kostenoptimierung
description: Weitere Informationen zum Senken der Ausgaben für SMS-Nachrichten durch Verwaltung von Zeichenbeschränkungen, Kodierung und Personalisierung in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 13b3c8aa7fce85029167ef31feb7272e4877b7b0
workflow-type: ht
source-wordcount: '521'
ht-degree: 100%

---

# Best Practices für Optimierung der SMS-Kosten {#sms-cost-optimization}

SMS-Nachrichten werden von Anbietern in der Regel mit maximal 160 Zeichen pro Nachricht in Rechnung gestellt. Das Senden von SMS-Nachrichten kann zusätzliche Kosten verursachen, wenn Nachrichten in mehrere Teile aufgeteilt werden.

Befolgen Sie diese Leitlinien, um Ihre Messaging-Strategie zu optimieren und Kosten zu senken.

## Kurzhalten von Nachrichten {#keep-messages-short}

Journey Optimizer erlaubt in einem SMS-Nachrichtentext bis zu 1.500 Zeichen. Bei Überschreitung dieses Limits wird eine Warnung angezeigt. Zudem wird bei Nachrichten, die den Schwellenwert überschreiten, ein Fehler ausgelöst.

Die meisten SMS-Anbieter unterstützen GSM-7-Bit-Kodierung, bei der eine einzelne SMS bis zu 160 Zeichen enthalten kann. Nachrichten, die diese Länge überschreiten, werden automatisch in mehrere SMS-Teile aufgeteilt (Verkettung):

* **Weniger als 160 Zeichen**: 1 SMS-Teil
* **161 bis 306 Zeichen**: 2 SMS-Teile
* **307 bis 459 Zeichen**: 3 SMS-Teile

**Zum Minimieren der Kosten** sollten Nachrichten maximal 160 Zeichen lang sein, damit sie als ein SMS-Teil in Rechnung gestellt werden.

Eine Nachricht mit 1.600 Zeichen kann beispielsweise 10 SMS-Credits verbrauchen, auch wenn sie in Journey Optimizer als eine einzige Nachricht angezeigt wird.

## Vermeiden von Sonderzeichen, die die Nachricht verlängern {#avoid-special-characters}

Manche Zeichen (wie z. B. `| ^ € { } [ ] ~ \`) werden bei der GSM-Kodierung als zwei Zeichen gezählt. Das Verwenden solcher Zeichen kann dazu führen, dass Ihre Nachricht das **160-Zeichen-Limit** schneller überschreitet.

## Vermeiden von UCS-2-Kodierung {#prevent-ucs2-encoding}

Wenn die Nachricht Nicht-GSM-Zeichen enthält (wie z. B. chinesischen oder arabischen Text, Markensymbole oder harte Zeilenumbrüche bei Rich-Formatierungs-Tools), wird die Nachricht vom Anbieter mit UCS-2 kodiert. Dabei werden nur 70 Zeichen pro SMS unterstützt.

Eine Verwendung von UCS-2-Kodierung kann die Zeichenanzahl erhöhen und sich somit auf die Nachrichtenabrechnung Ihres Dienstleisters auswirken.

Beispielsweise wird eine Unicode-Nachricht mit 200 Zeichen in drei SMS-Teilen gesendet.

## Best Practices für das Authoring {#authoring-best-practices}

Erstellen Sie die endgültige SMS-Nachricht direkt in Journey Optimizer oder fügen Sie sie aus Nur-Text-Anwendungen ein.

Vermeiden Sie den Einsatz von Rich-Text-Anwendungen, da es hier verborgene Zeichen oder Zeilenumbrüche geben kann, die UCS-2-Kodierung auslösen und ggf. sowohl die Anzahl der SMS-Teile als auch die damit verbundenen Kosten erhöhen.

## Prüfen der Zeichenanzahl vor dem Senden {#check-character-count}

Verwenden Sie Nur-Text-Anwendungen oder das Journey Optimizer-Menü **[!UICONTROL Inhalt simulieren]**, um die Zeichenanzahl zu prüfen.

Journey Optimizer zeigt bei der Inhaltssimulation zwar eine Zeichenanzahl einschließlich Leerzeichen an, doch Sie sollten Folgendes beachten:

* Die Zeichenanzahl enthält **keine** Zeichen, die durch dynamische Personalisierung generiert wurden. Auch bestimmte Sonderzeichen sind nicht enthalten.

* Der **x/1.500-Zähler** dient als visueller Indikator für das technische Payload-Limit, nicht für das nachrichtenspezifische Limit (z. B. das 160-stellige 7-Bit-Limit bei GSM).

* Adobe unterstützt UTF-8-Kodierung im Editor, die sich von GSM-7-Bit-Kodierung unterscheidet.

## Grundlegendes zum Reporting {#understanding-reporting}

**Journey Optimizer-Reporting** zählt die gesamte Nachricht als einen Versand, unabhängig von der Anzahl der SMS-Teile.

**Anbieter-Reporting** spiegelt die tatsächliche Anzahl der für den Versand verwendeten SMS-Teile wider und sollte zur Überprüfung der Abrechnung und möglicher Überschüsse konsultiert werden. Wenn Adobe über Sinch Ihr SMS-Anbieter ist, erhalten Sie diesen Abrechnungsbericht monatlich separat.

## Überlegungen zu Personalisierung {#personalization-considerations}

Dynamische Personalisierung kann die Länge einer Nachricht erhöhen. Wenn Sie beispielsweise eine Variable durch einen langen Vornamen ersetzen, werden ggf. weitere Zeichen hinzugefügt.

## Weitere Ressourcen {#additional-resources}

Weitere Informationen zu unterstützten Zeichen und Kodierungsregeln finden Sie im [Handbuch zur Unterstützung von Zeichen in Sinch](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)

