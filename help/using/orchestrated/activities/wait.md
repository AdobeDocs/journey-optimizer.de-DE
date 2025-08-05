---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität Warten in orchestrierten Kampagnen
description: Erfahren Sie, wie Sie die Aktivität Warten in orchestrierten Kampagnen verwenden
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 77%

---


# Warten {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Aktivität „Warten“"
>abstract="Die Aktivität **Warten** wird verwendet, um die Transition von einer Aktivität zu einer anderen zu verzögern."

Die **[!UICONTROL Warten]**-Aktivität ist eine **[!UICONTROL Fluss-Kontrolle]**-Komponente, die verwendet wird, um in einer orchestrierten Kampagne eine Verzögerung zwischen zwei Aktivitäten einzuführen. Dadurch können Sie sicherstellen, dass Ihre Folgeaktivitäten zeitlich besser abgestimmt und relevanter für die Benutzerinteraktion sind.

Sie können beispielsweise einige Tage nach einem E-Mail-Versand warten, um Öffnungen und Klicks zu verfolgen, bevor Sie eine Folgenachricht senden.

## Konfiguration{#wait-configuration}

Gehen Sie folgendermaßen vor, um die Aktivität **[!UICONTROL Warten]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL orchestrierte Kampagne]** Aktivität „Warten“ hinzu.

1. Wählen Sie den Wartetyp aus, der am besten Ihren Anforderungen entspricht:

   * **[!UICONTROL Dauer]**: Geben Sie die Verzögerung bis zum Fortfahren mit der nächsten Aktivität in Sekunden, Minuten, Stunden oder Tagen an.

   * **[!UICONTROL Feste Zeit]**: Legen Sie ein bestimmtes Datum und eine bestimmte Uhrzeit fest, an denen die nächste Aktivität beginnt.

   ![](../assets/wait_activity.png)

## Beispiel{#wait-example}

Das folgende Beispiel erläutert die Aktivität **[!UICONTROL Warten]** anhand eines typischen Fallbeispiels.  An Profile, die Geburtstag feiern, wird eine E-Mail mit einem Gutschein-Code gesendet. Nach 29 Tagen wird eine SMS an dieselbe Gruppe gesendet, um sie daran zu erinnern, dass ihr Gutschein-Code für ihren Geburtstag bald abläuft.

![](../assets/wait-example.png)
