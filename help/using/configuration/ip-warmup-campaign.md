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
source-git-commit: 77d8da88b72cada82d30afa8bab5a63ab435f625
workflow-type: ht
source-wordcount: '407'
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

Bevor Sie den eigentlichen IP-Warmup-Plan in [!DNL Journey Optimizer] erstellen, müssen Sie zunächst eine oder mehrere Kampagnen erstellen, die speziell für die Verwendung in einem IP-Warmup-Plan<!--through a dedicated option--> konzipiert sind.

Um eine IP-Aufwärmkampagne zu erstellen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine [E-Mail](../email/email-settings.md)-Kanal-[Oberfläche](channel-surfaces.md) für die Domain und die IPs, die für den Aufwärmplan identifiziert wurden.

   >[!NOTE]
   >
   >Weitere Informationen dazu, wie die Domäne und IPs ausgewählt werden können, die auf einer E-Mail-Oberfläche verwendet werden sollen, finden Sie in [diesem Abschnitt](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Arbeiten Sie mit Ihren Fachleuten für Zustellbarkeit zusammen, um die Domain und die IPs zu identifizieren, die für Ihren IP-Aufwärmplan verwendet werden sollen.<!--TBC-->

1. Erstellen Sie eine geplante [Kampagne](../campaigns/create-campaign.md) und wählen Sie die Aktion [E-Mail](../email/create-email.md#create-email-journey-campaign).

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

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

1. [Aktivieren](../campaigns/review-activate-campaign.md) Sie die Kampagne. Der Status ändert sich in **[!UICONTROL Live]**

   >[!NOTE]
   >
   >Bei einer Live-Kampagne mit aktiviertem IP-Aufwärmplan ist die Schaltfläche **[!UICONTROL Löschen]** verfügbar, bis sie mit einem IP-Aufwärmplan verknüpft ist. Sobald die Kampagne in einem Plan verwendet wurde, kann sie nicht mehr gelöscht werden.

1. Die Kampagne wird in der Liste **[!UICONTROL Kampagnen]** angezeigt. Um alle in der aktuellen Sandbox erstellten IP-Aufwärmkampagnen einfach abzurufen, können Sie nach der Kampagnenoption **[!UICONTROL IP-Aufwärmen]** filtern.

   ![](assets/ip-warmup-campaign-filter.png)

Sobald die Kampagne live ist, kann sie in einem IP-Aufwärmplan verwendet werden. [Weitere Informationen](ip-warmup-plan.md)

Eine IP-Warmup-Kampagne kann in nur einem IP-Warmup-Plan verwendet werden. Dieselbe Kampagne kann jedoch in einer oder mehreren Phasen desselben IP-Aufwärmplans verwendet werden. [Weitere Informationen](ip-warmup-plan.md#define-phases)

>[!NOTE]
>
>Wenn eine Live-Kampagne in einem IP-Warmup-Plan verwendet wird, ändert sich der Status dieser Kampagne, nachdem der Plan als [abgeschlossen](ip-warmup-execution.md#mark-as-completed) markiert wurde, in **[!UICONTROL gestoppt]**.

