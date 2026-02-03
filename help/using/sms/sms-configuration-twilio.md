---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des Twilio-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten mit Journey Optimizer mit Twilio konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 93%

---

# Konfigurieren des Twilio-Anbieters {#sms-configuration-twilio}

Durch die Integration von Twilio mit Adobe Journey Optimizer können Sie im Rahmen Ihrer Journey und Kampagnen Textnachrichten an Ihre Profile senden.

Gehen Sie wie folgt vor, um Twilio als Ihren SMS-Provider zu konfigurieren:

1. [Erstellen von API-Anmeldedaten](#api-credential)
1. [Erstellen eines Webhook](sms-webhook.md)
1. [Erstellen einer Kanalkonfiguration](sms-configuration-surface.md)
1. [Erstellen einer Journey oder Kampagne mit der SMS-Kanalaktion](create-sms.md)

## Konfigurieren von API-Anmeldedaten für SMS/MMS {#api-credential}

Um Twilio mit Journey Optimizer zu konfigurieren, müssen Sie neue API-Anmeldedaten für Twilio erstellen:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** `>` **[!UICONTROL SMS-Einstellungen]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten wie unten beschrieben:

   * **[!UICONTROL SMS-Anbieter]**: Twilio.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL Konto-SID]** und **[!UICONTROL Authentifizierungs-Token]**: Rufen Sie den Bereich mit den **Kontoinformationen** Ihrer Twilio Console-Dashboard-Seite auf. Dort finden Sie Ihre Anmeldedaten.

   * **[!UICONTROL Nachrichten-SID]**: Geben Sie die eindeutige Kennung ein, die jeder von der Twilio-API erstellten Nachricht zugewiesen ist. Weitere Informationen finden Sie in der [Twilio-Dokumentation](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Eingehende Zahl]**: Fügen Sie Ihre eindeutige eingehende Zahl hinzu. Auf diese Weise können Sie dieselben API-Anmeldedaten für verschiedene Sandboxes verwenden, von denen jede über eine eigene eingehende Nummer verfügt.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldedaten]** auf das Papierkorbsymbol, um Ihre API-Anmeldedaten zu löschen.

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

1. Klicken Sie anhand Ihrer bestehenden API-Anmeldedaten auf **[!UICONTROL SMS-Verbindung überprüfen]**, um Ihre SMS-API-Anmeldedaten zu testen und zu überprüfen, indem Sie eine Beispielnachricht an ein bestimmtes Gerät senden.

1. Füllen Sie die Felder **Anzahl** und **Nachricht** aus und klicken Sie auf **[!UICONTROL Verbindung überprüfen]**.

   >[!IMPORTANT]
   >
   >Die Nachricht muss so strukturiert sein, dass sie mit dem Payload-Format des Anbieters übereinstimmt.

   ![](assets/verify-connection.png)

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie nun eine Kanalkonfiguration für SMS- und MMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

## Konfigurieren der API-Anmeldedaten für RCS

RCS-Messaging wird in Adobe Journey Optimizer über Twilio mithilfe der Funktion [Benutzerdefinierter SMS-Anbieter](sms-configuration-custom.md) unterstützt. Dies ermöglicht den Versand von umfangreichen, interaktiven Nachrichten über verifizierte Geschäftsprofile, die Elemente wie Karussells, Schaltflächen und Multimedia-Inhalte enthalten.

➡️ [Informationen zur Unterstützung von RCS durch Twilio in der Twilio-Dokumentation](https://www.twilio.com/docs/rcs)

Um RCS-Messaging mit Twilio zu aktivieren, müssen neue API-Anmeldedaten über einen benutzerdefinierten SMS-Anbieter konfiguriert werden. Bestehende Twilio-SMS-Anmeldedaten sind nicht kompatibel, da RCS ein eigenes Payload-Format erfordert.

So konfigurieren Sie RCS mit Twilio:

1. **Registrieren für RCS-Messaging in Twilio**

   Schließen Sie zunächst den RCS-Registrierungsprozess auf der Twilio-Plattform ab. Dazu gehört die Einrichtung Ihres Geschäftsprofils und die Aktivierung der RCS-Funktionen für Ihr Konto.

1. **Erstellen eines SMS-Webhooks**

   [Konfigurieren Sie einen SMS-Webhook](sms-configuration-custom.md#webhook), der eingehende RCS-Nachrichtenantworten oder -Versandaktualisierungen empfangen kann. Dieser Webhook muss zur wechselseitigen Kommunikation ordnungsgemäß mit Ihrem Twilio-Setup verknüpft sein.

1. **Erstellen von API-Anmeldedaten mit einem benutzerdefinierten SMS-Anbieter**

   Definieren Sie in Journey Optimizer [neue API-Anmeldedaten](sms-configuration-custom.md#api-credential) speziell für RCS. Verwenden Sie dabei „Benutzerdefiniert“ als SMS-Anbieter. Verwenden Sie die entsprechende RCS-Endpunkt-Authentifizierungsmethode, Basis-URL und Header.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für Ihre RCS-Nachrichten erstellen. [Weitere Informationen](sms-configuration-surface.md)







