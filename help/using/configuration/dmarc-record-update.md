---
solution: Journey Optimizer
product: journey optimizer
title: Einhalten der neuen DMARC-Anforderung
description: Erfahren Sie, warum und wann Sie einen DMARC-Eintrag in Journey Optimizer festlegen müssen
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Domain, Mail, DMARC, Eintrag
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
TQID: https://experienceleague.adobe.com/B-gnzjRpmhxELBiXRZxkBvE2yNNgozy-Hed5-k1oaIQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: ht
source-wordcount: 493
ht-degree: 100%

---

# Einhalten der neuen DMARC-Anforderung {#dmarc-record-update}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, warum und wann Sie einen DMARC-Eintrag für die Subdomains einrichten müssen, die Sie in Adobe Journey Optimizer an Adobe delegiert haben, um die Absenderanforderungen von Google und Yahoo zu erfüllen.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Weitere Informationen zur obligatorischen DMARC-Aktualisierung"
>abstract="Zur Einhaltung der Best Practices in der Branche verlangen Google und Yahoo seit dem **1. Februar 2024** einen **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails an sie verwenden.<br>Daher müssen Sie unbedingt für alle Subdomains, die Sie in Journey Optimizer an Adobe delegiert haben, einen DMARC-Eintrag einrichten."

Die Domain-basierte Nachrichtenauthentifizierung, Berichte und Konformität (DMARC) ist eine E-Mail-Authentifizierungsmethode, mit der der Inhaberinnen und Inhaber einer Domain ihre Domain vor unbefugter Verwendung schützen können. Durch eine klare Richtlinie für E-Mail-Anbieter/ISPs verhindert sie, dass auf böswillige Weise E-Mails gesendet werden, die scheinbar von Ihrer Domain stammen. Die Implementierung von DMARC verringert das Risiko, dass legitime E-Mails als Spam gekennzeichnet oder abgelehnt werden, und verbessert die Zustellbarkeit Ihrer E-Mails.

Zur Einhaltung der Best Practices in der Branche verlangen Google und Yahoo! einen **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails an sie verwenden. Diese neue Anforderung gilt seit dem **1. Februar 2024**.

>[!CAUTION]
>
>Bei Nichteinhaltung dieser neuen Anforderung von Gmail und Yahoo! werden E-Mails wahrscheinlich im Spam-Ordner landen oder blockiert.

Adobe empfiehlt daher dringend, DMARC-Einträge für alle Subdomains einzurichten, die Sie in [!DNL Journey Optimizer] an Adobe delegiert haben. Befolgen Sie die folgenden Schritte, die auf Ihren Fall zutreffen:

* Wenn Sie Ihre sendenden Subdomains [vollständig an Adobe delegiert](delegate-subdomain.md#set-up-subdomain) haben, führen Sie eine der folgenden Optionen aus:

   * Richten Sie DMARC auf der übergeordneten Domain Ihrer delegierten Subdomains **in Ihrer Hosting-Lösung** ein.
oder
   * Richten Sie DMARC in Ihren delegierten Subdomains **in der Konfigurations-Benutzeroberfläche von[!DNL Journey Optimizer]** ein – ohne zusätzliche Arbeit an Ihrer Hosting-Lösung. [Weitere Informationen](dmarc-record.md#implement-dmarc)

* Wenn Sie Ihre Versand-Subdomains mit [CNAME](delegate-subdomain.md#cname-subdomain-setup) eingerichtet haben, führen Sie eine der folgenden Optionen aus:

   * Richten Sie DMARC auf Ihren Subdomains oder auf der übergeordneten Domain Ihrer Subdomains **in Ihrer Hosting-Lösung** ein.
oder
   * Richten Sie DMARC auf Ihren delegierten Subdomains **in der[!DNL Journey Optimizer]** Konfigurations-Benutzeroberfläche ein. [Weitere Informationen](dmarc-record.md#implement-dmarc)

  Für die Einrichtung des CNAME ist jedoch auch ein zusätzlicher Eintrag in Ihrer Hosting-Lösung erforderlich. Daher sollten Sie sich mit Ihrer IT-Abteilung abstimmen, damit diese die in [diesem Abschnitt](dmarc-record.md#implement-dmarc) beschriebene Aktualisierung durchführen kann.

<!--
The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>Wenn Sie Fragen haben oder Unterstützung benötigen, wenden Sie sich an Ihren Kontakt bei der Adobe-Zustellbarkeitsabteilung bzw. beim Adobe-Support.

**Nützliche Links**

* Weitere Informationen über DMARC finden Sie im [Handbuch zu Best Practices bei der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=de#about){target="_blank"}
* [Google-Gmail-Ankündigung](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"} lesen
* [Yahoo!- Ankündigung](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"} lesen

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
