---
solution: Journey Optimizer
product: journey optimizer
title: Externe Integrationen aktivieren
description: Integrieren Sie externe Integrationen in den Prozess der Kanalerstellung, um Inhalte mit personalisierten und dynamischen Informationen anzureichern
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: Integration
hide: true
hidefromtoc: true
source-git-commit: e8512ddab2548c8b2156331c335632cde8686f80
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 1%

---

# Arbeiten mit Integrationen {#external-sources}

## Überblick

Die **Integrationen** ermöglicht die nahtlose Integration von Datenquellen von Drittanbietern in Adobe Journey Optimizer. Diese Funktion optimiert die Integration externer Daten und Inhaltsquellen in Ihre Kampagnen und ermöglicht es Ihnen, hochgradig personalisierte und dynamische Nachrichten über mehrere Kanäle hinweg bereitzustellen.

Sie können diese Funktion verwenden, um auf externe Daten zuzugreifen und Inhalte von Drittanbieter-Tools abzurufen, z. B.:

* **Prämienpunkte** aus Treuesystemen
* **Preisinformationen** für Produkte.
* **Produktempfehlungen** von Empfehlungs-Engines.
* **Logistische Updates** wie Versandstatus.

## Konfigurieren der Integration {#configure}

Als Administrator können Sie externe Integrationen einrichten, indem Sie die folgenden Schritte ausführen:

1. Navigieren Sie zum Abschnitt **[!UICONTROL Konfigurationen]** im linken Menü und klicken Sie auf **[!UICONTROL Karte]** Integrationen **[!UICONTROL auf]**.

   Klicken Sie dann auf **[!UICONTROL Integration erstellen]**, um eine neue Konfiguration zu starten.

   ![](assets/external-integration-config-1.png)

1. Geben Sie einen **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** für Ihre Integration an.

   >[!NOTE]
   >
   >Diese Felder dürfen keine Leerzeichen enthalten.

1. Geben Sie den API-Endpunkt **[!UICONTROL URL]** ein, der Pfadparameter mit Variablen enthalten kann, die mithilfe von Kennzeichnungen und Standardwerten definiert werden können.

1. Konfigurieren Sie **[!UICONTROL Pfadvorlage]** mit **[!UICONTROL Name]** und **[!UICONTROL Standardwert]**.

   ![](assets/external-integration-config-2.png)

1. Wählen Sie die **[!UICONTROL HTTP-Methode]** zwischen GET und POST aus.

1. Klicken Sie **[!UICONTROL Kopfzeile hinzufügen]** und/oder **[!UICONTROL Abfrageparameter hinzufügen]** wie für Ihre Integration erforderlich. Geben Sie für jeden Parameter die folgenden Details an:

   * **[!UICONTROL Parameter]**: Eine eindeutige Kennung, die intern verwendet wird, um auf den Parameter zu verweisen.

   * **[!UICONTROL Name]**: Der tatsächliche Name des Parameters, wie von der API erwartet.

   * **[!UICONTROL Typ]**: Wählen Sie **Konstante** für einen festen Wert oder **Variable** für die dynamische Eingabe.

   * **[!UICONTROL Wert]**: Geben Sie den Wert direkt für Konstanten ein oder wählen Sie eine Variablenzuordnung aus.

   * **[!UICONTROL Obligatorisch]**: Geben Sie an, ob dieser Parameter erforderlich ist.

   ![](assets/external-integration-config-3.png)

1. Wählen Sie einen **[!UICONTROL Authentifizierungstyp]**:

   * **[!UICONTROL Keine Authentifizierung]**: Für offene APIs, für die keine Anmeldeinformationen erforderlich sind.

   * **[!UICONTROL API-Schlüssel]**: Authentifizieren von Anfragen mithilfe eines statischen API-Schlüssels. Geben Sie den **[!UICONTROL API-Schlüsselnamen &#x200B;]**, **[!UICONTROL API-Schlüsselwert &#x200B;]** und geben Sie Ihren **[!UICONTROL Speicherort]** an.

   * **[!UICONTROL Einfache Authentifizierung]**: Verwenden Sie die standardmäßige HTTP-Standardauthentifizierung. Geben Sie **[!UICONTROL Benutzername]** und **[!UICONTROL Kennwort]** ein.

   * **[!UICONTROL OAuth 2.0]**: Authentifizierung mit dem OAuth 2.0-Protokoll. Klicken Sie auf das ![Bearbeiten](assets/do-not-localize/Smock_Edit_18_N.svg)-Symbol, um die **[!UICONTROL Payload“ zu konfigurieren oder]**.

   ![](assets/external-integration-config-4.png)

1. Legen Sie **[!UICONTROL Richtlinienkonfiguration]** wie **[!UICONTROL Timeout]** für API-Anfragen fest und wählen Sie die Aktivierung von Drosselung, Cache und/oder Wiederholung aus.

1. Mit dem **[!UICONTROL Antwort-Payload]**-Feld können Sie entscheiden, welche Felder der Beispielausgabe für die Nachrichtenpersonalisierung verwendet werden müssen.

   Klicken Sie auf ![Bearbeiten](assets/do-not-localize/Smock_Edit_18_N.svg) und fügen Sie eine JSON-Beispiel-Antwort-Payload ein, um Datentypen automatisch zu erkennen.

1. Wählen Sie die Felder aus, die für die Personalisierung bereitgestellt werden sollen, und geben Sie die entsprechenden Datentypen an.

   ![](assets/external-integration-config-5.png)

1. Verwenden Sie **[!UICONTROL Testverbindung senden]** um die Integration zu validieren.

   Klicken Sie nach der Validierung auf **[!UICONTROL Aktivieren]**.

## Verwenden externer Integrationen für die Personalisierung {#personalization}

Als Marketing-Experte können Sie konfigurierte Integrationen verwenden, um Ihre Inhalte zu personalisieren. Führen Sie folgende Schritte aus:

1. Greifen Sie auf Ihren Kampagneninhalt zu und klicken Sie auf **[!UICONTROL Personalisierung hinzufügen]** in Ihrem Text oder in HTML **[!UICONTROL Komponenten]**.

[Weitere Informationen zu Komponenten](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Navigieren Sie zum Abschnitt **[!UICONTROL Integrationen]** und klicken Sie auf **[!UICONTROL Integrationen öffnen]** um alle aktiven Integrationen anzuzeigen.

   ![](assets/external-integration-content-2.png)

1. Wählen Sie eine Integration aus und klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/external-integration-content-3.png)

1. Aktivieren Sie den **[!UICONTROL Pillen]**-Modus, um das erweiterte Integrationsmenü zu entsperren.

   ![](assets/external-integration-content-4.png)

1. Um die Einrichtung der Integration abzuschließen, definieren Sie die Integrationsattribute, die zuvor während der Konfiguration [ wurden](#configure).

   Sie können diesen Attributen Werte zuweisen, entweder mithilfe statischer Werte, die konstant bleiben, oder mithilfe von Profilattributen, die Informationen dynamisch aus Benutzerprofilen abrufen.

   ![](assets/external-integration-content-5.png)

1. Sobald Integrationsattribute definiert sind, können Sie jetzt die Integrationsfelder in Ihrem Inhalt für personalisierte Nachrichten verwenden, indem Sie auf das Symbol ![Hinzufügen](assets/do-not-localize/Smock_Add_18_N.svg) klicken.

   ![](assets/external-integration-content-6.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Ihre Integrations-Personalisierung wird jetzt erfolgreich auf Ihre Inhalte angewendet, sodass jeder Empfänger ein maßgeschneidertes, relevantes Erlebnis erhält, das auf den von Ihnen konfigurierten Attributen basiert.

![](assets/external-integration-content-7.png)




