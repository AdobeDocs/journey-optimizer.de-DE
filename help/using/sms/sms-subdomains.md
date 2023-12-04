---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von Subdomains für Textnachrichten (SMS/MMS)
description: Erfahren Sie, wie Sie mit Journey Optimizer SMS-Subdomains konfigurieren
role: Admin
feature: SMS, Channel Configuration
level: Intermediate
keywords: SMS, Subdomains, Konfiguration
exl-id: 08a546d1-060c-43e8-9eac-4c38945cc3e1
source-git-commit: 227cdb77b0db40c59fa089789c444c2364fd062e
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 72%

---

# Konfigurieren von SMS-Subdomains {#sms-mms-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="SMS/MMS-Subdomain delegieren"
>abstract="Richten Sie Ihre Subdomain für SMS/MMS ein. Sie können eine Subdomain verwenden, die bereits an Adobe delegiert wurde, oder eine neue Subdomain konfigurieren."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="SMS/MMS-Subdomain delegieren"
>abstract="Sie müssen eine Subdomain für Ihre Textnachrichten konfigurieren, da diese Subdomain zum Erstellen einer SMS-Oberfläche erforderlich ist. Sie können eine bereits an Adobe delegierte Subdomain verwenden oder eine neue Subdomain konfigurieren."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=de#message-preset-sms" text="Erstellen von SMS-Oberflächen"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="SMS/MMS-Subdomain auswählen"
>abstract="Um eine SMS-Oberfläche erstellen zu können, müssen Sie zuvor mindestens eine SMS-Subdomain konfiguriert haben, die aus der Liste der Subdomain-Namen ausgewählt werden kann."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=de#message-preset-sms" text="Erstellen von SMS-Oberflächen"

Um die URLs zu Ihren SMS-/MMS-Nachrichten verkürzen zu können, müssen Sie die Subdomain einrichten, die Sie beim [SMS-Oberfläche erstellen](sms-configuration.md#message-preset-sms).

Sie können eine Subdomain verwenden, die bereits an Adobe delegiert wurde, oder eine andere Subdomain konfigurieren. Weitere Informationen zum Delegieren von Subdomains an Adobe finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>* Die Konfiguration von SMS-Subdomains wird in allen Umgebungen verwendet. Daher wirkt sich jede Änderung an einer SMS-Subdomain auch auf andere Produktions-Sandboxes aus.
>
>* Zum Zugreifen auf und Bearbeiten von SMS-Subdomains benötigen Sie die **[!UICONTROL Verwalten von SMS-Subdomains]** -Berechtigung für die Produktions-Sandbox. Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/high-low-permissions.md).
>

## Verwenden einer vorhandenen Subdomain {#sms-use-existing-subdomain}

Gehen Sie wie folgt vor, um eine Subdomain zu verwenden, die bereits an Adobe delegiert wurde.

1. Navigieren Sie zum **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** und wählen Sie **[!UICONTROL SMS-Konfiguration]** > **[!UICONTROL SMS-Subdomains]**.

   ![](assets/sms_access-subdomains.png)

1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.

   ![](assets/sms_set-up-subdomain.png)

1. Wählen Sie **[!UICONTROL Delegierte Subdomain verwenden]** im Abschnitt **[!UICONTROL Konfigurationstyp]** aus.

   ![](assets/sms_use-delegated-subdomain.png)

1. Geben Sie das Präfix ein, das in Ihrer SMS-URL angezeigt werden soll.

   >[!NOTE]
   >
   >Nur alphanumerische Zeichen und Bindestriche sind zulässig.

1. Wählen Sie aus der Liste eine delegierte Subdomain aus.

   >[!NOTE]
   >
   >Sie können keine Subdomain auswählen, die bereits als SMS-Subdomain verwendet wird.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >Wenn Sie eine Domain auswählen, die mit der [CNAME-Methode](../configuration/delegate-subdomain.md#cname-subdomain-delegation) an Adobe delegiert wurde, müssen Sie den DNS-Eintrag auf Ihrer Hosting-Plattform erstellen. Um den DNS-Eintrag zu generieren, gehen Sie genauso vor wie bei der Konfiguration einer neuen SMS-Subdomain. Weitere Informationen dazu finden Sie in [diesem Abschnitt](#sms-configure-new-subdomain).

1. Klicken Sie auf **[!UICONTROL Senden]**.

1. Nach der Übermittlung wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was bis zu 4 Stunden dauern kann.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Subdomain den Status **[!UICONTROL Erfolg]**. Er kann zur Erstellung von Oberflächen für SMS-Kanäle verwendet werden.

## Konfigurieren einer neuen Subdomain {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="Erstellen des passenden DNS-Eintrags"
>abstract="Um eine neue SMS-Subdomain zu konfigurieren, müssen Sie die auf der Journey Optimizer-Benutzeroberfläche angezeigten Adobe-Nameserver-Informationen kopieren und in Ihre Domain-Hosting-Lösung einfügen, um den passenden DNS-Eintrag zu generieren. Nachdem die Prüfungen erfolgreich waren, kann die Subdomain zur Erstellung von SMS-Oberflächen verwendet werden."

Gehen Sie wie folgt vor, um eine neue Subdomain zu konfigurieren.

1. Navigieren Sie zum **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** Menü und wählen Sie **[!UICONTROL SMS-Konfiguration]** > **[!UICONTROL SMS-Subdomains]**.

1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.

1. Wählen Sie **[!UICONTROL Eigene Domain hinzufügen]** im Abschnitt **[!UICONTROL Konfigurationstyp]**.

   ![](assets/sms_add-your-own-subdomain.png)

1. Geben Sie die zu delegierende Subdomain an.

   >[!CAUTION]
   >
   >* Sie können keine bereits vorhandene SMS-Subdomain verwenden.
   >
   >* Großbuchstaben sind in Subdomains nicht zulässig.

   Es ist nicht zulässig, Adobe eine ungültige Subdomain zuzuweisen. Vergewissern Sie sich, dass Sie eine gültige Subdomain eingeben, die Ihrem Unternehmen gehört, z. B. marketing.ihrunternehmen.com.

   >[!NOTE]
   >
   >Es werden Subdomains mit mehreren Ebenen (derselben übergeordneten Domain) unterstützt. Sie können beispielsweise „sms.marketing.meinefirma.com“ verwenden.

1. Die Liste der Einträge, die auf Ihren DNS-Servern gespeichert werden sollen, wird angezeigt. Kopieren Sie diesen Datensatz oder laden Sie eine CSV-Datei herunter und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um den entsprechenden DNS-Eintrag zu generieren.

1. Stellen Sie sicher, dass in Ihrer Domain-Hosting-Lösung ein DNS-Eintrag generiert wurde. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie die Checkbox „Ich bestätige...“ und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Wenn Sie eine neue SMS-Subdomain konfigurieren, verweist sie immer auf einen CNAME-Eintrag.

1. Nachdem die Subdomain-Zuweisung übermittelt wurde, wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

Bevor Sie eine Subdomain zum Versand von SMS-Nachrichten verwenden, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchführt, was bis zu 4 Stunden dauern kann.<!--Learn more in [this section](#subdomain-validation).--> Sobald die Prüfungen erfolgreich waren, erhält die Subdomain die **[!UICONTROL Erfolg]** -Status. Er kann zur Erstellung von Oberflächen für SMS-Kanäle verwendet werden.

Beachten Sie, dass die Subdomain als **[!UICONTROL Fehlgeschlagen]** markiert wird, wenn Sie den Validierungseintrag in Ihrer Hosting-Lösung nicht erstellen können.
