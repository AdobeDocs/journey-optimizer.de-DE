---
title: Erstellen von IP-Pools
description: „Informationen zum Verwalten von IP-Pools“
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 100%

---


# Erstellen von IP-Pools

## Über IP-Pools

Mit Journey Optimizer können Sie IP-Pools erstellen, um die IP-Adressen Ihrer Subdomains zu Gruppen zusammenzufassen.

Zur verbesserten Zustellbarkeit von E-Mails wird dringend empfohlen, IP-Pools zu erstellen. Auf diese Weise können Sie verhindern, dass die Reputation einer Subdomain eine Auswirkung auf Ihre anderen Subdomains hat.

Eine Best Practice ist beispielsweise, einen IP-Pool für Ihre Marketing-Nachrichten und einen weiteren für Ihre Transaktionsnachrichten zu nutzen. Auf diese Weise wirkt sich eine Marketing-Nachricht, die vom Kunden abgelehnt und als Spam gekennzeichnet wird, nicht auf die an denselben Kunden gesendeten Transaktionsnachrichten aus, sodass dieser Kunde weiterhin Transaktionsnachrichten erhält (Kaufbestätigungen, Nachrichten zur Passwortwiederherstellung usw.).

## Erstellen eines IP-Pools

Gehen Sie wie folgt vor, um einen IP-Pool zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL IP-Pools]** auf und klicken Sie dann auf **[!UICONTROL IP-Pool erstellen]**.

   ![](../assets/ip-pool-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für den IP-Pool an.

   >[!NOTE]
   >
   >Der Name der Subdomain muss mit einem Buchstaben (A–Z) beginnen und nur alphanumerische Zeichen oder Sonderzeichen ( _, ., - ) enthalten.

1. Wählen Sie aus der Dropdown-Liste die IP-Adressen aus, die in den Pool aufgenommen werden sollen, und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Alle mit Ihrer Instanz bereitgestellten IP-Adressen sind in der Liste verfügbar.

Der IP-Pool wird jetzt erstellt und in der Liste angezeigt. Sie können ihn auswählen, um auf seine Eigenschaften zuzugreifen und die zugehörige Nachrichtenvorgabe anzuzeigen. Weiterführende Informationen zum Verknüpfen einer Nachrichtenvorgabe mit einem IP-Pool finden Sie in [diesem Abschnitt](message-presets.md).

![](../assets/ip-pool-created.png)

Um einen IP-Pool zu bearbeiten, öffnen Sie ihn und bearbeiten Sie dann seine Eigenschaften nach Bedarf.

>[!NOTE]
>
>Wenn eine Nachrichtenvorgabe mit dem IP-Pool verknüpft wurde, müssen Sie sie entfernen, bevor Sie den IP-Pool bearbeiten können. Nachdem die Änderungen vorgenommen wurden, können Sie die Nachrichtenvorgabe erneut verknüpfen.
