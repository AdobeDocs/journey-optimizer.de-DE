---
solution: Journey Optimizer
product: journey optimizer
title: Personalisieren von Inhalten in Journey Optimizer
description: Erste Schritte bei der Personalisierung.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: Ausdruck, Editor, Start, Personalisierung
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 93%

---

# Erste Schritte bei der Personalisierung{#add-personalization}

Erkunden Sie die Personalisierungs-Funktionen von [!DNL Adobe Journey Optimizer], um Ihre Nachrichten an jeden einzelnen Empfänger anhand der vorhandenen Daten anzupassen. Dabei kann es sich z. B. um den Vornamen des Empfängers, seine Interessen, seinen Wohnort oder zuvor gekaufte Artikel handeln.

➡️ [In diesen Videos erfahren Sie, wie Sie eine Nachricht personalisieren](#video-perso)
➡️ [Entdecken Sie Anwendungsfälle, die Personalisierung nutzen](personalization-use-case.md)

## Erstellen von Personalisierungsausdrücken mithilfe einer dedizierten Syntax {#syntax}

[!DNL Journey Optimizer] verwendet eine einfache **Inline**-Personalisierungssyntax, die auf Handlebars basiert. Damit können Sie Ausdrücke mit Inhalten erstellen, die von geschweiften Klammern **{{}}** eingeschlossen sind. Sie können ohne Einschränkungen mehrere Ausdrücke in demselben Inhalt oder Feld hinzufügen. Weitere Informationen finden Sie unter [Personalisierungssyntax](personalization-syntax.md).

**Beispiele:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Bei der Verarbeitung der Nachricht (E-Mail und Push-Benachrichtigung) ersetzt Journey Optimizer den Ausdruck durch die in der Experience Platform-Datenbank enthaltenen Daten: `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wird zu „Hallo, Max Mustermann“.

## Nutzen von Profildaten, um Ihre Nachrichten zu personalisieren {#data}

Die Personalisierung basiert auf den Profildaten, die von dem in Adobe Experience Platform definierten Schema **XDM-Kontaktprofil** verwaltet werden. Weitere Informationen finden Sie in der [Dokumentation zum Adobe Experience Platform-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}.

>[!CAUTION]
>Das Schema **XDM-Kontaktprofil** ist das einzige, das Sie zum Personalisieren von Inhalten in [!DNL Journey Optimizer] verwenden können.

## Hinzufügen der Personalisierung in unterschiedlichen Kontexten {#contexts}

[!DNL Journey Optimizer] ermöglicht es Ihnen, den Inhalt und die Anzeige von Nachrichten auf unterschiedliche Weise zu personalisieren. Weitere Informationen zu den Kontexten, in denen Sie Personalisierungen durchführen können, finden Sie in [diesem Abschnitt](personalization-contexts.md).

## Arbeiten mit dem Ausdruckseditor {#editor}

[!DNL Journey Optimizer] bietet einen Ausdruckseditor, in dem Sie alle Daten auswählen, anordnen, anpassen und validieren können, um eine individuelle Personalisierung für Ihre Inhalte zu erstellen.

Es stehen verschiedene Tools zur Verfügung, die Sie bei der Erstellung Ihres Personalisierungsinhalts unterstützen (Hilfsfunktionen, Bibliothek mit vordefinierten Ausdrücken, Favorisierung von Attributen usw.).

Weitere Informationen zum [!DNL Journey Optimizer] Ausdruckseditor finden Sie in [diesem Abschnitt](personalization-build-expressions.md)

## Anleitungsvideos{#video-perso}

Erfahren Sie, wie Sie kontextuelle Ereignisinformationen von einer Journey verwenden können, um eine Nachricht zu personalisieren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Erfahren Sie, wie Sie einer Nachricht profilbasierte Personalisierung hinzufügen und wie Sie die Zielgruppenzugehörigkeit als Voraussetzung für einen Gestaltungsbaustein verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
