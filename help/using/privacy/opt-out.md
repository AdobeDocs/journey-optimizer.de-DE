---
solution: Journey Optimizer
product: journey optimizer
title: Opt-out verwalten
description: Erfahren Sie, wie Sie Opt-out und Datenschutz verwalten
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Opt-out verwalten {#consent}

## Über die Opt-out-Verwaltung {#about}

Eine gesetzliche Voraussetzung ist, Empfängern die Möglichkeit zu geben, sich vom Erhalt von Nachrichten einer Marke abzumelden. Weitere Informationen zu den geltenden Rechtsvorschriften finden Sie im Abschnitt [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

**Warum ist es wichtig?**

* Die Nichteinhaltung dieser Vorschriften führt zu rechtlichen Risiken für Ihre Marke.
* Auf diese Weise können Sie vermeiden, unerwünschte Nachrichten an Ihre Empfänger zu senden, wodurch diese Ihre Nachrichten als Spam markieren und Ihrer Reputation schaden könnten.

## Opt-out-Verwaltung in Journey Optimizer {#opt-out-ajo}

Beim Versand von Nachrichten aus Journeys oder Kampagnen müssen Sie stets sicherstellen, dass Kunden sich von künftigen Nachrichten abmelden können. Nach der Abmeldung werden die Profile automatisch aus der Audience künftiger Marketing-Nachrichten entfernt.

while **[!DNL Journey Optimizer]** bietet Möglichkeiten zum Verwalten des Opt-outs in E-Mails und SMS-Nachrichten. Push-Benachrichtigungen erfordern keine Aktion auf Ihrer Seite, da sich Empfänger selbst über ihre Geräte abmelden können. Beispielsweise können sie beim Herunterladen oder bei Verwendung Ihrer App auswählen, ob sie die Benachrichtigungen stoppen möchten. Ebenso können sie die Benachrichtigungseinstellungen über das mobile Betriebssystem ändern.

In den folgenden Abschnitten erfahren Sie, wie Sie Opt-out in E-Mail- und SMS-Nachrichten von Journey Optimizer verwalten:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Lead" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>Opt-out-Verwaltung für E-Mails</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Gelegentlich" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>SMS-Abmeldeverwaltung</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>In [!DNL Journey Optimizer], wird die Zustimmung von Experience Platform verarbeitet. [Einverständnisschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}. Standardmäßig ist der Wert für das Einverständnisfeld leer und wird als Einverständnis für den Empfang Ihrer Nachrichten behandelt. Sie können diesen Standardwert beim Onboarding auf einen der möglichen Werte ändern [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}.