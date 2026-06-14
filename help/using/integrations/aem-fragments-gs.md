---
solution: Journey Optimizer
product: journey optimizer
title: AEM-Inhaltsfragmente
description: Erfahren Sie, wie Sie auf AEM-Inhaltsfragmente zugreifen und diese verwalten
topic: Content Management
role: User
level: Beginner
exl-id: c36a53a4-c324-4082-838e-ed27bd3b2e90
TQID: https://experienceleague.adobe.com/GRQ3Wz7Y4YJ3545mTtju0R8en9BYiejyo8UoMx558nM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 40%

---

# Erste Schritte mit Adobe Experience Manager-Inhaltsfragmenten {#aem-fragments}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erste Schritte mit Adobe Experience Manager-Inhaltsfragmenten und erfahren Sie, wie der Autoren- und Veröffentlichungslebenszyklus bestimmt, welche Fragmente in Journey Optimizer verfügbar sind.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Für Kundinnen und Kunden im Gesundheitswesen wird die Integration nur bei einer Lizenzierung der Add-on-Angebote Journey Optimizer Healthcare Shield und Adobe Experience Manager Enhanced Security aktiviert.

Durch die Integration von Adobe Experience Manager as a Cloud Service mit Adobe Journey Optimizer können Sie jetzt Ihre AEM-Inhaltsfragmente nahtlos in Journey Optimizer in Ihre Inhalte integrieren. Diese optimierte Verbindung vereinfacht den Zugriff auf und die Nutzung von AEM-Inhalten und ermöglicht die Erstellung personalisierter und dynamischer Kampagnen und Journeys.

Weitere Informationen zu AEM-Inhaltsfragmenten finden Sie unter [Arbeiten mit Inhaltsfragmenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} in der Dokumentation zu Experience Manager.

## Lebenszyklus von Inhaltsfragmenten

![](assets/do-not-localize/AEM_CF.png)

Inhaltsfragmente folgen verschiedenen Lebenszyklusphasen, je nachdem, in welcher Adobe Experience Manager-Ebene sie vorhanden sind. [Weitere Informationen finden Sie in der Dokumentation zu Adobe Experience Manager](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Inhalte werden auf der **Autorenebene“ erstellt und verwaltet** wo Fragmente Status wie Neu, Entwurf, Veröffentlicht, Geändert oder Veröffentlichung rückgängig gemacht haben können. Diese Status gelten nur für die **Autorenebene** und unterstützen die Inhaltserstellung und -überprüfung.

Wenn ein Inhaltsfragment veröffentlicht wird, wird eine Kopie auf der **Veröffentlichungsebene** erstellt und über einen öffentlichen, nicht authentifizierten Endpunkt verfügbar gemacht. Journey Optimizer kann ausschließlich mit dieser **Veröffentlichungsebene“ integriert**.

Infolgedessen werden in Journey Optimizer nur veröffentlichte oder geänderte Inhaltsfragmente angezeigt und es wird immer die neueste veröffentlichte Version verwendet. Änderungen, die nach der Veröffentlichung vorgenommen werden, werden erst dann in Journey Optimizer übernommen, wenn das Inhaltsfragment erneut veröffentlicht wurde.
