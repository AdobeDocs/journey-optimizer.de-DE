---
title: Erste Schritte mit der Genehmigung von Journey und Kampagnen
description: Erfahren Sie, wie Sie einen Validierungsprozess für Ihre Journey und Kampagnen einrichten.
role: User
level: Beginner
feature: Approval
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: a3a0820565bbd8b2d8d0ce37e5b3e5ad37b064cf
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 18%

---


# Erste Schritte mit der Genehmigung von Journey und Kampagnen {#send-proofs}

>[!AVAILABILITY]
>
> Genehmigungsrichtlinien sind derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.

## Erste Schritte mit Validierungsrichtlinien {#gs}

Mit Journey Optimizer können Sie einen Validierungsprozess einrichten, der es Marketing-Teams ermöglicht, sicherzustellen, dass Kampagnen und Journey von den jeweiligen Interessenträgern geprüft und signiert werden, bevor sie live geschaltet werden.

Genehmigungsrichtlinien führen einen strukturierten Workflow direkt in der Benutzeroberfläche ein, wodurch externe Medien wie E-Mail- oder Aufgabenverwaltungswerkzeuge entfallen und alle Genehmigungen zentral verwaltet und verfolgt werden.

Darüber hinaus bietet diese Funktion eine verbesserte Kontrolle über die Veröffentlichung Ihrer Journey und Kampagnen: Durch den in Journey Optimizer eingebetteten Genehmigungsprozess bleiben Kampagnen und Journey während der Überprüfung in einem &quot;gesperrten&quot;Status, sodass keine Änderungen oder unbeabsichtigten Aktivierungen vorgenommen werden, bevor alle erforderlichen Genehmigungen erteilt werden.

## Voraussetzungen {#prerequisites}

Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Berechtigungen konfiguriert wurden.

Um auf Journey und Kampagnen zugreifen und diese veröffentlichen zu können, müssen Benutzer über die Berechtigungen **Kampagnen genehmigen und veröffentlichen** und **Journey genehmigen und veröffentlichen** verfügen. [Weitere Informationen](../administration/permissions.md)

+++  Erfahren Sie, wie Sie genehmigungsbezogene Berechtigungen zuweisen

1. Gehen Sie im Produkt **Berechtigungen** zur Registerkarte **Rollen** und wählen Sie die gewünschte **Rolle** aus.

1. Klicken Sie auf **Bearbeiten**, um die Berechtigungen zu ändern.

1. Fügen Sie die Ressource **Kampagnen** hinzu und wählen Sie dann **Kampagnen genehmigen und veröffentlichen** aus dem Dropdownmenü aus.

   ![](assets/permissions_approval.png){zoomable="yes"}

1. Fügen Sie die Ressource **Journey** hinzu und wählen Sie dann **Journey genehmigen und veröffentlichen** aus dem Dropdownmenü aus.

   ![](assets/permissions_approval_2.png){zoomable="yes"}

1. Klicken Sie auf **Speichern**, um die Änderungen anzuwenden.

Die Berechtigungen aller Benutzenden, die dieser Rolle bereits zugewiesen sind, werden automatisch aktualisiert.

1. Um diese Rolle neuen Benutzenden zuzuweisen, navigieren Sie im Dashboard **Rollen** zur Registerkarte **Benutzer** und klicken Sie auf **Benutzer hinzufügen**.

1. Geben Sie den Namen und die E-Mail-Adresse der Benutzerin oder des Benutzers ein oder wählen Sie aus der Liste aus und klicken Sie dann auf **Speichern**.

1. Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie [diese Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/users).

Die Benutzerin oder der Benutzer erhält eine E-Mail mit Anweisungen zum Zugriff auf Ihre Instanz.

+++

## Übersicht über den Genehmigungsprozess {#process}

Der globale Validierungsprozess sieht wie folgt aus:

![](assets/approval-process.png){zoomable="yes"}

1. **Einrichten von Genehmigungsrichtlinien**

   Administratoren erstellen eine Genehmigungsrichtlinie, in der die Bedingungen definiert werden, unter denen die Richtlinie auf Journey oder Kampagnen angewendet werden soll. Sie können beispielsweise eine Validierungsrichtlinie erstellen, die es erfordert, dass alle von einem bestimmten Benutzer erstellten geplanten Kampagnen vor der Aktivierung genehmigt werden. [Erfahren Sie, wie Sie Genehmigungsrichtlinien erstellen](approval-policies.md)

1. **Kampagnen-/Journey-Übermittlung zur Genehmigung**

   Die Kampagnen-/Journey-Ersteller erstellen eine Journey oder Kampagne und senden sie zur Genehmigung. Die Kampagne/Journey wechselt in den Status &quot;In Überprüfung&quot;, während der keine Änderungen vorgenommen werden können, es sei denn, die Anfrage wird abgebrochen. [Erfahren Sie, wie Sie eine Genehmigung anfordern](request-approval.md)

   >[!NOTE]
   >
   >Kampagnen und Journey müssen nur dann zur Genehmigung eingereicht werden, wenn eine Validierungsrichtlinie vorhanden ist. Wenn keine solche Richtlinie zutrifft, kann der Ersteller die Kampagne oder Journey direkt veröffentlichen, ohne dass eine Genehmigung erforderlich ist.

1. **Überprüfen und Genehmigen**

   Der/die Genehmiger, der/die in der Validierungsrichtlinie für die Journey oder Kampagne definiert ist/sind, erhält/erhalten eine Benachrichtigung. Sie können den Journey- oder Kampagneninhalt, die Zielgruppe und die Einstellungen überprüfen. Wenn Änderungen erforderlich sind, fordert der Genehmiger sie an und gibt die Kampagne für Revisionen an &quot;Entwurf&quot;zurück. Wenn sie bereit sind, können sie die Journey oder Kampagne aktivieren und starten. [Erfahren Sie, wie Sie eine Anforderung überprüfen und genehmigen](review-approve-request.md)

## Überwachen von Genehmigungsanfragen {#monitor}

Sie können alle Genehmigungs- und Änderungsanfragen überwachen, die für eine bestimmte Journey oder Kampagne eingereicht wurden. Klicken Sie dazu auf das Symbol **[!UICONTROL Audit-Protokoll anzeigen]** oben rechts auf der Journey-Arbeitsfläche oder im Bildschirm zur Kampagnenüberprüfung.

![](assets/monitor-requests.png)
