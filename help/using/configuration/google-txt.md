---
title: Zuweisen von Subdomains
description: Erfahren Sie, wie Sie Ihre Subdomains zuweisen
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
source-git-commit: 2d8b7bbaee7509d4cc33445c64b2382ed14a9678
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 24%

---


# Hinzufügen eines Google TXT-Eintrags zu einer Subdomain

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Um eine gute Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen, können Sie mit Customer Journey Management Ihren Subdomains spezielle TXT-Einträge für die Websiteüberprüfung von Google hinzufügen, um sicherzustellen, dass sie verifiziert sind.

>[!NOTE]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomain den Status **[!UICONTROL Erfolg]** aufweist. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](access-subdomains.md).

Gehen Sie wie folgt vor, um Ihrer Subdomain einen Google TXT-Eintrag hinzuzufügen:

1. Öffnen Sie die Subdomain über das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Subdomains]** .

1. Geben Sie im Abschnitt &quot;Google TXT-Eintrag&quot;den Verifizierungscode ein, der in [G Suite Admin Tools](https://support.google.com/a/answer/183895) generiert wurde, und klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![](../assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, müssen Sie ihn von Google verifizieren lassen. Navigieren Sie dazu zu den G Suite Admin Tools und starten Sie dann den Verifizierungsschritt.
