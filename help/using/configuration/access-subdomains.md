---
title: Zugriff auf zugewiesene Subdomains
description: Erfahren Sie, wie Sie auf zugewiesene Subdomains zugreifen können.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: ht
source-wordcount: '168'
ht-degree: 100%

---

# Zugriff auf zugewiesene Subdomains {#access-delegated-subdomains}

Alle zugewiesenen Subdomains werden im Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Subdomains]** angezeigt. Es stehen Filter zur Verfügung, mit denen Sie die Liste eingrenzen können (Datum der Zuweisung, Benutzer oder Status).

![](assets/subdomain-list.png)

Die Spalte **[!UICONTROL Status]** enthält Informationen zum Prozess der Zuweisung von Subdomains:

* **[!UICONTROL Entwurf]**: Die Subdomain-Zuweisung wurde als Entwurf gespeichert. Klicken Sie auf den Namen der Subdomain, um den Zuweisungsprozess fortzusetzen.
* **[!UICONTROL In Verarbeitung]**: Die Subdomain wird mehreren Konfigurationsprüfungen unterzogen, bevor sie verwendet werden kann.
* **[!UICONTROL Erfolgreich]**: Die Subdomain hat die Prüfungen erfolgreich durchlaufen und bestanden und kann zum Versand von Nachrichten verwendet werden.
* **[!UICONTROL Fehlgeschlagen]**: Eine oder mehrere Prüfungen sind fehlgeschlagen, nachdem die Subdomain-Zuweisung übermittelt wurde.

Um auf detaillierte Informationen zu einer Subdomain zuzugreifen, öffnen Sie sie aus der Liste. Sie haben folgende Möglichkeiten:

* Rufen Sie den während des Zuweisungsprozesses konfigurierten Subdomain-Namen (schreibgeschützt) sowie die generierten URLs (Ressourcen, Mirror-Seite, Tracking-URLs) ab oder

* Fügen Sie Ihrer Subdomain einen TXT-Eintrag für die Website-Überprüfung von Google hinzu, um sicherzustellen, dass er verifiziert ist (siehe [Hinzufügen eines Google TXT-Eintrags zu einer Subdomain](google-txt.md)).

![](assets/subdomain-delegated.png)
