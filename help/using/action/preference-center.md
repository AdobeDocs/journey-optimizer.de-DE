---
solution: Journey Optimizer
product: journey optimizer
title: Kundeneinstellungen verwalten
description: Erfahren Sie, wie Sie die Voreinstellungen von Benutzenden mithilfe von Einverständnisrichtlinien verwalten
feature: Journeys, Privacy, Consent Management, Landing Pages
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Richtlinien, Governance, Plattform, Einverständnis, Healthcare Shield
source-git-commit: bbea90bd21bd19941e8c8df93c8ec7a8a2769d77
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 4%

---

# Kundeneinstellungen verwalten {#preference-center}

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** oder **Privacy and Security Shield** erworben haben.

In einem modernen Ökosystem der Marketing-Automatisierung interagieren Marken mit Kunden über verschiedene Touchpoints hinweg und sehen sich dem Risiko irrelevanter oder übermäßiger Kommunikation ausgesetzt, was zu Interaktion, Spam-Beschwerden und Compliance-Risiken führt. Aus diesem Grund müssen sie die Präferenzen ihrer Kunden verwalten, um Echtzeiteinblicke in ihre Zielgruppe zu erhalten und personalisierte, respektvolle Kommunikation bereitzustellen.

Mit [!DNL Adobe Journey Optimizer] können Sie durch die Verwendung [Einverständnisrichtlinien](consent.md) die Vorlieben Ihrer Kunden berücksichtigen<!-- in terms of **channels** and **topics**-->. Dadurch wird sichergestellt, dass [!DNL Journey Optimizer] nur Kunden anspricht, die auf ihrer <!-- their preferred channels and on the subscription topics--> basieren, und gleichzeitig ihr Einverständnis respektiert.

Um die Benutzereinstellungen mit [!DNL Journey Optimizer] zu verwalten, haben Sie folgende Möglichkeiten:

* Rufen Sie die Zustimmung Ihrer Kundinnen und Kunden zum Opt-in/Opt-out für einen nativen ausgehenden Kanal ab. Erstellen Sie beispielsweise eine Einverständnisrichtlinie, [!DNL Experience Platform] Kunden auszuschließen, die dem Empfang von Nachrichten für einen bestimmten Kanal nicht zugestimmt haben. Wenden Sie diese Einverständnisrichtlinie dann mithilfe einer E-Mail-Kanal-Konfiguration in [!DNL Journey Optimizer] an. [Weitere Informationen](consent.md#surface-marketing-actions)

  >[!NOTE]
  >
  >Die unterstützten Kanäle sind E-Mail, Push, SMS und InApp.<!--To check-->

* Fragen Sie Ihre Kunden, welche Themen sie abonnieren möchten (z. B. welche Art von Nachrichten sie akzeptieren oder nicht). [Weitere Informationen](#manage-preferences)

>[!IMPORTANT]
>
>Das Einverständnis hat Vorrang vor den Voreinstellungen. Beispielsweise hat eine Ihrer Kundinnen und Kunden angegeben, dass ihr bevorzugter Kanal E-Mail ist und dass sie dem Empfang von Newslettern zugestimmt haben<!-- they are interested in yoga-->. Wenn sie sich jedoch gegen den Erhalt von Nachrichten von Ihnen entschieden haben, können sie nicht von einem E-Mail-Newsletter angesprochen werden, den Sie senden<!-- on yoga-->.

## Aufzeichnen und Berücksichtigen von Voreinstellungen {#manage-preferences}

Mit Einverständnisrichtlinien in [!DNL Journey Optimizer] können Sie die Voreinstellungen Ihrer Kunden zentral verwalten. Auf diese Weise können Sie sicherstellen, dass Sie Kundinnen und Kunden nur auf der Grundlage der von ihnen ausgewählten Themen ansprechen und dabei ihre Einverständnisentscheidungen respektieren. Gehen Sie dazu wie folgt vor.

Angenommen, Sie möchten Ihre Kunden anhand ihrer Kommunikationsvoreinstellungen über mehrere Abonnementthemen (*Newsletter*, *Angebote* und *Produkteinführungen*) durch Journey und Kampagnen ansprechen.

1. Definieren Sie Präferenzattribute mit dem booleschen Operator auf Profilebene<!--how??-->. Sie können beispielsweise Folgendes angeben:

   * *Newsletter_Email* - Boolesch (true/false)
   * *offers_push* - Boolesch (true/false)
   * *Neue Produkteinführungen* - Boolesch (true/false)

   Diese Attribute werden im Schema eines profilaktivierten Datensatzes ([) erfasst ](../data/get-started-datasets.md) dem [Unified Customer Profile](../audience/get-started-profiles.md) zugeordnet.

   >[!NOTE]
   >
   >Kundenzustimmung und Kontaktvoreinstellungen sind komplexe Themen. Um zu erfahren, wie Einverständnis- und Kontextvoreinstellungen in [!DNL Experience Platform] erfasst, verarbeitet und gefiltert werden können, sollten Sie die folgenden Dokumente lesen:
   >
   >* Informationen zu den Schemafeldgruppen, die zum Erfassen von Einverständnisdaten erforderlich sind, finden Sie auf [dieser Seite](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/overview){target="_blank"}. Es wird beschrieben, wie Sie die von Ihren Kunden erfassten Einverständnisdaten verarbeiten und in Ihre gespeicherten Kundenprofile integrieren können.
   >* Weitere Informationen zur Feldergruppe „Einverständnis“ und „Voreinstellungen“ finden Sie auf [dieser Seite](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/consents#ingest){target="_blank"}.
   >* Um benutzerdefinierte Voreinstellungsfelder zum Schema hinzuzufügen, führen Sie die Schritte in [diesem Abschnitt](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/dataset#custom-consent){target="_blank"} aus.

1. Erstellen Sie eine Seite, um die Voreinstellungen Ihrer Kunden zu erfassen. Verwenden Sie eine der folgenden Methoden:

   * Erstellen Sie eine Web-Seite, um die Voreinstellungen Ihrer Kunden mithilfe der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/home){target="_blank"} aufzuzeichnen.

   * Verwenden Sie eine [!DNL Journey Optimizer] [Landingpage](../landing-pages/create-lp.md) die Formulare enthält, um die Voreinstellungen Ihrer Kunden mithilfe von Profildaten zu erfassen.  [Weitere Informationen zu Formularen](../landing-pages/lp-forms.md) <!--Forms not released/announced yet - TBC-->

     >[!NOTE]
     >
     >Stellen Sie sicher, dass die Domain der verwendeten Landingpage zur oberen Marke und nicht zu einer Untermarke gehört. Die erfassten Voreinstellungen werden in den Profildaten gespeichert, die auf der Ebene der übergeordneten Marke gespeichert sind.

1. Auf dieser Seite können Kundinnen und Kunden ihre Voreinstellungen, z. B. themenbezogene Abonnements, aktualisieren, indem sie Kontrollkästchen aktivieren oder deaktivieren.

   Trigger Jede Aktion gibt ein Einverständnisereignis aus, das für die entsprechenden Profilattribute gespeichert wird (`true` für Opt-in, `false` für Opt-out), indem die Daten in das profilaktivierte Datensatzschema aufgenommen werden<!-- that contains the corresponding preference fields-->.

   <!--Record your users' preferences through the web page or landing page that you created. The data is saved against the corresponding profile, meaning that the preference data is ingested into a Profile-enabled dataset whose schema contains consent/preference fields.-->

   Ein Benutzer <!--whose email address is john.black@lumamail.com--> beispielsweise dem Empfang von Push-Angeboten zugestimmt, möchte jedoch keine E-Mail-Newsletter erhalten. Das entsprechende Profil wird wie folgt aktualisiert:

   ![](assets/profile-preference-attributes.png){width=80%}

<!--The corresponding profile dataset is updated as follows:

|Attribute = Email id | Attribute = Offers_Push | Attribute = Newsletters_Email |
|---------|----------|---------|
| john.black@lumamail.com | Y | N |-->

    >[!NOTE]
    >
    >Die eingehenden Einverständnisereignisse werden in das Kundenprofil eingespeist, sodass Echtzeit-Aktualisierungen gewährleistet sind. Jedes Profil spiegelt die neuesten Auswahlmöglichkeiten in den Abonnementvoreinstellungen wider.

1. Erstellen Sie in Adobe Experience Platform eine benutzerdefinierte Richtlinie (über das Menü **[!UICONTROL Datenschutz]** > **[!UICONTROL Richtlinien]**). [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#create-policy){target="_blank"}

   >[!AVAILABILITY]
   >
   >Einverständnisrichtlinien sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** oder **Privacy and Security Shield** erworben haben. [Weitere Informationen zu Einverständnisrichtlinien](consent.md)

   Um Einverständnisrichtlinien verwenden zu können, müssen in den Profildaten Präferenzattribute vorhanden sein. Daher müssen Sie diese Attribute auf Profilebene definieren (wie in Schritt 1 beschrieben).

1. Wählen Sie den Typ der **[!UICONTROL Einverständnisrichtlinien]** und konfigurieren Sie eine Bedingung wie folgt. [Erfahren Sie, wie Sie Einverständnisrichtlinien konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#consent-policy){target="_blank"}

<!--Consent policies are comprised of two logical components:

* **If**: The condition that will trigger the policy check, based on a certain marketing action (email, SMS, push, custom action, etc.) being performed, the presence of certain data usage labels, or a combination of the two.

* **Then**: The consent attribute must be present for a profile to be included in the action that triggered the policy. More than one field can also be selected.-->

    Um beispielsweise Nachrichten nur an Kundinnen und Kunden zu senden, die sich nicht gegen den Erhalt von E-Mail-Newslettern entschieden haben, erstellen Sie eine benutzerdefinierte Richtlinie und definieren Sie die folgende Bedingung:
    
    * Wenn **[!UICONTROL Marketing-Aktion]** gleich **[!UICONTROL E-Mail]**
    
    * Dann **[!UICONTROL Newsletter_E-Mail]** nicht vorhanden ist **[!UICONTROL false]** Oder **[!UICONTROL Newsletter_E-]**nicht gleich **[!UICONTROL false]**
    
    ![](assets/consent-policy-email-newsletter.png){width=80%}
    
    >[!TIP]
    >
    >Der Datensatz mit aktiviertem Profil muss das Profilattribut **[!UICONTROL Newsletter_Email]** mit dem Wert „true“ enthalten (wie in Schritt 1 beschrieben)

1. Journey Nachdem Sie die Einverständnisrichtlinie erstellt haben, nutzen Sie sie in [!DNL Journey Optimizer] mithilfe von [Kanalkonfigurationen](consent.md#surface-marketing-actions) oder [benutzerdefinierten Aktionen](consent.md#journey-custom-actions).

1. Jetzt können Sie diese Kanalkonfigurationen oder benutzerdefinierten Aktionen in Ihren Journey und Kampagnen verwenden, um sicherzustellen, dass die Voreinstellungen Ihrer <!--targeted--> Kunden berücksichtigt werden.
