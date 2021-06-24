---
title: Entscheidungsregeln erstellen
description: Erfahren Sie, wie Sie in Adobe Experience Platform Entscheidungsregeln erstellen.
feature: Angebote
topic: Integrationen
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 100%

---

# Entscheidungsregeln erstellen {#creating-decision-rules}

Auf Grundlage der in Adobe Experience Platform verfügbaren Daten können Sie Entscheidungsregeln für Angebote erstellen. Entscheidungsregeln bestimmen, wem ein Angebot unterbreitet werden kann.

Sie können beispielsweise angeben, dass ein „Angebot von Winterkleidung für Frauen“ nur dann angezeigt werden soll, wenn (Geschlecht = „Weiblich“) und (Region = „Nordost“) zutrifft.

![](../../assets/do-not-localize/how-to-video.png) [Funktion im Video kennenlernen](#video).

Die Liste der erstellten Entscheidungsregeln ist im Menü **[!UICONTROL Komponenten]** verfügbar.

![](../../assets/decision_rules_list.png)

Gehen Sie wie folgt vor, um eine Entscheidungsregel zu erstellen:

1. Gehen Sie zur Registerkarte **[!UICONTROL Regeln]** und klicken Sie auf **[!UICONTROL Regel erstellen]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. Benennen Sie Ihre Regel, geben Sie eine Beschreibung ein und konfigurieren Sie dann die Regel entsprechend Ihren Anforderungen.

   Dazu steht Ihnen der **Segment Builder** in Adobe Experience Platform zur Verfügung, mit dem Sie die Regelbedingungen erstellen können. Weiterführende Informationen zu dessen Verwendung finden Sie im [entsprechenden Handbuch](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=de).

   In diesem Beispiel werden Kunden mit der Treuestufe „Gold“ als Zielgruppe ausgewählt.

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Der zum Erstellen von Entscheidungsregeln bereitgestellte Segment Builder weist einige Besonderheiten im Vergleich zum Dienst **[!UICONTROL Audience-Ziele]** auf. Beispielsweise ist die Registerkarte **[!UICONTROL Segmente]** nicht verfügbar. Das in der Segment Builder-Dokumentation beschriebene globale Verfahren gilt jedoch weiter, um Entscheidungsregeln für Angebote zu erstellen.

1. Klicken Sie zur Bestätigung auf **[!UICONTROL Speichern]**.

1. Nachdem die Regel erstellt wurde, wird sie in der Regelliste angezeigt. Sie können sie auswählen, um ihre Eigenschaften anzuzeigen und zu bearbeiten oder zu löschen.

   ![](../../assets/rule_created.png)

## Tutorial {#video}

>[!NOTE]
>
>Dieses Video bezieht sich auf den auf Adobe Experience Platform aufbauenden Programm-Service Offer Decisioning. Es enthält allgemeine Leitlinien für die Verwendung von Angeboten im Kontext von Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
