---
solution: Journey Optimizer
product: journey optimizer
title: Abrufen und Abonnieren von Systemwarnhinweisen
description: Informationen zum Zugreifen auf und Abonnieren von Systemwarnhinweisen
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 34649ab411823f1aa09d390d23484697e80763c5
workflow-type: ht
source-wordcount: '1313'
ht-degree: 100%

---

# Abrufen und Abonnieren von Systemwarnhinweisen {#alerts}

Verwenden Sie beim Erstellen Ihrer Journeys und Kampagnen die Schaltfläche **Warnhinweise**, um Fehler vor der Ausführung oder Veröffentlichung zu überprüfen und zu beheben.



Über das dedizierte Menü **[!UICONTROL Warnhinweise]** können Sie auch [!DNL Adobe Journey Optimizer]-Systemwarnhinweise abonnieren, wie auf dieser Seite beschrieben.

## Zugriff auf Warnhinweise {#access-alerts}

Wenn ein Fehler auftritt, können Sie Systemwarnungen im Journey Optimizer-Benachrichtigungszentrum (In-App-Warnungen) und/oder als E-Mail erhalten. Gehen Sie wie folgt vor, um auf diese Warnhinweise zuzugreifen:

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

>[!NOTE]
>
>Weitere Informationen zu Warnhinweisen in Adobe Experience Platform finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=de){target="_blank"}.

Klicken Sie im linken Menü unter **[!UICONTROL Administration]** auf **[!UICONTROL Warnhinweise]**. Für Journey Optimizer sind mehrere vorkonfigurierte Warnhinweise verfügbar.

Sie werden hier aufgelistet und jeder Warnhinweis wird nachfolgend beschrieben.

* Spezifische Warnhinweise für Journeys:

   * Warnhinweis beim [Fehlschlagen einer benutzerdefinierten Journey-Aktion](#alert-custom-actions)
   * Warnhinweis [Auslösen von „Zielgruppe lesen“ fehlgeschlagen](#alert-read-audiences)
<!--DOCAC-13465   * the [Profile Discard Rate Exceeded](#alert-discard-rate) alert
   * the [Custom Action Error Rate Exceeded](#alert-custom-action-error-rate) alert
   * the [Profile Error Rate Exceeded](#alert-profile-error-rate) alert-->

* Warnhinweise speziell für die Kanalkonfiguration:

   * Warnhinweis ](#alert-dns-record-missing)DNS-Eintrag für AJO-Domain fehlt[
   * Warnhinweis ](#alert-channel-config-failure)Fehler bei der AJO-Kanalkonfiguration[
     <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## Abonnieren von Warnhinweisen {#subscribe-alerts}

Wenn ein unerwartetes Verhalten auftritt und/oder bestimmte Bedingungen in Ihren Vorgängen erfüllt sind (z. B. ein potenzielles Problem, wenn das System einen Schwellenwert überschreitet), werden Warnhinweise an alle Benutzenden in Ihrer Organisation gesendet, die diese abonniert haben.

Sie können die Warnhinweise einzeln über die Benutzeroberfläche oder global über das Menü **[!UICONTROL Warnhinweise]** (siehe [Globales Abonnement](#global-subscription)) abonnieren<!--DOCAC-13465, or unitary for a specific journey (see [Unitary subscription](#unitary-subscription))-->.

Je nach den Benutzereinstellungen werden Warnhinweise per E-Mail gesendet und/oder erscheinen direkt im Journey Optimizer-Benachrichtigungszentrum oben rechts in der Benutzeroberfläche. Wählen Sie in den **[!UICONTROL Voreinstellungen]** von [!DNL Adobe Experience Cloud] aus, wie Sie diese Warnhinweise erhalten möchten. [Weitere Informationen](../start/user-interface.md#in-product-alerts)

Wenn ein Warnhinweis aufgelöst wurde, erhalten die Abonnentinnen und Abonnenten die Benachrichtigung „Aufgelöst“.


### Globales Abonnement {#global-subscription}

Gehen Sie wie folgt vor, um einen Warnhinweis für alle Journeys und Kampagnen zu abonnieren oder abzubestellen:

1. Navigieren Sie im linken Menü zum Dashboard **[!UICONTROL Warnhinweise]** und wählen Sie die Option **[!UICONTROL Abonnieren]** für den Warnhinweis, den Sie abonnieren möchten.

   ![Abonnieren eines Warnhinweises](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >Das Abonnement gilt nur für eine bestimmte Sandbox. Sie müssen also Warnhinweise für jede Sandbox einzeln abonnieren.

1. Auf dieselbe Weise können Sie sich auch wieder **[!UICONTROL abmelden]**.

Sie können Warnhinweise auch über [E/A-Ereignisbenachrichtigungen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=de){target="_blank"} abonnieren. Warnhinweisregeln sind in verschiedene Abonnementpakete unterteilt. Abonnements für Ereignisse, die den jeweiligen Journey Optimizer-Warnhinweisen entsprechen, werden [nachfolgend](#journey-alerts) beschrieben.

<!--DOCAC-13465
### Unitary subscription {#unitary-subscription}

To subscribe/unsubscribe to an alert for a specific journey, follow these steps:

1. Browse to the journey inventory and select the **[!UICONTROL Subscribe to alerts]** option for a specific journey.

      ![Subscribing to an alert for a specific journey](assets/subscribe-journey-alert.png){width=80%}

1. Choose the alert(s). The following alerts are available: [Profile Discard Rate Exceeded](#alert-discard-rate), [Custom Action Error Rate Exceeded](#alert-custom-action-error-rate), and [Profile Error Rate Exceeded](#alert-profile-error-rate).
   
1. To unsubscribe to an alert, unselect it from the same screen.

1. Click **[!UICONTROL Save]** to confirm.
-->

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=de#enable-email-alerts){target="_blank"}.-->




## Journey-Warnhinweise {#journey-alerts}

>[!CAUTION]
>
>Adobe Journey Optimizer-spezifische Warnhinweise gelten nur für **Live**-Journeys. Warnhinweise werden für Journeys im Testmodus nicht ausgelöst.


### Benutzerdefinierte Journey-Aktion fehlgeschlagen {#alert-custom-actions}

Dieser Warnhinweis warnt Sie, wenn eine benutzerdefinierte Aktion fehlschlägt. Wir gehen davon aus, dass die Aktion fehlgeschlagen ist, wenn in den letzten 5 Minuten bei einer bestimmten benutzerdefinierten Aktion mehr als 1 % Fehler aufgetreten sind. Dies wird alle 30 Sekunden ausgewertet.

Klicken Sie auf den Namen des Warnhinweises, um dessen Details und Konfiguration zu überprüfen.

![](assets/alerts-custom-action.png)

Warnhinweise zu benutzerdefinierten Aktionen werden aufgelöst, wenn in den letzten 5 Minuten:

* bei dieser benutzerdefinierten Aktion keine Fehler (oder nur Fehler unter dem Schwellenwert von 1 %) aufgetreten sind.

* oder kein Profil diese benutzerdefinierte Aktion erreicht hat.

Der Name des E/A-Ereignissabonnements, der dem Warnhinweis für benutzerdefinierte Aktionen entspricht, lautet: **Benutzerdefinierte Journey-Aktion fehlgeschlagen**.

Fehlerbehebung von Warnhinweisen bei **benutzerdefinierten Aktionen**:

* Prüfen Sie Ihre benutzerdefinierte Aktion mithilfe des Testmodus in einer anderen Journey:

  ![](assets/alert-troubleshooting-2.png)

* Prüfen Sie Ihren Journey-Bericht, um die Fehlerursachen für die Aktion zu sehen.

  ![](assets/alert-troubleshooting-3.png)

* Prüfen Sie Ihre Journey-stepEvents, um weitere Informationen zu „failureReason“ zu erhalten.

* Prüfen Sie die Konfiguration Ihrer benutzerdefinierten Aktion und überprüfen Sie, ob die Authentifizierung weiterhin korrekt ist. Führen Sie beispielsweise eine manuelle Prüfung mit Postman durch.

### Zielgruppe-lesen-Auslöser konnte nicht gelesen werden {#alert-read-audiences}

Dieser Warnhinweis erscheint, wenn eine Aktivität **Zielgruppe lesen** 10 Minuten nach der festgelegten Ausführungszeit kein Profil bearbeitet hat. Dieser Fehler kann durch technische Probleme oder eine leere Zielgruppe verursacht werden. Wenn dieser Fehler auf technische Probleme zurückzuführen ist, sind je nach Problemtyp dennoch weitere Versuche möglich (wenn z. B. die Erstellung eines Exportauftrags fehlgeschlagen ist, erfolgt alle 10 Minuten, aber höchstens eine Stunde lang, ein erneuter Versuch).

![](assets/alerts1.png)

Warnhinweise zu **Zielgruppe lesen** gelten nur für wiederkehrende Journey. Aktivitäten vom Typ **Zielgruppe lesen** in Live-Journeys, für deren Ausführung **Einmal** oder **So bald wie möglich** festgelegt wurde, werden ignoriert.

Warnhinweise zu **Zielgruppe lesen** werden aufgelöst, wenn ein Profil den Knoten **Zielgruppe lesen** erreicht.

Der Name des E/A-Ereignisabonnements, das dem **Alert Read Audience Trigger Unsuccessful** entspricht, ist **Journey read audience Delays, Failures and Errors**.

Überprüfen Sie zur Fehlerbehebung von Warnhinweisen bei **Zielgruppe lesen** die Anzahl Ihrer Zielgruppen auf der Experience Platform-Oberfläche.

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

<!--DOCAC-13465

### Profile Discard Rate Exceeded {#alert-discard-rate}

This alert warns you if the ratio of profile discards to entered profiles over the last 5 minutes exceeded threshold. The defaut threshold is set to 20% but you can [define a custom theshold](#custom-threshold).

Click the name of the alert to check the alert details and configuration.


### Custom Action Error Rate Exceeded {#alert-custom-action-error-rate}

This alert warns you if the ratio of custom action errors to successful HTTP calls over the last 5 minutes exceeded threshold. The defaut threshold is set to 20% but you can [define a custom theshold](#custom-threshold).

### Profile Error Rate Exceeded {#alert-profile-error-rate}

This alert warns you if the ratio of custom action errors to successful HTTP calls over the last 5 minutes exceeded threshold. The defaut threshold is set to 20% but you can [define a custom theshold](#custom-threshold).

Click the name of the alert to check the alert details and configuration.
-->

## Konfigurationswarnhinweise {#configuration-alerts}

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
<!--DOCAC-13465
For Journey alerts, use the **[!UICONTROL More actions]** button to edit them. You can then define a [custom theshold](#custom-threshold) for these alerts.-->

![](assets/alert-more-actions.png){width=60%}

<!--DOCAC-13465
#### Define a custom threshold {#custom-threshold}

You can set thresholds for the [Journey alerts](#journey-alerts). The threshold alerts above default to 20%. 

To change the threshold:

1. Browse to the **Alerts** screen
1. Click the **[!UICONTROL More actions]** button of the alert to update
1. Enter the new threshold and confirm. The new threshold applies to **all** journeys


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>The threshold levels are global across all journeys and cannot be individually modified per journey.
-->

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

## Weitere Ressourcen {#additional-resources-alerts}


* Weitere Informationen zum Beheben von Fehlern in Journeys finden Sie auf [dieser Seite](../building-journeys/troubleshooting.md).
* Weitere Informationen zum Überprüfen von Kampagnen finden Sie auf [dieser Seite](../campaigns/review-activate-campaign.md).