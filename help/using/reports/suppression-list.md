---
solution: Journey Optimizer
product: journey optimizer
title: Unterdrückungsliste
description: 'Erfahren Sie, wie Sie die Unterdrückungsliste wie folgt verwenden:'
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Unterdrückungsliste {#suppression-list}

Eine Unterdrückungsliste besteht aus Adressen und Domänen, die Sie aus Ihren Sendungen ausschließen möchten, da der Versand an diese Kontakte Ihrer Reputation und den Versandraten schaden könnte.

Die [!DNL Journey Optimizer] Die Unterdrückungsliste wird auf Ihrer eigenen Umgebungsebene verwaltet, d. h. für eine bestimmte Sandbox.

Sie erfasst E-Mail-Adressen und Domänen, die in allen Mailings in einer einzigen Client-Umgebung unterdrückt werden, d. h. eine Organisations-ID, die mit einer Sandbox-ID verknüpft ist.

>[!NOTE]
>
>Adobe führt eine aktualisierte Liste bekannter schlechter Adressen, die nachweislich die Interaktion und Reputation des Mailings beeinträchtigen, und stellt sicher, dass ihnen keine E-Mails zugestellt werden. Diese Liste wird in einer globalen Unterdrückungsliste verwaltet, die für alle Adobe-Kunden gleich ist. Die in der globalen Unterdrückungsliste enthaltenen Adressen und Domänennamen werden ausgeblendet. In den Versandberichten wird nur die Anzahl der ausgeschlossenen Empfänger angegeben.

## Warum eine Unterdrückungsliste? {#why-suppression-list}

Um die E-Mail-Nachrichten, die von den Inbox-Inhabern empfangen werden, zu steuern und sicherzustellen, dass sie nur die von ihnen gewünschten erhalten, verfügen Internet Service Provider (ISPs) und kommerzielle Spam-Filter über eigene Algorithmen, um die allgemeine Reputation von E-Mail-Absendern basierend auf den von ihnen verwendeten IP-Adressen und Versanddomänen zu verfolgen.

Wenn Sie kein Feedback abgeben (z. B. Beschwerden wegen Spam, Bounces usw.) berücksichtigen, werden sie Ihre Reputation unterschätzen. Die Unterdrückungsliste hilft Ihnen dabei, das Feedback der ISPs zu berücksichtigen.

Empfänger, deren E-Mail-Adressen unterdrückt werden, werden automatisch vom Nachrichtenversand ausgeschlossen. Dies beschleunigt den Versand, da sich die Fehlerrate maßgeblich auf die Versandgeschwindigkeit auswirkt.

## Was steht auf der Unterdrückungsliste? {#what-s-on-suppression-list}

Adressen werden der Unterdrückungsliste wie folgt hinzugefügt:

* Alle **Hardbounces** und **Spam-Beschwerden** automatisch die entsprechenden Adressen an die Unterdrückungsliste senden, nachdem sie nur einmal aufgetreten sind.

* **Softbounces** senden Sie nicht sofort eine Adresse an die Unterdrückungsliste, sondern erhöhen einen Fehlerzähler. Mehrere [retries](../configuration/retries.md) ausgeführt werden und wenn der Fehlerzähler den Schwellenwert erreicht, wird die Adresse der Unterdrückungsliste hinzugefügt.

* Sie können auch [**manuell** Adresse oder Domain hinzufügen](../configuration/manage-suppression-list.md#add-addresses-and-domains) in die Unterdrückungsliste ein.

Weitere Informationen zu Hardbounces und Softbounces finden Sie unter [diesem Abschnitt](#delivery-failures).

>[!NOTE]
>
>Die Adressen abgemeldeter Benutzer können nicht an die Unterdrückungsliste gesendet werden, da sie keine E-Mails von erhalten [!DNL Journey Optimizer]. Ihre Auswahl erfolgt auf Experience Platform-Ebene. Weitere Informationen finden Sie unter [Opt-out](../privacy/opt-out.md).

Für jede Adresse den Grund für die Unterdrückung und die Unterdrückungskategorie (weich, hart usw.) werden in der Unterdrückungsliste angezeigt. Erfahren Sie mehr über den Zugriff auf und die Verwaltung der Unterdrückungsliste in [diesem Abschnitt](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Die Profile mit **[!UICONTROL Suppressed]** -Status während des Nachrichtenversands ausgeschlossen werden. Daher muss während der **Journey-Berichte** zeigt an, dass sich diese Profile durch die Journey bewegt haben ([Segment lesen](../building-journeys/read-segment.md) und [Nachrichtenaktivitäten](../building-journeys/journeys-message.md)), die **E-Mail-Berichte** werden sie nicht in die **[!UICONTROL Sent]** Metriken, da sie vor dem E-Mail-Versand herausgefiltert werden.
>
>Weitere Informationen finden Sie unter [Live-Bericht](../reports/live-report.md) und [Globaler Bericht](../reports/global-report.md). Um den Grund für alle Ausschlussfälle zu ermitteln, können Sie die [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.

### Versandfehler {#delivery-failures}

Wenn ein Versand fehlschlägt, gibt es zwei Typen von Fehlern:

* **Hardbounce**. Ein Hardbounce zeigt eine ungültige E-Mail-Adresse an (d. h. eine nicht vorhandene E-Mail-Adresse). Dies umfasst eine Bounce-Nachricht vom E-Mail-Empfangs-Server, die explizit angibt, dass die Adresse ungültig ist.
* **Softbounce**. Dies ist ein temporärer E-Mail-Bounce, der für eine gültige E-Mail-Adresse aufgetreten ist.

A **Hardbounce** fügt die E-Mail-Adresse automatisch zur Unterdrückungsliste hinzu.

A **Softbounce** <!--or an **ignored** error--> , das zu oft auftritt, sendet auch die E-Mail-Adresse nach mehreren weiteren Versuchen an die Unterdrückungsliste. [Weitere Informationen zu Wiederholungen](../configuration/retries.md)

Wenn Sie weiterhin an diese Adressen senden, kann dies Auswirkungen auf Ihre Zustellraten haben, da ISPs darauf hingewiesen wird, dass Sie möglicherweise die Best Practices zur Wartung der E-Mail-Adressen nicht befolgen und daher möglicherweise kein vertrauenswürdiger Absender sind.

### Beschwerden wegen Spam {#spam-complaints}

Die Unterdrückungsliste erfasst E-Mail-Adressen, die Ihre Nachricht als Spam markieren. Wenn beispielsweise jemand an einen Kundendienst schreibt, der anfordert, nie wieder E-Mails von Ihnen zu erhalten, wird die E-Mail-Adresse dieser Person in Ihrer Instanz unterdrückt und Sie können an diese Adresse nicht mehr senden.

Der Versand an Empfänger, nachdem diese eine Spam-Beschwerde eingereicht haben, kann sich sehr auf Ihre Reputation des Versands auswirken, da ISPs davon in Kenntnis gesetzt werden, dass Sie unerwünschte E-Mails senden und möglicherweise nicht auf Ihre Empfänger hören.

Dies kann dazu führen, dass Ihre IP-Adresse oder Versanddomäne blockiert wird, was verhindert werden kann, dass diese Adressen auf der Unterdrückungsliste stehen.
