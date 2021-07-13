---
title: PTR-Einträge
description: „Informationen zum Verwalten von PTR-Einträgen“
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
feature: Anwendungskonfiguration
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 100%

---


# PTR-Einträge

## Informationen zu PTR-Einträgen

Ein PTR (Pointer Record, „Zeigereintrag“) ist ein Typ von DNS (Domain Name System)-Eintrag, der den mit einer IP-Adresse verknüpften Domain-Namen bereitstellt.

Mit PTR-Einträgen können Empfänger-E-Mail-Server die Authentizität der Sender-E-Mail-Server überprüfen, indem sie feststellen, ob ihre IP-Adressen mit den Namen übereinstimmen, mit denen sich die Server verbinden.

## Zugriff auf PTR-Einträge Ihrer Subdomains

Nachdem eine Subdomain in Customer Journey Management zugewiesen wurde, wird automatisch ein PTR-Eintrag erstellt und mit dieser Subdomain verknüpft. Sie können darauf über das Menü **[!UICONTROL Kanäle]** `>` **[!UICONTROL PTR-Einträge]** zugreifen.

![](../assets/ptr-records.png)

In der Liste werden die für jede zugewiesene Subdomain generierten PTR-Einträge anhand der unten stehenden Syntax angezeigt:

* „r“ für Eintrag (record),
* „xx“ für die beiden letzten Zahlen der IP-Adresse,
* Name der Subdomain.

Sie können einen PTR-Eintrag aus der Liste öffnen, um den zugehörigen Subdomain-Namen und die IP-Adresse anzuzeigen.

>[!NOTE]
>
>Beachten Sie, dass die PTR-Einträge schreibgeschützt sind und dass Sie die mit einer IP-Adresse verknüpfte Subdomain nicht ändern können.
