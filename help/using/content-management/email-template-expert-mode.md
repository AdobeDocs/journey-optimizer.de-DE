---
solution: Journey Optimizer
product: journey optimizer
title: Bearbeiten von E-Mail-Vorlagen mit dem erweiterten HTML-Editor
description: Verwenden Sie den Expertenmodus, um die HTML-Quelle für E-Mail-Inhalte im WYSIWYG-Editor mit Feature-Flag-Steuerung, Leitplanken und Speichervalidierung anzuzeigen und zu bearbeiten.
feature: Templates
topic: Content Management
role: User
hidefromtoc: true
hide: true
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: 76bb202375cdfe1c8abacc1670ba6e794175215d
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 5%

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

Wenn Sie den erweiterten HTML-Editor verwenden, sind die folgenden Leitplanken vorhanden, um die Inhaltskompatibilität zu schützen und Erwartungen festzulegen.

* Derzeit gibt es **erweiterten HTML** Editor keinen Validierungsprozess. Syntaxfehler und fehlerhafte Layouts werden nicht geprüft. Prüfen Sie Ihren Inhalt sorgfältig, bevor Sie ihn speichern.

* Bei zukünftigen Systemaktualisierungen können Änderungen am Standard-Markup rückgängig gemacht werden. Beachten Sie Folgendes **Ihre Änderungen können überschrieben**.

* Probleme, die durch benutzerdefinierten Code und manuelle Änderungen **nicht behoben werden können** oder vom [!DNL Adobe]-Supportteam behoben werden können. Stellen Sie sicher, dass Sie über eine Sicherung Ihres Inhalts verfügen, falls Sie zu einer früheren Version zurückkehren müssen.

* Um die Inhaltskompatibilität sicherzustellen, **Speichern ist nicht verfügbar** in der erweiterten HTML-Ansicht. Wenn Sie bereit sind, Ihre Änderungen zu speichern, müssen Sie zur Desktop-Ansicht zurückkehren.

>[!WARNING]
>
>Der erweiterte HTML-Editor in der Inhaltsvorlage ist nicht identisch mit dem Modus **[!UICONTROL Eigenen Code erstellen]** in der E-Mail-Designer. Im Modus [!UICONTROL Eigenen Code erstellen] können Sie nicht zum visuellen Editor zurückkehren. Sobald Sie diesen Pfad ausgewählt haben, bleiben Sie in der schreibgeschützten Bearbeitung. Der erweiterte HTML-Editor dagegen ermöglicht es Ihnen, jederzeit zwischen der HTML- und der Desktopansicht (visuell) umzuschalten. [Erfahren Sie mehr über den Code-Editor](../email/code-content.md)

## Zur erweiterten HTML-Ansicht wechseln {#switch-to-desktop-view}

1. Öffnen oder erstellen Sie eine [E-Mail](../content-management/create-content-templates.md)Vorlage und öffnen Sie die [E-Mail-Designer](../email/get-started-email-design.md), um den Inhalt zu bearbeiten.

1. Klicken Sie oben rechts **[!UICONTROL Bildschirm auf die Schaltfläche]** HTML.

   ![](assets/email-template-expert-mode-button.png)

1. Beim ersten Öffnen des erweiterten HTML-Editors wird eine Warnmeldung angezeigt. Überprüfen Sie sie sorgfältig und klicken Sie auf **[!UICONTROL OK]**, um fortzufahren. [Weitere Informationen](#guardrails)

   >[!NOTE]
   >
   >Diese Warnung wird nur angezeigt, wenn Sie den erweiterten HTML-Editor zum ersten Mal öffnen und monatlich zurücksetzen.

   ![](assets/email-template-expert-mode-warning.png){zoomable="yes"}

1. Der erweiterte HTML-Editor wird angezeigt.

   ![](assets/email-template-expert-mode.png)

1. Fügen Sie die gewünschten Änderungen an Ihrem E-Mail-Inhalt hinzu.

   >[!WARNING]
   >
   >Achten Sie darauf, den richtigen HTML- und CSS-Code einzugeben, da es keinen Syntaxvalidierungsprozess gibt und von [!DNL Adobe] keine Unterstützung bereitgestellt wird. [Weitere Informationen](#guardrails)

1. Speichern ist in der erweiterten HTML-Ansicht nicht verfügbar. Wechseln Sie zurück zur Desktop-Ansicht, um Ihre Änderungen zu speichern.

   ![](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >Inhalte können aus Gründen der Inhaltskompatibilität nur in der Desktop-Ansicht gespeichert werden. Ihre Bearbeitungen bleiben beim Wechseln der Ansichten erhalten.

1. Die Inhaltssimulation ist in der erweiterten HTML-Ansicht nicht verfügbar. Um Ihren Inhalt zu simulieren, wechseln Sie zur Desktop-Ansicht.

   ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}

