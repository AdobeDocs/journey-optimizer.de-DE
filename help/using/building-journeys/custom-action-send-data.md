---
solution: Journey Optimizer
product: journey optimizer
title: Senden von Daten an AEP
description: Erfahren Sie, wie Sie Daten an AEP senden.
feature: Journeys, Use Cases
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: Journey, Anwendungsfall
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 711
ht-degree: 30%

---

# Anwendungsfall: Erstellen einer benutzerdefinierten Aktion zum Senden von Daten an [!DNL Adobe Experience Platform]{#send-data-to-aep}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie mit der Aktivität Optimieren mit einer Profilbegrenzungsbedingung Ihr E-Mail-Volumen schrittweise erhöhen können, um Ihre IP-Adresse aufzuwärmen und Ihre Reputation als Absender zu schützen.

>[!ENDSHADEBOX]

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, sollten Sie Ihre Reputation als Absender aufbauen. Andernfalls können Sendungen blockiert oder in die Spam-Ordner der Empfänger verschoben werden. Eine Anleitung finden Sie im [Handbuch mit den Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de){target="_blank"}.

Um die Reputation Ihrer IP-Adresse zu verbessern, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Mehr dazu erfahren Sie unter [Zustellbarkeit in Journey Optimizer optimieren](../reports/deliverability.md).

In diesem Anwendungsbeispiel wird eine Journey erstellt, um die Versandaktivität Ihrer E-Mails zu steigern. Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen Sie eine Journey. [Weitere Informationen](journey-gs.md).

1. Fügen Sie **[!UICONTROL Journey]** Aktivität „Optimieren“ hinzu. [Weitere Informationen](optimize.md).

1. Legen Sie in den Einstellungen für die Aktivität **[!UICONTROL Bedingung]** die maximale Empfängeranzahl für Ihren Versand fest:

   1. Wählen Sie in **[!UICONTROL Aktivitätseinstellungen]** Optimieren) die Methode **[!UICONTROL Bedingungen]** und setzen Sie das Feld **[!UICONTROL Typ]** auf **[!UICONTROL Profilbegrenzung]**. [Weitere Informationen](conditions.md#profile_cap).

   1. Legen Sie das Feld **[!UICONTROL Limit]** auf die maximale Anzahl an Empfängern für diesen Versand fest.

   ![Profilbegrenzungsbedingung zur Steuerung des Ausführungsvolumens benutzerdefinierter Aktionen](assets/profile-cap-condition.png)

   Sie können dieses Limit schrittweise auf die Gesamtzahl Ihrer Abonnenten erhöhen.

1. Fügen Sie im nominalen Pfad nach der Aktivität **[!UICONTROL Bedingung]** die Aktionsaktivität **[!UICONTROL E-Mail]** hinzu.

   ![Journey mit benutzerdefinierter Aktion zum Senden von Daten an ein externes System](assets/ramp-up-deliveries-message.png)

   Wenn die Journey ausgeführt wird, wird die Nachricht bis zu der von Ihnen angegebenen Höchstzahl an Profilen an die eingehenden Profile gesendet. Wenn dieses Limit erreicht ist, nehmen die eingehenden Profile den alternativen Pfad.

1. Vervollständigen Sie die Journey mit den Aktivitäten Ihrer Wahl.

Nach dem Aufwärmen Ihrer IP können Sie diese Bedingung entfernen.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Diese Seite führt Sie durch einen Anwendungsfall zum Journey-basierten IP-Warming, der das E-Mail-Versandvolumen mithilfe einer Profilbegrenzungsbedingung schrittweise erhöht, um die Reputation des Absenders zu schützen.

**intents:**

* Erstellen einer IP-Warming-Journey zur schrittweisen Erhöhung des E-Mail-Versandvolumens
* Konfigurieren einer Profilbegrenzungsbedingung, um die Anzahl der Empfänger pro Versand zu begrenzen
* Hinzufügen der Aktionsaktivität E-Mail zum nominalen Journey-Pfad
* Bedingung für die Profilbegrenzung entfernen, sobald die IP-Erwärmung abgeschlossen ist

**Glossar:**

* **IP-Warming**: Der Prozess der schrittweisen Erhöhung des E-Mail-Versandvolumens von einer neuen IP-Adresse, um die Reputation des Absenders *produktspezifisch) herzustellen*
* **Profilbegrenzung**: Ein Bedingungstyp in Journey Optimizer, der die maximale Anzahl von Profilen begrenzt, die einen bestimmten Journey-Pfad annehmen können *(produktspezifisch)*
* **Nominaler Pfad**: Der primäre Zweig einer Journey, dem Profile folgen, wenn Bedingungen erfüllt sind *(produktspezifisch)*

**Leitplanken:**

* Für die Aktivität Bedingung muss eine Bedingung für die Profilbegrenzung festgelegt werden, um das Versandvolumen während des IP-Warmens zu steuern.
* Profile, die das obere Limit überschreiten, werden an den alternativen Pfad weitergeleitet.
* Die Journey muss nach Abschluss des IP-Warmings neu erstellt oder geändert werden, um die Kappenbedingung zu entfernen.

**Terminologie:**

* Kanonischer Name: IP Warming — Akronym: n/a — Varianten: IP Warm-up, Sender Reputation Warm-up
* Synonyme: „Profile cap“ = „Empfänger-Limit-Bedingung“
* Verwechseln Sie nicht: „IP-Warming“ ≠ „E-Mail-Authentifizierung“ (SPF/DKIM/DMARC-Einrichtung ist separat)

**FAQ:**

* **F: Warum muss ich meine IP aufwärmen?** — Neue IP-Adressen haben keinen Versandverlauf, sodass Mailbox-Anbieter Nachrichten blockieren oder Spam-Ordner senden können, bis die Reputation hergestellt ist.
* **F: Was passiert mit Profilen, die die Profilbegrenzung überschreiten?** — Sie folgen dem alternativen Pfad, der in der Aktivität Bedingung definiert ist.
* **F: Wie kann ich die Obergrenze im Laufe der Zeit erhöhen?** — Bearbeiten Sie das Feld Limit in den Einstellungen der Aktivität Bedingung und erhöhen Sie es schrittweise auf die Gesamtzahl der Abonnenten.
* **F: Wann kann ich die Bedingung für die Profilbegrenzung entfernen?** — Sobald Ihre IP über ausreichend Versandverlauf und Zustellbarkeitsmetriken verfügt, können Sie die Bedingung von der Journey entfernen.

+++
