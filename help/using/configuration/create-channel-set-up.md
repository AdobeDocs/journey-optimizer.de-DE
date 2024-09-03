---
solution: Journey Optimizer
product: journey optimizer
title: Einrichten eines Kanals
description: Erfahren Sie, wie Sie einen Kanal einrichten
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Kanal, Oberfläche, technisch, Parameter, Optimizer
source-git-commit: 549efb9e12dccedb27335553194e09deab09a35f
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 4%

---

# Einrichten eines Kanals {#set-mobile-ios}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_javascript_code"
>title="JavaScript-Code"
>abstract="Das head -Tag enthält wichtige Metadaten und Ressourcen, die vor dem Hauptinhalt Ihrer Webseite geladen werden. Durch die Platzierung von Code in diesem Abschnitt wird sichergestellt, dass er frühzeitig initialisiert und ausgeführt wird, sodass Ihre Webseite effizient geladen und funktioniert. Durch Hinzufügen von Code zum Kopfabschnitt können Sie die Struktur, die Leistung und das gesamte Benutzererlebnis Ihrer Site verbessern."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_token"
>title="Abrufen des Geräte-Tokens"
>abstract="Um sicherzustellen, dass das Push-Token des Geräts ordnungsgemäß mit Ihrem Adobe Experience Platform-Profil synchronisiert wird, müssen Sie den folgenden Code in Ihre Anwendung integrieren. Diese Integration ist für die Aufrechterhaltung aktueller Kommunikationskapazitäten und die Sicherstellung eines nahtlosen Benutzererlebnisses unerlässlich."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_xcode"
>title="Starten der Anwendung aus Xcode"
>abstract="Um Ihr Push-Token zu erhalten, starten Sie zunächst Ihre Anwendung mit Xcode. Nachdem die Anwendung gestartet wurde, starten Sie sie neu, um sicherzustellen, dass der Validierungsprozess abgeschlossen ist. Adobe stellt dann Ihr Push-Token als Teil der Überprüfungsergebnisse bereit. Dieses Token ist für die Aktivierung von Push-Benachrichtigungen unerlässlich und wird angezeigt, sobald die Einrichtung erfolgreich validiert wurde."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_push_certificate_fcm"
>title="Bereitstellen eines Push-Zertifikats"
>abstract="Ziehen Sie die .json-Datei mit dem privaten Schlüssel per Drag-and-Drop in den Arbeitsbereich. Diese Datei enthält Authentifizierungsinformationen, die für die sichere Integration und Kommunikation zwischen Ihrer Anwendung und dem Server erforderlich sind."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_certificate"
>title="Bereitstellen eines Push-Zertifikats"
>abstract="Die .p8-Schlüsseldatei enthält einen privaten Schlüssel, mit dem Ihre App bei den Servern von Apple für sichere Push-Benachrichtigungen authentifiziert wird. Sie können diesen Schlüssel über die Seite &quot;Zertifikate&quot;, &quot;Kennungen&quot;und &quot;Profile&quot;in Ihrem Entwicklerkonto erwerben."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_key_id"
>title="Schlüssel-ID"
>abstract="Die Schlüssel-ID, eine 10-stellige Zeichenfolge, die bei der Erstellung des p8-Authentifizierungsschlüssels zugewiesen wurde, befindet sich auf der Registerkarte **Schlüssel** auf der Seite &quot;Zertifikate&quot;, &quot;Kennungen&quot;und &quot;Profile&quot;in Ihrem Entwicklerkonto."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_team_id"
>title="Team-ID"
>abstract="Die Team-ID, ein string -Wert, der zur Identifizierung Ihres Teams verwendet wird, befindet sich auf der Registerkarte **Mitgliedschaft** in Ihrem Entwicklerkonto."

Diese Konfiguration vereinfacht die schnelle Konfiguration von Marketing-Kanälen, sodass alle wichtigen Ressourcen in den Experience Platform-, Journey Optimizer- und Datenerfassungs-Apps verfügbar sind. Dadurch kann Ihr Marketing-Team schnell mit der Erstellung von Kampagnen und Journey beginnen.

1. Klicken Sie auf der Journey Optimizer-Homepage auf **[!UICONTROL Starten]** auf der Karte **[!UICONTROL Mobil- und Webkanäle einrichten]** .

   ![](assets/guided-setup-config-1.png)

1. Erstellen Sie eine **[!UICONTROL Neue]** -Konfiguration.

   Wenn Sie bereits über vorhandene Konfigurationen verfügen, können Sie eine auswählen oder eine neue Konfiguration erstellen.

   ![](assets/guided-setup-config-2.png)

1. Geben Sie einen **[!UICONTROL Namen]** für Ihre neue Konfiguration ein und wählen Sie Ihren **[!UICONTROL Datastraam]** aus oder erstellen Sie ihn. Dieser **[!UICONTROL Name]** wird für jede automatisch erstellte Ressource verwendet.

1. Wenn Ihr Unternehmen über mehrere Datenspeicher verfügt, wählen Sie bitte einen aus den vorhandenen Optionen aus. Wenn Sie keinen Datastream haben, wird einer automatisch erstellt.

1. Wählen Sie Ihre Plattform aus und klicken Sie auf **[!UICONTROL Ressourcen automatisch erstellen]**.

1. Um den Einrichtungsprozess zu optimieren, werden die erforderlichen Ressourcen automatisch erstellt, um Ihnen die ersten Schritte zu erleichtern. Dazu gehören die Erstellung einer neuen **[!UICONTROL Mobile Tag-Eigenschaft]** und die Installation von Erweiterungen.

[Erfahren Sie mehr über die automatisch generierten Ressourcen](set-mobile-config.md#auto-create-resources)

1. Nachdem die Ressourcengenerierung abgeschlossen ist, befolgen Sie die Anweisungen in der Benutzeroberfläche, um Ihre SDKs und Kanäle einzurichten und zu validieren.

1. Geben Sie nach Abschluss der Konfiguration die automatisch generierte **[!UICONTROL Kanalkonfiguration]** für die Teammitglieder frei, die für die Erstellung von Journey und Kampagnen verantwortlich sind.

   ![](assets/guided-setup-config-ios-8.png){zoomable="yes"}

1. Sie können jetzt auf der Kampagnen- oder Journey-Oberfläche auf die **[!UICONTROL Kanalkonfiguration]** verweisen, was eine nahtlose Verbindung zwischen Ihrer Einrichtung und der Ausführung von zielgerichteten Journey und Kampagnen für Ihre Zielgruppe ermöglicht.

## Ändern einer vorhandenen mobilen Konfiguration {#reconnect}

Nachdem Sie Ihre Konfiguration erstellt haben, können Sie sie jederzeit einfach erneut aufrufen, um zusätzliche Kanäle hinzuzufügen oder weitere Anpassungen an Ihre Anforderungen vorzunehmen

1. Klicken Sie auf der Journey Optimizer-Homepage auf **[!UICONTROL Starten]** auf der Karte **[!UICONTROL Mobil- und Webkanäle einrichten]** .

   ![](assets/guided-setup-config-1.png)

1. Wählen Sie **[!UICONTROL Vorhandenes]** und wählen Sie Ihre vorhandene **[!UICONTROL Tag-Eigenschaft]** aus der Dropdown-Liste aus.

   ![](assets/guided-setup-config-ios-9.png)

1. Beim Zugriff auf Ihre bestehende Konfiguration müssen Sie eine erneute Verbindung mit Adobe Assurance herstellen. Klicken Sie im SDK-Setup-Menü auf **[!UICONTROL Neu verbinden]**.

   ![](assets/guided-setup-config-ios-10.png)

1. Wählen Sie Ihr Gerät aus der Dropdownliste **[!UICONTROL Verfügbare Geräte]** aus und klicken Sie auf **[!UICONTROL Verbinden]**.

   ![](assets/guided-setup-config-ios-11.png){zoomable="yes"}

1. Jetzt können Sie Ihre Konfiguration nach Bedarf aktualisieren.
