---
title: E-Mail-Spam-Bericht verwenden
description: Erfahren Sie, wie Sie den E-Mail-Spam-Bericht verwenden.
feature: Preview
role: User
level: Beginner
badge: label="Beta"
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 5f69b252f5812f43b3d0a6fed0aac074ece0d10f
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 17%

---

# E-Mail-Spam-Bericht {#spam-report}

>[!CONTEXTUALHELP]
>id="ajo_simulate_spam_report"
>title="E-Mail-Spam-Bericht"
>abstract="Mit dem Spam-Bericht können Sie die Spam-Bewertung Ihres E-Mail-Inhalts überprüfen. Dieser Wert gibt an, ob ISPs oder Postfachanbieter Ihre Nachricht als Spam betrachten oder nicht. Je niedriger die Punktzahl, desto besser. Wenn Ihr E-Mail-Inhaltswert über 2 liegt, sollten Sie in Erwägung ziehen, Probleme zu beheben, die dazu führen, dass Tests fehlschlagen."

Sie können die Spam-Bewertung Ihres E-Mail-Inhalts in einem speziellen Spam-Bericht überprüfen. Verwenden [SpamAssassin](https://spamassassin.apache.org/){target="_blank"}, kann Adobe Journey Optimizer Ihren E-Mail-Inhalt testen und eine Punktzahl angeben, um anzugeben, ob ISPs oder Postfachanbieter ihn als Spam betrachten oder nicht.

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der Betaversion und steht nur Beta-Kunden zur Verfügung. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Bei der Bearbeitung oder Vorschau Ihres E-Mail-Inhalts wird die **[!UICONTROL Spam-Bericht]** -Schaltfläche bietet Scoring und Ratschläge zur Verbesserung der Punktzahl für jedes aufgelistete Element.

Mit dieser Funktion können Sie feststellen, ob eine Nachricht von den Anti-Spam-Tools, die bei Erhalt verwendet werden, als Spam eingestuft werden kann, und gegebenenfalls Maßnahmen ergreifen. Viele E-Mail-Posteingangsanbieter verwenden Tools als Teil ihres Spam-Filtervorgangs. Der Versand von E-Mails mit einer schlechten Punktzahl kann die Zustellbarkeit erheblich beeinträchtigen.

So greifen Sie auf die **[!UICONTROL Spam-Bericht]** führen Sie die folgenden Schritte aus.

1. Klicken Sie auf dem Bildschirm **[!UICONTROL Simulieren]** auf die Schaltfläche **[!UICONTROL Spam-Bericht]**.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Eine Anti-Spam-Prüfung wird automatisch durchgeführt und der **[!UICONTROL Spam-Bericht]** zeigt die Ergebnisse an. Er zeigt die Leistung Ihres Inhalts in Bezug auf das Text-Layout, die Struktur, die Bildgröße, ggf. Wörter, die Spam triggern usw.

   ![](assets/spam-report-high-score.png)

1. Überprüfen Sie die Bewertungen und Beschreibungen für jedes Element.

   Je niedriger die Punktzahl, desto besser. Wenn der Wert größer als 5 ist, wird ein Warnhinweis angezeigt, der anzeigt, dass manche Nachrichten beim Empfang blockiert oder als Spam gekennzeichnet werden können. Es empfiehlt sich, einen Wert unter 2 zu erzielen.

1. Wenn Sie auf der Grundlage dieser Auswertung der Ansicht sind, dass einige Elemente verbessert werden können, bearbeiten Sie Ihren Inhalt im [Email Designer](../email/content-from-scratch.md) und nehmen die notwendigen Aktualisierungen vor.

1. Nachdem Sie Ihre Änderungen vorgenommen haben, wechseln Sie zurück zum **[!UICONTROL Spam-Bericht]** angezeigt, um sicherzustellen, dass Ihr Ergebnis verbessert wurde.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
