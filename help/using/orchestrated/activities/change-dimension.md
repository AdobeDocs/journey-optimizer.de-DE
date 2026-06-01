---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Dimensionsänderung“
description: Erfahren Sie, wie Sie die Aktivität „Dimensionsänderung“ verwenden
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/yN2RlYom4xpdiG0G8pt3U4MeY0C1JjDudDqYg-HPv1w
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: 
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 63%

---

# Dimensionsänderung {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **Komplement erzeugen** ein"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Aktivität „Dimensionsänderung“"
>abstract="Mithilfe dieser Aktivität können Sie die Zielgruppendimension beim Erstellen einer Zielgruppe ändern. Diese Aktivität verschiebt die Achse je nach Datenvorlage und der Eingabedimension. Beispielsweise können Sie von der Dimension „Verträge“ zur Dimension „Kundinnen und Kunden“ wechseln."

Als Marketing-Fachkraft können Sie das Zielgruppen-Targeting verbessern, indem Sie innerhalb einer orchestrierten Kampagne von einer Datenentität zu einer zugehörigen wechseln. Auf diese Weise können Sie über Benutzerprofile hinausgehen und sich auf bestimmte Verhaltensweisen wie Käufe, Buchungen oder andere Interaktionen konzentrieren.

Verwenden Sie dazu die Aktivität **[!UICONTROL Dimensionsänderung]**. So können Sie die Zielgruppendimension während der orchestrierten Kampagne anpassen.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.
-->

## Konfigurieren der Aktivität „Dimensionsänderung“ {#configure}

Gehen Sie folgendermaßen vor, um die Aktivität **[!UICONTROL Dimensionsänderung]** zu konfigurieren:

1. Fügen Sie Ihrer orchestrierten Kampagne eine Aktivität des Typs **[!UICONTROL Dimensionsänderung]** hinzu.

   ![](../assets/orchestrated-change-dimension.png)

1. Definieren Sie die **[!UICONTROL neue Zielgruppendimension]**. Der Schritt Dimensionsänderung verwendet einen externen Join: Alle Datensätze aus der Eingabepopulation werden durchlaufen, einschließlich der Datensätze ohne übereinstimmenden Eintrag in der neuen Dimension.

   >[!IMPORTANT]
   >
   >Datensätze, die in der neuen Zielgruppendimension kein übereinstimmendes Profil aufweisen, werden **beim Nachrichtenversand im Hintergrund ausgeschlossen**. Dieser Ausschluss wird derzeit nicht in den Ausschlusslogs angezeigt. Um nicht übereinstimmende Datensätze frühzeitig zu identifizieren, verwenden Sie die Option **Vorschau der Ergebnisse** auf der Transition nach dem Schritt Dimensionsänderung und überprüfen Sie, ob die Datensatzzählungen Ihren Erwartungen entsprechen, bevor Sie fortfahren.


## Beispiel {#example}

Dieser Anwendungsfall konzentriert sich auf den Versand einer SMS an Profile, die innerhalb des letzten Monats eine Wunschliste erstellt haben.

Beginnen Sie mit einer Aktivität des Typs **[!UICONTROL Zielgruppe erstellen]** und verwenden Sie die Zielgruppendimension **[!UICONTROL Wunschliste]**, um alle relevanten Wunschlisten zu ermitteln.

Fügen Sie dann die Aktivität **[!UICONTROL Dimension ändern]** hinzu, um die Zielgruppendimension von **[!UICONTROL Wunschliste]** auf **[!UICONTROL Empfänger] umzustellen** Dieser Schritt stellt sicher, dass die orchestrierte Kampagne die richtigen Profile anspricht, die mit diesen Wunschlisten verknüpft sind, sodass die SMS an die gewünschten Profile gesendet werden kann.

![](../assets/orchestrated-change-dimension-example.png)
