---
solution: Journey Optimizer
product: journey optimizer
title: Profileintritt-Verwaltung
description: Verwaltung des Profileintritts
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: Wiedereintritt, Journey, Profil, wiederkehrend
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: a2e4a6c15ea9e6a96544eaa8f58dc0cd55854bbe
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---


# Profileintrittsverwaltung {#entry-management}

Die Profileintrittsverwaltung hängt vom Typ der Journey ab. 

## Journey-Typen {#types-of-journeys}

Mit Adobe Journey Optimizer können Sie die folgenden Journey-Typen erstellen:

* Journeys vom Typ **Unitäres Ereignis**: Diese Journeys beginnen mit einem unitären Ereignis. Wenn das Ereignis empfangen wird, tritt das verknüpfte Profil in die Journey ein. [Weitere Informationen](#entry-unitary)

* Journeys vom Typ **Geschäftsereignis**: Diese Journeys beginnen mit einem Geschäftsereignis, unmittelbar gefolgt von einer Aktivität **Zielgruppe lesen**. Nach Empfang des Ereignisses treten die der angegebenen Zielgruppe angehörenden Profile in die Journey ein.  Für jedes Profil wird eine Instanz dieser Journey erstellt. [Weitere Informationen](#entry-business)

* Journeys vom Typ **Zielgruppe lesen**: Diese Journeys beginnen mit einer Aktivität **Zielgruppe lesen**. Wenn die Journey ausgeführt wird, treten die der angegebenen Zielgruppe angehörenden Profile in die Journey ein. Für jedes Profil wird eine Instanz dieser Journey erstellt. Diese Journeys können wiederkehrend oder einmalig sein. [Weitere Informationen](#entry-read-audience)

* **Zielgruppen-Qualifizierungs**-Journeys: Diese Journeys beginnen mit einem Zielgruppen-Qualifizierungsereignis. Diese Journeys überwachen die Ein- und Austritte von Profilen in Zielgruppen. In diesem Fall tritt das verknüpfte Profil die Journey ein. [Weitere Informationen](#entry-unitary)

Für alle Journey-Typen gilt, dass ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey für alle aktiven [Journey-Versionen](publishing-the-journey.md#journey-versions-journey-versions) vorhanden sein kann. Um zu überprüfen, ob sich eine Person in einer Journey befindet, wird die Profilidentität als Schlüssel verwendet. Das System lässt nicht zu, dass sich derselbe Schlüssel, z. B. der Schlüssel `CRMID=3224`, an verschiedenen Stellen in derselben Journey befindet.

## Journeys für unitäre Ereignisse und Zielgruppen-Qualifizierungen{#entry-unitary}

In den Journeys **Unitäre Ereignisse** und **Zielgruppenqualifikation** können Sie den erneuten Eintritt aktivieren oder deaktivieren:

* Wenn der erneute Eintritt aktiviert ist, kann ein Profil mehrmals in eine Journey eintreten, aber erst dann, wenn es aus der vorherigen Instanz der Journey vollständig ausgetreten ist.

* Wenn der erneute Eintritt deaktiviert ist, kann ein Profil nicht mehrmals innerhalb des globalen Journey-Timeout-Zeitraums in dieselbe Journey eintreten.  Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/journey-properties.md#global_timeout).

Standardmäßig ist bei Journeys der erneute Eintritt erlaubt. Wenn die Option **Erneuten Eintritt erlauben** aktiviert ist, wird das Feld **Wartezeit bis zum erneuten Eintritt** angezeigt. Damit können Sie die Wartezeit definieren, bevor ein Profil erneut in die Journey eintreten kann.  Dadurch wird verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Standardmäßig ist das Feld auf 5 Minuten eingestellt. Die maximale Wartezeit beträgt 91 Tage ([maximale globale Wartezeit](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

Nach dem Zeitraum für den erneuten Eintritt können Profile erneut in die Journey eintreten. Um dies zu vermeiden und den erneuten Eintritt für diese Profile vollständig zu deaktivieren, können Sie eine Bedingung hinzufügen, um anhand von Profil- oder Zielgruppendaten zu testen, ob das Profil bereits eingetreten ist oder nicht.

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## Geschäfts-Journeys {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

Um in **Geschäfts-Journeys** mehrere Ausführungen für Geschäftsereignisse zuzulassen, aktivieren Sie die entsprechende Option im Abschnitt **[!UICONTROL Ausführung]** der Journey-Eigenschaften.

![](assets/business-entry.png)

Im Falle von Geschäftsereignissen werden für eine bestimmte Journey die bei der ersten Ausführung abgerufenen Zielgruppendaten innerhalb eines Zeitfensters von einer Stunde wiederverwendet.

Ein Profil kann mehrmals gleichzeitig in derselben Journey vorhanden sein, aber im Kontext verschiedener Geschäftsereignisse.

Weitere Informationen hierzu finden Sie in diesem [Abschnitt](../event/about-creating-business.md).

## „Zielgruppe lesen“-Journeys {#entry-read-audience}

**Zielgruppe-lesen**-Journeys können wiederkehrend oder einmalig sein:

* Für nicht wiederkehrende/einmalige Journeys: Das Profil tritt nur einmal in die Journey ein.

* Für wiederkehrende Journeys: Standardmäßig treten bei jeder Wiederholung alle Profile der Zielgruppe in die Journey ein. Sie müssen die Journey beenden, bevor sie in einer anderen Instanz wieder eintreten können.

Für wiederkehrende Journeys vom Typ „Zielgruppe lesen“ stehen verschiedene Optionen zur Verfügung. Weitere Informationen finden Sie im Abschnitt [Verwenden einer Zielgruppe in einer Journey](../building-journeys/read-audience.md).

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
