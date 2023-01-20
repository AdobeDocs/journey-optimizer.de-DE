---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Einverständnisrichtlinien
description: Erfahren Sie, wie Sie mit Adobe Experience Platform-Zustimmungsrichtlinien arbeiten.
feature: Privacy
topic: Administration
role: Admin,Developer
level: Experienced
keywords: Politik, Governance, Plattform, Gesundheitsschutz, Einverständnis
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 1177a0ac99035837ff4a7422808bb92a91710f15
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 98%

---

# Arbeiten mit Einverständnisrichtlinien {#consent-management}

Mit Adobe Experience Platform können Sie einfach Marketing-Richtlinien übernehmen und durchsetzen, um die Einverständnispräferenzen Ihrer Kunden zu respektieren. Einverständniserklärungen werden in Adobe Experience Platform definiert. In [dieser Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=de#consent-policy) finden Sie weitere Informationen.

In Journey Optimizer können Sie diese Einverständniserklärungen auf Ihre benutzerdefinierten Aktionen anwenden. Beispielsweise können Sie Einverständniserklärungen definieren, um Kunden auszuschließen, die dem Empfang von E-Mail-, Push- oder SMS-Nachrichten nicht zugestimmt haben.

>[!NOTE]
>
>Einverständniserklärungen sind derzeit nur für Organisationen verfügbar, die das Zusatzangebot zum Healthcare Shield erworben haben.

In Journey Optimizer wird das Einverständnis auf mehreren Ebenen definiert:

* beim **Konfigurieren einer benutzerdefinierten Aktion** können Sie einen Kanal und eine Marketing-Aktion definieren. Weitere Informationen finden Sie in diesem [Abschnitt](../action/consent.md#consent-custom-action).
* beim Hinzufügen der **benutzerdefinierten Aktion in einer Journey** können Sie eine zusätzliche Marketing-Aktion definieren. Weitere Informationen finden Sie in diesem [Abschnitt](../action/consent.md#consent-journey).

## Wichtige Hinweise {#important-notes}

In Journey Optimizer kann das Einverständnis in benutzerdefinierten Aktionen genutzt werden. Wenn Sie es mit den integrierten Nachrichtenfunktionen verwenden möchten, müssen Sie eine Bedingungsaktivität verwenden, um Kunden in Ihrer Journey zu filtern.

Mit der Einverständnisverwaltung werden zwei Journey-Aktivitäten analysiert:

* Segment lesen: das abgerufene Segment wird berücksichtigt.
* Benutzerdefinierte Aktion: Die Einverständnisverwaltung berücksichtigt die verwendeten Attribute ([Aktionsparameter](../action/about-custom-action-configuration.md#define-the-message-parameters)) sowie die definierte(n) Marketing-Aktion(en) (erforderliche Marketing-Aktion und zusätzliche Marketing-Aktion).
* Attribute, die Teil einer Feldergruppe sind, die das vordefinierte Vereinigungsschema verwendet, werden nicht unterstützt. Diese Attribute werden in der Benutzeroberfläche ausgeblendet. Sie müssen eine weitere Feldergruppe mit einem anderen Schema erstellen.
* Die Einverständniserklärungen gelten nur, wenn eine Marketing-Aktion (erforderlich oder zusätzlich) auf der Ebene der benutzerdefinierten Aktion festgelegt ist.

Alle anderen in einer Journey verwendeten Aktivitäten werden nicht berücksichtigt. Wenn Sie Ihre Journey mit einer Segmentqualifikation starten, wird das Segment nicht berücksichtigt.

Wenn in einer Journey ein Profil durch eine Einverständniserklärung in einer benutzerdefinierten Aktion ausgeschlossen wird, wird ihm die Nachricht nicht gesendet, aber es setzt die Journey fort. Das Profil gelangt nicht in den Pfad für Zeitüberschreitung und Fehler, wenn eine Bedingung verwendet wird.

Bevor Sie Richtlinien in einer benutzerdefinierten Aktion aktualisieren, die in einer Journey platziert wird, stellen Sie sicher, dass Ihre Journey keinen Fehler enthält.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## Konfigurieren der benutzerdefinierten Aktion {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_admin"
>title="Definieren einer erforderlichen Marketing-Aktion"
>abstract="Mit der „Erforderlichen Marketing-Aktion“ können Sie die Marketing-Aktion für Ihre benutzerdefinierte Aktion definieren. Wenn Sie beispielsweise diese benutzerdefinierte Aktion zum Senden von E-Mails verwenden, können Sie E-Mail-Targeting auswählen. Bei Verwendung in einer Journey werden alle mit dieser Marketing-Aktion verknüpften Einverständniserklärungen abgerufen und genutzt. Dies kann nicht in der Arbeitsfläche geändert werden."

Beim Konfigurieren einer benutzerdefinierten Aktion können zwei Felder für die Einverständnisverwaltung verwendet werden.

Im Feld **Kanal** können Sie den Kanal für diese benutzerdefinierte Aktion auswählen: **E-Mail**, **SMS** oder **Push-Benachrichtigung**. Dadurch wird die **Erforderliche Marketing-Aktion** mit der standardmäßigen Marketing-Aktion für den ausgewählten Kanal vorausgefüllt. Wenn Sie **Sonstige** auswählen, wird standardmäßig keine Marketing-Aktion definiert.

![](assets/consent1.png)

Mit der **Erforderlichen Marketing-Aktion** können Sie die Marketing-Aktion für Ihre benutzerdefinierte Aktion definieren. Wenn Sie beispielsweise diese benutzerdefinierte Aktion zum Senden von E-Mails verwenden, können Sie **E-Mail-Targeting** auswählen. Bei Verwendung in einer Journey werden alle mit dieser Marketing-Aktion verknüpften Einverständniserklärungen abgerufen und genutzt. Es wird eine standardmäßige Marketing-Aktion ausgewählt, Sie können jedoch auf den Abwärtspfeil klicken, um alle verfügbaren Marketing-Aktionen aus der Liste auszuwählen.

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

Sie können eine **Zusätzliche Marketing-Aktion** definieren, um den Typ der benutzerdefinierten Aktion festzulegen. Auf diese Weise können Sie den Zweck der benutzerdefinierten Aktion in dieser Journey definieren. Zusätzlich zur erforderlichen Marketing-Aktion, die normalerweise kanalspezifisch ist, können Sie eine zusätzliche Marketing-Aktion definieren, die speziell für die benutzerdefinierte Aktion in dieser bestimmten Journey gilt. Beispiel: eine Workout-Nachricht, Newsletter, Fitness-Nachricht usw. Sowohl die erforderliche Marketing-Aktion als auch die zusätzliche Marketing-Aktion kommen zur Anwendung.

![](assets/consent3.png)

Klicken Sie auf **Erklärungen aktualisieren** unten im Bildschirm, um die Liste der für diese benutzerdefinierte Aktion berücksichtigten Erklärungenn zu aktualisieren und zu überprüfen. Dies dient nur zu Informationszwecken beim Erstellen einer Journey. Bei Live-Journeys werden Einverständniserklärungen automatisch alle 6 Stunden abgerufen und aktualisiert.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-segment.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

Die anderen Schritte zum Konfigurieren einer benutzerdefinierten Aktion in einem Journey werden in [diesem Abschnitt](../building-journeys/using-custom-actions.md) ausführlicher behandelt.
