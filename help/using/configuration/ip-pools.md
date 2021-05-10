---
title: Erstellen von IP-Pools
description: Erfahren Sie, wie xxxx funktioniert
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
translation-type: tm+mt
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Erstellen von IP-Pools

## Info zu IP-Pools

Mit Journey Optimizer können Sie IP-Pools erstellen, um die IP-Adressen Ihrer Subdomänen zu gruppieren.

Die Erstellung von IP-Pools wird dringend empfohlen, um eine E-Mail-Zustellung zu ermöglichen. Auf diese Weise können Sie verhindern, dass der Ruf einer Subdomäne Ihre anderen Subdomänen beeinflusst.

Eine der Best Practices besteht beispielsweise darin, einen IP-Pool für Ihre Marketing-Nachrichten und einen weiteren für Ihre Transaktionsnachrichten zu haben. Wenn eine Ihrer Marketing-Nachrichten schlecht läuft und von einem Kunden als Spam deklariert wird, hat dies keine Auswirkungen auf die Transaktionsnachrichten, die an denselben Kunden gesendet werden, der weiterhin Transaktionsnachrichten erhalten wird (Kaufbestätigungen, Passwortwiederherstellungsmeldungen usw.).

## Erstellen eines IP-Pools

Gehen Sie wie folgt vor, um einen IP-Pool zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanal]** / **[!UICONTROL IP-Pools]** auf und klicken Sie dann auf **[!UICONTROL IP-Pool erstellen]**.

   ![](../assets/ip-pool-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für den IP-Pool ein.

1. Wählen Sie in der Dropdown-Liste die IP-Adressen aus, die in den Pool aufgenommen werden sollen, und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Alle mit Ihrer Instanz bereitgestellten IP-Adressen sind in der Liste verfügbar.

Der IP-Pool wird jetzt erstellt und in der Liste angezeigt. Sie können sie auswählen, um auf ihre Eigenschaften zuzugreifen und die zugehörigen Nachrichtenvorgaben anzuzeigen (siehe [Eine Nachrichtenvorgabe erstellen](message-presets.md)).

![](../assets/ip-pool-created.png)

Um einen IP-Pool zu bearbeiten, öffnen Sie ihn und bearbeiten Sie dann seine Eigenschaften nach Bedarf.

>[!NOTE]
>
>Wenn eine Nachrichtenvorgabe mit dem IP-Pool verknüpft wurde, müssen Sie sie zunächst entfernen, bevor Sie den IP-Pool bearbeiten. Nachdem die Änderungen vorgenommen wurden, können Sie die Nachrichtenvorgabe erneut verknüpfen.
