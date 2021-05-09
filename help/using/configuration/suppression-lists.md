---
title: Überwachung der Nachrichtenausführung
description: Richtlinien zur Überwachung und Bereitstellung
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: monitoring and deliverability
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 7a097706-4da2-4f7b-885f-1a9d6b7c9a91
translation-type: tm+mt
source-git-commit: 9368f01d2a15879ce58518b09a78d09d5390818b
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Verwalten von Unterdrückungs-Listen {#manage-suppression-lists}

Eine Unterdrückungs-Liste besteht aus E-Mail-Adressen, die Sie von Ihren Versänden ausschließen möchten, da das Senden an diese Kontakte Ihren Ruf und Ihre Versand beeinträchtigen könnte.

Die Journey Optimizer **Suppression-Liste** wird auf Ihrer eigenen Umgebung verwaltet. Es sammelt Spam-Beschwerden, harte Absprünge und weiche Absprünge, die konsistent ablaufen.

## Warum unterdrückende Listen? {#why-suppression-lists}

Um die E-Mail-Nachrichten zu kontrollieren, die von den Inbox-Inhabern empfangen werden, und sicherzustellen, dass sie nur die von ihnen gewünschten Nachrichten erhalten, verfügen Internet-Dienstleister (ISPs) und kommerzielle Spam-Filter über eigene Algorithmen, um den allgemeinen Ruf von E-Mail-Absendern anhand der IP-Adressen und der sendenden Domäne(n), die sie verwenden, zu verfolgen.

Wenn Sie kein Feedback abgeben (z. B. Spam-Beschwerden, Absprünge usw.) berücksichtigen, wird Ihr Ruf heruntergestuft. Die Unterdrückungs-Liste hilft Ihnen, das Feedback der ISPs zu berücksichtigen.

Die Empfänger, deren E-Mail-Adressen unterdrückt werden, werden automatisch aus dem Versand der Nachricht ausgeschlossen. Dies beschleunigt die Versand, da die Fehlerquote sich erheblich auf die Geschwindigkeit des Versands auswirkt.

### Spam-Beschwerden {#spam-complaints}

Die Unterdrückungs-Liste erfasst E-Mail-Adressen, die Ihre Nachricht als Spam kennzeichnen. Das Senden an Empfänger, nachdem sie eine Spam-Beschwerde eingereicht haben, kann sich sehr auf Ihren Ruf auswirken, da es ISPs mitteilt, dass Sie unerwünschte E-Mails senden und möglicherweise nicht auf Ihre Empfänger hören.

Dies könnte dazu führen, dass Ihre IP-Adresse oder die sendende Domäne blockiert wird, was vermieden werden kann, dass diese Adressen auf der Unterdrückungs-Liste vorhanden sind.

### Absprünge {#bounces}

Darüber hinaus enthält die Unterdrückungs-Liste E-Mail-Adressen, die zu oft abgesprungen werden oder zu oft abspringen. Wenn Sie weiterhin an diese Adressen senden, kann dies sich auf Ihre Versand-Raten auswirken, da es den ISPs mitteilt, dass Sie möglicherweise die Best Practices zur Wartung der E-Mail-Adressen nicht befolgen und daher möglicherweise kein vertrauenswürdiger Absender sind.

## Suppression-Liste-Management {#suppression-list-management}

Die Journey Optimizer-Unterdrückungs-Liste erfasst E-Mail-Adressen und Domänen, die in allen Mailings **in einer Client-Umgebung** unterdrückt werden, was für eine IMS-Organisations-ID gilt, die mit einer Sandbox-ID verknüpft ist.

Mit der Unterdrückungs-Liste können Sie automatisch Folgendes erfassen:
* E-Mail-Adressen, die ungültig sind oder die durchgängig weich abspringen und sich negativ auf Ihren E-Mail-Ruf auswirken können, wenn Sie sie weiterhin in Ihre Versand aufnehmen.
* Empfänger, die eine Spam-Beschwerde gegen eine Ihrer E-Mails ausstellen.

Wenn zum Beispiel jemand an einen Kundendienst schreibt, der darum bittet, nie wieder E-Mails von Ihnen zu erhalten, wird die E-Mail-Adresse dieser Person in Ihrer gesamten Instanz unterdrückt, und Sie können diese Adresse nicht mehr an diese Adresse senden.

<!--For each address, the basic reason for suppression (soft bounces, a hard bounce or a spam complaint) will be shown in the Suppression list.-->

### Versand-Fehler {#delivery-failures}

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

Es gibt drei Fehlertypen, wenn ein Versand fehlschlägt:

* **Harter Absprung**. Eine feste Adresse weist auf eine ungültige E-Mail-Adresse hin (d. h. eine nicht vorhandene E-Mail-Adresse). Dies umfasst eine Absprungmeldung des empfangenden E-Mail-Servers, in der explizit angegeben wird, dass die Adresse ungültig ist, z. B. &quot;Unbekannte Nutzer&quot;.
* **Weicher Absprung**. Dies ist ein temporärer E-Mail-Absprung, der für eine gültige E-Mail-Adresse aufgetreten ist.
* **Ignoriert**. Hierbei handelt es sich um einen E-Mail-Absprung, der für eine gültige E-Mail-Adresse aufgetreten ist, aber als vorübergehend bekannt ist, z. B. ein fehlgeschlagener Verbindungsversuch, ein temporäres Spam-Problem (E-Mail-Ruf) oder ein temporäres technisches Problem.

Die harten Absprünge und weichen Absprünge können ein Grund dafür sein, dass eine E-Mail-Adresse automatisch zur Unterdrückungs-Liste hinzugefügt wird.

### Was ist mit der Unterdrückungs-Liste? {#what-s-on-suppression-list}

E-Mail-Adressen werden wie folgt zur Unterdrückungs-Liste hinzugefügt:

* Alle **Hardbounces** und **Spam-Beschwerden** senden die entsprechenden E-Mail-Adressen nach einem einzigen Vorfall automatisch an die Suppression-Liste.

* **Weiche** Absprünge senden nicht sofort eine E-Mail-Adresse an die Unterdrückungs-Liste, sondern erhöhen einen Fehlerzähler. Wenn der Fehlerzähler den Schwellenwert erreicht, wird die Adresse der Unterdrückungs-Liste hinzugefügt.

   Der Schwellenwert wird auf drei Fehler festgelegt:
   * Im selben Versand wird die Adresse beim dritten Versuch unterdrückt.
   * Wenn es unterschiedliche Versand gibt und zwei Fehler im Abstand von mindestens 24 Stunden auftreten, wird der Fehlerzähler bei jedem Fehler inkrementiert und die Adresse wird auch beim dritten Versuch unterdrückt.

   Wenn ein Versand nach einem erneuten Versuch erfolgreich war, wird der Fehlerzähler der Adresse erneut initialisiert.

### weitere Zustellversuche {#retries}

Wenn eine Nachricht aufgrund eines temporären Absprungs des Typs **Ignoriert** fehlschlägt, werden weitere Zustellversuche für **3,5 Tage** ausgeführt, nachdem die Nachricht der E-Mail-Warteschlange hinzugefügt wurde.

Die minimale Verzögerung zwischen weiteren Zustellversuchen und die maximale Anzahl der auszuführenden weitere Zustellversuche sind <!--managed by the Enhanced MTA,--> abhängig davon, wie gut eine IP läuft, sowohl historisch als auch aktuell in einer bestimmten Domäne.

Nach 3,5 Tagen werden alle Nachrichten in der Warteschlange zum Wiederholen aus der Warteschlange entfernt und als Absprung zurückgesendet.
