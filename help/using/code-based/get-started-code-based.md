---
title: Erste Schritte mit Code-basierten Erlebnissen
description: Informationen zu Code-basierten Erlebnissen in Journey Optimizer
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 100%

---

# Erste Schritte mit dem Code-basierten Kanal {#get-sarted-code-based}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* **[Erste Schritte mit dem Code-basierten Kanal](get-started-code-based.md)**
* [Voraussetzungen für Code-basierte Erlebnisse](code-based-prerequisites.md)
* [Implementierungsbeispiele für Code-basierte Erlebnisse](code-based-implementation-samples.md)
* [Erstellen von Code-basierten Erlebnissen](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Dieser Code-basierte Kanal ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Mit [!DNL Journey Optimizer] können Sie die Erlebnisse, die Sie Ihren Kundinnen und Kunden bereitstellen möchten, für alle Touchpoints personalisieren und testen, z. B. Web-Apps, Mobile Apps, Desktop-Apps, Video-Konsolen, TV-verbundene Geräte, Smart-TVs, Kiosks, Geldautomaten, Sprachassistenten, IoT-Geräte usw.

Mit der Funktion **Code-basiertes Erlebnis** können Sie eingehende Erlebnisse mit einem einfachen und intuitiven, nicht visuellen Editor definieren. Sie können damit unabhängig vom Anwendungstyp bestimmte Elemente an einzelnen und detaillierteren Stellen Ihrer Apps oder Web-Seiten einfügen und bearbeiten, anstatt Änderungen an einem gesamten Inhalt vorzunehmen.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

Wählen Sie unter [Kampagne erstellen](../campaigns/create-campaign.md#configure) die Option **Code-basiertes Erlebnis (Beta)** als Aktion und legen Sie die Grundeinstellungen fest.

>[!NOTE]
>
>Wenn Sie zum ersten Mal ein Web-Erlebnis erstellen, stellen Sie sicher, dass Sie die in [diesem Abschnitt](code-based-prerequisites.md) beschriebenen Voraussetzungen befolgen.

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
<a href="code-based-prerequisites.md"><strong>Voraussetzungen</strong></a>
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
<td>
<a href="create-code-based.md#edit-code">
<img alt="Validierung" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="create-code-based.md#edit-code"><strong>Code bearbeiten</strong></a>
</div>
<p>
</td>
</tr></table>



<!--[Learn how to create a code-based campaign in this video](#video)-->

## Verwendung von Code-basierten anstelle von anderen Kanälen {#code-based-vs-other-channels}

### Code-basierte und andere Kanäle im Vergleich

Wann sollte anstelle der anderen [!DNL Journey Optimizer]-Kanäle ein Code-basierter Kanal verwendet werden?

* Sie können Code-basierte Erlebnisse jederzeit verwenden, wenn nicht über einen Webbrowser oder eine Mobile App auf Ihre digitale Eigenschaft zugegriffen wird. In den letzteren Fällen sollten Sie lieber den Kanal [!DNL Journey Optimizer] [Web-Kanal](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} verwenden.

* Sie können den Code-basierten Kanal als Alternative zum Web-Kanal von [!DNL Journey Optimizer] verwenden, wenn Ihre Webseite nicht in den [Web-Designer](../web/edit-web-content.md#work-with-web-designer){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} geladen werden kann, der das visuelle Authoring für den Web-Kanal ermöglicht.

* Sie können den Code-basierten Kanal auch als Alternative zu den Web- oder In-App-Kanälen von [!DNL Journey Optimizer] verwenden, falls Sie über eine API-basierte Headless- oder Server-seitige Implementierung verfügen.

### Code-basierte Kanäle und Web-Kanäle im Vergleich

Um Web-Anwendungsfälle auszuführen, können Sie entweder den Web-Kanal oder das Code-basierte Erlebnis verwenden. Je nach Kontext eignet sich ein Erlebnis jedoch meist besser als das andere. Die wichtigsten Unterschiede sind unten aufgeführt, sodass Sie eine fundierte Entscheidung darüber treffen können, wann Sie was verwenden.

**Web**
* Bearbeiten Sie Ihre Inhalte mithilfe des Visual Editors [Web-Designer](../web/edit-web-content.md#work-with-web-designer){target="_blank"}.
* Dazu benötigen Sie das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* Mit dem Web-Kanal können Sie alles auf Ihrer Seite ändern. Außerdem bietet er eine vordefinierte Liste von Aktionen, mit denen Sie Änderungen vornehmen können. [Weitere Informationen](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* Er lässt sich schnell einrichten und ausführen.
* Er ist auf Marketing-Fachleute ausgerichtet.

**Code-basiertes Erlebnis**
* Bearbeiten Sie Ihren Inhalt mit dem [Ausdruckseditor](create-code-based.md#edit-code).
* Das Code-basierte Erlebnis erfordert vorherige Entwicklungsarbeiten an Ihrer Implementierung, um sicherzustellen, dass Ihre Oberflächen die von [!DNL Journey Optimizer] für diese Oberflächen veröffentlichten Inhalte interpretieren und bereitstellen können. [Weitere Informationen](#surface-definition)
* Dies erfordert mehr Planung, und es können nur die von den Entwicklungspersonen festgelegten Punkte geändert werden. Daher müssen die Komponenten (Startseiten-Banner, Hero-Bild, Menüleiste usw.) auf den Oberflächen, die für die Personalisierung oder Tests geändert werden müssen, unbedingt festgelegt werden. Erstellen Sie zusammen mit Ihrem Entwicklungs-Team die für diese Änderungen erforderliche Implementierung.
* So können Sie JSON-Code-Inhalte verwenden.
* Es ist auf Entwicklungspersonen ausgerichtet.

## Funktionsweise {#how-it-works}

>[!CAUTION]
>
>Diese Funktion richtet sich an Entwicklungspersonen und/oder erfahrene Benutzerinnen und Benutzer. Sie kann von Marketing-Fachleuten mit einiger Erfahrung im Schreiben von Code verwendet werden, sofern die Implementierungen und die Ersteinrichtung der Oberflächen von Ihrem Entwicklungs-Team durchgeführt werden.

Damit Sie Ihren Inhalt mit der Funktion [!DNL Journey Optimizer] Code-basiertes Erlebnis bearbeiten können, müssen Ihre Seiten oder Apps entsprechend ausgerüstet sein. Dazu müssen Sie zuerst die einzelnen Stellen („[Oberflächen](#surface-definition)“ genannt) festlegen, an denen Sie Inhalte einfügen oder ersetzen möchten<!--HOW??-->.

>[!NOTE]
>
>Derzeit können nur HTML- und JSON-Inhalte mit einer Oberfläche verknüpft werden. <!--WILL COME LATER: text, image or another format depending on the application-->

Die wichtigsten Schritte zur Implementierung einer Code-basierten Kampagne:

1. Definieren Sie eine [Oberfläche](#surface-definition); also den Ort, zu dem Sie Ihr Code-basiertes Erlebnis hinzufügen möchten, und erstellen Sie mithilfe dieser Oberfläche eine Kampagne in [!DNL Journey Optimizer]. [Weitere Informationen](create-code-based.md#create-code-based-campaign)

1. Erstellen Sie ein Erlebnis, indem Sie mit dem [!DNL Journey Optimizer]-Ausdruckseditor Inhalte für die ausgewählte Oberfläche angeben. [Weitere Informationen](create-code-based.md#edit-code)

1. Ihr App-Implementierungs-Team erstellt explizite API- oder SDK-Aufrufe, um Inhalte für die benannten Oberflächen abzurufen, z. B. „Bannertext“ oder „Empfehlungsablage 1“, oder nicht UI-bezogene Entscheidungspunkte in einer Anwendung, z. B. „Suchalgorithmusparameter“. In diesem Fall ist das Implementierungs-Team für das Rendern oder die anderweitige Interpretation und die Bearbeitung des zurückgegebenen Inhalts verantwortlich.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## Was ist eine Oberfläche? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definieren einer Code-basierten Erlebnisoberfläche"
>abstract="Eine Code-basierte Oberfläche ist eine Entität, die für Benutzer- oder Systeminteraktionen entwickelt wurde und durch einen URI eindeutig gekennzeichnet ist."

Eine **Code-basierte Erlebnisoberfläche** ist jede Entität, die für Benutzer- oder Systeminteraktionen entwickelt wurde.<!--ask Robert to explain further--> und durch einen **URI** eindeutig gekennzeichnet ist.

Mit anderen Worten, eine Oberfläche kann als Container auf jeder Hierarchieebene mit einer vorhandenen Entität (Touchpoint) betrachtet werden.<!--good idea to illustrate how it can be seen, but to clarify-->

* Dabei kann es sich um eine Webseite, eine Mobile App, eine Desktop-App, einen bestimmten Inhaltsspeicherort innerhalb einer größeren Entität (z. B. eine `div`) oder ein nicht standardmäßiges Anzeigemuster (z. B. ein Kiosk oder ein Desktop-Programm-Banner) handeln.<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Für Nicht-Anzeigen oder abstrakte Anzeigen (z. B. für Dienste bereitgestellte JSON-Blobs) kann sie auch auf bestimmte Teile von Inhalts-Containern erweitert werden.

* Es kann sich auch um eine Platzhalteroberfläche handeln, die einer Vielzahl von Client-Oberflächendefinitionen entspricht (z. B. kann die Position eines Hero-Bilds auf jeder Seite Ihrer Website in einen Oberflächen-URI wie web://mydomain.com/*#hero_image übersetzt werden).

Grundsätzlich besteht ein Oberflächen-URI aus mehreren Abschnitten:
1. **Typ**: Web, Mobile App, Dienst, Kiosk, tvcd usw.
1. **Eigenschaft**: Domain oder App-Paket
1. **Pfad**: Seite/App-Aktivität ± Position auf der Seite/App-Aktivität <!--to clarify-->

In der folgenden Tabelle sind einige beispielhafte Definitionen von Oberflächen-URI für verschiedene Geräte aufgeführt.

| Typ | URI | Beschreibung |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | Stellt einen einzelnen Pfad und eine einzelne Seite einer Website dar. |
| Web | web://domain.com/path/page.html#element | Stellt ein einzelnes Element innerhalb einer bestimmten Seite einer bestimmten Domain dar. |
| Web | web://domain.com/*#element | Platzhalteroberfläche - stellt ein einzelnes Element auf jeder Seite unter einer bestimmten Domain dar. |
| Desktop | desktop://com.vendor.bundle | Stellt eine bestimmte Desktop-Anwendung dar. |
| Desktop | desktop://com.vendor.bundle#element | Stellt ein bestimmtes Element in einer Anwendung dar, z. B. eine Schaltfläche, ein Menü, ein Hero-Banner usw. |
| iOS-App | mobileapp://com.vendor.bundle | Stellt eine bestimmte mobile App für eine Plattform dar, in diesem Fall die iOS-App. |
| iOS-App | mobileapp://com.vendor.bundle/activity | Stellt eine bestimmte Aktivität (Ansicht) in einer mobilen App dar. |
| iOS-App | mobileapp://com.vendor.bundle/activity#element | Stellt ein bestimmtes Element innerhalb einer Aktivität dar, z. B. eine Schaltfläche oder ein anderes Ansichtselement. |
| Android-App | mobileapp://com.vendor.bundle | Stellt eine bestimmte Mobile App für eine einzelne Plattform dar, in diesem Fall eine Android-App. |
| tvOS-App | tvos://com.vendor.bundle | Stellt eine bestimmte tvOS-App dar. |
| TV-App | tvcd://com.vendor.bundle | Stellt eine bestimmte mit einem Smart TV- oder TV-Gerät verbundene Geräteanwendung dar – Bundle-ID. |
| Service | service://servicename | Stellt einen Server-seitigen Prozess oder eine andere manuelle Entität dar. |
| Kiosk | kiosk://location/screen | Beispiel potenzieller zusätzlicher Oberflächentypen, die leicht hinzugefügt werden können. |
| ATM | atm://location/screen | Beispiel potenzieller zusätzlicher Oberflächentypen, die leicht hinzugefügt werden können. |
