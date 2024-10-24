---
title: Anfordern einer Genehmigung
description: Erfahren Sie, wie Sie vor der Veröffentlichung Ihrer Journeys und Kampagnen eine Genehmigung anfordern können.
role: User
level: Beginner
feature: Approval
source-git-commit: 509ebc377ac8c24db464728b7544eaa96e8e5da4
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 39%

---


# Anfordern einer Genehmigung  {#request-approval}

Der Zugriff auf den Validierungs-Workflow hängt von Ihrem Anwendungsfall ab:

* **Es gibt keine aktive Genehmigungsrichtlinie**

   * **Kampagnen**: Wenn keine Genehmigungsrichtlinie für das Kampagnenobjekt in einer Sandbox aktiv ist, wird in Kampagnen die Schaltfläche **[!UICONTROL Aktivieren]** angezeigt, mit der Sie sie aktivieren können, ohne eine Genehmigung erforderlich zu sein.

   * **Journey**: Wenn keine Genehmigungsrichtlinie für das Journey-Objekt aktiv ist, zeigen Journey die Schaltfläche **[!UICONTROL Publish]** an, sodass Sie direkt veröffentlichen können.

* **Aktive Validierungsrichtlinien sind vorhanden**

   * **Kampagnen**: Wenn eine oder mehrere aktive Validierungsrichtlinien für das Campaign-Objekt in einer Sandbox vorhanden sind, wird für alle Kampagnen in dieser Sandbox die Schaltfläche **[!UICONTROL Genehmigung anfordern]** angezeigt.
Wenn beim Klicken auf die Schaltfläche **[!UICONTROL Genehmigung anfordern]** keine Genehmigungsrichtlinie für das ausgewählte Objekt gilt, wird der Arbeitsablauf für die automatische Genehmigung ausgelöst.

   * **Journey**: Wenn eine oder mehrere aktive Genehmigungsrichtlinien für das Journey-Objekt in einer Sandbox vorhanden sind, zeigen alle Journey die Schaltfläche **[!UICONTROL Genehmigung anfordern]** an.
Wenn beim Klicken auf die Schaltfläche **[!UICONTROL Genehmigung anfordern]** keine Genehmigungsrichtlinie für das ausgewählte Objekt gilt, wird der Arbeitsablauf für die automatische Genehmigung ausgelöst.

## Genehmigungsanfrage senden

Klicken Sie nach der Erstellung Ihrer Kampagne oder Journey auf die Schaltfläche **[!UICONTROL Genehmigung anfordern]** . Dadurch wird geprüft, ob in Ihrer Sandbox eine aktive Validierungsrichtlinie für die Kampagne oder Journey vorhanden ist.

* Wenn eine gültige Validierungsrichtlinie gefunden wird, wird Ihre Kampagne oder Journey zur Überprüfung gesendet.

* Wenn nach dem Klicken auf die Schaltfläche **[!UICONTROL Genehmigung anfordern]** keine Genehmigungsrichtlinie für die Kampagne oder die Journey gilt, wird die Kampagne bzw. die Journey automatisch genehmigt und entweder aktiviert oder veröffentlicht.

Der Bereich **[!UICONTROL Genehmigung anfordern]** wird geöffnet. Geben Sie ggf. eine Nachricht für die genehmigende(n) Person(en) ein und klicken Sie auf **[!UICONTROL Senden]**, um Ihre Anfrage zu übermitteln.

![](assets/approval-request.png)

Während sich die Kampagne oder Journey im Status **[!UICONTROL In Überprüfung]** befindet, haben Sie die Möglichkeit, die Genehmigungsanfrage zu stornieren. Wenn Sie auf die Schaltfläche **[!UICONTROL Anfrage abbrechen]** klicken, kehrt die Kampagne bzw. Journey zur Entwurfsstufe zurück und die Validierer werden über den Abbruch der Anforderung informiert. Sie können dann die erforderlichen Änderungen vornehmen und die Kampagne oder Journey erneut zur Genehmigung einreichen.

![](assets/approval-cancel.png)

## Genehmigungsanforderungen verwalten

Sobald die Genehmigungsanfrage an die genehmigenden Personen gesendet wurde, können diese sie überprüfen und entweder die Journey/Kampagne aktivieren, um sie live zu schalten, oder bei Bedarf Änderungen anfordern. [Erfahren Sie, wie Sie eine Anfrage überprüfen und genehmigen](review-approve-request.md)

Wenn die genehmigenden Personen Änderungen beantragen, werden Sie durch eine E-Mail und eine Journey Optimizer-Benachrichtigung benachrichtigt, die Sie durch Klicken auf das Glockensymbol oben rechts im Bildschirm auf der Registerkarte **[!UICONTROL Anfragen]** aufrufen können.

![](assets/changes-requested.png)

Öffnen Sie die Änderungsanforderung über die E-Mail oder die Benachrichtigung, um auf die Journey oder Kampagne zuzugreifen und die gewünschten Änderungen vorzunehmen. Wenn Ihre Journey/Kampagne zur erneuten Prüfung bereit ist, senden Sie eine neue Genehmigungsanfrage über die Schaltfläche **[!UICONTROL Genehmigung anfordern]**.



