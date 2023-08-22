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
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 100%

---


# Profileintritt-Verwaltung {#entry-management}

Es gibt zwei Hauptarten von Journeys:

* ereignisbasierte Journeys: Diese Journeys, die mit einem Ereignis beginnen, sind einheitlich und mit einem Kontakt verknüpft. Wenn das Ereignis empfangen wird, tritt der Kontakt in die Journey ein. [Weitere Informationen](#entry-unitary)
* Zielgruppe-lesen-Journeys: Diese Journeys, die mit dem Lesen einer Zielgruppe beginnen, sind Batch-Journeys. Kontakte, die zur Zielgruppe gehören, treten alle in dieselbe Journey ein. Diese Journeys können wiederkehrend oder einmalig sein. [Weitere Informationen](#entry-read-segment)

In den meisten Fällen kann ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey vorhanden sein.

## Einheitliche Journeys{#entry-unitary}

In einheitlichen Journey können Sie den Wiedereintritt aktivieren oder deaktivieren:

* Wenn der erneute Eintritt aktiviert ist, kann ein Profil mehrmals in eine Journey eintreten, aber erst dann, wenn es aus der vorherigen Instanz der Journey vollständig ausgetreten ist.

* Wenn der erneute Eintritt deaktiviert ist, kann ein Profil nicht mehrmals in dieselbe Journey eintreten.

Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die Option für „einmalige“ Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt. In diesem Fall möchten Sie nicht, dass der Kunde die Journey erneut betreten und das Angebot erneut wahrnehmen kann. Wenn eine Journey beendet wird, lautet ihr Status **[!UICONTROL Geschlossen]**. Neue Kontakte können nicht mehr in die Journey eintreten. Personen, die sich bereits in der Journey befinden, beenden die Journey wie gewohnt. [Weitere Informationen](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

Nach der standardmäßigen globalen maximalen Wartezeit von 30 Tagen wird der Status der Journey in **Beendet** geändert. Neue Kontakte können nicht mehr in die Journey eintreten. Personen, die sich bereits in der Journey befinden, beenden die Journey normal. Aufgrund des 30-tägigen Journey-Timeouts, wenn der erneute Eintritt in die Journey nicht erlaubt ist, können wir nicht sicherstellen, dass die Sperrung des Wiedereintritts mehr als 30 Tage dauert. Da wir alle Informationen über Personen, die an der Journey teilgenommen haben, 30 Tage nach deren Eintritt entfernen, können wir nicht wissen, dass die Person vor mehr als 30 Tagen bereits Eintritt hatte. [Weitere Informationen](journey-gs.md#global_timeout).

Unitäre Journeys (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung) enthalten einen Schutzmechanismus, der verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.

Der Schlüssel wird auch verwendet, um zu überprüfen, ob sich eine Person in einer Journey befindet. Eine Person kann nicht an zwei verschiedenen Stellen in derselben Journey sein. Das System lässt daher nicht zu, dass sich derselbe Schlüssel, z. B. der Schlüssel CRMID=3224, an verschiedenen Stellen in derselben Journey befindet.

## „Zielgruppe lesen“-Journeys{#entry-read-segment}

Bei einer „Zielgruppe lesen“-Journey gilt Folgendes:

* Für nicht wiederkehrende Journeys: Das Profil tritt nur einmal in die Journey ein.

* Für wiederkehrende Journeys: Standardmäßig treten bei jeder Wiederholung alle Profile der Zielgruppe in die Journey ein. Sie müssen die Journey beenden, bevor sie in einer anderen Instanz wieder eintreten können.

>[!NOTE]
>
>Für wiederkehrende Zielgruppe-lesen-Journeys stehen zwei Optionen zur Verfügung. Die Option **Erneuten Eintritt bei Wiederholung erzwingen** bewirkt, dass alle noch in der Journey vorhandenen Profile die Journey bei der nächsten Ausführung automatisch verlassen. Die Option **Inkrementelles Lesen** zielt nur auf die Kontakte ab, die seit der letzten Ausführung der Journey der Zielgruppe beigetreten sind. Siehe diesen [Abschnitt](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

Bei Geschäftsereignis-Journeys, die mit der Aktivität **Zielgruppe lesen** beginnen: Da diese Journey auf dem Empfang eines Geschäftsereignisses basiert, tritt das Profil, wenn es für die erwartete Zielgruppe qualifiziert ist, bei jedem empfangenen Geschäftsereignis in die Journey ein. Dies bedeutet, dass dieses Profil gleichzeitig mehrfach in derselben Journey sein kann, jedoch dann im Kontext verschiedener Geschäftsereignisse.