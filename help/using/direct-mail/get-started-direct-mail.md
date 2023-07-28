---
title: Erste Schritte mit Briefpost
description: Erfahren Sie, wie Sie in Journey Optimizer eine Briefpost-Nachricht erstellen und senden.
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: Direkt-Mail, Nachricht, Kampagne
source-git-commit: a445e418dc11f577c609c16894ce119359f2a261
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 46%

---

# Erste Schritte mit Briefpost {#create-direct}

>[!AVAILABILITY]
>
>Derzeit ist der Briefpost-Kanal nicht für Organisationen verfügbar, die das Zusatzangebot Adobe Healthcare Shield erworben haben.
>

Briefpost ist ein Offline-Kanal, mit dem Sie die Extraktionsdateien personalisieren und generieren können, die Briefpostanbieter zum Senden von Nachrichten an Ihre Kunden benötigen.

Bei der Erstellung einer Briefpost-Kampagne generiert Journey Optimizer automatisch eine Datei, die alle Zielgruppenprofile und ausgewählten Daten enthält, z. B. Postanschriften und Profilattribute. Diese Datei wird an den Server Ihrer Wahl gesendet, damit sie von Ihrem ausgewählten Briefpost-Dienstleister zugänglich ist, der den eigentlichen Versandprozess für Sie handhabt.

Die wichtigsten Schritte zum Senden von Briefpost-Nachrichten sind:

![](assets/dm-creation-process.png)

Briefpostnachrichten können nur im Rahmen geplanter Kampagnen erstellt werden. Sie sind nicht für die Verwendung in API-basierten Kampagnen oder in Journeys verfügbar.

>[!IMPORTANT]
>
>Bevor Sie eine Briefpostnachricht senden, stellen Sie sicher, dass Sie Folgendes konfiguriert haben:
>
>1. Eine [Dateirouting-Konfiguration](../direct-mail/direct-mail-configuration.md#file-routing-configuration), die den Server angibt, auf den die Extraktionsdatei hochgeladen und gespeichert werden soll,
>1. Eine [Oberfläche für Briefpostnachrichten](../direct-mail/direct-mail-configuration.md#direct-mail-surface), die auf die Datei-Routing-Konfiguration verweist.
