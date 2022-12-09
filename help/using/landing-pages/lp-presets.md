---
solution: Journey Optimizer
product: journey optimizer
title: Landingpage-Vorgaben definieren
description: Erfahren Sie, wie Sie Ihre Umgebung für die Erstellung und Verwendung von Landingpages mit Journey Optimizer konfigurieren.
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Landingpage-Vorgaben definieren {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="Landingpage-Vorgabe erstellen"
>abstract="Um eine Landingpage zu erstellen und sie über Journey Optimizer zu nutzen, müssen Sie eine Landingpage-Vorgabe erstellen, die die zu verwendende Subdomain enthält."

Wann [Landingpage erstellen](../landing-pages/create-lp.md#create-a-lp)müssen Sie eine Landingpage-Vorgabe auswählen, um die Landingpage erstellen und nutzen zu können. **[!DNL Journey Optimizer]**.

## Auf Landingpage-Vorgaben zugreifen {#access-lp-presets}

Gehen Sie wie folgt vor, um auf Landingpage-Vorgaben zuzugreifen.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Channels]** Menü.

1. Auswählen **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

   ![](assets/lp_presets-access.png)

1. Klicken Sie auf eine beliebige vordefinierte Beschriftung, um auf die Vorgabendetails der Landingpage zuzugreifen.

   ![](assets/lp_preset-details.png)

## Landingpage-Vorgabe erstellen {#lp-create-preset}

Gehen Sie wie folgt vor, um eine Landingpage-Vorgabe zu erstellen.

>[!NOTE]
>
>Um eine Vorgabe erstellen zu können, stellen Sie sicher, dass Sie zuvor mindestens eine Subdomain der Landingpage konfiguriert haben. [Erfahren Sie mehr](lp-subdomains.md)

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Channels]** Menü und wählen Sie **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

1. Auswählen **[!UICONTROL Create landing page preset]**.

   ![](assets/lp_create-preset-temp.png)

1. Geben Sie einen Namen und eine Beschreibung für die Vorgabe ein.

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A-Z) beginnen. Sie darf nur alphanumerische Zeichen enthalten. Sie können auch Unterstriche verwenden `_`, Punkt`.` und Bindestrich `-` Zeichen.

1. Wählen Sie aus der Dropdown-Liste eine Landingpage-Subdomain aus.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Um eine Subdomain auswählen zu können, stellen Sie sicher, dass Sie zuvor mindestens eine Landingpage-Subdomain konfiguriert haben. [Erfahren Sie mehr](#lp-subdomains)

   Die der ausgewählten Subdomain entsprechenden Einstellungen werden angezeigt.

1. Wenn Sie die Subdomain der Landingpage für die Tracking-URL auswählen möchten, überprüfen Sie die **[!UICONTROL Same as landing page subdomain]** -Option. [Erfahren Sie mehr über Tracking](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Wenn die URL der Landingpage beispielsweise &quot;pages.mail.luma.com&quot;lautet und die Tracking-URL &quot;data.mail.luma.com&quot;lautet, können Sie &quot;pages.mail.luma.com&quot;als Tracking-Subdomain auswählen.

1. Klicken **[!UICONTROL Submit]** , um die Erstellung der Landingpage-Vorgabe zu bestätigen. <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. Nachdem die Landingpage-Vorgabe erstellt wurde, wird sie in der Liste mit der **[!UICONTROL Active]** Status. Es kann für Ihre Landingpages verwendet werden.

   ![](assets/lp-preset-active-temp.png)

Sie können jetzt [Landingpages erstellen](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**Verwandte Themen**:

* [Erste Schritte mit Landingpages](../landing-pages/get-started-lp.md)
* [Landingpage erstellen](../landing-pages/create-lp.md#create-a-lp)
