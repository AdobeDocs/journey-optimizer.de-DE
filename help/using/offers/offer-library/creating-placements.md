---
title: Erstellen von Platzierungen
description: Erfahren Sie, wie Sie Platzierungen für Ihre Angebote erstellen
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 51f93270c969875e94cc3e98919149d67d764ed1
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 47%

---

# Erstellen von Platzierungen {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="Platzierung"
>abstract="Eine Platzierung ist ein Container, der zur Präsentation von Angeboten verwendet wird. Sie hilft sicherzustellen, dass der richtige Angebotsinhalt an der richtigen Stelle Ihrer Nachricht angezeigt wird. Platzierungen werden im Menü „Komponenten“ definiert."

Eine Platzierung hilft sicherzustellen, dass der richtige Angebotsinhalt an der richtigen Stelle Ihrer Nachricht angezeigt wird. Wenn Sie Inhalte zu einem Angebot hinzufügen, werden Sie aufgefordert, eine Platzierung auszuwählen, an der diese Inhalte angezeigt werden können.

➡️ [In diesem Video erfahren Sie, wie Sie Platzierungen erstellen](#video)

Im folgenden Beispiel gibt es drei Platzierungen, die verschiedenen Inhaltstypen entsprechen (Bild, Text, HTML).

![](../assets/offers_placement_schema.png)

Die Liste der Platzierungen ist im Menü **[!UICONTROL Komponenten]** verfügbar. Es gibt Filter, mit denen Sie Platzierungen nach einem bestimmten Kanal oder Inhalt abrufen können.

![](../assets/placements_filter.png)

Gehen Sie wie folgt vor, um eine Platzierung zu erstellen:

1. Klicken Sie auf **[!UICONTROL Platzierung erstellen]**.

   ![](../assets/offers_placement_creation.png)

1. Definieren Sie die Eigenschaften der Platzierung:

   * **[!UICONTROL Name]**: der Name der Platzierung. Achten Sie darauf, einen aussagekräftigen Namen zu wählen, um die Platzierung leichter abrufen zu können.
   * **[!UICONTROL Kanaltyp]**: Der Kanal, für den die Platzierung verwendet wird.
   * **[!UICONTROL Content-Typ]**: Der Typ des Contents, den die Platzierung anzeigen darf: Text, HTML, Bild-Link oder JSON.
   * **[!UICONTROL Beschreibung]**: eine Beschreibung der Platzierung (optional).

   ![](../assets/offers_placement_creation_properties.png)


1. Die **[!UICONTROL Anforderungseinstellungen]** und **[!UICONTROL Antwortformat]** -Abschnitte enthalten zusätzliche Parameter:

   * **[!UICONTROL Duplikate über Platzierungen hinweg zulassen]**: Steuern Sie, ob dasselbe Angebot mehrmals für verschiedene Platzierungen vorgeschlagen werden kann. Wenn diese Option aktiviert ist, berücksichtigt das System dasselbe Angebot für mehrere Platzierungen. Standardmäßig ist der Parameter auf false gesetzt.

      Wenn diese Option bei einer Platzierung in einer Entscheidungsanfrage auf &quot;false&quot;gesetzt ist, erben alle Platzierungen in der Anfrage die Einstellung &quot;false&quot;.

   * **[!UICONTROL Angebot anfordern]**: Standardmäßig wird für jedes Profil ein Angebot des Entscheidungsbereichs zurückgegeben. Mit dieser Option können Sie die Anzahl der zurückgegebenen Angebote anpassen. Wenn Sie beispielsweise „2“ auswählen, werden für diesen Entscheidungsumfang die besten zwei Angebote angezeigt.

   * **[!UICONTROL Inhalt einschließen]** / **[!UICONTROL Metadaten einschließen]**: geben Sie an, ob der Inhalt und die Metadaten des Angebots in der API-Antwort zurückgegeben werden sollen. Sie können alle Metadaten oder nur bestimmte Felder einschließen. Standardmäßig ist der Wert Metadaten einschließen auf &quot;true&quot;gesetzt.
   Diese Parameter können auch direkt in Ihrer API-Anfrage festgelegt werden, wenn Sie mit der [Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). Die Konfiguration in der Benutzeroberfläche kann Ihnen jedoch Zeit sparen, da Sie sie nicht in jeder API-Anfrage weitergeben müssen. Beachten Sie, dass bei der Konfiguration der Parameter sowohl in der Benutzeroberfläche als auch in der API-Anfrage die Werte aus der API-Anfrage Vorrang vor den Werten aus der Benutzeroberfläche haben.

   >[!NOTE]
   >
   >Wenn Sie mit dem [Edge Decisioning-API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?)können Sie diese Parameter nicht in Ihrer Anfrage festlegen. Sie müssen sie in diesem Bildschirm definieren.
   >
   >Wenn Sie mit dem [Batch Decisioning-API](../api-reference/offer-delivery-api/batch-decisioning-api.md)können Sie diese Parameter entweder in diesem Bildschirm oder in Ihrer API-Anfrage festlegen. Wenn es zwischen dem Bildschirm und der APi-Anforderung eine Nichtübereinstimmung der Parameterwerte gibt, werden die Anforderungswerte verwendet.

1. Klicken Sie zur Bestätigung auf **[!UICONTROL Speichern]**.

1. Nachdem die Platzierung erstellt wurde, wird sie in der Liste der Platzierungen angezeigt. Sie können das Fallback-Angebot auswählen, um seine Eigenschaften anzuzeigen und zu bearbeiten.

   ![](../assets/placement_created.png)

## Anleitungsvideo{#video}

Erfahren Sie, wie Sie im Entscheidungs-Management Platzierungen erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

