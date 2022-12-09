---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit der Zustellbarkeit
description: Zustellbarkeitsrichtlinien
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Erste Schritte mit der Zustellbarkeit {#manage-deliverability}

Die Zustellbarkeit misst, wie erfolgreich Ihre Sendungen an die Empfängerpostfächer gesendet werden.

>[!NOTE]
>
>Für Kunden, die den Gesundheitsschild lizenzieren, verwendet Adobe Transport Layer Security (TLS) 1.2, um den Datenaustausch zwischen den Systemen (Empfängern) der Benutzer und Journey Optimizer (Absender) zu sichern. Wenn der E-Mail-Empfangs-Server TLS 1.2 nicht unterstützt, treten bei Kunden Probleme mit der Zustellbarkeit auf, einschließlich des E-Mail-Bounce zurück zum ursprünglichen Absender.

**Email Deliverability** bezieht sich auf die Merkmale, die bestimmen, ob eine Nachricht innerhalb kurzer Zeit über eine persönliche E-Mail-Adresse ihr Ziel erreichen kann und die die erwartete Qualität in Bezug auf Inhalt und Format aufweisen. Diese Merkmale fallen in vier Hauptkategorien: Datenqualität, Nachricht und Inhalt, Versandinfrastruktur und Reputation. Gemeinsam bilden sie die Grundlage eines erfolgreichen E-Mail-Zustellprogramms.

Die **Zustellrate** ist die Anzahl der Nachrichten, die die Postfächer der Empfänger erreichen, in Bezug auf die Zahl der zugestellten Nachrichten. Dabei spielen insbesondere folgende Faktoren eine Rolle:

* Eingeschränkte Spam-Beschwerden
* Niedrige Hardbounce-Rate
* Qualität der Zielkontakte
* Nachrichteninhalt
* Absender-Reputation

So optimieren Sie die Zustellbarkeit Ihrer [!DNL Journey Optimizer] Erlebnisse verwenden, empfehlen wir die in diesem Abschnitt aufgeführten Best Practices. Zustellbarkeitsprobleme stehen im Allgemeinen im Zusammenhang mit dem Schutz vor Spam, der von Internetdienstanbietern (ISPs) und Mail-Server-Administratoren implementiert wird.

Einen tieferen Einblick in die Zustellbarkeit erhalten Sie im Abschnitt [Best Practices für die Zustellbarkeit von Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html){target=&quot;_blank&quot;}.

## Verringern der Beschwerderate {#reduce-complaint-rate}

ISPs bieten in der Regel eine Möglichkeit, eine erhaltene Nachricht als Spam zu melden. Dies ermöglicht die Identifizierung unzuverlässiger Quellen. Wenn Sie Opt-out-Anfragen schnell berücksichtigen und damit nachweisen, dass Sie ein zuverlässiger Absender sind, können Sie die Beschwerderate reduzieren. [Erfahren Sie mehr über die Opt-out-Verwaltung](../privacy/opt-out.md#opt-out-management).

Generell sollten Sie Empfängern, die sich abmelden möchten, nicht die Möglichkeit geben, sich einzuschränken, indem Sie sie dazu verpflichten, Felder wie z. B. ihre E-Mail-Adresse oder ihren Namen auszufüllen. Die Abmelde-Landingpage sollte nur über eine Validierungsschaltfläche verfügen.

Wenn Sie eine zusätzliche Bestätigung anfordern, sollten Sie besonders vorsichtig sein: Ein Benutzer kann zwei E-Mail-Adressen in dasselbe Feld umleiten (z. B.: firstname.lastname@club.com und firstname.lastname@internet-club.com). Wenn sich das Profil nur an die erste Adresse erinnern kann und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, verweigert das Formular dies, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Unterdrückungslisten nutzen {#suppression-lists}

[!DNL Journey Optimizer] verwaltet eine Unterdrückungsliste, in der Spam-Beschwerden, Hardbounces und Softbounces erfasst werden, die konsistent auftreten.

Zum Schutz Ihrer Zustellbarkeit werden die Empfänger, deren Adressen auf der Unterdrückungsliste stehen, standardmäßig von allen zukünftigen Sendungen ausgeschlossen, da der Versand an diese Kontakte Ihrer Reputation schaden könnte.

[Erfahren Sie mehr über die Unterdrückungsliste](suppression-list.md).

## Verwenden von Monitoring-Tools {#monitoring-tools}

Verwenden Sie die Funktionen von [!DNL Journey Optimizer] um Ihre Zustellbarkeit zu überwachen.

Die **[!UICONTROL Executions]** in der Nachrichtenliste können Sie die Leistung Ihrer Sendungen anhand einer Reihe von Echtzeitindikatoren überprüfen. Diese Registerkarte zeigt unter anderem Folgendes an:
* Die Anzahl der erfolgreich ausgeführten, gesendeten und zugestellten Nachrichten.
* Die Anzahl der geöffneten Nachrichten und die Anzahl der angeklickten Nachrichten/Links.

## Nachrichteninhalt anpassen {#adapt-message-content}

In geringerem Umfang kann der Inhalt bestimmter Nachrichten als Spam erkannt werden.

Um Ihre Zustellrate zu verbessern und sicherzustellen, dass Ihre E-Mails Ihre Empfänger erreichen, befolgen Sie bei der Erstellung Ihres Nachrichteninhalts die unten stehenden Grundsätze:

* **Name und Adresse des Absenders**: Die Adresse muss den Absender explizit identifizieren. Die Domain muss im Besitz des Absenders sein und für ihn registriert sein. Die Domain-Registrierung darf nicht privatisiert werden.

* **Abmelde-Link und -Landingpage**: Der Abmelde-Link ist unbedingt erforderlich. Sie muss sichtbar und gültig sein und das Formular muss funktionieren.

[Erfahren Sie mehr über die Erstellung von E-Mail-Inhalten](../email/get-started-email-design.md).

## Reputation als Absender etablieren

Wenn Sie kürzlich zu einem anderen E-Mail-Dienstleister, einer IP-Adresse, einer E-Mail-Domain oder einer Subdomäne gewechselt haben, müssen Sie Ihre Reputation als Absender nachweisen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden.

Um Ihre IP-Adresse aufzuwärmen, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Siehe dies [Anwendungsfall](../building-journeys/ramp-up-deliveries-uc.md).
