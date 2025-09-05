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
source-git-commit: 13623d28ba7b852f7267b5f800f2c9a3afda4a62
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 34%

---

# Abrufen und Abonnieren von Systemwarnhinweisen {#alerts}

Verwenden Sie beim Erstellen Ihrer Journey und Kampagnen die Schaltfläche **Warnhinweise**, um Fehler zu überprüfen und zu beheben, bevor Sie sie ausführen oder veröffentlichen:

* Auf dieser Seite erfahren Sie, wie Sie Fehler bei Ihren Journey [ beheben ](../building-journeys/troubleshooting.md).
* Weitere Informationen zum Überprüfen von Kampagnen finden Sie auf [dieser Seite](../campaigns/review-activate-campaign.md).

Über das dedizierte Menü **[!UICONTROL Warnhinweise]** können Sie auch [!DNL Adobe Journey Optimizer] Systemwarnhinweise abonnieren, wie auf dieser Seite beschrieben.

## Zugriff auf Warnhinweise {#access-alerts}

Wenn ein Fehler auftritt, können Sie Systemwarnungen im Journey Optimizer-Benachrichtigungszentrum (In-App-Warnungen) erhalten und/oder eine E-Mail erhalten. Gehen Sie wie folgt vor, um auf diese Warnhinweise zuzugreifen.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

>[!NOTE]
>
>Weitere Informationen zu Warnhinweisen in Adobe Experience Platform finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=de){target="_blank"}.

Klicken Sie im linken Menü unter **[!UICONTROL Administration]** auf **[!UICONTROL Warnhinweise]**. Für Journey Optimizer sind mehrere vorkonfigurierte Warnhinweise verfügbar.

Sie werden wie folgt aufgelistet und jede Warnmeldung wird nachfolgend beschrieben.

* Spezifische Warnhinweise für Journey:

   * Warnhinweis für Fehler bei benutzerdefinierter Aktion für [&#128279;](#alert-custom-actions)Journey
   * Warnhinweis [Zielgruppen-Trigger lesen ](#alert-read-audiences) nicht erfolgreich)

* Warnhinweise speziell für die Kanalkonfiguration:

   * Warnhinweis für fehlenden DNS-Eintrag der AJO[Domäne ](#alert-dns-record-missing)
  <!--* the [AJO channel configuration failure](#alert-channel-config-failure) alert
   * the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## Abonnieren von Warnhinweisen {#subscribe-alerts}

1. Sie können jeden Warnhinweis einzeln über die Benutzeroberfläche abonnieren, indem Sie die Option **[!UICONTROL Abonnieren]** auswählen.

   ![](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >Das Abonnement gilt nur für eine bestimmte Sandbox. Sie müssen Warnhinweise für jede Sandbox einzeln abonnieren.

1. Verwenden Sie dieselbe Methode zum **[!UICONTROL Abmelden]**.

1. Sie können Warnhinweise auch über [E/A-Ereignisbenachrichtigungen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=de){target="_blank"} abonnieren. Warnregeln sind in verschiedene Abonnementpakete unterteilt. Ereignisabonnements, die den spezifischen Journey Optimizer-Warnhinweisen entsprechen, werden [unten](#journey-alerts) beschrieben.

1. Wenn ein unerwartetes Verhalten auftritt und/oder eine Reihe von Bedingungen in Ihren Vorgängen erfüllt werden (z. B. ein potenzielles Problem, wenn das System einen Schwellenwert überschreitet), werden Warnbenachrichtigungen an alle Benutzenden in Ihrer Organisation gesendet, die sich für sie angemeldet haben.

Je nach den Voreinstellungen des Abonnenten werden Warnhinweise per E-Mail und/oder direkt im Journey Optimizer-Benachrichtigungszentrum in der oberen rechten Ecke der Benutzeroberfläche gesendet (In-App-Benachrichtigungen). Wählen Sie in der [!DNL Adobe Experience Cloud] (Voreinstellungen) aus **[!UICONTROL wie Sie diese Warnhinweise]** möchten. [Weitere Informationen](../start/user-interface.md#in-product-alerts)

>[!NOTE]
>
>Standardmäßig sind nur In-App-Warnungen aktiviert.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=de#enable-email-alerts){target="_blank"}.-->

Wenn ein Warnhinweis aufgelöst wurde, erhalten die Abonnentinnen und Abonnenten die Benachrichtigung „Aufgelöst“.

## Verwalten von Warnhinweisen {#manage-alerts}

Um Warnhinweise zu verwalten, wählen Sie ein Element aus und verwenden Sie die Schaltfläche **[!UICONTROL Weitere Aktionen]**.

![](assets/alert-more-actions.png){width=80%}

Standardmäßig sind alle Warnhinweise aktiviert. Um einen Warnhinweis zu deaktivieren, wählen Sie die Option **[!UICONTROL Warnhinweis deaktivieren]** aus dem Menü **[!UICONTROL Mehr Aktionen]** aus. Alle Abonnentinnen und Abonnenten dieses Warnhinweises erhalten nicht mehr die zugehörigen Benachrichtigungen.

Wählen Sie **[!UICONTROL Warnhinweis-Abonnenten verwalten]** aus, um die Liste der Benutzer anzuzeigen, die den Warnhinweis abonniert haben. Verwenden Sie das leere Feld, um weitere Abonnenten hinzuzufügen.

![](assets/alert-subscribers.png){width=80%}

Die möglichen Warnhinweisstatus sind unten aufgeführt:

* **[!UICONTROL Aktiviert]** - Der Warnhinweis ist aktiviert und überwacht derzeit den Zustand des Triggers.
* **[!UICONTROL Deaktiviert]** - Der Warnhinweis ist deaktiviert und überwacht derzeit den Zustand des Triggers nicht. Sie erhalten keine Benachrichtigungen für diesen Warnhinweis.
* **[!UICONTROL Ausgelöst]** - Die Bedingung für den Trigger des Warnhinweises wird derzeit erfüllt.

## Journey-Warnhinweise {#journey-alerts}

>[!CAUTION]
>
>Adobe Journey Optimizer-spezifische Warnhinweise gelten nur für **Live**-Journeys. Warnhinweise werden für Journeys im Testmodus nicht ausgelöst.

### Benutzerdefinierte Journey-Aktion fehlgeschlagen {#alert-custom-actions}

Dieser Warnhinweis warnt Sie, wenn eine benutzerdefinierte Aktion fehlschlägt. Wir gehen davon aus, dass die Aktion fehlgeschlagen ist, wenn in den letzten 5 Minuten bei einer bestimmten benutzerdefinierten Aktion mehr als 1 % Fehler aufgetreten sind. Dies wird alle 30 Sekunden ausgewertet.

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

## Konfigurationswarnungen {#configuration-alerts}

### AJO Domain-DNS-Eintrag fehlt {#alert-dns-record-missing}

Dieser Warnhinweis benachrichtigt Sie, wenn kritische DNS-Einträge (NS oder CNAME), die für eine ordnungsgemäße Zustellbarkeitskonfiguration erforderlich sind, fehlen oder falsch konfiguriert sind. Ohne diese Datensätze kann die E-Mail-Zustellbarkeit beeinträchtigt sein.

>[!NOTE]
>
>* NS-Einträge sind für die vollständige Subdomain-Delegierung an Adobe unerlässlich. [Weitere Informationen](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* CNAME-Einträge unterstützen die Einrichtung von CNAME-Subdomains. [Weitere Informationen](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

Der **AJO Domain-DNS-Eintrag fehlt** Warnhinweis wird ausgelöst, wenn das System erkennt, dass die erforderlichen NS- oder CNAME-Einträge fehlen oder nicht den Konfigurationsstandards entsprechen.

1. Klicken Sie auf den Warnhinweis, um zur betroffenen [Subdomain](../configuration/delegate-subdomain.md) in der [!DNL Journey Optimizer] weitergeleitet zu werden.

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. Stellen Sie die DNS-Konfiguration wieder her, indem Sie die Einträge korrekt festlegen und [die Subdomain übermitteln](../configuration/delegate-subdomain.md#submit-subdomain)Delegierung erneut durchführen.

   >[!NOTE]
   >
   >Stellen Sie sicher, dass alle Einträge ordnungsgemäß in Ihrer Domain-Hosting-Lösung erstellt wurden, bevor Sie fortfahren.

1. Wenn Sie sich nicht sicher sind, welche Werte richtig sind, können Sie eine neue Subdomain in [!DNL Journey Optimizer] mit demselben Namen wie die betroffene Subdomain erstellen. [Erfahren Sie, wie Sie eine neue Subdomain einrichten](../configuration/delegate-subdomain.md#set-up-subdomain)

Wenn das Problem durch die Änderungen nicht behoben wird, wird derselbe Warnhinweis am nächsten Tag erneut ausgelöst.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?-->

### AJO-Kanalkonfigurationsfehler {#alert-channel-config-failure}

>[!IMPORTANT]
>
>Dieser Warnhinweis gilt nur für **E-Mail**-Kanalkonfigurationen, die den Delegierungstyp [benutzerdefinierte Subdomain](../configuration/delegate-custom-subdomain.md) verwenden. <!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

Dieser Warnhinweis wird ausgelöst, wenn die Systemüberwachung Konfigurationsprobleme des E-Mail-Kanals erkennt. Zu diesen Problemen können falsch konfigurierte Kanaleinstellungen, eine ungültige DNS-Konfiguration, ein Problem mit der Unterdrückungsliste, IP-Inkonsistenzen oder andere Fehler gehören, die sich auf den E-Mail-Versand auswirken können.

Wenn Sie einen solchen Warnhinweis erhalten, sind die Auflösungsschritte unten aufgeführt:

1. Klicken Sie auf den Warnhinweis, um zur betroffenen [E-Mail-Kanalkonfiguration](../email/get-started-email-config.md) in der [!DNL Journey Optimizer] weitergeleitet zu werden.

   Anleitungen zum Bearbeiten von Kanalkonfigurationen finden Sie [diesem Abschnitt](../configuration/channel-surfaces.md#edit-channel-surface).

1. Überprüfen Sie die Konfigurationsdetails und Fehlermeldungen. Häufige Fehlerursachen sind:

   * SPF-Validierung fehlgeschlagen
   * DKIM-Validierung fehlgeschlagen
   * MX-Eintragsvalidierung fehlgeschlagen
   * Ungültige DNS-Einträge

   >[!NOTE]
   >
   >Die möglichen Ursachen für Konfigurationsfehler sind in [ Abschnitt ](../configuration/channel-surfaces.md).

1. Beheben Sie das Problem:

   * Aktualisieren Sie die Kanalkonfiguration nach Bedarf.
   * Möglicherweise müssen Sie bestimmte DNS-Probleme beheben, die in dem Warnhinweis erwähnt werden.

   >[!NOTE]
   >
   >Da eine einzelne Domain mit mehreren Kanalkonfigurationen verknüpft werden kann, können verwandte Probleme in mehreren Konfigurationen automatisch behoben werden, wenn DNS-Probleme für eine Kanalkonfiguration behoben werden.

Wenn die Änderung das Problem nicht behebt, wird derselbe Warnhinweis am nächsten Tag erneut ausgelöst.

Beachten Sie beim Beheben von E-Mail-Konfigurationsproblemen die unten aufgeführten Best Practices:

* Sofortiges Handeln - Beheben Sie Konfigurationsfehler, sobald sie erkannt werden, um Unterbrechungen beim E-Mail-Versand zu vermeiden.
* Alle Konfigurationen überprüfen - Wenn der Warnhinweis mehrere betroffene E-Mail-Konfigurationen anzeigt, überprüfen und beheben Sie jede davon.

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->





