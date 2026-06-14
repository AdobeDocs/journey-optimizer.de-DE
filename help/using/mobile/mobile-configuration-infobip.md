---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des Infobip-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für den Versand von Mobile-Nachrichten und MMS mit Journey Optimizer mit Infobip konfigurieren.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
TQID: https://experienceleague.adobe.com/hkloRlDuOO-lNSezWvOcD3dtsHrhDqCJGo3cHq5pWog
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
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 801
ht-degree: 77%

---

# Konfigurieren des Infobip-Anbieters {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Infobip als Provider in Adobe Journey Optimizer konfigurieren, indem Sie SMS-API-Anmeldeinformationen einrichten, und wie Sie RCS-Messaging über eine benutzerdefinierte Provider-Integration aktivieren.

>[!ENDSHADEBOX]

Durch die Integration von Infobip mit Adobe Journey Optimizer können Sie im Rahmen Ihrer Journey- und Kampagnenkampagnen Nachrichten an Ihre Profile senden.

Gehen Sie wie folgt vor, um Infobip als SMS-Provider zu konfigurieren:

1. [Erstellen von API-Anmeldedaten](#api-credential)
1. [Erstellen eines Webhook](mobile-webhook.md)
1. [Erstellen einer Kanalkonfiguration](mobile-configuration-surface.md)
1. [Erstellen einer Journey oder Kampagne mit der SMS-Kanalaktion](create-mobile-message.md)

## Konfigurieren von API-Anmeldedaten für SMS {#api-credential}

Gehen Sie wie folgt vor, um Infobip mit Journey Optimizer zu konfigurieren:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]** aus. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten wie unten beschrieben:

   +++ Liste der SMS-Anmeldedaten für die Konfiguration

   | Konfigurationsfelder | Beschreibung |
   |---|---|
   | SMS-Anbieter | Infobip |
   | Name | Wählen Sie einen Namen für Ihre API-Anmeldedaten. |
   | API-Basis-URL und API-Schlüssel | Rufen Sie die Startseite Ihrer Web-Oberfläche oder die Seite zur Verwaltung von API-Schlüsseln auf. Dort finden Sie Ihre Anmeldedaten. Geben Sie für regionale oder alternative Domain-Endpunkte, z. B. `api-ny2.infobip.com`, die vollständige Basis-URL an und überprüfen Sie Ihr Autorisierungs-Token mit Infobip-Unterstützung. </br>Weitere Informationen finden Sie in der [Infobip-Dokumentation](https://www.infobip.com/docs/api){target="_blank"}. |
   | Prinzipalentitäts-ID | Geben Sie die Ihnen zugewiesene DLT-Prinzipalentitäts-ID ein. |
   | Inhaltsvorlagen-ID | Geben Sie Ihre registrierte DLT-Inhaltsvorlagen-ID ein. |
   | Gültigkeitszeitraum | Geben Sie den Gültigkeitszeitraum der Nachricht in Stunden ein. Wenn Nachrichten nicht innerhalb dieses Zeitrahmens zugestellt werden können, unternimmt das System zusätzliche Versuche, sie erneut zu senden. Der standardmäßige Gültigkeitszeitraum beträgt 48 Stunden. |
   | Callback-Daten | Geben Sie die zusätzlichen Client-Daten ein, die an die Benachrichtigungs-URL gesendet werden. |
   | Eingehende Nummer | Fügen Sie Ihre eindeutige eingehende Nummer hinzu. Auf diese Weise können Sie dieselben API-Anmeldedaten für verschiedene Sandboxes verwenden, von denen jede über eine eigene eingehende Nummer verfügt. |

   +++

1. Aktivieren Sie die Option **[!UICONTROL Unpräzises Opt-out]**, um Nachrichten zu erkennen, die Opt-out-Schlüsselwörtern ähneln (z. B. „ABNELDEN“), und passen Sie die Bestätigungsantwort im Feld **[!UICONTROL Unpräzise automatische Antwort]** an.

   **[!UICONTROL Unpräzises Opt-out]** kennzeichnet SMS-Nachrichten, die darauf hinweisen, dass jemand das Abonnement kündigen möchte, auch wenn die Nachricht nicht genau mit einem definierten Keyword zum Abmelden übereinstimmt. Es kann häufig verwendete Opt-out-Phrasen und bestimmte anstößige Begriffe erkennen und sicherstellen, dass Ihre Kampagnen die Benutzerpräferenzen respektieren und die Regeln einhalten.

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

RCS-Messaging wird in Adobe Journey Optimizer über Infobip mit der Funktion [Benutzerdefinierter SMS-Anbieter](mobile-configuration-custom.md) unterstützt. Dies ermöglicht den Versand von umfangreichen, interaktiven Nachrichten über verifizierte Geschäftsprofile, die Elemente wie Karussells, Schaltflächen und Multimedia-Inhalte enthalten.

➡️ [Erfahren Sie in der Infobip-Dokumentation, wie RCS von Infobip unterstützt wird](https://www.infobip.com/docs/api/channels/rcs)

Um RCS-Messaging mit Infobip zu aktivieren, müssen neue API-Anmeldedaten über einen benutzerdefinierten SMS-Anbieter konfiguriert werden. Bestehende Infobip-SMS-Anmeldedaten sind nicht kompatibel, da RCS ein eigenes Payload-Format erfordert.

So konfigurieren Sie RCS mit Infobip:

1. **Registrieren Ihres Unternehmens für RCS über Infobip**

   Schließen Sie zunächst das RCS-Onboarding und den RCS-Registrierungsprozess auf der Infobip-Plattform ab. Dazu müssen Sie Ihr RCS-Absendeprofil einrichten und sicherstellen, dass Ihr Konto RCS-fähig ist. Weitere Informationen finden Sie in der [Infobip-Dokumentation](https://www.infobip.com/docs/rcs/get-started).

1. **Erstellen eines SMS-Webhooks**

   [Konfigurieren Sie einen benutzerdefinierten SMS-Webhook](mobile-configuration-custom.md#webhook) in Journey Optimizer. Dieser Webhook ist für die Verarbeitung von Versandbestätigungen, eingehenden RCS-Nachrichten und Statusaktualisierungen von der Infobip-Plattform verantwortlich.

1. **Erstellen von API-Anmeldedaten mit einem benutzerdefinierten SMS-Anbieter**

   [Erstellen Sie neue API-Anmeldedaten](mobile-configuration-custom.md#api-credential) in Journey Optimizer. Wählen Sie dabei „Benutzerdefiniert“ als SMS-Anbieter aus. Verwenden Sie die entsprechende RCS-Endpunkt-Authentifizierungsmethode, Basis-URL und Header.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt [Ihren Webhook](mobile-webhook.md) und eine Kanalkonfiguration für Ihre RCS-Nachrichten erstellen. [Weitere Informationen](mobile-configuration-surface.md)
