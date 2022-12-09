---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen eines Google TXT-Eintrags zu einer Subdomain
description: Erfahren Sie, wie Sie einen Google TXT-Eintrag zu einer Subdomain hinzufügen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Hinzufügen eines Google TXT-Eintrags zu einer Subdomain {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT-Einträge"
>abstract="Um einen erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen, können Sie Ihrer Subdomain spezielle TXT-Einträge für die Websiteüberprüfung von Google hinzufügen, um sicherzustellen, dass sie verifiziert ist."

TXT-Einträge sind eine Art von DNS-Einträgen, die zur Bereitstellung von Textinformationen über eine Domäne verwendet werden und von externen Quellen gelesen werden können.

Um eine optimale Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen, [!DNL Journey Optimizer] ermöglicht es Ihnen, Ihrer Subdomain spezielle TXT-Einträge für die Überprüfung der Google-Site hinzuzufügen, um sicherzustellen, dass sie verifiziert ist.

>[!CAUTION]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomain über die **[!UICONTROL Success]** Status. Weitere Informationen zum Status von Subdomains finden Sie unter [diesem Abschnitt](about-subdomain-delegation.md#access-delegated-subdomains).

Gehen Sie wie folgt vor, um Ihrer Subdomain einen Google TXT-Eintrag hinzuzufügen:

1. Öffnen Sie die Subdomain über die **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** Menü.

1. Im **[!UICONTROL Google txt record]** geben Sie den aus generierten Verifizierungscode ein. [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->Klicken Sie auf **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, müssen Sie ihn von Google verifizieren lassen. Navigieren Sie dazu zu [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->und starten Sie dann den Verifizierungsschritt.
