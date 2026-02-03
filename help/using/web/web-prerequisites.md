---
title: Voraussetzungen für Web-Kanäle
description: Um in der Benutzeroberfläche von Journey Optimizer auf Web-Seiten zuzugreifen oder sie dort zu verfassen, folgen Sie den Voraussetzungen in diesem Abschnitt
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 22e1f08f434a3ceb4be6c539d4007178062cba9e
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 97%

---

# Voraussetzungen und Leitlinien {#web-prerequisites}

Sie müssen folgende Voraussetzungen erfüllen, um Web-Seiten in der Benutzeroberfläche von [!DNL Journey Optimizer] aufzurufen und zu verfassen.

* Um Änderungen an Ihrer Website hinzuzufügen, benötigen Sie eine bestimmte Implementierung. [Weitere Informationen](#implementation-prerequisites)

* Um auf den Web-Designer von [!DNL Journey Optimizer] zuzugreifen, müssen Sie eine bestimmte Browser-Erweiterung für Google Chrome installiert haben. [Weitere Informationen](#visual-authoring-prerequisites)

* Damit das Web-Erlebnis ordnungsgemäß bereitgestellt werden kann, müssen Sie die Adobe Experience Platform-Einstellungen [hier](#delivery-prerequisites) detailliert definieren.

* Um das Reporting für den Web-Kanal zu aktivieren, müssen Sie sicherstellen, dass der Datensatz, der im Datenstrom Ihrer Web-Implementierung verwendet wird, auch in Ihrer Reporting-Konfiguration enthalten ist.  [Weitere Informationen](#experiment-prerequisites)

>[!IMPORTANT]
>
>* Web-Kampagnen in [!DNL Journey Optimizer] sprechen neue Profile an, die zuvor noch nicht auf anderen Kanälen kontaktiert wurden. Dadurch erhöht sich die Gesamtzahl [Engagierbaren Profile](../audience/license-usage.md) was sich auf die Kosten auswirken kann, wenn die vertragliche Anzahl der von Ihnen erworbenen Engagierbaren Profile überschritten wird. Lizenzmetriken für jedes Paket finden Sie auf der Seite [Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Sie können die Anzahl der kontaktierbaren Profile im [Lizenznutzungs-Dashboard“ &#x200B;](../audience/license-usage.md).
>
>* Wenn pseudonyme Profile (nicht authentifizierte Besuchende) mit Ihren Web-Seiten angesprochen werden, sollten Sie eine Time-to-Live (TTL) für die automatische Profillöschung festlegen, um die Anzahl der ansprechbaren Profile und die damit verbundenen Kosten zu verwalten. [Weitere Informationen](../start/guardrails.md#profile-management-inbound)

## Voraussetzungen für die Implementierung {#implementation-prerequisites}

Es werden zwei Arten von Implementierungen unterstützt, um die Erstellung und der Versand von Web-Kanal-Kampagnen in Ihren Web-Eigenschaften zu ermöglichen:

* Nur Client-seitig – Um Änderungen an Ihrer Website vorzunehmen, müssen Sie das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} auf Ihrer Website implementieren.

  >[!NOTE]
  >
  >Stellen Sie sicher, dass Ihre [Adobe Experience Platform Web SDK-Version](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/release-notes){target="_blank"} 2.16 oder höher ist.

* Hybridmodus: Sie können die [AEP Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de){target="_blank"} verwenden, um die Personalisierung Server-seitig anzufordern. Die Antwort wird an das Adobe Experience Platform Web SDK weitergeleitet, um die Änderungen Client-seitig zu rendern. Weitere Informationen finden Sie in der [Dokumentation zur Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=de){target="_blank"} von Adobe Experience Platform. Weitere Informationen zum Hybridmodus und einige Implementierungsbeispiele finden Sie in [diesem Blogpost](https://blog.developer.adobe.com/de/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>Die nur Server-seitige Implementierung wird derzeit für den Web-Kanal nicht unterstützt.  Bei einer nur Server-seitigen Implementierung für Ihre Web-Seiten kann stattdessen der [Code-basierte Erlebniskanal](../code-based/get-started-code-based.md) verwendet werden.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Voraussetzungen für visuelles Authoring {#visual-authoring-prerequisites}

>[!CONTEXTUALHELP]
>id="ajo_web_browser_extension"
>title="Erstellen einer Regel zum Seitenabgleich"
>abstract="Für den Zugriff auf den Web-Designer von [!DNL Journey Optimizer] muss eine bestimmte Browser-Erweiterung installiert sein: Adobe Experience Cloud Visual Editing Helper (nur in Google Chrome oder Microsoft Edge verfügbar)."

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Damit Sie Ihre Web-Seiten zuverlässig im Web-Designer von [!DNL Journey Optimizer] erstellen können, müssen Sie in Ihrem Webbrowser die Browser-Erweiterung [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} installiert haben.

>[!CAUTION]
>
>Google Chrome und Microsoft Edge sind derzeit die einzigen Browser, die die Erstellung von Web-Seiten in [!DNL Journey Optimizer] unterstützen.

### Installieren der Erweiterung Visual Editing Helper {#install-visual-editing-helper}

Gehen Sie wie folgt vor, um die Browser-Erweiterung „Visual Editing Helper“ herunterzuladen und zu installieren.

1. Öffnen Sie eine neue Registerkarte in Ihrem Browser (Google Chrome oder Microsoft Edge).

1. Navigieren Sie zum [Google Chrome Web Store](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Wenn Sie Microsoft Edge verwenden, wählen Sie **[!UICONTROL Erweiterungen von anderen Stores erlauben]** auf dem oberen Banner aus. Dadurch können Sie Erweiterungen aus dem Chrome Web Store zu Microsoft Edge hinzufügen.

1. Suchen Sie die Browser-Erweiterung [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} und navigieren Sie zu ihr.

1. Klicken Sie auf **[!UICONTROL Zu Chrome hinzufügen]** > **[!UICONTROL Erweiterung hinzufügen]**.

   >[!NOTE]
   >
   >Wenn Sie Microsoft Edge verwenden, wird die Erweiterung zu Edge hinzugefügt, auch wenn die Schaltfläche **[!UICONTROL Zu Chrome hinzufügen]** lautet.

1. Stellen Sie sicher, dass die Browser-Erweiterung „Visual Editing Helper“ in der Symbolleiste Ihres Browsers korrekt aktiviert ist.

   ![](assets/web-visual-editing-extension-edge.png)

Der Visual Editing Helper von Adobe Experience Cloud wird jetzt automatisch aktiviert, wenn eine Website im Web-Designer von [!DNL Journey Optimizer] geöffnet wird, um die Inhaltserstellung zu unterstützen.[&#128279;](web-visual-editor.md)

Die Erweiterung verfügt über keine bedingten Einstellungen und verarbeitet alle Einstellungen automatisch, einschließlich der SameSite-Cookie-Einstellungen.

>[!NOTE]
>
>Einige Websites werden möglicherweise aus einem der folgenden Gründe nicht zuverlässig im [!DNL Journey Optimizer]-Web-Designer geöffnet:
>
> * Die Website hat strenge Sicherheitsrichtlinien.
> * Die Website befindet sich in einem iFrame.
> * Die QA- oder Staging-Site des Kunden ist für die Außenwelt nicht zugänglich (die Site ist intern).

### Fehlerbehebung beim Laden einer Website {#troubleshooting}

Wenn Sie bei Verwendung des Adobe [!DNL Journey Optimizer]-Web-Designers versuchen, eine Website zu laden, die nicht geladen werden kann, wird eine Meldung angezeigt, die die Installation der [Browser-Erweiterung Visual Editing Helper](#install-visual-editing-helper) empfiehlt.

1. Stellen Sie sicher, dass die Browser-Erweiterung „Visual Editing Helper“ korrekt installiert ist.

1. Wenn sich die Website immer noch unerwartet verhält, vergewissern Sie sich, dass Cookies von Drittanbietern in Ihrem Browser zugelassen sind, sonst kann die Web-Seite nicht innerhalb des [!DNL Journey Optimizer]-Web-Designers geladen werden.

Bei Seiten unter Authentifizierung, wenn die Anmeldeseite nicht geladen werden kann oder wenn Sie nach dem Anmeldeversuch immer noch nicht angemeldet sind:

1. Versuchen Sie zunächst, sich in einer neuen Browser-Registerkarte anzumelden, navigieren Sie zur gewünschten Seite, kopieren Sie dann die URL und versuchen Sie sie im Web-Designer von [!DNL Journey Optimizer] zu öffnen.

2. Wenn Sie Ihre Website weiterhin nicht in den Web-Designer von [!DNL Journey Optimizer] laden können, wenden Sie sich an die Kundenunterstützung von Adobe, um das Problem zu melden, und geben Sie dabei die fehlerhafte URL an.

## Versandvoraussetzungen {#delivery-prerequisites}

Damit das Web-Erlebnis ordnungsgemäß bereitgestellt werden kann, müssen die folgenden Einstellungen definiert werden:

* Für die [Datenerfassung in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=de){target="_blank"} muss ein Datenstrom definiert sein. Sie können beispielsweise für den **[!UICONTROL Adobe Experience Platform]**-Service die Option **[!UICONTROL Adobe Journey Optimizer]** aktivieren.

  Dadurch wird sichergestellt, dass die von Journey Optimizer eingehenden Ereignisse korrekt von Adobe Experience Platform Edge verarbeitet werden. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* Vergewissern Sie sich in [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de){target="_blank"}, dass Sie eine Zusammenführungsrichtlinie mit der Option **[!UICONTROL Active-On-Edge-Zusammenführungsrichtlinie]** aktiviert haben. Wählen Sie dazu im Experience Platform-Menü **[!UICONTROL Kunde]** > **[!UICONTROL Profile]** > **[!UICONTROL Zusammenführungsrichtlinien]** eine Richtlinie aus. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=de#configure){target="_blank"}

  Diese Zusammenführungsrichtlinie wird von eingehenden Kanälen in [!DNL Journey Optimizer] verwendet, um eingehende Kampagnen am Edge korrekt zu aktivieren und zu veröffentlichen. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=de){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* Zur Fehlerbehebung beim Versand von Journey Optimizer-Web-Erlebnissen können Sie die Ansicht **Edge Delivery** innerhalb von **Adobe Experience Platform Assurance** verwenden. Mit diesem Plug-in können Sie Anfrageaufrufe im Detail untersuchen, überprüfen, ob die erwarteten Edge-Aufrufe wie vorgesehen erfolgen, und Profildaten, einschließlich Identitätskarten, Segmentzugehörigkeiten und Zustimmungseinstellungen, untersuchen. Zusätzlich können Sie die Aktivitäten überprüfen, für die sich die Anfrage qualifiziert hat, und diejenigen identifizieren, für die sie nicht qualifiziert war.

  Mit dem Plug-in **Edge Delivery** erhalten Sie die nötigen Erkenntnisse, um Ihre eingehenden Implementierungen effektiv zu verstehen und Fehler zu beheben.

  [Weitere Informationen zur Ansicht „Edge Delivery“](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/view/edge-delivery)

## Reporting-Voraussetzungen {#experiment-prerequisites}

Um das Reporting für den Web-Kanal zu aktivieren, müssen Sie sicherstellen, dass der [Datensatz](../data/get-started-datasets.md), der im [Datenstrom](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=de){target="_blank"} Ihrer Web-Implementierung verwendet wird, auch in Ihrer Reporting-Konfiguration enthalten ist.

Mit anderen Worten: Wenn Sie bei der Konfiguration des Reportings einen Datensatz hinzufügen, der nicht in Ihrem Web-Datenstrom enthalten ist, werden die Web-Daten nicht in Ihren Berichten angezeigt.

Erfahren Sie in [diesem Abschnitt](../reports/reporting-configuration.md#add-datasets), wie Sie Datensätze für das Reporting hinzufügen.

>[!NOTE]
>
>Der Datensatz wird schreibgeschützt vom Reporting-System von [!DNL Journey Optimizer] verwendet und hat keine Auswirkungen auf die Erfassung oder Aufnahme von Daten.

Wenn Sie die vordefinierten [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} `AEP Web SDK ExperienceEvent` und `Consumer Experience Event` (wie auf [dieser Seite](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html?lang=de#add-field-groups){target="_blank"} definiert) für Ihr Datensatzschema **nicht** verwenden, stellen Sie sicher, dass Sie die folgenden Feldergruppen hinzufügen: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` und `Web Details`. Diese werden vom Reporting in [!DNL Journey Optimizer] benötigt, da sie verfolgen, an welchen Kampagnen und Journeys die einzelnen Profile teilnehmen.

[Weitere Informationen zur Reporting-Konfiguration](../reports/reporting-configuration.md)

>[!NOTE]
>
>Das Hinzufügen dieser Feldgruppen hat keine Auswirkungen auf die normale Datenerfassung. Dies ist nur für die Seiten nützlich, bei denen eine Kampagne oder Journey ausgeführt wird, sodass das Tracking aller anderen Seiten unberührt bleibt.

## Marken-Domains für Assets {#branded-domains-for-assets}

Wenn Sie beim Erstellen von Web-Erlebnissen Inhalte aus der Bibliothek von [Adobe Experience Manager Assets](../integrations/assets.md) verwenden, müssen Sie die Subdomain einrichten, die zum Veröffentlichen dieses Inhalts verwendet wird. [Weitere Informationen](web-delegated-subdomains.md)
