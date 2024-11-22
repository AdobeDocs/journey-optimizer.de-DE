---
title: Erste Schritte mit Code-basierten Erlebnissen
description: Informationen zu Code-basierten Erlebnissen in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: bf0a6fa496a08348be16896a7f2313882eb97c06
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 66%

---

# Erste Schritte mit dem Code-basierten Kanal {#get-sarted-code-based}

Mit [!DNL Journey Optimizer] können Sie die Erlebnisse, die Sie Ihren Kundinnen und Kunden bereitstellen möchten, für alle Touchpoints personalisieren und testen, z. B. Web-Apps, Mobile Apps, Desktop-Apps, Video-Konsolen, TV-verbundene Geräte, Smart-TVs, Kiosks, Geldautomaten, Sprachassistenten, IoT-Geräte usw.

Mit der Funktion **Code-basiertes Erlebnis** können Sie eingehende Erlebnisse mit einem einfachen und intuitiven, nicht visuellen Editor definieren. Sie können damit unabhängig vom Anwendungstyp bestimmte Elemente an einzelnen und detaillierteren Stellen Ihrer Apps oder Web-Seiten einfügen und bearbeiten, anstatt Änderungen an einem gesamten Inhalt vorzunehmen.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Auf [dieser Seite](code-based-prerequisites.md) werden spezifische Schutzmechanismen und Empfehlungen für Code-basierte Erlebnisse ausführlich beschrieben.


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Lead" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>Funktionsweise</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="Validierung" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>Schutzmechanismen und Voraussetzungen</strong></a>
</div>
<p>
</td>
<td>
<a href="code-based-configuration.md">
<img alt="Validierung" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>Code-basierte Kanalkonfiguration</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Gelegentlich" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Erstellen eines Code-basierten Erlebnisses</strong></a>
</div>
<p></td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## Verwendung von Code-basierten anstelle von anderen Kanälen {#code-based-vs-other-channels}

### Code-basierte und andere Kanäle im Vergleich

Wann sollte anstelle der anderen [!DNL Journey Optimizer]-Kanäle ein Code-basierter Kanal verwendet werden?

* Sie können Code-basierte Erlebnisse jederzeit verwenden, wenn nicht über einen Webbrowser oder eine Mobile App auf Ihre digitale Eigenschaft zugegriffen wird. In den letzteren Fällen sollten Sie lieber den Kanal [!DNL Journey Optimizer] [Web-Kanal](../web/get-started-web.md){target="_blank"} oder [!DNL Journey Optimizer] [In-App-Messaging](../in-app/get-started-in-app.md){target="_blank"} verwenden.

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* Sie können den code-basierten Kanal als Alternative zu den Web- oder In-App-Kanälen von [!DNL Journey Optimizer] verwenden, falls Sie über eine API-basierte, Headless- oder serverseitige Implementierung verfügen.

* Sie können den code-basierten Kanal auch in nativen mobilen Anwendungen als Alternative zum In-App-Kanal nutzen, wenn Sie den Inhalt in Ihrer nativen App ändern möchten, anstatt Modale, Popups oder Überlagerungen anzuzeigen.

### Code-basierte Kanäle und Web-Kanäle im Vergleich {#code-based-vs-web}

Um Web-Anwendungsfälle auszuführen, können Sie entweder den Web-Kanal oder das Code-basierte Erlebnis verwenden. Je nach Kontext eignet sich ein Erlebnis jedoch meist besser als das andere. Die wichtigsten Unterschiede sind unten aufgeführt, sodass Sie eine fundierte Entscheidung darüber treffen können, was verwendet werden soll und wann.

**Web**

* Bearbeiten Sie Ihren Inhalt mit dem Visual Editor [Web Designer](../web/web-visual-editor.md){target="_blank"} oder dem Web [nicht visuellen Editor](../web/web-non-visual-editor.md).
* Sie benötigen das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} - eine clientseitige Implementierung.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* Mit dem Web-Kanal können Sie alles auf Ihrer Seite ändern. Außerdem bietet er eine vordefinierte Liste von Aktionen, mit denen Sie Änderungen vornehmen können. [Weitere Informationen](../web/web-visual-editor.md){target="_blank"}
* Er lässt sich schnell einrichten und ausführen.
* Er ist auf Marketing-Fachleute ausgerichtet.

**Code-basiertes Erlebnis**

* Bearbeiten Sie Ihren Inhalt mit dem [Personalisierungseditor](create-code-based.md#edit-code).
* Sie benötigen entweder das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} - clientseitige Implementierung oder die [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de){target="_blank"} - serverseitige Implementierung.
* Das Code-basierte Erlebnis erfordert vorherige Entwicklungsarbeiten an Ihrer Implementierung, um sicherzustellen, dass Ihre Anwendungen die von [!DNL Journey Optimizer] für diese Speicherorte veröffentlichten Inhalte interpretieren und bereitstellen können. [Weitere Informationen](code-based-surface.md)
* Dies erfordert mehr Planung, und es können nur die von den Entwicklungspersonen festgelegten Punkte geändert werden. Daher müssen die Komponenten (Startseiten-Banner, Hero Image, Menüleiste) in den Anwendungen, die für die Personalisierung oder Tests geändert werden müssen, unbedingt festgelegt werden. Erstellen Sie zusammen mit Ihrem Entwicklungs-Team die für diese Änderungen erforderliche Implementierung.
* So können Sie JSON-Code-Inhalte verwenden.
* Es ist auf Entwicklungspersonen ausgerichtet.

## Funktionsweise {#how-it-works}

>[!CAUTION]
>
>Diese Funktion richtet sich an Entwicklungspersonen und/oder erfahrene Benutzerinnen und Benutzer. Sie kann von Marketing-Fachleuten mit einiger Erfahrung im Schreiben von Code verwendet werden, sofern die Kanalkonfigurationen und die Ersteinrichtung von Ihrem Entwicklungs-Team durchgeführt werden.

Um Ihre Inhalte mit der Funktion für Code-basierte Erlebnisse von [!DNL Journey Optimizer] zu bearbeiten, müssen Ihre Seiten oder Apps instrumentiert sein. Dazu müssen Sie zuerst die einzelnen Stellen ([Oberflächen](code-based-surface.md) genannt) festlegen, an denen Sie Inhalte einfügen oder ersetzen möchten.

>[!NOTE]
>
>Derzeit können nur HTML- und JSON-Inhalte mit einer Konfiguration verknüpft werden.

Die wichtigsten Schritte zum Erstellen und Bereitstellen eines code-basierten Erlebnisses lauten wie folgt.

1. Befolgen Sie die kanalspezifischen Voraussetzungen. [Weitere Informationen](code-based-prerequisites.md)

1. Definieren Sie eine [Oberfläche](code-based-surface.md#surface-definition) in Ihrer Anwendungsimplementierung, die im Wesentlichen der Ort ist, an dem Sie Ihr Erlebnis hinzufügen möchten.

1. Erstellen Sie eine Code-basierte Kanalkonfiguration, die auf diesen Speicherort verweist. [Weitere Informationen](code-based-configuration.md#create-code-based-configuration)

1. Erstellen Sie mit dieser Konfiguration eine Journey oder Kampagne in [!DNL Journey Optimizer]. [Weitere Informationen](create-code-based.md#create-code-based-campaign)

1. Erstellen Sie ein Erlebnis, indem Sie mit dem Personalisierungseditor von [!DNL Journey Optimizer] Inhalte für die ausgewählte Konfiguration angeben. [Weitere Informationen](create-code-based.md#edit-code)

1. Testen Sie Ihr code-basiertes Erlebnis. [Weitere Informationen](test-code-based.md)

1. Publish. [Weitere Informationen](publish-code-based.md)

1. Sobald Ihre code-basierte Erlebnis-Journey oder -Kampagne live ist, muss die App- oder Seitenimplementierung, die Inhalte für die Oberfläche anfordert, vorhanden sein, damit der Inhalt abgerufen und angezeigt werden kann.

   >[!INFO]
   >
   >Um dies sicherzustellen, sendet Ihr App-Implementierungsteam explizite API- oder SDK-Aufrufe, um Inhalte für die in der code-basierten Konfiguration definierte Oberfläche abzurufen, z. B. &quot;Bannertext&quot;, &quot;Recommendations Tray 1&quot;oder nicht UI-bezogene Entscheidungspunkte in einer Anwendung, z. B. &quot;Suchalgorithmparameter&quot;. <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [Weitere Informationen](code-based-implementation-samples.md)



