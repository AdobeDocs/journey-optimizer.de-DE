---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines Infobip-Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten und MMS mit Journey Optimizer mit Infobip konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 63%

---

# Konfigurieren eines Infobip-Anbieters {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

Wenn keine Opt-in- oder Opt-out-Keywords angegeben werden, werden standardmäßige Einverständnisnachrichten verwendet, um den Datenschutz der Benutzenden zu berücksichtigen. Durch das Hinzufügen benutzerdefinierter Keywords werden die Standardwerte automatisch überschrieben.

**Standard-Keywords:**

* **Opt-in**: SUBSCRIBE, YES, UNSTOP, START, CONTINUE, RESUME, BEGIN
* **Opt-out**: STOP, QUIT, CANCEL, END, UNSUBSCRIBE, NO
* **Hilfe**: HELP.

>[!ENDSHADEBOX]

## Konfigurieren von API-Anmeldeinformationen für SMS

Gehen Sie wie folgt vor, um Infobip mit Journey Optimizer zu konfigurieren:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]** aus. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten wie unten beschrieben:

+++ Liste der SMS-Anmeldedaten für die Konfiguration

   | Konfigurationsfelder | Beschreibung |
   |---|---|    
   | SMS-Anbieter | Infobip |
   | Name | Wählen Sie einen Namen für Ihre API-Anmeldedaten. |
   | API-Basis-URL und API-Schlüssel | Rufen Sie die Startseite Ihrer Web-Oberfläche oder die Seite zur Verwaltung von API-Schlüsseln auf. Dort finden Sie Ihre Anmeldedaten. Weitere Informationen finden Sie in [InfoIP-Dokumentation](https://www.infobip.com/docs/api){target="_blank"} |
   | Opt-in-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Opt-in-Nachricht automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Opt-in-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Opt-in-Nachricht gesendet wird. |
   | Opt-out-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Opt-out-Nachricht automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Opt-out-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Opt-out-Nachricht gesendet wird. |
   | Hilfe-Keywords | Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre **Hilfenachricht** automatisch ausgelöst wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte. |
   | Hilfenachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch als **Hilfenachricht** gesendet wird. |
   | Double-Opt-in-Keywords | Geben Sie die Keywords ein, die den Double-Opt-in-Prozess auslösen. Wenn kein Benutzerprofil vorhanden ist, wird es nach erfolgreicher Bestätigung erstellt. Verwenden Sie für mehrere Keywords kommagetrennte Werte. [Erfahren Sie mehr über das SMS-Double-Opt-in](https://video.tv.adobe.com/v/3427129/?learn=on). |
   | Double-Opt-in-Nachricht | Geben Sie die benutzerdefinierte Antwort ein, die automatisch nach der Double-Opt-in-Bestätigung gesendet wird. |
   | ID der Prinzipalentität | Geben Sie die zugewiesene DLT-Prinzipalentitäts-ID ein. |
   | Inhaltsvorlagen-ID | Geben Sie Ihre registrierte DLT-Inhaltsvorlagen-ID ein. |
   | Gültigkeitszeitraum | Geben Sie den Gültigkeitszeitraum der Nachricht in Stunden ein. Wenn Nachrichten nicht innerhalb dieses Zeitrahmens zugestellt werden können, unternimmt das System zusätzliche Versuche, sie erneut zu senden. Der standardmäßige Gültigkeitszeitraum beträgt 48 Stunden. |
   | Callback-Daten | Geben Sie die zusätzlichen Client-Daten ein, die über die Benachrichtigungs-URL gesendet werden. |
   | Eingehende Nummer | Eindeutige eingehende Nummer hinzufügen. Auf diese Weise können Sie dieselben API-Anmeldeinformationen für verschiedene Sandboxes verwenden, von denen jede über eine eigene eingehende Zahl verfügt. |
   | Benutzerdefinierte eingehende Keywords | Definieren Sie eindeutige Keywords für bestimmte Aktionen, z. B. RABATT, ANGEBOTE, REGISTRIEREN. Diese Keywords werden als Attribute im Profil erfasst und gespeichert, sodass Sie eine Streaming-Segmentqualifikation innerhalb der Journey auslösen und eine benutzerdefinierte Antwort oder Aktion bereitstellen können. |
   | Eingehende Standard-Antwortnachricht | Geben Sie die Standardantwort ein, die gesendet wird, wenn eine Endanwenderin oder ein Endanwender eine eingehende SMS sendet, die keinem der definierten Keywords entspricht. |

+++

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldedaten]** auf das Papierkorbsymbol, um Ihre API-Anmeldedaten zu löschen.

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie nun eine Kanalkonfiguration für SMS- und MMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

## Konfigurieren der API-Anmeldedaten für RCS

RCS-Messaging wird in Adobe Journey Optimizer über Infobip mit der Funktion [Benutzerdefinierter SMS-Provider](sms-configuration-custom.md) unterstützt. Dies ermöglicht den Versand von umfangreichen, interaktiven Nachrichten über verifizierte Geschäftsprofile, die Elemente wie Karussells, Schaltflächen und Multimedia-Inhalte enthalten.

Um RCS-Messaging mit Infobip zu aktivieren, müssen neue API-Anmeldedaten über einen benutzerdefinierten SMS-Provider konfiguriert werden. Bestehende Infobip SMS-Anmeldedaten sind nicht kompatibel, da RCS ein eigenes Payload-Format erfordert.

1. **Registrieren Sie Ihr Unternehmen für RCS über Infobip**

   Beginnen Sie mit dem Abschluss des RCS Onboarding- und Registrierungsprozesses innerhalb der Infobip-Plattform. Dazu müssen Sie Ihr RCS Absenderprofil einrichten und sicherstellen, dass Ihr Konto RCS-fähig ist. Weitere Informationen finden Sie in [Infobip-Dokumentation](https://www.infobip.com/docs/rcs/get-started)

1. **Erstellen eines SMS-Webhooks**

   [Konfigurieren eines benutzerdefinierten SMS-Webhooks](sms-configuration-custom.md#webhook) in Journey Optimizer. Dieser Webhook ist für die Verarbeitung von Empfangsbestätigungen, eingehenden RCS-Nachrichten und Statusaktualisierungen von der Plattform von Infobip verantwortlich.

1. **Erstellen von API-Anmeldeinformationen mit „Benutzerdefiniert“ als SMS-Anbieter**

   [Neue API-Anmeldedaten erstellen](sms-configuration-custom.md#api-credential) Wählen Sie in Journey Optimizer „Benutzerdefiniert“ als SMS-Anbieter aus. Verwenden Sie die entsprechende RCS-Endpunktauthentifizierungsmethode, Basis-URL und Header.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanalkonfiguration für Ihre RCS-Nachrichten erstellen. [Weitere Informationen](sms-configuration-surface.md)
