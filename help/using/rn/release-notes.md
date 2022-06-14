---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0ca491315e214e3c12bec11a93da1a2b98b493b6
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 90%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Version Mai 2022 {#may-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Häufigkeitsregeln für Nachrichten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt kanalübergreifende Geschäftsregeln festlegen, mit denen Profile, die zu oft angesprochen wurden, automatisch aus Nachrichten und Aktionen ausgeschlossen werden.</p>
<img src="assets/frequency-rn.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../configuration/frequency-rules.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Email BCC</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Availability date: <strong>May, 31</strong></p>
<p>You can now use the Email BCC (blind carbon copy) capability to store emails sent by Adobe Journey Optimizer. Enable this option in your email presets so that every email sent is blind-copied to your BCC address.</p>
<img src="assets/bcc-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/email-settings.md#bcc-email">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Entscheidungs-Management – Modell zur automatischen Optimierung des KI-Rankings</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt trainierte Modellsysteme im Entscheidungs-Management verwenden. Mit dieser neuen Funktion wird eine Rangliste der Angebote erstellt, die für ein bestimmtes Profil angezeigt werden.</p>
<img src="assets/optimization.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

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

* **Neue Hilfsfunktion für ausgeblendete Zeichen**: Mit der Hilfsfunktion `mask` können Sie einen Teil einer Zeichenfolge durch „X“-Zeichen ersetzen. [Weitere Informationen](../personalization/functions/string.md#mask)

**Landingpages**

* **Landingpages ohne Formular**: Sie können jetzt eine Landingpage erstellen und veröffentlichen, die kein Formular enthält und keine Aktion von Besuchern erfordert.
* **Landingpage-Vorlagen**: Sie können jetzt eine Landingpage als Vorlage speichern und sie bei der Erstellung anderer Landingpages wiederverwenden. [Weitere Informationen](../landing-pages/lp-templates.md)
* **Zurück zur primären Seite**: Sie können nun von einer beliebigen Unterseite innerhalb derselben Landingpage aus einen Link zur primären Seite hinzufügen.
* **Unterstützung von benutzerdefiniertem JavaScript**: Sie können jetzt benutzerdefinierten JavaScript-Code zu Ihren Landingpage-Inhalten hinzufügen, um erweiterte Formatierungen durchzuführen oder Ihren Landingpages benutzerspezifische Verhaltensweisen hinzuzufügen.	[Weitere Informationen](../landing-pages/lp-custom-js.md)

**Journeys**

* **Segment lesen**: Einmalige Journeys mit dem Schritt „Segment lesen“ gehen jetzt 30 Tage nach der Ausführung der Journey in den Status „Beendet“ über. Folgt der Schritt „Segment lesen“ einem Zeitplan, wird er 30 Tage nach der letzten Ausführung beendet. [Weitere Informationen](../building-journeys/read-segment.md)
* **Ausdruckseditor**: Die Funktion [Limit](../building-journeys/functions/functionlimit.md) wurde hinzugefügt, um die Anzahl der Elemente einer Liste zu begrenzen. Mit der Funktion [Sortierung](../building-journeys/functions/functionsort.md) können Sie jetzt ein Listenobjekt sortieren. Die Unterstützung von listObject wurde auch den Funktionen [distinct](../building-journeys/functions/functiondistinct.md) und [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) hinzugefügt.

**Administration**

* **Aktualisierung des Lizenzverwendungs-Dashboards** - Das Dashboard zur Lizenzverwendung im [!DNL Adobe Journey Optimizer] Die Benutzeroberfläche spiegelt jetzt den genauen Wert für die **Lizenziert** Durchschnittliche Reichweite des Profils. In dieser Metrikdarstellung wird ein Rückgang angezeigt, was bedeutet, dass die Lizenzbeschränkung jetzt korrekt gemeldet wird. [Weitere Informationen](../segment/license-usage.md)
