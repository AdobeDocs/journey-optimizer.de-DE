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
source-git-commit: 28395abcdcba6ed8fd02f252a57022aa473f3d3b
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 22%

---

# Erste Schritte mit Adobe Experience Manager-Inhaltsfragmenten {#aem-fragments}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erste Schritte mit Adobe Experience Manager-Inhaltsfragmenten und erfahren Sie, wie der Autoren- und Veröffentlichungslebenszyklus bestimmt, welche Fragmente in Journey Optimizer verfügbar sind.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Für Kundinnen und Kunden im Gesundheitswesen wird die Integration nur bei einer Lizenzierung der Add-on-Angebote Journey Optimizer Healthcare Shield und Adobe Experience Manager Enhanced Security aktiviert.

Durch die Integration von **[!DNL Adobe Experience Manager as a Cloud Service]** und **[!DNL Adobe Experience Manager Managed Service]** mit Adobe Journey Optimizer können Sie AEM-Inhaltsfragmente in Journey und Kampagnen verwenden. **[!DNL Adobe Experience Manager Managed Service]** unterstützt die Integration die Ebenen **Autor** und **Publish** auf **AEM Long Term Support (LTS) SP2**. Echtzeitaktualisierungen von Adobe Experience Manager sind in dieser Version nicht verfügbar. Wenden Sie sich zum Einrichten an den Adobe Managed Services-Support und [Konfigurieren des Adobe Experience Manager-Repository-Zugriffs](aem-admin-settings.md), um Ihr Managed Services-Repository hinzuzufügen.

Weitere Informationen zu AEM-Inhaltsfragmenten finden Sie unter [Arbeiten mit Inhaltsfragmenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} in der Dokumentation zu Experience Manager.

## Lebenszyklus von Inhaltsfragmenten

![](assets/do-not-localize/AEM_CF.png)

Inhaltsfragmente folgen verschiedenen Lebenszyklusphasen, je nachdem, in welcher Adobe Experience Manager-Ebene sie vorhanden sind. [Weitere Informationen finden Sie in der Dokumentation zu Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Inhalte werden auf der **Autorenebene“ erstellt und verwaltet** wo Fragmente Status wie Neu, Entwurf, Veröffentlicht, Geändert oder Veröffentlichung rückgängig gemacht haben können. Diese Status gelten nur für die **Autorenebene** und unterstützen die Inhaltserstellung und -überprüfung.

Wenn ein Inhaltsfragment veröffentlicht wird, wird eine Kopie auf der **Veröffentlichungsebene** erstellt und über einen öffentlichen, nicht authentifizierten Endpunkt verfügbar gemacht. Journey Optimizer unterstützt **[!DNL Adobe Experience Manager as a Cloud Service]** die Integration sowohl mit der **Autorenebene** als auch mit der **Veröffentlichungsebene**.

Infolgedessen werden in Journey Optimizer nur veröffentlichte oder geänderte Inhaltsfragmente angezeigt und es wird immer die neueste veröffentlichte Version verwendet. Änderungen, die nach der Veröffentlichung vorgenommen werden, werden erst dann in Journey Optimizer übernommen, wenn das Inhaltsfragment erneut veröffentlicht wurde.
