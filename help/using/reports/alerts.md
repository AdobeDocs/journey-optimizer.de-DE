---
solution: Journey Optimizer
product: journey optimizer
title: Abrufen und Abonnieren von Systemwarnhinweisen
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer auf Systemwarnungen zugreifen, diese abonnieren und verwalten können. Überwachen Sie die Journey-Leistung, Fehler bei benutzerdefinierten Aktionen, Profilprobleme und die E-Mail-Zustellbarkeit mit proaktiven Warnbenachrichtigungen.
feature: Journeys, Alerts, Monitoring
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 6976f2b1b8b95f7dc9bffe65b7a7ddcc5dab5474
workflow-type: tm+mt
source-wordcount: '2693'
ht-degree: 58%

---

# Abrufen und Abonnieren von Systemwarnhinweisen {#alerts}

## Übersicht

Warnhinweise sind automatische Benachrichtigungen, mit denen Sie Probleme in Adobe Journey Optimizer überwachen und beheben können. Sie bieten Echtzeit-Erkennung potenzieller Probleme in Ihren Journey-, Kampagnen- und Kanalkonfigurationen, sodass Sie Korrekturmaßnahmen ergreifen können, bevor Kundenerlebnisse beeinträchtigt werden.

Adobe Journey Optimizer bietet zwei Arten von Warnhinweisen:

* **Validierungswarnungen auf der Arbeitsfläche**: Verwenden Sie beim Erstellen von Journey und Kampagnen die Schaltfläche **Warnhinweise** auf der Arbeitsfläche, um Konfigurationsfehler vor der Veröffentlichung zu identifizieren und zu beheben. Erfahren Sie, wie [Fehler bei Ihren Journey](../building-journeys/troubleshooting.md) beheben und Ihre Kampagnen überprüfen können: [Aktionskampagnen](../campaigns/review-activate-campaign.md) | [API-ausgelöste Kampagnen](../campaigns/review-activate-api-triggered-campaign.md) | [Orchestrierte Kampagnen](../orchestrated/start-monitor-campaigns.md).

* **Systemüberwachungswarnungen** (auf dieser Seite beschrieben): Empfangen Sie proaktive Benachrichtigungen, wenn Betriebsschwellenwerte überschritten werden oder Probleme in Live-Journey- und Kanalkonfigurationen erkannt werden. Systemwarnungen überwachen Metriken wie Fehlerquoten, Profilverwerfen und E-Mail-Zustellbarkeitsprobleme.

**Die wichtigsten Vorteile von Systemwarnungen:**

* Proaktive Problemerkennung vor der Beeinträchtigung des Kunden
* Automatisierte Überwachung von Journey-Leistung und -Zustand
* Frühwarnung bei Problemen mit der E-Mail-Zustellbarkeit
* Weniger Zeit für die Identifizierung und Lösung betrieblicher Probleme

Systemwarnhinweise sind im Menü **[!UICONTROL Warnhinweise]** unter **[!UICONTROL Administration]** verfügbar. Adobe Experience Platform bietet mehrere vordefinierte Warnhinweisregeln, die Sie aktivieren können, einschließlich [!DNL Adobe Journey Optimizer] Warnhinweise für Journey- und Kanalkonfigurationen.

## Voraussetzungen

Vor der Arbeit mit Warnhinweisen:

* **Berechtigungen**: Sie benötigen spezifische Berechtigungen zum Anzeigen und Verwalten von Warnhinweisen. Siehe [Erforderliche Berechtigungen in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html#permissions){target="_blank"}.

* **Sandbox-**: Warnhinweis-Abonnements sind Sandbox-spezifisch. Wenn Sie Warnhinweise abonnieren, gelten diese nur für die aktuelle Sandbox. Wenn eine Sandbox zurückgesetzt wird, werden auch alle Warnhinweis-Abonnements zurückgesetzt.

* **Benachrichtigungseinstellungen**: Konfigurieren Sie, wie Sie Warnhinweise (E-Mail und/oder In-App) in Ihren [Adobe Experience Cloud-Einstellungen erhalten](../start/user-interface.md#in-product-uc).

>[!NOTE]
>
>Journey Optimizer-spezifische Warnhinweise gelten nur für **Live**-Journey. Warnhinweise werden für Journey im Testmodus nicht ausgelöst. Weitere Informationen zum Warnhinweis-Framework finden Sie in der Dokumentation zu [Adobe Experience Platform-Warnhinweisen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=de){target="_blank"}.

## Verfügbare Warnhinweise in Journey Optimizer {#available-alerts}

Journey Optimizer bietet vorkonfigurierte Warnhinweisregeln, die bestimmte Aspekte Ihrer Journey- und Kanalkonfigurationen überwachen. Sie müssen diese Warnhinweise nicht erstellen. Sie sind standardmäßig verfügbar und können über ein Abonnement aktiviert werden.

**So greifen Sie auf die Warnmeldungsliste zu:**

Navigieren Sie **[!UICONTROL linken Menü]** Administration > **[!UICONTROL Warnhinweise]**. Auf **Registerkarte** Durchsuchen“ werden alle vorkonfigurierten Warnhinweise angezeigt, die für Journey Optimizer verfügbar sind.

![](assets/updated-alerts-list.png){width=50%}

### Warnhinweiskategorien

Journey Optimizer bietet zwei Kategorien von Systemwarnungen:

>[!BEGINTABS]

>[!TAB Journey-Warnhinweise]

Überwachen der Journey-Ausführung und -Leistung:

* [Trigger „Zielgruppe lesen“ nicht ](#alert-read-audiences) - Warnt, wenn eine Aktivität „Zielgruppe lesen“ keine Profile verarbeiten kann
* [Fehlerrate für benutzerdefinierte Aktion überschritten](#alert-custom-action-error-rate) - Erkennt hohe Fehlerraten in API-Aufrufen für benutzerdefinierte Aktion (ersetzt den vorherigen Warnhinweis für Fehler bei benutzerdefinierter Journey-Aktion)
* [Profil-Verwerfungsrate überschritten](#alert-discard-rate) - Gibt an, wann Profile mit einer abnormalen Rate verworfen werden
* [Profilfehlerrate überschritten](#alert-profile-error-rate) - Flags, wenn bei Profilen während der Journey-Ausführung Fehler auftreten
* [Journey veröffentlicht](#alert-journey-published) - Benachrichtigung zur Information, wenn eine Journey veröffentlicht wird
* [Journey beendet](#alert-journey-finished) - Benachrichtigung, wenn eine Journey abgeschlossen ist
* [Benutzerdefinierte Aktionsbegrenzung ausgelöst](#alert-custom-action-capping) - Benachrichtigt, wenn die API-Aufrufbeschränkungen erreicht sind.

>[!TAB Warnhinweise zur Kanalkonfiguration]

Probleme beim Einrichten der E-Mail-Zustellbarkeit erkennen:

* [DNS-Eintrag der AJO-Domain fehlt](#alert-dns-record-missing) - Identifiziert fehlende oder falsch konfigurierte DNS-Einträge.
* [AJO-Kanalkonfigurationsfehler](#alert-channel-config-failure) - Erkennt E-Mail-Konfigurationsprobleme (SPF-, DKIM-, MX-Einträge)
  <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

>[!ENDTABS]

>[!NOTE]
>
>Warnhinweise von anderen Adobe Experience Platform-Services (Datenaufnahme, Identitätsauflösung, Segmentierung usw.) finden Sie in der [Standarddokumentation zu Warnhinweisregeln](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/rules.html){target="_blank"}.

## Abonnieren von Warnhinweisen {#subscribe-alerts}

Warnhinweis-Abonnements bestimmen, welche Benutzer Benachrichtigungen erhalten, wenn bestimmte Bedingungen erfüllt sind (z. B. Schwellenwerte für Fehlerquoten oder erkannte Konfigurationsprobleme). Nur abonnierte Benutzer erhalten Warnhinweise für die ausgewählten Warnhinweise.

### Abonnementmethoden

Warnhinweise können auf zwei Arten abonniert werden:

* **[Globales Abonnement](#global-subscription)**: Gilt für alle Journey und Kampagnen in der aktuellen Sandbox. Verwenden Sie diese Methode, wenn Sie die gesamte Journey-Aktivität in Ihrem Unternehmen überwachen möchten.
* **[Journey-spezifisches Abonnement](#unitary-subscription)**: Gilt nur für einzelne Journey. Verwenden Sie diese Methode, wenn Sie bestimmte Journey mit hoher Priorität überwachen möchten, ohne Warnhinweise für alle Journey zu erhalten.

### Funktionsweise von Warnhinweisen

**Warnhinweis-Lebenszyklus:**

1. **Auslösen**: Der Warnhinweis wird Trigger, wenn seine spezifische Bedingung erfüllt ist (z. B. die Fehlerrate überschreitet 20 %).
2. **Benachrichtigung**: Alle abonnierten Benutzer erhalten Benachrichtigungen über ihre konfigurierten Kanäle
3. **Überwachung**: Der Warnhinweis überwacht den Zustand weiterhin in regelmäßigen Abständen
4. **Lösung**: Nach Behebung der Bedingung erhalten Abonnentinnen und Abonnenten eine Benachrichtigung mit dem Hinweis „Aufgelöst“

**Benachrichtigungsversand:**

* **Versandkanäle**: Warnhinweise werden per E-Mail und/oder In-App-Benachrichtigungen im Journey Optimizer-Benachrichtigungszentrum gesendet (Glockensymbol oben rechts). Konfigurieren Sie Ihre bevorzugten Versandkanäle in Ihren [Adobe Experience Cloud-Voreinstellungen](../start/user-interface.md#in-product-uc).

* **Warnhinweistypen**: Journey Optimizer bietet sowohl einmalige Warnhinweise (Informationsereignisse wie &quot;Journey veröffentlicht„) als auch sich wiederholende Warnhinweise (Überwachungsschwellen). Die Auswertung und Benachrichtigung bei sich wiederholenden Warnhinweisen wird fortgesetzt, bis die Bedingung behoben ist.

* **Automatische Auflösung**: Um zu verhindern, dass die Benachrichtigungsermüdung zu schwankenden Werten führt, werden Warnhinweise nach einer Stunde automatisch aufgelöst, selbst wenn die Bedingung weiterhin besteht. Dadurch werden kontinuierliche Benachrichtigungen verhindert, wenn Metriken über Schwellenwerte bewegen.

**Alternative Anmeldemethode:**

Bei erweiterten Integrationen können Sie über I/O Events abonnieren, um Warnhinweise an externe Systeme zu senden. Weitere Informationen sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=de){target="_blank"} verfügbar.


### Globales Abonnement {#global-subscription}

Globale Abonnements ermöglichen den Empfang von Warnhinweisen für alle Journey und Kampagnen in der aktuellen Sandbox.

**So abonnieren Sie einen Warnhinweis:**

1. Navigieren Sie **[!UICONTROL linken Menü]** Administration > **[!UICONTROL Warnhinweise]**.

1. Suchen Sie auf **[!UICONTROL Registerkarte]** Durchsuchen“ den Warnhinweis, den Sie überwachen möchten.

1. Klicken Sie **[!UICONTROL den gewünschten]** auf „Abonnieren“.

   ![Abonnieren eines Warnhinweises](assets/alert-subscribe.png){width=80%}

**Abo kündigen:**

Klicken Sie **[!UICONTROL Abo beenden]** neben dem Warnhinweis.

>[!IMPORTANT]
>
>Warnhinweis-Abonnements sind sandbox-spezifisch. Sie müssen Warnhinweise separat in jeder Sandbox abonnieren, in der Sie Benachrichtigungen erhalten möchten.

**Alternative Anmeldemethode:**

Sie können auch über [E/A-Ereignisbenachrichtigungen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=de){target="_blank"} abonnieren, was die Integration in externe Systeme ermöglicht. Ereignisabonnementnamen für Journey Optimizer-Warnhinweise werden in jeder [Warnhinweisbeschreibung unten) ](#journey-alerts).

### Journey-spezifisches Abonnement {#unitary-subscription}

Journey-spezifische Abonnements ermöglichen es Ihnen, einzelne Journey mit hoher Priorität zu überwachen, ohne Warnhinweise für alle Journey in Ihrem Unternehmen zu erhalten.

**So abonnieren Sie Warnhinweise für eine bestimmte Journey:**

1. Gehen Sie zum Journey-Inventar.

1. Klicken Sie auf das **⋯**-Menü (weitere Aktionen) für die Journey, die Sie überwachen möchten.

1. Wählen Sie **[!UICONTROL Warnhinweise abonnieren]** aus.

   ![Abonnieren eines Warnhinweises für eine bestimmte Journey](assets/subscribe-journey-alert.png){width=75%}

1. Wählen Sie aus den verfügbaren Optionen den/die Warnhinweis(e) aus, den/die Sie aktivieren möchten:
   * [Rate beim Verwerfen des Profils überschritten](#alert-discard-rate)
   * [Fehlerrate bei benutzerdefinierter Aktion überschritten](#alert-custom-action-error-rate)
   * [Fehlerrate bei Profil überschritten](#alert-profile-error-rate)
   * [Journey veröffentlicht](#alert-journey-published)
   * [Journey abgeschlossen](#alert-journey-finished)
   * [Begrenzung benutzerdefinierter Aktionen ausgelöst](#alert-custom-action-capping)

1. Klicken Sie **[!UICONTROL Speichern]**, um Ihre Abonnements zu bestätigen.

**Abo kündigen:**

Öffnen Sie dasselbe Dialogfeld, heben Sie die Auswahl der Warnhinweise auf und klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Der Warnhinweis [Zielgruppen-Trigger nicht erfolgreich](#alert-read-audiences) ist nur über ein globales Abonnement verfügbar, nicht pro Journey-Abonnement.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->

## Journey-Warnhinweise {#journey-alerts}


Alle in der Benutzeroberfläche verfügbaren Journey-Benachrichtigungen sind unten aufgeführt.

>[!CAUTION]
>
>Adobe Journey Optimizer-spezifische Warnhinweise gelten nur für **Live**-Journeys. Warnhinweise werden für Journeys im Testmodus nicht ausgelöst.

### Zielgruppe-lesen-Auslöser konnte nicht gelesen werden {#alert-read-audiences}

Dieser Warnhinweis erscheint, wenn eine Aktivität **Zielgruppe lesen** 10 Minuten nach der festgelegten Ausführungszeit kein Profil bearbeitet hat. Dieser Fehler kann durch technische Probleme oder eine leere Zielgruppe verursacht werden. Wenn dieser Fehler auf technische Probleme zurückzuführen ist, sind je nach Problemtyp dennoch weitere Versuche möglich (wenn z. B. die Erstellung eines Exportauftrags fehlgeschlagen ist, erfolgt alle 10 Minuten, aber höchstens eine Stunde lang, ein erneuter Versuch).

Warnhinweise zu **Zielgruppe lesen** gelten nur für wiederkehrende Journey. Aktivitäten vom Typ **Zielgruppe lesen** in Live-Journeys, für deren Ausführung **Einmal** oder **So bald wie möglich** festgelegt wurde, werden ignoriert.

Warnhinweise zu **Zielgruppe lesen** werden entweder aufgelöst, wenn ein Profil den Knoten **Zielgruppe lesen** erreicht, oder nach einer Stunde.

Der Name des I/O-Ereignis-Abonnements, das dem Warnhinweis **Auslösen von „Zielgruppe lesen“ fehlgeschlagen** entspricht, ist **Verzögerungen und Fehler bei Journeys des Typs „Zielgruppe lesen“**.

Überprüfen Sie zur Fehlerbehebung von Warnhinweisen bei **Zielgruppe lesen** die Anzahl Ihrer Zielgruppen auf der Experience Platform-Oberfläche.

### Rate beim Verwerfen des Profils überschritten {#alert-discard-rate}

Dieser Warnhinweis warnt Sie, wenn das Verhältnis zwischen verworfenen Profilen und eingetretenen Profilen in den letzten 5 Minuten den Schwellenwert überschritten hat. Der Standardschwellenwert ist auf 20 % festgelegt, Sie können jedoch [einen benutzerdefinierten Schwellenwert definieren](#custom-threshold).

Klicken Sie auf den Namen des Warnhinweises, um dessen Details und Konfiguration zu prüfen.

![](assets/profile-discard-alert.png)

Es kann mehrere Gründe dafür geben, wieso ein Profil verworfen wird. Die Methode der Fehlerbehebung hängt vom Grund ab. Einige häufige Gründe sind unten aufgeführt:

* Ein Profil wird bei Eintritt verworfen, da es bereits auf dieser unitären Journey live ist. Um dies zu beheben, stellen Sie sicher, dass das Profil genügend Zeit zum Aussteigen aus der Journey hat, bevor das nächste Ereignis für dieses Profil beginnt.
* Die Identität ist nicht für das Profil festgelegt oder der in der Journey des Typs „Zielgruppe lesen“ verwendete Namespace wird in diesem Profil nicht genutzt. Um dies zu beheben, stellen Sie sicher, dass der Namespace in der Journey mit dem von den Profilen verwendeten Identity-Namespace übereinstimmt.
* Die Ereignisdurchsatzrate wurde überschritten. Um dies zu beheben, stellen Sie sicher, dass die in das System eingehenden Ereignisse diese Grenzwerte nicht überschreiten.


### Fehlerrate bei benutzerdefinierter Aktion überschritten {#alert-custom-action-error-rate}

Dieser Warnhinweis warnt Sie, wenn das Verhältnis von Fehlern bei benutzerdefinierten Aktionen zu erfolgreichen HTTP-Aufrufen in den letzten 5 Minuten den Schwellenwert überschritten hat. Der Standardschwellenwert ist auf 20 % festgelegt, Sie können jedoch [einen benutzerdefinierten Schwellenwert definieren](#custom-threshold).

>[!NOTE]
>
>Dieser Warnhinweis ersetzt den vorherigen Warnhinweis für **Fehlschlagen einer benutzerdefinierten Journey-Aktion**.

Klicken Sie auf den Namen des Warnhinweises, um dessen Details und Konfiguration zu prüfen.

Fehler bei benutzerdefinierten Aktionen können aus verschiedenen Gründen auftreten. Es gibt folgende Möglichkeiten zur Behebung dieser Fehler:

* Prüfen Sie Ihre benutzerdefinierte Aktion mithilfe des [Testmodus](../building-journeys/testing-the-journey.md) in einer anderen Journey.
* Prüfen Sie Ihren [Journey-Bericht](../reports/journey-live-report.md), um die Fehlerursachen für die Aktion zu erfahren.
* Prüfen Sie Ihre Journey-stepEvents, um weitere Informationen zu „failureReason“ zu erhalten.
* Prüfen Sie, ob Ihre benutzerdefinierte Aktion korrekt konfiguriert ist, und stellen Sie sicher, dass die Authentifizierung weiterhin gültig ist. Führen Sie beispielsweise eine manuelle Prüfung mit Postman durch.
* Prüfen Sie, ob der Endpunkt erreichbar ist und die benutzerdefinierte Aktion ihn über die Konnektivitätsprüfung für benutzerdefinierte Aktionen erreichen kann.
* Überprüfen Sie die Anmeldeinformationen, die Internet-Verbindung usw.

### Fehlerrate bei Profil überschritten {#alert-profile-error-rate}

Dieser Warnhinweis warnt Sie, wenn das Verhältnis zwischen fehlerhaften Profilen und eingetretenen Profilen in den letzten 5 Minuten den Schwellenwert überschritten hat. Der Standardschwellenwert ist auf 20 % festgelegt, Sie können jedoch [einen benutzerdefinierten Schwellenwert definieren](#custom-threshold).

Klicken Sie auf den Namen des Warnhinweises, um dessen Details und Konfiguration zu prüfen.

Um Profilfehler zu beheben, können Sie die Daten in Schrittereignissen abfragen und so erfahren, wo und warum das Profil während der Journey fehlgeschlagen ist.

### Journey veröffentlicht {#alert-journey-published}

Dieser Warnhinweis informiert Sie, wenn eine Journey von jemandem auf der Journey-Arbeitsfläche veröffentlicht wurde.

Dies ist ein informativer Warnhinweis, mit dem Sie Journey-Lebenszyklusereignisse in Ihrem Unternehmen verfolgen können. Es gibt keine Auflösungskriterien, da es sich um eine einmalige Benachrichtigung handelt.

### Journey abgeschlossen {#alert-journey-finished}

Dieser Warnhinweis informiert Sie, wenn eine Journey abgeschlossen wurde. Die Definition von „beendet“ variiert je nach Journey-Typ. [Erfahren Sie mehr darüber, wann Journey als abgeschlossen gelten](../building-journeys/end-journey.md#journey-finished-definition).

Dies ist ein informativer Warnhinweis, mit dem Sie den Abschluss der Journey verfolgen können. Es gibt keine Auflösungskriterien, da es sich um eine einmalige Benachrichtigung handelt.

### Begrenzung benutzerdefinierter Aktionen ausgelöst {#alert-custom-action-capping}

Dieser Warnhinweis warnt Sie, wenn bei einer benutzerdefinierten Aktion eine Begrenzung ausgelöst wurde. Mit einer Begrenzung wird die Anzahl der an einen externen Endpunkt gesendeten Aufrufe begrenzt, um zu verhindern, dass der Endpunkt überlastet wird.

Klicken Sie auf den Namen des Warnhinweises, um dessen Details und Konfiguration zu prüfen.

Wenn eine Begrenzung ausgelöst wird, bedeutet dies, dass die maximale Anzahl von API-Aufrufen innerhalb des definierten Zeitraums erreicht wurde und weitere Aufrufe gedrosselt oder in die Warteschlange gestellt werden. Weitere Informationen zur Begrenzung von benutzerdefinierten Aktionen finden Sie auf [dieser Seite](../action/about-custom-action-configuration.md#custom-action-enhancements-best-practices).

Dieser Warnhinweis wird aufgelöst, wenn die Begrenzung nicht mehr aktiv ist oder wenn während des Auswertungszeitraums keine Profile die benutzerdefinierte Aktion erreichen.

Beheben von Begrenzungsproblemen:

* Überprüfen Sie die Begrenzungskonfiguration für Ihre benutzerdefinierte Aktion, um sicherzustellen, dass die Beschränkungen für Ihren Anwendungsfall geeignet sind.
* Überprüfen Sie, ob die Anzahl der API-Aufrufe höher ist als erwartet, und passen Sie Ihr Journey-Design oder Ihre Begrenzungseinstellungen an.
* Überwachen Sie den externen Endpunkt, um sicherzustellen, dass er die erwartete Last verarbeiten kann.

## Konfigurationswarnhinweise {#configuration-alerts}

In der Benutzeroberfläche verfügbare Warnhinweise zum Monitoring der Kanalkonfiguration sind unten aufgeführt.

### DNS-Eintrag für AJO-Domain fehlt {#alert-dns-record-missing}

Dieser Warnhinweis benachrichtigt Sie, wenn kritische DNS-Einträge (NS oder CNAME), die für eine ordnungsgemäße Zustellbarkeitskonfiguration erforderlich sind, fehlen oder falsch konfiguriert sind. Ohne diese Einträge kann die E-Mail-Zustellbarkeit beeinträchtigt sein.

>[!NOTE]
>
>* NS-Einträge sind für die vollständige Subdomain-Delegierung an Adobe unerlässlich. [Weitere Informationen](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* CNAME-Einträge unterstützen die Einrichtung von CNAME-Subdomains. [Weitere Informationen](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

Der Warnhinweis **DNS-Eintrag für AJO-Domain fehlt** wird ausgelöst, wenn das System erkennt, dass die erforderlichen NS- oder CNAME-Einträge fehlen oder nicht den Konfigurationsstandards entsprechen.

1. Klicken Sie auf den Warnhinweis, um zur betroffenen [Subdomain](../configuration/delegate-subdomain.md) in der [!DNL Journey Optimizer]-Benutzeroberfläche weitergeleitet zu werden.

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. Stellen Sie die DNS-Konfiguration wieder her, indem Sie die Einträge korrekt festlegen und die Delegierung der [Subdomain erneut übermitteln](../configuration/delegate-subdomain.md#submit-subdomain).

   >[!NOTE]
   >
   >Stellen Sie sicher, dass alle Einträge ordnungsgemäß in Ihrer Domain-Hosting-Lösung erstellt wurden, bevor Sie fortfahren.

1. Wenn Sie sich nicht sicher sind, welche Werte richtig sind, können Sie in [!DNL Journey Optimizer] eine neue Subdomain mit demselben Namen wie die betroffene Subdomain erstellen. [Informationen dazu, wie Sie eine neue Subdomain einrichten](../configuration/delegate-subdomain.md#set-up-subdomain)

Wenn das Problem trotz der Änderungen weiterhin besteht, wird derselbe Warnhinweis am nächsten Tag erneut ausgelöst.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?-->

### Fehler bei der AJO-Kanalkonfiguration {#alert-channel-config-failure}

>[!IMPORTANT]
>
>Dieser Warnhinweis gilt nur für **E-Mail**-Kanalkonfigurationen, die den Delegierungstyp [benutzerdefinierte Subdomain](../configuration/delegate-custom-subdomain.md) verwenden. <!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

Dieser Warnhinweis wird ausgelöst, wenn das System-Audit Konfigurationsprobleme beim E-Mail-Kanal erkennt. Zu den Problemen können falsch konfigurierte Kanaleinstellungen, eine ungültige DNS-Konfiguration, ein Problem mit der Unterdrückungsliste, IP-Inkonsistenzen oder andere Fehler gehören, die sich auf den E-Mail-Versand auswirken.

Wenn Sie einen solchen Warnhinweis erhalten, sind die Lösungsschritte unten aufgeführt:

1. Klicken Sie auf den Warnhinweis, um zur betroffenen [E-Mail-Kanalkonfiguration](../email/get-started-email-config.md) in der [!DNL Journey Optimizer]-Benutzeroberfläche weitergeleitet zu werden.

   Anleitungen zum Bearbeiten von Kanalkonfigurationen finden Sie [diesem Abschnitt](../configuration/channel-surfaces.md#edit-channel-surface).

1. Prüfen Sie die Konfigurationsdetails und Fehlermeldungen. Häufige Fehlerursachen sind:

   * SPF-Validierung fehlgeschlagen
   * DKIM-Validierung fehlgeschlagen
   * MX-Eintragsvalidierung fehlgeschlagen
   * Ungültige DNS-Einträge

   >[!NOTE]
   >
   >Die möglichen Ursachen für Konfigurationsfehler sind in [diesem Abschnitt](../configuration/channel-surfaces.md) aufgelistet.

1. Beheben Sie das Problem:

   * Aktualisieren Sie die Kanalkonfiguration nach Bedarf.
   * Möglicherweise müssen Sie bestimmte DNS-Probleme beheben, die in dem Warnhinweis erwähnt werden.

   >[!NOTE]
   >
   >Da eine einzelne Domain mit mehreren Kanalkonfigurationen verknüpft sein kann, können verwandte Probleme in verschiedenen Konfigurationen automatisch behoben werden, wenn DNS-Probleme für eine Kanalkonfiguration behoben werden.

Wenn das Problem trotz der Änderung weiterhin besteht, wird derselbe Warnhinweis am nächsten Tag erneut ausgelöst.

Beachten Sie beim Beheben von E-Mail-Konfigurationsproblemen die unten aufgeführten Best Practices:

* Handeln Sie sofort – Beheben Sie Konfigurationsfehler, sobald sie erkannt werden, um Unterbrechungen beim E-Mail-Versand zu vermeiden.
* Prüfen Sie alle Konfigurationen – Wenn der Warnhinweis mehrere betroffene E-Mail-Konfigurationen anzeigt, überprüfen und beheben Sie jede einzelne davon.

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->

## Verwalten von Warnhinweisen {#manage-alerts}

### Bearbeiten eines Warnhinweises

Sie können die Details eines Warnhinweises prüfen, indem Sie auf dessen Zeile klicken. Im linken Panel werden der Name, der Status und die Benachrichtigungskanäle angezeigt.
Verwenden Sie die Schaltfläche **[!UICONTROL Weitere Aktionen]** zum Bearbeiten von Journey-Warnhinweisen. Anschließend können Sie einen [benutzerdefinierten Schwellenwert](#custom-threshold) für diese Warnhinweise definieren.

![](assets/alert-more-actions.png){width=60%}

### Definieren eines benutzerdefinierten Schwellenwerts {#custom-threshold}

Sie können Schwellenwerte für die [Journey-Warnhinweise](#journey-alerts) festlegen. Der Schwellenwert für die obigen Warnhinweise liegt standardmäßig bei 20 %.

Ändern des Schwellenwerts:

1. Navigieren Sie zum Bildschirm **Warnhinweise**.
1. Klicken Sie auf die Schaltfläche **[!UICONTROL Weitere Aktionen]** des zu aktualisierenden Warnhinweises.
1. Geben Sie den neuen Schwellenwert ein und bestätigen Sie. Der neue Schwellenwert gilt für **alle** Journeys.


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>Die Schwellenwerte gelten für alle Journeys und können nicht einzeln pro Journey geändert werden.

### Deaktivieren eines Warnhinweises

Standardmäßig sind alle Warnhinweise aktiviert. Um einen Warnhinweis zu deaktivieren, wählen Sie die Option **[!UICONTROL Warnhinweis deaktivieren]**: Alle Abonnierenden dieses Warnhinweises erhalten die entsprechenden Benachrichtigungen dann nicht mehr.


### Status von Warnhinweisen

Die möglichen Status von Warnhinweisen sind unten aufgeführt:

* **[!UICONTROL Aktiviert]** – Der Warnhinweis ist aktiviert, und es wird derzeit auf die Auslösebedingung überwacht.
* **[!UICONTROL Deaktiviert]** – Der Warnhinweis ist deaktiviert, und es wird derzeit nicht auf die Auslösebedingung überwacht. Sie erhalten keine Benachrichtigungen für diesen Warnhinweis.
* **[!UICONTROL Ausgelöst]** – Die Auslösebedingung für den Warnhinweis ist derzeit erfüllt.


### Anzeigen und Aktualisieren von Abonnierenden {#manage-subscribers}

Wählen Sie **[!UICONTROL Warnhinweis-Abonnierende verwalten]** aus, um die Liste der Benutzenden anzuzeigen, die den Warnhinweis abonniert haben. 

![](assets/alert-subscribers.png){width=80%}

Um weitere Abonnierende hinzuzufügen, geben Sie ihre E-Mail-Adressen durch Kommata getrennt ein und wählen Sie **[!UICONTROL Aktualisieren]** aus.

Um Abonnierende zu entfernen, löschen Sie ihre E-Mail-Adressen aus den aktuellen Abonnierenden und wählen Sie **[!UICONTROL Aktualisieren]** aus.

## Verwandte Themen {#additional-resources-alerts}

**Journey- und Kampagnenverwaltung:**

* [Fehlerbehebung bei Journey](../building-journeys/troubleshooting.md) - Identifizieren und Beheben häufiger Journey-Probleme und -Fehler
* [Journey testen und veröffentlichen](../building-journeys/publishing-the-journey.md) - Validieren der Journey-Konfiguration vor der Veröffentlichung
* [Überprüfen und Aktivieren von Aktionskampagnen](../campaigns/review-activate-campaign.md) - Validierung vor der Veröffentlichung für geplante und einmalige Kampagnen
* [Überprüfen und Aktivieren von API-ausgelösten Kampagnen](../campaigns/review-activate-api-triggered-campaign.md) - Validierung für API-ausgelöste Kampagnen
* [Überwachen orchestrierter Kampagnen](../orchestrated/start-monitor-campaigns.md) - Verfolgen und Verwalten der orchestrierten Kampagnenausführung

**Warnhinweis-Framework:**

* [Übersicht über Adobe Experience Platform-Warnhinweise](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=de){target="_blank"} - Grundlagen zum Warnhinweis-Framework
* [Verwalten von Warnhinweisen in der ](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=de){target="_blank"}: Anzeigen, Abonnieren und Verwalten von Warnhinweisen
* [Warnhinweise über I/O-Ereignisse abonnieren](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=de){target="_blank"} - Erweiterte Integrationsoptionen
* [Standardwarnungsregeln](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/rules.html){target="_blank"} - Vollständige Liste der verfügbaren Platform-Warnungen
