---
solution: Journey Optimizer
product: journey optimizer
title: Definieren der API-ausgelösten Kampagnen-Audience
description: Erfahren Sie, wie Sie die Zielgruppe einer API-ausgelösten Kampagne definieren.
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 57%

---


# Definieren der API-ausgelösten Kampagnen-Audience {#api-audience}

Definieren Sie auf **[!UICONTROL Registerkarte]** Audience“ die Kampagnentität.

![](assets/campaign-audience.png)

1. **Zielgruppe auswählen**

   * Klicken Sie bei Kampagnen, die von der Marketing **[!UICONTROL API ausgelöst werden, auf die Schaltfläche]** Zielgruppe auswählen“, um die Liste der verfügbaren Adobe Experience Platform-Zielgruppen anzuzeigen. [Weitere Informationen zu Zielgruppen](../audience/about-audiences.md).

     >[!IMPORTANT]
     >
     >Zielgruppen und Attribute aus der [Zielgruppenkomposition](../audience/get-started-audience-orchestration.md) stehen derzeit nicht zur Verwendung mit Healthcare Shield oder Privacy und Security Shield zur Verfügung

   * Für Kampagnen, die durch eine Transaktions-API ausgelöst werden, müssen die Zielgruppenprofile im API-Aufruf definiert werden. Ein einzelner API-Aufruf unterstützt bis zu 20 eindeutige Empfängerinnen und Empfänger. Jede Empfängerin und jeder Empfänger muss über eine eindeutige Benutzer-ID verfügen. Doppelte Benutzer-IDs sind nicht zulässig. Weitere Informationen finden Sie in der [Dokumentation zur Interactive Message Execution API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}

1. **Identitätstyp auswählen**

   Wählen Sie im Feld **[!UICONTROL Identitätstyp]** den Schlüsseltyp aus, der zur Identifizierung der Kontakte in der ausgewählten Zielgruppe verwendet werden soll. Sie können entweder einen vorhandenen Identitätstyp verwenden oder mit dem Identity Service einen neuen erstellen. Standardmäßige Identity-Namespaces werden auf [dieser Seite](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} aufgeführt.

   Pro Kampagne ist nur ein Identitätstyp zulässig. Kontakte, die zu einem Segment gehören, das nicht den ausgewählten Identitätstyp unter den verschiedenen Identitäten hat, können nicht von der Kampagne angesprochen werden. Weitere Informationen zu Identitätstypen und Namespaces sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de){target="_blank"} verfügbar.

1. **Profilerstellung bei der Kampagnenausführung aktivieren**

   In einigen Fällen müssen Sie möglicherweise Transaktionsnachrichten an Profile senden, die nicht im System sind. Wenn beispielsweise ein unbekannter Benutzer versucht, sein Kennwort auf Ihrer Website zurückzusetzen. Wenn ein Profil nicht in der Datenbank vorhanden ist, erlaubt Journey Optimizer Ihnen, es automatisch bei der Ausführung der Kampagne zu erstellen, um das Senden der Nachricht an dieses Profil zu ermöglichen.

   Um die Profilerstellung bei der Kampagnenausführung zu aktivieren, schalten Sie die Option **[!UICONTROL Neue Profile erstellen]** ein. Wenn diese Option deaktiviert ist, werden unbekannte Profile für jeden Versand zurückgewiesen und der API-Aufruf schlägt fehl.

   ![](assets/api-triggered-create-profile.png)

   >[!IMPORTANT]
   >
   >Diese Option ist für die Erstellung **Profilen mit sehr geringem** in einem Anwendungsfall mit großem Versandvolumen vorgesehen, wobei ein Großteil der Profile bereits in Platform vorhanden ist.
   >
   >Unbekannte Profile werden im **Profil-Datensatz von AJO Interactive Messaging** erstellt, und zwar in drei Standard-Namespaces (E-Mail, Telefon und ECID) für jeden ausgehenden Kanal (E-Mail, SMS und Push). Wenn Sie jedoch einen benutzerdefinierten Namespace verwenden, wird die Identität mit demselben benutzerdefinierten Namespace erstellt.

## Nächste Schritte {#next}

Sobald Ihre Kampagnenkonfiguration und der Inhalt fertig sind, können Sie die Ausführung planen. [Weitere Informationen](api-triggered-campaign-schedule.md)
