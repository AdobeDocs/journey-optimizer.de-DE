---
title: Erste Schritte mit code-basierten Erlebnissen
description: Informationen zu code-basierten Erlebnissen in Journey Optimizer
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: f271aa457d2f8b7e66e58692b613d80c6e6b3adb
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 7%

---

# Erste Schritte mit dem code-basierten Kanal {#get-sarted-code-based}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* **[Erste Schritte mit dem code-basierten Kanal](get-started-code-based.md)**
* [Codebasierte Voraussetzungen](code-based-prerequisites.md)
* [Codebasierte Implementierungsbeispiele](code-based-implementation-samples.md)
* [Codebasierte Erlebnisse erstellen](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Der code-basierte Erlebniskanal ist derzeit als Beta-Version verfügbar, um nur Benutzer auszuwählen. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

[!DNL Journey Optimizer] ermöglicht Ihnen, die Erlebnisse, die Sie Ihren Kunden bereitstellen möchten, für alle Touchpoints zu personalisieren und zu testen, z. B. Web-Apps, mobile Apps, Desktop-Apps, Video-Konsolen, TV-verbundene Geräte, Smart-TVs, Kiosks, ATMs, Sprachassistenten, IoT-Geräte usw.

Mit dem **code-basiertes Erlebnis** -Funktion können Sie eingehende Erlebnisse mit einem einfachen und intuitiven nicht visuellen Editor definieren. Sie können damit bestimmte Elemente an einzelnen und detaillierteren Speicherorten Ihrer Apps oder Webseiten einfügen und bearbeiten, unabhängig vom Anwendungstyp - anstatt Änderungen an einem gesamten Inhalt vorzunehmen.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

Wenn Sie [Kampagne erstellen](../campaigns/create-campaign.md#configure)auswählen **Codebasiertes Erlebnis (Beta)** als Aktion definieren und grundlegende Einstellungen definieren.

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
<a href="create-code-based.md#create-code-based-campaign"><strong>Codebasiertes Erlebnis erstellen</strong></a>
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

## Verwendung von code-basierten und anderen Kanälen {#code-based-vs-other-channels}

### Codebasierte und andere Kanäle

Verwendung des code-basierten Kanals anstelle des anderen [!DNL Journey Optimizer] Kanäle?

* Sie können Code-basierte Erlebnisse jederzeit verwenden, wenn nicht über einen Webbrowser oder eine mobile App auf Ihre digitale Eigenschaft zugegriffen wird - in Fällen, in denen Sie die [!DNL Journey Optimizer] [Webkanal](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} -Kanal.

* Sie können den code-basierten Kanal als Alternative zum [!DNL Journey Optimizer] Webkanal , wenn Ihre Website nicht in die [Web Visual Editor](../web/author-web.md){target="_blank"} or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} , das visuelles Authoring für den Webkanal ermöglicht.

* Sie können den code-basierten Kanal auch als Alternative zum [!DNL Journey Optimizer] Web- oder In-App-Kanäle, falls Sie über eine API-basierte, Headless- oder serverseitige Implementierung verfügen.

### Codebasierte im Vergleich zum Webkanal

Um Webanwendungsfälle auszuführen, können Sie entweder den Webkanal oder das code-basierte Erlebnis verwenden. Je nach Kontext ist jedoch eines der Erlebnisse angemessener als der andere. Die wichtigsten Unterschiede sind unten aufgeführt, sodass Sie eine fundierte Entscheidung darüber treffen können, wann Sie sie verwenden möchten.

**Web**
* Bearbeiten Sie den Inhalt mithilfe der [Visual Editor](../web/author-web.md){target="_blank"}.
* Sie benötigen die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* Der Webkanal ermöglicht es Ihnen, alles auf Ihrer Seite zu ändern und verfügt über eine vordefinierte Liste von Aktionen, die Sie zum Vornehmen von Änderungen verwenden können. [Weitere Informationen](../web/author-web.md){target="_blank"}
* Es ist einfach einzurichten und schnell zu gehen.
* Es ist auf Marketingexperten ausgerichtet.

**Codebasiertes Erlebnis**
* Bearbeiten Sie den Inhalt mithilfe der [Ausdruckseditor](create-code-based.md#edit-code).
* Das code-basierte Erlebnis erfordert vorherige Entwicklungsarbeiten an Ihrer Implementierung, um sicherzustellen, dass Ihre Oberflächen die Inhalte interpretieren und bereitstellen können, die auf der Edge-Seite von [!DNL Journey Optimizer] für diese Oberflächen. [Weitere Informationen](#surface-definition)
* Es erfordert mehr Planung und kann nur die Dinge ändern, die Entwickler angeben. Daher ist es wichtig, die Komponenten zu identifizieren (Startseiten-Banner, Hero-Bild, Menüleiste usw.) auf den Oberflächen, die für Personalisierung oder Tests geändert werden müssen, und wenden Sie sich an Ihr Entwicklungsteam, um die für die Bearbeitung dieser Änderungen erforderliche Implementierung zu erstellen.
* Damit können Sie JSON-Code-Inhalte verwenden.
* Entwickler-Persona-fokussiert.

## Funktionsweise {#how-it-works}

>[!CAUTION]
>
>Diese Funktion richtet sich an Entwickler und/oder erfahrene Benutzer. Sie kann von Marketingexperten mit einigen Fähigkeiten zum Schreiben von Code verwendet werden, sofern die Implementierungen der Oberfläche und die Ersteinrichtung von Ihrem Entwicklungsteam verarbeitet werden.

So bearbeiten Sie Ihren Inhalt mit [!DNL Journey Optimizer] Code-basierte Erlebnisfunktion verwenden, müssen Ihre Seiten oder Apps instrumentiert werden. Dazu müssen Sie die einzelnen Orte (mit dem Namen[Oberflächen](#surface-definition)&quot;), wo Sie Inhalte einfügen oder ersetzen möchten<!--HOW??-->.

>[!NOTE]
>
>Derzeit kann der mit einer Oberfläche verknüpfte Inhalt nur HTML oder JSON sein. <!--WILL COME LATER: text, image or another format depending on the application-->

Die wichtigsten Schritte zur Implementierung einer code-basierten Kampagne sind:

1. Definieren Sie eine [Oberfläche](#surface-definition); dies ist im Grunde der Ort, an dem Sie Ihr code-basiertes Erlebnis hinzufügen und eine Kampagne in [!DNL Journey Optimizer] mit dieser Oberfläche. [Weitere Informationen](create-code-based.md#create-code-based-campaign)

1. Erstellen Sie mithilfe der [!DNL Journey Optimizer] Ausdruckseditor. [Weitere Informationen](create-code-based.md#edit-code)

1. Ihr App-Implementierungsteam sendet explizite API- oder SDK-Aufrufe, um Inhalte für die benannten Oberflächen abzurufen, z. B. &quot;Bannertext&quot;oder &quot;Recommendations Tray 1&quot;oder nicht UI-bezogene Entscheidungspunkte in einer Anwendung, z. B. &quot;Suchalgorithmparameter&quot;. In diesem Fall ist das Implementierungsteam für das Rendern oder anderweitige Interpretation und die Bearbeitung des zurückgegebenen Inhalts verantwortlich.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## Was ist eine Oberfläche? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definieren einer code-basierten Erlebnisoberfläche"
>abstract="Eine code-basierte Oberfläche ist eine Entität, die für Benutzer- oder Systeminteraktionen entwickelt wurde und durch einen URI eindeutig identifiziert wird."

A **Code-basierte Erlebnisoberfläche** ist jede Entität, die für Benutzer- oder Systeminteraktionen entwickelt wurde.<!--ask Robert to explain further-->, der durch eine **URI**.

Mit anderen Worten, eine Oberfläche kann auf jeder Hierarchieebene als Container mit einer vorhandenen Entität (Touchpoint) betrachtet werden.<!--good idea to illustrate how it can be seen, but to clarify-->

* Dabei kann es sich um eine Webseite, eine mobile App, ein Desktop-Programm, einen bestimmten Inhaltsspeicherort innerhalb einer größeren Entität handeln (z. B. eine `div`) oder einem nicht standardmäßigen Anzeigemuster (z. B. einem Kiosk oder einem Desktop-Programm-Banner).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Sie kann auch auf bestimmte Teile von Inhalts-Containern für Zwecke der Nicht-Anzeige oder abstrahierten Anzeige ausgedehnt werden (z. B. JSON-Blobs, die für Dienste bereitgestellt werden).

* Es kann sich auch um eine Platzhalteroberfläche handeln, die einer Vielzahl von Client-Oberflächendefinitionen entspricht (z. B. könnte eine Hero-Image-Position auf jeder Seite Ihrer Website in einen Oberflächen-URI wie web://mydomain.com/*#hero_image übersetzt werden).

Grundsätzlich besteht ein Oberflächen-URI aus mehreren Abschnitten:
1. **Typ**: web, mobileapp, service, kiosk, tvcd usw.
1. **Eigenschaft**: Domäne oder App-Paket
1. **Pfad**: Seite/App-Aktivität ± Position auf der Seite/App-Aktivität <!--to clarify-->

In der folgenden Tabelle sind einige Beispiele für die Definition von Oberflächen-URIs für verschiedene Geräte aufgeführt.

| Typ | URI | Beschreibung |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | Stellt einen einzelnen Pfad und eine einzelne Seite einer Website dar. |
| Web | web://domain.com/path/page.html#element | Stellt ein einzelnes Element innerhalb einer bestimmten Seite einer bestimmten Domäne dar. |
| Web | web://domain.com/*#element | Platzhalteroberfläche - stellt ein einzelnes Element auf jeder Seite unter einer bestimmten Domäne dar. |
| Desktop | desktop://com.vendor.bundle | Stellt ein bestimmtes Desktop-Programm dar. |
| Desktop | desktop://com.vendor.bundle#element | Stellt ein bestimmtes Element in einer Anwendung dar, z. B. eine Schaltfläche, ein Menü, ein Hero-Banner usw. |
| iOS-App | mobileapp://com.vendor.bundle | Stellt eine bestimmte Mobile App für eine Plattform dar, in diesem Fall die iOS-App. |
| iOS-App | mobileapp://com.vendor.bundle/activity | Stellt eine bestimmte Aktivität (Ansicht) in einer Mobile App dar. |
| iOS-App | mobileapp://com.vendor.bundle/activity#element | Stellt ein bestimmtes Element innerhalb einer Aktivität dar, z. B. eine Schaltfläche oder ein anderes Ansichtselement. |
| Android-App | mobileapp://com.vendor.bundle | Stellt eine bestimmte Mobile App für eine einzelne Plattform dar - in diesem Fall eine Android-App. |
| tvOS-App | tvos://com.vendor.bundle | Stellt eine bestimmte tvOS-App dar. |
| TV-Programm | tvcd://com.vendor.bundle | Stellt eine bestimmte mit Smart TV oder TV verbundene Geräteanwendung dar - Bundle-ID. |
| Service | service://servicename | Stellt einen serverseitigen Prozess oder eine andere manuelle Entität dar. |
| Kiosk | kiosk://location/screen | Beispiel potenzieller zusätzlicher Oberflächentypen, die leicht hinzugefügt werden können. |
| ATM | atm://location/screen | Beispiel potenzieller zusätzlicher Oberflächentypen, die leicht hinzugefügt werden können. |