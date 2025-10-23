---
solution: Journey Optimizer
product: journey optimizer
title: Definieren der Eigenschaften einer Kampagne, die durch API ausgelöst wird
description: Informationen zum Definieren der Eigenschaften einer Kampagne, die durch API ausgelöst wird.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
exl-id: bda7e337-a246-4f01-b935-4a234d4c4baa
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 64%

---

# Definieren der Eigenschaften einer Kampagne, die durch API ausgelöst wird {#api-properties}

Gehen Sie wie folgt vor, um eine neue Kampagne zu erstellen, die durch API ausgelöst wird:

1. Navigieren Sie zum Menü **[!UICONTROL Kampagnen]** und wählen Sie die Registerkarte **[!UICONTROL Durch API ausgelöst]** aus.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Kampagne erstellen]** und wählen Sie den Kampagnentyp aus:

   * **[!UICONTROL API-ausgelöst – Marketing]** – Wählen Sie diesen durch API ausgelösten Kampagnentyp aus, um personalisierte Marketing-Kommunikation an ausgewählte Zielgruppen zu senden.

   * **[!UICONTROL API-ausgelöst - Transaktion]** - Transaktionskampagnen dienen dem Versand von Transaktionsnachrichten, d. h. Nachrichten, die nach einer von einem Kontakt durchgeführten Aktion gesendet werden: Anforderung zum Zurücksetzen des Passworts, Warenkorbkauf usw.

     +++Hoher Durchsatz

     Für Kampagnen, die durch eine Transaktions-API ausgelöst werden, können Sie den Modus **[!UICONTROL Hoher Durchsatz]** aktivieren. Dieser Modus wurde für umfangreiches Echtzeit-Messaging (bis zu 5.000 Transaktionen pro Sekunde) entwickelt und bietet eine höhere Verfügbarkeit mit geringerer Latenz. [Erfahren Sie, wie Sie mit dem Hochdurchsatzmodus arbeiten](../campaigns/api-triggered-high-throughput.md)

     >[!AVAILABILITY]
     >
     >Derzeit ist der Modus „Hoher Durchsatz“ nur für den E-Mail-Kanal und in der US-Region verfügbar.
     >
     >Diese Funktion ist nur für Unternehmen verfügbar, die das Adobe Add-on **Transaktionsnachrichten mit hohem**&quot; erworben haben. Weitere Informationen erhalten Sie beim Adobe-Support.

     +++

   ![](assets/api-triggered-modal.png)

1. Geben Sie auf der Registerkarte **[!UICONTROL Eigenschaften]** einen Namen und eine Beschreibung für Ihre Kampagne ein.

   ![](assets/create-campaign-properties.png)

1. Verwenden Sie das Feld **Tags**, um Ihrer Kampagne einheitliche Adobe Experience Platform-Tags zuzuweisen. Dies ermöglicht eine einfache Klassifizierung und verbesserte Suche über die Kampagnenliste. [Erfahren Sie, wie Sie mit Tags arbeiten](../start/search-filter-categorize.md#tags).

1. Sie können den Zugriff auf diese Kampagne basierend auf Zugriffs-Labels einschränken. Um eine Zugriffsbeschränkung hinzuzufügen, navigieren Sie zur Schaltfläche **[!UICONTROL Zugriff verwalten]** oben auf dieser Seite. Es muss sichergestellt sein, dass Sie nur Labels ausgewählt werden, für die eine Berechtigung besteht. [Erfahren Sie mehr über die Zugriffssteuerung auf Objektebene](../administration/object-based-access.md).

## Nächste Schritte {#next}

Sobald die Konfiguration und der Inhalt der Kampagne fertiggestellt sind, können Sie ihre Aktion konfigurieren. [Weitere Informationen](api-triggered-campaign-action.md)
