---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen einer Nachricht zu einer Journey
description: Erfahren Sie, wie Sie ein Nachricht zu einer Journey hinzufügen können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 73%

---

# E-Mail, SMS, Push-Benachrichtigung{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen. Sie können einfach eine Push-, SMS- oder E-Mail-Nachrichtenaktivität zu Ihrer Journey hinzufügen und [Einstellungen und Inhalte definieren](../messages/messages-in-journeys.md). Sie wird dann ausgeführt und innerhalb der Journey gesendet..

Sie können auch bestimmte Aktionen zum Senden von Nachrichten einrichten:

* Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../action/action.md).

* Wenn Sie mit Campaign und Journey Optimizer arbeiten, lesen Sie diese Abschnitte:

   * [[!DNL Journey Optimizer] und Campaign Classic v7 / Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] und Campaign Standard](../action/acs-action.md)

Gehen Sie wie folgt vor, um eine Nachricht zu einer Journey hinzuzufügen:

1. Beginnen Sie Ihre Journey mit einem [Ereignis](general-events.md) oder einer Aktivität vom Typ [Segment lesen](read-segment.md).

1. Ziehen Sie aus dem Abschnitt **Aktionen** der Palette eine **E-Mail**-, **SMS**- oder **Push**-Aktivität auf die Arbeitsfläche und legen Sie sie dort ab.

   ![](../messages/assets/add-a-message.png)


   Alle Schritte zum Konfigurieren der Nachricht und zum Definieren der Inhalte werden in [diesem Abschnitt](../messages/get-started-content.md) beschrieben.

## Live-Inhalt aktualisieren{#update-live-content}

Sie können den Inhalt einer Nachricht (E-Mail, SMS, Push) in einer Live-Journey aktualisieren.

Öffnen Sie dazu Ihre Live-Journey, wählen Sie die Nachrichtentätigkeit aus und klicken Sie auf **Inhalt bearbeiten**.

![](assets/add-a-message2.png)

Sie können jedoch die in der Personalisierung verwendeten Attribute nicht ändern, unabhängig davon, ob es sich um Profilattribute oder Kontextdaten handelt (aus Ereignis- oder Journey-Eigenschaften).
