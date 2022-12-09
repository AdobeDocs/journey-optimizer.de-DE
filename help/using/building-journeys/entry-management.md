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
source-wordcount: '349'
ht-degree: 0%

---

# Profileintragsverwaltung {#entry-management}

Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die Option für &quot;einmalige&quot;Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt. In diesem Fall möchten Sie nicht, dass der Kunde erneut in die Journey eintreten und das Angebot erneut erhalten kann.

![](assets/journey-re-entrance.png)

Wenn eine Journey endet, lautet ihr Status **[!UICONTROL Closed]**. Neue Personen können nicht mehr in die Journey eintreten. Personen, die sich bereits in der Journey befinden, beenden die Journey normal.

Nach der standardmäßigen globalen Zeitüberschreitung von 30 Tagen wechselt die Journey zum **Abgeschlossen** Status.  [Weitere Infos](journey-gs.md#global_timeout).


## Einzelne Journeys{#entry-unitary}

Einzelne Journeys (beginnend mit einem Ereignis oder einer Segmentqualifikation) enthalten eine Schutzmaßnahme, die verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Eintritt in das Profil wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis eine Journey um 12:01 Uhr für ein bestimmtes Profil auslöst und ein anderes um 12:03 Uhr eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), startet die Journey für dieses Profil nicht erneut.

Zusätzlich:

* Wenn der erneute Eintritt aktiviert ist, kann ein Profil mehrmals in eine Journey eintreten, dies jedoch erst tun, wenn er die vorherige Instanz der Journey vollständig verlassen hat.

* Wenn der erneute Eintritt deaktiviert ist, kann ein Profil nicht mehrmals in dieselbe Journey eintreten

## Segmentreisen lesen{#entry-read-segment}

In einer Journey zum Lesen von Segmenten:

* Für nicht wiederkehrende Journeys: das Profil wird nur einmal und nur einmal in die Journey aufgenommen.

* Für wiederkehrende Journeys: das Profil wird bei jeder Wiederholung in die Journey geleitet, wenn es sich im Segment-/erwarteten Status befindet. Wenn er sich noch aus einer früheren Wiederholung in der Journey befand, wird er sie von Anfang an neu starten.

Bei Geschäftsereignis-Journeys, die mit einer **Segment lesen** Aktivität: Da er weiß, dass diese Journey auf dem Empfang eines Geschäftsereignisses basiert, wird er, wenn das Profil im erwarteten Segment qualifiziert ist, für jedes empfangene Geschäftsereignis in die Journey eintreten. Das bedeutet, dass dieses Profil mehrere Male in derselben Journey, gleichzeitig aber im Kontext verschiedener Geschäftsereignisse sein kann.
