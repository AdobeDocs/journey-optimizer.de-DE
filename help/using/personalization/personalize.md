---
title: Inhalte in Journey Optimizer personalisieren
description: Erste Schritte mit der Personalisierung
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Erste Schritte {#add-personalization}

![](../assets/do-not-localize/badge.png)

Personalisierung im Kontext von Journey Optimizer ist die Aktion, eine Nachricht an einen bestimmten Abonnenten zu richten, indem die Daten und Informationen, die Sie über ihn haben, genutzt werden. Es kann sein Vorname sein, seine Interessen, wo er lebt und mehr.

Journey Optimizer verwendet eine einfache Personalisierungssyntax **inline**, die auf den Handlebars basiert, mit der Sie Ausdruck mit Inhalten erstellen können, die von den geschweiften Klammern **{}** eingeschlossen sind. Sie können ohne Einschränkungen mehrere Ausdruck in demselben Inhalt oder Feld hinzufügen. Siehe [Personalisierungssyntax](personalization-syntax.md).

Die Personalisierung basiert auf den Profil-Daten, die von dem in Adobe Experience Platform definierten Schema **XDM Individuelles Profil** verwaltet werden. Weitere Informationen hierzu finden Sie in der [Dokumentation zum Adobe Experience Platform-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

>[!CAUTION]
>Das Schema **XDM Individuelles Profil** ist das einzige, das Sie zum Personalisieren von Inhalten in Journey Optimizer verwenden können.

**Beispiele:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Bei der **Nachrichtenverarbeitung** (E-Mail und Push) wird der Ausdruck durch die Daten in den Experience Cloud-Plattformdatenbanken ersetzt.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
