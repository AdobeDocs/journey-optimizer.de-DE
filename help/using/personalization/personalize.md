---
solution: Journey Optimizer
product: journey optimizer
title: Personalisieren von Inhalten in Journey Optimizer
description: Erste Schritte mit der Personalisierung.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Erste Schritte mit der Personalisierung{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] Personalisierungsfunktionen , mit denen Sie Ihre Nachrichten an jeden einzelnen Empfänger anpassen können, indem Sie die vorhandenen Daten und Informationen nutzen. Es kann sein Vorname, Interessen, wo sie leben, was sie kauften und mehr.

➡️ [In diesen Videos erfahren Sie, wie Sie eine Nachricht personalisieren.](#video-perso)
➡️ [Anwendungsbeispiele zur Personalisierung in Discover](personalization-use-case.md)

## Personalisierungsausdrücke mithilfe einer dedizierten Syntax erstellen {#syntax}

[!DNL Journey Optimizer] verwendet eine **inline** einfache Personalisierungssyntax, die auf Handlebars basiert und es Ihnen ermöglicht, Ausdrücke mit Inhalten zu erstellen, die von doppelten geschweiften Klammern eingeschlossen sind **{{}}**. Sie können im selben Inhalt oder Feld mehrere Ausdrücke ohne Einschränkungen hinzufügen. Weitere Informationen finden Sie unter [Personalisierungssyntax](personalization-syntax.md).

**Beispiele:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Bei der Verarbeitung der Nachricht (E-Mail und Push-Benachrichtigung) ersetzt Journey Optimizer den Ausdruck durch die in der Experience Platform-Datenbank enthaltenen Daten:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wird zu &quot;Hallo Max Mustermann&quot;.

## Nutzen Sie Profildaten, um Ihre Nachrichten zu personalisieren. {#data}

Die Personalisierung basiert auf den Profildaten, die von der **XDM Individual Profile** in Adobe Experience Platform definiertes Schema. Weitere Informationen finden Sie unter [Dokumentation zum Adobe Experience Platform-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

>[!CAUTION]
>Die **XDM Individual Profile** schema ist das einzige Schema, mit dem Sie Inhalte personalisieren können in [!DNL Journey Optimizer].

## Personalisierung in unterschiedlichen Kontexten hinzufügen {#contexts}

[!DNL Journey Optimizer] ermöglicht es Ihnen, den Inhalt und die Anzeige von Nachrichten auf verschiedene Weise zu personalisieren. Weitere Informationen zu den Kontexten, in denen Sie Personalisierungen durchführen können, finden Sie unter [diesem Abschnitt](personalization-contexts.md).

## Arbeiten mit dem Ausdruckseditor {#editor}

[!DNL Journey Optimizer] bietet einen Ausdruckseditor, in dem Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihren Inhalt zu erstellen.

Es stehen verschiedene Tools zur Verfügung, die Sie bei der Erstellung Ihres Personalisierungsinhalts unterstützen (Hilfsfunktionen, vordefinierte Ausdrucksbibliothek, beliebte Attribute usw.).

Weitere Informationen [!DNL Journey Optimizer] Ausdruckseditor in [diesem Abschnitt](personalization-build-expressions.md)

## Anleitungsvideos{#video-perso}

Erfahren Sie, wie Sie kontextbezogene Ereignisinformationen aus einer Journey verwenden können, um eine Nachricht zu personalisieren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Erfahren Sie, wie Sie einer Nachricht profilbasierte Personalisierung hinzufügen und wie Sie die Segmentzugehörigkeit als Voraussetzung für einen Gestaltungsbaustein verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
