---
title: PTR-Datensätze
description: '"Erfahren Sie, wie Sie ptr-records verwalten."'
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
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---


# PTR-Datensätze

## Über PTR-Datensätze

Ein Zeigerdatensatz (PTR) ist ein Typ von DNS-Eintrag (Domain Name System), der den mit einer IP-Adresse verknüpften Domänennamen bereitstellt.

Mit PTR-Datensätzen können Empfänger-E-Mail-Server die Authentizität der E-Mail-Server überprüfen, indem sie feststellen, ob ihre IP-Adressen mit den Namen übereinstimmen, mit denen sich die Server verbinden.

## Zugreifen auf PTR-Datensätze Ihrer Subdomains

Nachdem eine Subdomain in Customer Journey Management zugewiesen wurde, wird automatisch ein PTR-Datensatz erstellt und mit dieser Subdomain verknüpft. Sie können darauf über das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL PTR-Datensätze]** zugreifen.

![](../assets/ptr-records.png)

In der Liste werden die für jede zugewiesene Subdomain generierten PTR-Datensätze anhand der unten stehenden Syntax angezeigt:

* &quot;r&quot;für Datensatz,
* &quot;xx&quot; für die beiden letzten Zahlen der IP-Adresse,
* Name der Subdomäne.

Sie können einen PTR-Datensatz aus der Liste öffnen, um den zugehörigen Subdomain-Namen und die IP-Adresse anzuzeigen.

>[!NOTE]
>
>Beachten Sie, dass die PTR-Einträge schreibgeschützt sind und dass Sie die mit einer IP-Adresse verknüpfte Subdomain nicht ändern können.
