---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines Twilio-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten mit Journey Optimizer mit Twilio konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 604af3a0ac9febb62f2e2b1705e2751b2c476e04
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 49%

---

# Konfigurieren eines Twilio-Anbieters {#sms-configuration-twilio}

## Konfigurieren der API-Anmeldeinformationen für SMS/MMS

Um Twilio mit Journey Optimizer zu konfigurieren, müssen Sie neue API-Anmeldedaten für Twilio erstellen:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** `>` **[!UICONTROL SMS-Einstellungen]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten wie unten beschrieben:

   * **[!UICONTROL SMS-Anbieter]**: Twilio.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL Konto-SID]** und **[!UICONTROL Authentifizierungs-Token]**: Rufen Sie den Bereich mit den **Kontoinformationen** Ihrer Twilio Console-Dashboard-Seite auf. Dort finden Sie Ihre Anmeldedaten.

   * **[!UICONTROL Nachrichten-SID]**: Geben Sie die eindeutige Kennung ein, die jeder von der Twilio-API erstellten Nachricht zugewiesen ist. Weitere Informationen finden Sie in [Twilio-Dokumentation](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Eingehende Zahl]**: Fügen Sie Ihre eindeutige eingehende Zahl hinzu. Auf diese Weise können Sie dieselben API-Anmeldeinformationen für verschiedene Sandboxes verwenden, von denen jede über eine eigene eingehende Zahl verfügt.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldedaten]** auf das Papierkorbsymbol, um Ihre API-Anmeldedaten zu löschen.

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie nun eine Kanalkonfiguration für SMS- und MMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

## Konfigurieren der API-Anmeldedaten für RCS

RCS-Messaging wird in Adobe Journey Optimizer über Twilio mithilfe der Funktion [Benutzerdefinierter SMS-Provider](sms-configuration-custom.md) unterstützt. Dies ermöglicht den Versand von umfangreichen, interaktiven Nachrichten über verifizierte Geschäftsprofile, die Elemente wie Karussells, Schaltflächen und Multimedia-Inhalte enthalten.

➡️ [Wie Twilio RCS unterstützt, erfahren Sie in der Twilio-Dokumentation](https://www.twilio.com/docs/rcs)

Um RCS-Messaging mit Twilio zu aktivieren, müssen neue API-Anmeldedaten über einen benutzerdefinierten SMS-Provider konfiguriert werden. Vorhandene Twilio SMS-Anmeldedaten sind nicht kompatibel, da RCS ein eigenes Payload-Format erfordert.

RCS mit Twilio konfigurieren:

1. **Registrieren Sie sich für RCS Messaging in Twilio**

   Beginnen Sie mit dem Abschluss des RCS-Registrierungsprozesses in der Twilio-Plattform. Dazu gehört die Einrichtung Ihres Geschäftsprofils und die Aktivierung der RCS-Funktionen für Ihr Konto.

1. **Erstellen eines SMS-Webhooks**

   [Konfigurieren eines SMS-Webhooks](sms-configuration-custom.md#webhook) der eingehende RCS-Nachrichtenantworten oder Versandaktualisierungen empfangen kann. Dieser Webhook muss ordnungsgemäß mit Ihrem Twilio-Setup für bidirektionale Kommunikation verknüpft sein.

1. **Erstellen von API-Anmeldeinformationen mit „Benutzerdefiniert“ als SMS-Anbieter**

   Journey Optimizer Definieren Sie in [neue API-Anmeldeinformationen](sms-configuration-custom.md#api-credential) speziell für RCS mit „Benutzerdefiniert“ als SMS-Anbieter. Verwenden Sie die entsprechende RCS-Endpunktauthentifizierungsmethode, Basis-URL und Header.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für Ihre RCS-Nachrichten erstellen. [Weitere Informationen](sms-configuration-surface.md)







