---
solution: Journey Optimizer
product: journey optimizer
title: Bearbeiten von E-Mail-Vorlagen mit dem erweiterten HTML-Editor
description: Verwenden Sie den Expertenmodus, um die HTML-Quelle für E-Mail-Inhalte im WYSIWYG-Editor mit Feature-Flag-Steuerung, Leitplanken und Speichervalidierung anzuzeigen und zu bearbeiten.
feature: Templates
topic: Content Management
role: User
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 7%

---

# Bearbeiten von E-Mail-Vorlagen mit dem erweiterten HTML-Editor {#email-template-expert-mode}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Der **erweiterte HTML-Editor** ist ein Expertenmodus, mit dem Sie den Rohcode von E-Mail-Inhaltsvorlagen direkt über die [!DNL Journey Optimizer] E-Mail-Designer-Benutzeroberfläche anzeigen und bearbeiten können.

Mit dieser Funktion können Sie erweiterte Ausdrücke - wie Bedingungen - direkt in die Quelle einfügen. Wenn Sie zur visuellen Ansicht (Desktop) zurückkehren, wird der Inhalt erneut gerendert, damit Sie überprüfen können, wie er aussieht, und die Bearbeitung in jeder Ansicht fortsetzen können.

>[!NOTE]
>
>Diese Funktion ist nur in Inhaltsvorlagen und für den E-Mail-Kanal verfügbar.

## Leitlinien {#guardrails}

Wenn Sie den erweiterten HTML-Editor verwenden, schützen die folgenden Leitplanken die Inhaltskompatibilität und definieren Erwartungen.

* Der erweiterte HTML-Editor **validiert** Code nicht. Syntaxfehler oder fehlerhafte Layouts werden nicht geprüft. Überprüfen Sie Ihre Inhalte sorgfältig, bevor Sie sie speichern.

* Zukünftige Systemaktualisierungen können Änderungen überschreiben, die Sie am Standard-Markup vornehmen. **Ihre Änderungen bleiben möglicherweise nicht erhalten**.

* Das [!DNL Adobe] Support-Team **kann keine Probleme beheben oder**), die durch benutzerdefinierten Code und manuelle Änderungen verursacht werden. Erstellen Sie eine Sicherungskopie Ihres Inhalts, für den Fall, dass Sie ihn wiederherstellen müssen.

* In der erweiterten HTML-Ansicht können keine Inhalte simuliert werden. Zur Desktop-Ansicht wechseln, um eine Vorschau des Inhalts anzuzeigen.

* Um die Inhaltskompatibilität sicherzustellen, **Sie können nicht speichern** in der erweiterten HTML-Ansicht. Wechseln Sie zurück zur Desktop-Ansicht, wenn Sie zum Speichern Ihrer Änderungen bereit sind.

>[!WARNING]
>
>Der erweiterte HTML-Editor in der Inhaltsvorlage ist nicht identisch mit dem Modus **[!UICONTROL Eigenen Code erstellen]** in der E-Mail-Designer. Im Modus [!UICONTROL Eigenen Code erstellen] können Sie nicht zum visuellen Editor zurückkehren. Sobald Sie diesen Pfad ausgewählt haben, bleiben Sie in der schreibgeschützten Bearbeitung. Der erweiterte HTML-Editor dagegen ermöglicht es Ihnen, jederzeit zwischen der HTML- und der Desktopansicht (visuell) umzuschalten. [Erfahren Sie mehr über den Code-Editor](../email/code-content.md)

## Zur erweiterten HTML-Ansicht wechseln {#switch-to-html-view}

Gehen Sie wie folgt vor, um den erweiterten HTML-Editor zu öffnen und Ihre Vorlagenquelle zu bearbeiten.

1. Öffnen oder erstellen Sie eine [E-Mail](../content-management/create-content-templates.md)Vorlage und öffnen Sie die [E-Mail-Designer](../email/get-started-email-design.md), um den Inhalt zu bearbeiten.

1. Klicken Sie oben rechts **[!UICONTROL Bildschirm auf die Schaltfläche]** HTML.

   ![Position der Schaltfläche HTML in der E-Mail-Symbolleiste von Designer](assets/email-template-expert-mode-button.png)

1. Beim ersten Öffnen des erweiterten HTML-Editors wird eine Warnmeldung angezeigt. Überprüfen Sie sie sorgfältig und klicken Sie auf **[!UICONTROL OK]**, um fortzufahren. [Weitere Informationen](#guardrails)

   ![Warndialogfeld beim erstmaligen Öffnen des erweiterten HTML-Editors](assets/email-template-expert-mode-warning.png){zoomable="yes"}

   >[!NOTE]
   >
   >Diese Warnung wird nur angezeigt, wenn Sie den erweiterten HTML-Editor zum ersten Mal öffnen und monatlich zurücksetzen.

1. Der erweiterte HTML-Editor wird angezeigt.

   ![Erweiterte HTML-Editor-Benutzeroberfläche mit Quell-Code der E-Mail-Vorlage](assets/email-template-expert-mode.png)

1. Fügen Sie die gewünschten Änderungen an Ihrem E-Mail-Inhalt hinzu.

   >[!WARNING]
   >
   >Achten Sie darauf, den richtigen HTML- und CSS-Code einzugeben, da es keinen Syntaxvalidierungsprozess gibt und von [!DNL Adobe] keine Unterstützung bereitgestellt wird. [Weitere Informationen](#guardrails)

1. Inhaltssimulation und -speicherung sind in der erweiterten HTML-Ansicht aus Kompatibilitätsgründen nicht verfügbar. Wechseln Sie zurück zur Desktop-Ansicht, um eine Vorschau Ihres Inhalts anzuzeigen und Ihre Änderungen zu speichern.

   ![Wechseln Sie zurück zur Desktop-Ansicht, um Ihre Änderungen zu speichern](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >Ihre Bearbeitungen bleiben beim Wechseln der Ansichten erhalten.

<!--
    ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}
-->

## Verwandte Themen

* [Codieren Ihres eigenen E-Mail-Inhalts](../email/code-content.md)
* [Erstellen von Inhaltsvorlagen](create-content-templates.md)
* [Erste Schritte mit dem Email Designer](../email/get-started-email-design.md)

