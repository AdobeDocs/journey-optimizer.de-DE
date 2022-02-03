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
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 100%

---

# Hinzufügen eines Google TXT-Eintrags zu einer Subdomain {#google-txt-record}

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Für optimale Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen ermöglicht Ihnen [!DNL Journey Optimizer], Ihren Subdomains spezielle TXT-Einträge der Websiteüberprüfung von Google hinzuzufügen, um ihre Verifizierung sicherzustellen.

>[!CAUTION]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomain den Status **[!UICONTROL Erfolg]** aufweist. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](access-subdomains.md).

Gehen Sie wie folgt vor, um Ihrer Subdomain einen Google TXT-Eintrag hinzuzufügen:

1. Öffnen Sie die Subdomain über das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Subdomains]** .

1. Geben Sie im Abschnitt **[!UICONTROL Google TXT-Eintrag]** den Verifizierungs-Code ein, der in [Google Workspace](https://support.google.com/a/answer/183895){ target=&quot;_blank&quot;}<!--G Suite Admin tools--> generiert wurde. Klicken Sie dann auf  **[!UICONTROL Speichern]**.

   ![](../assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, muss er von Google verifiziert werden. Gehen Sie dazu zu [Google Workspace](https://support.google.com/a/answer/183895){ target=&quot;_blank&quot;}<!--G Suite Admin tools--> und starten Sie den Verifizierungsvorgang.
