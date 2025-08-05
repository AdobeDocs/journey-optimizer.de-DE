---
solution: Journey Optimizer
product: journey optimizer
title: Vorab veröffentlichte Versionshinweise für Journey Optimizer
description: Vorab-Versionshinweise zu Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 46%

---

# Hinweise zu Vorabversionen {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Die unten stehenden Hinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.


## Vorab-Versionshinweise August 2025 {#25-7-rn}

**Die unten stehenden Hinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Screenshots und die aktualisierte Dokumentation werden am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Adobe Experience Platform-Hinweise zur Vorabversion](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: Mittwoch, 19. August 2025


### Neue Funktionen {#Aug-25-8-features}

Im Folgenden werden die neuen Funktionen dieser Version beschrieben.

<table>
<thead>
<tr>
<th><strong>Pausieren und Fortsetzen von Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Ihre Journeys jetzt pausieren und fortsetzen. Diese Funktion gibt Journey-Anwendenden mehr Kontrolle und Flexibilität, da Live-Journeys vorübergehend ausgesetzt werden können, ohne das Kundenerlebnis zu stören. Während der Pause werden keine Nachrichten gesendet und die Profile verbleiben in einem ausgesetzten Zustand, bis die Journey fortgesetzt wird.</p>
<p>Sie können nur eine Journey pausieren und fortsetzen oder Vorgänge zur Massenpause und -fortsetzung von einer Gruppe von Journeys durchführen.</p>
<p>Darüber hinaus können Sie globale Filter auf pausierte Journeys anwenden, um Profile auf der Grundlage ihrer Attribute auszuschließen.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Zuvor für eine begrenzte Anzahl von Kunden verfügbar (eingeschränkte Verfügbarkeit), ist diese Funktion jetzt für alle Umgebungen verfügbar (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-pause.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Kalenderansicht</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine Kalenderansicht ist nun in den Journey- und Kampagnenlisten verfügbar. Damit können Sie alle Journey- und Kampagnenaktivierungen in den jeweiligen Listen visualisieren.</p>
<p>Diese Funktion war bisher nur in begrenzter Verfügbarkeit verfügbar und steht nun allen Umgebungen zur Verfügung. Mit dieser allgemeinen Verfügbarkeit umfasst die Funktion:</p>
<ul>
<li>Design-Verbesserungen für die Navigation in Datumsangaben</li>
<li>Die Möglichkeit, Kampagnenentwürfe anzuzeigen, wenn Sie ein Start- und Enddatum festgelegt haben</li>
<li>Eine neue Einstellung zum Ausblenden und Anzeigen von Kalenderelementen, die über einen langen Zeitraum ausgeführt werden</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-ui.md#journeys-calendar">detaillierten Dokumentation</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Dunkler Modus im E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Journey Optimizer E-Mail-Designer bietet jetzt die Möglichkeit, in die Ansicht „Dunkler Modus“ zu wechseln, in der Sie zusätzlich bestimmte benutzerdefinierte Einstellungen definieren können, die nur für Empfänger angezeigt werden, die ihre E-Mails im Dunkeln Modus lesen.</p>
<p>Beachten Sie Folgendes:</p>
<ul>
<li>Das endgültige Rendering im Dunkelmodus kann variieren und hängt vom E-Mail-Client des Empfängers ab.</li>
<li>Nicht alle E-Mail-Clients unterstützen einen benutzerdefinierten dunklen Modus. Darüber hinaus wenden einige E-Mail-Clients ausschließlich ihren eigenen standardmäßigen dunklen Modus auf alle empfangenen E-Mails an. In beiden Fällen können die im E-Mail-Designer definierten benutzerdefinierten Einstellungen nicht gerendert werden.</li>
</ul>
<P>Diese Funktion befindet sich derzeit in der Beta-Version und steht nur der Beta-Kundschaft zur Verfügung. Wenden Sie sich an den Adobe-Support, um am Beta-Programm teilzunehmen.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../email/dark-mode.md">ausführlichen Dokumentation</a>. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Optimierung in Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Journey Optimizer können Sie jetzt personalisierte und optimierte Inhalte für die Zielgruppen Ihrer Kampagnen bereitstellen, indem Sie Inhaltsexperimente durchführen, regelbasiertes Targeting erstellen und erweiterte Kombinationen aus beiden verwenden können, um die Effektivität Ihrer Kampagnen zu maximieren.</p>
<p>Mit der Optimierung können Sie:</p>
<ul>
<li>Testen Sie mehrere Inhaltsvarianten, um die effektivste Botschaft zu identifizieren.</li>
<li>Stellen Sie personalisierte Inhalte auf der Basis von Benutzerattributen und kontextuellen Daten bereit.</li>
<li>Kombinieren Sie Targeting und Experimentieren für erweiterte Kampagnenstrategien.</li>
<li>Filtern Sie Benutzer heraus, die nicht den Variantenkriterien entsprechen.</li>
<li>Fallback-Mechanismen zur Aufrechterhaltung der Benutzerinteraktion sicherstellen.</li>
</ul>
<P>Sobald die Kampagne live ist, werden Profile anhand der definierten Kriterien bewertet und auf der Grundlage übereinstimmender Kriterien mit dem entsprechenden Erlebnis oder Inhalt aus der Kampagne bereitgestellt.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#Aug-25-8-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.