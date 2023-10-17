---
solution: Journey Optimizer
product: journey optimizer
title: Unterdrückungsliste
description: Erfahren Sie, wie Sie die Unterdrückungsliste verwenden
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 100%

---

# Unterdrückungsliste {#suppression-list}

Eine Unterdrückungsliste besteht aus Adressen und Domains, die von den Sendungen ausgeschlossen werden sollen, da das Senden an diese Kontakte den Ruf als Versender und die Versandraten beeinträchtigen könnte.

Die Unterdrückungsliste in [!DNL Journey Optimizer] wird auf der Ebene Ihrer eigenen Umgebung verwaltet, das heißt für eine bestimmte Sandbox.

Sie sammelt E-Mail-Adressen und Domains, die für alle Mailings in einer Einzel-Client-Umgebung unterdrückt werden, d. h. spezifisch für eine Organisations-ID, die mit einer Sandbox-ID verbunden ist.

>[!NOTE]
>
>Adobe führt eine aktualisierte Liste bekannter schlechter Adressen, die nachweislich die Interaktion und die Sender-Reputation beeinträchtigen, und stellt sicher, dass E-Mails an diese Adressen nicht zugestellt werden. Diese Liste wird in einer globalen Unterdrückungsliste verwaltet, die für alle Adobe-Kunden gleich ist. Die Adressen und Domain-Namen in der globalen Unterdrückungsliste sind verborgen. In den Versandberichten wird nur die Anzahl der ausgeschlossen Empfänger angegeben.

## Wozu eine Unterdrückungsliste? {#why-suppression-list}

Um die E-Mail-Nachrichten zu kontrollieren, die von den Inhabern der Posteingänge empfangen werden, und sicherzustellen, dass sie nur die von ihnen gewünschten Nachrichten erhalten, verfügen Internet-Dienstleister (ISPs) und kommerzielle Spam-Filter über eigene Algorithmen, um den allgemeinen Ruf von E-Mail-Versendern anhand der IP-Adressen und der sendenden Domain(s), die sie verwenden, zu verfolgen.

Wenn Sie deren Feedback (z. B. Spam-Beschwerden, Bounces usw.) nicht berücksichtigen, werden sie Ihre Reputation herabstufen. Die Unterdrückungsliste hilft Ihnen, das Feedback der ISPs zu berücksichtigen.

Die Empfänger, deren E-Mail-Adressen unterdrückt werden, werden automatisch vom Versand der Nachricht ausgeschlossen. Dies beschleunigt den Versand, da sich die Fehlerrate maßgeblich auf die Versandgeschwindigkeit auswirkt.

## Was steht in der Unterdrückungsliste? {#what-s-on-suppression-list}

Adressen werden wie folgt zur Unterdrückungsliste hinzugefügt:

* Alle **Hardbounces** und **Spam-Beschwerden** senden die entsprechenden Adressen nach einem einzigen Vorfall automatisch an die Unterdrückungsliste.

* **Softbounces** senden eine Adresse nicht sofort an die Unterdrückungsliste, sondern bewirken, dass der Fehlerzähler erhöht wird. Anschließend werden [weitere Zustellversuche](../configuration/retries.md) unternommen. Wenn der Fehlerzähler den Schwellenwert erreicht, wird die Adresse der Unterdrückungsliste hinzugefügt.

* Sie können auch [**manuell** eine Adresse oder eine Domain](../configuration/manage-suppression-list.md#add-addresses-and-domains) zur Unterdrückungsliste hinzufügen.

Weitere Informationen zu Hardbounces und Softbounces finden Sie in [diesem Abschnitt](#delivery-failures).

>[!NOTE]
>
>Die Adressen von abgemeldeten Benutzern können nicht an die Unterdrückungsliste gesendet werden, da sie keine E-Mails von [!DNL Journey Optimizer] erhalten. Ihre Entscheidung wird auf der Ebene von Experience Platform gehandhabt. Weitere Informationen zum [Opt-out](../privacy/opt-out.md)

Für jede Adresse werden der wesentliche Grund für die Unterdrückung und die Unterdrückungskategorie (weich, hart, usw.) in der Unterdrückungsliste angezeigt. Weitere Informationen zum Zugriff auf und zur Verwaltung der Unterdrückungsliste finden Sie in [diesem Abschnitt](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Die Profile mit dem Status **[!UICONTROL Unterdrückt]** werden während des Nachrichtenversands ausgeschlossen. Daher zeigen die **Journey-Berichte** zwar an, dass sich diese Profile durch die Journey bewegt haben (Aktivitäten [Zielgruppe lesen](../building-journeys/read-audience.md) und [Nachrichten](../building-journeys/journeys-message.md)), sie sind aber nicht in der Metrik **[!UICONTROL Gesendet]** der **E-Mail-Berichte** enthalten, da sie vor dem E-Mail-Versand herausgefiltert werden.
>
>Erfahren Sie mehr über den [Live-Bericht](../reports/live-report.md) und den [globalen Bericht](../reports/global-report.md). Um den Grund für alle Ausschlussfälle zu ermitteln, können Sie den [Abfrage-Service von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=de){target="_blank"} verwenden.

### Versandfehler {#delivery-failures}

Bei Fehlschlägen des Versands gibt es drei Typen von Fehlern:

* **Hardbounce**. Ein Hardbounce weist auf eine ungültige E-Mail-Adresse hin (d. h. eine E-Mail-Adresse, die nicht existiert). Dies beinhaltet eine Bounce-Nachricht des empfangenden E-Mail-Servers, in der explizit angegeben wird, dass die Adresse ungültig ist.
* **Softbounce**. Dies ist ein temporärer E-Mail-Bounce, der bei einer gültige E-Mail-Adresse aufgetreten ist.

Ein **Hardbounce** fügt die E-Mail-Adresse automatisch zur Unterdrückungsliste hinzu.

Ein **Softbounce** <!--or an **ignored** error-->, der zu oft auftritt, sendet die E-Mail-Adresse nach mehreren Zustellversuchen ebenfalls an die Unterdrückungsliste. [Erfahren Sie mehr über weitere Zustellversuche](../configuration/retries.md)

Wenn Sie weiterhin an diese Adressen senden, kann sich dies auf Ihre Versandraten auswirken, da es den ISPs mitteilt, dass Sie möglicherweise die Best Practices zur Wartung von E-Mail-Adressen nicht befolgen und daher möglicherweise kein vertrauenswürdiger Versender sind.

### Spam-Beschwerden {#spam-complaints}

Die Unterdrückungsliste erfasst E-Mail-Adressen, die Ihre Nachricht als Spam kennzeichnen. Wenn zum Beispiel jemand an den Kundendienst schreibt und darum bittet, nie wieder E-Mails von Ihnen zu erhalten, wird die E-Mail-Adresse dieser Person in Ihrer Instanz unterdrückt und Sie können nicht mehr an diese Adresse versenden.

Das Senden an Empfänger, nachdem sie eine Spam-Beschwerde eingereicht haben, kann sich sehr auf Ihren Ruf auswirken, da es den ISPs mitteilt, dass Sie unerwünschte E-Mails senden und möglicherweise nicht auf Ihre Empfänger hören.

Dies könnte dazu führen, dass Ihre IP-Adresse oder die sendende Domain blockiert wird. Das kann vermieden werden, wenn diese Adressen auf der Unterdrückungsliste vorhanden sind.
