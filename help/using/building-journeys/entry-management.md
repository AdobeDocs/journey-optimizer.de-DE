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
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 27%

---


# Profil-Eintrittsverwaltung {#entry-management}

Es gibt vier Arten von Journey:

* **Einzelereignis** Journey: Diese Journey beginnen mit einem Einzelereignis. Wenn das Ereignis empfangen wird, gibt das verknüpfte Profil die Journey ein. [Weitere Informationen](#entry-unitary)

* **Geschäftsereignis** Journey: Diese Journey beginnen mit einem Business-Ereignis, unmittelbar gefolgt von einer Read-Audience. Nach Empfang des Ereignisses werden die Profile der Zielgruppe in die Journey aufgenommen. Für jedes Profil wird eine Instanz dieser Journey erstellt. [Weitere Informationen](#entry-business)

* **Audience lesen** Journey: Diese Journey beginnen mit einer Audience lesen . Wenn die Journey ausgeführt wird, geben die Profile der jeweiligen Audience die Journey ein. Für jedes Profil wird eine Instanz dieser Journey erstellt. Diese Journeys können wiederkehrend oder einmalig sein. [Weitere Informationen](#entry-read-audience)

* **Zielgruppenqualifikation** Journey: Diese Journey beginnen mit einem Ereignis zur Zielgruppenqualifizierung. Diese Journey überwachen die Ein- und Austritte von Profilen in Zielgruppen. In diesem Fall gibt das verknüpfte Profil die Journey ein. [Weitere Informationen](#entry-unitary)

Bei allen Journey-Typen kann ein Profil nicht mehrmals im selben Journey vorhanden sein. Um zu überprüfen, ob sich eine Person auf einer Journey befindet, wird die Profilkennung als Schlüssel verwendet. Das System lässt nicht zu, dass sich derselbe Schlüssel, z. B. der Schlüssel CRMID=3224, an verschiedenen Stellen im selben Journey befindet.

## Journey für Einzelereignisse und Zielgruppenqualifizierung{#entry-unitary}

In den Journey &quot;Einzelereignisse&quot;und &quot;Zielgruppenqualifizierung&quot;können Sie den Wiedereintritt aktivieren oder deaktivieren:

* Wenn der erneute Eintritt aktiviert ist, kann ein Profil mehrmals eine Journey eingeben, dies aber erst tun, wenn er die vorherige Instanz der Journey vollständig verlassen hat.

* Wenn der erneute Eintritt deaktiviert ist, kann ein Profil innerhalb der globalen Journey-Timeout-Zeit nicht mehrmals dieselbe Journey eingeben. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/journey-gs.md#global_timeout).

Standardmäßig ist der erneute Eintritt in Journey zulässig. Wenn die Option **Erneuten Eintritt erlauben** aktiviert ist, wird das Feld **Wartezeit bis zum erneuten Eintritt** angezeigt. Damit können Sie die Wartezeit definieren, bevor ein Profil die Journey erneut aufrufen kann. Dadurch wird verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Standardmäßig ist das Feld auf 5 Minuten eingestellt. Die maximale Wartezeit beträgt 29 Tage.

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. [Learn more](journey-gs.md#entrance)
-->

![](assets/journey-re-entrance.png)

Nach dem erneuten Eintritt können Profile erneut in die Journey eintreten. Um dies zu vermeiden und den erneuten Eintritt für diese Profile vollständig zu deaktivieren, können Sie eine Bedingung hinzufügen, um anhand von Profil- oder Zielgruppendaten zu testen, ob das Profil bereits eingetreten ist oder nicht.

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. -->

## Journey für Unternehmen{#entry-business}

<!--
Business events follow re-entrance rules in the same way as for unitary events. If a journey allows re-entrance, the next business event will be processed.
-->

Um mehrere Ausführungen für Geschäftsereignisse zuzulassen, aktivieren Sie die entsprechende Option im Abschnitt **[!UICONTROL Ausführung]** der Journey-Eigenschaften.

![](assets/business-entry.png)

Bei Geschäftsereignissen werden die bei der ersten Ausführung abgerufenen Zielgruppendaten für eine bestimmte Journey innerhalb eines Zeitfensters von einer Stunde wiederverwendet.

Ein Profil kann mehrmals im selben Journey vorhanden sein, gleichzeitig aber im Kontext verschiedener Geschäftsereignisse.

Weiterführende Informationen dazu finden Sie in diesem Abschnitt [Abschnitt](../event/about-creating-business.md)

## „Zielgruppe lesen“-Journeys{#entry-read-audience}

Lesen Sie Audience-Journey können wiederkehrend oder einmalig sein:

* Für nicht wiederkehrende Journeys: Das Profil tritt nur einmal in die Journey ein.

* Für wiederkehrende Journey: Standardmäßig geben bei jeder Wiederholung alle Profile der Audience die Journey ein. Sie müssen die Journey beenden, bevor sie in einer anderen Instanz wieder eintreten können.

Für wiederkehrende Lesen der Audience-Journey stehen zwei Optionen zur Verfügung:

* Option **Inkrementelles Lesen**: Wenn eine Journey mit einer wiederkehrenden Aktion vom Typ **Zielgruppe lesen** zum ersten Mal ausgeführt wird, treten alle Profile in der Zielgruppe in die Journey ein. Mit dieser Option können Sie nach dem ersten Vorkommen nur die Kontakte auswählen, die seit der letzten Ausführung der Journey in die Audience eingestiegen sind.

* **Wiedereintritt erzwingen bei Wiederholung**: Mit dieser Option können Sie festlegen, dass alle noch in der Journey vorhandenen Profile bei der nächsten Ausführung automatisch beendet werden. Wenn die Lebensdauer Ihrer Profile in dieser Journey länger als die Häufigkeit der Wiederholungen sein kann (z. B. wenn Sie Warteaktivitäten verwenden), aktivieren Sie diese Option nicht, um sicherzustellen, dass Profile ihre Journey abschließen können.

![](assets/read-audience-options.png)

Weiterführende Informationen dazu finden Sie in diesem Abschnitt [Abschnitt](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

<!--
After 30 days, a Read audience journey switches to the **Finished** status. This behavior is set for 30 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 30 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
