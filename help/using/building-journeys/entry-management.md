---
solution: Journey Optimizer
product: journey optimizer
title: Profileintragsverwaltung
description: Erfahren Sie, wie Sie die Profileingabe verwalten
feature: Journeys
role: User
level: Intermediate
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 95%

---

# Profileintragsverwaltung {#entry-management}

In einer unitären Journey gilt folgendes:

* Wenn der erneute Eintritt aktiviert ist, kann ein Profil mehrmals in eine Journey eintreten, aber erst dann, wenn es aus der vorherigen Instanz der Journey vollständig ausgetreten ist.

* Wenn der erneute Eintritt deaktiviert ist, kann ein Profil nicht mehrmals in dieselbe Journey eintreten.

Weiterführende Informationen zum erneuten Eintreten von Profilen finden Sie in [diesem Abschnitt](../building-journeys/journey-gs.md#change-properties).

In einer Journey mit dem Schritt „Segment lesen“ gilt Folgendes:

* Für nicht wiederkehrende Journeys: Das Profil tritt nur einmal in die Journey ein.
* für wiederkehrende Journeys: Das Profil tritt bei jeder Wiederholung in die Journey ein, wenn es sich im Segment / im erwarteten Status befindet. Wenn es sich noch in der Journey einer früheren Wiederholung befindet, fängt es wieder von vorne an.

Bei Journeys mit Geschäftsereignissen, die mit dem Schritt „Segment lesen“ beginnen, gilt Folgendes:

Da diese Journey auf dem Empfang eines Geschäftsereignisses basiert, tritt das Profil, wenn es im erwarteten Segment ist, bei jedem empfangenen Geschäftsereignis in die Journey ein. Dies bedeutet, dass dieses Profil gleichzeitig mehrfach in derselben Journey sein kann, aber im Kontext verschiedener Geschäftsereignisse.

Einzelne Journeys (beginnend mit einem Ereignis oder einer Segmentqualifikation) enthalten eine Schutzvorkehrung, die verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.
