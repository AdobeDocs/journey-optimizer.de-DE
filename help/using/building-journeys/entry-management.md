---
solution: Journey Optimizer
product: journey optimizer
title: Profileintragsverwaltung
description: Erfahren Sie, wie Sie die Profileingabe verwalten
feature: Journeys
role: User
level: Intermediate
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 59%

---

# Profileintragsverwaltung {#entry-management}

Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die Option für „einmalige“ Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt. In diesem Fall möchten Sie nicht, dass der Kunde die Journey erneut betreten und das Angebot erneut wahrnehmen kann.

![](assets/journey-re-entrance.png)

Wenn eine Journey beendet wird, lautet ihr Status **[!UICONTROL Geschlossen]**. Neue Personen können nicht mehr in die Journey eintreten. Personen, die sich bereits im Journey befinden, beenden das Journey normal.

Nach der standardmäßigen globalen Zeitüberschreitung von 30 Tagen wechselt die Journey zur **Abgeschlossen** Status.  [Weitere Informationen](journey-gs.md#global_timeout).


## Einzelne Journey{#entry-unitary}

Einzelne Journeys (beginnend mit einem Ereignis oder einer Segmentqualifikation) enthalten eine Schutzvorkehrung, die verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.

Zusätzlich:

* Wenn der erneute Eintritt aktiviert ist, kann ein Profil mehrmals in eine Journey eintreten, aber erst dann, wenn es aus der vorherigen Instanz der Journey vollständig ausgetreten ist.

* Wenn der erneute Eintritt deaktiviert ist, kann ein Profil nicht mehrmals in dieselbe Journey eintreten.

## Journey für Segmente lesen{#entry-read-segment}

In einer Journey mit dem Schritt „Segment lesen“ gilt Folgendes:

* Für nicht wiederkehrende Journeys: Das Profil tritt nur einmal in die Journey ein.

* Für wiederkehrende Journey: das Profil gibt bei jeder Wiederholung die Journey ein, wenn es sich im Segment-/Erwartungsstatus befindet. Wenn es sich noch in der Journey einer früheren Wiederholung befindet, fängt es wieder von vorne an.

Bei Geschäftsereignissen beginnen Journey mit einer **Segment lesen** Aktivität: Da diese Journey auf dem Empfang eines Geschäftsereignisses basiert, wird, wenn das Profil im erwarteten Segment qualifiziert ist, für jedes empfangene Geschäftsereignis die Journey angegeben. Dies bedeutet, dass dieses Profil mehrere Male in derselben Journey, aber gleichzeitig im Kontext verschiedener Geschäftsereignisse sein kann.
