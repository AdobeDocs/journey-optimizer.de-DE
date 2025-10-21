---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Einverständnisrichtlinien
description: Informationen zur Arbeit mit Einverständnisrichtlinien in Adobe Experience Platform
feature: Journeys, Actions, Custom Actions, Privacy, Consent Management
topic: Administration
role: Developer, Admin
level: Experienced
keywords: Richtlinien, Governance, Platform, Healthcare Shield, Einverständnis
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 0aa29a163e337359ea4455edee57bc49fd06a020
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 89%

---

# Arbeiten mit Einverständnisrichtlinien {#consent-management}

Ihre Daten können Nutzungsbeschränkungen unterliegen, die von Ihrer Organisation oder durch gesetzliche Bestimmungen festgelegt werden. Daher müssen Sie dafür sorgen, dass Ihre Datenoperationen in Journey Optimizer mit den [Datennutzungsrichtlinien“ konform ](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=de){target="_blank"}. Diese Richtlinien sind Regeln von Adobe Experience Platform, die festlegen, welche Marketing-Aktionen Sie für Daten ausführen dürfen.

Wenn sich ein Profil vom Erhalt von Nachrichten von Ihnen abgemeldet hat, wird das entsprechende Profil standardmäßig von nachfolgenden Sendungen ausgeschlossen. Sie können eine **Einverständnisrichtlinie** erstellen, die diese Standardlogik überschreibt. Sie können beispielsweise eine Einverständnisrichtlinie in Experience Platform erstellen, um Kunden auszuschließen, die dem Empfang von Nachrichten für einen bestimmten Kanal nicht zugestimmt haben. Wenn keine benutzerdefinierte Richtlinie vorhanden ist, gilt die Standardrichtlinie.

>[!IMPORTANT]
>
>Einverständnisrichtlinien sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** und **Privacy and Security Shield** erworben haben.

Die wichtigsten Schritte zum Anwenden von Einverständnisrichtlinien sind folgende:

1. Erstellen Sie eine Einverständnisrichtlinie in Adobe Experience Platform mit einer zugehörigen Marketing-Aktion. [Erfahren Sie, wie Sie eine Einverständnisrichtlinie erstellen](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#consent-policy){target="_blank"}

2. Wenden Sie Einverständnisrichtlinien in Adobe Journey Optimizer mithilfe von Kanalkonfigurationen oder Journey benutzerdefinierter Aktionen an.

   * Erstellen Sie eine Kanalkonfiguration mit einer zugehörigen Marketing-Aktion. Bei der Erstellung von Kommunikation mithilfe der Kanalkonfiguration wird die zugeordnete Marketingaktion übernommen und die entsprechenden in Adobe Experience Platform definierten Einverständnisrichtlinien angewendet. [Informationen zur Verwendung von Einverständnisrichtlinien durch Kanalkonfigurationen](#surface-marketing-actions)

   * Auf Journey-Ebene können Sie entweder:

      * Verknüpfen Sie bei der Konfiguration einen Kanal und eine Marketing-Aktion mit einer benutzerdefinierten Aktion. [Informationen zur Verwendung von Einverständnisrichtlinien beim Konfigurieren einer benutzerdefinierten Aktion](#consent-custom-action)
      * Definieren Sie beim Hinzufügen einer benutzerdefinierten Aktion zu einer Journey eine zusätzliche Marketing-Aktion. [Informationen zur Verwendung von Einverständnisrichtlinien beim Hinzufügen einer benutzerdefinierten Aktion zu einer Journey](#consent-journey)

## Verwenden von Einverständnisrichtlinien durch Kanalkonfigurationen {#surface-marketing-actions}

In [!DNL Journey Optimizer] wird das Einverständnis durch das [Einverständnisschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=de){target="_blank"} von Experience Platform verarbeitet. Standardmäßig ist der Wert für das Einverständnisfeld leer und gilt als Einverständnis für den Empfang Ihrer Nachrichten. Sie können diesen Standardwert beim Onboarding in einen der möglichen ([ aufgelisteten) Werte ](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=de#choice-values){target="_blank"}.

Um den Wert des Feldes „Einverständnis“ zu ändern, können Sie eine benutzerdefinierte Einverständnisrichtlinie erstellen, in der Sie eine Marketing-Aktion und die Bedingungen definieren, unter denen diese Aktion ausgeführt wird. [Erfahren Sie mehr über Marketing-Aktionen](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=de#marketing-actions){target="_blank"}

Wenn Sie z. B. eine Einverständnisrichtlinie erstellen möchten, um nur Profile anzusprechen, die dem Empfang von E-Mail-Nachrichten zugestimmt haben, führen Sie die folgenden Schritte aus.

1. Stellen Sie sicher, dass Ihr Unternehmen die Zusatzangebote Adobe **Healthcare Shield** oder **Privacy and Security Shield** erworben hat. [Weitere Informationen](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=de){target="_blank"}

1. Erstellen Sie in Adobe Experience Platform eine benutzerdefinierte Richtlinie (über das Menü **[!UICONTROL Datenschutz]** > **[!UICONTROL Richtlinien]**). [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#create-policy){target="_blank"}

   <!--![](assets/consent-policy-create.png)-->

1. Wählen Sie den Typ der **[!UICONTROL Einverständnisrichtlinien]** und konfigurieren Sie eine Bedingung wie folgt. [Erfahren Sie, wie Sie Einverständnisrichtlinien konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#consent-policy){target="_blank"}

   1. Wählen Sie unter dem Abschnitt **[!UICONTROL Wenn]** die standardmäßige Marketing-Aktion **[!UICONTROL E-Mail-Targeting]** aus.

      <!--![](assets/consent-policy-marketing-action.png)-->

      >[!NOTE]
      >
      >Die wichtigsten Marketing-Aktionen, die von Adobe standardmäßig bereitgestellt werden, sind in [dieser Tabelle](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=de#core-actions){target="_blank"} aufgeführt. Die Schritte zum Erstellen einer benutzerdefinierten Marketing-Aktion werden in [diesem Abschnitt](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#create-marketing-action){target="_blank"} aufgeführt.

   1. Wählen Sie aus, was passiert, wenn die Marketing-Aktion angewendet wird. Wählen Sie in diesem Beispiel **[!UICONTROL Zustimmung zum E-Mail-Marketing]**.

   ![](assets/consent-policy-then.png)

1. Speichern und [aktivieren](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#enable){target="_blank"} diese Richtlinie.

1. Erstellen Sie in Journey Optimizer eine E-Mail-Kanalkonfiguration. [Weitere Informationen](../configuration/channel-surfaces.md#create-channel-surface)

1. Wählen Sie in den Details der E-Mail-Konfiguration die Marketing-Aktion **[!UICONTROL E-Mail-Targeting]** aus.

   ![](assets/surface-marketing-action.png)

Alle mit dieser Marketing-Aktion verknüpften Einverständnisrichtlinien werden automatisch verwendet, um die Voreinstellungen Ihrer Kundinnen und Kunden zu respektieren.

Daher wird in diesem Beispiel jede [E-Mail](../email/create-email.md), die diese Konfiguration in einer Kampagne oder einer Journey verwendet, nur an die Profile gesendet, die dem Empfang von E-Mails von Ihnen zugestimmt haben. Profile, die dem Empfang von E-Mail-Nachrichten nicht zugestimmt haben, werden ausgeschlossen.

## Verwenden von Einverständnisrichtlinien durch benutzerdefinierte Aktionen {#journey-custom-actions}

### Wichtige Hinweise {#important-notes}

In Journey Optimizer kann das Einverständnis auch in benutzerdefinierten Aktionen genutzt werden.  Wenn Sie es mit den integrierten Nachrichtenfunktionen verwenden möchten, müssen Sie eine Bedingungsaktivität verwenden, um Kunden in Ihrer Journey zu filtern.

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

### Verwenden von Einverständnisrichtlinien beim Konfigurieren einer benutzerdefinierten Aktion{#consent-custom-action}

Beim Konfigurieren einer benutzerdefinierten Aktion können zwei Felder für die Einverständnisverwaltung verwendet werden.

Im Feld **Kanal** können Sie den mit dieser benutzerdefinierten Aktion verbundenen Kanal auswählen. Dadurch wird das Feld **Erforderliche Marketing-Aktion** mit der standardmäßigen Marketing-Aktion für den ausgewählten Kanal vorausgefüllt. Wenn Sie **Sonstige** auswählen, wird standardmäßig keine Marketing-Aktion definiert. 

![](assets/consent1.png)

Mit der **Erforderlichen Marketing-Aktion** können Sie die Marketing-Aktion für Ihre benutzerdefinierte Aktion definieren. Wenn Sie beispielsweise diese benutzerdefinierte Aktion zum Senden von E-Mails verwenden, können Sie **E-Mail-Targeting** auswählen. Bei Verwendung in einer Journey werden alle mit dieser Marketing-Aktion verknüpften Einverständniserklärungen abgerufen und genutzt.  Es wird eine standardmäßige Marketing-Aktion ausgewählt, Sie können jedoch auf den Abwärtspfeil klicken, um alle verfügbaren Marketing-Aktionen aus der Liste auszuwählen.

![](assets/consent2.png)

Bei bestimmten wichtigen Kommunikationsarten, z. B. Transaktionsnachrichten, die zum Zurücksetzen des Passworts des Kunden gesendet werden, ist es möglicherweise nicht angeraten, eine Einverständniserklärung anzuwenden. Wählen Sie dann im Feld **Erforderliche Marketing-Aktion** **Keine** aus.

Die anderen Schritte zum Konfigurieren einer benutzerdefinierten Aktion werden in [diesem Abschnitt](../action/about-custom-action-configuration.md#consent-management) ausführlicher behandelt.

### Verwenden von Einverständnisrichtlinien beim Hinzufügen einer benutzerdefinierten Aktion zu einer Journey {#consent-journey}

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
