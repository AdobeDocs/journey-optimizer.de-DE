---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Einverständnisrichtlinien
description: Informationen zur Arbeit mit Einverständnisrichtlinien in Adobe Experience Platform
feature: Journeys, Actions, Custom Actions, Privacy, Consent Management
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Richtlinien, Governance, Platform, Healthcare Shield, Einverständnis
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 334527cbad3363b77d14dd447e06d4e8da79daec
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 100%

---

# Arbeiten mit Einverständnisrichtlinien {#consent-management}

Ihre Daten können Nutzungsbeschränkungen unterliegen, die von Ihrer Organisation oder durch gesetzliche Bestimmungen festgelegt werden. Daher müssen Sie sicherstellen, dass Ihre Datenvorgänge in Journey Optimizer mit [Datennutzungsrichtlinien](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=de) konform sind{target="_blank"}. These policies are Adobe Experience Platform rules defining which [marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=de#marketing-actions){target="_blank"} Sie für Daten durchführen dürfen.

Ein Typ verfügbarer Datennutzungsrichtlinien sind **Einverständnisrichtlinien**. Mit diesen können Sie einfach Marketing-Richtlinien übernehmen und durchsetzen, um die Einverständnispräferenzen Ihrer Kundinnen und Kunden zu respektieren. [Weitere Informationen zur Durchsetzung von Richtlinien](https://experienceleague.adobe.com/docs/experience-platform/data-governance/enforcement/auto-enforcement.html?lang=de){target="_blank"}

>[!IMPORTANT]
>
>Einverständnisrichtlinien sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** und **Privacy and Security Shield** erworben haben.

Beispielsweise können Sie [Einverständnisrichtlinien in Experience Platform erstellen](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#consent-policy){target="_blank"}, um Kundinnen und Kunden auszuschließen, die dem Empfang von E-Mail-, Push- oder SMS-Kommunikationen nicht zugestimmt haben.

<!--* For the native outbound channels (Email, Push, SMS, Direct mail), the logic is as follows:

    * By default, if a profile has opted out from receiving communications from you, the corresponding profile is excluded from subsequent deliveries.

    * If you have the Adobe **Healthcare Shield** or **Privacy and Security Shield**, you can create a custom consent policy that overrides the default logic. For example, you can define a policy to only send email messages to all individuals who have opted in. In the absence of a custom policy, the default policy applies.
    
    To apply a custom policy, you need to define a marketing action in that policy and associate it to a channel surface. [Learn more](#marketing-actions)-->

Auf der Journey-Ebene können Sie Einverständnisrichtlinien auf Ihre benutzerdefinierten Aktionen anwenden:

* Beim **Konfigurieren einer benutzerdefinierten Aktion** können Sie einen Kanal und eine Marketing-Aktion definieren. [Weitere Informationen](#consent-custom-action)
* Beim Hinzufügen der **benutzerdefinierten Aktion in einer Journey** können Sie eine zusätzliche Marketing-Aktion definieren. [Weitere Informationen](#consent-journey)

<!--

## Leverage consent policies through channel surfaces {#marketing-actions}

In [!DNL Journey Optimizer], consent is handled by the Experience Platform [Consent schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target="_blank"}.

To modify the consent field value, you can create a custom consent policy in which you define a marketing action and the conditions under which that action is performed. [Learn more on marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html#marketing-actions){target="_blank"}

For example, if you want to create a consent policy to target only profiles who have consented to receive email communications, follow the steps below.

1. Make sure your organization has purchased the Adobe **Healthcare Shield** or **Privacy and Security Shield** add-on offerings. [Learn more](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html){target="_blank"}

1. In Adobe Experience Platform, create a custom policy (from the **[!UICONTROL Privacy]** > **[!UICONTROL Policies]** menu). [Learn how](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-policy){target="_blank"}

    ![](assets/consent-policy-create.png)

1. Choose the **[!UICONTROL Consent policy]** type and configure a condition as follows. [Learn how to configure consent policies](https://experienceleague-review.corp.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy){target="_blank"}

    1. Under the **[!UICONTROL If]** section, select the **[!UICONTROL Email Targeting]** default marketing action.

        ![](assets/consent-policy-marketing-action.png)

        >[!NOTE]
        >
        >The core marketing actions provided out-of-the-box by Adobe are listed in [this table](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=en#core-actions){target="_blank"}. The steps to create a custom marketing action are listed in [this section](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-marketing-action){target="_blank"}.

    1. Select what happens when the marketing action applies. In this example, select **[!UICONTROL Email Marketing Consent]**.

    ![](assets/consent-policy-then.png)

1. Save and [enable](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#enable){target="_blank"} this policy.

1. In Journey Optimizer, create an email surface. [Learn how](../configuration/channel-surfaces.md#create-channel-surface)

1. In the email surface details, select the **[!UICONTROL Email Targeting]** marketing action.

    ![](assets/surface-marketing-action.png)

All consent policies associated with that marketing action are automatically leveraged in order to respect the preferences of your customers.

Therefore, in this example, any [email](../email/create-email.md) using that surface in a campaign or a journey is only sent to the profiles who have consented to receive emails from you. Profiles who have not consented to receive email communications are excluded.-->

## Verwenden von Einverständnisrichtlinien durch benutzerdefinierte Aktionen {#journey-custom-actions}

### Wichtige Hinweise {#important-notes}

In Journey Optimizer kann das Einverständnis <!--also -->in benutzerdefinierten Aktionen genutzt werden.  Wenn Sie es mit den integrierten Nachrichtenfunktionen verwenden möchten, müssen Sie eine Bedingungsaktivität verwenden, um Kunden in Ihrer Journey zu filtern.

Mit der Einverständnisverwaltung werden zwei Journey-Aktivitäten analysiert:

* Zielgruppe lesen: Die abgerufene Zielgruppe wird berücksichtigt.
* Benutzerdefinierte Aktion: Die Einverständnisverwaltung berücksichtigt die verwendeten Attribute ([Aktionsparameter](../action/about-custom-action-configuration.md#define-the-message-parameters)) sowie die definierte(n) Marketing-Aktion(en) (erforderliche Marketing-Aktion und zusätzliche Marketing-Aktion).
* Attribute, die Teil einer Feldergruppe sind, die das vordefinierte Vereinigungsschema verwendet, werden nicht unterstützt. Diese Attribute werden in der Benutzeroberfläche ausgeblendet. Sie müssen eine weitere Feldergruppe mit einem anderen Schema erstellen.
* Die Einverständniserklärungen gelten nur, wenn eine Marketing-Aktion (erforderlich oder zusätzlich) auf der Ebene der benutzerdefinierten Aktion festgelegt ist.

Alle anderen in einer Journey verwendeten Aktivitäten werden nicht berücksichtigt. Wenn Sie Ihre Journey mit einer Zielgruppen-Qualifizierung beginnen, wird die Zielgruppe nicht berücksichtigt.

Wenn in einer Journey ein Profil durch eine Einverständniserklärung in einer benutzerdefinierten Aktion ausgeschlossen wird, wird ihm die Nachricht nicht gesendet, aber es setzt die Journey fort. Das Profil gelangt nicht in den Pfad für Zeitüberschreitung und Fehler, wenn eine Bedingung verwendet wird.

Bevor Sie Richtlinien in einer benutzerdefinierten Aktion aktualisieren, die in einer Journey platziert wird, stellen Sie sicher, dass Ihre Journey keinen Fehler enthält.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

### Konfigurieren der benutzerdefinierten Aktion {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action"
>title="Definieren einer erforderlichen Marketing-Aktion"
>abstract="Mit der „Erforderlichen Marketing-Aktion“ können Sie die Marketing-Aktion für Ihre benutzerdefinierte Aktion definieren. Wenn Sie beispielsweise diese benutzerdefinierte Aktion zum Senden von E-Mails verwenden, können Sie E-Mail-Targeting auswählen. Bei Verwendung in einer Journey werden alle mit dieser Marketing-Aktion verknüpften Einverständniserklärungen abgerufen und genutzt. Dies kann nicht in der Arbeitsfläche geändert werden."

Beim Konfigurieren einer benutzerdefinierten Aktion können zwei Felder für die Einverständnisverwaltung verwendet werden.

Im Feld **Kanal** können Sie den Kanal für diese benutzerdefinierte Aktion auswählen: **E-Mail**, **SMS** oder **Push-Benachrichtigung**. Dadurch wird das Feld **Erforderliche Marketing-Aktion** mit der standardmäßigen Marketing-Aktion für den ausgewählten Kanal vorausgefüllt. Wenn Sie **Sonstige** auswählen, wird standardmäßig keine Marketing-Aktion definiert. 

![](assets/consent1.png)

Mit der **Erforderlichen Marketing-Aktion** können Sie die Marketing-Aktion für Ihre benutzerdefinierte Aktion definieren. Wenn Sie beispielsweise diese benutzerdefinierte Aktion zum Senden von E-Mails verwenden, können Sie **E-Mail-Targeting** auswählen. Bei Verwendung in einer Journey werden alle mit dieser Marketing-Aktion verknüpften Einverständniserklärungen abgerufen und genutzt.  Es wird eine standardmäßige Marketing-Aktion ausgewählt, Sie können jedoch auf den Abwärtspfeil klicken, um alle verfügbaren Marketing-Aktionen aus der Liste auszuwählen.

![](assets/consent2.png)

Bei bestimmten wichtigen Kommunikationsarten, z. B. Transaktionsnachrichten, die zum Zurücksetzen des Passworts des Kunden gesendet werden, ist es möglicherweise nicht angeraten, eine Einverständniserklärung anzuwenden. Wählen Sie dann im Feld **Erforderliche Marketing-Aktion** **Keine** aus.

Die anderen Schritte zum Konfigurieren einer benutzerdefinierten Aktion werden in [diesem Abschnitt](../action/about-custom-action-configuration.md#consent-management) ausführlicher behandelt.

### Erstellen der Journey {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="Erforderliche Marketing-Aktion"
>abstract="Eine erforderliche Marketing-Aktion wird beim Erstellen einer benutzerdefinierten Aktion definiert. Diese erforderliche Marketing-Aktion kann nicht aus der Aktion entfernt oder geändert werden."

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="Zusätzliche Marketing-Aktion"
>abstract="Fügen Sie zusätzlich zur erforderlichen Marketing-Aktion eine weitere Marketing-Aktion hinzu. Für beide Marketing-Aktionen werden Einverständniserklärungen erzwungen."

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="Visualisieren von Einverständniserklärungen, die zur Laufzeit gelten"
>abstract="Marketing-Aktionen beinhalten Einverständniserklärungen, die Aktionsparameter und individuelle Einverständniswerte des Profils kombinieren, um Benutzer herauszufiltern. Rufen Sie die neueste Definition dieser Erklärungen ab, indem Sie auf den Button klicken, um sie zu aktualisieren."

Beim Hinzufügen der benutzerdefinierten Aktion zu einer Journey können Sie mit verschiedenen Optionen das Einverständnis verwalten. Klicken Sie auf **Schreibgeschützte Felder anzeigen**, um alle Parameter anzuzeigen.

Der **Kanal** und die **Erforderliche Marketing-Aktion**, die bei der Konfiguration der benutzerdefinierten Aktion definiert wurden, werden oben im Bildschirm angezeigt. Sie können diese Felder nicht ändern.

![](assets/consent4.png)

Sie können eine **Zusätzliche Marketing-Aktion** definieren, um den Typ der benutzerdefinierten Aktion festzulegen. Auf diese Weise können Sie den Zweck der benutzerdefinierten Aktion in dieser Journey definieren. Zusätzlich zur erforderlichen Marketing-Aktion, die normalerweise kanalspezifisch ist, können Sie eine zusätzliche Marketing-Aktion definieren, die speziell für die benutzerdefinierte Aktion in dieser bestimmten Journey gilt.  Beispiel: eine Workout-Kommunikation, ein Newsletter, eine Fitness-Kommunikation usw. Sowohl die erforderliche Marketing-Aktion als auch die zusätzliche Marketing-Aktion kommen zur Anwendung.

![](assets/consent3.png)

Klicken Sie auf **Erklärungen aktualisieren** unten im Bildschirm, um die Liste der für diese benutzerdefinierte Aktion berücksichtigten Erklärungenn zu aktualisieren und zu überprüfen. Dies dient nur zu Informationszwecken beim Erstellen einer Journey. Bei Live-Journeys werden Einverständniserklärungen automatisch alle 6 Stunden abgerufen und aktualisiert.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-audience.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

Die anderen Schritte zum Konfigurieren einer benutzerdefinierten Aktion in einem Journey werden in [diesem Abschnitt](../building-journeys/using-custom-actions.md) ausführlicher behandelt.
