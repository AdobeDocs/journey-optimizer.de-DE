---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von IP-Aufwärmekampagnen
description: Erfahren Sie, wie Sie eine IP-Warmup-Kampagne erstellen.
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, Pools, Gruppe, Subdomains, Zustellbarkeit
hide: true
hidefromtoc: true
source-git-commit: ea86d44f7c9309ff69877e01cea6a13e7907a039
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 8%

---

# Erstellen von IP-Aufwärmekampagnen {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Aktivieren Sie die Option IP-Warmup-Plan ."
>abstract="Wählen Sie die Option zur Aktivierung des IP-Aufwärmungsplans aus. Sobald die Kampagne aktiv ist, kann sie mit einem IP-Warmup-Plan verknüpft werden."

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit IP-Wärme](ip-warmup-gs.md)
* **[Erstellen von IP-Aufwärmekampagnen](ip-warmup-campaign.md)**
* [Erstellen eines IP-Warmup-Plans](ip-warmup-plan.md)
* [IP-Warmup-Plan ausführen](ip-warmup-running.md)

>[!ENDSHADEBOX]

Sie müssen eine oder mehrere Kampagnen mit aktivierter Option erstellen, damit sie in einem IP-Aufwärmplan verwendet werden können.

Gehen Sie wie folgt vor, um eine IP-Warmup-Kampagne zu erstellen.

1. E-Mail erstellen [Oberfläche](channel-surfaces.md) für die Domain und die IPs, die Sie für Ihren Warmup-Plan identifiziert haben.<!--how do you identify these or who does it at the customer level?-->

   >[!NOTE]
   >
   >Erfahren Sie, wie Sie die Domäne und IPs auswählen, die auf einer E-Mail-Oberfläche verwendet werden sollen in [diesem Abschnitt](../email/email-settings.md#subdomains-and-ip-pools).

1. Erstellen Sie eine [Kampagne](../campaigns/create-campaign.md) und wählen Sie die [Email](../email/create-email.md#create-email-journey-campaign) Aktion.

1. Wählen Sie die Oberfläche aus, die Sie für die IP-Wärme-Kopplung erstellt haben.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Aus dem **[!UICONTROL Zeitplan]** Bereich, wählen Sie **[!UICONTROL Aktivierung des IP-Warmlaufplans]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   Die Kampagne [Zeitplan](../campaigns/create-campaign.md#schedule) wird von der [IP-Warmup-Plan](ip-warmup-plan.md) wird mit verknüpft, was bedeutet, dass der Zeitplan in der Kampagne selbst nicht mehr definiert ist.

1. [Aktivieren](../campaigns/review-activate-campaign.md) die Kampagne. Sobald es live ist, kann es in einem IP-Warmup-Plan verwendet werden.

>[!NOTE]
>
>Bei einer Live-Kampagne mit aktiviertem IP-Warmup-Plan wird die Variable **[!UICONTROL Löschen]** -Schaltfläche verfügbar, bis sie mit einem IP-Warmup-Plan verknüpft ist.

Weitere Informationen zur Konfiguration Ihrer Kampagne finden Sie auf [dieser Seite](../campaigns/get-started-with-campaigns.md).

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

