---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Zielgruppe speichern“
description: Erfahren Sie, wie Sie die Aktivität „Zielgruppe speichern“ in einer koordinierten Kampagne verwenden
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 17%

---


# Speichern einer Zielgruppe {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Aktivität „Zielgruppe speichern“"
>abstract="Die Aktivität **Zielgruppe speichern** ist eine **Zielgruppenbestimmungs**-Aktivität, mit der Sie eine vorhandene Zielgruppe aktualisieren oder eine neue Zielgruppe aus der zuvor in der orchestrierten Kampagne generierten Population erstellen können. Nach der Erstellung werden diese Zielgruppen zur Liste der Anwendungszielgruppen hinzugefügt und können über das Menü **Zielgruppen** aufgerufen werden."

Die Aktivität **[!UICONTROL Zielgruppe speichern]** ist eine **[!UICONTROL Zielgruppenbestimmungs]**-Aktivität, mit der basierend auf der zuvor in der orchestrierten Kampagne generierten Population eine neue Zielgruppe erstellt oder eine vorhandene aktualisiert wird. Nach dem Speichern wird die Zielgruppe zur Liste der Anwendungszielgruppen hinzugefügt und kann über das Menü **[!UICONTROL Zielgruppen]** aufgerufen werden.

Sie wird häufig verwendet, um Zielgruppensegmente zu erfassen, die innerhalb desselben Kampagnen-Workflows erstellt wurden, und sie so für die Wiederverwendung in zukünftigen Kampagnen verfügbar zu machen. Normalerweise ist dies mit anderen Zielgruppenbestimmungsaktivitäten verbunden, z. B. **[!UICONTROL Zielgruppe erstellen]** oder **[!UICONTROL Kombinieren]**, um die endgültige Zielpopulation zu speichern.
Beachten Sie, dass Sie mit der Aktivität **[!UICONTROL Zielgruppe speichern]** eine vorhandene Zielgruppe nicht aktualisieren können. Sie können nur eine neue Zielgruppe erstellen oder eine vorhandene mit einer neuen Definition überschreiben.

## Konfigurieren der Aktivität „Zielgruppe speichern“ {#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Zielgruppe aufbauen]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL orchestrierten Kampagne]** Aktivität „Zielgruppe speichern“ hinzu.

1. Geben Sie ein **[!UICONTROL Zielgruppen-Label]** ein, das die gespeicherte Zielgruppe identifiziert.

   >[!NOTE]
   >
   >Die Zielgruppe **[!UICONTROL label]** muss in allen Kampagnen eindeutig sein. Ein Zielgruppenname, der bereits in der Aktivität „Zielgruppe speichern“ einer anderen Kampagne verwendet wurde **[!UICONTROL kann nicht]** werden.

1. Wählen Sie ein **[!UICONTROL Profilzuordnungsfeld&#x200B; aus]** Zielgruppendimension Ihrer Kampagne aus. Diese Zuordnung definiert, wie Profile in der **gespeicherten Zielgruppe** während der Ausführung mit der Zielgruppendimension der Kampagne verknüpft werden.

   Nur Zuordnungen, die mit der aktuellen Zieldimension kompatibel sind, d. h. die der eingehenden Transition, sind in der Dropdown-Liste verfügbar, um eine ordnungsgemäße Abstimmung zwischen der Audience und dem Kampagnenkontext sicherzustellen.

   ➡️ [Führen Sie die auf dieser Seite beschriebenen Schritte aus, um Ihre Zielgruppendimension für Campaign zu erstellen](../target-dimension.md)

   ![](../assets/save-audience-1.png)

1. Klicken Sie **[!UICONTROL Zielgruppenzuordnungen hinzufügen]**, um zusätzliche Daten aus Attributen der **[!UICONTROL Zielgruppendimension]** oder angereicherten **[!UICONTROL Profilattributen]** einzuschließen.

   Auf diese Weise können Sie der Aktivität **[!UICONTROL Gespeicherte Zielgruppe]** über die primäre Profilzuordnung hinaus weitere Informationen zuordnen, wodurch die Zielgruppenbestimmungs- und Personalisierungsoptionen verbessert werden.

   ![](../assets/save-audience-2.png)

1. Schließen Sie die Einrichtung ab, indem Sie die orchestrierte Kampagne speichern und veröffentlichen. Dadurch wird Ihre Zielgruppe generiert und gespeichert.

1. Veröffentlichen Sie die Kampagne für die Audience, die erstellt oder ersetzt werden soll, da die Aktivität **[!UICONTROL Audience speichern]** nicht ausgeführt wird, während sich die Kampagne im **[!UICONTROL Entwurfsmodus]** befindet.

Der Inhalt der gespeicherten Zielgruppe ist dann in der Detailansicht der Zielgruppe verfügbar. Diese kann über das Menü **[!UICONTROL Zielgruppen]** aufgerufen oder bei der Zielgruppenbestimmung ausgewählt werden, z. B. mit der Aktivität **[!UICONTROL Zielgruppe lesen]**.

![](../assets/save-audience-4.png)


## Beispiel {#save-audience-example}

Im folgenden Beispiel wird veranschaulicht, wie eine einfache Zielgruppe mithilfe von Targeting erstellt wird. Eine Abfrage identifiziert alle Empfängerinnen und Empfänger, die in den letzten 30 Tagen eine Reise gebucht haben, indem sie diese Population in Ihrer orchestrierten Kampagne filtert. Wenn Sie **Empfänger - CRMID** als **Zielgruppendimension** auswählen, richtet sich die Zielgruppe an jedes einzelne Buchungsereignis und nicht nur an den Empfänger als Ganzes. Die Aktivität **[!UICONTROL Zielgruppe speichern]** erfasst dann diese Profile, um eine wiederverwendbare Zielgruppe aus aktuellen Käuferinnen und Käufern zu erstellen.

![](../assets/save-audience-3.png)
