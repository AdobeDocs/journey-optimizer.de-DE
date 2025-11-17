---
title: Erste Schritte mit Code-basierten Erlebnissen
description: Informationen zu Code-basierten Erlebnissen in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '855'
ht-degree: 100%

---

# Erste Schritte mit dem Code-basierten Kanal {#get-started-code-based}

Mit [!DNL Journey Optimizer] können Sie die Erlebnisse, die Sie Ihren Kundinnen und Kunden bereitstellen möchten, für alle Touchpoints personalisieren und testen, z. B. Web-Apps, Mobile Apps, Desktop-Apps, Video-Konsolen, TV-verbundene Geräte, Smart-TVs, Kiosks, Geldautomaten, Sprachassistenten, IoT-Geräte usw.

Mit der Funktion **Code-basiertes Erlebnis** können Sie eingehende Erlebnisse mit einem einfachen und intuitiven, nicht visuellen Editor definieren. Sie können damit unabhängig vom Anwendungstyp bestimmte Elemente an einzelnen und detaillierteren Stellen Ihrer Apps oder Web-Seiten einfügen und bearbeiten, anstatt Änderungen an einem gesamten Inhalt vorzunehmen.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Auf [dieser Seite](code-based-prerequisites.md) werden spezifische Empfehlungen für Code-basierte Erlebnisse beschrieben.


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ In [diesem Abschnitt](../experience-decisioning/experience-decisioning-uc.md) wird ein End-to-End-Anwendungsfall vorgestellt, der zeigt, wie Inhaltsexperimente verwendet werden können, um Entscheidungen mit dem Code-basierten Erlebniskanal zu vergleichen.

## Verwendung von Code-basierten anstelle von anderen Kanälen {#code-based-vs-other-channels}

### Code-basierte und andere Kanäle im Vergleich

Wann sollte anstelle der anderen [!DNL Journey Optimizer]-Kanäle ein Code-basierter Kanal verwendet werden?

* Sie können Code-basierte Erlebnisse jederzeit verwenden, wenn nicht über einen Webbrowser oder eine Mobile App auf Ihre digitale Eigenschaft zugegriffen wird. In den letzteren Fällen sollten Sie lieber den Kanal [!DNL Journey Optimizer] [Web-Kanal](../web/get-started-web.md){target="_blank"} oder [!DNL Journey Optimizer] [In-App-Messaging](../../rp_landing_pages/in-app-landing-page.md){target="_blank"} verwenden.

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* Sie können den Code-basierten Kanal als Alternative zu den Web- oder In-App-Kanälen von [!DNL Journey Optimizer] verwenden, falls Sie über eine API-basierte Headless- oder Server-seitige Implementierung verfügen.

* Sie können den Code-basierten Kanal auch in nativen mobilen Anwendungen als Alternative zum In-App-Kanal nutzen, wenn Sie den Inhalt in Ihrer nativen App ändern möchten, anstatt Modale, Popups oder Überlagerungen anzuzeigen.

### Code-basierte Kanäle und Web-Kanäle im Vergleich {#code-based-vs-web}

Um Web-Anwendungsfälle auszuführen, können Sie entweder den Web-Kanal oder das Code-basierte Erlebnis verwenden. Je nach Kontext eignet sich ein Erlebnis jedoch meist besser als das andere. Die wichtigsten Unterschiede sind unten aufgeführt, sodass Sie eine fundierte Entscheidung darüber treffen können, was Sie wann verwenden.

**Web**

* Bearbeiten Sie Ihre Inhalte mit dem visuellen Editor [Web Designer](../web/web-visual-editor.md){target="_blank"} oder dem [nicht visuellen Editor](../web/web-non-visual-editor.md) im Web.
* Sie benötigen eine Client-seitige Implementierung des [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"}.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* Mit dem Web-Kanal können Sie alles auf Ihrer Seite ändern. Außerdem bietet er eine vordefinierte Liste von Aktionen, mit denen Sie Änderungen vornehmen können. [Weitere Informationen](../web/web-visual-editor.md){target="_blank"}
* Er lässt sich schnell einrichten und ausführen.
* Er ist auf Marketing-Fachleute ausgerichtet.

**Code-basiertes Erlebnis**

* Bearbeiten Sie Ihren Inhalt mit dem [Personalisierungseditor](create-code-based.md#edit-code).
* Sie benötigen entweder die Client-seitige Implementierung des [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} oder die Server-seitige Implementierung des [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de){target="_blank"}.
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

Nachstehend finden Sie die wichtigsten Schritte zur Erstellung und Bereitstellung eines Code-basierten Erlebnisses.

1. Befolgen Sie die kanalspezifischen Voraussetzungen. [Weitere Informationen](code-based-prerequisites.md)

1. Definieren Sie eine [Oberfläche](code-based-surface.md#surface-definition) in Ihrer Anwendungsimplementierung, die im Wesentlichen der Ort ist, zu dem Sie Ihr Erlebnis hinzufügen möchten.

1. Erstellen Sie eine Code-basierte Kanalkonfiguration, die auf diesen Ort verweist. [Weitere Informationen](code-based-configuration.md#create-code-based-configuration)

1. Erstellen Sie mit dieser Konfiguration eine Journey oder Kampagne in [!DNL Journey Optimizer]. [Weitere Informationen](create-code-based.md#create-code-based-experience)

1. Erstellen Sie ein Erlebnis, indem Sie mit dem Personalisierungseditor von [!DNL Journey Optimizer] Inhalte für die ausgewählte Konfiguration angeben. [Weitere Informationen](create-code-based.md#edit-code)

1. Testen Sie das Code-basierte Erlebnis. [Weitere Informationen](test-code-based.md)

1. Veröffentlichen Sie es. [Weitere Informationen](publish-code-based.md)

1. Sobald die Code-basierte Erlebnis-Journey oder -Kampagne live ist, muss die App- oder Seitenimplementierung vorhanden sein, die Inhalte für die Oberfläche anfordert, damit die Inhalte abgerufen und angezeigt werden können.

   >[!INFO]
   >
   >Um das zu gewährleisten, erstellt das App-Implementierungs-Team explizite API- oder SDK-Aufrufe, um Inhalte für die in der Code-basierten Konfiguration definierten Oberfläche abzurufen, z. B. „Bannertext“ oder „Empfehlungsablage 1“, oder nicht UI-bezogene Entscheidungspunkte in einer Anwendung, z. B. „Suchalgorithmusparameter“. <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [Weitere Informationen](code-based-implementation-samples.md)

## Weitere Ressourcen

* **[Erstellen von Code-basierten Erlebnissen](create-code-based.md)** – Erfahren Sie, wie Sie Code-basierte Kampagnen und Journeys für benutzerdefinierte Implementierungen erstellen und konfigurieren.
* **[Konfigurieren des Code-basierten Kanals](code-based-configuration.md)** – Richten Sie Konfigurationen für Code-basierte Erlebnisse mit geeigneten Oberflächen- und Implementierungseinstellungen ein.
* **[Code-basierte Voraussetzungen](code-based-prerequisites.md)** – Machen Sie sich mit den technischen Anforderungen und Entwicklerressourcen vertraut, die für die Implementierung erforderlich sind.
* **[Testen von Code-basierten Erlebnissen](test-code-based.md)** – Erfahren Sie, wie Sie Ihre Code-basierten Erlebnisse vor der Veröffentlichung in der Vorschau anzeigen und testen können.
* **[Implementierungsbeispiele](code-based-implementation-samples.md)** – Erkunden Sie Code-Beispiele und Implementierungsmuster für verschiedene Anwendungsfälle.
* **[Tutorials für Code-basierte Erlebnisse](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/create-a-code-based-experience-campaign){target="_blank"}** – Erkunden Sie detaillierte Video-Tutorials zu Code-basierten Funktionen und Best Practices.

