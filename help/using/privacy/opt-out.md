---
solution: Journey Optimizer
product: journey optimizer
title: Verwalten von Opt-out
description: Erfahren Sie, wie Sie Opt-out- und Datenschutzeinstellungen verwalten können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 45%

---

# Verwalten von Opt-out {#consent}

Es ist gesetzlich vorgeschrieben, den Empfängern die Möglichkeit zu geben, sich vom Erhalt von Nachrichten einer Marke abzumelden, und sicherzustellen, dass diese Entscheidung respektiert wird. Weitere Informationen zu den geltenden Rechtsvorschriften finden Sie in der Dokumentation zu [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=de#regulations){target="_blank"}.

**Warum ist das wichtig?**

* Die Nichtbeachtung dieser Vorschriften birgt rechtliche Risiken für Ihre Marke.
* Auf diese Weise vermeiden Sie das Verschicken unerwünschter Nachrichten an Empfänger, die Ihre Nachrichten als Spam kennzeichnen und Ihrem Ruf schaden könnten.

## Abmeldungen in Journey und Kampagnen verwalten {#opt-out-ajo}

Beim Versand von Nachrichten von Journeys oder Kampagnen müssen Sie stets sicherstellen, dass sich Kunden von der künftigen Kommunikation abmelden können. Nach der Kündigung des Abos werden die Profile automatisch aus der Audience künftiger Marketing-Nachrichten entfernt.

**[!DNL Journey Optimizer]** bietet Möglichkeiten zum Verwalten des Opt-outs in E-Mails und SMS-Nachrichten. Push-Benachrichtigungen erfordern hingegen keine Maßnahme Ihrerseits, da sich Empfänger selbst über ihre Geräte abmelden können. Beispielsweise können sie den Versand von Benachrichtigungen beim Herunterladen oder bei der Nutzung Ihrer Mobile App deaktivieren. Ebenso können sie die Benachrichtigungseinstellungen über das mobile Betriebssystem ändern.

In den folgenden Abschnitten erfahren Sie, wie Sie Opt-out-Verfahren in E-Mails und SMS-Nachrichten von Journey Optimizer verwalten:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Lead" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>Opt-out-Verwaltung für E-Mails</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Gelegentlich" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>Opt-out-Verwaltung bei SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>In [!DNL Journey Optimizer] wird das Einverständnis durch das [Einverständnisschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=de){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=de#choice-values){target="_blank"} von Experience Platform verarbeitet.

## Implementieren der Personalisierungszustimmung {#opt-out-personalization}

Ihre Kunden können sich auch von der Anzeige personalisierter Inhalte abmelden. Nachdem sich ein Profil von der Personalisierung abgemeldet hat, müssen Sie sicherstellen, dass seine Daten nicht für die Personalisierung verwendet werden, und Sie müssen alle personalisierten Inhalte durch eine Fallback-Variante ersetzen.

### In der Entscheidungsverwaltung

Bei der Nutzung von Angeboten werden Personalisierungseinstellungen nicht automatisch in implementiert [Entscheidungsbereiche](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) verwendet von [Entscheidungsfindung](../offers/api-reference/offer-delivery-api/decisioning-api.md) API-Anfrage oder [Edge-Entscheidung](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md) API-Anfrage. In diesem Fall müssen Sie die Zustimmung zur Personalisierung manuell erzwingen. Gehen Sie dazu wie folgt vor.

>[!NOTE]
>
>In verwendete Entscheidungsbereiche [!DNL Journey Optimizer] erstellte Kanäle erfüllen diese Anforderung von der Journey oder Kampagne, zu der sie gehören.



1. Erstellen Sie eine [Adobe Experience Platform-Segment](../segment/about-segments.md) Verwendung eines Profilattributs wie: *&quot;Zustimmung zur Personalisierung = true&quot;* , um Benutzer anzusprechen, die der Personalisierung zugestimmt haben.

1. Beim Erstellen einer [Entscheidung](../offers/offer-activities/create-offer-activities.md), fügen Sie einen Entscheidungsbereich hinzu und definieren Sie eine auf diesem Segment basierende Eignungsbegrenzung für jede Bewertungskriterien-Kollektion, die personalisierte Angebote enthält.

1. Erstellen Sie eine [Fallback-Angebot](../offers/offer-library/creating-fallback-offers.md) , der keine personalisierten Inhalte enthält.

1. [Zuweisen](../offers/offer-activities/create-offer-activities.md#add-fallback) das nicht personalisierte Fallback-Angebot für die Entscheidung.

1. [Entscheidung überprüfen und speichern.](../offers/offer-activities/create-offer-activities.md#review)

Wenn ein Benutzer über Folgendes verfügt:

* Einverständnis für die Personalisierung erhält, bestimmt der Entscheidungsbereich das beste Angebot für dieses Profil.

* nicht zur Personalisierung zugelassen wurde, kommt das entsprechende Profil für keines der Angebote in den Bewertungskriterien infrage und erhält daher das nicht personalisierte Fallback-Angebot.

>[!NOTE]
>
>Einverständnis für die Verwendung von Profildaten in [Datenmodellierung](../offers/ranking/ai-models.md) wird noch nicht unterstützt in [!DNL Journey Optimizer].

