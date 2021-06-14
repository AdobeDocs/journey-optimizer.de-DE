---
title: Personalisieren von Inhalten in Journey Optimizer
description: Erste Schritte mit der Personalisierung
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 52%

---

# Erste Schritte mit der Personalisierung{#add-personalization}

![](../assets/do-not-localize/badge.png)

Entdecken Sie die Personalisierungsfunktionen von Journey Optimier, um Ihre Nachrichten an jeden einzelnen Empfänger anzupassen, indem Sie die vorhandenen Daten und Informationen zu ihm/ihr nutzen. Es kann sein Vorname, seine Interessen, wo er lebt, was er kaufte und mehr.

Journey Optimizer verwendet eine einfache **Inline**-Personalisierungssyntax, die auf Handlebars basiert. Damit können Sie Ausdrücke mit Inhalten erstellen, die von geschweiften Klammern **{{}}** eingeschlossen sind. Sie können ohne Einschränkungen mehrere Ausdrücke in demselben Inhalt oder Feld hinzufügen. Weitere Informationen finden Sie unter [Personalisierungssyntax](personalization-syntax.md).

Die Personalisierung basiert auf den Profildaten, die von dem in Adobe Experience Platform definierten Schema **Individuelles XDM-Profil** verwaltet werden. Weitere Informationen hierzu finden Sie in der [Dokumentation zum Adobe Experience Platform-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de).

>[!CAUTION]
>Das Schema **XDM Individual Profile** ist das einzige Schema, das Sie zum Personalisieren von Inhalten in Journey Optimizer verwenden können.

**Beispiele:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Bei der Verarbeitung der Nachricht (E-Mail und Push-Benachrichtigung) ersetzt Journey Optimizer den Ausdruck durch die in der Experience Cloud Platform-Datenbank enthaltenen Daten.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
