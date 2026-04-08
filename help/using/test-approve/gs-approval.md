---
title: Erste Schritte mit Journey- und Kampagnengenehmigungen
description: Erfahren Sie, wie Sie einen Genehmigungsprozess für Ihre Journeys und Kampagnen einrichten.
role: User
level: Beginner
feature: Approval
exl-id: 92d1439e-5cac-4e7d-85f8-ebf432e9ef7c
source-git-commit: 58d83c2d3c6c1d3b3c680e394323de33321eeb6e
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 53%

---

# Erste Schritte mit Journey- und Kampagnengenehmigungen {#send-proofs}

## Erste Schritte mit Genehmigungsrichtlinien {#gs}

Mit [!DNL Journey Optimizer] können Sie einen Validierungsprozess einrichten, mit dem Marketing-Teams sicherstellen können, dass Kampagnen und Journey von den entsprechenden Stakeholdern geprüft und abgemeldet werden, bevor sie live geschaltet werden.

Genehmigungsrichtlinien führen einen strukturierten Workflow direkt in der Benutzeroberfläche ein. Dadurch entfällt die Notwendigkeit externer Medien wie E-Mail oder Aufgaben-Management-Tools und es wird sichergestellt, dass alle Genehmigungen zentral verwaltet und verfolgt werden.

Darüber hinaus bietet diese Funktion eine verbesserte Kontrolle über die Veröffentlichung Ihrer Journeys und Kampagnen: Durch den in Journey Optimizer eingebetteten Genehmigungsprozess bleiben Kampagnen und Journeys während der Überprüfung in einem „gesperrten“ Status, sodass keine Änderungen oder unbeabsichtigten Aktivierungen vorgenommen werden können, bevor alle erforderlichen Genehmigungen erteilt wurden.

## Voraussetzungen {#prerequisites}

Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Berechtigungen konfiguriert wurden.

Um Journey und Kampagnen zu genehmigen und zu veröffentlichen, müssen Benutzenden die Berechtigungen **Genehmigen und veröffentlichen** und **Journey genehmigen und**) gewährt werden. [Weitere Informationen](../administration/permissions.md)

+++  Erfahren Sie, wie Sie genehmigungsbezogene Berechtigungen zuweisen

1. Gehen Sie im Produkt **Berechtigungen** zur Registerkarte **Rollen** und wählen Sie die gewünschte **Rolle** aus.

1. Klicken Sie auf **Bearbeiten**, um die Berechtigungen zu ändern.

1. Fügen Sie die Ressource **Kampagnen** hinzu und wählen Sie dann **Kampagnen genehmigen und veröffentlichen** aus dem Dropdown-Menü aus.

   ![Berechtigung zum Zuweisen, Genehmigen und Veröffentlichen ](assets/permissions_approval.png){zoomable="yes"}

1. Fügen Sie die Ressource **Journey** hinzu und wählen Sie dann **Journeys genehmigen und veröffentlichen** aus dem Dropdown-Menü aus.

   ![Berechtigung zum Zuweisen und Genehmigen von Journey](assets/permissions_approval_2.png){zoomable="yes"}

1. Klicken Sie auf **Speichern**, um die Änderungen anzuwenden.

Die Berechtigungen aller Benutzenden, die dieser Rolle bereits zugewiesen sind, werden automatisch aktualisiert.

1. Um diese Rolle neuen Benutzenden zuzuweisen, navigieren Sie im Dashboard **Rollen** zur Registerkarte **Benutzer** und klicken Sie auf **Benutzer hinzufügen**.

1. Geben Sie den Namen und die E-Mail-Adresse der Benutzerin oder des Benutzers ein oder wählen Sie aus der Liste aus und klicken Sie dann auf **Speichern**.

1. Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie [diese Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/users).

Die Benutzerin oder der Benutzer erhält eine E-Mail mit Anweisungen zum Zugriff auf Ihre Instanz.

+++

## Überblick über den Genehmigungsprozess {#process}

Der globale Genehmigungsprozess sieht folgendermaßen aus:

![Genehmigungsprozess](assets/approval-process.png){zoomable="yes"}

1. **Einrichtung von Genehmigungsrichtlinien**

   Ein Administrator erstellt eine Validierungsrichtlinie und definiert Bedingungen, unter denen die Richtlinie auf Journey oder Kampagnen angewendet werden soll. Sie können beispielsweise eine Validierungsrichtlinie erstellen, die erfordert, dass alle von einem bestimmten Benutzer erstellten geplanten Kampagnen vor der Aktivierung genehmigt werden. [Informationen zur Erstellung von Genehmigungsrichtlinien](approval-policies.md)

1. **Einreichung von Kampagnen/Journeys zur Genehmigung**

   Die Kampagnen-/Journey-Ersteller erstellen eine Journey oder Kampagne und reichen sie zur Genehmigung ein. Die Kampagne/Journey wechselt in den Status „Wird überprüft“. In diesem Status können keine Änderungen vorgenommen werden, es sei denn, die Anfrage wird abgebrochen. [Informationen zum Anfordern einer Genehmigung](request-approval.md)

   >[!NOTE]
   >
   >Kampagnen und Journeys müssen nur dann zur Genehmigung eingereicht werden, wenn eine Genehmigungsrichtlinie vorhanden ist. Wenn keine solche Richtlinie zutrifft, können erstellende Personen die Kampagne oder Journey direkt veröffentlichen, ohne dass eine Genehmigung erforderlich ist.

1. **Überprüfung und Genehmigung**

   Die genehmigenden Personen, die in der Genehmigungsrichtlinie für die Journey oder Kampagne definiert sind, erhalten eine Benachrichtigung. Sie können den Journey- oder Kampagneninhalt, die Zielgruppe und die Einstellungen überprüfen. Wenn Änderungen erforderlich sind, fordern die genehmigenden Personen diese an und setzen die Kampagne für Revisionen auf „Entwurf“ zurück. Wenn sie bereit sind, können sie die Journey oder Kampagne aktivieren und starten. [Informationen zur Überprüfung und Genehmigung einer Anfrage](review-approve-request.md)

## Überwachen von Genehmigungsanfragen {#monitor}

Sie können alle Genehmigungs- und Änderungsanfragen überwachen, die für eine bestimmte Journey oder Kampagne eingereicht wurden. Klicken Sie dazu oben rechts auf der Journey-Arbeitsfläche oder am Bildschirm zur Kampagnenüberprüfung auf das Symbol **[!UICONTROL Audit-Protokoll anzeigen]**.

![Audit-Protokoll für Genehmigungsanfragen](assets/monitor-requests.png)

## Häufig gestellte Fragen {#faq}

+++Muss ich für jede Kampagne oder Journey eine Validierungsrichtlinie erstellen?

Nein. Genehmigungsrichtlinien sind bedingt. Sie müssen nur eine Richtlinie erstellen, wenn Sie die Überprüfung für eine bestimmte Kampagnengruppe oder Journey erzwingen möchten (z. B. für alle geplanten Kampagnen, die von einem bestimmten Team erstellt wurden). Wenn für eine Kampagne oder Journey keine Richtlinie gilt, kann der Ersteller bzw. die Erstellerin direkt veröffentlichen, ohne die Genehmigung anzufordern.

+++

+++Was passiert, wenn die genehmigende Person nicht verfügbar ist?

Die Anfrage bleibt „In Prüfung“, bis eine genehmigende Person tätig wird. Sie können die Anfrage abbrechen (das Element an „Entwurf“ zurückgeben) und erneut senden, sobald die richtige genehmigende Person verfügbar ist. Administratoren können auch die Genehmigungsrichtlinie aktualisieren, um weitere genehmigende Personen hinzuzufügen.

+++

+++Kann ich eine Kampagne oder Journey bearbeiten, während die Genehmigung aussteht?

Nein. Nach der Übermittlung zur Validierung befindet sich die Kampagne oder Journey in einem gesperrten Status „In Überprüfung“. Um Änderungen vorzunehmen, muss der Ersteller oder eine genehmigende Person die Anforderung zuerst abbrechen. Das Element kehrt zu „Entwurf“ zurück und kann vor dem erneuten Senden bearbeitet werden.

+++

+++Ich sehe die Berechtigung Genehmigen und Veröffentlichen in der Dropdown-Liste nicht - was soll ich überprüfen?

Stellen Sie sicher, dass Sie zuerst die richtige Ressource hinzufügen. Für die Berechtigung **Kampagnen genehmigen und veröffentlichen** muss die Ressource **Kampagnen** zur Rolle hinzugefügt werden und **Journey genehmigen und veröffentlichen** ist die Ressource **Journey** erforderlich. Beide müssen separat hinzugefügt werden. [Erfahren Sie, wie Sie genehmigungsbezogene Berechtigungen zuweisen](#prerequisites)

+++

+++Wie bestimmt [!DNL Journey Optimizer], welche Genehmigungsrichtlinie gilt, wenn mehr als eine Richtlinie übereinstimmen könnte?

Wenn mehrere aktive Genehmigungsrichtlinien auf dieselbe Journey oder Kampagne angewendet werden können, hat die Richtlinie, **zuletzt aktiviert wurde,**. Die in dieser Richtlinie definierten Benutzergruppen für genehmigende Personen sind diejenigen, die benachrichtigt werden und die Anfrage steuern.

[Weitere Informationen](approval-policies.md#multiple-policies)

+++

+++Wenn ein Antragsteller mehreren Benutzergruppen angehört, kann er dann auswählen, an welche Gruppe die Genehmigungsanfrage gesendet werden soll?

Nein. Anfordernde können nicht manuell auswählen, welche Benutzergruppe die Genehmigungsanfrage erhält oder weiterleitet. Die Benutzergruppen, die in der geltenden Genehmigungsrichtlinie angegeben sind, werden entsprechend [Richtlinienpriorität](approval-policies.md#multiple-policies) automatisch benachrichtigt.

+++

## Weitere Ressourcen

* **[Erstellen von Genehmigungsrichtlinien](approval-policies.md)** – Erfahren Sie, wie Sie Genehmigungsrichtlinien einrichten, um Überprüfungs-Workflows für Kampagnen und Journeys durchzusetzen.
* **[Genehmigung von Anfragen](request-approval.md)** – Verstehen Sie, wie Sie Inhalte zur Genehmigung einreichen und den Genehmigungsstatus verfolgen.
* **[Prüfen und Genehmigen von Anfragen](review-approve-request.md)** – Erfahren Sie, wie Sie als genehmigende Person Anfragen überprüfen, genehmigen oder ablehnen können.
* **[Simulieren mit Beispieleingaben](simulate-sample-input.md)** – Erfahren Sie, wie Sie Inhalte mithilfe von Beispielprofildaten testen und validieren können.
