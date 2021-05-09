---
title: Subdomänen delegieren
description: Erfahren Sie, wie Sie Ihre Subdomänen delegieren
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
source-git-commit: 65e677860a6ba77532cc23b992d2671652548d0f
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# hinzufügen eines Google TXT-Datensatzes in eine Subdomäne

TXT-Datensätze sind eine Art DNS-Datensätze, die zur Bereitstellung von Textinformationen über eine Domäne verwendet werden, die von externen Quellen gelesen werden können.

Um eine gute Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen, ermöglicht Ihnen das Kundenmanagement, Ihren Subdomänen besondere TXT-Verifizierungs-TXT-Datensätze für Google-Journey hinzuzufügen, um sicherzustellen, dass diese verifiziert werden.

>[!NOTE]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomäne den Status **[!UICONTROL Verified]** hat. Weitere Informationen zu den Status von Subdomänen finden Sie in [diesem Abschnitt](access-subdomains.md).

Gehen Sie wie folgt vor, um Ihrer Subdomäne einen Google TXT-Datensatz hinzuzufügen:

1. Öffnen Sie die Subdomäne im Menü **[!UICONTROL Message Configuration]** / **[!UICONTROL Subdomain delegation]**.

1. Geben Sie im Abschnitt &quot;Google-TXT-Datensatz&quot;den in [G Suite Admin Tools](https://support.google.com/a/answer/183895) generierten Verifizierungscode ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

![](../assets/subdomain-google-txt.png)

1. Nachdem der TXT-Datensatz hinzugefügt wurde, müssen Sie ihn von Google überprüfen lassen. Navigieren Sie dazu zu den Admin Tools der G Suite und starten Sie dann den Überprüfungsschritt.
