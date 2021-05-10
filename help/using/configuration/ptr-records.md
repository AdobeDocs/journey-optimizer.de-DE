---
title: PTR-Aufzeichnungen
description: Erfahren Sie, wie xxxx funktioniert
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
source-wordcount: '165'
ht-degree: 0%

---


# PTR-Aufzeichnungen

## Über PTR-Datensätze

Ein Zeigerdatensatz (PTR) ist ein Typ des DNS-Datensatzes (Domain Name System), der den mit einer IP-Adresse verknüpften Domänennamen bereitstellt.

Bei PTR-Aufzeichnungen können Empfänger-E-Mail-Server die Authentizität des Versendens von E-Mail-Servern überprüfen, indem sie erkennen, ob ihre IP-Adressen mit den Namen übereinstimmen, mit denen die Server verbunden sind.

## Zugriff auf PTR-Datensätze Ihrer Subdomänen

Nachdem eine Subdomäne in Customer Journey Management delegiert wurde, wird automatisch ein PTR-Datensatz erstellt und dieser Subdomäne zugeordnet. Sie können darauf über das Menü **[!UICONTROL Kanal]** / **[!UICONTROL PTR-Datensätze]** zugreifen.

![](../assets/ptr-records.png)

Die Liste zeigt die für jede delegierte Subdomäne generierten PTR-Datensätze anhand der folgenden Syntax an:

* ‚r‘ für Datensatz,
* &quot;xx&quot; für die beiden letzten Zahlen der IP-Adresse,
* Subdomänenname.

Sie können einen PTR-Datensatz aus der Liste öffnen, um den zugehörigen Subdomänennamen und die IP-Adresse anzuzeigen.

>[!NOTE]
>
>Beachten Sie, dass die PTR-Datensätze schreibgeschützt sind und dass Sie die einer IP-Adresse zugeordnete Subdomäne nicht ändern können.
