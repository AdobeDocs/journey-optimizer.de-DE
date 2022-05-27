---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 53a625c0e62fbfae703b40bb1d47105c168730ea
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 35%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Version Mai 2022 {#may-2022-release}

### Neue Funktionen

<!--table>
<thead>
<tr>
<th><strong>Message Frequency Rules</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now set cross-channel business rules that will automatically exclude over-solicited profiles from messages and actions.</p>
<img src="assets/frequency-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/frequency-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>E-Mail-BCC</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verfügbarkeitsdatum: <strong>31. Mai</strong></p>
<p>Sie können jetzt die Funktion E-Mail-BCC (Blind Carbon Copy) verwenden, um von Adobe Journey Optimizer gesendete E-Mails zu speichern. Aktivieren Sie diese Option in Ihren E-Mail-Vorgaben, damit jede gesendete E-Mail blind in Ihre BCC-Adresse kopiert wird.</p>
<img src="assets/bcc-rn.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../configuration/email-settings.md#bcc-email">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Decision Management - AI Ranking auto-optimization model</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use trained model systems in Decision Management. This new capability ranks offers to display for a given profile.</p>
<img src="assets/optimization.gif"/>
<p>For more information, refer to the <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer-Auditprotokolle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Aktionen überwachen, die von Benutzern auf Adobe Journey Optimizer-Ressourcen ausgeführt werden.</p>
<img src="assets/audit-rn.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../reports/audit-logs.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Personalisierung**

* **Neue Hilfsfunktion für ausgeblendete Zeichen** - die `mask` Mit der Hilfsfunktion können Sie einen Teil einer Zeichenfolge durch &quot;X&quot;-Zeichen ersetzen. [Weitere Informationen](../personalization/functions/string.md#mask)

**Landingpages**

* **Landingpages ohne Formular** - Sie können jetzt eine Landingpage erstellen und veröffentlichen, die kein Formular enthält und keine Aktion von Besuchern erfordert.
* **Landingpage-Vorlagen** - Jetzt können Sie eine Landingpage als Vorlage speichern und sie bei der Erstellung anderer Landingpages wiederverwenden. [Weitere Informationen](../landing-pages/lp-templates.md)
* **Zurück zur primären Seite** - Sie können nun von einer beliebigen Unterseite innerhalb derselben Landingpage aus einen Link zur primären Seite hinzufügen.
* **Benutzerdefinierte JavaScript-Unterstützung** - Sie können jetzt benutzerdefinierten JavaScript-Code zu Ihren Landingpage-Inhalten hinzufügen, um erweiterte Formatierungen durchzuführen oder Ihren Landingpages benutzerspezifische Verhaltensweisen hinzuzufügen.	[Weitere Informationen](../landing-pages/lp-custom-js.md)

<!--**Decision management**

* **HTML and JSON files support** - You can now drag and drop external HTML and JSON files from the AEM repository into the offer representation content.-->

**Journeys**

* **Segment lesen** - Die Journey zum Lesen von Segmenten mit einer Aufnahme wechseln 30 Tage nach der Journey-Ausführung in den Status Abgeschlossen . Bei geplanten Read-Segmenten ist es 30 Tage nach der Ausführung des letzten Vorkommens. [Weitere Informationen](../building-journeys/read-segment.md)
* **Ausdruckseditor** - die [limit](../building-journeys/functions/functionlimit.md) wurde hinzugefügt, damit Sie die Anzahl der Elemente einer Liste begrenzen können. Die [sort](../building-journeys/functions/functionsort.md) -Funktion können Sie nun ein Listenobjekt sortieren. Die Unterstützung von listObject wurde auch der [distinct](../building-journeys/functions/functiondistinct.md) und [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) Funktionen.
