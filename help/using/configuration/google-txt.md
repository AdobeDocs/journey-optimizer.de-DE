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
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 100%

---


# Hinzufügen eines Google TXT-Eintrags zu einer Subdomain

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Für optimale Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen können Sie Ihren Subdomains mit Customer Journey Management spezielle TXT-Einträge der Website-Überprüfung von Google hinzufügen, um für ihre Verifizierung zu sorgen.

>[!NOTE]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomain den Status **[!UICONTROL Erfolg]** aufweist. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](access-subdomains.md).

Gehen Sie wie folgt vor, um Ihrer Subdomain einen Google TXT-Eintrag hinzuzufügen:

1. Öffnen Sie die Subdomain über das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Subdomains]** .

1. Geben Sie im Abschnitt „Google TXT-Eintrag“ den Verifizierungs-Code ein, der in [G Suite Admin Tools](https://support.google.com/a/answer/183895) generiert wurde, und klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![](../assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, müssen Sie ihn von Google verifizieren lassen. Navigieren Sie dazu zu den G Suite Admin Tools und starten Sie dann den Verifizierungsvorgang.
