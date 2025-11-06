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
version: Journey Orchestration
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 51%

---


# Profileintrittsverwaltung {#entry-management}

Die Profileintrittsverwaltung hängt vom Typ der Journey ab. 

## Journey-Typen {#types-of-journeys}

Mit Adobe Journey Optimizer können Sie die folgenden Journey-Typen erstellen:

* Journeys vom Typ **Unitäres Ereignis**: Diese Journeys beginnen mit einem unitären Ereignis. Wenn das Ereignis empfangen wird, tritt das verknüpfte Profil in die Journey ein. [Weitere Informationen](#entry-unitary)

* Journeys vom Typ **Geschäftsereignis**: Diese Journeys beginnen mit einem Geschäftsereignis, unmittelbar gefolgt von einer Aktivität **Zielgruppe lesen**. Nach Empfang des Ereignisses treten die der angegebenen Zielgruppe angehörenden Profile in die Journey ein.  Für jedes Profil wird eine Instanz dieser Journey erstellt. [Weitere Informationen](#entry-business)

* Journeys vom Typ **Zielgruppe lesen**: Diese Journeys beginnen mit einer Aktivität **Zielgruppe lesen**. Wenn die Journey ausgeführt wird, treten die der angegebenen Zielgruppe angehörenden Profile in die Journey ein. Für jedes Profil wird eine Instanz dieser Journey erstellt. Diese Journeys können wiederkehrend oder einmalig sein. [Weitere Informationen](#entry-read-audience)

* **Zielgruppen-Qualifizierungs**-Journeys: Diese Journeys beginnen mit einem Zielgruppen-Qualifizierungsereignis. Diese Journeys überwachen die Ein- und Austritte von Profilen in Zielgruppen. In diesem Fall tritt das verknüpfte Profil die Journey ein. [Weitere Informationen](#entry-unitary)

Für alle Journey-Typen gilt, dass ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey für alle aktiven [Journey-Versionen](publish-journey.md#journey-versions-journey-versions) vorhanden sein kann. Um zu überprüfen, ob sich eine Person in einer Journey befindet, wird die Profilidentität als Schlüssel verwendet. Das System lässt nicht zu, dass sich derselbe Schlüssel, z. B. der Schlüssel `CRMID=3224`, an verschiedenen Stellen in derselben Journey befindet.

## Journey-Verarbeitungsrate {#journey-processing-rate}

Die Journey-Verarbeitungsrate wird durch mehrere Faktoren beeinflusst, die bestimmen, wie Profile eine Journey durchlaufen:

### Profileintrittsrate {#profile-entrance-rate}

Wie Profile in Journey eintreten und wie hoch ihre erwartete Rate ausfällt, hängt von der ersten verwendeten Aktivität ab:

* **Zielgruppe lesen** Journey (Batch-Szenario, in dem Sie eine Zielgruppe von Profilen ansprechen und eine Journey für diese gesamte Zielgruppe Trigger haben): Der Maximalwert beträgt 20.000 TPS (Transaktionen pro Sekunde). Dies ist das auf einer **Sandbox-Ebene** verfügbare Kontingent. Wenn mehrere Journey auf dieser Sandbox gleichzeitig ausgeführt werden, sind 20.000 TPS möglicherweise nicht erreichbar. Betrachten Sie dieses Maximum als das beste Szenario.

* **Zielgruppenqualifizierung** Journey (Einzelszenario, in dem Sie eine Journey zum Trigger bringen möchten, wenn ein Profil für eine Streaming-Zielgruppe qualifiziert oder nicht qualifiziert ist): Der Maximalwert beträgt 5.000 TPS. Beachten Sie, dass es sich hierbei um ein freigegebenes Limit für Journey handelt, das mit Ereignissen beginnt. Außerdem ist es für alle Journey auf **Organisationsebene)**.

* **Unitäres Ereignis** Journey (unitäres Szenario, in dem Sie eine Journey zum Trigger bringen möchten, wenn ein Ereignis von einem Profil ausgegeben wird): Wie oben, beide verwenden dasselbe 5.000-TPS-Limit. Weitere Informationen zum Durchsatz beim Journey-Ereignis finden Sie in [diesem Abschnitt](../event/about-events.md#event-thoughput).

* **Geschäftsereignis** Journeys (das im Wesentlichen ein Unitär-Batch-Szenario ist, da ein Geschäftsereignis immer mit dem Schritt „Zielgruppe lesen“ gefolgt wird): Geschäftsereignisse zählen auch für das 5.000-TPS-Kontingent, aber die Aktivität „Zielgruppe lesen“ direkt danach hat dasselbe Limit wie Journeys, beginnend mit einer „Zielgruppe lesen“ (20.000 TPS).

### Veranstaltungen und Zielgruppenqualifikationen innerhalb der Journey {#events-inside-journeys}

Nach dem Eintritt können Sie Aktivitäten **Unitäres Ereignis** oder **Zielgruppen-Qualifizierung** innerhalb der Journey verwenden. Ein Profil kann in einen der vier oben beschriebenen Profiltypen eintreten und auf die Ausgabe eines Journey warten oder darauf warten, dass dieses Profil für eine Zielgruppe qualifiziert wird. Diese unitären Ereignisse und Zielgruppenqualifikationen werden für das oben beschriebene Kontingent gezählt. Beispiel: Wenn Sie eine Journey mit einer Lesekonferenz (mit maximal 20.000 TPS) starten und direkt danach ein Ereignis haben, beträgt dieses Ereignis maximal 5.000 TPS.

### Auswirkungen von Warteaktivitäten {#wait-activities-impact}

**Warten** Aktivitäten in Journey können sich auch darauf auswirken, wie viele Profile zu einem bestimmten Zeitpunkt durch einen Journey fließen. Normalerweise basiert eine Warteaktivität auf einer relativen Zeit (z. B.: Beenden 2 Stunden nach Eintritt in die Wartezeit, sodass nicht alle Profile gleichzeitig beendet werden). Wenn für diese Warteaktivität jedoch eine feste Zeit definiert ist, können mehrere Profile diese Journey exakt zur gleichen Zeit verlassen. Dies ist keine empfohlene Vorgehensweise. Es konnten enorme Mengen entdeckt werden, und der TPS-Wert kann ab diesem Zeitpunkt 20.000 TPS überschreiten.

### Aktionsaktivitäten {#action-activities-impact}

Schließlich können **action**-Aktivitäten (native Kanäle wie E-Mail, SMS, Push usw., Outbound oder Inbound, benutzerdefinierte Aktionen, Sprünge, die Profile an andere Journey senden, Aktualisierungsprofile, die Daten an den Unified Profile Service senden, usw.) durch die Profillast von Journey beeinflusst werden, aber auch die Verarbeitungsrate beeinflussen. Beispielsweise verlangsamt eine benutzerdefinierte Aktion, die auf einen externen Endpunkt mit einer hohen Antwortzeit abzielt, die Journey-Verarbeitungsrate.

Für benutzerdefinierte Aktionen beträgt die standardmäßige Begrenzung 300.000 Aufrufe pro Minute. Diese können mithilfe einer benutzerdefinierten Begrenzungsrichtlinie geändert werden. Weitere Informationen zur Begrenzung benutzerdefinierter Aktionen finden Sie in [diesem Abschnitt](../configuration/external-systems.md#capping).

## Journeys für unitäre Ereignisse und Zielgruppen-Qualifizierungen{#entry-unitary}

In den Journeys **Unitäre Ereignisse** und **Zielgruppenqualifizierung** können Sie den erneuten Eintritt aktivieren oder deaktivieren:

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
