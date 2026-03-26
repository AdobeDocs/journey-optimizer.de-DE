---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Landingpages
description: Informationen zu Landingpages in Journey Optimizer
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: Landing, Landingpage, Starten, erste Schritte
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 14%

---

# Erste Schritte mit Landingpages {#get-started-lp}

Eine Landingpage ist eine eigenständige Web-Seite, auf die ein Benutzer geleitet wird, nachdem er auf eine E-Mail, eine Website, eine Anzeige oder einen anderen digitalen Ort geklickt hat.

[!DNL Journey Optimizer] können Sie Landingpages erstellen und gestalten, um Ihre Benutzer zu Online-Formularen zu leiten, über die sie sich für den Erhalt Ihrer Nachrichten oder eines bestimmten Services wie eines Newsletters anmelden oder abmelden können.

➡️ [Informationen zur Konfiguration von Abonnements und zur Erstellung von Landingpages finden Sie in diesem Video](#video)

## Verwendung von Landingpages {#when-to-use}

Verwenden Sie Landingpages, wenn Sie Folgendes tun möchten:

* Ermöglicht Kunden **Opt-in oder Opt-out** von Marketing-Nachrichten oder einem bestimmten Service oder Newsletter von einem Link in einer E-Mail oder Kampagne, einschließlich Abonnement-Listen für zielgerichtete Services. [Weitere Informationen](lp-use-cases.md#subscription-to-a-service)
* **Einverständnis einholen** bevor Nachrichten gesendet werden, und eine **Bestätigungs-E-Mail** beim Opt-in oder Opt-out senden. [Weitere Informationen](lp-use-cases.md#send-confirmation-email)
* **Erfassen oder Aktualisieren von Profildaten** mithilfe von Formularen auf **[!UICONTROL Datenerfassung]** Landingpages - für die progressive Profilerstellung, Voreinstellungen, Registrierungen und ähnliche Szenarien. [Weitere Informationen](#data-capture-lp)
* Benutzer zu einem **Web-Formular umleiten** ohne eine externe Seite außerhalb von [!DNL Journey Optimizer] zu erstellen
* Erstellen **responsiven Landingpages** mithilfe der Funktionen zur Inhaltserstellung von [!DNL Journey Optimizer]

### Datenerfassung mit Landingpages {#data-capture-lp}

**[!UICONTROL Datenerfassung]** Mit Landingpages können Sie veröffentlichte Formulare einbetten, damit Besucher Attribute senden können, die über die in Ihrer Formularvorgabe konfigurierte Streaming-Verbindung in Ihren [!DNL Adobe Experience Platform] Datensatz geschrieben werden. [Erfahren Sie, wie Sie Formulare in eine Landingpage erstellen und einbetten](lp-forms.md)

>[!NOTE]
>
>Die Datenerfassung über Landingpage-Formulare wird für **bekannte Profile“ unterstützt** vorhandene Profile, die in [!DNL Adobe Experience Platform] identifiziert wurden). Die Landingpage sollte über einen **personalisierten Link** (z. B. über eine E-Mail-Kampagne) geöffnet werden, damit die Profilidentität beim Laden der Seite aufgelöst werden kann.

Im Folgenden finden Sie Beispiele für Anwendungsfälle:

1. **Progressive Profilanreicherung** - Erfassen Sie zusätzliche Attribute bekannter Kundinnen und Kunden - wie Telefonnummer, Geburtsdatum oder Standort - über eine personalisierte Landingpage, um ihr vorhandenes [!DNL Experience Platform] zur Segmentierung und Personalisierung anzureichern.

2. **Aktualisierung des Präferenzzentrums** - Ermöglicht bekannten Abonnentinnen und Abonnenten, ihre Kommunikationsvoreinstellungen (Kanal, Themeninteressen) über eine Landingpage zu verwalten, wobei Änderungen in der Regel innerhalb von etwa 15 Minuten in ihrem [!DNL Experience Platform] Profil widergespiegelt werden.

3. **Ereignis- oder Webinar-Registrierung** - Erfassen Sie ereignisspezifische Daten bekannter Profile auf einer Registrierungsseite, aktualisieren Sie das Profil mit Registrierungsattributen und erstellen Sie einen Trigger auf einer Bestätigungs-Journey.

4. **Treue- oder Programmregistrierung** - Lassen Sie bestehende Kundinnen und Kunden sich für Treueprogramme oder Mitgliedschaftsstufen registrieren, indem sie zusätzliche Details über eine Landingpage übermitteln, wodurch das Profil für das nachgelagerte Targeting angereichert wird.

5. **Teilnahme an Wettbewerben oder Wettbewerben** - Kunden über ein Landingpage-Formular an Wettbewerben oder Gewinnspielen teilnehmen lassen; erfassen eintragsspezifische Details (Antworten, Voreinstellungen oder Erklärungen) und schreiben sie in das Profil, um die Eignung, die Gewinnerauswahl und Folgeprofile zu unterstützen.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="Lead" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>Landingpages erstellen</strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="Gelegentlich" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>Abonnement-Listen erstellen</strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Forms-Liste für Landingpages in Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Verwenden von Formularen auf Ihren Landingpages</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="Validierung" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>Reporting</strong></a>
</div>
<p>
</td>
</tr></table>

## Bevor Sie beginnen {#prerequisites}

Führen Sie vor dem Erstellen einer Landingpage die folgenden Schritte aus:

1. **Subdomain konfigurieren** - Richten Sie eine Subdomain ein, die dem Hosten Ihrer Landingpages dient. [Weitere Informationen](lp-subdomains.md)
1. **Landingpage-Voreinstellung erstellen** - Eine Voreinstellung definiert die Subdomain und andere Einstellungen, die auf Ihre Landingpages angewendet werden. [Weitere Informationen](lp-presets.md#lp-create-preset)
1. **Abonnement-Liste erstellen** (für Abonnement-Anwendungsfälle) - Erforderlich, wenn Kundinnen und Kunden einen bestimmten Dienst abonnieren oder abmelden sollen. [Weitere Informationen](subscription-list.md)
1. **Formular erstellen** (für Anwendungsfälle zur Datenerfassung) - Erforderlich, wenn Sie ein Formular in eine Landingpage zur **[!UICONTROL Datenerfassung]** einbetten und Übermittlungen an [!DNL Experience Platform] senden möchten. [Weitere Informationen](lp-forms.md)

## Funktionsweise {#how-it-works}

Das Erstellen und Bereitstellen einer Landingpage folgt dieser Reihenfolge:

1. **Landingpage erstellen und konfigurieren** - Wählen Sie eine Voreinstellung aus, richten Sie die Primärseite ein und fügen Sie alle erforderlichen Unterseiten hinzu. [Weitere Informationen](create-lp.md#create-landing-page)
1. **Seite gestalten** - Seiteninhalt und Formular mit dem Drag-and-Drop-Editor von [!DNL Journey Optimizer] erstellen. [Weitere Informationen](design-lp.md)
1. **Landingpage testen und veröffentlichen** - Vorschau der Seite, Testen des Formularverhaltens und anschließendes Veröffentlichen, um sie live zu schalten. [Weitere Informationen](create-lp.md#test-landing-page)
1. **Link in einer Nachricht oder einer Journey** - Fügen Sie die Landingpage-URL zu einer E-Mail-, Kampagnen- oder Journey-Aktion hinzu, damit Kunden sie erreichen können. [Weitere Informationen](../email/message-tracking.md#insert-links)

## Anleitungsvideo{#video}

Das folgende Video zeigt, wie Sie eine Abonnement-Liste erstellen, Landingpages zum Opt-in oder Opt-out für einen Service einrichten, die Opt-in-/Opt-out-Option in eine Nachricht integrieren und entsprechende Journey konfigurieren.

>[!VIDEO](https://video.tv.adobe.com/v/3409511?captions=ger&quality=12&learn=on)
