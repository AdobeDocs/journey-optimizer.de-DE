---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Dimensionsänderung“
description: Erfahren Sie, wie Sie die Aktivität „Dimensionsänderung“ verwenden
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 67%

---

# Ändern der Dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **Komplement erzeugen** ein"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Aktivität „Dimensionsänderung“"
>abstract="Mithilfe dieser Aktivität können Sie die Zielgruppendimension beim Erstellen einer Zielgruppe ändern. Diese Aktivität verschiebt die Achse je nach Datenvorlage und der Eingabedimension. Beispielsweise können Sie von der Dimension „Verträge“ zur Dimension „Kundinnen und Kunden“ wechseln."

Die Aktivität **Dimensionsänderung** ist eine Aktivität zur **Zielgruppenbestimmung**. Mit dieser Aktivität können Sie die Zielgruppendimension ändern, während Sie Ihre mehrstufige Kampagne erstellen. Die Achse wird je nach Datenvorlage und der Eingabedimension verschoben.

Sie können beispielsweise die Zielgruppendimension einer mehrstufigen Kampagne von „Empfänger“ in „Abonnentenanwendung“ ändern, um Push-Benachrichtigungen an die Zielgruppenempfänger zu senden.

>[!IMPORTANT]
>
>Beachten Sie, dass die Aktivitäten **[!UICONTROL Dimension ändern]** und **[!UICONTROL Datenquelle ändern]** nicht in einer Zeile hinzugefügt werden sollten. Wenn Sie beide Aktivitäten nacheinander verwenden müssen, muss die Aktivität **[!UICONTROL Anreicherung]** zwischen ihnen enthalten sein. Dadurch wird eine ordnungsgemäße Ausführung sichergestellt und potenzielle Konflikte oder Fehler werden vermieden.

## Konfigurieren der Aktivität „Dimensionsänderung“ {#configure}

Gehen Sie folgendermaßen vor, um die Aktivität **Dimensionsänderung** zu konfigurieren:

1. Fügen Sie **mehrstufigen Kampagne** Aktivität „Dimension ändern“ hinzu.

   ![](../assets/workflow-change-dimension.png)

1. Definieren Sie die **neue Zielgruppendimension**. Bei einer Dimensionsänderung werden alle Einträge beibehalten. Andere Optionen sind noch nicht verfügbar.

1. Führen Sie die mehrstufige Kampagne aus, um das Ergebnis anzuzeigen. Vergleichen Sie die Daten in den Tabellen vor und nach der Aktivität Dimensionsänderung und vergleichen Sie die Struktur der mehrstufigen Kampagnentabellen.

## Beispiel {#example}

In diesem Beispiel möchten wir einen SMS-Versand an alle Profile senden, die einen Kauf getätigt haben. Dazu verwenden wir zunächst die Aktivität **[!UICONTROL Zielgruppe erstellen]**, die mit einer benutzerdefinierten Zielgruppendimension „Kauf“ verknüpft ist, um alle erfolgten Käufe auszuwählen.

Anschließend verwenden wir die Aktivität **[!UICONTROL Dimensionsänderung]**, um die mehrstufige Zielgruppendimension der Kampagne in „Empfänger“ zu ändern. Auf diese Weise können wir die Empfängerinnen und Empfänger ansprechen, die der Abfrage entsprechen.

![](../assets/workflow-change-dimension-example.png)
