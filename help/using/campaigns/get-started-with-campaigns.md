---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Kampagnen
description: Weitere Informationen zu Kampagnen in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: Kampagne, Vorgehensweise, Starten, Optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 801b90201c3ffcbfb7b038abac2bf99209a14c7a
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 61%

---

# Erste Schritte mit Kampagnen {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Kampagnenzeitplan"
>abstract="Standardmäßig starten Kampagnen bei manueller Aktivierung und enden unmittelbar nach dem einmaligen Versand der Nachricht. Sie haben die Möglichkeit, ein bestimmtes Datum und eine bestimmte Uhrzeit für den Versand der Nachricht festzulegen. Darüber hinaus können Sie ein Enddatum für wiederkehrende Aktionskampagnen angeben. In den Aktionsauslösern können Sie auch die Versandhäufigkeit der Nachrichten nach eigenen Wünschen konfigurieren."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Kampagnenstart"
>abstract="Geben Sie ein Datum und eine Uhrzeit an, zu der die Nachricht gesendet werden soll."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Kampagnenende"
>abstract="Geben Sie an, wann die Ausführung einer wiederkehrenden Kampagne gestoppt werden soll."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Auslöser für Kampagnenaktionen"
>abstract="Definieren Sie, wie häufig die Nachricht der Kampagne gesendet werden soll."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Ratensteuerung"
>abstract="Legen Sie die Ratensteuerung für Ihre Kampagne fest, indem Sie die gewünschten Ratenbegrenzungen angeben. Diese Funktion ist besonders nützlich, um eine Überlastung nachgelagerter Systeme zu verhindern, beispielsweise Landingpages oder Plattformen für die Kundenunterstützung."

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Erstellen von Kampagnen"
>abstract="Verwenden Sie **Journey Optimizer-Kampagnen**, um mithilfe verschiedener Kanäle einmalige Inhalte für eine bestimmte Zielgruppe bereitzustellen. Bei Verwendung von Journeys werden die Aktionen nacheinander ausgeführt. Bei Kampagnen werden die Aktionen gleichzeitig ausgeführt, entweder sofort oder nach einem bestimmten Zeitplan."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Kampagnen"
>abstract="Kampagnen erstellen, um einmalige Inhalte für eine bestimmte Zielgruppe über verschiedene Kanäle hinweg bereitzustellen. Vor Erstellung einer Kampagne überprüfen, ob eine einsatzbereite Kanalkonfiguration und Adobe Experience Platform-Zielgruppe vorhanden sind."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Kampagnentyp"
>abstract="Wählen Sie den Kampagnentyp aus. Die verfügbaren Kanäle variieren je nach ausgewähltem Typ. <br>**Geplante Kampagnen** (Aktionskampagnen) – Ideal für einfache, einmalige Batch-Nachrichten, deren Ausführung für einen bestimmten Zeitpunkt geplant werden kann.<br>**Per API ausgelöste Kampagnen** – Werden über einen API-Aufruf aktiviert, wodurch direkt von externen Systemen aus automatisiertes, ereignisbasiertes Messaging ermöglicht wird.<br>**Orchestrierte Kampagnen** – Stellen eine visuelle Drag-and-Drop-Arbeitsfläche bereit, auf der komplexe, mehrstufige Marketing-Workflows entworfen und automatisiert werden können: von der Zielgruppensegmentierung bis hin zum kanalübergreifenden Versand personalisierter Nachrichten."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="Kampagnen"
>abstract="Erstellen Sie Ihren Segmentierungsfluss, gestalten Sie Ihre kanalübergreifenden Nachrichten und planen Sie Ihre Kampagnen. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigung."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Kampagnen"
>abstract="Führen Sie einzelne oder wiederkehrende ausgehende Sendungen bzw. fortlaufende eingehende Aktionen aus."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Kampagnen"
>abstract="Stellen Sie einzelne oder wiederkehrende ausgehende Transaktionsaktionen bereit."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Kampagnen"
>abstract="Stellen Sie personalisierte Marketing-Nachrichten für ausgewählte Zielgruppen bereit. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigungen."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Kampagnen"
>abstract="Senden Sie Transaktionsnachrichten an einzelne Profile oder Profilgruppen. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigungen."

Verwenden Sie [!DNL Journey Optimizer] Kampagnen, um einmalige Inhalte für eine bestimmte Zielgruppe über mehrere Kanäle hinweg bereitzustellen. Im Gegensatz zu Journey, die Aktionen Schritt für Schritt ausführen, führen Kampagnen Aktionen gleichzeitig aus - entweder sofort oder nach einem definierten Zeitplan.

![](assets/gs-campaigns.png)

## Kampagnentypen

[!DNL Journey Optimizer] unterstützt drei Kampagnentypen. Jeder Typ eignet sich für verschiedene Anwendungsfälle und unterstützt verschiedene Kanäle.

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Orchestrierte Kampagnen]

**Orchestrierte Kampagnen** ermöglichen anspruchsvolle, markeninitiierte Marketing-Kampagnen über verschiedene Kanäle hinweg und helfen Ihnen so, Interaktion, Umsatz und Kundenloyalität in großem Umfang zu steigern.

Kanalübergreifendes Marketing ist unerlässlich, und orchestrierte Kampagnen machen es nahtlos. Auf einer visuellen Drag-and-Drop-Oberfläche können Sie komplexe Marketing-Workflows, von der Segmentierung bis hin zum Nachrichtenversand, über mehrere Kanäle hinweg entwerfen und automatisieren. Alles geschieht in einer intuitiven Umgebung, die auf Geschwindigkeit, Kontrolle und Effizienz ausgelegt ist.

➡️ [Erfahren Sie, wie Sie mit orchestrierten Kampagnen &#x200B;](../orchestrated/gs-orchestrated-campaigns.md).

>[!TAB Aktionskampagnen (oder geplante Kampagnen)]

**Aktionskampagnen** auch als geplante Kampagnen bezeichnet, ermöglichen einfache, im Batch versendete Ad-hoc-Nachrichten.

* **Geplant - Marketing** - Für Marketing-Anwendungsfälle wie Werbeangebote, Interaktionskampagnen, Ankündigungen, rechtliche Hinweise oder Richtlinienaktualisierungen. Erfordert, dass Empfänger angemeldet werden.
* **Geplant - Transaktion** - Im Gegensatz zu Marketing-Kampagnen erfordern Transaktions-Kampagnen nicht die Anmeldung von Empfängern. Verwenden Sie diese Kategorie für Kommunikationen im Zusammenhang mit Störungen, Notfällen, Stornierungen. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigung.

➡️ [Erfahren Sie, wie Sie mit Aktionskampagnen arbeiten](create-campaign.md)

>[!TAB Durch API ausgelöste Kampagnen]

**API-ausgelöste Kampagnen** ermöglichen es Ihnen, die Ausführung der Kampagne mithilfe eines API-Aufrufs im Trigger zu halten. Diese Nachrichten können an Stellen gesendet werden, an denen eine Personalisierung erforderlich sein kann, indem nicht nur das Profilattribut zum Zurücksetzen des Kennworts zurückgesetzt wird, sondern auch die Echtzeit-Kontextdaten im Trigger, der eine REST-API-Payload ist.

* **API-ausgelöst - Marketing** - Senden Sie personalisierte Marketing-Nachrichten an ausgewählte Zielgruppen.
* **API-ausgelöst - Transaktion** - Senden von Nachrichten nach einer Aktion, die von einer Person ausgeführt wurde, z. B. Anforderung zum Zurücksetzen des Kennworts, Warenkorbkauf usw.

➡️ [Erfahren Sie, wie Sie mit API-ausgelösten Kampagnen arbeiten](api-triggered-campaigns.md)


>[!ENDTABS]

## Unterstützte Kanäle nach Kampagnentyp {#channels}

Die nachstehende Tabelle zeigt die Verfügbarkeit der einzelnen Kanäle über verschiedene Kampagnentypen hinweg und gibt an, wo sie unterstützt werden.

| Kanal | Aktion (Marketing) | Aktion (Transaktion) | API-ausgelöst (Marketing) | API-ausgelöst (Transaktion) | orchestriert |
|----------------------|---------------------|-------------------------|----------------------------|--------------------------------|--------------|
| E-Mail | ✅ | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ | ✅ |
| Push-Benachrichtigung | ✅ | ✅ | ✅ | ✅ | ✅ |
| In-App | ✅ | — | — | — | — |
| Direkt-Mail | ✅ | — | — | — | — |
| Web | ✅ | — | — | — | — |
| Code-basierte Ausl. | ✅ | — | — | — | — |
| Inhaltskarten | ✅ | — | — | — | — |
| WhatsApp | ✅ | — | — | — | — |
| Zeile | ✅ | — | — | — | — |

## Voraussetzungen {#prerequisites}

Bevor Sie mit Kampagnen arbeiten, stellen Sie sicher, dass Sie die folgenden Voraussetzungen gelesen haben.

* **Zielgruppen** Zielgruppen müssen vor der Erstellung der Kampagne verfügbar sein. [Erste Schritte mit Zielgruppen](../audience/about-audiences.md).

* **Kanalkonfigurationen** - Um einen Kanal auswählen zu können, muss die entsprechende Kanalkonfiguration (d. h. Voreinstellung) erstellt und verfügbar sein. [Erfahren Sie, wie Sie die Kanalkonfiguration einrichten](../configuration/channel-surfaces.md).

* **Berechtigungen** - Kampagnen sind nur für Benutzer mit den entsprechenden unten aufgeführten Berechtigungen verfügbar. Wenn Sie nicht auf die Campaign-Funktionen zugreifen können, wenden Sie sich an Ihren Administrator, um die erforderlichen Berechtigungen anzufordern. [Weitere Informationen über native Rollen in Journey Optimizer](../administration/ootb-product-profiles.md)

  | Kampagnentyp | Berechtigungen |
  |----------------------------|----------------------------------------------------------------------------|
  | **Aktionskampagnen** | Campaign-Administrator<br>Campaign-Genehmiger<br>Kampagnen-Manager<br>Kampagnen-Betrachter |
  | **Durch API ausgelöste Kampagnen** | Campaign-Administrator<br>Campaign-Genehmiger<br>Kampagnen-Manager<br>Kampagnen-Betrachter |
  | **Orchestrierte Kampagnen** | Orchestrierte Kampagne Administrator<br>Orchestrierte Kampagne Genehmigende<br>Orchestrierte Kampagne Manager<br>Orchestrierte Kampagne Betrachtende |

  +++Informationen dazu, wie Sie eine kampagnenbezogene Rolle zuweisen

   1. Um einer Person eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie eine der oben beschriebenen nativen, kampagnenbezogenen **[!UICONTROL Rollen]** aus.

   1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   1. Geben Sie den Namen oder die E-Mail-Adresse der jeweiligen Person ein oder wählen Sie sie aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

      Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzenden](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users).

  Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zu Ihrer Instanz erhalten.

  +++

## Tauchen wir tiefer in die Materie ein

Nachdem Sie sich mit Kampagnen in [!DNL Journey Optimizer] vertraut gemacht haben, ist jetzt der richtige Zeitpunkt, tiefer in diese Dokumentationsabschnitte einzusteigen und Ihre erste Kampagne zu erstellen.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="Aktionskampagnen" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Aktionskampagnen</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Kampagnen, die durch API ausgelöst werden</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrierte Kampagnen</a></td>
</tr></table>
