---
title: Schutzmechanismen und Voraussetzungen für Code-basierte Erlebnisse
description: Um Apps und Web-Seiten mit der Code-basierten Funktion von Journey Optimizer bearbeiten zu können, befolgen Sie die Voraussetzungen auf dieser Seite
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: b8a71c43ad5b456bfc9ec9b9d3fba06049e604ed
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 100%

---

# Schutzmechanismen und Voraussetzungen {#web-prerequisites}

Um Code-basierte Erlebnisaktionen in [!DNL Journey Optimizer] verwenden und die Payload des Code-Inhalts bereitstellen zu können, die von Ihren Anwendungen verwendet werden kann, müssen Sie die folgenden Voraussetzungen erfüllen:

* Um Änderungen an Ihren Anwendungen hinzuzufügen, benötigen Sie eine bestimmte Implementierung. [Weitere Informationen](#implementation-prerequisites)

* Damit das Code-basierte Erlebnis ordnungsgemäß bereitgestellt werden kann, müssen Sie die Adobe Experience Platform-Einstellungen definieren, die [hier](#delivery-prerequisites) im Detail beschrieben werden.

>[!CAUTION]
>
>Sie können Code-basierte Erlebnisse nur in **Kampagnen** erstellen. [Weitere Informationen](../campaigns/create-campaign.md#configure).

## Voraussetzungen für die Implementierung {#implementation-prerequisites}

Das Code-basierte Erlebnis unterstützt alle Arten der Kundenimplementierung, wie in den folgenden Optionen dargestellt. Sie können für Ihre Eigenschaften entweder eine Client-seitige, eine Server-seitige oder eine hybride Implementierungsmethode verwenden:

* Nur Client-seitig: Um Änderungen an Ihren Web-Seiten oder Mobile Apps vorzunehmen, müssen Sie entweder das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} in Ihre Website oder das [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} in Ihre Mobile Apps implementieren.

* Hybridmodus: Sie können das [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de){target="_blank"} verwenden, um die Personalisierung Server-seitig anzufordern. Die Antwort wird an das Adobe Experience Platform Web SDK weitergeleitet, um die Änderungen Client-seitig zu rendern. Weitere Informationen finden Sie in der [Dokumentation zur Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=de){target="_blank"} von Adobe Experience Platform. Weitere Informationen über den Hybridmodus und einige Implementierungsbeispiele finden Sie in [diesem Blogpost](https://blog.developer.adobe.com/de/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Server-seitig – Sie können die [AEP Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de){target="_blank"} verwenden, um eine Server-seitige Personalisierung anzufordern. Ihr Entwicklungs-Team muss die Antwort verarbeiten und die Änderungen Client-seitig in Ihrer App-Implementierung rendern.

Beispiele für die oben genannten Implementierungsmethoden finden Sie in [diesem Abschnitt](code-based-implementation-samples.md).

## Versandvoraussetzungen {#delivery-prerequisites}

Damit das Code-basierte Erlebnis ordnungsgemäß bereitgestellt werden kann, müssen die folgenden Einstellungen definiert werden:

* Zur [Datenerfassung in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=de){target="_blank"} muss ein Datenstrom definiert sein. Sie können beispielsweise für den **[!UICONTROL Adobe Experience Platform]**-Service die Option **[!UICONTROL Adobe Journey Optimizer]** aktivieren.

  Dadurch wird sichergestellt, dass die von Journey Optimizer eingehenden Ereignisse korrekt von Adobe Experience Platform Edge verarbeitet werden. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* Vergewissern Sie sich in [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de){target="_blank"}, dass Sie eine Zusammenführungsrichtlinie mit der Option **[!UICONTROL Active-On-Edge-Zusammenführungsrichtlinie]** aktiviert haben. Wählen Sie dazu im Experience Platform-Menü **[!UICONTROL Kunde]** > **[!UICONTROL Profile]** > **[!UICONTROL Zusammenführungsrichtlinien]** eine Richtlinie aus. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=de#configure){target="_blank"}

  Diese Zusammenführungsrichtlinie wird von eingehenden Kanälen in [!DNL Journey Optimizer] verwendet, um eingehende Kampagnen auf der Edge korrekt zu aktivieren und zu veröffentlichen. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=de){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Zur Fehlerbehebung beim Versand von Journey Optimizer-Web-Erlebnissen können Sie die Ansicht **Edge Delivery** in **Adobe Experience Platform Assurance** verwenden. Mit diesem Plug-in können Sie Anfrageaufrufe im Detail untersuchen, überprüfen, ob die erwarteten Edge-Aufrufe wie vorgesehen erfolgen, und Profildaten, einschließlich Identitätskarten, Segmentzugehörigkeiten und Zustimmungseinstellungen, untersuchen. Zusätzlich können Sie die Aktivitäten überprüfen, für die sich die Anfrage qualifiziert hat, und diejenigen identifizieren, für die sie nicht qualifiziert war.

  Mit dem Plug-in **Edge Delivery** erhalten Sie die nötigen Erkenntnisse, um Ihre eingehenden Implementierungen effektiv zu verstehen und Fehler zu beheben.

  [Weitere Informationen zur Ansicht „Edge Delivery“](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/view/edge-delivery)

## Voraussetzungen für Inhaltsexperimente {#experiment-prerequisites}

Um Inhaltsexperimente für den Code-basierten Kanal zu aktivieren, müssen Sie sicherstellen, dass der [Datensatz](../data/get-started-datasets.md), der im [Datenstrom](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=de){target="_blank"} Ihrer Web-Implementierung verwendet wird, auch in Ihrer Reporting-Konfiguration enthalten ist.

Anders ausgedrückt: Wenn Sie beim Konfigurieren des Reportings für Experimente einen Datensatz hinzufügen, der nicht in Ihrem App-Datenstrom vorhanden ist, werden keine App-Daten in den Inhaltsexperimentberichten angezeigt.

In [diesem Abschnitt](../content-management/reporting-configuration.md#add-datasets) erfahren Sie, wie Sie Datensätze für das Reporting zu Inhaltsexperimenten hinzufügen.

>[!NOTE]
>
>Der Datensatz wird schreibgeschützt vom Reporting-System von [!DNL Journey Optimizer] verwendet und hat keine Auswirkungen auf die Erfassung oder Aufnahme von Daten.
