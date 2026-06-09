---
solution: Journey Optimizer
product: journey optimizer
title: Definieren der Journey-Eigenschaften
description: Erfahren Sie, wie Sie Eigenschaften Ihres Journey mit festlegen [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Konfiguration, Eigenschaften
exl-id: 6c21371c-6cbc-4d39-8fe6-39f1b8b13280
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/fDzEwuisEjAKvpIs9SKoz-9IIJXJQ-md9FlCbWQOJz8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: ba62ad25-65cb-4ea9-b7aa-0fa87c4a9fa0
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 84d3c8bd62648c7d1b6cd969ceb7f80329110982
workflow-type: tm+mt
source-wordcount: 3646
ht-degree: 75%

---

# Festlegen der Journey-Eigenschaften {#jo-properties}

Verwenden Sie Journey-Eigenschaften, um globale Einstellungen für Ihren Journey zu konfigurieren, einschließlich Name, Eintrittsregeln, Zeitzone, Start- und Enddatum, Zeitüberschreitungsdauer, Ausstiegskriterien und Konfliktmanagement. Eigenschaften können in jeder Phase des Journey-Authorings über die rechte Leiste aufgerufen werden.

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Journey-Eigenschaften"
>abstract="Konfigurieren Sie globale Einstellungen für diese Journey, einschließlich Name, Tags, Eintrittsregeln, Zeitzone, Datumsangaben, Zeitüberschreitung und Konflikt-Management. Schreibgeschützte Parameter sind standardmäßig ausgeblendet. Die verfügbaren Optionen variieren je nach Journey-Status, Berechtigungen und Produktkonfiguration."

## Zugreifen auf die Eigenschaften einer Journey {#access-properties}

Die Eigenschaften einer Journey sind in der rechten Leiste zentralisiert. Dieser Abschnitt wird beim Erstellen einer neuen Journey standardmäßig angezeigt. Klicken Sie zum Öffnen bestehender Journeys auf das Stiftsymbol neben dem Journey-Namen.

Über diesen Abschnitt können Sie den Namen der Journey definieren, eine Beschreibung hinzufügen und globale Journey-Eigenschaften festlegen.

Sie haben folgende Möglichkeiten:

* Weisen Sie Ihrem Journey [!DNL Adobe Experience Platform] einheitliche Tags zu, um sie einfach zu klassifizieren und die Suche über die Kampagnenliste zu verbessern. [Weitere Informationen zum Arbeiten mit Tags](../start/search-filter-categorize.md#tags)
* Auswählen von Journey-Metriken. [Weitere Informationen zum Konfigurieren und Tracking von Journey-Metriken](success-metrics.md)
* Verwalten Sie [Eintritt und Wiedereintritt](#entrance). Die Verwaltung des Profileintritts hängt vom Typ der Journey ab. Einzelheiten hierzu finden Sie auf [dieser Seite](entry-management.md).
* Verwalten des [Zugriffs auf Daten](#manage-access)
* Auswählen der [Zeitzonen](#timezone) für die Journey und das Profil
* Festlegen benutzerdefinierter [Start- und Enddaten](#dates)
* Definieren einer [Timeout-Dauer](#timeout) in Journey-Aktivitäten (nur für Admins)
* Überwachen Sie die [aktuelle Größe der Journey-Payload](#journey-payload-size), um Veröffentlichungsfehler zu vermeiden.
* Überwachen von Konflikten und Priorisieren Ihrer Journeys mithilfe von [Konflikt-Management-Tools](#conflict)

![Panel zur Konfiguration von Journey-Eigenschaften mit allgemeinen Einstellungen und erweiterten Optionen](assets/new-journey-properties.png){width="80%"}{zoomable="yes"}

>[!NOTE]
>
>Für Live-Journeys werden in diesem Bildschirm nur das Veröffentlichungsdatum und der Name der Person angezeigt, die die Journey veröffentlicht hat.

Mithilfe der Option **Technische Details kopieren** können Sie jederzeit technische Informationen zur Journey kopieren, die dem Support-Team bei der Problembehebung helfen. Die folgenden Informationen werden kopiert:

**Allgemein**

* `JourneyVersion UID` - Eindeutige Kennung dieser Journey-Version
* `OrgID` - Kennung Ihres Unternehmens (IMS)
* `orgName` - Name Ihres Unternehmens
* `sandboxName` : Name der Sandbox, in der die Journey ausgeführt wird
* `lastDeployedBy` - Benutzer, der die Journey zuletzt veröffentlicht hat
* `lastDeployedAt` - Datum und Uhrzeit der letzten Veröffentlichung


**Anhalten und Fortsetzen** (enthalten, wenn die Journey mindestens einmal angehalten wurde)

* `lastPausedAt` - Datum und Uhrzeit der letzten Pause der Journey
* `lastPausedBy` - Anzeigename des Benutzers, der die letzte Pause durchgeführt hat
* `lastPausedById` - Interne Kennung des Benutzers, der die letzte Pause ausgeführt hat.
* `lastResumedAt` - Datum und Uhrzeit der letzten Wiederaufnahme der Journey
* `lastResumedBy` - Anzeigename des Benutzers, der den letzten Lebenslauf ausgeführt hat
* `lastResumedById` - Interne Kennung des Benutzers, der den letzten Lebenslauf ausgeführt hat.

**Einstellungen für Journey angehalten** (in `pausedJourneySettings`, wenn die Journey angehalten wurde oder wurde)

* `pauseBehavior` - Was passiert mit Profilen auf der Journey, wenn sie pausiert werden (beispielsweise verwerfen oder an Ort und Stelle behalten)?
* `maxPauseDurationInMinutes` - Maximale Pausendauer in Minuten, nach der die Journey automatisch fortgesetzt wird (z. B. 20160 = 14 Tage)
* `transitionStateForAutoResume` - Status, der angewendet wird, wenn die Journey am Ende der Pausenzeit automatisch fortgesetzt wird (z. B. Beenden oder Fortsetzen)
* `pauseId` - Eindeutige Kennung für die aktuelle Pauseninstanz

Weitere Informationen zu technischen Feldern, die mit einer Journey für ein bestimmtes Profil in Verbindung stehen, und dazu, wie Sie sie verwenden können, finden Sie [auf dieser Seite](expression/journey-properties.md).

## Eintritt und Wiedereintritt {#entrance}

Der Eintrittsmodus des Profils wird auf der Journey-Ebene im rechten Konfigurationsbereich definiert. Die Einstellungen werden nachfolgend beschrieben.

Die Verwaltung des Profileintritts hängt vom Typ der Journey ab. Weitere Informationen zur Verwaltung des Profileintritts und -wiedereintritts finden Sie auf [dieser Seite](entry-management.md). Weitere Informationen zu Journey-Verarbeitungsraten und dazu, wie Profile die Journey durchlaufen, finden Sie [in diesem Abschnitt](entry-management.md#journey-processing-rate).

### Erneuten Eintritt erlauben  {#allow-reentrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="Erneuten Eintritt erlauben"
>abstract="Standardmäßig erlauben neue Journeys einen erneuten Eintritt. Die Option **Erneuten Eintritt erlauben** kann deaktiviert werden, z. B. wenn ein einmaliges Geschenk angeboten werden soll, wenn eine Person einen Shop betritt."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Profileintrittsverwaltung"

Standardmäßig erlauben neue Journeys einen erneuten Eintritt. Sie können die Option **Erneuten Eintritt erlauben** für „einmalige“ Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt.

### Wartezeit bis zum erneuten Eintritt  {#reentrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="Wartezeit bis zum erneuten Eintritt"
>abstract="Legen Sie die Wartezeit fest, bevor Sie in einheitlichen Journeys einem Profil erlauben, erneut in die Journey einzutreten. Dadurch wird verhindert, dass Benutzende während eines bestimmten Zeitraums erneut in die Journey eintreten. Maximale Dauer: 90 Tage."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Profileintrittsverwaltung"

Wenn die Option **Erneuten Eintritt erlauben** aktiviert ist, wird das Feld **Wartezeit bis zum erneuten Eintritt** angezeigt. In diesem Feld kann die Wartezeit definiert werden, bevor es einem Profil erlaubt wird, in unitären Journeys erneut in die Journey einzutreten (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung). Dadurch wird verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Standardmäßig ist das Feld auf 5 Minuten eingestellt. Die maximale Wartezeit beträgt 90 Tage.

## Verwalten des Zugriffs {#manage-access}

Sie können den Zugriff auf eine Journey basierend auf Zugriffs-Labels einschränken.

Um der Journey benutzerdefinierte Datennutzungs-Label zuzuweisen, klicken Sie auf das Symbol **[!UICONTROL Verwalten von Zugriffs-Labels]** und wählen Sie ein oder mehrere Labels aus.

[Weitere Informationen zur Zugriffssteuerung auf Objektebene (Object Level Access Control, OLAC)](../administration/object-based-access.md)

## Journey-Payload-Größe {#journey-payload-size}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_payload_size"
>title="Aktuelle Journey-Payload-Größe"
>abstract="Zeigt die aktuelle Größe der Journey-Payload im Vergleich zum konfigurierten Limit an. Verwenden Sie diesen Indikator, um die Journey-Komplexität vor dem Veröffentlichen zu überwachen und Fehler zu vermeiden, die durch eine Überschreitung des Limits der Payload-Größe verursacht werden."

Das Feld **[!UICONTROL Aktuelle Journey-Payload]** im Bedienfeld Journey-Eigenschaften zeigt die aktuelle Payload-Größe Ihrer Journey im Verhältnis zum konfigurierten Limit an - z. B. *1,5 MB (von 2 MB)*. Dieser schreibgeschützte Indikator ist in jeder Phase des Journey-Authorings sichtbar.

![Größenanzeige der aktuellen Journey-Payload im Bedienfeld &quot;Journey-Eigenschaften“](assets/journey-payload-size.png){width="50%" zoomable="yes"}

Verwenden Sie diese Informationen, um die Komplexität Ihres Journey vor der Veröffentlichung zu überwachen. Wenn die Payload-Größe das Limit erreicht oder überschreitet, schlägt die Journey-Veröffentlichung fehl. Um die Größe zu reduzieren, sollten Sie die Journey-Logik vereinfachen oder die Anzahl der Aktivitäten reduzieren.

Der Standardwert ist 4 MB. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie eine höhere Begrenzung für Ihr Unternehmen anfordern müssen.

Ausführliche Informationen zu Schwellenwerten, Warn- und Fehlermeldungen sowie Schritten zur Fehlerbehebung finden Sie unter [Validierung der Journey-Payload](../start/guardrails.md#journey-payload-size) und [Allgemeine Schutzmaßnahmen beim Journey](../start/guardrails.md#journeys-guardrails-journeys).

## Zeitzonen von Journeys und Profilen {#timezone}

Die Zeitzone wird auf Journey-Ebene definiert. Sie können eine feste Zeitzone eingeben oder [!DNL Adobe Experience Platform] verwenden, um die Zeitzone für das Journey festzulegen. Wenn eine Zeitzone in [!DNL Adobe Experience Platform] Profil definiert ist, kann sie auf der Journey abgerufen werden.

[Weitere Informationen zum Zeitzonen-Management](../building-journeys/timezone-management.md)

## Start- und Enddatum {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="Startdatum"
>abstract="Wählen Sie das Datum aus, ab dem Profile in die Journey eintreten können. Wenn kein Startdatum festgelegt ist, wird standardmäßig das Veröffentlichungsdatum der Journey verwendet."

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="Enddatum"
>abstract="Legen Sie das Datum fest, an dem die Journey endet. An diesem Datum verlassen aktive Profile automatisch die Journey und es wird kein neuer Eintritt mehr zugelassen."

Standardmäßig können Profile in eine Journey sofort nach ihrer Veröffentlichung eintreten und so lange bleiben, bis das [globale Journey-Timeout](#global_timeout) erreicht ist. Die einzige Ausnahme sind wiederkehrende „Zielgruppe lesen“-Journeys, bei denen die Option **Bei wiederholter Ausführung erneuten Eintritt erzwingen** aktiviert ist und die am Startdatum des nächsten Vorkommens enden.

Bei Bedarf können Sie ein benutzerdefiniertes **Start**- und **Enddatum** festlegen. Dadurch können Profile an einem bestimmten Datum in Ihre Journey eintreten und diese bei Erreichen des Enddatums wieder automatisch verlassen.

## Timeout {#timeout}

Zeitüberschreitungseinstellungen steuern, wie lange ein Journey auf die Ausführung einer Aktivität wartet und wie lange Profile auf einem Journey verbleiben können.

### Timeout bei Journey-Aktivitäten {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_timeout"
>title="Timeout oder Fehler"
>abstract="Die Option **Zeitüberschreitung oder Fehler** definiert einen alternativen Pfad auf der Journey, wenn die Aktion eine Zeitüberschreitung aufweist oder einen Fehler zurückgibt, sodass Profile weiterhin einen Fallback-Pfad verwenden, anstatt bei diesem Schritt anzuhalten. Die empfohlenen Werte liegen zwischen 1 und 30 Sekunden."

Beim Bearbeiten einer Aktions- oder Bedingungsaktivität können Sie im Falle eines Fehlers oder einer Überschreitung des Timeouts einen alternativen Pfad definieren. Wenn die Verarbeitung der Aktivität, die ein Drittanbietersystem abfragt, den im Feld **[!UICONTROL Zeitüberschreitung oder Fehler]** festgelegten Timeout der Journey-Eigenschaften überschreitet, wird der zweite Pfad ausgewählt, um eine potenzielle Ausweichaktion durchzuführen.

Die empfohlenen Werte liegen zwischen 1 und 30 Sekunden.

Es wird empfohlen, unter **[!UICONTROL Timeout oder Fehler]** einen sehr kurzen Wert festzulegen, wenn Ihre Journey zeitempfindlich ist (z. B. als Reaktion auf den Echtzeit-Standort einer Person), da Sie Ihre Aktion nicht länger als einige Sekunden verzögern können. Wenn Ihre Journey weniger zeitkritisch ist, können Sie einen längeren Wert verwenden, um dem aufgerufenen System mehr Zeit zum Senden einer gültigen Antwort zu geben.

Journey verwenden auch eine maximale globale Wartezeit, wie unten beschrieben.

### Globaler Timeout der Journey {#global_timeout}

Zusätzlich zum in den Journey-Aktivitäten verwendeten [Timeout](#timeout_and_error) wird ein globaler Journey-Timeout angewendet. Sie wird nicht auf der Benutzeroberfläche angezeigt und kann nicht geändert werden.

Dieser globale Timeout stoppt den Fortschritt von Kontakten in der Journey **91 Tage** nach ihrem Eintritt. Das bedeutet, dass die Journey eines Kontakts nicht länger als 91 Tage dauern kann. Nach Ablauf des Timeouts werden die Daten des Kontakts gelöscht. Kontakte, die sich nach dem Timeout noch in der Journey befinden, werden gestoppt und beim Reporting nicht berücksichtigt. Sie könnten also mehr Personen sehen, die in die Journey eintreten, als Personen, die sie beenden.

>[!NOTE]
>
>Die genaue Definition, wann eine Journey als „beendet“ gilt, variiert je nach Journey-Typ. [Siehe detaillierte &#x200B;](end-journey.md#journey-finished-definition).

Aufgrund des Journey-Timeouts von 91 Tagen können wir, wenn der erneute Eintritt in die Journey nicht erlaubt ist, nicht sicherstellen, dass die Sperrung des erneuten Eintritts nach mehr als 91 Tagen erhalten bleibt. Da wir alle Informationen über Personen, die in die Journey eingetreten sind, 91 Tage nach deren Eintritt entfernen, können wir nicht wissen, dass die Person vor mehr als 91 Tagen bereits Eintritt hatte.

Ein Kontakt kann nur dann eine Warteaktivität annehmen, wenn er oder sie noch genügend Zeit hat, um die Wartezeit vor Ablauf des 91-tägigen Timeouts der Journey zu erfüllen. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/wait-activity.md).

### Häufig gestellte Fragen zu Time-to-Live (TTL) und Datenspeicherung {#timeout-faq}

Ab [!DNL Adobe Journey Optimizer] Version Juni 2024 wurde die globale Zeitüberschreitung bei Journey von 30 auf 91 Tage verschoben. Die Auswirkungen sind in den folgenden häufig gestellten Fragen aufgeführt:

**Für einheitliche Journeys**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit Journeys, die nach dem Rollout der TTL-Verlängerung veröffentlicht wurden?</p>
    </td>
    <td>
      <p>Für Profile, die in die neue Journey eintreten, beträgt die TLL automatisch 91 Tage.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem Profil, das in eine Journey eintritt, die vor dem Launch der TTL-Verlängerung veröffentlicht wurde?</p>
    </td>
    <td>
      <p>Die TTL für das Profil beträgt 30 Tage (7 Tage für HIPAA) ab dem Zeitpunkt, zu dem die Journey ursprünglich veröffentlicht wurde.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem Profil, das beim Launch der TTL-Verlängerung bereits in eine Journey eingetreten ist?</p>
    </td>
    <td>
      <p>Für das Profil bleibt eine TTL von 30 Tagen (7 Tage für HIPAA) gemäß dem ursprünglichen Veröffentlichungszeitpunkt der Journey bestehen.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem Profil in einer früheren Journey-Version, die nach dem Launch der TTL-Verlängerung erneut veröffentlicht wird?</p>
    </td>
    <td>
      <p>Für das Profil bleibt eine TTL von 30 Tagen (7 Tage für HIPAA) gemäß bestehen, ausgerichtet auf den ursprünglichen Veröffentlichungszeitpunkt der Journey.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem neuen Profil, das nach dem Launch der TTL-Verlängerung in eine erneut veröffentlichte Journey-Version eintritt?</p>
    </td>
    <td>
      <p>Die TTL für das Profil beträgt 91 Tage (7 Tage für HIPAA), entsprechend der TTL der erneut veröffentlichten Journey-Version.</p>
    </td>
  </tr>
</table>

**Für Segmentauslöser-Journeys**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit neuen einmaligen Journeys, die nach der TTL-Verlängerung veröffentlicht werden?</p>
    </td>
    <td>
      <p>Die TTL für Profile, die in die neue Journey eintreten, beträgt automatisch 91 Tage.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit neuen wiederkehrenden Journeys ohne erzwungenen erneuten Eintritt, die nach der TTL-Verlängerung veröffentlicht werden?</p>
    </td>
    <td>
      <p>Die TTL für Profile, die in die neue Journey eintreten, beträgt automatisch 91 Tage.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit neuen wiederkehrenden Journeys mit erzwungenem erneuten Eintritt, die nach der TTL-Verlängerung veröffentlicht werden?</p>
    </td>
    <td>
      <p>Die TTL für Profile, die in die neue Journey eintreten, entspricht dem Wiederholungsintervall. Wenn die Journey beispielsweise täglich ausgeführt wird, beträgt die TTL 1 Tag.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem Profil, das in eine Journey eintritt, die vor dem Launch der TTL-Verlängerung veröffentlicht wurde?</p>
    </td>
    <td>
      <p>Die TTL für das Profil beträgt 30 Tage (7 Tage für HIPAA) ab dem ursprünglichen Veröffentlichungszeitpunkt. Bei wiederkehrenden Journeys mit erzwungenem erneuten Eintritt entspricht die TTL dem Wiederholungsintervall.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem Profil, das beim Launch der TTL-Verlängerung gerade eine Journey durchläuft?</p>
    </td>
    <td>
      <p>Für das Profil bleibt eine TTL von 30 Tagen (7 Tage für HIPAA) gemäß dem ursprünglichen Veröffentlichungszeitpunkt der Journey bestehen. Bei wiederkehrenden Journeys mit erzwungenem erneuten Eintritt entspricht die TTL dem Wiederholungsintervall.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem laufenden Profil in einer vorherigen Journey-Version, die nach dem Launch der TTL-Erweiterung erneut veröffentlicht wird?</p>
    </td>
    <td>
      <p>Für das Profil bleibt eine TTL von 30 Tagen (7 Tage für HIPAA) gemäß bestehen, ausgerichtet auf den ursprünglichen Veröffentlichungszeitpunkt der Journey. Bei wiederkehrenden Journeys mit erzwungenem erneuten Eintritt entspricht die TTL dem Wiederholungsintervall.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem neuen Profil, das nach dem Launch der TTL-Verlängerung in eine erneut veröffentlichte Journey-Version eintritt?</p>
    </td>
    <td>
      <p>Die TTL für das Profil beträgt 91 Tage (7 Tage für HIPAA), entsprechend der TTL der erneut veröffentlichten Journey-Version. Bei wiederkehrenden Journeys mit erzwungenem erneuten Eintritt entspricht die TTL dem Wiederholungsintervall.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wird die wiederkehrende Read Audience Journey nach 91 Tagen beendet?</p>
    </td>
    <td>
      <p>Nein. Eine wiederkehrende Journey mit dem Titel „Zielgruppe lesen“ ohne Enddatum bleibt <strong>Live</strong> solange sie veröffentlicht wird. Der Status <strong>Beendet</strong> wird nur 91 Tage nach der Ausführung des <strong>letzten Vorkommens“ </strong>. Das globale 91-Tage-Timeout gilt für einzelne Profile, die die Journey durchlaufen (maximale aktive Dauer pro Profil), nicht für den Live-Status der Journey.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was ist der Unterschied zwischen der 91-tägigen Journey-Zeitüberschreitung und dem 91-tägigen Berichtsfenster?</p>
    </td>
    <td>
      <p>Dies sind zwei separate Konzepte. Das globale Zeitlimit von <strong>Journey</strong> (91 Tage) ist die maximale Zeit, die ein einzelnes Profil innerhalb eines Journey aktiv bleiben kann - nach 91 Tagen wird das Profil beendet und seine Daten gelöscht. Das <strong>Reporting-Fenster</strong> (ca. 91 Tage) ist eine Anzeigebeschränkung in der Benutzeroberfläche: Leistungsdaten, die älter als ~91 Tage sind, sind in Berichten nicht mehr sichtbar, aber die Journey selbst wird weiterhin ausgeführt und neue Profile treten weiterhin ein.</p>
    </td>
  </tr>
</table>

## Zusammenführungsrichtlinie {#merge-policies}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_merge_policy"
>title="Zusammenführungsrichtlinie"
>abstract="Die Zusammenführungsrichtlinie wird automatisch basierend auf Ihrem ausgewählten Ereignis oder Ihrer ausgewählten Zielgruppe abgerufen. Diese Zusammenführungsrichtlinie wird für die gesamte Journey verwendet."

[!DNL Adobe Journey Optimizer] verwendet Zusammenführungsrichtlinien beim Abrufen von Profildaten aus [!DNL Adobe Experience Platform]. Je nach Journey-Typ werden unterschiedliche Zusammenführungsrichtlinien verwendet:

* In **[Zielgruppe lesen](read-audience.md)** oder **[Zielgruppen-Qualifizierung](audience-qualification-events.md)** Journey wird die Zusammenführungsrichtlinie der Zielgruppe verwendet
* In **[Unitäres](../event/about-events.md)**: Journey wird die standardmäßige Zusammenführungsrichtlinie verwendet
* In **[Geschäftsereignis](../event/about-creating-business.md)** Journeys: Die Zusammenführungsrichtlinie der Zielgruppe wird in der folgenden Aktivität vom Typ Zielgruppe lesen verwendet

[!DNL Adobe Journey Optimizer] wendet die im gesamten Journey verwendete Zusammenführungsrichtlinie an. Wenn also mehrere Zielgruppen in einer Journey verwendet werden (z. B. [`inAudience`-Funktionen](functions/functioninaudience.md)), entstehen Inkonsistenzen mit der von der Journey verwendeten Zusammenführungsrichtlinie, es wird ein Fehler generiert und die Veröffentlichung blockiert. Wenn jedoch bei der Nachrichtenpersonalisierung eine inkonsistente Zielgruppe verwendet wird, wird trotz der Inkonsistenz kein Warnhinweis generiert. Aus diesem Grund wird dringend empfohlen, die mit Ihrer Zielgruppe verknüpfte Zusammenführungsrichtlinie zu überprüfen, wenn diese Zielgruppe bei der Nachrichtenpersonalisierung verwendet wird.

Weitere Informationen zu Zusammenführungsrichtlinien finden Sie unter [[!DNL Adobe Experience Platform] Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

>[!NOTE]
>
>Wenn eine Zielgruppen-Zusammenführungsrichtlinie aktualisiert wird, müssen alle aktiven Journeys, die auf diese Zielgruppe verweisen, erneut veröffentlicht (oder dupliziert) werden. Wenn Sie die Zusammenführungsrichtlinie ändern, wird tatsächlich eine „neue“ Zielgruppe erstellt, auf die die laufende Journey nicht zugreifen kann. Auf diese Weise wird Datenkonsistenz sichergestellt.

## Ausstiegskriterien {#exit-criteria}

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Ausstiegskriterien"
>abstract="In diesem Abschnitt werden die Optionen für Ausstiegskriterien angezeigt. Sie können für die Ausstiegskriterien Ihrer Journey ein oder mehrere Regeln und Filter erstellen."

### Kriterien für den Journey-Ausstieg {#exit-criteria-desc}

Durch Hinzufügen von Beendigungskriterien veranlassen Sie die Profile, die Journey zu verlassen, sobald ein Ereignis eintritt (z. B. Kauf) oder sie für eine Zielgruppe qualifiziert sind. Dadurch wird verhindert, dass Benutzende weitere Nachrichten von der Journey erhalten.

Sie können Profile aus einer Journey entfernen, wenn sie nicht mehr dem Zweck der Journey entsprechen. Dies kann durch **globale Ausstiegskriterien** erreicht werden, die eng mit dem Ziel-Management verbunden sind.

>[!TIP]
>
>Suchen Sie nach einer praktischer Anleitung mit Beispielen aus der Praxis? Lesen Sie unseren [umfassenden Leitfaden zu Journey-Eintritts- und Ausstiegskriterien](entry-exit-criteria-guide.md), der vollständige Anwendungsfälle mit Eintritts- und Ausstiegskonfigurationen, Best Practices und Optimierungsstrategien umfasst.

**Beispiel für einen Anwendungsfall**

Eine Marketing-Fachperson hat eine Werbe-Journey, die eine Reihe von Kommunikationsmaßnahmen umfasst. Jede dieser Kommunikationsmaßnahmen zielt darauf ab, die Kundschaft zum Kauf zu bewegen. Sobald der Kauf getätigt wurde, sollte die Kundin bzw. der Kunde die restlichen Nachrichten der Serie nicht mehr erhalten. Durch die Definition von Ausstiegskriterien werden alle Profile, die einen Kauf getätigt haben, aus der Journey entfernt.

### Konfiguration und Verwendung {#exit-criteria-config}

Ausstiegskriterien werden auf Journey-Ebene festgelegt. Eine Journey kann mehrere Ausstiegskriterien haben. Wenn Sie mehrere Ausstiegskriterien festgelegt haben, erfolgt die Auswertung von oben nach unten mit einer `OR`-Logik. Wenn Sie also Ausstiegskriterien A und Ausstiegskriterien B haben, wird es als A **ODER** B ausgewertet. Die Kriterien werden bei jedem Schritt der Journey ausgewertet.

Um ein Ausstiegskriterium zu **erstellen**, gehen Sie folgendermaßen vor:

1. Öffnen Sie Ihre Journey.

1. Klicken Sie oben rechts auf der Journey-Arbeitsfläche auf das Symbol ![Symbol „Ausstiegskriterien anzeigen“](assets/do-not-localize/Smock_UserCheckedOut_18_N.svg) **[!UICONTROL Ausstiegskriterien anzeigen]**.

1. Wählen Sie **[!UICONTROL Ausstiegskriterien hinzufügen]** aus.

1. Geben Sie ein **Label** ein und wählen Sie aus, ob Ihr Ausstiegskriterium auf einem **Ereignis** oder einer **Zielgruppe** basiert.

   * Für Ausstiegskriterien, die auf einem Ereignis basieren, wie z. B. das Herunterladen einer App oder das Hinzufügen eines Produkts zu einem Warenkorb, wählen Sie nur ein einziges Ereignis.
   * Für Ausstiegskriterien, die auf einer Zielgruppe basieren, wie z. B. eine Zielgruppe, die überprüft, ob eine Person in den letzten 24 Stunden einen Kauf getätigt hat, wählen Sie eine Zielgruppe. Hinweis: Es kann bis zu 10 Minuten dauern, bis Ausstiegskriterien, die eine Zielgruppe verwenden, wirksam werden.

Sie können mehrere Ausstiegskriterien hinzufügen. Das Ausstiegskriterium ist nun aktiviert und wird bei jedem Schritt des Journey ausgewertet.

![Panel für Ausstiegskriterien, das die Zielgruppenbedingungen für das Beenden der Journey anzeigt](assets/exitcriteria-sample.png){width="40%"}


### Auf Profilattributen basierende Ausstiegskriterien {#profile-exit-criteria}

Die auf Profilattributen basierenden Ausstiegskriterien geben Ihnen mehr Kontrolle über pausierte Journeys, indem Sie Regeln definieren können, mit denen bestimmte Profile automatisch entfernt werden, bevor die Journey fortgesetzt wird. Sie können Ausstiegsbedingungen basierend auf Profilattributen festlegen, z. B. Standort, Status oder Voreinstellungen, um sicherzustellen, dass nach der Wiederaufnahme nur relevante Profile in der Journey bleiben.

Sie können beispielsweise [eine Journey anhalten](journey-pause.md), eine Ausstiegsbedingung hinzufügen, um alle in Frankreich befindlichen Profile zu entfernen, und dann die Journey in dem Wissen fortsetzen, dass diese Profile im nächsten Aktionsschritt ausgeschlossen werden. Diese Logik gilt sowohl für Profile, die sich bereits in der Journey befinden, als auch für neue Profile, die sich nach der Wiederaufnahme der Journey qualifizieren.

Diese Funktion arbeitet mit der Funktion „Pausieren/Fortsetzen“ zusammen und hilft Ihnen, Journeys sicherer und flexibler zu verwalten. Sie minimiert manuelle Eingriffe, reduziert das Risiko des Versands irrelevanter oder nicht konformer Nachrichten und hält Ihre Journey-Logik mit den aktuellen Geschäftsanforderungen im Einklang.

In diesem Abschnitt erfahren Sie, wie Sie [Ausstiegskriterien für Profilattribute in pausierten Journeys verwenden](journey-pause.md#journey-pause-sample).

### Leitlinien und Einschränkungen {#exit-criteria-guardrails}

Die folgenden Leitlinien und Einschränkungen gelten für die [Ausstiegskriterien der Journey](#exit-criteria-desc):

* Die Ausstiegskriterien sind nur im Entwurfsstadium definiert
* Kohärenz des Journey-Namespace zwischen Ereignissen und ereignisbasierten Ausstiegskriterien

Bei Verwendung der Funktion [Profilattributbasierte Ausstiegskriterien](#profile-exit-criteria) gelten die folgenden Leitlinien:

* **Ausstiegskriterien gelten auf Aktionsebene**\
  Die Ausstiegskriterien des Typs „Profilattribut“ werden nur in Aktionsschritten ausgewertet. Im Gegensatz zu anderen Ausstiegskriterien gelten diese nicht global für die Journey.\
  Wenn Sie eine Journey fortsetzen und einige Profile die Ausstiegsbedingung erfüllen, werden diese Profile beim nächsten Aktionsknoten ausgeschlossen.\
  Neue Profile, die nach der Wiederaufnahme in die Journey eintreten, werden ebenfalls bei ihrem ersten Aktionsknoten ausgewertet und ausgeschlossen, falls sie die Bedingung erfüllen.

* **Eine profilbasierte Ausstiegsregel pro Journey**\
  Pro Journey kann nur ein Ausstiegskriterium des Typs „Profilattribut“ definiert werden. Diese Einschränkung hilft, die Klarheit zu bewahren und Konflikte in der Journey-Logik zu vermeiden.

* **Nur in pausierten Journeys verfügbar**\
  Sie können nur dann Ausstiegskriterien des Typs „Profilattribut“ hinzufügen oder bearbeiten, wenn die Journey angehalten wurde.

   * In einem **Entwurf einer Journey** ist die Option *Profilattribut* deaktiviert (schreibgeschützt), während die Optionen *Ereignis* und *Zielgruppe* aktiv bleiben.
   * In einer **angehaltenen Journey** wird die Option *Profilattribut* bearbeitbar, während die Optionen *Ereignis* und *Zielgruppe* schreibgeschützt werden.

### Verwandte Themen {#exit-criteria-related}

* [Leitfaden zu Eintritts- und Ausstiegskriterien für Journeys](entry-exit-criteria-guide.md) – Vollständiger Leitfaden mit Beispielen und Best Practices aus der Praxis
* [Verwaltung des Profileintritts](entry-management.md) – Konfigurieren Sie, wie Profile in Journeys eintreten
* [Beenden von Journeys](end-journey.md) – Erfahren Sie, wie Journeys regulär abgeschlossen werden
* [Pausieren einer Journey mit Profilattribut-Ausstiegskriterien](journey-pause.md#journey-exit-criteria) – Verwenden Sie Ausstiegskriterien beim Pausieren von Journeys

## Journey-Zeitplan {#schedule}

Der Abschnitt **[!UICONTROL Zeitplan]** ist nur dann verfügbar, wenn eine Aktivität vom Typ **[!UICONTROL Zielgruppe lesen]** auf der Arbeitsfläche abgelegt wurde. Darin können Sie Datum, Uhrzeit und Häufigkeit für die Ausführung der Journey festlegen. [Informationen zum Planen einer Journey vom Typ „Zielgruppe lesen“](read-audience.md#schedule)

>[!TIP]
>
>Bei der Planung der Journey können Sie auch den Wave-Versand so konfigurieren, dass Journey-Aktionen im Zeitverlauf stapelweise bereitgestellt werden. [Erfahren Sie, wie Sie mithilfe von Schüben in Journey senden](send-using-waves.md)


## Konflikt-Management {#conflict}

Im Abschnitt **[!UICONTROL Konflikt-Management]** in den Eigenschaften der Journey können Sie Konflikte überwachen und Ihre Journeys priorisieren. Sie haben folgende Möglichkeiten:

* Wenden Sie einen **Regelsatz** an, um diese Journey basierend auf Begrenzungsregeln für einen Teil der Zielgruppe auszuschließen. [Weitere Informationen zum Arbeiten mit Regelsätzen](../conflict-prioritization/rule-sets.md)

* Weisen Sie der Journey einen **Prioritätswert** von 0 bis 100 zu. Eine höhere Zahl bedeutet eine höhere Priorität. Der hier eingegebene Prioritätswert wird von allen eingehenden Aktionen übernommen (beispielsweise In-App-Aktionen), die in dieser Journey enthalten sind. [Informationen zum Arbeiten mit Prioritätswerten](../conflict-prioritization/priority-scores.md)

  In Fällen, in denen dieselbe eingehende Kanalkonfiguration in anderen Kampagnen oder Journeys verwendet wird, wird der Empfängerin bzw. dem Empfänger die eingehende Aktion mit der höchsten Priorität angezeigt. Wenn mehrere Journey oder Kampagnen dasselbe Ergebnis aufweisen, wird das zuletzt geänderte Element ausgewählt.

* **Zeigen Sie Konflikte** mit anderen Journeys, Kampagnen oder Kanalkonfigurationen an. Wenn Sie Überschneidungen bei Zielgruppe, Start- und Enddatum, Kanalkonfiguration oder Kanal oder Regelsatz identifizieren möchten, können Sie hier potenzielle Konflikte anzeigen. [Informationen zum Identifizieren potenzieller Konflikte in Journeys und Kampagnen](../conflict-prioritization/conflicts.md)

## Verwandte Themen {#related-topics}

* [Verwaltung des Profileintritts](entry-management.md) - Konfigurieren, wie Profile in Journey eintreten und erneut eintreten
* [Leitfaden zu Eintritts- und Ausstiegskriterien für Journeys](entry-exit-criteria-guide.md) – Vollständiger Leitfaden mit Beispielen und Best Practices aus der Praxis
* [Wie Journey enden](end-journey.md) - Verstehen Sie die natürliche Journey-Vervollständigung und den Profilaustritt
* [Journey anhalten](journey-pause.md) - Anhalten und Fortsetzen von Journey mit Beendigungskriterien für Profilattribute
* [Zeitzonenverwaltung](timezone-management.md) - Konfigurieren von Journey- und Profil-Zeitzonen
* [Konfliktmanagement und Priorisierung](../conflict-prioritization/conflicts.md) - Identifizieren und Beheben von Konflikten in Journey und Kampagnen
