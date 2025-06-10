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
source-git-commit: c9f9ee8734184a734cdf6e5af88fa5a05b49a8de
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 3%

---

# Journey anhalten {#journey-pause}

Sie können Ihre Live-Journey anhalten, alle erforderlichen Änderungen vornehmen und sie jederzeit wieder aufnehmen.<!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Während der Pause können Sie [globale Filter anwenden](#journey-global-filters) um Profile basierend auf ihren Attributen auszuschließen. Die Journey wird nach Ablauf der Pausenzeit automatisch fortgesetzt. Sie können sie auch [manuell fortsetzen](#journey-resume-steps).

>[!AVAILABILITY]
>
>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.


## Wichtigste Vorteile {#journey-dry-run-benefits}

Durch das Anhalten und Fortsetzen von Journey erhalten Journey-Anwender mehr Kontrolle und Flexibilität, da Live-Journey vorübergehend ausgesetzt werden können, ohne das Kundenerlebnis zu stören. Wenn angehalten, werden keine Nachrichten gesendet und die Profile verbleiben in einem ausgesetzten Zustand, bis die Journey fortgesetzt wird.

Diese Funktion reduziert das Risiko des Versands unbeabsichtigter Nachrichten während Fehlern oder Updates (z. B. Änderung des Nachrichteninhalts), unterstützt ein sichereres Journey-Management und erhöht das Vertrauen der Anwender. Die Einblicke in pausierte Journey und deren Status direkt in der Benutzeroberfläche erhöhen die Transparenz und die betriebliche Agilität.

>[!CAUTION]
>
>Die Berechtigungen zum Anhalten und Fortsetzen von Journey sind auf Benutzende mit der Berechtigung **[!DNL Publish journeys]** auf hoher Ebene beschränkt. Weitere Informationen zur Verwaltung der Zugriffsrechte für [!DNL Journey Optimizer]-Benutzende finden Sie in [diesem Abschnitt](../administration/permissions-overview.md).

## Schutzmechanismen und Empfehlungen

* Eine Journey-Version kann für maximal 14 Tage angehalten werden.
* Anhaltende Journey werden in allen Geschäftsregeln berücksichtigt, genauso wie wenn sie live wären.
* Profile werden in einer pausierten Journey „verworfen“, wenn sie eine Aktionsaktivität erreichen. Wenn sie während der Zeit, in der eine Journey angehalten wird, auf Wartezeit bleiben und diese Wartezeit nach der Wiederaufnahme beenden, setzen sie die Journey fort und werden nicht verworfen.
* Da weiterhin Ereignisse verarbeitet werden, werden diese Ereignisse auch nach der Pause auf die Anzahl der Journey-Ereignisse pro Sekunde angerechnet, nach denen eine Drosselung für unitäres Ereignis eintritt.
* Profile, die auf Journey zugegriffen haben, aber während der Pause verworfen wurden, werden weiterhin als kontaktierbare Profile gezählt.
* Wenn Profile auf einer pausierten Journey gespeichert werden, werden bei der Wiederaufnahme Profilattribute aktualisiert
* In angehaltenen Journey werden weiterhin Bedingungen ausgeführt. Wenn ein Journey aufgrund von Datenqualitätsproblemen angehalten wurde, kann jede Bedingung vor einem Aktionsknoten mit falschen Daten ausgewertet werden.
* Bei einer inkrementellen zielgruppenbasierten Journey mit „Zielgruppe lesen“ wird die Pausendauer berücksichtigt. Beispiel: Bei einem täglichen Journey, wenn es am 2. angehalten und am 5. des Monats fortgesetzt wurde, nimmt die Ausführung am 6. alle Profile auf, die sich vom 1. bis 6. qualifiziert haben. Dies ist nicht der Fall für die Zielgruppen-Qualifizierung oder ereignisbasierte Journey (wenn während einer Pause eine Zielgruppen-Qualifizierung oder ein Ereignis empfangen wird, werden diese Ereignisse verworfen).
* Anhaltende Journey werden auf das Live-Journey-Kontingent angerechnet.
* Das globale Journey-Timeout gilt weiterhin für pausierte Journey. Wenn sich beispielsweise ein Profil 90 Tage lang auf einer Journey befand und die Journey angehalten wurde, verlässt dieses Profil die Journey am 91. Tag weiterhin.
* Wenn Profile auf einer Journey gespeichert werden und diese Journey nach einigen Tagen automatisch wieder aufgenommen wird, setzen Sie die Journey fort und werden nicht gelöscht. Wenn Sie sie fallen lassen wollen, müssen Sie die Journey stoppen.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Anhalten einer Journey {#journey-pause-steps}

Sie können jede **Live**-Journey anhalten.

Gehen Sie wie folgt vor, um den Journey anzuhalten:

1. Öffnen Sie die Journey, die Sie anhalten möchten.
1. Klicken Sie auf die Schaltfläche **…** oben rechts auf der Journey-Arbeitsfläche und wählen Sie **Pause**.

   ![Pause der Journey-Taste](assets/pause-journey-button.png){width="80%" align="left"}

1. Wählen Sie die Option Verwalten von Profilen aus, die sich derzeit auf der Journey befinden.

   ![Journey-Optionen anhalten](assets/pause-confirm.png){width="50%" align="left"}

   Sie haben folgende Möglichkeiten:

   * **Hold** Profile - Profile warten, bis die Journey fortgesetzt wird
   * **Verwerfen** Profile - Profile werden beim nächsten Aktionsknoten von der Journey ausgeschlossen

1. Klicken Sie zur Bestätigung auf **Pause**-Schaltfläche.

In der Liste Ihrer Journey können Sie eine oder mehrere **Live**-Journey anhalten. Um eine Gruppe von Journey anzuhalten (_Bulk Pause_), wählen Sie sie in der Liste aus und klicken Sie auf die Schaltfläche **Pause** in der blauen Leiste am unteren Bildschirmrand. Die **Pause**-Schaltfläche ist nur verfügbar, wenn **Live**-Journey ausgewählt sind.

![Massenpause von zwei Live-Journey über die untere Leiste](assets/bulk-pause-journeys.png){width="80%" align="left"}


## Fortsetzen pausierter Journey {#journey-resume-steps}

Anhaltende Journey werden nach Ablauf der maximalen Pausenzeit von 14 Tagen automatisch wieder aufgenommen. Sie können jederzeit manuell fortgesetzt werden.

Gehen Sie wie folgt vor, um eine pausierte Journey fortzusetzen und wieder Journey-Ereignisse zu überwachen:

1. Öffnen Sie die Journey, die Sie fortsetzen möchten.
1. Klicken Sie auf die Schaltfläche **…** oben rechts auf der Journey-Arbeitsfläche und wählen Sie **Fortsetzen**.

   Die Journey wechselt in den Status **Wiederaufnahme**. Der Übergang vom Status **Wiederaufnahme** zum Status **Live** kann einige Zeit dauern: Alle Profile müssen fortgesetzt werden, damit die Journey wieder **Live** werden kann.

1. Klicken Sie zur Bestätigung auf **Fortsetzen**-Schaltfläche.


Aus der Liste Ihrer Journey Journey können Sie eine oder mehrere (**)** fortsetzen. Um eine Gruppe von Journey fortzusetzen (_Bulk Resume_), wählen Sie sie aus und klicken Sie auf die **Fortsetzen**-Schaltfläche in der blauen Leiste am unteren Bildschirmrand. Beachten Sie, dass die **Fortsetzen**-Schaltfläche nur verfügbar ist, wenn **Paused** Journey ausgewählt sind.


## Anwenden eines globalen Filters auf Profile in einem pausierten Journey  {#journey-global-filters}

Wenn ein Journey angehalten wird, können Sie einen globalen Filter basierend auf Profilattributen anwenden. Dieser Filter ermöglicht den Ausschluss von Profilen, die zum Zeitpunkt der Wiederaufnahme dem definierten Ausdruck entsprechen. Profile, die den Kriterien entsprechen, die sich derzeit auf der Journey befinden, beenden die Seite und neue Profile, die versuchen einzutreten, werden blockiert.

Gehen Sie wie folgt vor, um beispielsweise alle französischen Kundinnen und Kunden von der Marketing-Kommunikation nach Frankreich auszuschließen:

1. Navigieren Sie zu der angehaltenen Journey, die Sie ändern möchten.

1. Klicken Sie auf das Symbol **Ausstiegskriterien und globaler Filter** .

   ![Globalen Filter zu einer pausierten Journey hinzufügen](assets/add-global-filter.png){width="50%" align="left"}

1. Definieren **in den Einstellungen &quot;** und Globaler Filter“ einen Filter basierend auf Profilattributen.

1. Legen Sie den Ausdruck fest, um Profile auszuschließen, bei denen das Länderattribut Frankreich entspricht.

   ![Globalen Filter zu einer pausierten Journey hinzufügen](assets/add-country-filter.png){width="50%" align="left"}

1. Speichern Sie den Filter und klicken Sie auf **Journey aktualisieren**, um Ihre Änderungen anzuwenden.

1. [Setzen Sie die Journey fort](#journey-resume-steps).

   Bei der Wiederaufnahme werden alle Profile mit dem Länderattribut Frankreich automatisch von der Journey ausgeschlossen. Alle neuen Profile mit dem Länderattribut Frankreich, die versuchen, die Journey zu betreten, werden blockiert.

Beachten Sie, dass Profilausschlüsse für Profile, die sich derzeit auf der Journey befinden, und für neue Profile nur auftreten, wenn sie einen Aktionsknoten erreichen.

>[!CAUTION]
>
>* Sie können nur **einen** globalen Filter pro Journey festlegen.
>
>* Sie können einen globalen Filter nur in den Journey **Paused** erstellen, aktualisieren oder löschen.