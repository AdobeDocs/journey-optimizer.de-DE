---
title: Verwalten von API-Anmeldeinformationen für benutzerdefinierte Kanäle
description: Erfahren Sie, wie Sie API-Anmeldeinformationen für benutzerdefinierte Kanäle in Adobe Journey Optimizer verwalten.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 4%

---


# API-Anmeldeinformationen verwalten {#api-credentials}

Wenn ein benutzerdefinierter Kanal mit einem anderen Authentifizierungstyp als **None** erstellt wird, wird automatisch ein erster Satz von API-Anmeldeinformationen generiert, wenn der Kanal aktiviert wird.

Sie können Anmeldeinformationen unter **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Kanal Builder]** > **[!UICONTROL API-Anmeldeinformationen]** anzeigen, verwalten und bearbeiten.

![API-Anmeldeinformationen](assets/custom_channel_api_credentials.png){width="100%"}

Wenn Sie mehrere Anmeldeinformationen für denselben Kanal haben, können Sie verschiedene Authentifizierungswerte an verschiedene Kanalkonfigurationen anhängen - beispielsweise für verschiedene Marken oder Anwendungsfälle -, ohne die Kanaldefinition zu duplizieren.

Um einen vorhandenen Satz von Anmeldeinformationen zu bearbeiten, klicken Sie auf ein Element in der Inventarliste. Alle Felder können bearbeitet werden.

Gehen Sie wie folgt vor, um zusätzliche Anmeldeinformationen für denselben Kanal zu erstellen.

1. Klicken Sie in der Liste **[!UICONTROL API]** Anmeldeinformationen auf **[!UICONTROL API-Anmeldeinformationen erstellen]**.

1. Geben Sie einen Namen und eine Beschreibung an.

   ![API-Anmeldeinformationen erstellen](assets/custom_channel_create_api_credentials.png){width="100%"}

1. Wählen Sie den **[!UICONTROL Kanal]** für den Sie Anmeldeinformationen erstellen möchten.

   >[!NOTE]
   >
   >In der Dropdown-Liste werden nur aktivierte benutzerdefinierte Kanäle mit einem anderen Authentifizierungstyp **Keine** angezeigt.

1. Wählen Sie den **[!UICONTROL Authentifizierungstyp]** aus der Liste aus.
1. Füllen Sie die authentifizierungsspezifischen Felder aus:
   * **[!UICONTROL API-Schlüssel]** - Geben Sie den Schlüsselnamen, den Wert und den Speicherort (Abfrageparameter oder Kopfzeile) an.
   * **[!UICONTROL Einfache Authentifizierung]** - Geben Sie einen Benutzernamen und ein Kennwort ein.
   * **[!UICONTROL OAuth 2.0]** - Konfigurieren der Payload für die OAuth 2.0-Authentifizierung.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Nächste Schritte {#next-steps}

* [Subdomain delegieren](custom-channel-subdomains.md) (optional - für Linktracking erforderlich)
* [Erstellen einer Kanalkonfiguration](custom-channel-configuration.md)
