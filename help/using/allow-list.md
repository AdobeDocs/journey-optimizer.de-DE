---
title: Zulassungsliste
description: Erfahren Sie, wie Sie die Zulassungsliste verwenden.
feature: Zustellbarkeit
topic: Content-Management
role: User
level: Intermediate
source-git-commit: e2743c8fa624a7a95b12c3adb5dc17a1b632c25d
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---

# Zulassungsliste {#allow-list}

Es ist jetzt möglich, eine spezifische sendesichere Liste auf der Ebene [sandbox](administration/sandboxes.md) zu definieren, um eine sichere Umgebung für Testzwecke zu haben. Auf einer Nicht-Produktionsinstanz, bei der Fehler auftreten können, stellt die Zulassungsliste sicher, dass Sie kein Risiko haben, unerwünschte Nachrichten an Ihre Kunden zu senden.

Mit der Zulassungsliste können Sie einzelne E-Mail-Adressen oder Domänen angeben, die die einzigen Empfänger oder Domänen sind, die berechtigt sind, die von einer bestimmten Sandbox gesendeten E-Mails zu empfangen. Dadurch können Sie verhindern, dass Sie in einer Testumgebung versehentlich E-Mails an echte Kundenadressen senden.

>[!CAUTION]
>
>Diese Funktion ist **nicht** in Produktions-Sandboxes verfügbar. Dies gilt nur für den E-Mail-Kanal.

## Zulassungsliste aktivieren {#enable-allow-list}

Um diese Funktion in einer Nicht-Produktions-Sandbox zu aktivieren, aktualisieren Sie die Zulassungsliste, sodass sie nicht mehr leer ist. Um sie zu deaktivieren, löschen Sie die Zulassungsliste so, dass sie wieder leer ist.

Weitere Informationen zur Logik der Zulassungsliste finden Sie in [diesem Abschnitt](#logic).

<!--
To enable the allowed list on a non-production sandbox, you need to make an Adobe API call.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* The allowed list logic applies when the feature is enabled and if the allowed list is not empty. Learn more in this section (logic).
-->

>[!NOTE]
>
>Wenn diese Option aktiviert ist, wird die Zulassungsliste-Funktion beim Ausführen von Journey-Tests, aber auch beim Testen von Nachrichten mit [Testsendungen](preview.md#send-proofs) und beim Testen von Journey mithilfe des [Testmodus](building-journeys/testing-the-journey.md) berücksichtigt.

## Entitäten zur Zulassungsliste hinzufügen {#add-entities}

Um der Zulassungsliste für eine bestimmte Sandbox neue E-Mail-Adressen oder Domänen hinzuzufügen, müssen Sie die Unterdrückungs-API mit dem Wert `ALLOWED` für das Attribut `listType` aufrufen. Beispiel:

![](assets/allow-list-api.png)

Sie können die Vorgänge **Hinzufügen**, **Löschen** und **Get** ausführen.

>[!NOTE]
>
>Die Zulassungsliste kann bis zu 1.000 Einträge enthalten.

<!--Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## Zulassungsliste {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Wenn die Zulassungsliste **empty** ist, wird die Zulassungsliste nicht angewendet. Das bedeutet, dass Sie E-Mails an beliebige Profile senden können, sofern sie nicht auf der [Unterdrückungsliste](suppression-list.md) stehen.

Wenn die Zulassungsliste **nicht leer** ist, wird die Zulassungsliste-Logik angewendet:

* Wenn eine Entität **nicht auf der Zulassungsliste** und nicht auf der Unterdrückungsliste steht, erhält der entsprechende Empfänger die E-Mail nicht, weshalb **[!UICONTROL Nicht erlaubt]** ist.

* Wenn eine Entität **auf der Zulassungsliste** und nicht auf der Unterdrückungsliste steht, kann die E-Mail an den entsprechenden Empfänger gesendet werden. Wenn sich die Entität jedoch auch auf der [Unterdrückungsliste](suppression-list.md) befindet, erhält der entsprechende Empfänger die E-Mail nicht, weshalb **[!UICONTROL Unterdrückt]** ist.




