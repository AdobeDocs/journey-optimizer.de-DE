---
title: Verwenden eines Spam-Berichts
description: Erfahren Sie, wie Sie den Spam-Bericht verwenden
feature: Preview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: feae2cb9d0bed35f12eb117cf2969c9290ebc06f
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 100%

---

# Verwenden eines Spam-Berichts {#spam-report}

>[!AVAILABILITY]
>
>Die Spam-Bericht-Funktion ist derzeit nur als Betaversion für ausgewählte Benutzende verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Mit [!DNL Journey Optimizer] können Sie die Leistung Ihres Inhalts gegen Spam-Filterung überprüfen und sicherstellen, dass Ihre Nachrichten in den Postfächern Ihrer Kundschaft landen und nicht im Spam.

>[!CAUTION]
>
>* Diese Funktion ist derzeit nur für den E-Mail-Kanal verfügbar.
>
>* Derzeit kann die Spam-Berichtsanalyse nur für englischsprachige Inhalte durchgeführt werden.

Wenn Sie Inhalte bearbeiten oder in der Vorschau anzeigen, bietet die Option **[!UICONTROL Spam-Bericht]** eine Bewertung und Ratschläge zur Verbesserung der Bewertungen für jedes aufgelistete Element.

Auf diese Weise können Sie feststellen, ob eine Nachricht von den Anti-Spam-Tools, die bei Erhalt verwendet werden, als Spam eingestuft wird, und Maßnahmen ergreifen, falls dies nicht der Fall ist.

>[!CAUTION]
>
>Der Spam-Bericht enthält nur Hinweise und Warnungen. Beachten Sie, dass Sie nicht daran gehindert werden, Nachrichten zu senden, wenn der Spam-Bericht anzeigt, dass Ihr Inhalt als Spam gilt. Es ist Ihre Entscheidung, ob Sie die Bewertung und die Verbesserungsvorschläge befolgen.

Zur Verwendung der Funktion für **[!UICONTROL Spam-Berichte]** gehen Sie wie folgt vor.

<!--For example spam scoring tool can tell that there are too many Images compared to the text. Retailers tend to do this even though the spam score gets worse because the content is more engaging.-->

<!--Michael, who is a marketer with NIKE works along with Tara from testing team to ensure that the emails being sent as part of the campaign/journey don't get categorised as SPAM.

They need an integration within AJO's marketing system to show how the curated content is doing against different SPAM compliance pillars like for SPAM trigger words, HTML Body content and layout, subject line etc.

They should be able to get scores for each individual items as shown by market standard SPAM filtering tools like Spam Assassin, Symantec etc.

They should also get suggestions on how to improve the score better to be confident that the messages don't get categorised as spam.-->

1. Klicken Sie auf dem Bildschirm **[!UICONTROL Simulieren]** auf die Schaltfläche **[!UICONTROL Spam-Bericht]**.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Eine Anti-Spam-Prüfung wird automatisch durchgeführt und der **[!UICONTROL Spam-Bericht]** zeigt die Ergebnisse an. Er zeigt die Leistung Ihres Inhalts in Bezug auf das Text-Layout, die Struktur, die Bildgröße, ggf. Wörter, die Spam triggern usw.

   ![](assets/spam-report-high-score.png)

1. Überprüfen Sie die Bewertungen und Beschreibungen für jedes Element.

   Wenn der Wert größer als 5 ist, wird eine Warnung angezeigt. Sie weist darauf hin, dass beim Empfang manche Nachrichten von Anti-Spam-Tools blockiert oder als Spam gekennzeichnet werden können.

1. Basierend auf dieser Bewertung können Sie, wenn Sie der Ansicht sind, dass einige Elemente verbessert werden können, in Ihren Inhalten mithilfe von [E-Mail-Designer](../email/content-from-scratch.md) die erforderlichen Aktualisierungen vornehmen.

1. Sobald Sie Ihre Änderungen vorgenommen haben, kehren Sie zum Bildschirm **[!UICONTROL Spam-Bericht]** zurück, um sicherzustellen, dass sich Ihre Bewertung verbessert hat.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
