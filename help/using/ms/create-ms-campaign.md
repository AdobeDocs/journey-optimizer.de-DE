---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von orchestrierten Kampagnen mit Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer eine koordinierte Kampagne erstellen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 14%

---

# Erstellen einer orchestrierten Kampagne {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Liste der koordinierten Kampagnen"
>abstract="Die Registerkarte **Mehrstufig** enthält alle orchestrierten Kampagnen. Klicken Sie auf den Namen einer koordinierten Kampagne, um sie zu bearbeiten. Verwenden Sie die Schaltfläche **Orchestrierte Kampagne erstellen**, um eine neue orchestrierte Kampagne hinzuzufügen."

## Voraussetzungen

### Berechtigungen

### Einstellungen

Überblick über neue Admin-Einstellungen > Schemata, Ausführungsfelder, Zusammenführungsrichtlinie. [Weitere Informationen](ms-schemas.md)


## Erstellungsetappen

Gehen Sie wie folgt vor, um eine orchestrierte Kampagne zu erstellen:

1. Um eine **koordinierte Kampagne** zu erstellen, navigieren Sie zum Menü **Kampagnen**.

1. Klicken Sie auf **[!UICONTROL Orchestrierte Kampagne erstellen]** in der oberen rechten Ecke des Bildschirms.

1. Wählen Sie im Dialogfeld **Eigenschaften** die Vorlage aus, die zur Erstellung der orchestrierten Kampagne verwendet werden soll (Sie können auch die standardmäßige integrierte Vorlage verwenden). [Erfahren Sie mehr über orchestrierte Kampagnenvorlagen](#campaign-templates).

1. Geben Sie einen Titel für die orchestrierte Kampagne ein. Darüber hinaus empfehlen wir dringend, zu Ihrer orchestrierten Kampagne eine Beschreibung im entsprechenden Feld des Abschnitts „Zusätzliche **[!UICONTROL &quot;]** Bildschirms hinzuzufügen.

1. Erweitern Sie den Abschnitt **[!UICONTROL Zusätzliche Optionen]**, um weitere Einstellungen für die orchestrierte Kampagne zu konfigurieren.

1. Klicken Sie auf **[!UICONTROL Orchestrierte Kampagne erstellen]**, um die Erstellung Ihrer orchestrierten Kampagne zu bestätigen.

Ihre orchestrierte Kampagne wird jetzt erstellt und ist in der Liste der Workflows verfügbar. Sie können jetzt auf die visuelle Arbeitsfläche zugreifen und mit dem Hinzufügen, Konfigurieren und Orchestrieren der Aufgaben beginnen, die ausgeführt werden sollen. [Erfahren Sie, wie Sie orchestrierte Kampagnenaktivitäten ](orchestrate-activities.md).

## Arbeiten mit orchestrierten Kampagnenvorlagen {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Orchestrierte Kampagnenvorlagen"
>abstract="Orchestrierte Kampagnenvorlagen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die für die Erstellung neuer orchestrierter Kampagnen wiederverwendet werden können."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Orchestrierte Kampagneneigenschaften"
>abstract="Orchestrierte Kampagnenvorlagen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die für die Erstellung neuer orchestrierter Kampagnen wiederverwendet werden können. Geben Sie in diesem Bildschirm den Titel der orchestrierten Kampagnenvorlage ein und konfigurieren Sie deren Einstellungen wie ihren internen Namen, den Ordner und die Ausführungsordner, die Zeitzone und die Gruppe der Verantwortlichen."

Orchestrierte Kampagnenvorlagen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die für die Erstellung neuer orchestrierter Kampagnen wiederverwendet werden können. Sie können bei der Erstellung einer orchestrierten Kampagne die Vorlage der orchestrierten Kampagne in den Eigenschaften der orchestrierten Kampagne auswählen. Standardmäßig wird eine leere Vorlage bereitgestellt.

Sie können eine Vorlage aus einer vorhandenen orchestrierten Kampagne erstellen oder eine neue Vorlage von Grund auf neu erstellen. Beide Methoden werden nachfolgend beschrieben.

>[!BEGINTABS]

>[!TAB Erstellen Sie eine Vorlage aus einer vorhandenen orchestrierten Kampagne]

Gehen Sie wie folgt vor, um eine orchestrierte Kampagnenvorlage aus einer vorhandenen orchestrierten Kampagne zu erstellen:

1. Öffnen Sie das Menü **Kampagne** und navigieren Sie zur orchestrierten Kampagne, um sie als Vorlage zu speichern.
1. Klicken Sie auf die drei Punkte rechts neben dem Namen der orchestrierten Kampagne und wählen Sie **Als Vorlage kopieren**.
1. Bestätigen Sie im Popup-Fenster die Vorlagenerstellung.
1. Markieren, fügen Sie die Aktivitäten auf der Arbeitsfläche der orchestrierten Kampagnenvorlage nach Bedarf hinzu und konfigurieren Sie sie.
1. Navigieren Sie über die Schaltfläche **Einstellungen** zum Namen der orchestrierten Kampagnenvorlage und geben Sie eine Beschreibung ein.
1. Wählen Sie den **Ordner** und den **Ausführungsordner** der Vorlage aus. Der Ordner ist der Speicherort, an dem die orchestrierte Kampagnenvorlage gespeichert wird. Der Ausführungsordner ist der Ordner, in dem die auf dieser Vorlage basierenden orchestrierten Kampagnen gespeichert werden.
1. Speichern Sie Ihre Änderungen.

Die orchestrierte Kampagnenvorlage ist jetzt in der Vorlagenliste verfügbar. Sie können eine auf dieser Vorlage basierende orchestrierte Kampagne erstellen. Diese orchestrierte Kampagne wird mit den in der Vorlage definierten Einstellungen und Aktivitäten vorkonfiguriert.


>[!TAB Erstellen einer Vorlage von Grund auf]


Gehen Sie wie folgt vor, um eine neue orchestrierte Kampagnenvorlage zu erstellen:

1. Öffnen Sie das Menü **Kampagne** und navigieren Sie zur Registerkarte **Vorlagen**. Eine Liste der verfügbaren orchestrierten Kampagnenvorlagen wird angezeigt.
1. Klicken Sie auf **[!UICONTROL Vorlage erstellen]** in der rechten oberen Ecke des Bildschirms.
1. Geben Sie den Titel ein und öffnen Sie die zusätzlichen Optionen, um eine Beschreibung Ihrer orchestrierten Kampagnenvorlage einzugeben.
1. Wählen Sie den Ordner und den Ausführungsordner der Vorlage aus. Der Ordner ist der Speicherort, an dem die orchestrierte Kampagnenvorlage gespeichert wird. Der Ausführungsordner ist der Ordner, in dem die auf dieser Vorlage basierenden orchestrierten Kampagnen gespeichert werden.
1. Klicken Sie anschließend auf die Schaltfläche **Erstellen**, um Ihre Einstellungen zu bestätigen.
1. Fügen Sie auf der Arbeitsfläche für orchestrierte Kampagnenvorlagen die Aktivitäten nach Bedarf hinzu und konfigurieren Sie sie.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Speichern Sie Ihre Änderungen.

Die orchestrierte Kampagnenvorlage ist jetzt in der Vorlagenliste verfügbar. Sie können eine auf dieser Vorlage basierende orchestrierte Kampagne erstellen. Diese orchestrierte Kampagne wird mit den in der Vorlage definierten Einstellungen und Aktivitäten vorkonfiguriert.

>[!ENDTABS]
