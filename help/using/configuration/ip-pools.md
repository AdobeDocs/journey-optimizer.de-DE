---
title: Erstellen von IP-Pools
description: „Informationen zum Verwalten von IP-Pools“
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 92%

---

# Erstellen von IP-Pools {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="Einrichten eines IP-Pools"
>abstract="Sie können IP-Pools erstellen, um die IP-Adressen Ihrer Subdomains zu gruppieren und so die Zustellbarkeit Ihrer E-Mails zu verbessern."

## Über IP-Pools {#about-ip-pools}

Mit [!DNL Journey Optimizer]können Sie IP-Pools erstellen, um die IP-Adressen Ihrer Subdomains zu gruppieren.

Zur verbesserten Zustellbarkeit von E-Mails wird dringend empfohlen, IP-Pools zu erstellen. Auf diese Weise können Sie verhindern, dass die Reputation einer Subdomain eine Auswirkung auf Ihre anderen Subdomains hat.

Eine Best Practice ist beispielsweise, einen IP-Pool für Ihre Marketing-Nachrichten und einen weiteren für Ihre Transaktionsnachrichten zu nutzen. Auf diese Weise wirkt sich eine Marketing-Nachricht, die vom Kunden abgelehnt und als Spam gekennzeichnet wird, nicht auf die an denselben Kunden gesendeten Transaktionsnachrichten aus, sodass dieser Kunde weiterhin Transaktionsnachrichten erhält (Kaufbestätigungen, Nachrichten zur Passwortwiederherstellung usw.).

## Erstellen eines IP-Pools {#create-ip-pool}

Gehen Sie wie folgt vor, um einen IP-Pool zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL IP-Pools]** auf und klicken Sie dann auf **[!UICONTROL IP-Pool erstellen]**.

   ![](assets/ip-pool-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für den IP-Pool an.

   >[!NOTE]
   >
   >Der Name der Subdomain muss mit einem Buchstaben (A–Z) beginnen und nur alphanumerische Zeichen oder Sonderzeichen ( _, ., - ) enthalten.

1. Wählen Sie aus der Dropdown-Liste die IP-Adressen aus, die in den Pool aufgenommen werden sollen, und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Alle mit Ihrer Instanz bereitgestellten IP-Adressen sind in der Liste verfügbar.

Der IP-Pool wird jetzt erstellt und in der Liste angezeigt. Sie können ihn auswählen, um auf seine Eigenschaften zuzugreifen und die zugehörige Nachrichtenvoreinstellung anzuzeigen. Weiterführende Informationen zum Verknüpfen einer Nachrichtenvoreinstellung mit einem IP-Pool finden Sie in [diesem Abschnitt](message-presets.md).

![](assets/ip-pool-created.png)

## Bearbeiten eines IP-Pools {#edit-ip-pool}

So bearbeiten Sie einen IP-Pool:

1. Klicken Sie in der Liste auf den Namen des IP-Pools, um ihn zu öffnen.

   ![](assets/ip-pool-list.png)

1. Bearbeiten Sie die Eigenschaften nach Bedarf. Sie können die Beschreibung ändern und IP-Adressen hinzufügen oder entfernen.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Gehen Sie beim Löschen einer IP-Adresse mit besonderer Sorgfalt vor, da dies die anderen IPs zusätzlich belastet und möglicherweise erhebliche Auswirkungen auf Ihre Zustellbarkeit hat. Wenden Sie sich im Zweifel an einen Zustellbarkeitsexperten.

1. Speichern Sie Ihre Änderungen.

>[!NOTE]
>
>Der Name des IP-Pools kann nicht bearbeitet werden. Wenn Sie ihn ändern möchten, müssen Sie den IP-Pool löschen und einen neuen mit dem Namen Ihrer Wahl erstellen.

Die Aktualisierung ist sofort oder asynchron wirksam, je nachdem, ob der IP-Pool mit einer [Nachrichtenvoreinstellung](message-presets.md) verknüpft ist oder nicht:

* Wenn der IP-Pool in einer Nachrichtenvoreinstellung **nicht** ausgewählt ist, erfolgt die Aktualisierung sofort (Status **[!UICONTROL Erfolg]**).
* Wenn der IP-Pool in einer Nachrichtenvoreinstellung ausgewählt **ist**, kann die Aktualisierung mitunter 7–10 Werktage dauern (Status **[!UICONTROL wird verarbeitet]**).

Um den Status der Aktualisierung des IP-Pools zu überprüfen, klicken Sie auf den Button **[!UICONTROL Mehr Aktionen]** und wählen Sie **[!UICONTROL Letzte Updates]** aus.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Nachdem ein IP-Pool erfolgreich aktualisiert wurde, müssen Sie möglicherweise warten:
>* einige Minuten, bevor er von den unitären Nachrichten genutzt wird,
>* bis der nächste Batch für den IP-Pool in Batch-Nachrichten wirksam ist.


Sie können auch den Button **[!UICONTROL Löschen]** verwenden, um einen IP-Pool zu löschen. Beachten Sie, dass Sie einen mit einer Nachrichtenvoreinstellung verknüpften IP-Pool nicht löschen können.

