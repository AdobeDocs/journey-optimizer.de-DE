---
title: Erstellen von Entscheidungsregeln
description: Erfahren Sie, wie Sie Entscheidungsregeln erstellen, um zu definieren, wem Angebote angezeigt werden können
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 55d9befff9b9bf1bc81c6553cd76f015fdd3116e
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 100%

---

# Entscheidungsregeln erstellen {#create-decision-rules}

Auf Grundlage der in Adobe Experience Platform verfügbaren Daten können Sie Entscheidungsregeln für Angebote erstellen. Entscheidungsregeln bestimmen, wem ein Angebot unterbreitet werden kann.

Sie können beispielsweise angeben, dass ein „Angebot von Winterkleidung für Frauen“ nur dann angezeigt werden soll, wenn (Geschlecht = „Weiblich“) und (Region = „Nordost“) zutrifft.

➡️ [Entdecken Sie diese Funktion im Video](#video).

Die Liste der erstellten Entscheidungsregeln ist im Menü **[!UICONTROL Komponenten]** verfügbar.

![](../assets/decision_rules_list.png)

Gehen Sie wie folgt vor, um eine Entscheidungsregel zu erstellen:

1. Gehen Sie zur Registerkarte **[!UICONTROL Regeln]** und klicken Sie auf **[!UICONTROL Regel erstellen]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Benennen Sie Ihre Regel, geben Sie eine Beschreibung ein und konfigurieren Sie dann die Regel entsprechend Ihren Anforderungen.

   Dazu steht Ihnen der **Segment Builder** zur Verfügung, der Ihnen beim Erstellen der Regelbedingungen hilft. [Weitere Informationen](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Der zum Erstellen von Entscheidungsregeln bereitgestellte Segment Builder weist einige Besonderheiten im Vergleich zum Dienst **[!UICONTROL Audience-Ziele]** auf. Beispielsweise ist die Registerkarte **[!UICONTROL Segmente]** nicht verfügbar. Das in der [Segment Builder](../../segment/about-segments.md)-Dokumentation beschriebene globale Verfahren gilt jedoch weiter, um Entscheidungsregeln für Angebote zu erstellen. Weitere Informationen zu Datensätzen finden Sie in der [Dokumentation zum Adobe Experience Platform-Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=de).

1. Während Sie neue Felder im Arbeitsbereich hinzufügen und konfigurieren, zeigt der Fensterbereich **[!UICONTROL Segmenteigenschaften]** Informationen zur geschätzten Anzahl der zum Segment gehörenden Profile an. Klicken Sie auf **[!UICONTROL Schätzung aktualisieren]**, um diese Daten zu aktualisieren.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Profilschätzungen sind nicht verfügbar, wenn Regelparameter Daten enthalten, die nicht im Profil enthalten sind, z. B. Kontextdaten. Beispielsweise eine Eignungsregel, für die die aktuelle Temperatur höher als 25 °C sein muss.

1. Klicken Sie zur Bestätigung auf **[!UICONTROL Speichern]**.

1. Nachdem die Regel erstellt wurde, wird sie in der Liste **[!UICONTROL Regeln]** angezeigt. Sie können sie auswählen, um ihre Eigenschaften anzuzeigen oder um sie zu bearbeiten oder zu löschen.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Ereignisbasierte Angebote werden derzeit in [!DNL Journey Optimizer] nicht unterstützt. Wenn Sie eine Entscheidungsregel basierend auf einem [Ereignis](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=de#events){target="_blank"} erstellen, können Sie sie nicht in einem Angebot nutzen.

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
