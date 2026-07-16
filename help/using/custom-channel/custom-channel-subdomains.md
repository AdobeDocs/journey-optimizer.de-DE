---
title: Konfigurieren von Subdomains für benutzerdefinierte Kanäle
description: Erfahren Sie, wie Sie mit Journey Optimizer benutzerdefinierte Kanal-Subdomains konfigurieren
role: Admin
feature: Channel Configuration
level: Intermediate
keywords: Benutzerdefinierter Kanal, Subdomains, Konfiguration
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 42%

---

# Konfigurieren von benutzerdefinierten Kanal-Subdomains {#custom-channel-subdomains}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie in Adobe Journey Optimizer benutzerdefinierte Kanal-Subdomains einrichten, um das Linktracking in Ihren Nachrichten zu aktivieren, entweder durch Verwendung einer bestehenden delegierten Subdomain oder durch Konfiguration einer neuen Subdomain mit einem DNS-Eintrag.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom_channel"
>title="Delegieren einer benutzerdefinierten Kanal-Subdomain"
>abstract="Sie müssen eine Subdomain konfigurieren, die für Ihre benutzerdefinierten Kanalnachrichten verwendet werden soll, da diese Subdomain für die Erstellung einer benutzerdefinierten Kanalkonfiguration benötigt wird. Sie können eine bereits an Adobe delegierte Subdomain verwenden oder eine neue Subdomain konfigurieren."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/custom-channel/custom-channel-configuration" text="Konfigurieren eines benutzerdefinierten Kanals"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_custom_channel_subdomain"
>title="Benutzerdefinierte Kanal-Subdomain auswählen"
>abstract="Um eine benutzerdefinierte Kanalkonfiguration erstellen zu können, müssen Sie zuvor mindestens eine benutzerdefinierte Kanal-Subdomain konfiguriert haben, die aus der Liste der Subdomain-Namen ausgewählt werden kann."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/custom-channel/custom-channel-configuration" text="Konfigurieren eines benutzerdefinierten Kanals"

## Erste Schritte mit benutzerdefinierten Kanal-Subdomains {#gs-custom-channel-subdomains}

Um das Linktracking in Ihren benutzerdefinierten Kanalnachrichten zu aktivieren, müssen Sie die Subdomain einrichten, die Sie beim Erstellen [&#x200B; benutzerdefinierten Kanalkonfiguration auswählen](custom-channel-configuration.md#subdomain-delegation).

Sie können entweder eine Subdomain verwenden, die bereits an Adobe delegiert ist, oder eine andere Subdomain konfigurieren. Weitere Informationen zum Delegieren von Subdomains an Adobe finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md).

Die Konfiguration der benutzerdefinierten Kanal-Subdomain wird von allen Umgebungen gemeinsam genutzt. Daher wirkt sich jede Änderung an einer benutzerdefinierten Kanal-Subdomain auch auf andere Produktions-Sandboxes aus.

<!--
TBC
>[!NOTE]
>
>To access and edit custom channel subdomains, you must have the **[!UICONTROL Manage Custom Channel Subdomains]** permission on the production sandbox. Learn more about permissions in [this section](../administration/high-low-permissions.md).
-->

## Verwenden einer vorhandenen Subdomain {#custom-channel-use-existing-subdomain}

Gehen Sie wie folgt vor, um eine Subdomain zu verwenden, die bereits an Adobe delegiert wurde.

1. Navigieren Sie zum Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** und wählen Sie **[!UICONTROL Kanalgenerator]** > **[!UICONTROL Subdomains]**.

   ![](assets/custom_channel_subdomains.png){width="100%"}

1. Klicken Sie **[!UICONTROL Benutzerdefinierte Kanal-Subdomain erstellen]**.

1. Wählen Sie **[!UICONTROL Delegierte Subdomain verwenden]** im Abschnitt **[!UICONTROL Konfigurationstyp]** aus.

   ![](assets/custom_channel_create_subdomain.png){width="100%"}

1. Geben Sie das Präfix ein, das in Ihrer benutzerdefinierten Kanal-URL angezeigt wird. Nur alphanumerische Zeichen und Bindestriche sind zulässig.

   Das Präfix wird verwendet, um eine eindeutige Subdomain für diesen benutzerdefinierten Kanal zu erstellen. Wenn Sie beispielsweise `promo` eingeben und die Subdomain-`luma.com` auswählen, wird die resultierende Subdomain `promo.luma.com`.

   >[!CAUTION]
   >
   >Verwenden Sie die Präfixe `cdn` und `data` nicht, da diese für die interne Verwendung reserviert sind. Andere eingeschränkte oder reservierte Präfixe wie `dmarc` oder `spf` sollten ebenfalls vermieden werden.

1. Wählen Sie aus der Liste eine delegierte Subdomain aus.

   Es kann keine Subdomain ausgewählt werden, die bereits als benutzerdefinierte Kanal-Subdomain verwendet wird.

   >[!CAUTION]
   >
   >Wenn Sie eine Domain auswählen, die mit der [CNAME-Methode](../configuration/delegate-subdomain.md#cname-subdomain-setup) an Adobe delegiert wurde, müssen Sie den DNS-Eintrag auf Ihrer Hosting-Plattform erstellen. Um den DNS-Eintrag zu generieren, gehen Sie genauso vor wie bei der Konfiguration einer neuen benutzerdefinierten Kanal-Subdomain. Mehr dazu erfahren Sie in [diesem Abschnitt](#custom-channel-configure-new-subdomain).

1. Klicken Sie auf **[!UICONTROL Senden]**.

1. Nach der Übermittlung wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md#access-delegated-subdomains).

   Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was **bis zu 4 Stunden)** kann.

1. Sobald die Prüfungen erfolgreich abgeschlossen wurden, erhält die Subdomain den Status **[!UICONTROL Erfolgreich]**. Sie kann jetzt zum Erstellen benutzerdefinierter Kanalkonfigurationen verwendet werden.

## Konfigurieren einer neuen Subdomain {#custom-channel-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_custom_channel_subdomain_dns"
>title="Erstellen des passenden DNS-Eintrags"
>abstract="Um eine neue benutzerdefinierte Kanal-Subdomain zu konfigurieren, müssen Sie die auf der Journey Optimizer-Benutzeroberfläche angezeigten Adobe-Nameserver-Informationen kopieren und in Ihre Domain-Hosting-Lösung einfügen, um den entsprechenden DNS-Eintrag zu generieren. Sobald die Prüfungen erfolgreich abgeschlossen sind, kann die Subdomain zur Erstellung benutzerdefinierter Kanalkonfigurationen verwendet werden."

Gehen Sie wie folgt vor, um eine neue Subdomain zu konfigurieren.

1. Navigieren Sie zum Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** und wählen Sie dann **[!UICONTROL Kanalgenerator]** > **[!UICONTROL Subdomains]**.

1. Klicken Sie **[!UICONTROL Benutzerdefinierte Kanal-Subdomain erstellen]**.

1. Wählen Sie **[!UICONTROL Eigene Domain hinzufügen]** im Abschnitt **[!UICONTROL Konfigurationstyp]**.

   ![](assets/custom_channel_new_subdomain.png){width="70%"}

1. Geben Sie die zu delegierende Subdomain an.

   >[!CAUTION]
   >
   >* Eine vorhandene benutzerdefinierte Kanal-Subdomain kann nicht verwendet werden.
   >
   >* Großbuchstaben sind in Subdomains nicht zulässig.

   Es ist nicht zulässig, Adobe eine ungültige Subdomain zuzuweisen. Vergewissern Sie sich, dass Sie eine gültige Subdomain eingeben, die Ihrem Unternehmen gehört, z. B. marketing.ihrunternehmen.com.

   Es werden Subdomains mit mehreren Ebenen (derselben übergeordneten Domain) unterstützt. Sie können beispielsweise „custom.marketing.meinefirma.com“ verwenden.

1. Die Liste der Einträge, die auf Ihren DNS-Servern gespeichert werden sollen, wird angezeigt. Kopieren Sie diesen Datensatz oder laden Sie eine CSV-Datei herunter und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um den entsprechenden DNS-Eintrag zu generieren.

1. Stellen Sie sicher, dass in Ihrer Domain-Hosting-Lösung ein DNS-Eintrag generiert wurde. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie die Checkbox „Ich bestätige...“ und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](assets/custom_channel_new_subdomain_confirm.png)

   Wenn Sie eine neue benutzerdefinierte Kanal-Subdomain konfigurieren, verweist sie immer auf einen CNAME-Eintrag.

1. Nachdem die Subdomain-Zuweisung übermittelt wurde, wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md#access-delegated-subdomains).

Bevor Sie eine Subdomain zum Senden benutzerdefinierter Kanalnachrichten verwenden, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was bis zu 4 Stunden dauern kann. Sobald die Prüfungen erfolgreich abgeschlossen wurden, erhält die Subdomain den Status **[!UICONTROL Erfolgreich]**. Sie kann jetzt zum Erstellen benutzerdefinierter Kanalkonfigurationen verwendet werden.

Beachten Sie, dass die Subdomain als **[!UICONTROL Fehlgeschlagen]** markiert wird, wenn Sie den Validierungseintrag in Ihrer Hosting-Lösung nicht erstellen können.

<!--

Any specific guardrails to add? If so, can we link to email subdomain guardrails? journey-optimizer.en/help/using/configuration/delegate-subdomain.md#guardrails

Otherwise use the following from SMS subdomains?

## Guardrails {#guardrails}

Currently, the [!DNL Journey Optimizer] user interface does not support the deletion or undelegation of custom channel subdomains once they have been set up.

However, when testing features within [!DNL Journey Optimizer], it may be necessary to create a custom channel subdomain. Once the testing is complete, this can lead to cluttered environments with unnecessary configurations as the UI does not allow for removing or undelegating custom channel subdomains.

Here are some recommended steps and considerations:

* As a best practice, maintain a tidy environment by only creating necessary components and configurations.
* In situations where there is a business impact, contact your Adobe representative who may be able to assist with the removal/undelegation of the custom channel subdomain. [Learn more](#undelegate-subdomain)
* If further assistance is required, reach out to Adobe for guidance on managing your instance effectively.

## Undelegate a subdomain {#undelegate-subdomain}

If you wish to undelegate a custom channel subdomain, reach out to your Adobe representative with the subdomain you want to undelegate.

If the custom channel subdomain points to a CNAME record, you can delete the CNAME DNS record that you created for the custom channel subdomain from your hosting solution (but do not delete the original email subdomain if any).

>[!NOTE]
>
>A custom channel subdomain can point to a CNAME record because it was either an [existing subdomain](#custom-channel-use-existing-subdomain) delegated to Adobe using the [CNAME method](../configuration/delegate-subdomain.md#cname-subdomain-setup), or a [new custom channel subdomain](#custom-channel-configure-new-subdomain) that you configured.

After your request is handled by Adobe, the undelegated domain is no longer displayed on the subdomain inventory page.
-->


## Nächste Schritte {#next-steps}

* [Erstellen Sie eine Kanalkonfiguration](custom-channel-configuration.md) um Ihren benutzerdefinierten Kanal mit einer Subdomain, Anmeldeinformationen und Payload-Standardwerten zu verknüpfen, die Marketing-Experten in Kampagnen und Journey auswählen.
