---
title: Zulassungsliste
description: Erfahren Sie, wie Sie die Zulassungsliste verwenden.
feature: Zustellbarkeit
topic: Content-Management
role: User
level: Intermediate
source-git-commit: 288c27d4fc64a6d0a6f07b634ed044a6e858d0c1
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 2%

---

# Zulassungsliste {#allow-list}

Es ist jetzt möglich, eine spezifische sendesichere Liste auf der Ebene [sandbox](administration/sandboxes.md) zu definieren, um eine sichere Umgebung für Testzwecke zu haben. Auf einer Nicht-Produktionsinstanz, bei der Fehler auftreten können, stellt die Zulassungsliste sicher, dass Sie kein Risiko haben, unerwünschte Nachrichten an Ihre Kunden zu senden.

>[!CAUTION]
>
>Diese Funktion ist nicht in Produktions-Sandboxes verfügbar.

Mit der Zulassungsliste können Sie einzelne E-Mail-Adressen oder Domänen angeben, die die einzigen Empfänger oder Domänen sind, die berechtigt sind, die von einer bestimmten Sandbox gesendeten E-Mails zu empfangen. Dadurch können Sie verhindern, dass Sie in einer Testumgebung versehentlich E-Mails an echte Kundenadressen senden.

>[!NOTE]
>
>Diese Funktion gilt nur für den E-Mail-Kanal.

## Zulassungsliste aktivieren {#enable-allow-list}

Um die Zulassungsliste in einer Nicht-Produktions-Sandbox zu aktivieren, müssen Sie einen Adobe-API-Aufruf ausführen.

* Mit dieser API können Sie die Funktion auch jederzeit deaktivieren.

* Sie können die Zulassungsliste vor oder nach der Aktivierung der Funktion aktualisieren.

* Die Logik der Zulassungsliste gilt, wenn die Funktion aktiviert ist und die Zulassungsliste nicht leer ist. Weiterführende Informationen finden Sie in diesem [Abschnitt](#logic).

>[!NOTE]
>
>Wenn diese Option aktiviert ist, wird die Zulassungsliste-Funktion beim Ausführen von Journey-Tests, aber auch beim Testen von Nachrichten mit [Testsendungen](preview.md#send-proofs) und beim Testen von Journey mithilfe des [Testmodus](building-journeys/testing-the-journey.md) berücksichtigt.

## Entitäten zur Zulassungsliste hinzufügen {#add-entities}

>[!CAUTION]
>
>Diese Funktion ist **nicht** in Produktions-Sandboxes verfügbar. Dies gilt nur für den E-Mail-Kanal.

Um der Zulassungsliste für eine bestimmte Sandbox neue E-Mail-Adressen oder Domänen hinzuzufügen, müssen Sie die Unterdrückungs-API mit dem Wert `ALLOWED` für das Attribut `listType` aufrufen. Beispiel:

![](assets/allow-list-api.png)

Sie können die Vorgänge **Hinzufügen**, **Löschen** und **Get** ausführen.

>[!NOTE]
>
>Die Zulassungsliste kann bis zu 1.000 Einträge enthalten.

Weitere Informationen zum Ausführen von Adobe-API-Aufrufen finden Sie in der [Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).

## Zulassungsliste {#logic}

<!-- When the allowed list is \[enabled\]\(\add link here\) at the sandbox level using the API call above, the following applies.-->

1. Wenn die Zulassungsliste **empty** ist, wird die Zulassungsliste nicht angewendet. Das bedeutet, dass Sie E-Mails an beliebige Profile senden können, sofern sie nicht auf der [Unterdrückungsliste](suppression-list.md) stehen.

1. Wenn die Zulassungsliste **nicht leer** ist, wird die Zulassungsliste-Logik angewendet:

   * Wenn eine Entität **nicht auf der Zulassungsliste** und nicht auf der Unterdrückungsliste steht, erhält der entsprechende Empfänger die E-Mail nicht, weshalb **[!UICONTROL Nicht erlaubt]** ist.

   * Wenn eine Entität **auf der Zulassungsliste** und nicht auf der Unterdrückungsliste steht, kann die E-Mail an den entsprechenden Empfänger gesendet werden. Wenn sich die Entität jedoch auch auf der [Unterdrückungsliste](suppression-list.md) befindet, erhält der entsprechende Empfänger die E-Mail nicht, weshalb **[!UICONTROL Unterdrückt]** ist.




