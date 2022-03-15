---
title: Landingpage-Konfiguration
description: Erfahren Sie, wie Sie Ihre Umgebung für die Erstellung und Verwendung von Landingpages mit Journey Optimizer konfigurieren.
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: e9878246c2af5c7ee0f961aaaad64e186431d96e
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 15%

---

# Konfigurieren von Landingpages {#lp-configuration}

## Landingpage-Subdomains konfigurieren {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Landingpage-Vorgabe erstellen"
>abstract="Um eine Landingpage-Vorgabe erstellen zu können, müssen Sie zuvor mindestens eine Landingpage-Subdomain konfiguriert haben, die aus der Liste &quot;Subdomain-Name&quot;ausgewählt werden soll."

Um [Landingpage-Vorgaben erstellen](#lp-create-preset)müssen Sie nicht die Subdomains einrichten, die Sie für Ihre Landingpages verwenden.

Sie können eine Subdomain verwenden, die bereits Adobe zugewiesen ist, oder eine andere Subdomain konfigurieren. Erfahren Sie mehr über die Zuweisung von Subdomains zur Adobe in [diesem Abschnitt](delegate-subdomain.md).

### Vorhandene Subdomain verwenden {#lp-use-existing-subdomain}

Gehen Sie wie folgt vor, um eine Subdomain zu verwenden, die bereits an Adobe delegiert wurde.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** Menü und wählen Sie **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Subdomains von Landingpages]**.

   ![](assets/lp_access-subdomains.png)

1. Klicken **[!UICONTROL Einrichten der Subdomain]**.

   ![](assets/lp_set-up-subdomain.png)

1. Auswählen **[!UICONTROL Delegierte Domäne verwenden]** von **[!UICONTROL Konfigurationstyp]** Abschnitt.

   ![](assets/lp_use-delegated-subdomain.png)

1. Geben Sie das Präfix ein, das in Ihrer Landingpage-URL angezeigt werden soll.

   >[!NOTE]
   >
   >Nur alphanumerische Zeichen und Bindestriche sind zulässig.

1. Wählen Sie eine zugewiesene Subdomain aus der Liste aus.

   >[!NOTE]
   >
   >Sie können keine Subdomain auswählen, die bereits als Subdomain der Landingpage verwendet wurde.

   ![](assets/lp_prefix-and-subdomain.png)

   >[!CAUTION]
   >
   >Wenn Sie eine Domäne auswählen, die der Adobe mithilfe der [CNAME-Methode](delegate-subdomain.md#cname-subdomain-delegation), müssen Sie den DNS-Eintrag auf Ihrer Hosting-Plattform erstellen. Um den DNS-Eintrag zu generieren, läuft der Prozess genauso ab wie bei der Konfiguration einer neuen Landingpage-Subdomain. Mehr dazu erfahren Sie in [diesem Abschnitt](#lp-configure-new-subdomain).

1. Klicken Sie auf **[!UICONTROL Senden]**.

1. Nach der Übermittlung wird die Subdomain in der Liste mit der **[!UICONTROL Verarbeitung]** Status. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](access-subdomains.md).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchführt, die bis zu 4 Stunden dauern können.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Sobald die Prüfungen erfolgreich abgeschlossen wurden, erhält die Subdomain den Status **[!UICONTROL Erfolgreich]**. Sie können damit Landingpage-Vorgaben erstellen.

### Neue Subdomain konfigurieren {#lp-configure-new-subdomain}

Gehen Sie wie folgt vor, um eine neue Subdomain zu konfigurieren.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** Menü und wählen Sie **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Subdomains von Landingpages]**.

1. Klicken **[!UICONTROL Einrichten der Subdomain]**.

1. Auswählen **[!UICONTROL Eine eigene Domäne hinzufügen]** von **[!UICONTROL Konfigurationstyp]** Abschnitt.

   ![](assets/lp_add-your-own-subdomain.png)

1. Geben Sie die zu delegierende Subdomäne an.

   >[!CAUTION]
   >
   >Sie können keine vorhandene Subdomain der Landingpage verwenden.

   Es ist nicht zulässig, Adobe eine ungültige Subdomain zuzuweisen. Vergewissern Sie sich, dass Sie eine gültige Subdomain eingeben, die Ihrem Unternehmen gehört, z. B. marketing.ihrunternehmen.com.

   Mehrstufige Subdomains wie &quot;email.marketing.yourcompany.com&quot;werden derzeit nicht unterstützt.

1. Der Datensatz, der auf Ihren DNS-Servern platziert werden soll, wird angezeigt. Kopieren Sie diesen Datensatz oder laden Sie eine CSV-Datei herunter und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um den entsprechenden DNS-Eintrag zu generieren.

1. Stellen Sie sicher, dass in Ihrer Domain-Hosting-Lösung ein DNS-Eintrag generiert wurde. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie die Checkbox „Ich bestätige...“ und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Wenn Sie eine neue Subdomain für die Landingpage konfigurieren, verweist sie immer auf einen CNAME-Eintrag.

1. Nachdem die Subdomain-Zuweisung übermittelt wurde, wird die Subdomain in der Liste mit dem Status **[!UICONTROL In Verarbeitung]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](access-subdomains.md).<!--Same statuses?-->

   >[!NOTE]
   >
   >Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchführt, die bis zu 4 Stunden dauern können.<!--Learn more in [this section](#subdomain-validation).-->

1. Sobald die Prüfungen erfolgreich abgeschlossen wurden, erhält die Subdomain den Status **[!UICONTROL Erfolgreich]**. Sie können damit Landingpage-Vorgaben erstellen.

   Beachten Sie, dass die Subdomain als **[!UICONTROL Fehlgeschlagen]** , wenn Sie den Validierungsdatensatz nicht in Ihrer Hosting-Lösung erstellen.

## Landingpage-Vorgaben definieren {#lp-define-preset}

Wann [Landingpage erstellen](../landing-pages/create-lp.md#create-a-lp)müssen Sie eine Landingpage-Vorgabe auswählen, um die Landingpage erstellen und nutzen zu können. **[!DNL Journey Optimizer]**.

### Auf Landingpage-Vorgaben zugreifen {#lp-presets}

Gehen Sie wie folgt vor, um auf Landingpage-Vorgaben zuzugreifen.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** Menü.

1. Auswählen **[!UICONTROL Branding]** > **[!UICONTROL Landingpage-Vorgaben]**.

   ![](assets/lp_presets-access.png)

1. Klicken Sie auf eine beliebige vordefinierte Beschriftung, um auf die Vorgabendetails der Landingpage zuzugreifen.

   ![](assets/lp_preset-details.png)

### Landingpage-Vorgabe erstellen {#lp-create-preset}

Gehen Sie wie folgt vor, um eine Landingpage-Vorgabe zu erstellen.

>[!NOTE]
>
>Um eine Vorgabe erstellen zu können, stellen Sie sicher, dass Sie zuvor mindestens eine Subdomain der Landingpage konfiguriert haben. [Erfahren Sie mehr](#lp-subdomains)

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** Menü und wählen Sie **[!UICONTROL Branding]** > **[!UICONTROL Landingpage-Vorgaben]**.

1. Auswählen **[!UICONTROL Vorgabe für Landingpage erstellen]**.

   ![](assets/lp_create-preset-temp.png)

1. Geben Sie einen Namen und eine Beschreibung für die Vorgabe ein.

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Wählen Sie aus der Dropdown-Liste eine Landingpage-Subdomain aus.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Um eine Subdomain auswählen zu können, stellen Sie sicher, dass Sie zuvor mindestens eine Landingpage-Subdomain konfiguriert haben. [Erfahren Sie mehr](#lp-subdomains)

   Die der ausgewählten Subdomain entsprechenden Einstellungen werden angezeigt.

1. Wenn Sie die Subdomain der Landingpage als Tracking-URL auswählen möchten, überprüfen Sie die **[!UICONTROL Wie Subdomain der Landingpage]** -Option. [Erfahren Sie mehr über Tracking](../messages/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Wenn die URL der Landingpage beispielsweise &quot;pages.mail.luma.com&quot;lautet und die Tracking-URL &quot;data.mail.luma.com&quot;lautet, können Sie &quot;pages.mail.luma.com&quot;als Tracking-Subdomain auswählen.

1. Klicken **[!UICONTROL Einsenden]** , um die Erstellung der Landingpage-Vorgabe zu bestätigen. Sie können die Vorgabe auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. Nachdem die Landingpage-Vorgabe erstellt wurde, wird sie in der Liste mit der **[!UICONTROL Aktiv]** Status. Es kann für Ihre Landingpages verwendet werden.

   ![](assets/lp-preset-active-temp.png)

Sie können jetzt [Landingpages erstellen](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].

>[!NOTE]
>
>Informationen zum Erstellen von Nachrichtenvorgaben für Push-Benachrichtigungen und E-Mails finden Sie in [diesem Abschnitt](message-presets.md).

**Verwandte Themen**:

* [Erste Schritte mit Landingpages](../landing-pages/get-started-lp.md)
* [Erstellen einer Landingpage](../landing-pages/create-lp.md#create-a-lp)
