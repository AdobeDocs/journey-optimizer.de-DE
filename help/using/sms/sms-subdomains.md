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
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '1008'
ht-degree: 100%

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

Um die URLs zu Ihren SMS/MMS-Nachrichten kürzen zu können, müssen Sie die Subdomain einrichten, die Sie beim [Erstellen einer SMS-Konfiguration](sms-configuration.md#sms-prerequisites) auswählen.

Sie können entweder eine Subdomain verwenden, die bereits an Adobe delegiert ist, oder eine andere Subdomain konfigurieren. Weitere Informationen zum Delegieren von Subdomains an Adobe finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md).

Die Konfiguration von SMS-Subdomains ist **in allen Umgebungen gleich**. Daher wirkt sich jede Änderung an einer SMS-Subdomain auch auf die Produktions-Sandboxes aus.

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

   >[!CAUTION]
   >
   >Verwenden Sie die Präfixe `cdn` und `data` nicht, da diese für die interne Verwendung reserviert sind. Andere eingeschränkte oder reservierte Präfixe wie `dmarc` oder `spf` sollten ebenfalls vermieden werden.

1. Wählen Sie aus der Liste eine delegierte Subdomain aus.

   Sie können keine Subdomain auswählen, die bereits als SMS-Subdomain verwendet wird.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >Wenn Sie eine Domain auswählen, die mit der [CNAME-Methode](../configuration/delegate-subdomain.md#cname-subdomain-setup) an Adobe delegiert wurde, müssen Sie den DNS-Eintrag auf Ihrer Hosting-Plattform erstellen. Um den DNS-Eintrag zu generieren, gehen Sie genauso vor wie bei der Konfiguration einer neuen SMS-Subdomain. Weitere Informationen dazu finden Sie in [diesem Abschnitt](#sms-configure-new-subdomain).

1. Klicken Sie auf **[!UICONTROL Senden]**.

1. Nach der Übermittlung wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md#access-delegated-subdomains).<!--Same statuses?-->

   Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was **bis zu 4 Stunden** dauern kann.<!--Learn more in [this section](../configuration/delegate-subdomain.md#subdomain-validation).-->

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

1. Nachdem die Subdomain-Zuweisung übermittelt wurde, wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md#access-delegated-subdomains).<!--Same statuses?-->

Bevor Sie diese Subdomain zum Senden von SMS-Nachrichten verwenden, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was bis zu 4 Stunden dauern kann.<!--Learn more in [this section](#subdomain-validation).--> Sobald die Prüfungen erfolgreich abgeschlossen wurden, erhält die Subdomain den Status **[!UICONTROL Erfolgreich]**. Sie kann zur Erstellung von Kanälen für SMS-Konfigurationen verwendet werden.

Beachten Sie, dass die Subdomain als **[!UICONTROL Fehlgeschlagen]** markiert wird, wenn Sie den Validierungseintrag in Ihrer Hosting-Lösung nicht erstellen können.

## Leitlinien {#guardrails}

Derzeit unterstützt die Benutzeroberfläche von [!DNL Journey Optimizer] das Delegieren oder Aufheben der Delegierung von SMS-Subdomains nach der Einrichtung nicht.

Beim Testen von Funktionen in [!DNL Journey Optimizer] kann es jedoch erforderlich sein, eine SMS-Subdomain zu erstellen. Sobald die Tests abgeschlossen sind, kann dies zu überladenen Umgebungen mit unnötigen Konfigurationen führen, da die Benutzeroberfläche das Entfernen oder Aufheben der Delegierung von SMS-Subdomains nicht zulässt.

Im Folgenden finden Sie einige empfohlene Schritte und Überlegungen:

<!--As an alternative action, create a new SMS subdomain for future use cases and avoid using the existing one if it is no longer needed.-->

* Es empfiehlt sich, eine ordentliche Umgebung aufrechtzuerhalten, indem nur erforderliche Komponenten und Konfigurationen erstellt werden.
* Wenden Sie sich in Situationen, in denen es zu Geschäftsauswirkungen kommt, an Ihren Adobe-Support. Dieser kann Ihnen möglicherweise beim Entfernen/Aufheben der Delegierung der SMS-Subdomain helfen. [Weitere Informationen](#undelegate-subdomain)
* Wenn Sie weitere Unterstützung benötigen, wenden Sie sich an Adobe, um Anleitungen zur effektiven Verwaltung Ihrer Instanz zu erhalten.

## Aufheben der Delegierung einer Subdomain {#undelegate-subdomain}

Wenn Sie die Delegierung einer SMS-Subdomain aufheben möchten, wenden Sie sich an den Adobe-Support mit der Subdomain, deren Delegierung Sie aufheben möchten.

Wenn die SMS-Subdomain auf einen CNAME-Eintrag verweist, können Sie den für die SMS-Subdomain erstellten CNAME-DNS-Eintrag aus Ihrer Hosting-Lösung löschen (löschen Sie aber nicht die ursprüngliche E-Mail-Subdomain, falls vorhanden).

>[!NOTE]
>
>Eine SMS-Subdomain kann auf einen CNAME-Eintrag verweisen, da es sich entweder um eine [vorhandene Subdomain](#sms-use-existing-subdomain) handelte, die mithilfe der [CNAME-Methode](../configuration/delegate-subdomain.md#cname-subdomain-setup) an Adobe delegiert wurde, oder um eine [neue SMS-Subdomain](#sms-configure-new-subdomain), die Sie konfiguriert haben.

Nachdem Ihre Anfrage von Adobe bearbeitet wurde, wird die Domain mit der aufgehobenen Delegierung nicht mehr auf der Subdomain-Inventarseite angezeigt.
