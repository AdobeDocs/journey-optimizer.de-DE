---
title: weitere Zustellversuche vor dem Senden an die Unterdrückungs-Liste
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
source-git-commit: a65cefd0bbd15ffa389bac910eaceb40181cb38d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# weitere Zustellversuche vor dem Senden an die Unterdrückungs-Liste

Wenn eine Nachricht aufgrund eines Fehlers bei einem weichen Absprung fehlschlägt, werden mehrere weitere Zustellversuche ausgeführt, bevor die E-Mail-Adresse an die Unterdrückungs-Liste gesendet wird. Jeder Fehler inkrementiert einen Fehlerzähler. Wenn dieser Zähler den Grenzwert erreicht, wird die Adresse in die Unterdrückungs-Liste gesetzt.

In der Standardkonfiguration ist die Limit-Schwellenwert-Nummer auf 3-Fehler festgelegt, d. h. die Adresse wird an die Quartil-Liste zum dritten aufgetretenen Fehler gesendet. Wenn ein Versand nach einem erneuten Versuch erfolgreich war, wird der Fehlerzähler erneut initialisiert.

Sie können den Limit-Schwellenwert direkt über die Schaltfläche Bearbeiten im Menü Allgemeine Einstellungen ändern.

![](../assets/retries-edition.png)
