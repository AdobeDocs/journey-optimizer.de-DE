---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Zielgruppe speichern“
description: Informationen zur Verwendung der Aktivität „Zielgruppe speichern“ in einer orchestrierten Kampagne
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/YBp0ehescfw8tVa1pJD2YQuQqRXJ9iG8nDDq9FKzHPs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: b423a773-0a58-4a77-b65d-3dd4ae6ef841
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 548
ht-degree: 81%

---

# Speichern einer Zielgruppe {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Aktivität „Zielgruppe speichern“"
>abstract="Die Aktivität **Zielgruppe speichern** ist eine **Targeting**-Aktivität, mit der Sie eine vorhandene Zielgruppe aktualisieren oder eine neue Zielgruppe aus der zuvor in der orchestrierten Kampagne generierten Population erstellen können. Nach der Erstellung werden diese Zielgruppen zur Liste der Anwendungszielgruppen hinzugefügt und können über das Menü **Zielgruppen** aufgerufen werden."

Die Aktivität **[!UICONTROL Zielgruppe speichern]** ist eine **[!UICONTROL Targeting]**-Aktivität, mit der basierend auf der zuvor in der orchestrierten Kampagne generierten Population eine neue Zielgruppe erstellt oder eine vorhandene aktualisiert wird. Nach dem Speichern werden diese Zielgruppen zur Liste der Anwendungszielgruppen hinzugefügt und können über das Menü **[!UICONTROL Zielgruppen]** aufgerufen werden.

Sie wird häufig verwendet, um Zielgruppensegmente zu erfassen, die innerhalb desselben Kampagnen-Workflows erstellt wurden, und sie so für die Wiederverwendung in zukünftigen Kampagnen verfügbar zu machen. Normalerweise ist dies mit anderen Zielgruppenbestimmungsaktivitäten verbunden, z. B. **[!UICONTROL Zielgruppe erstellen]** oder **[!UICONTROL Kombinieren]**, um die endgültige Zielpopulation zu speichern.
Beachten Sie, dass Sie mit der Aktivität **[!UICONTROL Zielgruppe speichern]** eine vorhandene Zielgruppe nicht aktualisieren können. Sie können nur eine neue Zielgruppe erstellen oder eine vorhandene mit einer neuen Definition überschreiben.

## Konfigurieren der Aktivität „Zielgruppe speichern“ {#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Zielgruppe aufbauen]** zu konfigurieren:

1. Fügen Sie Ihrer orchestrierten Kampagne eine Aktivität des Typs **[!UICONTROL Zielgruppe speichern]** hinzu.

1. Geben Sie ein **[!UICONTROL Zielgruppen-Label]** ein, das die gespeicherte Zielgruppe identifiziert.

   >[!NOTE]
   >
   >Das **[!UICONTROL Zielgruppen-Label]** muss in allen Kampagnen eindeutig sein. Sie können keinen Zielgruppennamen wiederverwenden, der bereits in der Aktivität **[!UICONTROL Zielgruppe speichern]** einer anderen Kampagne genutzt wird.

1. Wählen Sie ein **[!UICONTROL Profil-Mapping-Feld]** aus der Zielgruppendimension Ihrer Kampagne aus. Diese Zuordnung definiert, wie Profile in der **gespeicherten Zielgruppe** bei der Ausführung mit der Zieldimension der Kampagne verknüpft werden.

   Um eine ordnungsgemäße Abstimmung zwischen der Zielgruppe und dem Kampagnenkontext sicherzustellen, sind in der Dropdown-Liste nur Zuordnungen verfügbar, die mit der aktuellen Zieldimension kompatibel sind, d. h. mit der der eingehenden Transition.

   ➡️ [Führen Sie die auf dieser Seite beschriebenen Schritte aus, um die Zielgruppendimension für Ihre Kampagne zu erstellen.](../target-dimension.md)

   ![](../assets/save-audience-1.png)

1. Klicken Sie auf **[!UICONTROL Zielgruppenzuordnungen hinzufügen]**, um zusätzliche Daten aus Attributen der **[!UICONTROL Zieldimension]** oder aus angereicherten **[!UICONTROL Profilattributen]** einzuschließen.

   So können Sie der Aktivität **[!UICONTROL Gespeicherte Zielgruppe]** über die primäre Profilzuordnung hinaus weitere Informationen zuordnen, wodurch die Targeting- und Personalisierungsoptionen verbessert werden.

   ![](../assets/save-audience-2.png)

1. Schließen Sie die Einrichtung ab, indem Sie die orchestrierte Kampagne speichern und veröffentlichen. Dadurch wird Ihre Zielgruppe generiert und gespeichert.

1. Veröffentlichen Sie die Kampagne für die Zielgruppe, die erstellt oder ersetzt werden soll, da die Aktivität **[!UICONTROL Zielgruppe speichern]** nicht ausgeführt wird, während sich die Kampagne im **[!UICONTROL Entwurfsmodus]** befindet.

>[!NOTE]
>
>Zum Zeitpunkt der Veröffentlichung werden **[!UICONTROL Zielgruppe speichern]**-Aktivitäten immer vor den Nachrichtenaktivitäten im Workflow ausgeführt. Die Audience-Shell wird erstellt und Profile beginnen mit der Aufnahme in das Audience Portal, bevor die Verarbeitung einer Kanalaktivität beginnt. [Erfahren Sie mehr über die Ausführungssequenz zur Veröffentlichungszeit](../start-monitor-campaigns.md#publication-sequence)

Der Inhalt der gespeicherten Zielgruppe ist dann in der Detailansicht der Zielgruppe verfügbar. Diese kann über das Menü **[!UICONTROL Zielgruppen]** aufgerufen oder bei der Zielgruppenbestimmung ausgewählt werden, z. B. mit der Aktivität **[!UICONTROL Zielgruppe lesen]**.

![](../assets/save-audience-4.png)

>[!NOTE]
>
>Wenn Ihre Zielgruppendefinition Experience Platform-Schemaattribute verwendet, die mit Datennutzungskennzeichnungen (DULE) gekennzeichnet sind, werden diese Kennzeichnungen automatisch von der gespeicherten Zielgruppe übernommen. Sie müssen sie nicht erneut anwenden. [Weitere Informationen zu Data Governance](../../action/action-privacy.md)

## Beispiel {#save-audience-example}

Im folgenden Beispiel wird veranschaulicht, wie eine einfache Zielgruppe mithilfe von Targeting erstellt wird. Eine Abfrage identifiziert alle Empfängerinnen und Empfänger, die in den letzten 30 Tagen eine Reise gebucht haben, indem sie diese Population in Ihrer orchestrierten Kampagne filtert. Wenn Sie **Empfänger – CRMID** als **Zielgruppendimension** auswählen, richtet sich die Zielgruppe an jedes einzelne Buchungsereignis und nicht nur an die Empfängerin bzw. den Empfänger als Ganzes. Die Aktivität **[!UICONTROL Zielgruppe speichern]** erfasst dann diese Profile, um eine wiederverwendbare Zielgruppe aus kürzlichen Käuferinnen und Käufern zu erstellen.

![](../assets/save-audience-3.png)
