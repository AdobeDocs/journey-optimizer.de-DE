---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Abstimmung“
description: Erfahren Sie, wie Sie die Aktivität Abstimmung in einer orchestrierten Kampagne verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: a6b293a5eb1358f692d53c9611b794cf8f7fc753
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 76%

---

# Abstimmung {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Aktivität „Abstimmung“"
>abstract="Die Aktivität **Abstimmung** ist eine Aktivität zur **Zielgruppenbestimmung**, mit der Sie die Verknüpfung zwischen den Daten in der Adobe Campaign-Datenbank und den Daten in einer Arbeitstabelle definieren können."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Abstimmung – Feld auswählen"
>abstract="Abstimmung – Feld auswählen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Abstimmung – Bedingung erstellen"
>abstract="Abstimmung – Bedingung erstellen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Abstimmung – Komplement erzeugen"
>abstract="Abstimmung – Komplement erzeugen"

Die Aktivität **Abstimmung** ist eine **Targeting**-Aktivität, mit der Sie die Relation zwischen den Daten in Adobe Journey Optimizer und den Daten in einer Arbeitstabelle definieren können, z. B. Daten, die aus einer externen Datei geladen wurden.

## Best Practices {#reconciliation-best-practices}

Mit der Aktivität **Anreicherung** können Sie zusätzliche Daten definieren, die in einer orchestrierten Kampagne verarbeitet werden sollen. Mit der Aktivität **Anreicherung** können Sie Daten aus mehreren Datensätzen kombinieren oder Links zu einer temporären Ressource erstellen. Dagegen ermöglicht Ihnen die Aktivität **Abstimmung** die Verknüpfung nicht identifizierter Daten mit vorhandenen Ressourcen.

>[!NOTE]
>Der Abstimmungsvorgang setzt voraus, dass die Daten der verknüpften Dimensionen bereits in der Datenbank vorhanden sind. Wenn Sie beispielsweise eine Datei mit Kaufdaten importieren möchten, in der verzeichnet ist, welches Produkt wann von welcher Kundin und welchem Kunden gekauft wurde, müssen sowohl das Produkt als auch die Person bereits in der Datenbank angelegt sein.

## Konfigurieren der Abstimmungsaktivität {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Zielgruppendimension"
>abstract="Wählen Sie die neue Zielgruppendimension aus. Mit einer Dimension können Sie die Zielpopulation definieren: Empfängerinnen und Empfänger, Abonnentinnen und Abonnenten der App, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw. Standardmäßig ist die aktuelle Zielgruppendimension ausgewählt."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Abstimmregeln"
>abstract="Wählen Sie die für die Deduplizierung zu verwendenden Abstimmungsregeln aus. Um Attribute zu verwenden, wählen Sie die Option **Einfache Attribute** und dann die Quell- und Zielfelder aus. Um mithilfe des Abfrage-Modelers eine eigene Abstimmbedingung zu erstellen, wählen Sie die Option **Erweiterte Abstimmbedingungen** aus."
>additional-url="https://experienceleague.adobe.com/de/docs/campaign-web/v8/query-database/query-modeler-overview" text="Arbeiten mit dem Abfrage-Modeler"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Auswählen der Zielgruppendimension"
>abstract="Wählen Sie die Zielgruppendimension für Ihre eingehenden Daten zum Abstimmen aus."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=de#targeting-dimensions" text="Zielgruppendimensionen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Beibehalten nicht abgestimmter Daten"
>abstract="Standardmäßig werden nicht abgestimmte Daten in der ausgehenden Transition beibehalten und stehen in der Arbeitstabelle zur späteren Verwendung zur Verfügung. Um nicht abgestimmte Daten zu entfernen, deaktivieren Sie die Option **Nicht abgestimmte Daten beibehalten**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Abstimmattribut"
>abstract="Wählen Sie das Attribut aus, das zur Abstimmung der Daten verwendet werden soll, und klicken Sie auf „Bestätigen“."

Gehen Sie wie folgt vor, um die Aktivität **Abstimmung** zu konfigurieren:

1. Fügen Sie **orchestrierten Kampagne** Aktivität „Abstimmung“ hinzu.

1. Wählen Sie die neue Zielgruppendimension aus. Mit einer Dimension können Sie die Zielpopulation definieren: Empfänger, App-Abonnenten, Benutzer, Abonnenten usw.

1. Wählen Sie die für Abstimmung zu verwendenden Felder aus. Sie können mehrere Abstimmkriterien verwenden.

   1. Um Datenabstimmungsattribute zu verwenden, wählen Sie die Option **Einfache Attribute**. Das Feld **Quelle** enthält die in der eingehenden Transition zur Verfügung stehenden Felder, die abgestimmt werden sollen. Das Feld **Ziel** entspricht den Feldern der ausgewählten Zielgruppendimension. Daten werden abgestimmt, wenn Quelle und Ziel gleich sind. Wählen Sie beispielsweise die **E-Mail**-Felder, um Profile anhand ihrer E-Mail-Adresse zu deduplizieren.

      Um weitere Abstimmungskriterien hinzuzufügen, klicken Sie auf die Schaltfläche **Regel hinzufügen**. Wenn mehrere Bedingungen für die Verknüpfung angegeben werden, müssen ALLE erfüllt sein, damit die Relation hergestellt werden kann.

      ![](../assets/workflow-reconciliation-criteria.png)

   1. Um andere Attribute zur Datenabstimmung zu verwenden, wählen Sie die Option **Erweiterte Abstimmungsbedingungen**. Anschließend können Sie mit dem Abfrage-Modellierer eine eigene Abstimmbedingung erstellen.

1. Mithilfe der Schaltfläche **Filter erstellen** können Sie die abzustimmenden Daten filtern. Auf diese Weise können Sie mithilfe des Abfrage-Modelers eine benutzerdefinierte Bedingung erstellen.

Standardmäßig werden nicht abgestimmte Daten in der ausgehenden Transition beibehalten und stehen in der Arbeitstabelle zur zukünftigen Verwendung zur Verfügung. Um nicht abgestimmte Daten zu entfernen, deaktivieren Sie die Option **Nicht abgestimmte Daten beibehalten**.
