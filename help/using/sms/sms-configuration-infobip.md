---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines Infobip-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten und MMS mit Journey Optimizer mit Infobip konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: bd925e1fd053a19e2102536049278e48b0784960
workflow-type: ht
source-wordcount: '902'
ht-degree: 100%

---

# Konfigurieren eines Infobip-Anbieters {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

Wenn keine Opt-in- oder Opt-out-Keywords angegeben werden, werden standardmäßige Einverständnisnachrichten verwendet, um den Datenschutz der Benutzenden zu berücksichtigen. Durch das Hinzufügen benutzerdefinierter Keywords werden die Standardwerte automatisch überschrieben.

**Standard-Keywords:**

* **Opt-in**: SUBSCRIBE, YES, UNSTOP, START, CONTINUE, RESUME, BEGIN
* **Opt-out**: STOP, QUIT, CANCEL, END, UNSUBSCRIBE, NO
* **Hilfe**: HELP.

>[!ENDSHADEBOX]

## Konfigurieren von API-Anmeldedaten für SMS

Gehen Sie wie folgt vor, um Infobip mit Journey Optimizer zu konfigurieren:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]** aus. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten wie unten beschrieben:

   +++ Liste der SMS-Anmeldedaten für die Konfiguration

   | Konfigurationsfelder | Beschreibung |
   |---|---|    
   | SMS-Anbieter | Infobip |
   | Name | Wählen Sie einen Namen für Ihre API-Anmeldedaten. |
   | API-Basis-URL und API-Schlüssel | Rufen Sie die Startseite Ihrer Web-Oberfläche oder die Seite zur Verwaltung von API-Schlüsseln auf. Dort finden Sie Ihre Anmeldedaten. Geben Sie für regionale oder alternative Domain-Endpunkte, z. B. `api-ny2.infobip.com`, die vollständige Basis-URL an und überprüfen Sie Ihr Autorisierungs-Token mit Infobip-Unterstützung. </br>Weitere Informationen finden Sie in der [Infobip-Dokumentation](https://www.infobip.com/docs/api){target="_blank"}. |
   | Opt-in-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Opt-in-Nachricht automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Opt-in-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Opt-in-Nachricht gesendet wird. |
   | Opt-out-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Opt-out-Nachricht automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Opt-out-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Opt-out-Nachricht gesendet wird. |
   | Hilfe-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **Hilfenachricht** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Hilfenachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als **Hilfenachricht** gesendet wird. |
   | Double-Opt-in-Keywords | Geben Sie die Keywords ein, die den Double-Opt-in-Prozess auslösen. Wenn kein Benutzerprofil vorhanden ist, wird es nach erfolgreicher Bestätigung erstellt. Verwenden Sie für mehrere Keywords kommagetrennte Werte. [Erfahren Sie mehr über das SMS-Double-Opt-in](https://video.tv.adobe.com/v/3427129/?learn=on). |
   | Double-Opt-in-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch nach der Double-Opt-in-Bestätigung gesendet wird. |
   | Prinzipalentitäts-ID | Geben Sie die Ihnen zugewiesene DLT-Prinzipalentitäts-ID ein. |
   | Inhaltsvorlagen-ID | Geben Sie Ihre registrierte DLT-Inhaltsvorlagen-ID ein. |
   | Gültigkeitszeitraum | Geben Sie den Gültigkeitszeitraum der Nachricht in Stunden ein. Wenn Nachrichten nicht innerhalb dieses Zeitrahmens zugestellt werden können, unternimmt das System zusätzliche Versuche, sie erneut zu senden. Der standardmäßige Gültigkeitszeitraum beträgt 48 Stunden. |
   | Callback-Daten | Geben Sie die zusätzlichen Client-Daten ein, die an die Benachrichtigungs-URL gesendet werden. |
   | Eingehende Nummer | Fügen Sie Ihre eindeutige eingehende Nummer hinzu. Auf diese Weise können Sie dieselben API-Anmeldedaten für verschiedene Sandboxes verwenden, von denen jede über eine eigene eingehende Nummer verfügt. |
   | Benutzerdefinierte eingehende Keywords | Definieren Sie eindeutige, nicht auf Einverständnis bezogene Keywords für Batch-basierte Aktionen, z. B. RABATT, ANGEBOTE, REGISTRIEREN. Diese Keywords werden als Attribute im Profil erfasst und gespeichert, sodass Sie eine Batch-Segmentqualifikation innerhalb der Journey auslösen und eine benutzerdefinierte Antwort oder Aktion bereitstellen können. |
   | Eingehende Standard-Antwortnachricht | Geben Sie die Standardantwort ein, die gesendet wird, wenn eine Endanwenderin oder ein Endanwender eine eingehende SMS sendet, die keinem der definierten Keywords entspricht. |

   +++

1. Aktivieren Sie die Option **[!UICONTROL Unpräzises Opt-out]**, um Nachrichten zu erkennen, die Opt-out-Schlüsselwörtern ähneln (z. B. „ABNELDEN“), und passen Sie die Bestätigungsantwort im Feld **[!UICONTROL Unpräzise automatische Antwort]** an.

   **[!UICONTROL Unpräzises Opt-out]** kennzeichnet SMS-Nachrichten, die darauf hinweisen, dass jemand das Abonnement kündigen möchte, auch wenn die Nachricht nicht genau mit einem definierten Keyword zum Abmelden übereinstimmt. Es kann häufig verwendete Opt-out-Phrasen und bestimmte anstößige Begriffe erkennen und sicherstellen, dass Ihre Kampagnen die Benutzerpräferenzen respektieren und die Regeln einhalten.

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

RCS-Messaging wird in Adobe Journey Optimizer über Infobip mit der Funktion [Benutzerdefinierter SMS-Anbieter](sms-configuration-custom.md) unterstützt. Dies ermöglicht den Versand von umfangreichen, interaktiven Nachrichten über verifizierte Geschäftsprofile, die Elemente wie Karussells, Schaltflächen und Multimedia-Inhalte enthalten.

➡️ [Erfahren Sie in der Infobip-Dokumentation, wie RCS von Infobip unterstützt wird](https://www.infobip.com/docs/api/channels/rcs)

Um RCS-Messaging mit Infobip zu aktivieren, müssen neue API-Anmeldedaten über einen benutzerdefinierten SMS-Anbieter konfiguriert werden. Bestehende Infobip-SMS-Anmeldedaten sind nicht kompatibel, da RCS ein eigenes Payload-Format erfordert.

So konfigurieren Sie RCS mit Infobip:

1. **Registrieren Ihres Unternehmens für RCS über Infobip**

   Schließen Sie zunächst das RCS-Onboarding und den RCS-Registrierungsprozess auf der Infobip-Plattform ab. Dazu müssen Sie Ihr RCS-Absendeprofil einrichten und sicherstellen, dass Ihr Konto RCS-fähig ist. Weitere Informationen finden Sie in der [Infobip-Dokumentation](https://www.infobip.com/docs/rcs/get-started).

1. **Erstellen eines SMS-Webhooks**

   [Konfigurieren Sie einen benutzerdefinierten SMS-Webhook](sms-configuration-custom.md#webhook) in Journey Optimizer. Dieser Webhook ist für die Verarbeitung von Versandbestätigungen, eingehenden RCS-Nachrichten und Statusaktualisierungen von der Infobip-Plattform verantwortlich.

1. **Erstellen von API-Anmeldedaten mit einem benutzerdefinierten SMS-Anbieter**

   [Erstellen Sie neue API-Anmeldedaten](sms-configuration-custom.md#api-credential) in Journey Optimizer. Wählen Sie dabei „Benutzerdefiniert“ als SMS-Anbieter aus. Verwenden Sie die entsprechende RCS-Endpunkt-Authentifizierungsmethode, Basis-URL und Header.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für Ihre RCS-Nachrichten erstellen. [Weitere Informationen](sms-configuration-surface.md)
