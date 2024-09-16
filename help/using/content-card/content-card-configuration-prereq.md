---
title: Konfiguration der Inhaltskarten
description: Voraussetzungen für den Kanal "Inhaltskarten"
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 19%

---

# Voraussetzungen für Inhaltskarten {#content-card-configuration-prereq}

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

* [Erste Schritte mit Inhaltskarten](get-started-content-card.md)
* **Voraussetzungen für Inhaltskarten**
* [Inhaltskartenkanal in Journey Optimizer konfigurieren](content-card-configuration.md)
* [Erstellen von Inhaltskarten](create-content-card.md)
* [Inhaltskarten erstellen](design-content-card.md)
* [Inhaltskarten-Bericht](content-card-report.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Inhaltskarten sind derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.

Damit Adobe Journey Optimizer Inhaltskarten korrekt anzeigt, müssen Sie die folgenden Adobe Experience Platform-Einstellungen konfigurieren:

* **Adobe Experience Platform-Datenerfassung**

  [Erstellen Sie einen Datastream](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) und [fügen Sie den Experience Platform-Dienst](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep) hinzu. Aktivieren Sie die Optionen **[!UICONTROL Edge Segmentation]** und **[!UICONTROL Adobe Journey Optimizer]** . Dadurch wird sichergestellt, dass Journey Optimizer-Ereignisse vom Adobe Experience Platform-Edge Network verarbeitet werden. Weitere Informationen zum Konfigurieren eines Datenspeichers finden Sie in der Dokumentation zu [datastreams](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) .

* **Adobe Experience Platform**

  Stellen Sie sicher, dass für die standardmäßige Zusammenführungsrichtlinie **Active-On-Edge-Zusammenführungsrichtlinie** unter dem Experience Platform-Menü **[!UICONTROL Kunde]** > **[!UICONTROL Profile]** > **[!UICONTROL Zusammenführungsrichtlinien]** aktiviert ist. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=de#configure){target="_blank"}

  >[!NOTE]
  >
  >Wenn Sie eine Zusammenführungsrichtlinie mit einer benutzerdefinierten **[!UICONTROL Datensatzpräferenz]** verwenden, stellen Sie sicher, dass Sie den Datensatz **[!UICONTROL Journey Inbound]** innerhalb der angegebenen Zusammenführungsrichtlinie hinzufügen.

* **Adobe Experience Platform Mobile- oder Platform Web-SDK**

  Um Änderungen an Ihren Web-Seiten oder Apps für mobile und Webanwendungen hinzuzufügen, müssen Sie entweder das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/platform-learn/implement-web-sdk/overview) auf Ihrer Website oder das [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/) auf Ihren mobilen Apps implementieren.

* **Journey Optimizer**

  Erstellen Sie eine [Inhaltskartenkonfiguration](#content-card-configuration).

* **Fehlerbehebung**

  Verwenden Sie die Ansicht **Edge Delivery** in **Adobe Experience Platform Assurance**, um Probleme mit mobilen Erlebnissen zu beheben. Sie kann Anforderungen überprüfen, Edge-Aufrufe überprüfen und Profildaten untersuchen. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/view/edge-delivery)

* **Inhaltserlebnisse**

  Stellen Sie sicher, dass der Datensatz, der im [Datastream](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank) Ihrer App verwendet wird, auch in Ihrer Konfiguration für die Berichterstellung zu Inhaltsexperimenten enthalten ist. App-Daten werden in Berichten nicht angezeigt, wenn Datensätze nicht übereinstimmen.

  In [diesem Abschnitt](../content-management/reporting-configuration.md) erfahren Sie, wie Sie Datensätze für das Reporting zu Inhaltsexperimenten hinzufügen.
