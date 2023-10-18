---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von IP-Aufwärmkampagnen
description: Informationen zum Erstellen einer IP-Aufwärmkampagne
feature: Campaigns, IP Warmup Plans
topic: Administration
role: Admin
level: Intermediate
keywords: IP, Pools, Zustellbarkeit
hide: true
hidefromtoc: true
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 100%

---

# Erstellen von IP-Aufwärmkampagnen {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Aktivieren der Option IP-Aufwärmplan"
>abstract="Wenn diese Option ausgewählt wurde, kann die Kampagne in einem IP-Aufwärmplan verwendet werden. Der Kampagnenzeitplan wird dann durch den IP-Aufwärmplan gesteuert, mit dem er verbunden ist."

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit IP-Aufwärmen](ip-warmup-gs.md)
* **[Erstellen von IP-Aufwärmkampagnen](ip-warmup-campaign.md)**
* [Erstellen eines IP-Aufwärmplans](ip-warmup-plan.md)
* [Ausführen des IP-Aufwärmplans](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Vor der Erstellung des IP-Aufwärmplans in [!DNL Journey Optimizer] müssen zunächst eine oder mehrere Kampagnen mit aktivierter dedizierter Option erstellt werden, damit sie in einem IP-Aufwärmplan verwendet werden können.

Um eine IP-Aufwärmkampagne zu erstellen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine [E-Mail](../email/email-settings.md)-Kanal-[Oberfläche](channel-surfaces.md) für die Domain und die IPs, die für den Aufwärmplan identifiziert wurden.

   >[!NOTE]
   >
   >Weitere Informationen dazu, wie die Domäne und IPs ausgewählt werden können, die auf einer E-Mail-Oberfläche verwendet werden sollen, finden Sie in [diesem Abschnitt](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Arbeiten Sie mit Ihren Fachleuten für Zustellbarkeit zusammen, um die Domain und die IPs zu identifizieren, die für Ihren IP-Aufwärmplan verwendet werden sollen.<!--TBC-->

1. Erstellen Sie eine [Kampagne](../campaigns/create-campaign.md) und wählen Sie die Aktion [E-Mail](../email/create-email.md#create-email-journey-campaign).

1. Wählen Sie die Oberfläche aus, die Sie für das IP-Aufwärmen erstellt haben.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Wählen Sie im Abschnitt **[!UICONTROL Zeitplan]** die Option **[!UICONTROL IP-Aufwärmplan aktivieren]** aus.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   Der [Zeitplan](../campaigns/create-campaign.md#schedule) der Kampagne wird vom IP-Aufwärmplan gesteuert, mit dem er verknüpft wird, was bedeutet, dass der Zeitplan nicht mehr in der Kampagne selbst definiert ist.

1. Führen Sie die Schritte zur Erstellung einer E-Mail-Kampagne aus, wie z. B. das Definieren der Kampagneneigenschaften, der [Zielgruppe](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?--> und des [Inhalts](../email/get-started-email-design.md#key-steps).

   >[!NOTE]
   >
   >Weitere Informationen zur Konfiguration Ihrer Kampagne finden Sie auf [dieser Seite](../campaigns/get-started-with-campaigns.md).

1. [Aktivieren](../campaigns/review-activate-campaign.md) Sie die Kampagne.

   >[!NOTE]
   >
   >Bei einer Live-Kampagne mit aktiviertem IP-Aufwärmplan ist die Schaltfläche **[!UICONTROL Löschen]** verfügbar, bis sie mit einem IP-Aufwärmplan verknüpft ist. Sobald die Kampagne in einem Plan verwendet wurde, kann sie nicht mehr gelöscht werden.

1. Die Kampagne wird in der Liste **[!UICONTROL Kampagnen]** angezeigt. Um alle in der aktuellen Sandbox erstellten IP-Aufwärmkampagnen einfach abzurufen, können Sie nach der Kampagnenoption **[!UICONTROL IP-Aufwärmen]** filtern.

   ![](assets/ip-warmup-campaign-filter.png)

Sobald die Kampagne live ist, kann sie in einem IP-Aufwärmplan verwendet werden. [Weitere Informationen](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->
