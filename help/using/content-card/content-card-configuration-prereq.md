---
title: Konfiguration von Inhaltskarten
description: Kanalvoraussetzungen für Inhaltskarten
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 1f9841ddd039a7591f396e38d8a93ed840d6879e
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 90%

---

# Voraussetzungen für Inhaltskarten {#content-card-configuration-prereq}

Damit Adobe Journey Optimizer Inhaltskarten korrekt anzeigt, müssen Sie die folgenden Adobe Experience Platform-Einstellungen konfigurieren:

* **Adobe Experience Platform – Datenerfassung**

  [Erstellen Sie einen Datenstrom](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/configure){target="_blank"} und [fügen Sie den Dienst „Experience Platform“ hinzu](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/configure#aep){target="_blank"}. Aktivieren Sie die Optionen **[!UICONTROL Edge Segmentation]** und **[!UICONTROL Adobe Journey Optimizer]**. Dadurch wird sichergestellt, dass Ereignisse von Journey Optimizer vom Adobe Experience Platform Edge Network verarbeitet werden.
Fügen Sie die Feldgruppe **Erlebnisereignis – Interaktion mit dem Angebot** zu Ihrem Datensatz hinzu, um diese Daten in Ihre Berichte aufzunehmen. [Weitere Informationen zu Datenströmen](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  Stellen Sie sicher, dass in der Standard-Zusammenführungsrichtlinie von Experience Platform die Option **Active-On-Edge-Zusammenführungsrichtlinie** unter **[!UICONTROL Kunde]** > **[!UICONTROL Profile]** > **[!UICONTROL Zusammenführungsrichtlinien]** aktiviert ist. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=de#configure){target="_blank"}

  >[!NOTE]
  >
  >Wenn Sie eine Zusammenführungsrichtlinie mit einer benutzerdefinierten **[!UICONTROL Datensatzpräferenz]** verwenden, stellen Sie sicher, dass Sie den Datensatz **[!UICONTROL Eingehende Journey]** innerhalb der angegebenen Zusammenführungsrichtlinie hinzufügen.

* **Adobe Experience Platform Mobile- oder Platform Web SDK**

  Für mobile und Web-Anwendungen müssen Sie entweder das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/platform-learn/implement-web-sdk/overview){target="_blank"} auf Ihrer Website oder das [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/){target="_blank"} auf Ihren mobilen Apps implementieren, um Änderungen an Ihren Webseiten oder mobilen Apps vorzunehmen.

* **Journey Optimizer**

  Erstellen Sie eine [Konfiguration für Inhaltskarten](#content-card-configuration).

* **Fehlerbehebung**

  Verwenden Sie die Ansicht **Edge-Versand** in **Adobe Experience Platform Assurance**, um Fehler in mobilen Erlebnissen zu beheben. Sie kann Anfragen untersuchen, Edge-Aufrufe überprüfen und Profildaten untersuchen. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **Experimente mit Inhalten**

  Stellen Sie sicher, dass der im [Datenstrom](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/overview#_blank){target="_blank"} Ihrer App verwendete Datensatz auch in der Konfiguration für das Reporting von Experimenten mit Inhalten enthalten ist. App-Daten werden nicht in Berichten angezeigt, wenn die Datensätze nicht übereinstimmen.

  In [diesem Abschnitt](../reports/reporting-configuration.md) erfahren Sie, wie Sie Datensätze für das Reporting zu Inhaltsexperimenten hinzufügen.

>[!CAUTION]
>
>Wenn Sie pseudonyme Profile (nicht authentifizierte Besucher) mit Ihren Inhaltskarten als Ziel auswählen, sollten Sie eine Time-to-Live (TTL) für das automatische Löschen von Profilen festlegen, um die Anzahl Ihrer interagierbaren Profile und die damit verbundenen Kosten zu verwalten. [Weitere Informationen](../start/guardrails.md#profile-management-inbound)