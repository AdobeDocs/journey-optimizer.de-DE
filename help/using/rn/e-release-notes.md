---
solution: Journey Optimizer
product: journey optimizer
title: Vorab veröffentlichte Versionshinweise zu Journey Optimizer
description: Vorab veröffentlichte Versionshinweise zu Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: f06a9d01721ff23dfdf95db8d984143bb36fe85c
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 41%

---

# Vorab veröffentlichte Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.


## Hinweise zur Vorabversion vom Oktober 2025 {#25-10-rn}

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden in den Versionshinweisen am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: 21.-22. Oktober 2025

### Neue Funktionen {#oct-25-10-features}



<table>
<thead>
<tr>
<th><strong>Überwachung und Reporting für benutzerdefinierte Aktionen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Diese Funktion bietet eine verbesserte Sichtbarkeit hinsichtlich des Zustands und der Ausführung von Journeys, einschließlich Lebenszyklusstatus- und Leistungswarnungen. Sie können jetzt schnell nachvollziehen, wann, wo und warum eine ungewöhnliche Situation in einer benutzerdefinierten Aktion auftritt.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem neuen Add-on RCS Basic können Sie nun Rich Communication Services (RCS)-Basisnachrichten in Journey Optimizer bereitstellen, um je nach Anbieter und geografischer Unterstützung die folgenden erweiterten Messaging-Funktionen zu ermöglichen:</p>
<ul>
<li><strong>Unterstützung für gebrandete und verifizierte Absender:</strong> Senden Sie Nachrichten mithilfe verifizierter Geschäftsprofile mit Branding-Elementen (Logo, Absendername usw.).</li>
<li><strong>Nachrichtenversand-Einblicke:</strong> Sie erhalten detaillierte Versandberichte einschließlich Statusaktualisierungen der Nachricht (z. B. gesendet, zugestellt, gelesen).</li>
<li><strong>Linktracking:</strong> Einbetten und Verfolgen von URLs in RCS-Nachrichten für Interaktionsanalysen.</li>
<li><strong>Fallback auf SMS:</strong> Automatisches Fallback auf SMS, wenn das Gerät des Empfängers RCS nicht unterstützt oder über RCS vorübergehend nicht erreichbar ist.</li>
<li><strong>Einfache Nachrichtenkomposition:</strong> Senden Sie einfache textbasierte RCS-Nachrichten.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Briefpost-Kanal in orchestrierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Briefpost-Kanal ist jetzt in orchestrierten Kampagnen verfügbar. Die Direkt-Mail-Aktivität erleichtert den Direkt-Mail-Versand innerhalb der orchestrierten Kampagne und ermöglicht sowohl einmalige als auch wiederkehrende Nachrichten. Sie dient dazu, das Generieren der von Direkt-Mail-Dienstleistern benötigten Extraktionsdatei zu automatisieren. Kanalaktivitäten können in der Arbeitsoberfläche für orchestrierte Kampagnen kombiniert werden, um kanalübergreifende Kampagnen zu erstellen, mit denen basierend auf Kundenverhalten und Daten Aktionen ausgelöst werden können.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Briefpost-Kanal in Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zuvor auf Kampagnen beschränkt, ist der Briefpostkanal jetzt auf der Journey-Arbeitsfläche verfügbar, sodass Sie Briefpost in Ihre Journey integrieren können. Briefpost kann jetzt sowohl in Batch- als auch in 1:1-Journey-Szenarien verwendet werden, mit Unterstützung für die Dateiextraktionskonfiguration und zeitbasierte Häufigkeitseinstellungen.</p>
<p> Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Neue API zum Abrufen von Aktionskampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Journey Optimizer-API ist jetzt verfügbar, mit der Sie kampagnenbezogene Daten wie Details, Versionen und Konfigurationen programmgesteuert abrufen und überprüfen können.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Neue Quell-Connectoren für Treue-Apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Adobe Experience Platform sind jetzt neue Quell-Connectoren für die Treueprogramme von Talon.One, Capillary und Kobie verfügbar. Mit diesen Connectoren können Sie Treueprogramm-Daten nahtlos in Adobe Experience Platform streamen und diese Daten in Journey Optimizer nutzen.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Unterstützung von Entscheidungen im E-Mail-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Entscheidungsrichtlinien zu E-Mail-Journeys und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Angebote, die die Entscheidungs-Engine nutzen, um für jedes Zielgruppenmitglied die besten Inhalte bereitzustellen.</p>
<p> Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Hoher Durchsatzmodus für API-ausgelöste E-Mail-Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Für Kampagnen, die durch API ausgelöst werden, ist jetzt ein neuer Modus mit hohem Durchsatz verfügbar. Dieser Modus ist für groß angelegtes Echtzeit-Messaging konzipiert (bis zu 5.000 Transaktionen pro Sekunde) und bietet eine höhere Verfügbarkeit bei geringerer Latenz.</p>
<p>Diese Funktion ist nur für den E-Mail-Kanal verfügbar und steht Unternehmen zur Verfügung, die das Adobe Add-on für Transaktionsnachrichten mit hohem Durchsatz erworben haben. Weitere Informationen erhalten Sie beim Adobe-Support.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ruhige Stunden/zeitbasierte Ausschlüsse</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit der Einstellung „Ruhige Stunden“ können Sie zeitbasierte Ausschlüsse für E-Mail-, SMS-, Push- und WhatsApp-Kanäle definieren. Sie stellen sicher, dass während bestimmter Zeiträume keine Nachrichten gesendet werden, und helfen Ihnen so, Kundenpräferenzen und Compliance-Anforderungen zu erfüllen.</p>
<p>Ruhestunden können über Regelsätze angewendet werden, die zur präzisen Steuerung Einzelaktionen in Kampagnen oder Journey zugewiesen werden können. Durch die Optimierung dieser Prozesse.</p>
<p>Diese Funktion ist nur für eine ausgewählte Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr>
<th><strong>Metadaten-Assistent für die Ausführung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Hilfsfunktion „executionMetadata“ ist im Personalisierungseditor verfügbar. Damit können Sie kontextuelle Informationen an jede native Aktion anhängen und sie in einem Datensatz erfassen, um sie in externe Systeme zu exportieren.</p>
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
<p>Weitere Informationen finden Sie in der <a href="../personalization/functions/helpers.md#execution-metadata">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 13. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentieragent ist hier!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit <a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator </a> ist der Experimentationsagent in Journey Optimizer verfügbar. </p>
<p>Der Experimentierungs-Agent ist ein KI-gestütztes Tool, das die Ausführung und Verwaltung digitaler Experimente auf Websites, E-Mails, Push-Nachrichten und Anwendungen modernisiert. Sie hilft Ihnen, Experimente effizienter durchzuführen, Geschäftsziele zu organisieren und umsetzbare Einblicke zu generieren, indem sie hervorhebt, was funktioniert hat, was nicht und wo Sie als Nächstes experimentieren können.</p>
<p>Weitere Informationen finden Sie in der <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=de" target="_blank">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 10. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>PDF-Anhänge an E-Mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt eine statische PDF-Datei an eine mit Journey Optimizer gesendete E-Mail anhängen.</p>
<ul>
<li>Pro Profil können pro Jahr bis zu 6 Nachrichten mit einem PDF-Anhang gesendet werden.</li>
<li>Die maximale Dateigröße pro Anhang beträgt 5 MB.</li>
<li>Für zusätzliche Größen oder Volumen können Sie das Add-on für PDF-Anhänge erwerben. Weitere Informationen erhalten Sie beim Adobe-Support.</li>
</ul>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../email/pdf-attachments.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 30. September 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Öffentliche API zum Abrufen von Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Journey Optimizer-API ist jetzt verfügbar, um Journey und ihre zugehörigen Objekte wie Kampagnen und Oberflächen abzurufen.</p>
<p>Weitere Informationen finden Sie in der <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 25. September 2025</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen

**Wiederverwendbare Regeln in der Zielgruppenbestimmung auswählen**

Sie können jetzt den Regel-Builder bei der Verwendung von Targeting-Regeln mit der Funktion „Nachrichtenoptimierung“ in Journey und Kampagnen nutzen. <!-- [Read more](../FILE.md) -->

**Ausführungsfeld für WhatsApp-Kanal**

Zusätzlich zu E-Mail und SMS ist es jetzt möglich, das Standard-Ausführungsfeld von WhatsApp zu aktualisieren. Es ist auch möglich, das Ausführungsfeld, das in den erweiterten Parametern der WhatsApp-Journey-Aktivität oder in der WhatsApp-Kanalkonfiguration global festgelegt ist, zu überschreiben. <!-- [Read more](../FILE.md) -->

**Berechtigungen**

**Neue Journey-Warnhinweise**

Für Journey sind neue vorkonfigurierte Warnhinweise verfügbar: [Profilverwerfungsrate überschritten](../reports/alerts.md#alert-discard-rate) (Verhältnis von Profilverwerfen zu eingegebenen Profilen in den letzten 5 Minuten überschritten), [Fehlerrate für benutzerdefinierte Aktion überschritten](../reports/alerts.md#alert-custom-action-error-rate) (Verhältnis von Fehlern bei benutzerdefinierten Aktionen zu erfolgreichen HTTP-Aufrufen in den letzten 5 Minuten überschritten) und [Profilfehlerrate überschritten](../reports/alerts.md#alert-profile-error-rate) (Verhältnis von fehlerhaften Profilen zu eingegebenen Profilen in den letzten 5 Minuten überschritten). Sie können Schwellenwerte anpassen und Warnhinweise entweder auf Journey-Ebene oder global abonnieren.

Verfügbarkeitsdatum: 14. Oktober 2025

**Unterstützung benutzerdefinierter Attribute für Mailto-Adresse (abmelden)**

Wenn Sie mit Journey Optimizer das Einverständnis außerhalb von Adobe verwalten, können Sie externe benutzerdefinierte Endpunkte festlegen, indem Sie Ihren eigenen Ein-Klick-Abmelde-Link und eine benutzerdefinierte Abmelde-E-Mail-Adresse in der E-Mail-Konfiguration definieren. Wenn Ihre Empfängerinnen oder Empfänger auf den Link zum Abmelden klicken, fügt Journey Optimizer standardmäßige profilspezifische Parameter an das Einverständnisaktualisierungsereignis an.

Um Ihre benutzerdefinierten Endpunkte weiter zu personalisieren, können Sie jetzt benutzerdefinierte Attribute definieren, die auch an das Einverständnisereignis angehängt werden. [Weitere Informationen](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Diese Funktion ist bereits seit dem 25. August für die benutzerdefinierte URL **[!UICONTROL Ein-Klick-Abmelde]** verfügbar und jetzt für die Option **[!UICONTROL Mailto (unsubscribe)]** in begrenzter Verfügbarkeit veröffentlicht. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Verfügbarkeitsdatum: 6. Oktober 2025