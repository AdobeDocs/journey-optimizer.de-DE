---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen zu Integrationen
description: Häufig gestellte Fragen zu Journey Optimizer-Integrationen für externe Daten und Inhalte in Nachrichten.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: Integration, häufig gestellte Fragen, externe Daten, Personalisierung
hide: true
source-git-commit: 3733c9ab401f85b22e1d6e07dbf4db535ff8a96d
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 1%

---

# Häufig gestellte Fragen zu Integrationen {#vendor-integration-faq}

>[!BEGINSHADEBOX]

Inhaltsverzeichnis:

* [Arbeiten mit Integrationen](external-sources.md)
* [Erste Schritte mit der Vendors-Integration](vendor-integration-gs.md)
* [Verfügbare Anbieter](vendor-integration.md)
* **[FAQs](vendor-integration-faq.md)**

>[!ENDSHADEBOX]

Im Folgenden finden Sie häufig gestellte Fragen zu **Integrationen** in Adobe Journey Optimizer.

## Erste Schritte

+++ Was tun Integrationen in Journey Optimizer?

Dadurch werden externe Datenquellen mit Journey Optimizer verbunden, sodass Sie Inhalte und Daten aus Drittanbietersystemen in Ihre Kampagnen und Journey übertragen und Nachrichten mithilfe dieser Daten personalisieren können.

➡️ [Weitere Informationen zur Übersicht über Integrationen](external-sources.md)

+++

+++ Wer konfiguriert Integrationen und wer verwendet sie in Inhalten?

Administratoren erstellen und aktivieren die technische Konfiguration (**[!UICONTROL Konfigurationen]** > **[!UICONTROL Integrationen]** > **[!UICONTROL Verwalten]** > **[!UICONTROL Integration erstellen]**). Marketer verwenden **[!UICONTROL Personalisierung hinzufügen]** in Text- oder HTML-Komponenten, öffnen **[!UICONTROL Integrationen]** wählen eine aktive Integration aus und ordnen Attribute zu.

➡️ [Erfahren Sie mehr über Administrator- und Marketing-Workflows](external-sources.md)

+++

+++ Wo kann ich als Administrator Integrationen in der Benutzeroberfläche erstellen oder verwalten?

Gehen Sie zum Abschnitt **[!UICONTROL Konfigurationen]** im linken Menü, öffnen Sie **[!UICONTROL Verwalten]** auf der Karte **[!UICONTROL Integrationen]** und wählen Sie dann **[!UICONTROL Integration erstellen]**.

➡️ [Weitere Informationen zum Erstellen einer Integration](external-sources.md#configure)

+++

+++ Was sind häufige Anwendungsfälle für Integrationen?

Beispiele sind Prämienpunkte aus Treuesystemen, Produktpreisinformationen, Empfehlungen von Empfehlungs-Engines und Logistik-Updates wie der Versandstatus.

➡️ [Erfahren Sie mehr über Beispieldaten aus Drittanbietersystemen](external-sources.md)

➡️ [Erfahren Sie mehr über Beispiele für die Anbieterintegration](vendor-integration.md)

+++

## Konfiguration

+++ Wie konfiguriere ich eine Integration auf hoher Ebene als Administrator?

Geben Sie einen Namen und eine Beschreibung, eine API-Endpunkt-URL (optional mit Pfadvariablen), Pfadvorlagenwerte, **[!UICONTROL GET]** oder **[!UICONTROL POST]**, optionale Kopfzeilen und Abfrageparameter, eine Authentifizierungsmethode, Richtlinieneinstellungen (wie Zeitüberschreitung und optionaler Cache oder erneuter Versuch), eine JSON-Beispielantwort für Zuordnungsfelder an und führen Sie dann **[!UICONTROL Testverbindung senden]** und **[!UICONTROL Aktivieren]** aus, sofern gültig.

➡️ [Weitere Informationen zur Integrationskonfiguration](external-sources.md#configure)

+++

+++ Welche Authentifizierungstypen werden unterstützt?

Diese Authentifizierungstypen sind verfügbar: **[!UICONTROL Keine Authentifizierung]**, **[!UICONTROL API-Schlüssel]**, **[!UICONTROL Einfache]** und **[!UICONTROL OAuth 2.0]** (mit Payload-Konfiguration für OAuth, falls zutreffend).

➡️ [Erfahren Sie mehr über Authentifizierungstypen](external-sources.md#configure)

+++

+++ Wofür wird der Schritt Antwort-Payload verwendet?

Fügen Sie eine JSON-Beispielantwort ein, damit das System Datentypen erkennen kann und Sie auswählen können, welche Felder für die Personalisierung in Nachrichten bereitgestellt werden. Sie können einschränken, welche Felder Marketing-Experten beim Authoring zur Verfügung stehen.

➡️ [Erfahren Sie mehr über die Zuordnung von Antwort-Payloads](external-sources.md#configure)

+++

+++ Wie fügen Marketer einer Nachricht eine Integration hinzu?

Verwenden Sie in Kampagnen- oder Journey **[!UICONTROL Inhalten „Personalisierung hinzufügen]** für eine Text- oder HTML-Komponente, gehen Sie zu **[!UICONTROL Integrationen]**, wählen Sie eine Integration aus und speichern Sie. Mit dem Pillenmodus im Personalisierungseditor können Sie Werte Variablen in der Konfiguration zuordnen (z. B. Kopfzeilen- oder Abfrageparameter oder Pfadvariablen in der URL).

➡️ [Weitere Informationen zur Personalisierung mit Integrationen](external-sources.md#personalization)

+++

## Funktionen und Anwendungsfälle

+++ Kann ich Integrationen in Journey und Kampagnen verwenden?

Ja. Die Funktion ist sowohl für Journey- als auch für Kampagnen für **ausgehende** Kanäle (z. B. E-Mail, SMS und Push-Benachrichtigungen) innerhalb der aktuellen Produktbeschränkungen verfügbar.

➡️ [Erfahren Sie mehr über Journey und Kampagnen](external-sources.md#limitations)

+++

+++ Kann ich Integrationen in wiederverwendbaren Fragmenten verwenden?

Die Integrationsfunktion wird **Fragmenten** unterstützt. Verwenden Sie Integrationen in Campaign und Journey-Nachrichteninhalt dort, wo das Produkt sie unterstützt.

➡️ [Weitere Informationen zu Fragmenten und Beta-Beschränkungen](external-sources.md#limitations)

+++

## Einschränkungen

+++ Welche Kanäle unterstützen Integrationen?

**Outbound**-Kanäle werden unterstützt (z. B. E-Mail, SMS und Push-Benachrichtigungen).

➡️ [Weitere Informationen zu unterstützten Kanälen](external-sources.md#limitations)

+++

+++ Welche API-Antwortformate werden unterstützt?

Bei API-Aufrufantworten wird **JSON** für die Feldzuordnung unterstützt. Rohe binäre Bildausgaben und Formate, die keine JSON sind, sind für diesen Workflow nicht verfügbar.

➡️ [Erfahren Sie mehr über JSON und Antwortformate](external-sources.md#limitations)

+++

+++ Mit welchen API-Mustern kann ich eine Verbindung herstellen?

**Abrufen** APIs, die auf bestimmte Inhalte abzielen, werden unterstützt. **Auflisten** APIs (Muster für umfassende Listen oder Paginierung) werden für dieses Integrationsmodell nicht unterstützt.

➡️ [Erfahren Sie mehr über Abrufen bzw. Auflisten von APIs](external-sources.md#limitations)

+++

## Berechtigungen und zugehörige Funktionen

+++ Welche Berechtigungen benötige ich, um Integrationen zu konfigurieren?

Configuration ist ein Administrator-Workflow unter **[!UICONTROL Konfigurationen]** > **[!UICONTROL Integrationen]**. Die genauen Berechtigungsnamen hängen von den Admin Console- und Journey Optimizer-Produktprofilen Ihres Unternehmens ab. Bestätigen Sie den Vorgang mit Ihrem Administrator oder Adobe-Support-Mitarbeiter.

➡️ [Erfahren Sie mehr darüber, wo Integrationen konfiguriert werden](external-sources.md#configure)

+++

+++ Ersetzen Integrationen Adobe Journey Optimizer-Connectoren durch Experience Platform-Quellen?

Nein. **Integrationen** dienen zur Personalisierung von Feldern im Nachrichteninhalt, die Sie über APIs verarbeiten. **Quellen** und andere Datenaufnahmefunktionen dienen verschiedenen Zwecken (z. B. Batch-Datenaufnahme und Profilanreicherung). Verwenden Sie jede Funktion für den vorgesehenen Umfang.

➡️ [Erfahren Sie mehr darüber, wozu Integrationen dienen](external-sources.md)

➡️ [Weitere Informationen zu Experience Platform-Quellen](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=de){target="_blank"}

+++

## Fehlerbehebung

+++ Warum schlägt die Testverbindung fehl oder bleibt sie ungültig?

Überprüfen Sie die Endpunkt-URL, die HTTP-Methode, die Pfadvorlagen, die Kopfzeilen und Abfrageparameter, die Authentifizierung und die maximale Wartezeit der Richtlinie. Verwenden Sie **[!UICONTROL Testverbindung senden]** nach der Anpassung. Stellen Sie bei Payload-Problemen sicher, dass das Beispiel eine gültige JSON widerspiegelt und dass die ausgewählten Felder mit dem übereinstimmen, was die API zurückgibt.

➡️ [Erfahren Sie mehr über das Testen der Verbindung und die Validierung der Payload](external-sources.md#configure)

+++

+++ Warum wird meine Integration von Marketing-Experten nicht in der Auswahl angezeigt?

Integrationen müssen nach **erfolgreichen** aktiviert werden. Wenn Marketing-Experten (Integrationen) öffnen **[!UICONTROL werden nur aktive Integrationen]**. Wenn die Integration noch immer Entwurf oder inaktiv ist, führen Sie zuerst die Aktivierung durch.

➡️ [Weitere Informationen zum Testen der Verbindung und Aktivierung](external-sources.md#configure)

+++

## Drittanbieter

+++ Welche Anbieterbeispiele sind verfügbar und wer sichert die API?

Sie können eine Integration mit jeder Plattform eines Drittanbieters durchführen, die einen kompatiblen API-Endpunkt bereitstellt. **Veranschaulichende** Anbietermuster und Konfigurationsbeispiele können Ihnen bei der Modellierung kompatibler APIs helfen. Die Verantwortung für die Sicherung von Endpunkten liegt bei der Drittanbieterplattform und Ihrem Team.

➡️ [Erfahren Sie mehr über Verfahren zur Anbieterintegration](vendor-integration.md)

+++
