---
solution: Journey Optimizer
product: journey optimizer
title: Definieren der Landingpage-Voreinstellungen
description: Erfahren Sie, wie Sie mit Journey Optimizer Ihre Umgebung zur Erstellung und Verwendung von Landingpages konfigurieren.
feature: Landing Pages, Channel Configuration
role: Admin
level: Experienced
keywords: Landing, Landingpage, Konfigurieren, Umgebung, Subdomain, Voreinstellungen
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 8e5a904f9310385f5a8186159dedde9942624268
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 56%

---

# Definieren der Landingpage-Voreinstellungen {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="Erstellen einer Landingpage-Voreinstellung"
>abstract="Um eine Landingpage erstellen und über Journey Optimizer nutzen zu können, müssen Sie eine Landingpage-Voreinstellung erstellen, die die zu verwendende Subdomain enthält."

## Erste Schritte mit Landingpage-Voreinstellungen {#gs-lp-presets}

Beim [Erstellen einer Landingpage](../landing-pages/create-lp.md#create-a-lp) müssen Sie eine Landingpage-Voreinstellung auswählen, damit Sie die Landingpage erstellen und über **[!DNL Journey Optimizer]** nutzen können. Die Voreinstellung enthält die Subdomain, die für die auf dieser Voreinstellung basierenden Landingpages verwendet werden soll.

Bevor Sie eine Voreinstellung erstellen, stellen Sie sicher, dass Sie zuvor mindestens eine Landingpage-Subdomain konfiguriert haben. [Erfahren Sie, wie Sie eine Landingpage-Subdomain erstellen](lp-subdomains.md).

## Zugriff auf Landingpage-Voreinstellungen {#access-lp-presets}

Gehen Sie wie folgt vor, um auf Landingpage-Voreinstellungen zuzugreifen:

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** auf.

1. Wählen Sie **[!UICONTROL Landingpage-Einstellungen]** > **[!UICONTROL Landingpage-Voreinstellungen]** aus.

   ![](assets/lp_presets-access.png)

1. Klicken Sie auf eine beliebige Voreinstellungsbeschriftung, um auf die Voreinstellungsdetails der Landingpage zuzugreifen.

   ![](assets/lp_preset-details.png)

## Erstellen einer Landingpage-Voreinstellung {#lp-create-preset}

Gehen Sie wie folgt vor, um eine Landingpage-Voreinstellung zu erstellen:

1. Durchsuchen Sie das **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** und wählen Sie dann **[!UICONTROL Landingpage-Einstellungen]** > **[!UICONTROL Landingpage-Voreinstellungen]**.

1. Wählen Sie **[!UICONTROL Landingpage-Voreinstellung erstellen]** aus.

   ![](assets/lp_create-preset-temp.png)

1. Geben Sie einen Namen und eine Beschreibung für die Voreinstellung ein.

   Namen müssen mit einem Buchstaben (A-Z) beginnen und dürfen nur alphanumerische Zeichen, Unterstriche `_`, Punkte `.` Bindestriche `-`.

1. Wählen Sie aus der Dropdown-Liste eine Landingpage-Subdomain aus.

   ![](assets/lp_preset-subdomain.png)

   Um eine Subdomain auswählen zu können, müssen Sie zuvor mindestens eine Landingpage-Subdomain konfiguriert haben. [Weitere Informationen dazu](#lp-subdomains)

   Die der ausgewählten Subdomain entsprechenden Einstellungen werden angezeigt.

1. Sie können die Landingpage-Subdomain für die Tracking-URL auswählen, indem Sie die Option **[!UICONTROL Gleiche Subdomain wie Landingpage]** aktivieren. [Weitere Informationen zum Tracking](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Wenn zum Beispiel die URL der Landingpage „pages.mail.luma.com“ und die Tracking-URL „data.mail.luma.com“ lautet, können Sie „pages.mail.luma.com“ als Tracking-Subdomain wählen.

1. Klicken Sie auf **[!UICONTROL Senden]**, um die Erstellung der Landingpage-Voreinstellung zu bestätigen. <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. Nachdem die Landingpage-Voreinstellung erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Aktiv]** angezeigt. Sie kann nun für Ihre Landingpages verwendet werden.

Sie sind nun bereit, in [!DNL Journey Optimizer] [Landingpages zu erstellen](../landing-pages/create-lp.md).
<!--
>[!NOTE]
>
>Learn how to create channel configurations for push notifications and emails in [this section](channel-surfaces.md).-->

**Verwandte Themen**:

* [Erste Schritte mit Landingpages](../landing-pages/get-started-lp.md)
* [Erstellen einer Landingpage](../landing-pages/create-lp.md#create-a-lp)
