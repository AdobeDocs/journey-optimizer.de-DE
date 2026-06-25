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
TQID: https://experienceleague.adobe.com/wr4XGNostKoN8jZ50VRAQPoGg9tsNhMOyJGEt1mASso
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b19d9237-76be-466d-a869-aacf2d72205f
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2956c3df01f4b2e753111ecf54163ec4084fecf2
workflow-type: ht
source-wordcount: 781
ht-degree: 100%

---

# Erste Schritte mit Landingpages {#get-started-lp}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Landingpages wandeln einen Klick aus einer E-Mail, Anzeige oder Kampagne in ein dediziertes Web-Ziel um, bei dem sich Kundinnen und Kunden anmelden oder abmelden können, ihre Voreinstellungen verwalten und Profildaten freigeben können – so können Sie Zielgruppen erweitern, die zugestimmt haben, und die für die Personalisierung erforderlichen First-Party-Daten erfassen.

>[!ENDSHADEBOX]

Eine Landingpage ist eine eigenständige Web-Seite, auf die ein Benutzer geleitet wird, nachdem er auf eine E-Mail, eine Website, eine Anzeige oder einen anderen digitalen Ort geklickt hat.

Mit [!DNL Journey Optimizer] können Sie Landingpages erstellen und gestalten und deren Benutzende zu Online-Formularen weiterleiten, über die sie sich für den Erhalt Ihrer Nachrichten oder einen bestimmten Service wie einen Newsletter an- oder abmelden können.

➡️ [Informationen zur Konfiguration von Abonnements und zur Erstellung von Landingpages finden Sie in diesem Video](#video)

## Verwendung von Landingpages {#when-to-use}

Verwenden Sie Landingpages für Folgendes:

* Ermöglichen Sie Kundinnen und Kunden das **Opt-in oder Opt-out** für Marketing-Nachrichten oder einen bestimmten Service oder Newsletter über einen Link in einer E-Mail oder Kampagne, einschließlich Abonnement-Listen für zielgerichtete Services. [Weitere Informationen](lp-use-cases.md#subscription-to-a-service)
* **Bitten Sie um Einverständnis** vor dem Versand von Nachrichten und senden Sie eine **Bestätigungs-E-Mail** nach dem Opt-in oder Opt-out. [Weitere Informationen](lp-use-cases.md#send-confirmation-email)
* **Erfassen oder aktualisieren Sie Profildaten** mithilfe von Formularen auf Landingpages zur **[!UICONTROL Datenerfassung]**. Dies ist ideal für progressive Profilierung, Voreinstellungen, Registrierungen und ähnliche Szenarien. [Weitere Informationen](#data-capture-lp)
* Leiten Sie Benutzende zu einem **bestimmten Web-Formular** um, ohne eine externe Seite außerhalb von [!DNL Journey Optimizer] erstellen zu müssen.
* Erstellen Sie **responsive Landingpages** mithilfe der Möglichkeiten zur Inhaltsgestaltung von [!DNL Journey Optimizer].

### Datenerfassung mit Landingpages {#data-capture-lp}

Mit Landingpages zur **[!UICONTROL Datenerfassung]** können Sie veröffentlichte Formulare einbetten, sodass Besuchende Attribute übermitteln können, die über die in Ihrer Formularvoreinstellung konfigurierte Streaming-Verbindung in Ihren [!DNL Adobe Experience Platform]-Datensatz geschrieben werden. [Weitere Informationen zum Erstellen und Einbetten von Formularen in einer Landingpage](lp-forms.md)

>[!NOTE]
>
>Die Datenerfassung über Landingpage-Formulare wird für **bekannte Profile** unterstützt (vorhandene, in [!DNL Adobe Experience Platform] identifizierte Profile). Die Landingpage sollte über einen **personalisierten Link** (z. B. über eine E-Mail-Kampagne) geöffnet werden, damit die Profilidentität beim Laden der Seite aufgelöst werden kann.

Im Folgenden finden Sie Beispiele für Anwendungsfälle:

1. **Progressive Profilanreicherung**: Erfassen Sie zusätzliche Attribute bekannter Kundinnen und Kunden – wie Telefonnummer, Geburtsdatum oder Standort – über eine personalisierte Landingpage, um ihr vorhandenes [!DNL Experience Platform]-Profil zur Segmentierung und Personalisierung anzureichern.

2. **Zentrale Aktualisierung von Voreinstellungen**: Ermöglichen Sie es bekannten Abonnierenden, ihre Kommunikationsvoreinstellungen (Kanal, Themeninteressen) über eine Landingpage zu verwalten, wobei Änderungen in der Regel innerhalb von etwa 15 Minuten in ihrem [!DNL Experience Platform]-Profil widergespiegelt werden.

3. **Ereignis- oder Webinar-Registrierung**: Erfassen Sie ereignisspezifische Daten bekannter Profile auf einer Registrierungsseite, aktualisieren Sie das Profil mit Registrierungsattributen und lösen Sie eine Bestätigungs-Journey aus.

4. **Treue- oder Programmregistrierung**: Ermöglichen Sie es bestehenden Kundinnen und Kunden, sich für Treueprogramme oder Mitgliedschaftsstufen zu registrieren, indem sie zusätzliche Details über eine Landingpage übermitteln, wodurch das Profil für das nachgelagerte Targeting angereichert wird.

5. **Teilnahme an Wettbewerben oder Gewinnspielen**: Ermöglichen Sie es Kundinnen und Kunden, über ein Landingpage-Formular an Wettbewerben oder Gewinnspielen teilzunehmen. Erfassen Sie eintrittsspezifische Details (Antworten, Voreinstellungen oder Erklärungen) und schreiben Sie sie in das Profil, um die Eignung, die Gewinnerauswahl und Folge-Journeys zu unterstützen.

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
<img alt="Formularliste für Landingpages in Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Verwenden von Formularen in Landingpages</strong></a>
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

## Vorbereitung {#prerequisites}

Führen Sie vor dem Erstellen einer Landingpage die folgenden Einrichtungsschritte aus:

1. **Konfigurieren einer Subdomain**: Richten Sie eine Subdomain zum Hosten Ihrer Landingpages ein. [Weitere Informationen](lp-subdomains.md)
1. **Erstellen einer Landingpage-Voreinstellung**: Eine Voreinstellung definiert die Subdomain und andere Einstellungen, die auf Ihre Landingpages angewendet werden. [Weitere Informationen](lp-presets.md#lp-create-preset)
1. **Erstellen einer Abonnement-Liste** (für Abonnement-Anwendungsfälle): Erforderlich, wenn Sie Ihren Kundinnen und Kunden das Abonnieren und Abmelden von einem bestimmten Service ermöglichen möchten. [Weitere Informationen](subscription-list.md)
1. **Erstellen eines Formulars** (für Anwendungsfälle zur Datenerfassung): Erforderlich, wenn Sie ein Formular in eine Landingpage zur **[!UICONTROL Datenerfassung]** einbetten und Übermittlungen an [!DNL Experience Platform] senden möchten. [Weitere Informationen](lp-forms.md)

## Funktionsweise {#how-it-works}

Das Erstellen und Bereitstellen einer Landingpage folgt dieser Reihenfolge:

1. **Erstellen und Konfigurieren der Landingpage**: Wählen Sie eine Voreinstellung aus, richten Sie die Primärseite ein und fügen Sie alle erforderlichen Unterseiten hinzu. [Weitere Informationen](create-lp.md#create-landing-page)
1. **Gestalten der Seite**: Erstellen Sie den Seiteninhalt und das Formular mit dem Drag-and-Drop-Editor von [!DNL Journey Optimizer]. [Weitere Informationen](design-lp.md)
1. **Testen und Veröffentlichen der Landingpage**: Zeigen Sie eine Vorschau der Seite an, testen Sie das Formularverhalten und veröffentlichen Sie die Seite anschließend, um sie live zu schalten. [Weitere Informationen](create-lp.md#test-landing-page)
1. **Verknüpfen einer Nachricht oder Journey**: Fügen Sie die Landingpage-URL zu einer E-Mail-, Kampagnen- oder Journey-Aktion hinzu, damit Kundinnen und Kunden sie erreichen können. [Weitere Informationen](../email/message-tracking.md#insert-links)

## Anleitungsvideo{#video}

Im folgenden Video erfahren Sie, wie Sie eine Abonnement-Liste erstellen, Landingpages zum Opt-in oder Opt-out für einen Service einrichten, die Optionen zum Opt-in oder Opt-out in eine Nachricht integrieren und entsprechende Journeys konfigurieren.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)

➡️ **In der Praxis:** Unter [Anwendungsfälle für Landingpages](lp-use-cases.md) finden Sie schrittweise Beispiele für die Abonnementverwaltung, Bestätigungs-E-Mails und Datenerfassungsszenarien.
