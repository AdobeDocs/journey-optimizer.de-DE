---
solution: Journey Optimizer
product: journey optimizer
title: Landingpage-Subdomains konfigurieren
description: Erfahren Sie, wie Sie mit Journey Optimizer Subdomains von Landingpages konfigurieren
role: Admin
level: Intermediate
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Landingpage-Subdomains konfigurieren {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="Zuweisen einer Subdomain für die Landingpage"
>abstract="Sie richten Ihre Subdomain für die Verwendung einer Landingpage ein. Sie können eine bereits Adobe zugewiesene Subdomain verwenden oder eine andere Subdomain konfigurieren."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="Zuweisen einer Subdomain für die Landingpage"
>abstract="Sie müssen eine Subdomain für Ihre Landingpages konfigurieren, da diese Subdomain zum Erstellen einer Landingpage-Vorgabe erforderlich ist. Sie können eine bereits Adobe zugewiesene Subdomain verwenden oder eine neue Subdomain konfigurieren."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="Landingpage-Vorgaben erstellen"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Landingpage-Vorgabe erstellen"
>abstract="Um eine Landingpage-Vorgabe erstellen zu können, müssen Sie zuvor mindestens eine Landingpage-Subdomain konfiguriert haben, die aus der Liste &quot;Subdomain-Name&quot;ausgewählt werden soll."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="Landingpage-Vorgaben erstellen"

Um [Landingpage-Vorgaben erstellen](lp-presets.md)müssen Sie die Subdomains einrichten, die Sie für Ihre Landingpages verwenden.

Sie können eine bereits Adobe zugewiesene Subdomain verwenden oder eine andere Subdomain konfigurieren. Erfahren Sie mehr über die Zuweisung von Subdomains an Adobe in [diesem Abschnitt](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>Die Konfiguration der Subdomain für Landingpages ist in allen Umgebungen üblich. Daher wirkt sich jede Änderung an einer Unterdomäne der Landingpage auch auf die Produktions-Sandboxes aus.

Beachten Sie, dass Großbuchstaben in einer Subdomain nicht zulässig sein sollten

## Vorhandene Subdomain verwenden {#lp-use-existing-subdomain}

Gehen Sie wie folgt vor, um eine bereits Adobe zugewiesene Subdomain zu verwenden.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Channels]** Menü und wählen Sie **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

   ![](assets/lp_access-subdomains.png)

1. Klicken **[!UICONTROL Set up subdomain]**.

   ![](assets/lp_set-up-subdomain.png)

1. Auswählen **[!UICONTROL Use delegated domain]** von **[!UICONTROL Configuration type]** Abschnitt.

   ![](assets/lp_use-delegated-subdomain.png)

1. Geben Sie das Präfix ein, das in Ihrer Landingpage-URL angezeigt werden soll.

   >[!NOTE]
   >
   >Nur alphanumerische Zeichen und Bindestriche sind zulässig.

1. Wählen Sie eine zugewiesene Subdomain aus der Liste aus.

   >[!NOTE]
   >
   >Sie können keine Subdomain auswählen, die bereits als Subdomain der Landingpage verwendet wurde.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/lp_prefix-and-subdomain.png)

   Beachten Sie, dass Sie nicht mehrere zugewiesene Subdomains derselben übergeordneten Domäne verwenden können. Wenn beispielsweise &quot;marketing1.yourcompany.com&quot;bereits für Ihre Landingpages an Adobe delegiert wurde, können Sie &quot;marketing2.yourcompany.com&quot;nicht verwenden. Da jedoch mehrstufige Subdomains für Landingpages unterstützt werden, können Sie eine Subdomain von &quot;marketing1.yourcompany.com&quot; (z. B. &quot;email.marketing1.yourcompany.com&quot;) oder eine andere übergeordnete Domäne verwenden.

   >[!CAUTION]
   >
   >Wenn Sie eine Domäne auswählen, die Adobe mithilfe der [CNAME-Methode](../configuration/delegate-subdomain.md#cname-subdomain-delegation), müssen Sie den DNS-Eintrag auf Ihrer Hosting-Plattform erstellen. Um den DNS-Eintrag zu generieren, läuft der Prozess genauso ab wie bei der Konfiguration einer neuen Landingpage-Subdomain. Erfahren Sie mehr über [diesem Abschnitt](#lp-configure-new-subdomain).

1. Klicken **[!UICONTROL Submit]**.

1. Nach der Übermittlung wird die Subdomain in der Liste mit der **[!UICONTROL Processing]** Status. Weitere Informationen zum Status von Subdomains finden Sie unter [diesem Abschnitt](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchführt, die bis zu 4 Stunden dauern können.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Sobald die Prüfungen erfolgreich waren, erhält die Subdomain die **[!UICONTROL Success]** Status. Sie können damit Landingpage-Vorgaben erstellen.

## Neue Subdomain konfigurieren {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="Den entsprechenden DNS-Eintrag generieren"
>abstract="Um eine neue Einstiegsseiten-Subdomain zu konfigurieren, müssen Sie die auf der Benutzeroberfläche von Journey Optimizer angezeigten Adobe-Nameserver-Informationen kopieren und in Ihre Domain-Hosting-Lösung einfügen, um den entsprechenden DNS-Eintrag zu generieren. Nach erfolgreicher Überprüfung kann die Subdomain zur Erstellung von Landingpage-Vorgaben verwendet werden."

Gehen Sie wie folgt vor, um eine neue Subdomain zu konfigurieren.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Channels]** Menü und wählen Sie **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

1. Klicken **[!UICONTROL Set up subdomain]**.

1. Auswählen **[!UICONTROL Add your own domain]** von **[!UICONTROL Configuration type]** Abschnitt.

   ![](assets/lp_add-your-own-subdomain.png)

1. Geben Sie die zu delegierende Subdomäne an.

   >[!CAUTION]
   >
   >Sie können keine vorhandene Subdomain der Landingpage verwenden.
   >
   >Großbuchstaben sind in Subdomänen nicht zulässig.

   Die Zuweisung einer ungültigen Subdomain zu Adobe ist nicht zulässig. Vergewissern Sie sich, dass Sie eine gültige Subdomain eingeben, die Ihrem Unternehmen gehört, z. B. marketing.yourcompany.com.

   >[!NOTE]
   >
   >Bei Landingpages werden mehrstufige Subdomains unterstützt. Sie können beispielsweise &quot;email.marketing.yourcompany.com&quot;verwenden.

1. Der Datensatz, der auf Ihren DNS-Servern platziert werden soll, wird angezeigt. Kopieren Sie diesen Datensatz oder laden Sie eine CSV-Datei herunter und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um den entsprechenden DNS-Eintrag zu generieren.

1. Stellen Sie sicher, dass in Ihrer Domain-Hosting-Lösung ein DNS-Eintrag generiert wurde. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie das Kontrollkästchen &quot;Ich bestätigen..&quot; und klicken Sie dann auf . **[!UICONTROL Submit]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Wenn Sie eine neue Subdomain für die Landingpage konfigurieren, verweist sie immer auf einen CNAME-Eintrag.

1. Sobald die Subdomain-Zuweisung gesendet wurde, wird die Subdomain in der Liste mit der **[!UICONTROL Processing]** Status. Weitere Informationen zum Status von Subdomains finden Sie unter [diesem Abschnitt](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchführt, die bis zu 4 Stunden dauern können.<!--Learn more in [this section](#subdomain-validation).-->

1. Sobald die Prüfungen erfolgreich waren, erhält die Subdomain die **[!UICONTROL Success]** Status. Sie können damit Landingpage-Vorgaben erstellen.

   Beachten Sie, dass die Subdomain als **[!UICONTROL Failed]** , wenn Sie den Validierungsdatensatz nicht in Ihrer Hosting-Lösung erstellen.
