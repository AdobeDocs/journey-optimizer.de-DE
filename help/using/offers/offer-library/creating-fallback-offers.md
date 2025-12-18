---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erstellen von Fallback-Angeboten
description: Erfahren Sie, wie Sie Fallback-Angebote erstellen, die Kunden angezeigt werden, die für kein Angebot infrage kommen
badge: label="Legacy" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 9ba16ad9-a5e7-4ce7-8ed6-7707d37178c6
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 93%

---

# Erstellen von Fallback-Angeboten {#create-fallback-offers}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="ajo_decisioning_new_fallback"
>title="Fallback-Angebot"
>abstract="Ein Fallback-Angebot ist das Standardangebot, das angezeigt wird, wenn ein Endanwender für keines der personalisierten Angebote qualifiziert ist."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_fallback_offer_details "
>title="Fallback-Angebotsdetails"
>abstract="Geben Sie den Namen des Fallback-Angebots an. Sie können auch einen oder mehrere vorhandene Sammlungsqualifizierer damit verknüpfen, sodass Sie die Angebotsbibliothek leichter durchsuchen und organisieren können."

Ein Fallback-Angebot wird an Kunden gesendet, wenn keine anderen Angebote für sie geeignet sind. Die Schritte zum Einrichten eines Fallback-Angebots bestehen darin, eine oder mehrere Darstellungen zu erstellen (ähnlich wie beim Erstellen eines Angebots).

➡️ [Funktion im Video kennenlernen](#video).

Die Liste der Fallback-Angebote ist im Menü **[!UICONTROL Angebote]** verfügbar.

![](../assets/offers_list.png)

Gehen Sie wie folgt vor, um ein Fallback-Angebot zu erstellen:

>[!NOTE]
>
>Beachten Sie, dass Fallback-Angebote im Gegensatz zu personalisierten Angeboten keine Eignungsregeln und Beschränkungsparameter aufweisen, da sie Kunden in letzter Instanz ohne Bedingung unterbreitet werden.

1. Klicken Sie auf **[!UICONTROL Angebot erstellen]** und wählen Sie dann **[!UICONTROL Fallback-Angebot]** aus.

   ![](../assets/create_fallback.png)

1. Geben Sie den Namen des Fallback-Angebots an. Sie können auch ein oder mehrere vorhandene Sammlungsqualifizierer (ehemals als „Tags“ bezeichnet) damit verknüpfen, um die Angebotsbibliothek einfacher durchsuchen und organisieren zu können.

   ![](../assets/fallback_details.png)

1. Um dem Angebot benutzerdefinierte oder zentrale Datennutzungs-Labels zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]**. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (Object Level Access Control, OLAC)](../../administration/object-based-access.md)

1. Erstellen Sie eine oder mehrere Darstellungen für das Fallback-Angebot. Ziehen Sie dazu Platzierungen per Drag-and-Drop aus dem linken Bereich (ähnlich wie beim Erstellen eines personalisierten Angebots). Weitere Informationen finden Sie unter [Erstellen von personalisierten Angeboten](../offer-library/creating-personalized-offers.md).

   ![](../assets/fallback_content.png)

   >[!CAUTION]
   >
   >Fallback-Angebote sollten alle Darstellungen enthalten, die in einer [Entscheidung](../offer-activities/create-offer-activities.md) verwendet werden. Wenn eine Entscheidung beispielsweise 5 Angebote umfasst und jedes davon eine andere Darstellung hat, sollten 5 Darstellungen in das Fallback-Angebot aufgenommen werden.

1. Nachdem die Darstellungen des Fallback-Angebots hinzugefügt wurden, wird eine Zusammenfassung angezeigt. Wenn alles ordnungsgemäß konfiguriert ist und Ihr Fallback-Angebot bereit für den Versand an Kunden ist, klicken Sie auf **[!UICONTROL Beenden]** und wählen Sie **[!UICONTROL Speichern und genehmigen]**.

   Sie können das Fallback-Angebot auch als Entwurf speichern, um es später zu bearbeiten und zu genehmigen.

   ![](../assets/fallback_review.png)

1. Das Fallback-Angebot wird in der Liste mit dem Status **[!UICONTROL Live]** oder **[!UICONTROL Entwurf]** angezeigt, je nachdem, ob Sie es im vorherigen Schritt genehmigt haben oder nicht.

   Es ist nun bereit, Kunden unterbreitet zu werden. Sie können das Fallback-Angebot auswählen, um seine Eigenschaften anzuzeigen und zu bearbeiten. <!-- no suppression? -->

   ![](../assets/fallback_created.png)

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329383?quality=12)

