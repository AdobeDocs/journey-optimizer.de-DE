---
solution: Journey Optimizer
product: journey optimizer
title: Pausieren einer Journey
description: Weitere Informationen zum Pausieren und Fortsetzen einer Live-Journey
feature: Journeys
role: User
level: Intermediate
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
keywords: veröffentlichen, Journey, live, Gültigkeit, prüfen
exl-id: a2892f0a-5407-497c-97af-927de81055ac
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '2106'
ht-degree: 28%

---

# Pausieren einer Journey {#journey-pause}

>[!CONTEXTUALHELP]
>id="ajo_journey_pause"
>title="Journey anhalten"
>abstract="Live-Journey anhalten, um den Eintritt neuer Profile zu verhindern. Wählen Sie aus, ob die aktuell auf der Journey befindlichen Profile verworfen oder beibehalten werden sollen. Wird sie beibehalten, wird die Ausführung bei der nächsten Aktionsaktivität fortgesetzt, sobald die Journey neu gestartet wird. Perfekt für Updates oder Notstopps, ohne den Fortschritt zu verlieren."

Sie können Ihre Live-Journeys pausieren, um alle erforderlichen Änderungen vorzunehmen, und danach jederzeit wieder fortsetzen.<!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Während der Pause können sie [globale Filter anwenden](#journey-global-filters), um Profile basierend auf ihren Attributen auszuschließen. Die Journey wird nach Ablauf des Pausierungszeitraums automatisch fortgesetzt. Sie kann auch [manuell fortgesetzt werden](#journey-resume-steps).

>[!AVAILABILITY]
>
>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.


## Wichtigste Vorteile {#journey-pause-benefits}

Das Pausieren und Fortsetzen von Journeys gibt Journey-Anwendenden mehr Kontrolle und Flexibilität, da Live-Journeys vorübergehend ausgesetzt werden können, ohne das Kundenerlebnis zu stören. Während der Pause werden keine Nachrichten gesendet und die Profile verbleiben in einem ausgesetzten Zustand, bis die Journey fortgesetzt wird.

Diese Funktion reduziert das Risiko des Versands unbeabsichtigter Nachrichten bei Fehlern oder Updates (z. B. bei Änderungen des Nachrichteninhalts), unterstützt höhere Sicherheit beim Journey-Management und erhöht das Vertrauen der Anwendenden. Durch die Sichtbarkeit pausierter Journeys und deren Status direkt in der Benutzeroberfläche werden die Transparenz und die betriebliche Agilität weiter erhöht.

>[!CAUTION]
>
>* Die Berechtigungen zum Pausieren und Fortsetzen von Journeys sind auf Benutzende mit der Berechtigung **[!DNL Publish journeys]** auf hoher Ebene beschränkt. Weitere Informationen zur Verwaltung der Zugriffsrechte für [!DNL Journey Optimizer]-Benutzende finden Sie in [diesem Abschnitt](../administration/permissions-overview.md).
>
>* Bevor Sie mit der Pause/Wiederaufnahme-Funktion beginnen[ lesen Sie die Leitplanken und Einschränkungen ](#journey-pause-guardrails).


## Pausieren einer Journey {#journey-pause-steps}

Jede **Live**-Journey kann pausiert werden.

Gehen Sie wie folgt vor, um diese Journey zu pausieren:

1. Öffnen Sie die zu pausierende Journey.
1. Klicken Sie auf die Schaltfläche **…** oben rechts auf der Journey-Arbeitsfläche und wählen Sie **Pause**.

   ![Schaltfläche zum Pausieren der Journey](assets/pause-journey-button.png)

1. Wählen Sie aus, wie Profile verwaltet werden sollen, die sich derzeit auf der Journey befinden.

   ![Pausieren von Journey-Optionen](assets/pause-confirm.png){width="50%" align="left"}

   Sie haben folgende Möglichkeiten:

   * **Hold** profiles - Profile warten auf dem nächsten **Action** Knoten, bis die Journey fortgesetzt wird
   * **Verwerfen** Profile - Profile werden beim nächsten **Action“-** aus dem Journey ausgeschlossen

1. Klicken Sie zur Bestätigung auf die Schaltfläche **Anhalten**.

In der Liste der Journeys können eine oder mehrere **Live**-Journeys pausiert werden. Wählen Sie zum Pausieren einer Gruppe von Journeys (_Massenpause_) die Journeys in der Liste aus und klicken Sie auf die Schaltfläche **Anhalten** in der blauen Leiste am unteren Bildschirmrand. Die Schaltfläche **Anhalten** ist nur verfügbar, wenn **Live**-Journeys ausgewählt sind.

![Massenpause von zwei Live-Journeys über die untere Leiste](assets/bulk-pause-journeys.png)

### Verhalten bei pausierten Journey

Wenn eine Journey angehalten wird, werden neue Eingänge unabhängig vom Halten-/Verwerfen-Modus immer verworfen.

Wenn ein Journey angehalten wird, hängt die Profilverwaltung und Aktivitätsausführung von der Aktivität ab. Die Verhaltensweisen werden im Folgenden beschrieben. Ein vollständiges Verständnis finden Sie auch in diesem [End-to-End-Beispiel](#journey-pause-sample).


| Journey-Aktivität | Wenn die Journey pausiert |
|-------------------------|--------------------------------------------------|
| [Zielgruppen-Qualifizierung](audience-qualification-events.md) | <ul> <li>Am ersten Knoten auf der Arbeitsfläche: Jede Profilqualifizierung für die Zielgruppe wird verworfen </li><li>In anderen Knoten: Dasselbe Verhalten wie bei einer Live-Journey. Wenn die Zielgruppen-Qualifizierung jedoch nach einer <strong>Action</strong>-Aktivität erfolgt und der/die Benutzende bei dieser Aktion angehalten wird, wird die Zielgruppen-Qualifizierung verworfen. </li></ul> |
| [Unitäres Ereignis](general-events.md) | <ul> <li>Am ersten Knoten auf der Arbeitsfläche: Das Ereignis wird verworfen</li><li>In anderen Knoten: Dasselbe Verhalten wie bei einer Live-Journey. Wenn das Ereignis jedoch nach einer <strong>Action</strong>-Aktivität eintritt und der/die Benutzende bei dieser Aktion angehalten wird, wird das Ereignis verworfen. </li></ul> |
| [Zielgruppe lesen](read-audience.md) | Dasselbe Verhalten wie bei einer Live-Journey mit einigen Besonderheiten: <ol> <li> Wenn <strong>Pause</strong> nach dem Start der Aktivität <strong>Zielgruppe lesen</strong> gedrückt wurde, werden Profile, die auf die Journey gelangt sind, fortgesetzt (bis zur nächsten Aktivität <strong>Aktion</strong>). Wenn Journey Zielgruppen mit einer bestimmten Geschwindigkeit liest und die vollständige Zielgruppe noch nicht eingegeben wurde, werden die verbleibenden Profile in der Warteschlange verworfen.</li><li> Bei einzelnen Ausführungen: Zum Zeitpunkt der Wiederaufnahme wird kein Fehler angezeigt, wenn das geplante Datum vor dem Wiederaufnahme-Datum lag. Dieser Zeitplan würde ignoriert.</li><li>Für inkrementelle Journey: <ul><li>Wenn die Aktion vor dem ersten Vorkommen angehalten wird, wird bei der Wiederaufnahme die vollständige Audience abgespielt. </li><li>Wenn das Anhalten beispielsweise am 4. Tag eines täglichen Wiederholungszeitraums stattfindet und das Journey bis zum 9. Tag angehalten bleibt, werden bei der Wiederaufnahme alle Profile einbezogen, die vom 4. bis 9. eingetreten sind  </li></ul></ol> |
| [Reaktion](reaction-events.md) | Dasselbe Verhalten wie bei einer Live-Journey. Wenn die Reaktion jedoch nach einer <strong>Action</strong>-Aktivität erfolgt und der Benutzer bei dieser Aktion angehalten wird, wird das Reaktionsereignis verworfen. |
| [Warten](wait-activity.md) | Gleiches Verhalten wie bei einer Live-Journey |
| [Bedingung](condition-activity.md) | Gleiches Verhalten wie bei einer Live-Journey |
| [Inhaltsentscheidung](content-decision.md) | Profile werden basierend auf der Auswahl der Benutzerin bzw. des Benutzers nach dem Anhalten des Journey geparkt oder verworfen |
| [Kanalaktion](journeys-message.md) | Profile werden basierend auf der Auswahl der Benutzerin bzw. des Benutzers nach dem Anhalten des Journey geparkt oder verworfen |
| [Benutzerdefinierte Aktion](../action/action.md) | Profile werden basierend auf der Auswahl der Benutzerin bzw. des Benutzers nach dem Anhalten des Journey geparkt oder verworfen |
| [Profil aktualisieren](update-profiles.md) und [springen](jump.md) | Gleiches Verhalten wie bei einer Live-Journey |
| [Externe Daten - Source](../datasource/external-data-sources.md) | Gleiches Verhalten wie bei einer Live-Journey |
| [Ausstiegskriterien](journey-properties.md#exit-criteria) | Gleiches Verhalten wie bei einer Live-Journey |

## Fortsetzen pausierter Journeys {#journey-resume-steps}

>[!CONTEXTUALHELP]
>id="ajo_journey_resume"
>title="Journey fortsetzen"
>abstract="Setzt eine pausierte Journey fort, damit neue Profile erneut eintreten können. Wenn Profile während der Pause gewartet haben, setzen sie ihren Journey fort. Ideal zum sicheren Neustart von Journey nach Updates oder Pausen."

Pausierte Journeys werden nach Ablauf des maximalen Pausierungszeitraums von 14 Tagen automatisch fortgesetzt. Sie können jederzeit manuell fortgesetzt werden. Eine angehaltene Journey fortsetzen, damit neue Profile erneut eintreten können. Wenn Profile während der Pause gewartet haben, setzen sie ihren Journey fort. Ideal zum sicheren Neustart von Journey nach Updates oder Pausen.

Mit den folgenden Schritten wird eine pausierte Journey fortgesetzt und Journey-Ereignisse werden wieder überwacht:

1. Öffnen Sie die Journey, die fortgesetzt werden soll.
1. Klicken Sie auf die Schaltfläche **…** oben rechts auf der Journey-Arbeitsfläche und **Fortsetzen**.

   Die Journey wechselt in den Status **Wird fortgesetzt**. Wenn die Journey fortgesetzt wird, beginnen innerhalb einer Minute neue Eintritte. Das Fortsetzen von gespeicherten Profilen kann einige Zeit in Anspruch nehmen - Profile werden mit einer 5.000-Bit-Rate wieder aufgenommen.  Da alle Profile erneut aufgenommen werden müssen, damit die Journey wieder **Live** ist, kann der Übergang vom **Wiederaufnahme** zum **Live**-Status einige Zeit dauern.

1. Klicken Sie zur Bestätigung auf die Schaltfläche **Fortsetzen**.


Aus der Liste der Journeys können eine oder mehrere **pausierte** Journeys fortgesetzt werden. Um eine Gruppe von Journeys fortzusetzen (_Massenfortsetzung_), wählen Sie diese aus und klicken Sie auf die Schaltfläche **Fortsetzen** in der blauen Leiste am unteren Bildschirmrand. Beachten Sie, dass die Schaltfläche **Fortsetzen** nur verfügbar ist, wenn **pausierte** Journeys ausgewählt sind.


## Anwenden eines globalen Filters auf Profile in einer pausierten Journey {#journey-global-filters}

Wenn eine Journey pausiert ist, kann ein globaler Filter basierend auf Profilattributen angewendet werden. Dieser Filter ermöglicht den Ausschluss von Profilen, die zum Zeitpunkt der Fortsetzung dem definierten Ausdruck entsprechen. Sobald der globale Filter festgelegt ist, wird er auf Aktionsknoten erzwungen, auch für den Eintritt neuer Profile. Bestehende Profile, die den Kriterien entsprechen, und neue Profile, die auf die Journey zugreifen, werden von der Journey ausgeschlossen **beim nächsten**).

Gehen Sie wie folgt vor, um beispielsweise alle französischen Kunden von einer angehaltenen Journey auszuschließen:

1. Navigieren Sie zur pausierten Journey, die geändert werden soll.

1. Wählen Sie das Symbol **Ausstiegskriterien und globaler Filter** aus.

   ![Hinzufügen eines globalen Filters zu einer pausierten Journey](assets/add-global-filter.png)

1. Klicken Sie in den **Ausstiegskriterien und globaler Filter** Einstellungen auf **Globalen Filter hinzufügen** um einen Filter basierend auf Profilattributen zu definieren.

1. Legen Sie den Ausdruck zum Ausschluss von Profilen fest, deren Länderattribut gleich Frankreich ist.

   ![Hinzufügen eines globalen Filters zu einer pausierten Journey](assets/add-country-filter.png)

1. Speichern Sie den Filter und klicken Sie auf **Journey aktualisieren**, um die Änderungen anzuwenden.

1. [Fortsetzen der Journey](#journey-resume-steps)

   Bei der Wiederaufnahme werden alle Profile mit dem Länderattribut Frankreich beim nächsten Aktionsknoten automatisch von der Journey ausgeschlossen. Alle neuen Profile mit dem Länderattribut Frankreich, die versuchen, auf die Journey zuzugreifen, werden ebenfalls beim nächsten Aktionsknoten blockiert.

Profilausschlüsse für Profile, die sich derzeit in der Journey befinden, und für neue Profile treten nur auf, wenn sie einen Aktionsknoten erreichen.

>[!CAUTION]
>
>* Es kann nur **ein** globaler Filter pro Journey festgelegt werden.
>
>* Ein globaler Filter kann nur in Journeys erstellt, aktualisiert oder gelöscht werden, die **Pausiert** sind.

## Schutzmechanismen und Einschränkungen {#journey-pause-guardrails}

* Eine Journey-Version kann bis zu **14 Tage lang angehalten werden** wobei in pausierten Journey in Ihrem Unternehmen maximal **10 Millionen** zulässig sind.
Diese Begrenzung wird alle 30 Minuten überprüft. Dies bedeutet, dass Sie den Schwellenwert von 10 Millionen möglicherweise vorübergehend überschreiten. Sobald das System ihn jedoch erkennt, werden alle zusätzlichen Profile automatisch verworfen.

  Wenn Sie die Journey fortsetzen, um die Anzahl der gespeicherten Profile wieder unter das Limit zu bringen, wird die Journey sofort fortgesetzt - es kann jedoch bis zu 30 Minuten dauern, bis die Profilanzahl aktualisiert wird. Während dieser Zeit kann das System diese Profile immer noch als angehalten betrachten.

* Anhaltende Journey werden auf das Live-Journey-Kontingent angerechnet
* Profile, die auf Journey zugegriffen haben, aber während der Pause verworfen wurden, werden weiterhin als kontaktierbare Profile gezählt
* Anhaltende Journey werden in allen Geschäftsregeln berücksichtigt, genauso wie wenn sie live wären
* Das maximale globale Journey-Timeout gilt weiterhin für pausierte Journeys. Wenn sich beispielsweise ein Profil 90 Tage lang auf einer Journey befand und die Journey angehalten wurde, verlässt dieses Profil die Journey am 91. Tag weiterhin
* Profile werden **angehaltenem Journey** verworfen), wenn sie eine Aktionsaktivität erreichen. Wenn sie während der Zeit, in der eine Journey angehalten wird, auf Wartezeit bleiben und diese Wartezeit nach der Wiederaufnahme beenden, setzen sie die Journey fort und werden nicht verworfen. [Siehe das End-to-End-Beispiel](#journey-pause-sample)
* Da weiterhin Ereignisse verarbeitet werden, werden diese Ereignisse auch nach der Pause auf die Anzahl der Journey-Ereignisse pro Sekunde angerechnet, nach denen eine Drosselung für unitäres Ereignis eintreten kann
* Wenn Profile in einer pausierten Journey enthalten sind, werden bei der Fortsetzung Profilattribute aktualisiert
* In angehaltenen Journey werden weiterhin Bedingungen ausgeführt. Wenn ein Journey aufgrund von Datenqualitätsproblemen angehalten wurde, kann jede Bedingung vor einem Aktionsknoten mit falschen Daten ausgewertet werden
* Bei Journey-**, die auf einer inkrementellen Zielgruppe** Zielgruppe lesen), wird die Pausendauer berücksichtigt. Dies ist bei der Zielgruppen-Qualifizierung oder ereignisbasierten Journey nicht der Fall (wenn während einer Pause eine Zielgruppen-Qualifizierung oder ein Ereignis empfangen wird und es sich um die erste Aktivität auf der Journey handelt, werden diese Ereignisse verworfen)
* Wenn Profile in einer Journey enthalten sind und diese Journey nach einigen Tagen automatisch fortgesetzt wird, setzen Profile die Journey fort und scheiden nicht aus ihr aus. Wenn Sie sie fallen lassen wollen, müssen Sie die Journey stoppen
* In ausgesetzten Journey werden Warnhinweise nicht für [Batch-Segmentwarnungen](../reports/alerts.md#alert-read-audiences) ausgelöst
* Es gibt keine Auditprotokolle im System, wenn nach 14 Tagen der Pausenstatus der Journey beendet wird
* Einige verworfene Profile können im Journey-Schrittereignis, aber nicht im Bericht angezeigt werden. z. B.:
   * Geschäftsereignisse für „Zielgruppe **&quot;**
   * **Zielgruppe lesen** Aufträge werden aufgrund eines angehaltenen Journey verworfen
   * Verworfene Ereignisse, wenn die **Ereignis**-Aktivität nach einer Aktion stattfand, bei der das Profil wartete
     <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## End-to-End-Beispiel {#journey-pause-sample}

Nehmen wir als Beispiel die folgende Journey:

![Beispiel einer Journey](assets/pause-journey-sample.png){zoomable="yes"}

Wenn Sie diese Journey anhalten, wählen Sie aus, ob **Profile** oder **Halten** werden sollen. Anschließend erfolgt die Profilverwaltung wie folgt:

1. **AddToCart**-Aktivität: Alle neuen Profileintritte sind blockiert. Wenn ein Profil bereits vor einer Pause auf die Journey zugegriffen hat, fährt es mit dem nächsten Aktionsknoten fort.
1. **Warten**-Aktivität: Profile warten weiterhin normal auf dem Knoten und werden ihn beenden, auch wenn die Journey angehalten wird.
1. **Bedingung**: Profile durchlaufen weiterhin Bedingungen und wechseln je nach dem in der Bedingung definierten Ausdruck in den rechten Zweig.
1. **Push**/**Email**-Aktivitäten: Während eines angehaltenen Journey beginnen Profile zu warten oder werden (basierend auf der Auswahl, die der Benutzer zum Zeitpunkt der Pause getroffen hat) auf dem nächsten Aktionsknoten verworfen. Profile warten also ab oder werden dort verworfen.
1. **Ereignisse** nach **Action**-Knoten: Wenn ein Profil auf einem **Action**-Knoten wartet und danach eine **Event**-Aktivität vorhanden ist, wird das Profil verworfen, wenn dieses Ereignis ausgelöst wird.

Entsprechend diesem Verhalten können Sie sehen, dass die Profilnummern bei pausiertem Journey zunehmen, hauptsächlich in Aktivitäten vor **Action**-Aktivitäten. In diesem Beispiel ist die Aktivität **Warten** weiterhin aktiviert, wodurch die Anzahl der Profile, die die Aktivität **Bedingung** durchlaufen, beim Verlassen dieser Aktivität steigt.

Wenn Sie diese Journey fortsetzen:

1. Neue Journey-Eintritte beginnen innerhalb einer Minute.
1. Profile, die derzeit auf der Journey auf **Action**-Aktivitäten warteten, werden mit einer 5.000-Bit-Rate wieder aufgenommen. Sie können dann die **Aktion**, auf die sie gewartet haben, eingeben und die Journey fortsetzen.
