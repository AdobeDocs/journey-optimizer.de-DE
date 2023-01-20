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
source-git-commit: b3270b8e806cf6e57ea4bcdfa93c8baedc9523f1
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 75%

---

# Hinzufügen eines Google TXT-Eintrags zu einer Subdomain {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="TXT-Einträge von Google"
>abstract="Für einen erfolgreichen Versand von E-Mails an Gmail-Adressen können Sie Ihren Subdomains spezielle TXT-Einträge der Website-Überprüfung von Google hinzuzufügen, um ihre Verifizierung sicherzustellen."

TXT-Einträge sind eine Art DNS-Eintrag, der verwendet wird, um Textinformationen über eine Domäne bereitzustellen, die von externen Quellen gelesen werden können.

Für optimale Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen ermöglicht es Ihnen [!DNL Journey Optimizer], Ihren Subdomains spezielle TXT-Einträge der Website-Überprüfung von Google hinzuzufügen, um ihre Verifizierung sicherzustellen.

>[!CAUTION]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomain den Status **[!UICONTROL Erfolg]** aufweist. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](about-subdomain-delegation.md#access-delegated-subdomains).

Gehen Sie wie folgt vor, um Ihrer Subdomain einen Google TXT-Eintrag hinzuzufügen:

1. Öffnen Sie die Subdomain über das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Subdomains]** .

1. Im **[!UICONTROL Google-Textdatensatz]** geben Sie den aus generierten Verifizierungscode ein. [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->Klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, muss er von Google verifiziert werden. Navigieren Sie dazu zu [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->und starten Sie dann den Verifizierungsschritt.
