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
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: ht
source-wordcount: '272'
ht-degree: 100%

---

# Verwalten von Opt-out {#consent}

## Über die Opt-out-Verwaltung {#about}

Die Möglichkeit für Empfänger, den Empfang von Mitteilungen einer Marke zu kündigen, ist eine gesetzliche Anforderung. Weitere Informationen zu den geltenden Rechtsvorschriften finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=de#regulations){target=&quot;_blank&quot;}.

**Warum ist das wichtig?**

* Die Nichtbeachtung dieser Vorschriften birgt rechtliche Risiken für Ihre Marke.
* Auf diese Weise vermeiden Sie das Verschicken unerwünschter Nachrichten an Empfänger, die Ihre Nachrichten als Spam kennzeichnen und Ihrem Ruf schaden könnten.

## Opt-out-Verwaltung in Journey Optimizer {#opt-out-ajo}

Beim Versand von Nachrichten von Journeys oder Kampagnen müssen Sie stets sicherstellen, dass sich Kunden von der künftigen Kommunikation abmelden können. Nach der Kündigung des Abos werden die Profile automatisch aus der Audience künftiger Marketing-Nachrichten entfernt.

**[!DNL Journey Optimizer]** bietet Möglichkeiten zum Verwalten des Opt-outs in E-Mails und SMS-Nachrichten. Push-Benachrichtigungen erfordern hingegen keine Maßnahme Ihrerseits, da sich Empfänger selbst über ihre Geräte abmelden können. Beispielsweise können sie den Versand von Benachrichtigungen beim Herunterladen oder bei der Nutzung Ihrer Mobile App deaktivieren. Ebenso können sie die Benachrichtigungseinstellungen über das mobile Betriebssystem ändern.

In den folgenden Abschnitten erfahren Sie, wie Sie Opt-out-Verfahren in E-Mails und SMS-Nachrichten von Journey Optimizer verwalten:

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
&lt;a href=" ../sms/sms-opt-out.md"><strong>Opt-out-Verwaltung für SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>In [!DNL Journey Optimizer] wird das Einverständnis durch das [Einverständnisschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=de){target=&quot;_blank&quot;} von Experience Platform gehandhabt. Standardmäßig ist der Wert für das Einverständnisfeld leer und gilt als Einverständnis für den Empfang Ihrer Nachrichten. Sie können diesen Standardwert beim Onboarding in einen der möglichen [hier](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=de#choice-values){target=&quot;_blank&quot;} aufgelisteten Werte ändern.