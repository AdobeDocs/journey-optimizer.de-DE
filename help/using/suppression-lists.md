---
title: Überwachen der Nachrichtenausführung
description: Lernen Sie Richtlinien zur Überwachung und Zustellbarkeit kennen
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: ht
source-wordcount: '775'
ht-degree: 100%

---

# Verwalten von Unterdrückungslisten {#manage-suppression-lists}

![](assets/do-not-localize/badge.png)

Eine Unterdrückungsliste besteht aus E-Mail-Adressen, die Sie von Ihren Sendungen ausschließen möchten, da das Senden an diese Kontakte Ihren Ruf als Versender und Ihre Versandraten beeinträchtigen könnte.

Die **Unterdrückungsliste** in Journey Optimizer wird auf der Ebene Ihrer eigenen Umgebung verwaltet. Sie sammelt Spam-Beschwerden, Hardbounces und Softbounces, die ständig auftreten.

## Warum Unterdrückungslisten? {#why-suppression-lists}

Um die E-Mail-Nachrichten zu kontrollieren, die von den Inhabern der Posteingänge empfangen werden, und sicherzustellen, dass sie nur die von ihnen gewünschten Nachrichten erhalten, verfügen Internet-Dienstleister (ISPs) und kommerzielle Spam-Filter über eigene Algorithmen, um den allgemeinen Ruf von E-Mail-Versendern anhand der IP-Adressen und der sendenden Domain(s), die sie verwenden, zu verfolgen.

Wenn Sie deren Feedback (z. B. Spam-Beschwerden, Bounces usw.) nicht berücksichtigen, werden sie Ihre Reputation herabstufen. Die Unterdrückungsliste hilft Ihnen, das Feedback der ISPs zu berücksichtigen.

Die Empfänger, deren E-Mail-Adressen unterdrückt werden, werden automatisch vom Versand der Nachricht ausgeschlossen. Dies beschleunigt den Versand, da sich die Fehlerrate maßgeblich auf die Versandgeschwindigkeit auswirkt.

### Spam-Beschwerden {#spam-complaints}

Die Unterdrückungsliste erfasst E-Mail-Adressen, die Ihre Nachricht als Spam kennzeichnen. Das Senden an Empfänger, nachdem sie eine Spam-Beschwerde eingereicht haben, kann sich sehr auf Ihren Ruf auswirken, da es den ISPs mitteilt, dass Sie unerwünschte E-Mails senden und möglicherweise nicht auf Ihre Empfänger hören.

Dies könnte dazu führen, dass Ihre IP-Adresse oder die sendende Domain blockiert wird. Das kann vermieden werden, wenn diese Adressen auf der Unterdrückungsliste vorhanden sind.

### Bounces {#bounces}

Darüber hinaus enthält die Unterdrückungsliste E-Mail-Adressen, die zu Hardbounces führen oder zu oft zu Softbounces führen. Wenn Sie weiterhin an diese Adressen senden, kann sich dies auf Ihre Versandraten auswirken, da es den ISPs mitteilt, dass Sie möglicherweise die Best Practices zur Wartung von E-Mail-Adressen nicht befolgen und daher möglicherweise kein vertrauenswürdiger Versender sind.

## Verwalten der Unterdrückungsliste {#suppression-list-management}

Die Unterdrückungsliste in Journey Optimizer sammelt E-Mail-Adressen und Domains, die für alle Mailings **in einer einzigen Client-Umgebung** unterdrückt werden, d. h. spezifisch für eine IMS-Organisations-ID, die mit einer Sandbox-ID verbunden ist.

Mit der Unterdrückungsliste können Sie automatisch Folgendes erfassen:
* E-Mail-Adressen, die ungültig sind oder die durchgängig zu Softbounces führen und sich negativ auf Ihre E-Mail-Reputation auswirken können, wenn Sie sie weiterhin in Ihre Sendungen aufnehmen.
* Empfänger, die eine Spam-Beschwerde gegen eine Ihrer E-Mails einreichen.

Wenn zum Beispiel jemand an den Kundendienst schreibt und darum bittet, nie wieder E-Mails von Ihnen zu erhalten, wird die E-Mail-Adresse dieser Person in Ihrer Instanz unterdrückt und Sie können nicht mehr an diese Adresse versenden.

<!--For each address, the basic reason for suppression (soft bounces, a hard bounce or a spam complaint) will be shown in the Suppression list.-->

### Versandfehler {#delivery-failures}

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

Bei Fehlschlägen des Versands gibt es drei Typen von Fehlern:

* **Hardbounce**. Ein Hardbounce weist auf eine ungültige E-Mail-Adresse hin (d. h. eine E-Mail-Adresse, die nicht existiert). Dies umfasst eine Bounce-Nachricht des empfangenden E-Mail-Servers, in der explizit angegeben wird, dass die Adresse ungültig ist, z. B. „Nutzer unbekannt“.
* **Softbounce**. Dies ist ein temporärer E-Mail-Bounce, der bei einer gültige E-Mail-Adresse aufgetreten ist.
* **Ignoriert**. Dies ist ein E-Mail-Bounce, der bei einer gültigen E-Mail-Adresse aufgetreten ist, aber bekanntermaßen vorübergehend ist, z. B. ein fehlgeschlagener Verbindungsversuch, ein vorübergehendes Spam-Problem (E-Mail-Reputation) oder ein vorübergehendes technisches Problem.

Hardbounces und Softbounces können ein Grund dafür sein, dass eine E-Mail-Adresse automatisch in die Unterdrückungsliste aufgenommen wird.

### Was steht in der Unterdrückungsliste? {#what-s-on-suppression-list}

E-Mail-Adressen werden wie folgt zur Unterdrückungsliste hinzugefügt:

* Alle **Hardbounces** und **Spam-Beschwerden** senden die entsprechenden E-Mail-Adressen nach einem einzigen Vorfall automatisch an die Unterdrückungsliste.

* **Softbounces** senden eine E-Mail-Adresse nicht sofort an die Unterdrückungsliste, sondern erhöhen einen Fehlerzähler. Wenn der Fehlerzähler den Schwellenwert erreicht, wird die E-Mail-Adresse der Unterdrückungsliste hinzugefügt.

   Der Schwellenwert ist auf drei Fehler festgelegt:
   * Im selben Versand wird die Adresse beim dritten Versuch unterdrückt.
   * Wenn es unterschiedliche Sendungen gibt und zwei Fehler im Abstand von mindestens 24 Stunden auftreten, wird der Fehlerzähler bei jedem Fehler erhöht und die E-Mail-Adresse wird ebenfalls beim dritten Versuch unterdrückt.

   Wenn ein Versand nach einem erneuten Versuch erfolgreich war, wird der Fehlerzähler der E-Mail-Adresse auf null zurückgesetzt.

### Weitere Zustellversuche {#retries}

Wenn eine Nachricht aufgrund eines temporären Bounces des Typs **Ignoriert** fehlschlägt, werden Wiederholungsversuche für **3,5 Tage** ab dem Zeitpunkt, an dem die Nachricht der E-Mail-Warteschlange hinzugefügt wurde, durchgeführt.

Das Mindestintervall zwischen erneuten Zustellversuchen und die maximale Anzahl weiterer Zustellversuche <!--managed by the Enhanced MTA,--> basieren sowohl auf der historischen als auch aktuellen Leistung einer IP-Adresse in einer bestimmten Domain.

Nach 3,5 Tagen wird jede Nachricht aus der Warteschlange für weitere Versuche entfernt und als Bounce zurückgesendet.
