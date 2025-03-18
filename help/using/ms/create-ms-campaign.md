---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen mehrstufiger Kampagnen mit Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer eine mehrstufige Kampagne erstellen
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 271c4739a5537a99da981913606bc9eb099b5139
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 31%

---

# Erstellen einer orchestrierten Kampagne {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Liste der mehrstufigen Kampagnen"
>abstract="Unter der Registerkarte **mehrstufig** werden alle mehrstufigen Kampagnen aufgelistet. Klicken Sie auf den Namen einer mehrstufigen Kampagne, um sie zu bearbeiten. Über die Schaltfläche **Mehrstufige Kampagne erstellen** können Sie eine neue mehrstufige Kampagne hinzufügen."

## Voraussetzungen

### Berechtigungen

### Einstellungen

Überblick über neue Admin-Einstellungen > Schemata, Ausführungsfelder, Zusammenführungsrichtlinie. [Weitere Informationen](ms-schemas.md)


## Erstellungsetappen

Gehen Sie wie folgt vor, um eine mehrstufige Kampagne zu erstellen:

1. Um eine **mehrstufige Kampagne** zu erstellen, navigieren Sie zum Menü **Kampagnen**.

1. Klicken Sie auf **[!UICONTROL Mehrstufige Kampagne erstellen]** in der rechten oberen Ecke des Bildschirms.

1. Wählen Sie im Dialogfeld **Eigenschaften** die Vorlage aus, die zur Erstellung der mehrstufigen Kampagne verwendet werden soll (Sie können auch die standardmäßige integrierte Vorlage verwenden). [Erfahren Sie mehr über mehrstufige Kampagnenvorlagen](#campaign-templates).

1. Geben Sie einen Titel für die mehrstufige Kampagne ein. Darüber hinaus empfehlen wir dringend, zu Ihrer mehrstufigen Kampagne im entsprechenden Feld des Abschnitts **[!UICONTROL Zusätzliche Optionen]** eine Beschreibung hinzuzufügen.

1. Erweitern Sie den Abschnitt **[!UICONTROL Zusätzliche Optionen]**, um weitere Einstellungen für die mehrstufige Kampagne zu konfigurieren.

1. Klicken Sie auf **[!UICONTROL Schaltfläche Mehrstufige Kampagne erstellen]**, um die Erstellung Ihrer mehrstufigen Kampagne zu bestätigen.

Ihre mehrstufige Kampagne ist jetzt erstellt und in der Liste der Workflows verfügbar. Sie können jetzt auf die visuelle Arbeitsfläche zugreifen und mit dem Hinzufügen, Konfigurieren und Orchestrieren der Aufgaben beginnen, die ausgeführt werden sollen. [Erfahren Sie, wie Sie mehrstufige Kampagnenaktivitäten ](orchestrate-activities.md).

## Arbeiten mit Vorlagen für mehrstufige Kampagnen {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Vorlagen für mehrstufige Kampagnen"
>abstract="Vorlagen für mehrstufige Kampagnen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die zur Erstellung neuer mehrstufiger Kampagnen wiederverwendet werden können."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Eigenschaften mehrstufiger Kampagnen"
>abstract="Vorlagen für mehrstufige Kampagnen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die zur Erstellung neuer mehrstufiger Kampagnen wiederverwendet werden können. Geben Sie in diesem Bildschirm den Titel der Workflow-Vorlage ein und konfigurieren Sie die zugehörigen Einstellungen wie den internen Namen, den Ordner und die Ausführungsordner, die Zeitzone und die Gruppe der Verantwortlichen."

Vorlagen für mehrstufige Kampagnen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die zur Erstellung neuer mehrstufiger Kampagnen wiederverwendet werden können. Sie können bei der Erstellung einer mehrstufigen Kampagne die Vorlage Ihrer mehrstufigen Kampagne aus den Eigenschaften der mehrstufigen Kampagne auswählen. Standardmäßig wird eine leere Vorlage bereitgestellt.

Sie können eine Vorlage aus einer vorhandenen mehrstufigen Kampagne erstellen oder eine neue Vorlage von Grund auf neu erstellen. Beide Methoden werden nachfolgend beschrieben.

>[!BEGINTABS]

>[!TAB Erstellen Sie eine Vorlage aus einer vorhandenen mehrstufigen Kampagne]

Gehen Sie wie folgt vor, um eine mehrstufige Kampagnenvorlage aus einer vorhandenen mehrstufigen Kampagne zu erstellen:

1. Öffnen Sie das Menü **Kampagne** und navigieren Sie zur mehrstufigen Kampagne, um sie als Vorlage zu speichern.
1. Klicken Sie auf die drei Punkte rechts neben dem Namen der mehrstufigen Kampagne und wählen Sie **Als Vorlage kopieren**.
1. Bestätigen Sie im Popup-Fenster die Vorlagenerstellung.
1. Markieren, fügen Sie die Aktivitäten auf der mehrstufigen Kampagnenvorlagen-Arbeitsfläche nach Bedarf hinzu und konfigurieren Sie sie.
1. Navigieren Sie über die Schaltfläche **Einstellungen** zu den Einstellungen, um den Namen der mehrstufigen Kampagnenvorlage zu ändern, und geben Sie eine Beschreibung ein.
1. Wählen Sie den **Ordner** und den **Ausführungsordner** der Vorlage aus. Der Ordner ist der Speicherort, an dem die mehrstufige Kampagnenvorlage gespeichert wird. Der Ausführungsordner ist der Ordner, in dem basierend auf dieser Vorlage erstellte mehrstufige Kampagnen gespeichert werden.
1. Speichern Sie Ihre Änderungen.

Die mehrstufige Kampagnenvorlage ist jetzt in der Vorlagenliste verfügbar. Basierend auf dieser Vorlage können Sie eine mehrstufige Kampagne erstellen. Diese mehrstufige Kampagne wird mit den in der Vorlage definierten Einstellungen und Aktivitäten vorkonfiguriert.


>[!TAB Erstellen einer Vorlage von Grund auf]


Gehen Sie wie folgt vor, um eine mehrstufige Kampagnenvorlage von Grund auf zu erstellen:

1. Öffnen Sie das Menü **Kampagne** und navigieren Sie zur Registerkarte **Vorlagen**. Sie können die Liste der verfügbaren mehrstufigen Kampagnenvorlagen anzeigen.
1. Klicken Sie auf **[!UICONTROL Vorlage erstellen]** in der rechten oberen Ecke des Bildschirms.
1. Geben Sie den Titel ein und öffnen Sie die zusätzlichen Optionen, um eine Beschreibung Ihrer mehrstufigen Kampagnenvorlage einzugeben.
1. Wählen Sie den Ordner und den Ausführungsordner der Vorlage aus. Der Ordner ist der Speicherort, an dem die mehrstufige Kampagnenvorlage gespeichert wird. Der Ausführungsordner ist der Ordner, in dem basierend auf dieser Vorlage erstellte mehrstufige Kampagnen gespeichert werden.
1. Klicken Sie anschließend auf die Schaltfläche **Erstellen**, um Ihre Einstellungen zu bestätigen.
1. Fügen Sie der mehrstufigen Kampagnenvorlagen-Arbeitsfläche die Aktivitäten hinzu und konfigurieren Sie sie nach Bedarf.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Speichern Sie Ihre Änderungen.

Die mehrstufige Kampagnenvorlage ist jetzt in der Vorlagenliste verfügbar. Basierend auf dieser Vorlage können Sie eine mehrstufige Kampagne erstellen. Diese mehrstufige Kampagne wird mit den in der Vorlage definierten Einstellungen und Aktivitäten vorkonfiguriert.

>[!ENDTABS]
