---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des Twilio-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für den Versand von Nachrichten an Mobilgeräte mit Journey Optimizer mit Twilio konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
TQID: https://experienceleague.adobe.com/EbPWXkbbXG4zazPUQsqaEeXx5wUi6VzFGrEeYmlAASY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 640
ht-degree: 74%

---

# Konfigurieren des Twilio-Anbieters {#sms-configuration-twilio}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie Twilio mit Adobe Journey Optimizer integrieren können, indem Sie API-Anmeldeinformationen für SMS-, MMS- und RCS-Nachrichten erstellen, damit Sie Nachrichten auf Mobilgeräten in Ihren Journey und Kampagnen versenden können.

>[!ENDSHADEBOX]

Durch die Integration von Twilio mit Adobe Journey Optimizer können Sie im Rahmen Ihrer Journey und Kampagnen mobile Nachrichten an Ihre Profile senden.

Gehen Sie wie folgt vor, um Twilio als Ihren SMS-Provider zu konfigurieren:

1. [Erstellen von API-Anmeldedaten](#api-credential)
1. [Erstellen eines Webhook](mobile-webhook.md)
1. [Erstellen einer Kanalkonfiguration](mobile-configuration-surface.md)
1. [Erstellen einer Journey oder Kampagne mit der SMS-Kanalaktion](create-mobile-message.md)

## Konfigurieren der API-Anmeldeinformationen für SMS/RCS/MMS {#api-credential}

Um Twilio mit Journey Optimizer zu konfigurieren, müssen Sie neue API-Anmeldedaten für Twilio erstellen:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** `>` **[!UICONTROL SMS-Einstellungen]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten wie unten beschrieben:

   * **[!UICONTROL SMS-Anbieter]**: Twilio.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL Konto-SID]** und **[!UICONTROL Authentifizierungs-Token]**: Rufen Sie den Bereich mit den **Kontoinformationen** Ihrer Twilio Console-Dashboard-Seite auf. Dort finden Sie Ihre Anmeldedaten.

   * **[!UICONTROL Nachrichten-SID]**: Geben Sie die eindeutige Kennung ein, die jeder von der Twilio-API erstellten Nachricht zugewiesen ist. Weitere Informationen finden Sie in der [Twilio-Dokumentation](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Eingehende Zahl]**: Fügen Sie Ihre eindeutige eingehende Zahl hinzu. Auf diese Weise können Sie dieselben API-Anmeldedaten für verschiedene Sandboxes verwenden, von denen jede über eine eigene eingehende Nummer verfügt.

1. Wählen Sie **[!UICONTROL Benutzerdefinierten Datensatz für eingehende]** verwenden) aus, um die eingehenden SMS dieser Berechtigung an einen vorab erstellten Datensatz weiterzuleiten, den Sie aus der Dropdown-Liste auswählen. [Erfahren Sie mehr über die Verwendung eines benutzerdefinierten Datensatzes für eingehende Keywords](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >Das Datensatzschema muss **[!UICONTROL XDM ExperienceEvent]** sein und mindestens die folgenden Feldergruppen enthalten:
   >* Adobe CJM ExperienceEvent - Details zur Nachrichteninteraktion
   >* Adobe CJM ExperienceEvent - Details zur Nachrichtenausführung
   >* Adobe CJM ExperienceEvent - Details zum Nachrichtenprofil
   >
   >Das Schema und der Datensatz müssen für das Profil aktiviert sein.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldedaten]** auf das Papierkorbsymbol, um Ihre API-Anmeldedaten zu löschen.

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

1. Klicken Sie anhand Ihrer bestehenden API-Anmeldedaten auf **[!UICONTROL SMS-Verbindung überprüfen]**, um Ihre SMS-API-Anmeldedaten zu testen und zu überprüfen, indem Sie eine Beispielnachricht an ein bestimmtes Gerät senden.

1. Füllen Sie die Felder **Anzahl** und **Nachricht** aus und klicken Sie auf **[!UICONTROL Verbindung überprüfen]**.

   >[!IMPORTANT]
   >
   >Die Nachricht muss so strukturiert sein, dass sie mit dem Payload-Format des Anbieters übereinstimmt.

   ![](assets/verify-connection.png)

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie nun eine Kanalkonfiguration für SMS- und MMS-Nachrichten erstellen. [Weitere Informationen](mobile-configuration-surface.md)

## Konfigurieren der API-Anmeldedaten für RCS

RCS-Messaging wird in Adobe Journey Optimizer über Twilio mithilfe der Funktion [Benutzerdefinierter SMS-Anbieter](mobile-configuration-custom.md) unterstützt. Dies ermöglicht den Versand von umfangreichen, interaktiven Nachrichten über verifizierte Geschäftsprofile, die Elemente wie Karussells, Schaltflächen und Multimedia-Inhalte enthalten.

➡️ [Informationen zur Unterstützung von RCS durch Twilio in der Twilio-Dokumentation](https://www.twilio.com/docs/rcs)

Um RCS-Messaging mit Twilio zu aktivieren, müssen neue API-Anmeldedaten über einen benutzerdefinierten SMS-Anbieter konfiguriert werden. Bestehende Twilio-SMS-Anmeldedaten sind nicht kompatibel, da RCS ein eigenes Payload-Format erfordert.

So konfigurieren Sie RCS mit Twilio:

1. **Registrieren für RCS-Messaging in Twilio**

   Schließen Sie zunächst den RCS-Registrierungsprozess auf der Twilio-Plattform ab. Dazu gehört die Einrichtung Ihres Geschäftsprofils und die Aktivierung der RCS-Funktionen für Ihr Konto.

1. **Erstellen eines SMS-Webhooks**

   [Konfigurieren Sie einen SMS-Webhook](mobile-configuration-custom.md#webhook), der eingehende RCS-Nachrichtenantworten oder -Versandaktualisierungen empfangen kann. Dieser Webhook muss zur wechselseitigen Kommunikation ordnungsgemäß mit Ihrem Twilio-Setup verknüpft sein.

1. **Erstellen von API-Anmeldedaten mit einem benutzerdefinierten SMS-Anbieter**

   Definieren Sie in Journey Optimizer [neue API-Anmeldedaten](mobile-configuration-custom.md#api-credential) speziell für RCS. Verwenden Sie dabei „Benutzerdefiniert“ als SMS-Anbieter. Verwenden Sie die entsprechende RCS-Endpunkt-Authentifizierungsmethode, Basis-URL und Header.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für Ihre RCS-Nachrichten erstellen. [Weitere Informationen](mobile-configuration-surface.md)







