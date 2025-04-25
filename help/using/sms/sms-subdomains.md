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
source-git-commit: 19f127c2abc81239abda8ebd38bdcacee796a1b0
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 70%

---

# Konfigurieren von SMS-Subdomains {#sms-mms-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="Delegieren einer SMS/MMS-Subdomain"
>abstract="Richten Sie Ihre Subdomain für Textnachrichten (SMS/MMS) ein. Es kann eine Subdomain verwendet werden, die bereits an Adobe delegiert ist, oder eine neue Subdomain konfiguriert werden."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="Delegieren einer SMS/MMS-Subdomain"
>abstract="Sie müssen eine Subdomain einrichten, die für Ihre Textnachrichten verwendet wird, da diese Subdomain für die Erstellung einer SMS-Konfiguration benötigt wird. Sie können eine bereits an Adobe delegierte Subdomain verwenden oder eine neue Subdomain konfigurieren."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Erstellen einer SMS-Konfiguration"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="Auswählen einer SMS/MMS-Subdomain"
>abstract="Um eine SMS-Konfiguration erstellen zu können, müssen Sie zuvor mindestens eine SMS-Subdomain konfiguriert haben, die aus der Liste der Subdomain-Namen ausgewählt werden kann."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Erstellen einer SMS-Konfiguration"

## Erste Schritte mit SMS-Subdomains {#gs-sms-mms-subdomains}

Um die URLs zu Ihren SMS-/MMS-Nachrichten kürzen zu können, müssen Sie die Subdomain einrichten, die Sie auswählen, wenn Sie [eine SMS-Konfiguration erstellen](sms-configuration.md#message-preset-sms).

Sie können entweder eine Subdomain verwenden, die bereits an Adobe delegiert ist, oder eine andere Subdomain konfigurieren. Weitere Informationen zum Delegieren von Subdomains an Adobe finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md).

Die Konfiguration von SMS-Subdomains wird **von allen Umgebungen gemeinsam genutzt**. Daher wirkt sich jede Änderung an einer SMS-Subdomain auch auf die Produktions-Sandboxes aus.

Um auf SMS-Subdomains zuzugreifen und sie zu bearbeiten, benötigen Sie die Berechtigung zum **[!UICONTROL Verwalten von SMS-Subdomains]** für die Produktions-Sandbox. Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/high-low-permissions.md).

## Verwenden einer vorhandenen Subdomain {#sms-use-existing-subdomain}

Gehen Sie wie folgt vor, um eine Subdomain zu verwenden, die bereits an Adobe delegiert wurde.

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** auf und wählen Sie **[!UICONTROL SMS-Einstellungen]** > **[!UICONTROL SMS-Subdomains]** aus.

1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.

   ![](assets/sms_set-up-subdomain.png)

1. Wählen Sie **[!UICONTROL Delegierte Subdomain verwenden]** im Abschnitt **[!UICONTROL Konfigurationstyp]** aus.

   ![](assets/sms_use-delegated-subdomain.png)

1. Geben Sie das Präfix ein, das in Ihrer SMS-URL angezeigt werden soll.

   Nur alphanumerische Zeichen und Bindestriche sind zulässig.

1. Wählen Sie aus der Liste eine delegierte Subdomain aus.

   Sie können keine Subdomain auswählen, die bereits als SMS-Subdomain verwendet wird.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >Wenn Sie eine Domain auswählen, die mit der [CNAME-Methode](../configuration/delegate-subdomain.md#cname-subdomain-delegation) an Adobe delegiert wurde, müssen Sie den DNS-Eintrag auf Ihrer Hosting-Plattform erstellen. Um den DNS-Eintrag zu generieren, gehen Sie genauso vor wie bei der Konfiguration einer neuen SMS-Subdomain. Weitere Informationen dazu finden Sie in [diesem Abschnitt](#sms-configure-new-subdomain).

1. Klicken Sie auf **[!UICONTROL Senden]**.

1. Nach der Übermittlung wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was **bis zu 4 Stunden**.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Subdomain den Status **[!UICONTROL Erfolg]**. Sie kann zur Erstellung von Kanälen für SMS-Konfigurationen verwendet werden.

## Konfigurieren einer neuen Subdomain {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="Erstellen des passenden DNS-Eintrags"
>abstract="Um eine neue SMS-Subdomain zu konfigurieren, müssen Sie die auf der Journey Optimizer-Benutzeroberfläche angezeigten Adobe-Nameserver-Informationen kopieren und in Ihre Domain-Hosting-Lösung einfügen, um den passenden DNS-Eintrag zu generieren. Nachdem die Prüfungen erfolgreich waren, kann die Subdomain zur Erstellung von SMS-Konfigurationen verwendet werden."

Gehen Sie wie folgt vor, um eine neue Subdomain zu konfigurieren.

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** auf und wählen Sie dann **[!UICONTROL SMS-Einstellungen]** > **[!UICONTROL SMS-Subdomains]**.

1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.

   ![](assets/sms_set-up-subdomain.png)

1. Wählen Sie **[!UICONTROL Eigene Domain hinzufügen]** im Abschnitt **[!UICONTROL Konfigurationstyp]**.

   ![](assets/sms_add-your-own-subdomain.png)

1. Geben Sie die zu delegierende Subdomain an.

   >[!CAUTION]
   >
   >* Sie können keine bereits vorhandene SMS-Subdomain verwenden.
   >
   >* Großbuchstaben sind in Subdomains nicht zulässig.

   Es ist nicht zulässig, Adobe eine ungültige Subdomain zuzuweisen. Vergewissern Sie sich, dass Sie eine gültige Subdomain eingeben, die Ihrem Unternehmen gehört, z. B. marketing.ihrunternehmen.com.

   Es werden Subdomains mit mehreren Ebenen (derselben übergeordneten Domain) unterstützt. Sie können beispielsweise „sms.marketing.meinefirma.com“ verwenden.

1. Die Liste der Einträge, die auf Ihren DNS-Servern gespeichert werden sollen, wird angezeigt. Kopieren Sie diesen Datensatz oder laden Sie eine CSV-Datei herunter und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um den entsprechenden DNS-Eintrag zu generieren.

1. Stellen Sie sicher, dass in Ihrer Domain-Hosting-Lösung ein DNS-Eintrag generiert wurde. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie die Checkbox „Ich bestätige...“ und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   Wenn Sie eine neue SMS-Subdomain konfigurieren, verweist sie immer auf einen CNAME-Eintrag.

1. Nachdem die Subdomain-Zuweisung übermittelt wurde, wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

Bevor Sie diese Subdomain zum Senden von SMS-Nachrichten verwenden, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was bis zu 4 Stunden dauern kann.<!--Learn more in [this section](#subdomain-validation).--> Sobald die Prüfungen erfolgreich abgeschlossen wurden, erhält die Subdomain den Status **[!UICONTROL Erfolgreich]**. Sie kann zur Erstellung von Kanälen für SMS-Konfigurationen verwendet werden.

Beachten Sie, dass die Subdomain als **[!UICONTROL Fehlgeschlagen]** markiert wird, wenn Sie den Validierungseintrag in Ihrer Hosting-Lösung nicht erstellen können.

## Delegierung einer Subdomain aufheben {#undelegate-subdomain}

Wenn Sie die Delegierung einer SMS-Subdomain aufheben möchten, wenden Sie sich an den Adobe-Support.

Sie müssen jedoch mehrere Schritte in der Benutzeroberfläche ausführen, bevor Sie sich an Adobe wenden.

>[!NOTE]
>
>Die Delegierung von Subdomains kann nur mit dem Status **[!UICONTROL Erfolg]** aufgehoben werden. Subdomains mit dem Status **[!UICONTROL Entwurf]** und **[!UICONTROL Fehlgeschlagen]** können einfach aus der Benutzeroberfläche gelöscht werden.

Führen Sie zunächst die folgenden Schritte in [!DNL Journey Optimizer] aus:

1. Deaktivieren Sie alle Kanalkonfigurationen, die mit der Subdomain verknüpft sind. [Weitere Informationen](../configuration/channel-surfaces.md#deactivate-a-surface)

<!--
1. If the SMS subdomain is using an email subdomain that was [already delegated](#lp-use-existing-subdomain) to Adobe, undelegate the email subdomain. [Learn how](../configuration/delegate-subdomain.md#undelegate-subdomain)-->

1. Beenden Sie die aktiven Kampagnen, die mit den Subdomains verknüpft sind. [Weitere Informationen](../campaigns/modify-stop-campaign.md#stop)

1. Beenden Sie die aktiven Journey, die mit den Subdomains verknüpft sind. [Weitere Informationen](../building-journeys/end-journey.md#stop-journey)

1. Wenn die SMS-Subdomain eine [neue delegierte Subdomain](#sms-configure-new-subdomain) war, entfernen Sie die mit dieser Subdomain verknüpften DNS-Einträge.

Wenden Sie sich anschließend mit der Subdomain, deren Delegierung Sie aufheben möchten, an den Adobe-Support.

Nachdem Ihre Anfrage von Adobe verarbeitet wurde, wird die nicht delegierte Domain nicht mehr auf der Subdomain-Inventarseite angezeigt.

>[!CAUTION]
>
>Nachdem die Delegierung einer Subdomain aufgehoben wurde:
>
>   * Die Kanalkonfigurationen, die diese Subdomain verwendet haben, können nicht reaktiviert werden.
>   * Die exakte Subdomain kann nicht erneut über die Benutzeroberfläche delegiert werden. Wenden Sie sich in diesem Fall an Ihren Adobe-Support-Mitarbeiter.
