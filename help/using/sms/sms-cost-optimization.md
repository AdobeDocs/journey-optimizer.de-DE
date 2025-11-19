---
solution: Journey Optimizer
product: journey optimizer
title: Best Practices für SMS zur Kostenoptimierung
description: Erfahren Sie, wie Sie die Kosten für SMS-Nachrichten optimieren können, indem Sie Zeichenbeschränkungen, Kodierung und Personalisierung in Journey Optimizer verwalten
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 13b3c8aa7fce85029167ef31feb7272e4877b7b0
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Best Practices für die SMS-Kostenoptimierung {#sms-cost-optimization}

SMS-Nachrichten werden in der Regel von Providern mit maximal 160 Zeichen pro Nachricht in Rechnung gestellt. Das Senden von SMS-Nachrichten kann zusätzliche Kosten verursachen, wenn Nachrichten in mehrere Teile aufgeteilt werden.

Befolgen Sie diese Richtlinien, um Ihre Messaging-Strategie zu optimieren und Kosten zu senken.

## Nachrichten kurz halten {#keep-messages-short}

Journey Optimizer erlaubt bis zu 1.500 Zeichen in einem SMS-Nachrichtentext. Bei Überschreitung dieses Grenzwerts wird eine Warnung angezeigt und bei Meldungen, die diesen Schwellenwert überschreiten, wird ein Trigger angezeigt.

Die meisten SMS-Anbieter unterstützen die GSM-7-Bit-Kodierung, bei der eine einzelne SMS bis zu 160 Zeichen enthalten kann. Nachrichten, die diese Länge überschreiten, werden automatisch in mehrere SMS-Teile aufgeteilt (Verkettung):

* **Weniger als 160 Zeichen**: 1 SMS-Teil
* **161-306 Zeichen**: 2 SMS-Teile
* **307-459 Zeichen**: 3 SMS-Teile

**Um die Kosten zu minimieren** sollten Nachrichten unter 160 Zeichen lang sein, damit sie als ein einziger SMS-Teil in Rechnung gestellt werden.

Eine Nachricht mit 1.600 Zeichen kann beispielsweise 10 SMS-Guthaben verbrauchen, auch wenn sie in Journey Optimizer als eine einzige Nachricht angezeigt wird.

## Vermeiden Sie Sonderzeichen, die länger sind {#avoid-special-characters}

Bestimmte Zeichen, z. B. `| ^ € { } [ ] ~ \`, werden bei der GSM-Kodierung als zwei Zeichen gezählt. Das Einschließen dieser Zeichen kann dazu führen, dass Ihre Nachricht das **160-Zeichen-Limit** überschreitet.

## UCS-2-Kodierung verhindern {#prevent-ucs2-encoding}

Wenn die Nachricht Nicht-GSM-Zeichen enthält, wie z. B. chinesischen oder arabischen Text, Markensymbole oder harte Rückgaben von Rich-Formatierungs-Tools, wird die Nachricht vom Provider mit UCS-2 codiert, das nur 70 Zeichen pro SMS unterstützt.

Die Verwendung der UCS-2-Kodierung kann die Zeichenanzahl erhöhen und sich daher auf die Nachrichtenabrechnung mit Ihrem Dienstleister auswirken.

Beispielsweise wird eine Unicode-Nachricht mit 200 Zeichen in drei SMS-Teilen gesendet.

## Best Practices für die Inhaltserstellung {#authoring-best-practices}

Erstellen Sie die endgültige SMS-Nachricht direkt in Journey Optimizer oder fügen Sie sie aus Nur-Text-Programmen ein.

Vermeiden Sie die Verwendung von Rich-Text-Anwendungen, da sie verborgene Zeichen oder Zeilenumbrüche einführen können, die die UCS-2-Kodierung des Triggers beeinflussen und möglicherweise sowohl die Anzahl der SMS-Teile als auch die damit verbundenen Kosten erhöhen.

## Zeichenanzahl vor dem Senden überprüfen {#check-character-count}

Verwenden Sie Textverarbeitungsprogramme oder das Journey Optimizer-Menü **[!UICONTROL Inhalt simulieren]**, um die Zeichenanzahl zu überprüfen.

Während Journey Optimizer während der Inhaltsimulation eine Zeichenanzahl einschließlich Leerzeichen anzeigt, beachten Sie Folgendes:

* Er enthält **nicht** Zeichen, die durch dynamische Personalisierung generiert wurden, oder bestimmte Sonderzeichen.

* Der **x/1500-Zähler** dient als visueller Indikator für das technische Payload-Limit, nicht für das Nachrichtenlimit pro Nachricht, z. B. das 160-stellige GSM-7-Bit-Limit.

* Adobe unterstützt die UTF-8-Kodierung im Editor, die sich von der GSM-7-Bit-Kodierung unterscheidet.

## Grundlegendes zum Reporting {#understanding-reporting}

**Journey Optimizer-Reporting** Zählt die gesamte Nachricht als einen Versand, unabhängig von den SMS-Teilen.

**Provider-Reporting** spiegelt die tatsächliche Anzahl der für den Versand verwendeten SMS-Nachrichtenteile wider und sollte zur Bestätigung der Abrechnung und möglicher Überschüsse referenziert werden. Wenn Adobe Ihr SMS-Provider über Sinch ist, erhalten Sie diesen Abrechnungsbericht monatlich separat.

## Überlegungen zu Personalization {#personalization-considerations}

Die dynamische Personalisierung kann die Länge einer Nachricht erhöhen. Wenn Sie beispielsweise eine Variable durch einen langen Vornamen ersetzen, können weitere Zeichen hinzugefügt werden.

## Weitere Ressourcen {#additional-resources}

Überprüfen Sie die unterstützten Zeichen und Kodierungsregeln im [Sinch Character Support Guide](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)

