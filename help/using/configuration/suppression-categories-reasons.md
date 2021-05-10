---
title: Kategorien und Gründe der Unterdrückung
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
source-wordcount: '139'
ht-degree: 2%

---


# Kategorien und Gründe der Unterdrückung

Wenn eine Nachricht nicht an eine E-Mail-Adresse gesendet werden kann, bestimmt Journey Optimizer, warum der Versand fehlgeschlagen ist, und verknüpft sie mit einer Unterdrückungs-Kategorie.

Die Unterdrückungs-Kategorie bestimmt, wann die E-Mail-Adresse an die Unterdrückungs-Liste gesendet wird:

* Weich: Bei Soft-Fehlern wird eine Adresse an die Suppression-Liste gesendet, sobald der Fehlerzähler den Limit-Schwellenwert erreicht hat (siehe -ref-weitere Zustellversuche section-).
* Hart: Die E-Mail-Adresse wird sofort an die Unterdrückungs-Liste gesendet.
* Manuell: xxxx. !! Wie werden Adressen manuell an die Unterdrückungs-Liste gesendet?

Mögliche Fehlerursachen und die damit verbundene Kategorie sind:

| Grund | Beschreibung | Unterdrückung Kategorie |
|------|-----------|----|
| Postfach voll | Das Postfach des Empfängers ist voll und konnte die Nachricht nicht empfangen. | Soft |
| DNS-Fehler | xxx | Weich |
| Ungültiger Empfänger | xxx | Hard |

    !! Liste zum Aufwerten
