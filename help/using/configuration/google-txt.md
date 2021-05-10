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
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 24%

---


# hinzufügen eines Google TXT-Datensatzes in eine Subdomäne

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Um eine gute Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen, ermöglicht Ihnen das Kundenmanagement, Ihren Subdomänen besondere TXT-Verifizierungs-TXT-Datensätze für Google-Journey hinzuzufügen, um sicherzustellen, dass diese verifiziert werden.

>[!NOTE]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomäne den Status **[!UICONTROL Erfolg]** hat. Weitere Informationen zu den Status von Subdomänen finden Sie in [diesem Abschnitt](access-subdomains.md).

Gehen Sie wie folgt vor, um Ihrer Subdomäne einen Google TXT-Datensatz hinzuzufügen:

1. Öffnen Sie die Subdomäne im Menü **[!UICONTROL Kanal]** / **[!UICONTROL Subdomains]**.

1. Geben Sie im Abschnitt &quot;Google-TXT-Datensatz&quot;den in [G Suite Admin Tools](https://support.google.com/a/answer/183895) generierten Verifizierungscode ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

![](../assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, müssen Sie ihn von Google verifizieren lassen. Navigieren Sie dazu zu den Admin Tools der G Suite und starten Sie dann den Überprüfungsschritt.
