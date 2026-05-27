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
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
TQID: https://experienceleague.adobe.com/mzP9buvUwW2h0QahDBXWxefokjZv-XziM-uFaPwg3Wg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c343082f-e963-4f57-a96b-b64d27f8118eid: e23d48b5-7858-4d45-9c56-9e2b4be8500eid: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 459
ht-degree: 100%

---

# Erstellen von IP-Aufwärmkampagnen {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Aktivieren der Option IP-Aufwärmplan"
>abstract="Wenn diese Option ausgewählt wurde, kann die Kampagne in einem IP-Aufwärmplan verwendet werden. Der Kampagnenzeitplan wird dann durch den IP-Aufwärmplan gesteuert, mit dem er verbunden ist."

Bevor Sie den eigentlichen IP-Warmup-Plan in [!DNL Journey Optimizer] erstellen, müssen Sie zunächst eine oder mehrere Kampagnen erstellen, die speziell für die Verwendung in einem IP-Warmup-Plan<!--through a dedicated option--> konzipiert sind.

Um eine IP-Aufwärmkampagne zu erstellen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine E-Mail-Kanal-[Konfiguration](channel-surfaces.md) für die Domain und die IPs erstellen, die für den Aufwärmplan identifiziert wurden.

   Arbeiten Sie mit Ihren Fachleuten für Zustellbarkeit zusammen, um die Domain und die IPs zu identifizieren, die verwendet werden sollen. Informationen zu ihrer Auswahl in einer E-Mail-Konfiguration finden Sie in [diesem Abschnitt](../email/email-settings.md#ip-pools).

   >[!CAUTION]
   >
   >Bearbeiten Sie die Konfiguration des E-Mail-Kanals nicht, nachdem der IP-Aufwärmplan [gestartet](ip-warmup-execution.md) wurde.

1. Erstellen Sie eine geplante Marketing-[Kampagne](../campaigns/create-campaign.md) und wählen Sie die Aktion [E-Mail](../email/create-email.md#create-email).

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

1. Wählen Sie die Konfiguration aus, die Sie für das IP-Aufwärmen erstellt haben.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same configuration as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Wählen Sie im Abschnitt **[!UICONTROL Zeitplan]** die Option **[!UICONTROL IP-Aufwärmplan aktivieren]** aus.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   Der [Zeitplan](../campaigns/campaign-schedule.md) der Kampagne wird vom IP-Aufwärmplan gesteuert, mit dem er verknüpft wird, was bedeutet, dass der Zeitplan nicht mehr in der Kampagne selbst definiert ist.

1. Führen Sie die Schritte zur Erstellung einer E-Mail-Kampagne aus, wie z. B. das Definieren der Kampagneneigenschaften, der [Zielgruppe](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?--> und des [Inhalts](../email/get-started-email-design.md#key-steps).

   >[!IMPORTANT]
   >
   >In einer IP-Aufwärmkampagne zulässige Zielgruppen müssen [segmentbasiert](../audience/creating-a-segment-definition.md) sein und mithilfe der [standardmäßigen Zusammenführungsrichtlinie](https://experienceleague.adobe.com/de/docs/experience-platform/profile/merge-policies/overview#default-merge-policy){target="_blank"} erstellt werden.
   >
   >CSV-Upload-Zielgruppen werden für IP-Aufwärmkampagnen nicht unterstützt und führen bei der Aktivierung der Kampagne zu einem Fehler.

   Weitere Informationen zur Konfiguration Ihrer Kampagne finden Sie auf [dieser Seite](../campaigns/get-started-with-campaigns.md).

1. [Aktivieren](../campaigns/review-activate-campaign.md) Sie die Kampagne. Der Status ändert sich in **[!UICONTROL Live]**

   >[!NOTE]
   >
   >[Geschäftsregeln](../conflict-prioritization/rule-sets.md#rule-sets) sollten nicht für IP-Aufwärmpläne verwendet werden. Die Anwendung dieser Regeln kann dazu führen, dass die gewünschte Anzahl von Zielgruppenprofilen für Kampagnen nicht erreicht wird.

   Bei einer Live-Kampagne mit aktiviertem IP-Aufwärmplan ist die Schaltfläche **[!UICONTROL Löschen]** verfügbar, bis sie mit einem IP-Aufwärmplan verknüpft ist. Sobald die Kampagne in einem Plan verwendet wurde, kann sie nicht mehr gelöscht werden.

1. Die Kampagne wird in der Liste **[!UICONTROL Kampagnen]** angezeigt. Um alle in der aktuellen Sandbox erstellten IP-Aufwärmkampagnen einfach abzurufen, können Sie nach der Kampagnenoption **[!UICONTROL IP-Aufwärmen]** filtern.

   ![](assets/ip-warmup-campaign-filter.png)

Sobald die Kampagne live ist, kann sie in einem IP-Aufwärmplan verwendet werden. [Weitere Informationen](ip-warmup-plan.md)

Eine IP-Warmup-Kampagne kann in nur einem IP-Warmup-Plan verwendet werden. Dieselbe Kampagne kann jedoch in einer oder mehreren Phasen desselben IP-Aufwärmplans verwendet werden. [Weitere Informationen](ip-warmup-plan.md#ip-warmup-plan-tab)

>[!NOTE]
>
>Wenn eine Live-Kampagne in einem IP-Aufwärmplan verwendet wird, ändert sich der [Status](../campaigns/manage-campaigns.md#statuses) dieser Kampagne, nachdem der Plan [als abgeschlossen markiert wurde](ip-warmup-execution.md#mark-as-completed), in **[!UICONTROL Gestoppt]**.

