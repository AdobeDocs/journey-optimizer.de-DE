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
TQID: https://experienceleague.adobe.com/cUhagNPBmqDDLIu-h9qcSSltOkbXTXx-pBh-rOskGr0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 845
ht-degree: 91%

---

# Unterdrückungsliste {#suppression-list}

Eine Unterdrückungsliste besteht aus Adressen und Domains, die von den Sendungen ausgeschlossen werden sollen, da das Senden an diese Kontakte den Ruf als Versender und die Versandraten beeinträchtigen könnte.

Die Unterdrückungsliste in [!DNL Journey Optimizer] wird auf der Ebene Ihrer eigenen Umgebung verwaltet, das heißt für eine bestimmte Sandbox.

Sie sammelt E-Mail-Adressen und Domains, die für alle Mailings in einer Einzel-Client-Umgebung unterdrückt werden, d. h. spezifisch für eine Organisations-ID, die mit einer Sandbox-ID verbunden ist.

>[!NOTE]
>
>Adobe führt eine aktualisierte Liste bekannter schlechter Adressen, die nachweislich die Interaktion und die Sender-Reputation beeinträchtigen, und stellt sicher, dass E-Mails an diese Adressen nicht zugestellt werden. Diese Liste wird in einer globalen Unterdrückungsliste verwaltet, die für alle Adobe-Kunden gleich ist. Die Adressen und Domain-Namen in der globalen Unterdrückungsliste sind verborgen. In den Versandberichten wird nur die Anzahl der ausgeschlossen Empfänger angegeben.

Darüber hinaus können Sie über das **Unterdrückungs-REST-API** von Journey Optimizer Ihre ausgehenden Nachrichten mithilfe von Unterdrückungs- und Zulassungslisten steuern. [Erfahren Sie, wie man mit der Unterdrückungs-REST-API arbeitet.](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"}

## Wozu eine Unterdrückungsliste? {#why-suppression-list}

Um die E-Mail-Nachrichten zu kontrollieren, die von den Inhabern der Posteingänge empfangen werden, und sicherzustellen, dass sie nur die von ihnen gewünschten Nachrichten erhalten, verfügen Internet-Dienstleister (ISPs) und kommerzielle Spam-Filter über eigene Algorithmen, um den allgemeinen Ruf von E-Mail-Versendern anhand der IP-Adressen und der sendenden Domain(s), die sie verwenden, zu verfolgen.

Wenn Sie deren Feedback nicht entgegennehmen (z. B. Spam-Beschwerden, Bounces usw.) berücksichtigen, werden sie Ihre Reputation herabstufen. Die Unterdrückungsliste hilft Ihnen, das Feedback der ISPs zu berücksichtigen.

Die Empfänger, deren E-Mail-Adressen unterdrückt werden, werden automatisch vom Versand der Nachricht ausgeschlossen. Dies beschleunigt den Versand, da sich die Fehlerrate maßgeblich auf die Versandgeschwindigkeit auswirkt.

## Was steht in der Unterdrückungsliste? {#what-s-on-suppression-list}

Adressen werden wie folgt zur Unterdrückungsliste hinzugefügt:

* Alle **Hardbounces** und **Spam-Beschwerden** senden die entsprechenden Adressen nach einem einzigen Vorfall automatisch an die Unterdrückungsliste. Weitere Informationen zu Spam-Beschwerden finden Sie in [diesem Abschnitt](#spam-complaints).

* **Softbounces** senden eine Adresse nicht sofort an die Unterdrückungsliste, sondern bewirken, dass der Fehlerzähler erhöht wird. Anschließend werden [weitere Zustellversuche](../configuration/retries.md) unternommen. Wenn der Fehlerzähler den Schwellenwert erreicht, wird die Adresse der Unterdrückungsliste hinzugefügt.

* Sie können auch [**manuell** eine Adresse oder eine Domain](../configuration/manage-suppression-list.md#add-addresses-and-domains) zur Unterdrückungsliste hinzufügen.

Weitere Informationen zu Hardbounces und Softbounces finden Sie in [diesem Abschnitt](#delivery-failures).

>[!NOTE]
>
>Die Adressen von abgemeldeten Benutzern können nicht an die Unterdrückungsliste gesendet werden, da sie keine E-Mails von [!DNL Journey Optimizer] erhalten. Ihre Entscheidung wird auf der Ebene von Experience Platform gehandhabt. Erfahren Sie mehr über [Opt-outs](../privacy/opt-out.md).

Für jede Adresse den grundlegenden Grund für die Unterdrückung und die Unterdrückungskategorie (weich, hart, usw.) werden in der Unterdrückungsliste angezeigt. Weitere Informationen zum Zugriff auf die und zur Verwaltung der Unterdrückungsliste finden Sie in [diesem Abschnitt](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Die Profile mit dem Status **[!UICONTROL Unterdrückt]** werden während des Nachrichtenversands ausgeschlossen. Daher zeigen die **Journey-Berichte** zwar an, dass sich diese Profile durch die Journey bewegt haben (Aktivitäten [Zielgruppe lesen](../building-journeys/read-audience.md) und [Nachrichten](../building-journeys/journey-action.md)), sie sind aber nicht in der Metrik **[!UICONTROL Gesendet]** der **E-Mail-Berichte** enthalten, da sie vor dem E-Mail-Versand herausgefiltert werden.
>
>Erfahren Sie mehr über den [Live-Bericht](../reports/live-report.md) und den [Customer Journey Analytics-Bericht](../reports/report-gs-cja.md). Um den Grund für alle Ausschlussfälle zu ermitteln, können Sie den [Adobe Experience Platform Query Service} ](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=de){target="_blank"}.

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

Einige ISPs bieten eine Feedback-Schleife (Feedback Loop, FBL), mit der die Absenderin bzw. der Absender einer E-Mail automatisch benachrichtigt werden kann, wenn Benutzende, die eine E-Mail erhalten, diese als Spam kennzeichnen. [Weitere Informationen](deliverability.md#feedback-loops)
