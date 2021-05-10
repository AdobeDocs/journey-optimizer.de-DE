---
title: Inhalte in Journey Optimizer personalisieren
description: Erste Schritte mit der Personalisierung
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---

# Erste Schritte mit der Personalisierung{#add-personalization}

![](../assets/do-not-localize/badge.png)

Discover Journey Optimier-Personalisierungsfunktionen, um Ihre Nachrichten an jeden bestimmten Empfänger anzupassen, indem Sie die Daten und Informationen nutzen, die Sie zu ihm/ihr haben. Es kann sein Vorname sein, seine Interessen, wo er lebt, was er kaufte und mehr.

Journey Optimizer verwendet eine einfache Personalisierungssyntax **inline**, die auf den Handlebars basiert, mit der Sie Ausdruck mit Inhalten erstellen können, die von den geschweiften Klammern **{}** eingeschlossen sind. Sie können ohne Einschränkungen mehrere Ausdruck in demselben Inhalt oder Feld hinzufügen. Weitere Informationen finden Sie unter [Personalisierungssyntax](personalization-syntax.md).

Die Personalisierung basiert auf den Profil-Daten, die von dem in Adobe Experience Platform definierten Schema **XDM Individuelles Profil** verwaltet werden. Weitere Informationen hierzu finden Sie in der [Dokumentation zum Adobe Experience Platform-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

>[!CAUTION]
>Das Schema **XDM Individuelles Profil** ist das einzige Schema, mit dem Sie Inhalte in Journey Optimizer personalisieren können.

**Beispiele:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Bei der Verarbeitung der Nachricht (E-Mail und Push) ersetzt Journey Optimizer den Ausdruck durch die Daten in der Experience Cloud Platform-Datenbank.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
