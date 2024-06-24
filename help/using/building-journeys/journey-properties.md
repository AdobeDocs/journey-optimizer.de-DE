---
solution: Journey Optimizer
product: journey optimizer
title: Definieren der Journey-Eigenschaften
description: Erfahren Sie, wie Sie Eigenschaften Ihrer Journey mit Adobe Journey Optimizer festlegen.
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Konfiguration, Eigenschaften
exl-id: 6c21371c-6cbc-4d39-8fe6-39f1b8b13280
source-git-commit: cb6a3b279158eb065c3dca5436bd992efb79fcff
workflow-type: tm+mt
source-wordcount: '1724'
ht-degree: 32%

---

# Festlegen der Journey-Eigenschaften {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Journey-Eigenschaften"
>abstract="In diesem Abschnitt werden die Journey-Eigenschaften angezeigt. Standardmäßig sind schreibgeschützte Parameter ausgeblendet. Die verfügbaren Einstellungen hängen vom Status der Journey, von Ihren Berechtigungen und der Produktkonfiguration ab."

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Kriterien für den Journey-Austritt"
>abstract="In diesem Abschnitt werden die Optionen für Austrittskriterien angezeigt. Sie können ein oder mehrere Austrittskriterien für Ihre Journey erstellen."


## Zugriff auf die Eigenschaften eines Journey {#access-properties}

Die Eigenschaften einer Journey sind in der rechten Leiste zentralisiert. Dieser Abschnitt wird beim Erstellen einer neuen Journey standardmäßig angezeigt. Für bestehende Journey klicken Sie auf das Stiftsymbol neben dem Journey, um es zu öffnen.

In diesem Abschnitt können Sie den Namen der Journey definieren, eine Beschreibung hinzufügen und:

* verwalten [Eintritt und Wiedereintritt](#entrance),
* Start und Ende auswählen [dates](#dates),
* verwalten [Datenzugriff](#manage-access),
* definieren [Zeitüberschreitungsdauer](#timeout) in Journey-Aktivitäten (nur für Admin-Benutzer),
* Journey und Profil auswählen [timezones](#timezone)
* Weisen Sie Ihrer Journey Adobe Experience Platform Unified Tags zu, um sie einfach zu klassifizieren und die Suche in der Kampagnenliste zu verbessern. [Erfahren Sie, wie Sie mit Tags arbeiten](../start/search-filter-categorize.md#tags)

![](assets/journey32.png)

>[!NOTE]
>
>Bei Live-Journey werden in diesem Bildschirm nur das Veröffentlichungsdatum und der Name des Benutzers angezeigt, der die Journey veröffentlicht hat.

Mit der Schaltfläche **Technische Details kopieren** lassen sich jederzeit technische Informationen zur Journey kopieren, die dem Support-Team bei der Problembehebung helfen. Die folgenden Informationen werden kopiert: `JourneyVersion UID`, `OrgID`, `orgName`, `sandboxName`, `lastDeployedBy`, `lastDeployedAt`.

Erfahren Sie mehr über technische Felder, die mit einer Journey für ein bestimmtes Profil in Verbindung stehen, und wie Sie sie verwenden können. [auf dieser Seite](expression/journey-properties.md).


## Eintritt und Wiedereintritt {#entrance}

Der Profileingabemodus wird auf der Journey-Ebene im rechten Konfigurationsbereich definiert. Die Einstellungen werden unten beschrieben.

Die Verwaltung des Profileintritts hängt vom Typ der Journey ab. Erfahren Sie mehr über die Verwaltung des Eintritts und Wiedereintritts von Profilen in [diese Seite](entry-management.md).

### Wiedereintritt erlauben  {#allow-re-entrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="Wiedereintritt erlauben"
>abstract="Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die **Wiedereintritt erlauben** beispielsweise, wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Laden betritt."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Profileintrittsverwaltung"

Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die Option **Erneuten Eintritt erlauben** für „einmalige“ Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt.

### Wartezeit beim erneuten Eintritt  {#re-entrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="Wartezeit beim erneuten Eintritt"
>abstract=" Legen Sie die Wartezeit fest, bevor Sie einem Profil erlauben, die Journey erneut in einheitlichen Journey aufzurufen. Dadurch wird verhindert, dass Benutzer während eines bestimmten Zeitraums erneut auf die Journey zugreifen. Maximale Dauer: 29 Tage."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Profileintrittsverwaltung"

Wenn die Option **Erneuten Eintritt erlauben** aktiviert ist, wird das Feld **Wartezeit bis zum erneuten Eintritt** angezeigt. In diesem Feld kann die Wartezeit definiert werden, bevor es einem Profil erlaubt wird, in unitären Journeys erneut in die Journey einzutreten (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung). Dadurch wird verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Standardmäßig ist das Feld auf 5 Minuten eingestellt. Die maximale Wartezeit beträgt 90 Tage.


## Verwalten des Zugriffs {#manage-access}

Um der Journey benutzerdefinierte oder Core-Datennutzungsbezeichnungen zuzuweisen, klicken Sie auf die Schaltfläche **[!UICONTROL Zugriff verwalten]**. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

## Zeitzonen von Journeys und Profilen {#timezone}

Die Zeitzone wird auf Journey-Ebene definiert. Sie können eine feste Zeitzone eingeben oder Adobe Experience Platform-Profile verwenden, um die Zeitzone der Journey festzulegen. Wenn eine Zeitzone im Adobe Experience Platform-Profil definiert ist, kann sie in der Journey abgerufen werden.

Weitere Informationen zum Zeitzonen-Management finden Sie auf [dieser Seite](../building-journeys/timezone-management.md).

## Start- und Enddatum {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="Startdatum"
>abstract="Wählen Sie den Datumseintrag in die Journey aus. Wenn kein Startdatum angegeben ist, wird es automatisch zum Zeitpunkt der Veröffentlichung festgelegt."


>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="Enddatum"
>abstract="Wählen Sie das Enddatum Ihres Journey aus. Wenn dieses Datum erreicht ist, werden die Profile in dieser Journey automatisch beendet und neue können nicht mehr in die Datenbank aufgenommen werden."

Sie können ein **Startdatum** festlegen. Wenn Sie dies nicht festgelegt haben, wird es automatisch zum Zeitpunkt der Veröffentlichung definiert.

Sie können außerdem ein **Enddatum** hinzufügen. Dadurch können Profile beim Erreichen des Datums automatisch die Journey verlassen. Wenn kein Enddatum angegeben ist, können Profile bis zum [globales Journey-Timeout](#global_timeout) (in der Regel 91 Tage). Die einzige Ausnahme sind wiederkehrende „Zielgruppe lesen“-Journeys, bei denen die Option **Erneuten Eintritt bei Wiederholung erzwingen** aktiviert ist und die am Startdatum des nächsten Vorkommens enden.

## Zeitüberschreitung {#timeout}

### Zeitüberschreitung oder Fehler in Journey-Aktivitäten {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_timeout"
>title="Zeitüberschreitung"
>abstract="Definieren Sie die Zeitdauer, die die Journey versuchen wird, eine Aktion auszuführen oder eine Bedingung zu überprüfen, bevor sie sie als Zeitüberschreitung betrachtet."


Beim Bearbeiten einer Aktions- oder Bedingungsaktivität können Sie im Falle eines Fehlers oder einer Zeitüberschreitung einen alternativen Pfad definieren. Wenn die Verarbeitung der Aktivität, die ein Drittanbietersystem abfragt, die in **[!UICONTROL Zeitüberschreitung oder Fehler]** -Feld der Journey-Eigenschaften ausgewählt wird, wird der zweite Pfad ausgewählt, um eine potenzielle Ausweichaktion durchzuführen.

Die zulässigen Werte liegen zwischen 1 und 30 Sekunden.

Es wird empfohlen, eine sehr kurze **[!UICONTROL Zeitüberschreitung oder Fehler]** -Wert, wenn Ihre Journey zeitkritisch ist (z. B. Reaktion auf den Echtzeit-Standort einer Person), da Sie Ihre Aktion nicht länger als einige Sekunden verzögern können. Wenn Ihre Journey weniger zeitkritisch ist, können Sie einen längeren Wert verwenden, um dem aufgerufenen System mehr Zeit zum Senden einer gültigen Antwort zu geben.

Journey verwenden auch eine globale Zeitüberschreitung, wie unten beschrieben.

### Maximale globale Wartezeit der Journey {#global_timeout}

Zusätzlich zu den [timeout](#timeout_and_error) wird in Journey-Aktivitäten verwendet, wird ein globales Journey-Timeout angewendet. Sie wird nicht in der Benutzeroberfläche angezeigt und kann nicht geändert werden.

Diese maximale globale Wartezeit stoppt den Fortschritt von Kontakten in der Journey **91 Tage** nach ihrem Eintritt. Das bedeutet, dass die Journey eines Kontakts nicht länger als 91 Tage dauern kann. Nach Ablauf der maximalen Wartezeit werden die Daten des Kontakts gelöscht. Kontakte, die sich nach der maximalen Wartezeit noch in der Journey befinden, werden gestoppt und beim Reporting nicht berücksichtigt. Sie könnten also mehr Personen sehen, die in die Journey eintreten, als Personen, die sie beenden.

Aufgrund der 91-tägigen Journey-Zeitüberschreitung können wir nicht sicherstellen, dass die Sperrung des erneuten Eintritts von Journey mehr als 91 Tage in Kraft tritt. Da wir alle Informationen über Personen, die an der Journey teilgenommen haben, 91 Tage nach deren Eintritt entfernen, können wir nicht wissen, dass die Person vor mehr als 91 Tagen bereits Eintritt hatte.

Eine Person kann nur dann in eine Warteaktivität eintreten, wenn sie genügend Zeit im Journey hat, um die Wartezeit vor dem Journey-Timeout von 91 Tagen abzuschließen. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/wait-activity.md).


#### Häufig gestellte Fragen zur Time-to-Live (TTL) und zur Datenausgabe {#timeout-faq}

Ab Adobe Journey Optimizer-Version vom Juni 2024 wurde das globale Zeitlimit für Journey von 30 auf 91 Tage verschoben. Die Auswirkungen sind in den folgenden häufig gestellten Fragen aufgeführt:

**Für Journey**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit Journey, das veröffentlicht wird, nachdem die TTL-Erweiterung ausgerollt wurde?</p>
    </td>
    <td>
      <p>Profile, die in die neue Journey eintreten, haben automatisch eine TTL von 91 Tagen.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit der Eingabe eines Profils, das vor dem Start der TTL-Erweiterung veröffentlicht wurde?</p>
    </td>
    <td>
      <p>Das Profil verfügt über eine TTL von 91 Tagen (7 Tage für HIPAA), die dem Zeitpunkt entspricht, zu dem die Journey ursprünglich veröffentlicht wurde.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem Profil, das bereits eine Journey eingegeben hat, wenn die TTL-Erweiterung gestartet wird?</p>
    </td>
    <td>
      <p>Das Profil behält gemäß der ursprünglichen Publikationszeit der Journey eine TTL von 91 Tagen (7 Tage für HIPAA) bei.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem Profil in einer früheren Journey-Version, die nach dem Start der TTL-Erweiterung erneut veröffentlicht wird?</p>
    </td>
    <td>
      <p>Das Profil behält eine TTL von 91 Tagen (7 Tage für HIPAA), die mit der Veröffentlichungszeit der ursprünglichen Journey-Version abgestimmt ist.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem neuen Profil, das nach dem Start der TTL-Erweiterung eine erneut veröffentlichte Journey-Version eingibt?</p>
    </td>
    <td>
      <p>Das Profil verfügt über eine TTL von 91 Tagen, die der TTL der neu veröffentlichten Journey-Version entspricht.</p>
    </td>
  </tr>
</table>

**Für Segment-Trigger-Journey**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit neuen einmaligen Journey, die nach der TTL-Erweiterung veröffentlicht werden?</p>
    </td>
    <td>
      <p>Profile, die in die neue Journey eintreten, haben automatisch eine TTL von 91 Tagen.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit neuen wiederkehrenden Journey ohne erzwungenen erneuten Eintritt, die nach der TTL-Erweiterung veröffentlicht werden?</p>
    </td>
    <td>
      <p>Profile, die in die neue Journey eintreten, haben automatisch eine TTL von 91 Tagen.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit neuen wiederkehrenden Journey mit erzwungener Wiedereinreise, die nach der TTL-Erweiterung veröffentlicht werden?</p>
    </td>
    <td>
      <p>Profile, die die neue Journey eingeben, haben eine TTL, die der Wiederholungszeit entspricht. Wenn die Journey beispielsweise täglich ausgeführt wird, beträgt die TTL 1 Tag.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit der Eingabe eines Profils, das vor dem Start der TTL-Erweiterung veröffentlicht wurde?</p>
    </td>
    <td>
      <p>Das Profil verfügt über eine TTL von 91 Tagen (7 Tage für HIPAA), die der ursprünglichen Veröffentlichungszeit entspricht. Bei wiederkehrenden Journey mit erzwungenem Wiedereintritt entspricht die TTL der Wiederholungszeit.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem Profil, das über eine Journey läuft, wenn die TTL-Erweiterung gestartet wird?</p>
    </td>
    <td>
      <p>Das Profil behält gemäß der ursprünglichen Publikationszeit der Journey eine TTL von 91 Tagen (7 Tage für HIPAA) bei. Bei wiederkehrenden Journey mit erzwungenem Wiedereintritt entspricht die TTL der Wiederholungszeit.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem laufenden Profil in einer vorherigen Journey-Version, die nach dem Start der TTL-Erweiterung erneut veröffentlicht wird?</p>
    </td>
    <td>
      <p>Das Profil behält eine TTL von 91 Tagen (7 Tage für HIPPA), die mit der Veröffentlichungszeit der ursprünglichen Journey-Version abgestimmt ist. Bei wiederkehrenden Journey mit erzwungenem Wiedereintritt entspricht die TTL der Wiederholungszeit.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Was passiert mit einem neuen Profil, das nach dem Start der TTL-Erweiterung eine erneut veröffentlichte Journey-Version eingibt?</p>
    </td>
    <td>
      <p>Das Profil verfügt über eine TTL von 91 Tagen, die der TTL der neu veröffentlichten Journey-Version entspricht. Bei wiederkehrenden Journey mit erzwungenem Wiedereintritt entspricht die TTL der Wiederholungszeit.</p>
    </td>
  </tr>
</table>

## Zusammenführungsrichtlinien {#merge-policies}

Eine Journey verwendet Zusammenführungsrichtlinien beim Abrufen von Profildaten von Adobe Experience Platform. Je nach Journey-Typ werden unterschiedliche Zusammenführungsrichtlinien verwendet:

* In den Journeys „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ wird die Zusammenführungsrichtlinie aus der Zielgruppe verwendet
* In Journey mit Einzelereignissen wird die standardmäßige Zusammenführungsrichtlinie verwendet
* In Business Event Journey: Die Zusammenführungsrichtlinie aus der Zielgruppe wird in der folgenden Lesen der Audience -Aktivität verwendet

Journey berücksichtigt die auf der gesamten Journey verwendete Zusammenführungsrichtlinie. Wenn also mehrere Zielgruppen in einer Journey verwendet werden (z. B. in &quot;inAudience&quot;-Funktionen) und Inkonsistenzen mit der von der Journey verwendeten Zusammenführungsrichtlinie entstehen, wird ein Fehler erzeugt und die Veröffentlichung blockiert. Wenn jedoch bei der Nachrichtenpersonalisierung eine inkonsistente Zielgruppe verwendet wird, wird trotz der Inkonsistenz kein Warnhinweis erzeugt. Daher wird dringend empfohlen, die mit Ihrer Audience verknüpfte Zusammenführungsrichtlinie zu überprüfen, wenn diese Audience bei der Nachrichtenpersonalisierung verwendet wird.

Weitere Informationen zu Zusammenführungsrichtlinien finden Sie unter [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.
