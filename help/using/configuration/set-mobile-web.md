---
solution: Journey Optimizer
product: journey optimizer
title: Web einrichten
description: Erfahren Sie, wie Sie Web-Konfigurationen konfigurieren und überwachen
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Kanal, Oberfläche, technisch, Parameter, Optimizer
hide: true
hidefromtoc: true
source-git-commit: 7a1f337e2bc257d8f0fa9bda17abdaff92a86de5
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 14%

---

# Webkonfiguration einrichten {#set-mobile-web}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_javascript_code"
>title="JavaScript-Code"
>abstract="Das head -Tag enthält wichtige Metadaten und Ressourcen, die vor dem Hauptinhalt Ihrer Webseite geladen werden. Durch die Platzierung von Code in diesem Abschnitt wird sichergestellt, dass er frühzeitig initialisiert und ausgeführt wird, sodass Ihre Webseite effizient geladen und funktioniert. Durch Hinzufügen von Code zum Kopfabschnitt können Sie die Struktur, die Leistung und das gesamte Benutzererlebnis Ihrer Site verbessern."

Diese Einrichtung erleichtert die schnelle Konfiguration von Marketing-Kanälen, sodass alle erforderlichen Ressourcen in Experience Platform, Journey Optimizer und der Datenerfassung sofort verfügbar sind. Dadurch kann Ihr Marketing-Team sofort mit der Erstellung von Kampagnen und Journeys beginnen.

## Neue Webeinrichtung erstellen {#new-setup}

1. Klicken Sie auf der Journey Optimizer-Homepage auf **[!UICONTROL Starten]** auf der Karte **[!UICONTROL Mobil- und Webkanäle einrichten]** .

   ![](assets/guided-setup-config-1.png)

1. Erstellen Sie eine **[!UICONTROL Neue]** -Konfiguration.

   Wenn Sie bereits über vorhandene Konfigurationen verfügen, können Sie eine auswählen oder eine neue Konfiguration erstellen.

   ![](assets/guided-setup-config-2.png)

1. Geben Sie einen **[!UICONTROL Namen]** für Ihre neue Konfiguration ein und wählen Sie Ihren **[!UICONTROL Datastraam]** aus oder erstellen Sie ihn. Dieser **[!UICONTROL Name]** wird für jede automatisch erstellte Ressource verwendet.

1. Wenn Ihr Unternehmen über mehrere Datenspeicher verfügt, wählen Sie bitte einen aus den vorhandenen Optionen aus. Wenn Sie keinen Datastream haben, wird einer automatisch erstellt.

1. Wählen Sie die Webplattform aus und klicken Sie auf **[!UICONTROL Ressourcen automatisch erstellen]**.

   ![](assets/guided-setup-config-5.png)

1. Um den Einrichtungsprozess zu optimieren, werden die erforderlichen Ressourcen automatisch erstellt, um Ihnen die ersten Schritte zu erleichtern.

   Nachfolgend finden Sie eine umfassende Liste aller automatisch generierten Ressourcen:

+++ Erstellte Ressourcen

   <table>
    <thead>
    <tr>
    <th><strong>Lösung</strong></th>
    <th><strong>Automatisch erstellte Ressourcen</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    </tr>
    <tr>
    <td>
    <p>Tags</p>
    </td>
    <td>
    <ul>
    <li>Mobile Tag-Eigenschaft</li>
    <li>Regeln</li>
    <li>Datenelemente</li>
    <li>Bibliothek</li>
    <li>Umgebungen (Staging, Produktion, Entwicklung)</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Tag-Erweiterungen</p>
    </td>
    <td>
    <ul>
    <li>Adobe Experience Platform Edge Network</li>
    <li>Adobe Journey Optimizer</li>
    <li>AEP-Sicherheit</li>
    <li>Einverständnis (mit aktivierten standardmäßigen Zustimmungsrichtlinien)</li>
    <li>Identität (mit Standard-ECID, mit standardmäßigen Stitching-Regeln)</li>
    <li>Core für Mobilgeräte</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Assurance</p>
    </td>
    <td>
    <p>Assurance-Sitzung</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Datenströme</p>
    </td>
    <td>
    <p>Datenspeicher mit Diensten</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Experience Platform</p>
    </td>
    <td>
    <ul>
    <li>Datensatz</li>
    <li>Schema</li>
    </ul>
    </td>
    </tr>
    </tbody>
    </table>

+++

1. Klicken Sie nach der Generierung der Ressourcen auf **[!UICONTROL Einrichten]** , um mit der Konfiguration Ihres SDK zu beginnen.

   ![](assets/guided-setup-config-web-1.png)

1. Fügen Sie den auf dem Bildschirm angezeigten Code in das Tag `<head>` Ihres Dokuments ein.

   ![](assets/guided-setup-config-web-2.png){zoomable="yes"}

1. Um Ihr SDK direkt in Ihrer Mobile App zu validieren, fügen Sie einfach Ihre Basis-URL ein.

   ![](assets/guided-setup-config-web-3.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Site starten und validieren]** aus, um Ihre Site zu verbinden.

   ![](assets/guided-setup-config-web-4.png){zoomable="yes"}

1. Geben Sie nach Abschluss der Konfiguration die automatisch generierte **[!UICONTROL mobile Webeigenschaft]** für die Teammitglieder frei, die für die Erstellung von Journey und Kampagnen verantwortlich sind.

   Die **[!UICONTROL mobile Webeigenschaft]** sollte in der Kampagnen- oder Journey-Benutzeroberfläche referenziert werden, sodass eine nahtlose Verbindung zwischen Ihrer Einrichtung und der Ausführung von zielgerichteten Journey und Kampagnen für Ihre Zielgruppe hergestellt werden kann.

   ![](assets/guided-setup-config-ios-8.png)

Sie können jetzt Webseiten mit der zuvor konfigurierten **[!UICONTROL mobilen Webeigenschaft]** erstellen. [Erfahren Sie, wie Sie eine Webseite erstellen](../web/create-web.md)

## Vorhandene Konfiguration ändern {#reconnect}

Nachdem Sie Ihre Konfiguration erstellt haben, können Sie sie jederzeit einfach erneut aufrufen, um zusätzliche Kanäle hinzuzufügen oder weitere Anpassungen an Ihre Anforderungen vorzunehmen

1. Klicken Sie auf der Journey Optimizer-Homepage auf **[!UICONTROL Starten]** auf der Karte **[!UICONTROL Mobil- und Webkanäle einrichten]** .

   ![](assets/guided-setup-config-1.png)

1. Wählen Sie **[!UICONTROL Vorhandenes]** und wählen Sie Ihre vorhandene **[!UICONTROL Tag-Eigenschaft]** aus der Dropdown-Liste aus.

   ![](assets/guided-setup-config-web-5.png)

1. Jetzt können Sie Ihre Konfiguration nach Bedarf aktualisieren.
