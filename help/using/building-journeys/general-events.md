---
solution: Journey Optimizer
product: journey optimizer
title: Allgemeine Ereignisse
description: Erfahren Sie, wie Sie allgemeine Ereignisse verwenden
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: benutzerdefiniert, allgemein, Ereignisse, Journey
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/jKMddtFlzmUinPK5-onY2u-kRAd1MD126biQVwq3aAg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1253
ht-degree: 51%

---

# Allgemeine Ereignisse {#general-events}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie allgemeine Ereignisse verwenden, um Journey-Trigger einheitlich in Echtzeit auszuführen, und wie Sie Zeitüberschreitungen und Zeitüberschreitungspfade für Ereignisse konfigurieren, um nur während eines definierten Zeitraums auf ein Ereignis zu warten.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Unitäre Ereignisse"
>abstract="Mit Hilfe von Ereignissen können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten. Für diesen Ereignistyp können Sie nur ein Label und eine Beschreibung hinzufügen. Die Ereigniskonfiguration wird von einem Datentechniker vorgenommen und kann nicht bearbeitet werden."

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business_canvas"
>title="Geschäftsereignisse"
>abstract="Mit diesen Ereignissen können Sie eine Journey mit einem nicht profilbezogenen Ereignis starten. Wenn dieses Ereignis ausgelöst wird, können Sie Nachrichten an eine Zielgruppe von Profilen senden. Für diesen Ereignistyp können Sie nur ein Label und eine Beschreibung hinzufügen. Die Ereigniskonfiguration wird von technischen Benutzenden vorgenommen und kann nicht bearbeitet werden."

Mit Hilfe von Ereignissen können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten.

Für diesen Ereignistyp können Sie nur ein Label und eine Beschreibung hinzufügen. Der Rest der Konfiguration kann nicht bearbeitet werden. Dies wurde vom technischen Anwender durchgeführt. Weitere Informationen finden Sie auf [dieser Seite](../event/about-events.md).

Weitere Informationen zu Ereignisdurchsatz und Journey-Verarbeitungsraten finden Sie [in diesem Abschnitt](entry-management.md#journey-processing-rate).

![Panel zur Konfiguration allgemeiner Ereignisse mit Ereignisauswahl und Einstellungen](assets/general-events.png)

Wenn Sie ein Geschäftsereignis einfügen, wird automatisch eine Aktivität **Zielgruppe lesen** hinzugefügt. Weiterführende Informationen zu Geschäftsereignissen finden Sie in [diesem Abschnitt](../event/about-events.md).

## Überwachen von Ereignissen während eines bestimmten Zeitraums {#events-specific-time}

Eine in der Journey positionierte Ereignisaktivität überwacht Ereignisse auf unbestimmte Zeit. Damit ein Ereignis nur während einer bestimmten Zeit überwacht wird, müssen Sie für das Ereignis einen Timeout konfigurieren.

Die Journey überwacht dann das Ereignis während der im Timeout angegebenen Zeit. Wenn ein Ereignis während dieses Zeitraums empfangen wird, wird die Person in den Ereignispfad geleitet. Andernfalls gelangt der Kunde bzw. die Kundin in den Pfad für den Timeout, sofern er definiert ist, oder setzt die Journey fort.

Wenn kein Pfad für den Timeout definiert ist, fungiert die Einstellung für den Timeout als Warteaktivität. Dadurch wartet das Profil für einen Zeitraum, der gestoppt werden kann, wenn ein Ereignis vor dem Ende dieser Wartezeit eintritt. Wenn Sie möchten, dass Profile nach einem Timeout von dieser Journey ausgeschlossen werden, müssen Sie einen Pfad für den Timeout festlegen.

Gehen Sie wie folgt vor, um für ein Ereignis einen Timeout zu konfigurieren:

1. Aktivieren Sie die Option **[!UICONTROL Timeout für das Ereignis definieren]** in den Eigenschaften des Ereignisses.

1. Legen Sie fest, wie lange die Journey auf das Ereignis warten soll. Die maximale Wartezeit beträgt **90 Tage**.

1. Wenn innerhalb des angegebenen Timeouts kein Ereignis empfangen wird, empfiehlt es sich, die Kontakte in einen Timeout-Pfad zu senden. Aktivieren Sie dazu die Option **[!UICONTROL Zeitüberschreitungspfad einrichten]**. In diesem Fall wird die Journey für den Kontakt fortgesetzt, sobald das Timeout erreicht ist. Wir empfehlen Ihnen, immer die Option **[!UICONTROL Zeitüberschreitungspfad einrichten]** zu aktivieren.

   ![Konfiguration des Timeouts für Ereignisse mit Optionen für Timeout-Dauer und -Pfad](assets/event-timeout.png)

In diesem Beispiel sendet die Journey erst dann eine Begrüßungs-E-Mail an eine Kundin oder einen Kunden, nachdem sie bzw. er die Lobby betreten hat. Es wird danach nur dann eine Essensrabatt-E-Mail gesendet, wenn die Kundin oder der Kunde das Restaurant innerhalb des nächsten Tages betritt. Deshalb wurde das Restaurantereignis mit einem Timeout von 1 Tag konfiguriert:

* Wenn das Restaurantereignis in weniger als 1 Tag nach der Begrüßungs-E-Mail eingeht, wird die E-Mail für den Essensrabatt gesendet.
* Wenn innerhalb des nächsten Tages kein Restaurantereignis eingeht, wird die Person durch den Zeitüberschreitungspfad geleitet.

Wenn Sie einen Timeout für mehrere Ereignisse konfigurieren möchten, die sich hinter einer **[!UICONTROL Warteaktivität]** befinden, müssen Sie den Timeout nur für eines dieser Ereignisse konfigurieren.

Der festgelegte Timeout gilt für alle Ereignisse, die hinter der **[!UICONTROL Warteaktivität]** positioniert wurden.

* Wird ein Ereignis innerhalb der Dauer des Timeouts empfangen, gelangt der Kontakt in den Pfad des empfangenen Ereignisses.
* Wenn innerhalb des Timeouts kein Ereignis empfangen wird, gelangt der Kontakt in die Verzweigung für den Timeout desjenigen Ereignisses, bei dem der Timeout definiert wurde.

![Mehrere Ereignisse mit Timeout-Konfigurationen in der Journey](assets/event-timeout-group.png)

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird erläutert, wie Sie allgemeine (unitäre und geschäftliche) Ereignisse in Journey verwenden können, um den Versand von Nachrichten auf individueller Ebene in Echtzeit zu Triggern, einschließlich der Konfiguration von Zeitüberschreitungen und Zeitüberschreitungspfaden für Ereignisse.

**intents:**
* Hinzufügen einer allgemeinen Ereignisaktivität zu einer Journey-Arbeitsfläche für den Echtzeit-Profileintrag eines Triggers
* Maximale Wartezeit für ein Ereignis konfigurieren, um zu begrenzen, wie lange eine Journey auf ein Ereignis wartet
* Richten Sie einen Pfad für die maximale Wartezeit ein, um Profile zu verarbeiten, bei denen nicht der Trigger des erwarteten Ereignisses rechtzeitig eintritt
* Unterscheiden Sie zwischen unitären Ereignissen und Geschäftsereignissen und verstehen Sie, wann jedes automatisch hinzugefügt wird
* Maximale Wartezeit bei Ereignissen mit Warteaktivitäten kombinieren, um die maximale Wartezeit bei mehreren Ereignissen zu steuern

**Glossar:**
* **Unitäres Ereignis**: Ein Ereignis, bei dem die Journey für jeweils eine Person in Echtzeit (*) Trigger wird*
* **Geschäftsereignis**: Ein nicht profilbezogenes Ereignis, bei dem eine Journey für eine Zielgruppe von Profilen Trigger wird und automatisch die Aktivität „Zielgruppe lesen“ hinzugefügt wird *(produktspezifisch)*
* **Maximale Wartezeit für Ereignis**: Eine konfigurierbare Dauer (bis zu 90 Tage), nach der die Journey nicht mehr auf ein bestimmtes Ereignis wartet und das Profil an einen Zeitüberschreitungspfad (*) weiterleitet*
* **Zeitüberschreitungspfad**: Eine optionale Journey-Verzweigung, der Profile folgen, wenn das erwartete Ereignis nicht innerhalb des Zeitüberschreitungsfensters empfangen wird *(produktspezifisch)*

**Leitplanken:**
* Ereignisbeschriftung und -beschreibung sind die einzigen bearbeitbaren Felder für ein allgemeines Ereignis auf der Arbeitsfläche. Alle anderen Konfigurationen werden von einem technischen Anwender durchgeführt und können nicht von der Journey aus geändert werden
* Maximale maximale Wartezeit für Ereignisse ist 90 Tage
* Wenn mehrere Ereignisse auf eine Warteaktivität folgen, muss die Zeitüberschreitung für nur eines dieser Ereignisse konfiguriert werden. Die definierte Zeitüberschreitung gilt dann für alle Ereignisse nach der Wartezeit
* Wenn kein Zeitüberschreitungspfad definiert ist, dient die Zeitüberschreitung als Warteaktivität. Profile, die das Ereignis nicht erhalten, verbleiben bis zum Ablauf der Zeitüberschreitung auf der Journey

**Terminologie:**
* Kanonischer Name: Allgemeines Ereignis — Akronym: none — Varianten: Unitäres Ereignis, benutzerspezifisches Ereignis
* Synonyme: „Allgemeines Ereignis“ = „Unitäres Ereignis“ (im Kontext der Canvas-Aktivität)
* Verwechseln Sie nicht: „Geschäftsereignis“ ≠ „Unitäres Ereignis“ - ein Geschäftsereignis richtet sich an eine Zielgruppe von Profilen, während ein unitäres Ereignis eine einzelne Person anspricht

**FAQ:**
* **F: Kann ich die Ereigniskonfiguration auf der Journey-Arbeitsfläche ändern?** - Nein. Nur Titel und Beschreibung können auf der Arbeitsfläche bearbeitet werden. Die vollständige Ereigniskonfiguration wird von einem technischen Anwender festgelegt und kann nicht von der Journey aus geändert werden.
* **F: Was passiert, wenn vor Ablauf der maximalen Wartezeit kein Ereignis empfangen wird?** - Wenn ein Zeitüberschreitungspfad definiert ist, fließt das Profil in diesen Pfad. Wenn kein Zeitüberschreitungspfad festgelegt ist, verhält sich die Zeitüberschreitung wie eine Warteaktivität, und das Profil fährt nach der Zeitüberschreitung mit der Journey fort.
* **F: Wie lange dauert die maximale Zeitüberschreitung bei einem Ereignis?** — 90 Tage.
* **F: Wann sollte ich die Option Zeitüberschreitungspfad aktivieren?** — Aktivieren Sie sie immer, wenn Profile diese Verzweigung nach der maximalen Wartezeit verlassen sollen. Ohne Zeitüberschreitungspfad bleiben Profile auf der Journey und warten auf das Ereignis.
* **F: Wie unterscheidet sich ein Geschäftsereignis von einem unitären Ereignis auf der Journey-Arbeitsfläche?** — Durch das Ablegen eines Geschäftsereignisses wird automatisch die Aktivität Zielgruppe lesen hinzugefügt, da Geschäftsereignisse auf mehrere Profile gleichzeitig und nicht auf eine einzelne Person abzielen.

+++
