---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von IP-Pools
description: Erfahren Sie, wie Sie IP-Pools verwalten
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---

# Erstellen von IP-Pools {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="Einrichten eines IP-Pools"
>abstract="IP-Pools sammeln die IP-Adressen Ihrer Subdomains, um die E-Mail-Zustellbarkeit zu verbessern."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="Einrichten eines IP-Pools"
>abstract="Mit Journey Optimizer können Sie IP-Pools erstellen, um die IP-Adressen Ihrer Subdomains zu gruppieren. Dies kann die Zustellbarkeit Ihrer E-Mail erheblich verbessern, da Sie dadurch verhindern können, dass sich die Reputation einer Subdomain auf Ihre anderen Subdomains auswirkt."

## Über IP-Pools {#about-ip-pools}

Mit [!DNL Journey Optimizer]können Sie IP-Pools erstellen, um die IP-Adressen Ihrer Subdomains zu gruppieren.

Für die Zustellbarkeit von E-Mails wird dringend empfohlen, IP-Pools zu erstellen. Auf diese Weise können Sie verhindern, dass die Reputation einer Subdomain Ihre anderen Subdomains beeinflusst.

Eine Best Practice ist beispielsweise, einen IP-Pool für Ihre Marketing-Nachrichten und einen weiteren für Ihre Transaktionsnachrichten zu nutzen. Auf diese Weise wirkt sich eine Ihrer Marketing-Nachrichten, die von einem Kunden als unzureichend und als Spam gekennzeichnet wird, nicht auf die an denselben Kunden gesendeten Transaktionsnachrichten aus, der weiterhin Transaktionsnachrichten erhält (Kaufbestätigungen, Nachrichten zur Passwortwiederherstellung usw.).

>[!CAUTION]
>
>Die Konfiguration des IP-Pools ist in allen Umgebungen üblich. Daher wirkt sich die Erstellung oder Bearbeitung von IP-Pools auch auf die Produktions-Sandboxes aus.

## Erstellen eines IP-Pools {#create-ip-pool}

Gehen Sie wie folgt vor, um einen IP-Pool zu erstellen:

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP pools]** Menü und klicken Sie auf **[!UICONTROL Create IP Pool]**.

   ![](assets/ip-pool-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für den IP-Pool an.

   >[!NOTE]
   >
   >Der Name muss mit einem Buchstaben (A-Z) beginnen und nur alphanumerische Zeichen oder Sonderzeichen ( _, ., - ) enthalten.

1. Wählen Sie aus der Dropdownliste die IP-Adressen aus, die in den Pool aufgenommen werden sollen, und klicken Sie dann auf **[!UICONTROL Submit]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Alle mit Ihrer Instanz bereitgestellten IP-Adressen sind in der Liste verfügbar.

Der IP-Pool wird jetzt erstellt und in der Liste angezeigt. Sie können es auswählen, um auf seine Eigenschaften zuzugreifen und die zugehörige Kanaloberfläche anzuzeigen (d. h. die Nachrichtenvorgabe). Weitere Informationen zum Verknüpfen einer Kanaloberfläche mit einem IP-Pool finden Sie unter [diesem Abschnitt](channel-surfaces.md).

![](assets/ip-pool-created.png)

## Bearbeiten eines IP-Pools {#edit-ip-pool}

Gehen Sie wie folgt vor, um einen IP-Pool zu bearbeiten.

1. Klicken Sie in der Liste auf den Namen des IP-Pools, um ihn zu öffnen.

   ![](assets/ip-pool-list.png)

1. Bearbeiten Sie die Eigenschaften nach Bedarf. Sie können die Beschreibung ändern und IP-Adressen hinzufügen oder entfernen.

   >[!NOTE]
   >
   >Der Name des IP-Pools kann nicht bearbeitet werden. Wenn Sie ihn ändern möchten, müssen Sie den IP-Pool löschen und einen weiteren mit dem Namen Ihrer Wahl erstellen.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Gehen Sie beim Löschen einer IP-Adresse mit besonderer Sorgfalt vor, da dies die anderen IPs zusätzlich belasten und möglicherweise erhebliche Auswirkungen auf Ihre Zustellbarkeit hat. Im Zweifelsfall kontaktieren Sie einen Zustellbarkeitsexperten.

1. Speichern Sie Ihre Änderungen.

Die Aktualisierung ist sofort oder asynchron wirksam, je nachdem, welcher IP-Pool mit einer [Kanaloberfläche](channel-surfaces.md) oder nicht:

* Wenn der IP-Pool **not** in Verbindung mit einer beliebigen Kanaloberfläche ist die Aktualisierung sofort (**[!UICONTROL Success]** Status).
* Wenn der IP-Pool **is** mit einer Kanaloberfläche verknüpft ist, kann die Aktualisierung bis zu 3 Stunden dauern (**[!UICONTROL Processing]** Status).

>[!NOTE]
>
>Wann [Kanaloberfläche erstellen](channel-surfaces.md#create-channel-surface), wenn Sie einen IP-Pool auswählen, der in Bearbeitung ist (**[!UICONTROL Processing]** -Status) und nie mit der für diese Oberfläche ausgewählten Subdomain verknüpft wurde, können Sie mit der Erstellung der Oberfläche nicht fortfahren. [Weitere Infos](channel-surfaces.md#subdomains-and-ip-pools)

Um den Status der Aktualisierung des IP-Pools zu überprüfen, klicken Sie auf das **[!UICONTROL More actions]** Schaltfläche und wählen Sie **[!UICONTROL Recent updates]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Nachdem ein IP-Pool erfolgreich aktualisiert wurde, müssen Sie möglicherweise warten:
>* einige Minuten vor der Nutzung durch die einheitlichen Nachrichten,
>* bis zum nächsten Batch für den IP-Pool in Batch-Nachrichten wirksam sein.


Sie können auch die **[!UICONTROL Delete]** Schaltfläche zum Löschen eines IP-Pools. Beachten Sie, dass Sie einen IP-Pool, der mit einer Kanaloberfläche verknüpft wurde, nicht löschen können.

