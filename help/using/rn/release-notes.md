---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: e0a12bd7971c778378f9905cf93653792f38509d
workflow-type: tm+mt
source-wordcount: 2279
ht-degree: 40%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** stellt regelmäßig neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen zur Verfügung. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht ein skalierbares Rollout von Funktionen in Phasen, um die Leistung und Stabilität aller Umgebungen sicherzustellen. Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

>[!NOTE]
>
>Die in diesen Versionshinweisen aufgeführten Funktionen umfassen ein **Verfügbarkeitsdatum**, das angibt, wann jede Änderung in Ihrer Umgebung verfügbar wird. Einträge in den Akkordeons **Demnächst verfügbar** werden in den kommenden Tagen oder Wochen erwartet. Informationen in diesen Abschnitten können Änderungen unterliegen.

## Versionshinweise Juni 2026 {#june-26-rn}

Die Version vom Juni 2026 bietet mehrere Flaggschiff-Funktionen für die allgemeine Verfügbarkeit - darunter **Journey-Simulation**, **Journey-Pfadoptimierungs-Targeting** und **Journey-Fragmente** - sowie neues KI-unterstütztes Authoring in Journey und Inhalten, erweiterte Entscheidungsunterstützung für den Briefpostkanal und zusätzliche Sicherheits- und Verwaltungssteuerelemente. Die folgenden Funktionen und Verbesserungen sind nach Themen geordnet. Weitere Änderungen werden auch in den kommenden Tagen oder Wochen erwartet.

### Journeys {#june-26-journeys}

Die folgenden Funktionen und Verbesserungen wurden in dieser Version zu Journeys hinzugefügt. Weitere Änderungen werden auch in den kommenden Tagen oder Wochen erwartet.


<table>
<thead>
<tr>
<th><strong>Journey-Simulation (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Jetzt können Sie Ihren Journey auf Simulation einstellen. In diesem Modus können Sie Ihre Logik mithilfe simulierter Benutzer überprüfen. Dies sind temporäre, speziell für die Simulation erstellte Profile, mit denen Sie frei testen können. So müssen Sie keine dauerhaften Testprofile in Adobe Experience Platform verwalten. </p>
<p>Journey-Simulation wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung. Mit dieser allgemeinen Verfügbarkeit können Sie jetzt Journey Agent verwenden, um simulierte Benutzende und Ereignisse direkt im Simulationsmenü zu generieren.</p>
<p><img src="assets/do-not-localize/journey-simulation.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/simulate-journey-gs.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 9. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Fragments (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>Journey-Fragmente</strong> in Adobe Journey Optimizer erstellen. Journey-Fragmente sind wiederverwendbare Sätze von Journey-Knoten, die Sie einmal erstellen und in einer beliebigen Journey in Ihrer Sandbox ablegen können. Unabhängig davon, ob es sich um eine Eignungsprüfung, eine bevorzugte Kanal-Routing-Logik oder eine Begrüßungssequenz handelt, helfen Fragmente Teams dabei, schneller und konsistent zu arbeiten, ohne dieselbe Logik jedes Mal von Grund auf neu zu erstellen.</p>
<p>Nach der Erstellung werden Fragmente in einem dedizierten <strong>Fragmentinventar</strong> gespeichert und können mithilfe der Aktivität <strong>Journey-Fragmente</strong> in Journeys eingefügt werden.</p>
<p>Diese Funktion war bisher nur in begrenzter Verfügbarkeit verfügbar und steht nun allgemein allen Kunden zur Verfügung. Journey-Fragmente unterstützen auch <strong>Sandbox-Tools</strong> mit denen Sie Fragmente über Sandboxes hinweg verpacken und exportieren können.</p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/journey-fragments.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 9. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Pfadoptimierung - Targeting (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die <strong>Optimierungsaktivität</strong> unterstützt jetzt <strong>Targeting-Regeln</strong> mit denen Sie spezifische Kriterien definieren können, die Kundinnen und Kunden erfüllen müssen, um sich basierend auf Zielgruppensegmenten oder Profilattributen für einen bestimmten Journey-Pfad zu qualifizieren.</p>
<p>Im Gegensatz zu Experimenten, bei denen Kundinnen und Kunden nach dem Zufallsprinzip Pfaden zugewiesen werden, verwendet das Targeting deterministische Logik, um sicherzustellen, dass die entsprechende Zielgruppe oder das entsprechende Kundenprofil zum gewünschten Pfad weitergeleitet wird.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/optimize.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/path-targeting.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 8. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>KI-Assistent für Journey-Ausdrücke (öffentliche Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der KI-Assistent arbeitet jetzt im erweiterten Ausdruckseditor von Journeys, um Prompts in natürlicher Sprache in gültige Ausdrücke und Bedingungslogik zu konvertieren. Beschreiben Sie die gewünschte Personalisierung und die KI generiert einsatzbereiten Code, den Sie sofort anwenden oder durch Folge-Prompts verfeinern können.</p>
<p>Diese Funktion steht allen Kundinnen und Kunden als öffentliche Beta-Version zur Verfügung.</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/expression/expression-agent.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 3. Juni 2026</p> 
</td>
</tr>
</tbody>
</table>

* **Zusätzliche Kennungsunterstützung für externe Zielgruppen** – Zusätzliche Kennungen in Journeys werden jetzt für externe Zielgruppen unterstützt, einschließlich Zielgruppen, die aus einer CSV-Datei importiert wurden, und Zielgruppen, die mit der Komposition föderierter Zielgruppen erstellt wurden. Sie können ein beliebiges Nicht-Identitätsattribut oder ein beliebiges Identitätsattribut aus der Zielgruppe als zusätzliche ID festlegen. Eine Schemakennzeichnung ist nicht erforderlich. [Weitere Informationen](../building-journeys/supplemental-identifier.md)

  Verfügbarkeitsdatum: 11. Juni 2026

* **Automatischer Stopp für nicht wiederkehrende Journey des Typs „Zielgruppe lesen** - Nicht wiederkehrende **Zielgruppe lesen** Journey wechseln jetzt automatisch in den Status **Angehalten**, sobald das letzte aktive Profil beendet wurde. Zuvor blieben diese Journeys bis zum Ablauf der 91-tägigen globalen maximalen Wartezeit **live**, selbst wenn sie nicht mehr von Profilen durchlaufen wurden. Mit dieser Verbesserung spiegelt der Journey-Status den tatsächlichen Ausführungsstatus nach Abschluss wider, sodass der Journey-Bestand ohne manuelles Eingreifen stets korrekt ist.

  Beachten Sie, dass dieses Verhalten nicht für Journeys mit Knoten gilt, die Wartezeiten verursachen, z. B. Warteknoten, Reaktionsknoten oder durch Ereignisse ausgelöste Transitionen. Diese Journeys unterliegen weiterhin dem standardmäßigen globalen Timeout von 91 Tagen. [Weitere Informationen](../building-journeys/end-journey.md#auto-stop-non-recurring)

  Verfügbarkeitsdatum: 9. Juni 2026

* **Zertifikatbasierte benutzerdefinierte Authentifizierung in benutzerdefinierten Aktionen** – Benutzerdefinierte Aktionen unterstützen jetzt die zertifikatbasierte benutzerdefinierte Authentifizierung. Durch das Hinzufügen von `subType: "certificateCredential"` zu einer benutzerdefinierten Autorisierungskonfiguration verwendet Journey Optimizer das verwaltete Zertifikat von Adobe, um eine JWT-Client-Bestätigung zu signieren und sie gegen ein Zugriffstoken einzutauschen – kein Client-Geheimnis erforderlich. Entwickelt für Unternehmens-APIs, die eine zertifikatbasierte Identitätsüberprüfung erzwingen, z. B. die Microsoft Entra ID. [Weitere Informationen](../datasource/external-data-sources.md#certificate-credential)

  Verfügbarkeitsdatum: 4. Juni 2026

### Orchestrierte Kampagnen {#june-26-oc}

Orchestrierte Kampagnen in dieser Version weisen die folgenden Funktionen und Verbesserungen auf.

+++ Demnächst verfügbar - **Informationen unten können sich ändern.**

<table>
<thead>
<tr>
<th><strong>Dateibasiertes Targeting in koordinierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrierte Kampagnen unterstützen jetzt das Laden einer <strong>CSV- oder TXT-Datei</strong> direkt in die Kampagnen-Arbeitsfläche als Zielgruppe, ohne die Datei zuerst in Adobe Experience Platform aufzunehmen. Die Dateidaten werden zur Ausführungszeit genutzt und nicht als Adobe Experience Platform-Datensatz beibehalten. Während der Dateieinrichtung können Sie Spaltenzuordnungen, Datentypen, die NULL-Verarbeitung und Fehlerrichtlinien pro Spalte definieren. Zeilen, die bei der Validierung fehlschlagen, werden abgelehnt und protokolliert, bevor die Kampagne ausgeführt wird. Dadurch wird die Zielgruppe ohne manuelle Vorverarbeitung sauber gehalten. Dies eignet sich besonders für Ad-hoc-Sendungen oder Partnerlisten-Kampagnen, bei denen der Aufbau einer vollständigen Aufnahme-Pipeline nicht praktisch ist.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p> Verfügbarkeitsdatum: 30. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

* **Schleifenbasierte Personalisierung für relationale Daten** - Der Personalisierungseditor unterstützt jetzt einen Schleifenblock, der relationale Sammlungen wie Bestellungen, Konten oder Buchungen durchläuft und einen Inhaltsblock pro Datensatz in einer einzelnen E-Mail oder SMS rendert. Sammlungen werden über die Datenauswahl mithilfe von Personalisierungs-Token konfiguriert, ohne dass ein Ausdruck geschrieben werden muss. [Weitere Informationen](../orchestrated/add-personalization.md#enrichment-collections)

  Verfügbarkeitsdatum: Ende Juni 2026

+++

### Entscheidungsfindung {#june-26-decisioning}

In dieser Version wurden die folgenden Funktionen und Verbesserungen zur Entscheidungsfindung hinzugefügt.

<table>
<thead>
<tr>
<th><strong>Unterstützung von Entscheidungen im Direkt-Mail-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Entscheidungsrichtlinien zu Direkt-Mail-Journeys und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Angebote, die die Entscheidungs-Engine nutzen, um für jedes Zielgruppenmitglied die besten Inhalte bereitzustellen. Die Direkt-Mail-Entscheidungsfindung unterstützt auch Anwendungsfälle für Batch-Entscheidungen, mit denen Sie die entsprechenden Angebotselemente für jedes Profil in einer bestimmten Adobe Experience Platform-Zielgruppe exportieren können. </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../experience-decisioning/use-decision-policy.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 3. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Demnächst verfügbar - **Informationen unten können sich ändern.**

* **Dynamische Elementattribute** - Benutzerdefinierte Attribute von Entscheidungselementen können jetzt zur Versandzeit mithilfe von Profil-, Kontext- und Zielgruppendaten personalisiert werden. Dadurch entfällt die Notwendigkeit, doppelte Angebote für kleinere Inhaltsvarianten zu verwalten, sodass Marketer weniger, flexiblere Entscheidungselemente verwalten können.

+++

### Content-Management {#june-26-content}

In dieser Version wurden die folgenden Funktionen und Verbesserungen zum Content-Management hinzugefügt.

<table>
<thead>
<tr>
<th><strong>Simulieren von Inhaltsvarianten - Generieren aktualisierter Erlebnisse und KI-Varianten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Für den Workflow <strong>Inhalt simulieren“ sind jetzt zwei </strong> verfügbar:</p>
<ul>
<li><strong>Neuer Standardpfad</strong> - Wenn Sie auf <strong>Inhalt simulieren</strong> klicken, wird jetzt <strong> Erlebnis „Inhaltsvarianten simulieren</strong> geöffnet. Sie können auf einem einzigen Bildschirm Beispieleingaben manuell oder aus einer CSV-/JSON-Datei hinzufügen, simulierte Benutzer wiederverwenden, das Rendering in der Vorschau anzeigen und Testsendungen durchführen. Um eine Vorschau mit Adobe Experience Platform-Testprofilen anzuzeigen, Testsendungen mit Testprofildaten durchzuführen oder E-Mail-Posteingang - Rendering und Spam-Berichte zu überprüfen, klicken Sie auf <strong>Inhalt simulieren</strong> und wählen Sie dann <strong>Inhalt simulieren (AEP-Profile)</strong> aus der Dropdown-Liste aus.</li>
<li><strong>KI-generierte Inhaltsvarianten</strong> - Klicken Sie im Erlebnis <strong>Inhaltsvarianten simulieren</strong> auf <strong>Generieren</strong>, um KI zum automatischen Erstellen von Inhaltsvarianten zu verwenden. Das System analysiert Ihre Nachricht, erkennt Personalisierungsfelder und bedingte Verzweigungen und füllt realistische Werte aus, sodass Sie das Rendering überprüfen können, ohne jede Variante von Hand erstellen zu müssen.</li>
</ul>
<p>Weitere Informationen finden Sie im <a href="../test-approve/simulate-sample-input.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 9. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

### E-Mail-Kanal {#june-26-email}

In dieser Version wurden die folgenden Verbesserungen zum E-Mail-Kanal hinzugefügt.

* **URL-Parameterverschlüsselung** – Sie können jetzt URL-Parameter in Tracking- und Landingpage-Links verschlüsseln, die Ihren E-Mail-Nachrichten hinzugefügt werden. Dies bietet eine zusätzliche Sicherheitsebene für vertrauliche Parameterdaten. Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit). [Weitere Informationen](../personalization/url-parameter-encryption.md)

  Verfügbarkeitsdatum: 1. Juni 2026

* **Neue Berechtigungen für die Schlüsselregistrierung** – Für den Zugriff auf und die Verwaltung der für die URL-Parameterverschlüsselung erforderlichen Schlüssel sind jetzt zwei neue Berechtigungen erforderlich: **Schlüsselregistrierung verwalten** und **Schlüsselregistrierung anzeigen**. [Weitere Informationen](../administration/high-low-permissions.md#administration-permissions)

  Verfügbarkeitsdatum: 1. Juni 2026

+++ Demnächst verfügbar – **Die Informationen unten können sich ändern.**

<table>
<thead>
<tr>
<th><strong>Qualitätsprüfungen von Inhalten in der E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet jetzt eine automatisierte technische Validierung direkt in der E-Mail-Designer, mit der Sie HTML- und CSS-Probleme vor dem Versand erfassen können.</p>
<p>Die Prüfungen umfassen nicht unterstützte Elemente wie <code>&lt;script&gt;</code>- und <code>&lt;base&gt;</code>-Tags, leere div-Tags, die das Layout in Microsoft Outlook beschädigen können, Meta-Aktualisierungs-Tags von HTML und CSS- oder HTML-Größenschwellen, die Trigger-Rendering-Fehler in Gmail verursachen.</p>
<p>Ergebnisse werden direkt im Authoring-Bereich als Fehler, Warnungen oder informative Hinweise angezeigt. Dort sind kontextuelle Details und Fehlerbehebungen mit einem Klick verfügbar, sodass Probleme gelöst werden können, ohne den Editor zu verlassen.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reduzierung der E-Mail-Größe aktivieren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet jetzt eine Option, die HTML Ihrer E-Mail zu verkleinern, indem unnötige Leerzeichen, Kommentare und redundanter Code entfernt werden - ohne die Darstellung der E-Mail zu beeinflussen.</p>
<p>Dies kann die Zustellbarkeit verbessern, indem Größenschwellen vermieden werden, die einige E-Mail-Anbieter zum Kennzeichnen oder Ablehnen von Nachrichten verwenden, und kann die Ladezeit für Empfänger verkürzen.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rich-Text in bearbeitbaren Feldern für Fragmente</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Rich-Text zu anpassbaren Fragmenten hinzufügen, die in Ihren E-Mail-Inhalten verwendet werden.</p>
<p>Wenn Sie beispielsweise die Textkomponente als bearbeitbares Feld in der E-Mail-Designer verwenden, können Sie den Inhalt direkt formatieren (z. B. fett und kursiv) und Hyperlinks einfügen.</p>
</td>
</tr>
</tbody>
</table>

+++

### Inhalte und Integrationen {#june-26-integration}

In dieser Version werden die folgenden Funktionen und Verbesserungen bei Content-Management und Integrationen eingeführt.

+++ Demnächst verfügbar - **Informationen unten können sich ändern.**

<table>
<thead>
<tr>
<th><strong>Verbesserungen an Adobe Experience Manager-Inhaltsfragmenten in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Diese Version bietet mehrere Verbesserungen, um <strong>Adobe Experience Manager</strong>Inhaltsfragmente innerhalb von Journey Optimizer-Authoring-Workflows nutzbarer, besser kontrollierbar und produktionsbereiter zu machen:</p>
<ul>
<li>Journey Optimizer unterstützt jetzt das Abrufen von Inhaltsfragmenten aus mehreren Adobe Experience Manager-Konfigurationen, einschließlich der Autoren-, Veröffentlichungs- und authentifizierten Veröffentlichungsebenen.</li>
<li>Sobald ein Fragment ausgewählt wurde, wird sein Kontext in der gesamten Nachricht beibehalten, sodass Autoren Fragmentfelder über Inhaltsblöcke hinweg wiederverwenden können, ohne die Auswahl erneut durchzuführen.</li>
<li>In Journey Optimizer wurde eine neue spezielle Seite zur Auflistung von Inhaltsfragmenten eingeführt, um die Lebenszyklusverwaltung zu verbessern. Benutzende können nicht synchronisierte Fragmente und manuelle Synchronisierungen von Triggern identifizieren, um auf dem neuesten Stand zu bleiben.</li>
<li>Die Unterstützung von Gebietsschemata und Varianten ermöglicht es Marketing-Experten jetzt, gezielter mit alternativen Versionen desselben Inhaltsfragments zu arbeiten.</li>
<li>Sie können jetzt flexibel darauf zugreifen, wie Adobe Journey Optimizer auf Ihre Adobe Experience Manager-Inhalte zugreift. Diese Version bietet die Möglichkeit, <strong> Quell-Repository für Inhaltsfragmente </strong> wechseln, die in Ihren Journey und Kampagnen verwendet werden.</li>
<li>Jetzt, mit <b>Managed Services</b> kompatibel, können Sie Adobe Experience Manager-Inhaltsfragmente direkt in Journey Optimizer anzeigen, darauf zugreifen und sie zur Personalisierung verwenden. Fügen Sie einfach Ihre Adobe Experience Manager Managed Services-Repository-URL in den Konfigurationseinstellungen als einmaliges Setup hinzu.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integration des KI-Assistenten mit Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der KI-Assistent ruft jetzt automatisch <b>markenbestätigte Bilder</b> direkt aus Ihrer Adobe Experience Manager Assets ab, wenn E-Mails, Web-Seiten und Push-Benachrichtigungen generiert werden. Dadurch entfällt die Notwendigkeit, die Assets manuell zu durchsuchen oder sich auf generische KI-Fallbacks zu verlassen, um sicherzustellen, dass jedes Bild perfekt präzise und markenkonform ist.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verbesserungen am KI-Assistenten für die Inhaltserstellung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Diese Version verbessert das <strong>KI-Assistent</strong> Erlebnis der Inhaltserstellung mit stärkerer Bildbearbeitung, zuverlässigerer Markenextraktion und Unterstützung der Inhaltsauthentizität im Bildfluss:</p>
<ul>
<li><strong>KI-Bildbearbeitung</strong> ist jetzt im Bildgenerierungsfluss verfügbar, einschließlich Unterstützung für Firefly-Drittanbietermodelle, sodass Sie Quellbilder verfeinern können, ohne den Assistenten zu verlassen.</li>
<li><strong>Markensignalextraktion</strong> liefert bessere Ergebnisse. Wenn für ausgewählte Seiten kein ausreichendes Signal vorhanden ist, werden durch verbesserte Fallbacks nun Farben, Typografie, Schreibrichtlinien und andere Markenattribute aufgefüllt.</li>
<li><strong>Web-basierte Markenextraktion</strong> ist zuverlässiger. Die verbesserte Zeitüberschreitungsverwaltung verhindert, dass langsame Seiten, Popups und Cookie-Banner die Extraktion blockieren.</li>
<li><strong>Inhaltsauthentizität (CAI</strong> wird jetzt im Bildfluss unterstützt. Diese Version behebt außerdem Probleme beim Hochladen von Referenzbildern und verbessert die Handhabung für Bilder ohne vorhandenes C2PA-Manifest.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++

### Administration {#june-26-administration}

In dieser Version wurden die folgenden Verbesserungen zur Verwaltung und Datenverwaltung hinzugefügt.

* [!BADGE Wichtig]{type=Informative} **AJO-Nachrichten-Feedback-Ereignisdatensatz, der zur Batch-Aufnahme** wird - Der **AJO-Nachrichten-Feedback-** Ereignisdatensatz) wechselt von der Streaming-Aufnahme zur Batch-Aufnahme. Erwarten Sie daher für diesen Datensatz eine Datenlatenz von bis zu 2 Stunden. Wenn Sie Berichte in Customer Journey Analytics erstellt haben oder Abfragen mithilfe dieses Datensatzes ausführen, berücksichtigen Sie in Zukunft diese erhöhte Latenz. [Weitere Informationen](../data/datasets-query-examples.md#message-feedback-event-dataset)

  Verfügbarkeitsdatum: 10. Juni 2026

* **Kundenwarnungen für Kampagnen-Lebenszyklus-Ereignisse** – Neue Systemwarnungen benachrichtigen Sie jetzt über wichtige Lebenszyklus-Ereignisse für Aktionen und durch API ausgelöste Kampagnen. Abonnieren Sie auf Sandbox-Ebene. [Weitere Informationen](../reports/alerts.md)

  Verfügbarkeitsdatum: 1. Juni 2026

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->
