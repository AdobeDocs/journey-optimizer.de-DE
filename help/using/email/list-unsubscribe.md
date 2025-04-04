---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren zum Abmelden von der Liste
description: Erfahren Sie, wie Sie beim Festlegen der Kanalkonfiguration eine URL zum Abmelden mit einem Klick in der E-Mail-Kopfzeile einfügen.
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: Einstellungen, E-Mail, Konfiguration
exl-id: c6c77975-ec9c-44c8-a8d8-50ca6231fea6
source-git-commit: 0fd6c054b9b4df9e3ed900c610e0d1186e479750
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 61%

---

# Abmelden von der Liste{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

In [!DNL Adobe Journey Optimizer] wird beim Konfigurieren einer neuen E-Mail-Kanal-Konfiguration bei der [Auswahl einer Subdomain](email-settings.md#subdomains-and-ip-pools) aus der Liste die Option **[!UICONTROL Listen-Abonnement]** aktivieren) angezeigt. Diese ist standardmäßig aktiviert.

![](assets/preset-list-unsubscribe.png)

Die Abmelde-URL mit einem Klick ist ein Abmelde-Link oder eine Schaltfläche neben den E-Mail-Absenderinformationen, über den bzw. die Empfänger Ihre Mailing-Listen sofort mit einem einzigen Klick abmelden können.

Beispielsweise zeigt die URL zum Abmelden mit einem Klick einen Link wie unten in Gmail an:

![](assets/preset-list-unsubscribe-header.png)

>[!IMPORTANT]
>
>Um die URL zum Abmelden mit einem Klick in der Kopfzeile der E-Mail anzuzeigen, muss der E-Mail-Client der Empfängerinnen und Empfänger diese Funktion unterstützen.

Je nach E-Mail-Client und den Abmeldeeinstellungen der E-Mail-Konfiguration kann das Klicken auf den Abmelde-Link in der E-Mail-Kopfzeile die folgenden Auswirkungen haben:

* Wenn die Funktion **E-Mail an (abmelden)** aktiviert ist, wird die Abmeldeanfrage an die Standardadresse zur Abmeldung gesendet, die auf der von Ihnen konfigurierten Subdomain basiert.
* Wenn die Funktion **URL zum Abmelden mit einem Klick** aktiviert ist – oder wenn Sie eine Abmelde-URL in den Inhalt Ihres E-Mail-Textkörpers eingefügt haben – werden Empfängerinnen und Empfänger direkt abgemeldet, und zwar entweder auf Kanal- oder ID-Ebene (je nach Einverständniseinstellungen), wenn sie auf die URL zum Abmelden mit einem Klick (basierend auf der von Ihnen konfigurierten Subdomain) klicken.

>[!NOTE]
>
>Wie Sie die Abmeldeeinstellungen verwalten, erfahren Sie in [diesem Abschnitt](#enable-list-unsubscribe) unten.

Wenn ein Empfänger auf den Abmelde-Link klickt, wird in beiden Fällen seine Abmelde-Anfrage entsprechend verarbeitet. Das entsprechende Profil wird sofort abgemeldet und in [Experience Platform aktualisiert](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=de#getting-started){target="_blank"}.

>[!NOTE]
>
>Gelegentlich kann es aufgrund der nachgelagerten Datenverarbeitung länger dauern, bis Ereignisse abgemeldet werden. Warten Sie etwas, bis das System aktualisiert wurde.

## Option „Abmelden von der Liste aktivieren“ {#enable-list-unsubscribe}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Hinzufügen einer Abmelde-URL zu Ihren E-Mails"
>abstract="Aktivieren Sie diese Option, um automatisch eine Abmelde-URL zur E-Mail-Kopfzeile hinzuzufügen. Sie können auch eine Abmelde-URL in einer Nachricht einrichten, indem Sie einen Ein-Klick-Ausschluss-Link in den Inhalt der E-Mail einfügen."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/email/email-opt-out#one-click-opt-out" text="Festlegen des Opt-outs mit einem Klick über den E-Mail-Inhalt"

Wenn die Option **[!UICONTROL Abmelden von einer Liste aktivieren]** aktiviert ist und vom E-Mail-Client der Empfänger unterstützt wird, enthält die E-Mail-Kopfzeile standardmäßig sowohl ein Mailto als auch eine URL, die Empfänger verwenden können, um sich von Ihrer Mailing-Liste abzumelden.

>[!NOTE]
>
>Wenn Sie diese Option deaktivieren, wird in der E-Mail-Kopfzeile keine URL zum Abmelden mit einem Klick angezeigt.

Die Kopfzeile „Von der Liste abmelden“ bietet zwei Funktionen, die standardmäßig aktiviert sind, sofern Sie nicht eine oder beide Funktionen deaktivieren:

![](assets/surface-list-unsubscribe.png){width="80%"}

* Eine **[!UICONTROL Mailto (unsubscribe)]**-Adresse, die die Zieladresse ist, an die Abmeldeanfragen zur automatischen Verarbeitung weitergeleitet werden. In [!DNL Journey Optimizer] ist die Abmelde-E-Mail-Adresse die standardmäßig **[!UICONTROL Mailto (unsubscribe)]** Adresse, die in der Kanalkonfiguration angezeigt wird, basierend auf der [ausgewählten Subdomain](email-settings.md#subdomains). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* Die **[!UICONTROL 1-Klick-Abmelde-URL]**, die standardmäßig die Kopfzeile der mit einem Klick-Opt-out-URL generierten Liste zur Abmeldung ist, basierend auf der [ausgewählten Subdomain](email-settings.md#subdomains). <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Die Einverständnisstufe kann aus der Dropdown-Liste **[!UICONTROL Einverständnisstufe]** ausgewählt werden. Sie kann sich auf den Kanal oder die Profilidentität beziehen. Basierend auf dieser Einstellung wird das Einverständnis in [!DNL Adobe Journey Optimizer] entweder auf Kanal- oder ID-Ebene aktualisiert, wenn sich jemand über die URL zum Abmelden von Listen in der Kopfzeile einer E-Mail abmeldet.

## Leitlinien und Empfehlungen {#list-unsubscribe-guardrails}

Die Funktion Abmelde-URL mit einem Klick ermöglicht es Ihren Empfängern, sich ganz einfach von Ihrer Kommunikation abzumelden. Da jedoch nicht alle E-Mail-Clients diesen Link in der E-Mail-Kopfzeile unterstützen, empfiehlt Adobe, auch einen [Ein-Klick-Opt-out-Link](email-opt-out.md#one-click-opt-out) oder einen [Abmelde-Link](email-opt-out.md#add-unsubscribe-link) in den Textkörper Ihrer E-Mail einzufügen.

Die Funktionen **[!UICONTROL E-Mail an (abmelden)]** und **[!UICONTROL URL zum Abmelden mit einem Klick]** sind optional. 

* Wenn Sie die Option **[!UICONTROL Abmelden von der Liste aktivieren]** in den [E-Mail-Konfigurationseinstellungen](email-settings.md) aktiviert haben, empfehlen wir, beide Methoden zu aktivieren – sowohl **E-Mail an (abmelden)** als auch **URL zum Abmelden mit einem Klick**. Nicht alle E-Mail-Clients unterstützen die HTTP-Methode. Mit der Funktion Mailto list-unsubscribe , mit der Sie eine Alternative auswählen können, kann Ihre Reputation als Absender besser geschützt werden und alle Ihre Empfänger können auf die Abmeldefunktion zugreifen.

* Wenn Sie die standardmäßig generierte Ein-Klick-Abmelde-URL nicht verwenden möchten, können Sie die Funktion deaktivieren.

   * In einem Szenario, in dem die Option **[!UICONTROL Abmelden von der Liste aktivieren]** aktiviert ist und die Funktion **[!UICONTROL URL zum Abmelden mit einem Klick]** deaktiviert ist und ein [Ausschluss-Link mit einem Klick](../email/email-opt-out.md#one-click-opt-out) zu einer Nachricht hinzugefügt wird, die mit dieser Konfiguration erstellt wurde, nimmt die Option „Abmelde-Link in Kopfzeile“ den Link zum Abmelden mit einem Klick auf, den Sie im Textkörper der E-Mail eingefügt haben, und verwendet ihn als den URL-Wert zum Abmelden mit einem Klick.

     ![](assets/preset-list-unsubscribe-opt-out-url.png)

   * Wenn Sie keinen Ein-Klick-Ausschluss-Link in den Nachrichteninhalt einfügen und die standardmäßige **[!UICONTROL URL zum Abmelden mit einem Klick]** in den Einstellungen der Kanalkonfiguration deaktiviert ist, wird keine URL als Teil des Abmelde-Links in der Kopfzeile in die E-Mail-Kopfzeile übernommen.

  >[!NOTE]
  >
  >In [diesem Abschnitt](../email/email-opt-out.md#unsubscribe-header) erfahren Sie mehr über die Verwaltung von Abmeldefunktionen innerhalb Ihrer Nachrichten.

In [!DNL Journey Optimizer] wird das Einverständnis durch das [Einverständnisschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=de){target="_blank"} von Experience Platform verarbeitet. Standardmäßig ist der Wert für das Einverständnisfeld leer und gilt als Einverständnis für den Empfang Ihrer Nachrichten. Sie können diesen Standardwert beim Onboarding in einen der möglichen Werte ([) ](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=de#choice-values){target="_blank"} oder verwenden [Einverständnisrichtlinien](../action/consent.md) um die Standardlogik zu überschreiben.

Derzeit hängt [!DNL Journey Optimizer] kein bestimmtes Tag an Abmeldeereignisse an, die durch die Abmeldefunktion für Listen ausgelöst werden. Wenn Sie Klicks zum Abmelden von einer Liste von anderen Abmeldeaktionen unterscheiden müssen, müssen Sie das benutzerdefinierte Tagging extern implementieren oder eine externe Landingpage für das Tracking nutzen.

## Externes Verwalten von Abmeldedaten {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Definieren, wie Abmeldedaten verwaltet werden"
>abstract="**Von Adobe verwaltet**: Einverständnisdaten werden von Ihnen innerhalb des Adobe-Systems verwaltet.<br>**Kundenseitig verwaltet**: Einverständnisdaten werden von Ihnen in einem externen System verwaltet. Im Adobe-System erfolgt keine Aktualisierung der Synchronisierung von Einverständnisdaten, sofern dies nicht von Ihnen initiiert wird."

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom_url"
>title="Eingeben der eigenen URL zum Abmelden mit einem Klick"
>abstract="Die **URL zum Abmelden mit einem Klick** muss die POST-Anfragemethode verwenden."

Wählen Sie im Falle einer Einverständnisverwaltung außerhalb von Adobe die Option **[!UICONTROL Kundenseitig verwaltet]** aus, um eine benutzerdefinierte Abmelde-E-Mail-Adresse und Ihre eigene URL zum Abmelden mit einem Klick einzugeben.

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

Die **[!UICONTROL Ein-Klick-Abmelde-URL]** muss eine POST-URL sein.

>[!WARNING]
>
>Wenn Sie die Option **[!UICONTROL Kundenseitig verwaltet]** verwenden, speichert Adobe weder Abmelde- noch Einverständnisdaten. Mit der Option **[!UICONTROL Kundenseitig verwaltet]** entscheiden sich Organisationen für die Verwendung eines externen Systems und sind für die Verwaltung ihrer Einverständnisdaten in diesem externen System verantwortlich. Es erfolgt keine automatische Synchronisierung von Einverständnisdaten zwischen dem externen System und [!DNL Journey Optimizer]. Jede Synchronisierung von Einverständnisdaten, die zur Aktualisierung von Benutzereinverständnisdaten in [!DNL Journey Optimizer] aus dem externen System herangezogen werden, muss von der Organisation als Datenübertragung initiiert werden, um die Einverständnisdaten wieder in [!DNL Journey Optimizer] zu übertragen.

### Konfigurieren der Entschlüsselungs-API {#configure-decrypt-api}

Wenn Sie bei ausgewählter Option **[!UICONTROL Vom Kunden verwaltet]** benutzerdefinierte Endpunkte eingeben und in einer Kampagne oder auf einer Journey verwenden, fügt [!DNL Journey Optimizer] einige standardmäßige profilspezifische Parameter an das Einverständnisaktualisierungsereignis an (<!--sent to the custom endpoint --> Ihre Empfänger auf den Abmelde-Link klicken).

Diese Parameter werden verschlüsselt an den Endpunkt gesendet. Daher muss das externe Einverständnissystem eine bestimmte API über [Adobe Developer](https://developer.adobe.com){target="_blank"} implementieren, um die von Adobe gesendeten Parameter zu entschlüsseln.

Der GET-Aufruf zum Abrufen dieser Parameter hängt von der von Ihnen verwendeten Option zum Abmelden von der Liste ab: **[!UICONTROL URL zum Abmelden mit einem Klick]** oder **[!UICONTROL E-Mail an (abmelden)]**.

<!--To configure the API to send back the information to [!DNL Adobe Journey Optimizer] when a recipient has unsubscribed using the List unsubscribe option with custom endpoints, follow the steps below.-->

+++ URL zum Abmelden mit einem Klick

Mit der Option **[!UICONTROL URL zum Abmelden mit einem Klick]** werden Benutzende durch Klicken auf den Abmelde-Link direkt abgemeldet.

Dieser GET-Aufruf sieht wie folgt aus:

Endpunkt: https://platform.adobe.io/journey/imp/consent/decrypt

Abfrageparameter:

* **params**: enthält die verschlüsselte Payload
* **pid**: verschlüsselte Profil-ID

Diese beiden Parameter werden in das Ereignis zur Einverständnisaktualisierung aufgenommen, das an die benutzerdefinierten Endpunkte gesendet wird.

Header-Anforderungen:

* x-api-key
* x-gw-ims-org-id
* Autorisierung (Benutzer-Token Ihres technischen Kontos)

Im Folgenden finden Sie Beispielparameter und die Einverständnisantwort:

| Abfrageparameter | Beispiel-Payload |
|---------|----------|
| PID | {<br>„pid“ : „5142733041546020095851529937068211571“,<br>„pns“ : „CRMID“,<br>„e“    : &quot;john@google.com&quot;,<br>„ens“ : „email“,<br>} |
| Parameter | {<br>„m“ : „messageExecutionId“,<br>„ci“ : „campaignId“,<br>„jv“ : „journeyVersionId“,<br>„ja“ : „journeyActionId“,<br>„s“ : „sandboxId“,<br>„us“ : „unsubscribeScope“<br>} |

Einverständnisantwort:

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
}
```

+++

+++ E-Mail an (abmelden)

Mit der Option **[!UICONTROL E-Mail an (abmelden)]** wird durch Klicken auf den Abmelde-Link eine vorausgefüllte E-Mail an die angegebene Abmelde-Adresse gesendet.

Dieser GET-Aufruf sieht wie folgt aus:

Endpunkt: https://platform.adobe.io/journey/imp/consent/decrypt

Abfrageparameter:

* **emailParams**: String, der die Parameter **params** (verschlüsselte Payload) und **pid** (verschlüsselte Profilkennung) enthält.

Die Parameter **params** und **pid** werden in das Ereignis zur Einverständnisaktualisierung aufgenommen, das an die benutzerdefinierten Endpunkte gesendet wird.

Header-Anforderungen:

* x-api-key
* x-gw-ims-org-id
* Autorisierung (Benutzer-Token Ihres technischen Kontos)

Im Folgenden finden Sie Beispielparameter und die Einverständnisantwort:

| Abfrageparameter | Beispiel-Payload |
|---------|----------|
| emailParams | {<br>„p“ : „profileId“,<br>„pn“ : „profileNamespace“,<br>„en“ : „emailNamespace“,<br>„ci“ : „campaignId“,<br>„jv“ : „journeyVersionId“,<br>„ja“ : „journeyActionId“,<br>„si“ : „sandboxId“,<br>„us“: „unsubscribeScope“<br>} |

Einverständnisantwort:

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
}
```

+++
