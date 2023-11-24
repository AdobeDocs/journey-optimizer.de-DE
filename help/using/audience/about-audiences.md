---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zu Adobe Experience Platform-Zielgruppen
description: Erfahren Sie, wie Sie mit Adobe Experience Platform-Zielgruppen arbeiten.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: de7c09fd5dcba80f23d136c067c2527fc4ec5f2e
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 59%

---

# Erste Schritte mit Adobe Experience Platform-Zielgruppen {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Zielgruppe"
>abstract="Mithilfe von Echtzeit-Kundenprofildaten können Sie mit Adobe Experience Platform auf einfache Weise Segmentdefinitionen für genaue Zielgruppen erstellen, die das einzigartige Verhalten und die Vorlieben Ihrer Kundinnen und Kunden erfassen."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Auswählen der Kampagnenzielgruppe"
>abstract="Diese Liste zeigt alle verfügbaren Adobe Experience Platform-Zielgruppen an. Wählen Sie die Zielgruppe aus, die mit Ihrer Kampagne angesprochen werden soll. Die in der Kampagne konfigurierte Nachricht wird an alle Kontakte gesendet, die zur ausgewählten Zielgruppe gehören. [Weitere Informationen zu Zielgruppen](../audience/about-audiences.md)"

Über [!DNL Journey Optimizer] können Sie Adobe Experience Platform-Zielgruppen mithilfe von Echtzeit-Kundenprofildaten direkt im Menü **[!UICONTROL Zielgruppen]** erstellen sowie nutzen und diese Zielgruppen in Ihre Journeys oder Kampagnen einbinden. Weitere Informationen finden Sie in der [Dokumentation zum Segmentierungs-Service in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de){target="_blank"}.

## Verwenden von Zielgruppen in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Sie können in Kampagnen und Journeys eine beliebige Adobe Experience Platform-Zielgruppe auswählen, die mit [Segmentdefinitionen](../audience/creating-a-segment-definition.md) generiert wurde.

>[!NOTE]
>
>Darüber hinaus können Sie Adobe Experience Platform-Zielgruppen ansprechen, die mit [Zielgruppenkompositionen](../audience/get-started-audience-orchestration.md) erstellt oder [aus einer CSV-Datei hochgeladen wurden](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=de#import-audience){target="_blank"}. Diese Funktionen sind als private Betaversion verfügbar.

Sie können Zielgruppen in **[!DNL Journey Optimizer]** auf verschiedene Weise nutzen:

* Wählen Sie eine Zielgruppe für eine **Kampagne** aus, sodass die Nachricht an alle Personen gesendet wird, die zur ausgewählten Zielgruppe gehören. [Erfahren Sie, wie Sie die Zielgruppe einer Kampagne definieren](../campaigns/create-campaign.md#define-the-audience-audience).

* Verwenden Sie die Orchestrierungsaktivität **Zielgruppe lesen** in einer Journey, damit alle Personen der Zielgruppe in die Journey eintreten und die in Ihrer Journey enthaltenen Nachrichten empfangen.

  Angenommen, Sie verfügen über eine Zielgruppe für „Silber-Kundinnen und -Kunden“. Mit dieser Aktivität können Sie dafür sorgen, dass alle Silber-Kundinnen und -Kunden in eine Journey eintreten, und ihnen eine Reihe personalisierter Nachrichten senden. [Erfahren Sie, wie Sie eine Aktivität vom Typ „Zielgruppe lesen“ konfigurieren](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Verwenden Sie die Ereignisaktivität **Zielgruppen-Qualifizierung**, um Personen auf der Grundlage von Adobe Experience Platform-Zielgruppeneintritten und -austritten zu veranlassen, in eine Journey einzutreten oder damit fortzufahren.

  So können Sie z. B. alle neuen Silber-Kundinnen und -Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weitere Informationen zum Verwenden dieser Aktivität finden Sie unter [Erfahren Sie, wie Sie eine Zielgruppen-Qualifizierungsaktivität konfigurieren](../building-journeys/audience-qualification-events.md).

* Verwenden Sie die Aktivität **Bedingung** in einer Journey, um Bedingungen zu erstellen, die auf der Zielgruppenzugehörigkeit basieren. [Erfahren Sie, wie Sie Zielgruppen in Bedingungen verwenden](../building-journeys/condition-activity.md#using-a-segment).

## Methoden zur Zielgruppen-Auswertung{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer werden Zielgruppen mithilfe einer der drei unten stehenden Auswertungsmethoden aus Segmentdefinitionen generiert.

+++ Streaming-Segmentierung 

Die Profilliste für die Audience wird in Echtzeit auf dem neuesten Stand gehalten, da neue Daten in das System fließen.

Die Streaming-Segmentierung ist ein fortlaufender Datenauswahlprozess, der Ihre Zielgruppen infolge von Benutzeraktivität aktualisiert. Nachdem eine Segmentdefinition erstellt und die daraus resultierende Zielgruppe gespeichert wurde, wird die Segmentdefinition auf Daten angewendet, die in Journey Optimizer eingehen. Das bedeutet, dass Personen bei sich ändernden Profildaten zur Zielgruppe hinzugefügt oder daraus entfernt werden, sodass Ihre Zielgruppe immer relevant ist. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html#query-types){target="_blank"}

>[!NOTE]
>
>Stellen Sie sicher, dass Sie die richtigen Ereignisse als Streaming-Segmentierungskriterien verwenden. [Weitere Informationen](#open-and-send-event-guardrails)

+++

+++ Batch-Segmentierung

Die Profilliste für die Audience wird alle 24 Stunden ausgewertet.

Die Batch-Segmentierung ist eine Alternative zur Streaming-Segmentierung, die alle Profildaten gleichzeitig über Segmentdefinitionen verarbeitet. Dadurch wird ein Schnappschuss der Zielgruppe erstellt, der gespeichert und zur Verwendung exportiert werden kann. Im Gegensatz zur Streaming-Segmentierung wird die Zielgruppenliste bei der Batch-Segmentierung jedoch nicht kontinuierlich in Echtzeit aktualisiert. Neue Daten, die nach dem Batch-Prozess eingehen, werden erst im nächsten Batch-Prozess in der Zielgruppe übernommen. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch){target="_blank"}

+++

+++ Edge-Segmentierung

Mit der Edge-Segmentierung können Segmente in Adobe Experience Platform sofort ausgewertet werden. [am Rand](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"}, enabling same-page and next-page personalization use cases. Currently only select query types can be evaluated with edge segmentation. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

+++

Wenn Sie wissen, welche Auswertungsmethode Sie verwenden möchten, wählen Sie sie mithilfe der Dropdownliste aus. Sie können auch auf das Ordnersymbol für das Durchsuchen-Symbol mit einer Lupe klicken, um eine Liste der verfügbaren Auswertungsmethoden für die Segmentdefinition anzuzeigen. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties){target="_blank"}

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

Nachdem Sie eine Zielgruppe zum ersten Mal definiert haben, werden Profile zur Zielgruppe hinzugefügt, wenn sie sich dafür qualifizieren.

Das Auffüllen der Zielgruppe anhand früherer Daten kann bis zu 24 Stunden dauern. Nachdem die Audience aufgefüllt wurde, wird sie kontinuierlich aktuell gehalten und ist immer für die Zielgruppenbestimmung bereit.

### Ereignisverwendung mit Streaming-Segmentierung {#open-and-send-event-guardrails}

Streaming-Segmentierung ist für die Echtzeit-Personalisierung mit hochwertigen Anwendungsfällen nützlich. Es ist jedoch wichtig, das Recht zu wählen [events](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=de#events){target="_blank"} zur Verwendung als Segmentierungskriterien.

Vermeiden Sie daher für eine Streaming-Segmentierung der optimalen Leistung die Verwendung der folgenden Ereignisse:

* **Nachricht geöffnet** Interaktionstyp-Ereignis

  Bei der Erstellung Ihrer Audience wird die Verwendung von **Nachricht geöffnet** Interaktionsereignisse wurden unzuverlässig, da es sich nicht um tatsächliche Indikatoren für Benutzeraktivitäten handelt und sich negativ auf die Segmentierungsleistung auswirken kann. Hier erfahren Sie, warum [Adobe-Blogpost](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}.

  Daher empfiehlt Adobe, die **Nachricht geöffnet** Interaktionsereignisse mit Streaming-Segmentierung. Verwenden Sie stattdessen reale Benutzeraktivitätssignale wie Klicks, Käufe oder Beacon-Daten.

* **Nachricht gesendet** Feedback-Status-Ereignis

  Die **Nachricht gesendet** Das Feedback-Ereignis wird oft vor dem Senden einer E-Mail zur Prüfung der Häufigkeit oder Unterdrückung verwendet. Adobe empfiehlt, dies zu vermeiden, da dies die Leistung beeinträchtigt und zu einer Verschlechterung des Systems führen kann.

  Verwenden Sie daher für die Häufigkeits- oder Unterdrückungslogik Geschäftsregeln anstelle von **Nachricht gesendet** Feedback-Ereignisse. Beachten Sie, dass in Kürze tägliche Frequenzobergrenzen für einzelne Profile verfügbar sein werden, was die bestehende monatliche Häufigkeit für Geschäftsregeln ergänzt.

>[!NOTE]
>
>Sie können **Nachricht geöffnet** und **Nachricht gesendet** -Ereignisse in der Batch-Segmentierung ohne Leistungsbedenken.
