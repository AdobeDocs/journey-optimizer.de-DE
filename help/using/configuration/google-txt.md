---
title: Zuweisen von Subdomains
description: Informationen zum Zuweisen Ihrer Subdomains
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
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 1d7f661dc0a89e4754a76ecf2cdce1e43a5275ec
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 60%

---

# Hinzufügen eines Google TXT-Eintrags zu einer Subdomain

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Um eine gute Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen, [!DNL Journey Optimizer] ermöglicht es Ihnen, Ihren Subdomains spezielle TXT-Einträge für die Google-Websiteüberprüfung hinzuzufügen, um sicherzustellen, dass sie verifiziert werden.

>[!CAUTION]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomain den Status **[!UICONTROL Erfolg]** aufweist. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](access-subdomains.md).

Gehen Sie wie folgt vor, um Ihrer Subdomain einen Google TXT-Eintrag hinzuzufügen:

1. Öffnen Sie die Subdomain über das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Subdomains]** .

1. Im **[!UICONTROL Google-Textdatensatz]** geben Sie den aus generierten Verifizierungscode ein. [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->Klicken Sie auf **[!UICONTROL Speichern]**.

   ![](../assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, müssen Sie ihn von Google verifizieren lassen. Navigieren Sie dazu zu [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->und starten Sie dann den Verifizierungsschritt.
