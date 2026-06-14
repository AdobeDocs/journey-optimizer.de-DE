---
solution: Journey Optimizer
product: journey optimizer
title: Anpassen der vertikalen Ausrichtung und des Abstands in Journey Optimizer
description: Erfahren Sie, wie Sie die vertikale Ausrichtung und den Abstand anpassen.
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: vertikale Ausrichtung, E-Mail-Editor, Abstand
exl-id: 1e1d90ff-df5d-4432-a63a-a32d0d281d48
TQID: https://experienceleague.adobe.com/vJhROWi5ZiOLJrESMe-oUkmve1vSXrE5sNewDLpv-eE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 92%

---

# Anpassen der vertikalen Ausrichtung und des Abstands {#alignment-and-padding}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie die senkrechte Ausrichtung und den Abstand von Spalten und Strukturen in der E-Mail-Designer anpassen, einschließlich der Behebung des restlichen Fragmentabstands für das korrekte Rendering auf Mobilgeräten.

>[!ENDSHADEBOX]

In diesem Beispiel passen wir den Abstand und die senkrechte Ausrichtung innerhalb einer Strukturkomponente an, die aus drei Spalten besteht.

1. Wählen Sie eine Strukturkomponente direkt in der E-Mail oder über den **[!UICONTROL Navigationsbaum]** im linken Menü aus.

1. Wählen Sie in der Symbolleiste mit der Option **[!UICONTROL Spalte auswählen]** die gewünschte Spalte aus. Sie können sie auch im Strukturbaum auswählen.

   Die bearbeitbaren Parameter für diese Spalte werden im Menü **[!UICONTROL Stile]** angezeigt.

   ![](assets/alignment_2.png)

1. Wählen Sie unter **[!UICONTROL Ausrichtung]** die Option **[!UICONTROL Oben]**, **[!UICONTROL Zentriert]** oder **[!UICONTROL Unten]** aus.

   ![](assets/alignment_3.png)

1. Legen Sie unter **[!UICONTROL Abstand]** den Abstand für alle Seiten fest.

   Wählen Sie **[!UICONTROL Unterschiedliche Abstände für jede Seite]** aus, wenn Sie eine Feinabstimmung für den Abstand vornehmen möchten. Klicken Sie auf das Sperrsymbol, um die Synchronisierung aufzuheben.

   ![](assets/alignment_4.png)

1. Gehen Sie analog mit den anderen Ausrichtungs- und Abstandseinstellungen der Spalten vor.

1. Speichern Sie Ihre Änderungen.

>[!TIP]
>
>Achten Sie beim Entwerfen von E-Mail-Inhalt für Gmail auf Android-Geräten darauf, dass für Bilder und Trennelemente Spaltenabstände und keine großen, festen Ränder verwendet werden. Gmail auf Android rendert übergroße Bilder und Ränder häufig falsch, was zu Layout-Überlauf oder reduzierten Trennlinien führt. Verwenden Sie eine kleinere Bildbreite oder spaltenbasierte Abstände, um eine konsistente Anzeige zu erreichen.

## Verwalten der Abstände von Fragmenten mit Breadcrumb-Navigation {#fragment-padding-breadcrumb}

Beim Arbeiten mit [Fragmenten](../content-management/fragments.md) im E-Mail-Designer kann es vorkommen, dass der ausgeblendete oder verbleibende Abstand das Rendering auf Mobilgeräten anders beeinflusst als auf dem Desktop. Dies geschieht besonders häufig, wenn Fragmente entsperrt wurden oder [die Vererbung unterbrochen wurde](use-visual-fragments.md#break-inheritance), da übrig gebliebene Formatierungen in den zugrunde liegenden Spalten- oder Textkomponenten verbleiben können.

So identifizieren und bearbeiten Sie verbleibende Abstände in Fragmenten:

1. Verwenden Sie den **[!UICONTROL Navigationsbaum]** oder klicken Sie direkt auf Elemente im Editor, um jede übergeordnete Struktur oder Spalte innerhalb Ihres Fragments auszuwählen. Auf diese Weise können Sie ausgeblendete Abstände oder Ränder finden, die speziell für Mobilgeräte gelten.

1. Nachdem Sie das Element im Breadcrumb ausgewählt haben, navigieren Sie auf der rechten Seite zur Registerkarte **[!UICONTROL Stile]**.

1. Überprüfen Sie die Einstellungen für **[!UICONTROL Abstände]** und entfernen Sie die Abstände nach Bedarf oder passen Sie sie an, um eine korrekte Ausrichtung auf Mobilgeräten zu erreichen.

1. Wenn bei der Wiederverwendung von Fragmenten weiterhin Ausrichtungsprobleme auftreten, wiederholen Sie diesen Vorgang für andere Spalten oder Textkomponenten innerhalb des Fragments.

>[!NOTE]
>
>Dieses Verhalten tritt in der Regel auf, wenn Fragmente wiederholt eingefügt und entfernt werden, da sich Stilregeln akkumulieren können. Überprüfen Sie die Abstandswerte immer mithilfe der Breadcrumb-Navigation, insbesondere für Mobilgeräte.