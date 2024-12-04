---
title: Code-basierte Oberfläche
description: Erfahren Sie, was eine Code-basierte Erlebnisoberfläche ist
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 07ec74fb-7fbc-48c6-a8fc-f58f24a60723
source-git-commit: f247ef3c3cd7d1d270893ae6bf88fadf3932d05e
workflow-type: ht
source-wordcount: '728'
ht-degree: 100%

---

# Code-basierte Erlebnisoberflächen {#code-based-surface}

## Was ist eine Oberfläche? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="Hinzufügen des Oberflächen-URI für Ihre Komponente"
>abstract="Wenn Ihre Implementierung nicht für Web, iOS oder Android geeignet ist oder Sie bestimmte URIs als Ziel auswählen müssen, geben Sie einen Oberflächen-URI ein, bei dem es sich um eine eindeutige Kennung handelt, die an die Entität weitergeleitet wird, bei der Sie Ihr Erlebnis bereitstellen möchten. Stellen Sie sicher, dass Sie einen Oberflächen-URI eingeben, der mit dem in Ihrer eigenen Implementierung verwendeten URI übereinstimmt."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="Erstellen einer Konfiguration für ein Code-basiertes Erlebnis für andere Plattformen"

Eine Code-basierte **Erlebnisoberfläche** ist jede Entität, die für Benutzer- oder Systeminteraktionen entwickelt wurde. Sie ist durch einen [URI](#surface-uri) eindeutig gekennzeichnet. Die Oberfläche wird in der [Implementierung der Anwendung](code-based-prerequisites.md#implementation-prerequisites) angegeben und muss mit der in der [Code-basierten Erlebniskanalkonfiguration](code-based-configuration.md) referenzierten Oberfläche übereinstimmen.

Eine Oberfläche kann als Container auf jeder Hierarchieebene mit einer vorhandenen Entität (Touchpoint) betrachtet werden.

* Dabei kann es sich um eine Webseite, eine Mobile App, eine Desktop-App, einen bestimmten Inhaltsspeicherort innerhalb einer größeren Entität (z. B. eine `div`) oder ein nicht standardmäßiges Anzeigemuster (z. B. ein Kiosk oder ein Desktop-Programm-Banner) handeln.<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Für Nicht-Anzeigen oder abstrakte Anzeigen (z. B. für Dienste bereitgestellte JSON-Blobs) kann sie auch auf bestimmte Teile von Inhalts-Containern erweitert werden.

* Es kann sich auch um eine Platzhalteroberfläche handeln, die einer Vielzahl von Client-Oberflächendefinitionen entspricht (z. B. kann die Position eines Hero-Bilds auf jeder Seite Ihrer Website in einen Oberflächen-URI wie web://mydomain.com/*#hero_image übersetzt werden).

## Oberflächenkennung {#surface-uri}

Ein **Oberflächen-URI** dient als präzise Kennung, die innerhalb einer Anwendung zu unterschiedlichen Benutzeroberflächen-Elementen oder -Komponenten führt. Grundsätzlich besteht ein Oberflächen-URI aus mehreren Abschnitten:

1. **Typ**: Web, Mobile App, ATM, Kiosk, tvcd, Dienst
1. **Eigenschaft**: Seiten-URL oder App-Paket
1. **Container**: Speicherort auf der Seite/App-Aktivität

In der folgenden Tabelle sind einige beispielhafte Definitionen eines Oberflächen-URI für verschiedene Geräte aufgeführt.

**Web und Mobil**

| Typ | URI | Beschreibung |
| --------- | ----------- | ------- | 
| Web | `web://domain.com/path/page.html#element` | Stellt ein einzelnes Element innerhalb einer bestimmten Seite einer bestimmten Domain dar, bei dem ein Element wie in den folgenden Beispielen eine Bezeichnung sein kann: hero_banner, top_nav, menu, footer. |
| iOS-App | `mobileapp://com.vendor.bundle/activity#element` | Stellt ein bestimmtes Element innerhalb der Aktivität einer nativen App dar, z. B. eine Schaltfläche oder ein anderes Ansichtselement. |
| Android-App | `mobileapp://com.vendor.bundle/#element` | Stellt ein bestimmtes Element in einer nativen App dar. |

**Andere Gerätetypen**

| Typ | URI | Beschreibung |
| --------- | ----------- | ------- | 
| Desktop | `desktop://com.vendor.bundle/#element` | Stellt ein bestimmtes Element in einer Anwendung dar, z. B. eine Schaltfläche, ein Menü, ein Hero-Banner usw. |
| TV-App | `tvcd://com.vendor.bundle/#element` | Stellt ein bestimmtes Element in einer mit einem Smart TV- oder TV-Gerät verbundenen Geräteanwendung dar – Bundle-ID. |
| Service | `service://servicename/#element` | Stellt einen Server-seitigen Prozess oder eine andere manuelle Entität dar. |
| Kiosk | `kiosk://location/screen#element` | Beispiel potenzieller zusätzlicher Oberflächentypen, die leicht hinzugefügt werden können. |
| ATM | `atm://location/screen#element` | Beispiel potenzieller zusätzlicher Oberflächentypen, die leicht hinzugefügt werden können. |

**Platzhalteroberfläche**

| Typ | URI | Beschreibung |
| --------- | ----------- | ------- | 
| Platzhalter-Web | `wildcard:web://domain.com/*#element` | Platzhalteroberfläche – stellt ein einzelnes Element auf jeder Seite unter einer bestimmten Domain dar. |
| Platzhalter-Web | `wildcard:web://*domain.com/*#element` | Platzhalteroberfläche – stellt ein einzelnes Element auf jeder Seite unter allen Domains dar, die auf „domain.com“ enden. |

## URI-Komposition {#uri-composition}

In [!DNL Journey Optimizer] unterstützt der Code-basierte Erlebniskanal zwei Arten von Kundenimplementierungen:

* Basierend auf dem [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} für Ihre Websites oder dem [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} für Ihre Apps,
* Server-seitig oder hybrid mit [AEP Edge Network Server APIs](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de){target="_blank"}.

>[!NOTE]
>
>Weitere Informationen zu Implementierungsvoraussetzungen finden Sie in [diesem Abschnitt](code-based-prerequisites.md#implementation-prerequisites).

Mithilfe Code-basierter Erlebnisse können Sie Inhalte an granularen Speicherorten ändern, <!--(such as a specific location on a page, or inside a mobile native app)-->die [!DNL Journey Optimizer] anhand von [Oberflächen-URIs](#surface-uri) eindeutig identifiziert werden.

Diese Oberflächen-URIs werden je nach Implementierungsmethode zusammengestellt und verarbeitet:

* **Web-/Mobile-SDK**: Die Web-/Mobile-Entwicklerinnen bzw. -entwickler müssen diese granularen Speicherorte als einfache Zeichenfolgen definieren, da das Web-/Mobile-SDK in der Lage ist, den Oberflächen-URI basierend auf der aktuellen URL/App-ID und der Speicherortzeichenfolge automatisch zu erstellen.

* **Edge Network-APIs**: Die App-/Seitenentwicklerinnen bzw. -entwickler müssen vollständige Oberflächen-URIs definieren, die den vollständigen Pfad und Speicherort enthalten, an dem der Inhalt verwendet wird, da die vollständigen URIs für diese Art der Implementierung erforderlich sind.

Daher haben Sie beim Erstellen einer [Code-basierte Erlebniskanalkonfiguration](code-based-configuration.md) zwei Möglichkeiten, die Oberfläche entsprechend der ausgewählten Plattform anzugeben:

* Bei den Plattformen **[!UICONTROL Web]**, **[!UICONTROL iOS]** und **[!UICONTROL Android]** müssen Sie die **URL/App-ID** und einen **Speicherort oder Pfad** eingeben, um die Oberfläche zusammenzustellen. Erfahren Sie mehr über die Konfiguration Code-basierter Erlebnisse für die Plattformen [Web](code-based-configuration.md#web) und [Mobile](code-based-configuration.md#mobile).

* Wenn die Plattform unter **[!UICONTROL Sonstige]** fällt, müssen Sie den vollständigen **Oberflächen-URI** eingeben, wie in den Beispielen [oben](#surface-uri) dargestellt. Erfahren Sie mehr über die Konfiguration Code-basierter Erlebnisse für [sonstige](code-based-configuration.md#other) Plattformen
