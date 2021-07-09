---
title: Unterdrückungsliste
description: Erfahren Sie, was die Unterdrückungsliste ist, welchen Zweck sie hat und was darin enthalten ist.
feature: Zustellbarkeit
topic: Content-Management
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: ht
source-wordcount: '643'
ht-degree: 100%

---

# Unterdrückungsliste {#suppression-list}

Eine Unterdrückungsliste besteht aus E-Mail-Adressen, die Sie von Ihren Sendungen ausschließen möchten, da das Senden an diese Kontakte Ihren Ruf als Versender und Ihre Versandraten beeinträchtigen könnte.

Die Unterdrückungsliste in [!DNL Journey Optimizer] wird auf der Ebene Ihrer eigenen Umgebung verwaltet.

Sie sammelt E-Mail-Adressen und Domains, die für alle Mailings in einer Einzel-Client-Umgebung unterdrückt werden, d. h. spezifisch für eine IMS-Organisations-ID, die mit einer Sandbox-ID verbunden ist.

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## Wozu eine Unterdrückungsliste? {#why-suppression-list}

Um die E-Mail-Nachrichten zu kontrollieren, die von den Inhabern der Posteingänge empfangen werden, und sicherzustellen, dass sie nur die von ihnen gewünschten Nachrichten erhalten, verfügen Internet-Dienstleister (ISPs) und kommerzielle Spam-Filter über eigene Algorithmen, um den allgemeinen Ruf von E-Mail-Versendern anhand der IP-Adressen und der sendenden Domain(s), die sie verwenden, zu verfolgen.

Wenn Sie deren Feedback (z. B. Spam-Beschwerden, Bounces usw.) nicht berücksichtigen, werden sie Ihre Reputation herabstufen. Die Unterdrückungsliste hilft Ihnen, das Feedback der ISPs zu berücksichtigen.

Die Empfänger, deren E-Mail-Adressen unterdrückt werden, werden automatisch vom Versand der Nachricht ausgeschlossen. Dies beschleunigt den Versand, da sich die Fehlerrate maßgeblich auf die Versandgeschwindigkeit auswirkt.

## Was steht in der Unterdrückungsliste? {#what-s-on-suppression-list}

E-Mail-Adressen werden wie folgt zur Unterdrückungsliste hinzugefügt:

* Alle **Hardbounces** und **Spam-Beschwerden** senden die entsprechenden E-Mail-Adressen nach einem einzigen Vorfall automatisch an die Unterdrückungsliste.

* **Softbounces** und vorübergehende, **ignorierte** Fehler senden eine E-Mail-Adresse nicht sofort an die Unterdrückungsliste, sondern erhöhen einen Fehlerzähler. Anschließend werden mehrere weitere Zustellversuche unternommen. Wenn der Fehlerzähler den Schwellenwert erreicht, wird die Adresse der Unterdrückungsliste hinzugefügt. Erfahren Sie mehr über [weitere Zustellversuche](configuration/retries.md).

<!--You can also manually add an address to the suppression list. Manual category will be available when ability to manually add an address to the suppression list (via API) is released.-->

>[!NOTE]
>
>Die Adressen von abgemeldeten Benutzern können nicht an die Unterdrückungsliste gesendet werden, da sie keine E-Mails von [!DNL Journey Optimizer] erhalten. Ihre Entscheidung wird auf der Ebene von Experience Platform gehandhabt. Weitere Informationen zum [Opt-out](../using/consent.md)
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Für jede Adresse werden der wesentliche Grund für die Unterdrückung und die Unterdrückungskategorie (weich, hart, usw.) in der Unterdrückungsliste angezeigt. Weitere Informationen zum Zugriff auf und zur Verwaltung der Unterdrückungsliste finden Sie in [diesem Abschnitt](configuration/manage-suppression-list.md).

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

### Versandfehler {#delivery-failures}

Bei Fehlschlägen des Versands gibt es drei Typen von Fehlern:

* **Hardbounce**. Ein Hardbounce weist auf eine ungültige E-Mail-Adresse hin (d. h. eine E-Mail-Adresse, die nicht existiert). Dies umfasst eine Bounce-Nachricht des empfangenden E-Mail-Servers, in der explizit angegeben wird, dass die Adresse ungültig ist, z. B. „Nutzer unbekannt“.
* **Softbounce**. Dies ist ein temporärer E-Mail-Bounce, der bei einer gültige E-Mail-Adresse aufgetreten ist.
* **Ignoriert**. Dies ist ein E-Mail-Bounce, der bei einer gültigen E-Mail-Adresse aufgetreten ist, aber bekanntermaßen vorübergehend ist, z. B. ein fehlgeschlagener Verbindungsversuch, ein vorübergehendes Spam-Problem (E-Mail-Reputation) oder ein vorübergehendes technisches Problem.<!--does it exist in CJM?-->

Ein **Hardbounce** fügt die E-Mail-Adresse automatisch zur Unterdrückungsliste hinzu.

Ein **Softbounce** oder ein **ignorierter** Fehler, der zu oft auftritt, sendet die E-Mail-Adresse nach mehreren weiteren Zustellversuchen ebenfalls an die Unterdrückungsliste. [Erfahren Sie mehr über weitere Zustellversuche](configuration/retries.md)

Wenn Sie weiterhin an diese Adressen senden, kann sich dies auf Ihre Versandraten auswirken, da es den ISPs mitteilt, dass Sie möglicherweise die Best Practices zur Wartung von E-Mail-Adressen nicht befolgen und daher möglicherweise kein vertrauenswürdiger Versender sind.

### Spam-Beschwerden {#spam-complaints}

Die Unterdrückungsliste erfasst E-Mail-Adressen, die Ihre Nachricht als Spam kennzeichnen. Wenn zum Beispiel jemand an den Kundendienst schreibt und darum bittet, nie wieder E-Mails von Ihnen zu erhalten, wird die E-Mail-Adresse dieser Person in Ihrer Instanz unterdrückt und Sie können nicht mehr an diese Adresse versenden.

Das Senden an Empfänger, nachdem sie eine Spam-Beschwerde eingereicht haben, kann sich sehr auf Ihren Ruf auswirken, da es den ISPs mitteilt, dass Sie unerwünschte E-Mails senden und möglicherweise nicht auf Ihre Empfänger hören.

Dies könnte dazu führen, dass Ihre IP-Adresse oder die sendende Domain blockiert wird. Das kann vermieden werden, wenn diese Adressen auf der Unterdrückungsliste vorhanden sind.

<!--### Unsubscriptions {#unsubscriptions}

Every email sent to recipients must include an unsubscribe link. Upon clicking this link, if a recipient confirms [opting out](consent.md), the corresponding email address is immediately sent to the suppression list. This user must not receive communication from your brand until subscribed again.
NOT TRUE > "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

<!--MOVED to Configuration/Retries section

The threshold is set at three errors:
* For the same delivery, at the third attempt, the address is suppressed.
* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.
When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are ///managed by the Enhanced MTA/// based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->
