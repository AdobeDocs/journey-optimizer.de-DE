---
solution: Journey Optimizer
product: journey optimizer
title: Journey anhalten
description: Erfahren Sie, wie Sie eine Live-Journey anhalten und fortsetzen können
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
keywords: veröffentlichen, Journey, live, Gültigkeit, prüfen
source-git-commit: cd85b58350b4f8829aa1bc925c151be9b061b170
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 6%

---

# Journey anhalten {#journey-pause}

Sie können Ihre Live-Journey anhalten, alle erforderlichen Änderungen vornehmen und sie jederzeit wieder aufnehmen. Eine Journey kann für maximal 14 Tage angehalten werden. Sie können auswählen, ob die Journey am Ende der Pausenzeit fortgesetzt wird oder ob sie vollständig beendet wird.


>[!AVAILABILITY]
>
>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.


## Wichtigste Vorteile {#journey-dry-run-benefits}

Durch das Anhalten und Fortsetzen von Journey erhalten Marketing-Fachleute mehr Kontrolle und Flexibilität, da Live-Journey vorübergehend ausgesetzt werden können, ohne das Kundenerlebnis zu beeinträchtigen. Wenn angehalten, werden keine Nachrichten gesendet und die Profile verbleiben in einem ausgesetzten Zustand, bis die Journey fortgesetzt wird.

Diese Funktion reduziert das Risiko des Versands unbeabsichtigter Nachrichten während Fehlern oder Updates (z. B. Änderung des Nachrichteninhalts), unterstützt ein sichereres Journey-Management und erhöht das Vertrauen der Anwender. Die Einblicke in pausierte Journey und deren Status direkt in der Benutzeroberfläche erhöhen die Transparenz und die betriebliche Agilität.

>[!CAUTION]
>
>Die Berechtigungen zum Anhalten und Fortsetzen von Journey sind auf Benutzende mit der Berechtigung **[!DNL Publish journeys]** auf hoher Ebene beschränkt. Weitere Informationen zur Verwaltung der Zugriffsrechte für [!DNL Journey Optimizer]-Benutzende finden Sie in [diesem Abschnitt](../administration/permissions-overview.md).

## Schutzmechanismen und Empfehlungen

* Eine Journey-Version kann für maximal 14 Tage angehalten werden.
* Anhaltende Journey werden in allen Geschäftsregeln berücksichtigt, genauso wie wenn sie live wären.
* Profile werden in einer pausierten Journey „verworfen“, wenn sie eine Aktionsaktivität erreichen. Wenn sie während der Zeit, in der eine Journey angehalten wurde, auf einer Wartezeit bleiben und diese Wartezeit beenden, wenn sie fortgesetzt wird, setzen sie die Journey fort und werden nicht verworfen.
* Selbst nach der Pause werden diese Ereignisse, da Ereignisse weiterhin verarbeitet werden, auf das 5-ktps-Kontingent angerechnet, nach dem eine Drosselung für unitär angezeigt wird.
* Profile, die auf Journey zugegriffen haben, aber während der Pause verworfen wurden, werden weiterhin als kontaktierbare Profile gezählt.
* Wenn Profile auf einer pausierten Journey gespeichert werden, werden bei der Wiederaufnahme Profilattribute aktualisiert
* In angehaltenen Journey werden weiterhin Bedingungen ausgeführt. Wenn ein Journey aufgrund von Datenqualitätsproblemen angehalten wurde, kann jede Bedingung vor einem Aktionsknoten mit falschen Daten ausgewertet werden.
* Bei einer inkrementellen zielgruppenbasierten Journey mit „Zielgruppe lesen“ wird die Pausendauer berücksichtigt. Beispiel: Bei einem täglichen Journey, wenn es am 2. angehalten und am 5. des Monats fortgesetzt wurde, nimmt die Ausführung am 6. alle Profile auf, die sich vom 1. bis 6. qualifiziert haben. Dies ist nicht der Fall für die Zielgruppen-Qualifizierung oder ereignisbasierte Journey (wenn während einer Pause eine Zielgruppen-Qualifizierung oder ein Ereignis empfangen wird, werden diese Ereignisse verworfen).
* Anhaltende Journey werden auf das Live-Journey-Kontingent angerechnet.
* Das globale Journey-Timeout gilt weiterhin für pausierte Journey. Wenn sich beispielsweise ein Profil 90 Tage lang auf einer Journey befand und die Journey angehalten wurde, verlässt dieses Profil die Journey am 91. Tag weiterhin.
* Ein neuer **Wiederaufnahme** Journey-Status ist verfügbar, wenn eine Journey fortgesetzt wird. Das Überwachen von Journey-Ereignissen wird erneut gestartet, wenn Sie auf **Fortsetzen** klicken.  Bei der Wiederaufnahme von Profilen auf der Journey treten Verzögerungen auf. Wenn der Journey von **Wiederaufnahme** auf **Live** wechselt, bedeutet dies, dass alle Profile wieder aufgenommen wurden. **Wiederaufnahme** kann daher einige Zeit in Anspruch nehmen.
* Wenn Profile auf einer Journey gespeichert werden und diese Journey nach XX Tagen automatisch wieder aufgenommen wird, setzen Sie die Journey fort und werden nicht gelöscht. Wenn Sie sie ablegen möchten, müssen Sie die Journey manuell fortsetzen.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Anhalten einer Journey {#journey-pause-steps}

Sie können jede Live-Journey anhalten.

Gehen Sie wie folgt vor, um den Journey anzuhalten:

1. Öffnen Sie die Journey, die Sie anhalten möchten.
1. Klicken Sie auf die Schaltfläche **…** oben rechts auf der Journey-Arbeitsfläche und wählen Sie **Pause**.

   ![Pause der Journey-Taste](assets/pause-journey-button.png)

1. Wählen Sie die Option Verwalten von Profilen aus, die sich derzeit auf der Journey befinden.

   ![Journey-Optionen anhalten](assets/pause-confirm.png){width="50%" align="left"}

   Sie haben folgende Möglichkeiten:

   * Profile speichern
   * Profile verwerfen

1. Klicken Sie zur Bestätigung auf **Pause**-Schaltfläche.

Eine Journey kann für maximal 14 Tage angehalten werden.

## Fortsetzen pausierter Journey {#journey-resume-steps}

Anhaltende Journey können jederzeit manuell wieder aufgenommen werden.

Gehen Sie wie folgt vor, um eine Journey fortzusetzen:

1. Öffnen Sie die Journey, die Sie fortsetzen möchten.
1. Klicken Sie auf die Schaltfläche **…** oben rechts auf der Journey-Arbeitsfläche und wählen Sie **Fortsetzen**.




