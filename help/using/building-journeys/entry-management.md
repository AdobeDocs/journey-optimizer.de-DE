---
solution: Journey Optimizer
product: journey optimizer
title: Profileintritt-Verwaltung
description: Verwaltung des Profileintritts
feature: Journeys
role: User
level: Intermediate
keywords: Wiedereintritt, Journey, Profil, wiederkehrend
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: deb3646235377bf48b91b019e3442e4a3d6f0cf8
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 70%

---

# Profileintritt-Verwaltung {#entry-management}

Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die Option für „einmalige“ Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt. In diesem Fall möchten Sie nicht, dass der Kunde die Journey erneut betreten und das Angebot erneut wahrnehmen kann.

![](assets/journey-re-entrance.png)

Wenn eine Journey beendet wird, lautet ihr Status **[!UICONTROL Geschlossen]**. Neue Personen können nicht mehr in die Journey eintreten. Personen, die sich bereits in der Journey befinden, beenden die Journey wie gewohnt.

Nach der standardmäßigen globalen maximalen Wartezeit von 30 Tagen wird der Status der Journey in **Beendet** geändert.  [Weitere Informationen](journey-gs.md#global_timeout).


## Einheitliche Journeys{#entry-unitary}

Einzelne Journeys (beginnend mit einem Ereignis oder einer Segmentqualifikation) enthalten eine Schutzmaßnahme, die verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.

Zusätzlich:

* Wenn der erneute Eintritt aktiviert ist, kann ein Profil mehrmals in eine Journey eintreten, aber erst dann, wenn es aus der vorherigen Instanz der Journey vollständig ausgetreten ist.

* Wenn der erneute Eintritt deaktiviert ist, kann ein Profil nicht mehrmals in dieselbe Journey eintreten.

## Journeys für „Segment lesen“{#entry-read-segment}

In einer Journey mit dem Schritt „Segment lesen“ gilt Folgendes:

* Für nicht wiederkehrende Journeys: Das Profil tritt nur einmal in die Journey ein.

* Für wiederkehrende Journey: das Profil gibt bei jeder Wiederholung die Journey ein, wenn es sich im Segment-/erwarteten Status befindet. Wenn sie sich noch von einer vorherigen Wiederholung auf der Journey befanden, werden sie von Anfang an neu gestartet.

Bei Geschäftsereignissen beginnen Journey mit einer **Segment lesen** Aktivität: Da diese Journey auf dem Empfang eines Geschäftsereignisses basiert, wird, wenn das Profil im erwarteten Segment qualifiziert ist, für jedes empfangene Geschäftsereignis die Journey erfasst, d. h., dieses Profil kann mehrere Male in derselben Journey, aber gleichzeitig im Kontext verschiedener Geschäftsereignisse sein.