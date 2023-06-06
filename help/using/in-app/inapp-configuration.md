---
title: In-App-Konfiguration
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von In-App-Nachrichten mit Journey Optimizer konfigurieren können
role: Admin
level: Intermediate
keywords: In-App, Nachricht, Konfiguration, Plattform
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 21aeac323a43ac95d98f4798ff3d51ad32f2ebf9
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 100%

---

# Konfigurieren des In-App-Kanals {#inapp-configuration}

Bevor Sie In-App-Nachrichten senden können, müssen Sie Ihren In-App-Kanal in [!DNL Adobe Experience Platform Data Collection] konfigurieren.

1. Rufen Sie von Ihrem [!DNL Adobe Experience Platform Data Collection]-Konto aus das Menü **[!UICONTROL Datenstrom]** auf und klicken Sie auf **[!UICONTROL Neuer Datenstrom]**. Weiterführende Informationen zur Erstellung von Datenströmen finden Sie auf [dieser Seite](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. Wählen Sie den [!DNL Adobe Experience Platform]-Service.

   [!DNL Edge Segmentation] und [!DNL Adobe Journey Optimizer] müssen ausgewählt sein.

   ![](assets/inapp_config_6.png)

1. Rufen Sie dann das Menü **[!UICONTROL Programmoberflächen]** auf und klicken Sie auf **[!UICONTROL Programmoberfläche erstellen]**.

   ![](assets/inapp_config_1.png)

1. Fügen Sie Ihrer **[!UICONTROL Programmoberfläche]** einen Namen hinzu.

1. Geben Sie in der Dropdown-Liste „Apple iOS“ Ihre **iOS-Paket-ID** ein. Weitere Informationen zur **Paket-ID** finden Sie in der [Apple-Dokumentation](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids).

   ![](assets/inapp_config_2.png)

1. Geben Sie in der Dropdown-Liste „Android“ Ihren **Android-Paketnamen** ein. Weitere Informationen zu **Paketnamen** finden Sie in der [Android-Dokumentation](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores).

1. Klicken Sie auf **[!UICONTROL Speichern]**, wenn Sie die Konfiguration der **[!UICONTROL Programmoberfläche]** abgeschlossen haben.

   ![](assets/inapp_config_3.png)

   Ihre **[!UICONTROL Programmoberfläche]** ist jetzt beim Erstellen einer neuen Kampagne mit einer In-App-Nachricht verfügbar. [Weitere Informationen](create-in-app.md)

1. Nachdem Sie Ihre Programmoberfläche erstellt haben, müssen Sie eine Eigenschaft für Mobilgeräte erstellen.

   Informationen zum detaillierten Verfahren finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=de#for-mobile).

   ![](assets/inapp_config_4.png)

1. Installieren Sie über das Menü „Erweiterungen“ Ihrer neu erstellten Eigenschaft die folgenden Erweiterungen:

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP-Sicherheit
   * Einverständnis
   * Identität
   * Core für Mobilgeräte
   * Profil

   Informationen zum detaillierten Verfahren finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=de#add-a-new-extension).

   ![](assets/inapp_config_5.png)

Der In-App-Kanal ist jetzt konfiguriert. Sie können nun mit dem Versand von In-App-Nachrichten an Ihre Benutzerinnen und Benutzer beginnen.

**Verwandte Themen:**

* [Erstellen einer In-App-Nachricht](create-in-app.md)
* [Erstellen einer Kampagne](../campaigns/create-campaign.md)
* [Entwerfen der In-App-Nachricht](design-in-app.md)
* [In-App-Bericht](../reports/campaign-global-report.md#inapp-report)
