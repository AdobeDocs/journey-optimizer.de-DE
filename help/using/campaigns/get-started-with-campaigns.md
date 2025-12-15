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
source-git-commit: b495462aed9a67ff25c2563288bb2ca57e9b7db7
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 98%

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
>abstract="Den Kampagnentyp auswählen. Die verfügbaren Kanäle variieren je nach ausgewähltem Typ. <br>**Geplante Kampagnen** (Aktionskampagnen) – Ideal für einfache, einmalige Batch-Nachrichten, deren Ausführung für einen bestimmten Zeitpunkt geplant werden kann.<br>**Durch API ausgelöste Kampagnen** – Werden über einen API-Aufruf aktiviert, wodurch direkt von externen Systemen aus automatisiertes, ereignisbasiertes Messaging ermöglicht wird.<br>**Orchestrierte Kampagnen** – Stellen eine visuelle Drag-and-Drop-Arbeitsfläche bereit, auf der komplexe, mehrstufige Marketing-Workflows entworfen und automatisiert werden können: von der Zielgruppensegmentierung bis hin zum kanalübergreifenden Versand personalisierter Nachrichten."

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

Verwenden Sie [!DNL Journey Optimizer]-Kampagnen, um einmalige Inhalte für eine bestimmte Zielgruppe über verschiedene Kanäle hinweg bereitzustellen. Im Gegensatz zu Journeys, die Aktionen Schritt für Schritt ausführen, führen Kampagnen Aktionen gleichzeitig aus, entweder sofort oder nach einem definierten Zeitplan.

![](assets/gs-campaigns.png)

## Kampagnentypen

[!DNL Journey Optimizer] unterstützt drei Kampagnentypen. Jeder Typ eignet sich für verschiedene Anwendungsfälle und unterstützt verschiedene Kanäle. Weitere Informationen zu den für jeden Kampagnentyp verfügbaren Kanälen finden Sie in der Tabelle in diesem Abschnitt: [Kanäle in Journeys und Kampagnen](../channels/gs-channels.md#channels)

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Orchestrierte Kampagnen]

**Orchestrierte Kampagnen** ermöglichen kanalübergreifend anspruchsvolle, markenkonforme Marketing-Kampagnen und helfen Ihnen so, die Interaktion, den Umsatz und die Kundentreue im benötigten Umfang zu fördern.

Kanalübergreifendes Marketing ist unerlässlich, und orchestrierte Kampagnen machen es nahtlos. Auf einer visuellen Drag-and-Drop-Oberfläche können Sie komplexe Marketing-Workflows, von der Segmentierung bis hin zum Nachrichtenversand, über mehrere Kanäle hinweg entwerfen und automatisieren. Alles geschieht in einer intuitiven Umgebung, die auf Geschwindigkeit, Kontrolle und Effizienz ausgelegt ist.

➡️ [Erfahren Sie mehr über das Arbeiten mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md).

>[!TAB Aktionskampagnen (oder geplante Kampagnen)]

**Aktionskampagnen**, auch als geplante Kampagnen bezeichnet, ermöglichen einfache, im Batch versendete Ad-hoc-Nachrichten.

* **Geplant – Marketing**: Für Marketing-Anwendungsfälle wie Werbeangebote, Interaktionskampagnen, Ankündigungen, rechtliche Hinweise oder Richtlinienaktualisierungen. Erfordert, dass Empfängerinnen und Empfänger zugestimmt haben.
* **Geplant – Transaktion**: Im Gegensatz zu Marketing-Kampagnen erfordern Transaktionskampagnen nicht das Opt-in von Empfängerinnen und Empfängern. Verwenden Sie diese Kategorie für Kommunikationen im Zusammenhang mit Störungen, Notfällen, Stornierungen. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigung.

➡️ [Informationen zum Arbeiten mit Aktionskampagnen](create-campaign.md)

>[!TAB Durch API ausgelöste Kampagnen]

**Durch API ausgelöste Kampagnen** ermöglichen es Ihnen, die Ausführung der Kampagne mithilfe eines API-Aufrufs auszulösen. Diese Nachrichten können gesendet werden, wenn möglicherweise nicht nur Personalisierung durch ein Profilattribut zum Zurücksetzen eines Passworts erforderlich ist, sondern auch Echtzeit-Kontextdaten im Trigger, der eine REST-API-Payload darstellt.

* **Durch API ausgelöst – Marketing**: Senden Sie personalisierte Marketing-Nachrichten an ausgewählte Zielgruppen.
* **Durch API ausgelöst – Transaktion**: Senden Sie Nachrichten nach einer Aktion, die von einer Person ausgeführt wurde, z. B. Anfrage zum Zurücksetzen des Passworts, Warenkorbkauf usw.

➡️ [Informationen zum Arbeiten mit durch API ausgelösten Kampagnen](api-triggered-campaigns.md)


>[!ENDTABS]

## Voraussetzungen {#prerequisites}

Stellen Sie vor der Arbeit mit Kampagnen sicher, dass Sie die folgenden Voraussetzungen überprüft haben.

* **Zielgruppen** Zielgruppen müssen vor der Erstellung der Kampagne verfügbar sein. [Erste Schritte mit Zielgruppen](../audience/about-audiences.md).

* **Kanalkonfigurationen**: Damit ein Kanal ausgewählt werden kann, muss die entsprechende Kanalkonfiguration (d. h. Voreinstellung) erstellt worden sein und verfügbar sein. [Erfahren Sie, wie Sie die Kanalkonfiguration einrichten](../configuration/channel-surfaces.md).

* **Berechtigungen**: Kampagnen stehen nur Benutzenden mit den entsprechenden Berechtigungen zur Verfügung, wie unten aufgeführt. Wenn Sie auf bestimmte Kampagnenfunktionen nicht zugreifen können, wenden Sie sich an Ihre bzw. Ihren Admin, um die erforderlichen Berechtigungen anzufordern. [Weitere Informationen über native Rollen in Journey Optimizer](../administration/ootb-product-profiles.md)

  | Kampagnentyp | Berechtigungen |
  |----------------------------|----------------------------------------------------------------------------|
  | **Aktionskampagnen** | Admin einer Kampagne<br>Genehmigende Person einer Kampagne<br>Managerin bzw. Manager einer Kampagne<br>Betrachterin bzw. Betrachter einer Kampagne |
  | **Durch API ausgelöste Kampagnen** | Admin einer Kampagne<br>Genehmigende Person einer Kampagne<br>Managerin bzw. Manager einer Kampagne<br>Betrachterin bzw. Betrachter einer Kampagne |
  | **Orchestrierte Kampagnen** | Admin einer orchestrierten Kampagne<br>Genehmigende Person einer orchestrierten Kampagne<br>Managerin bzw. Manager einer orchestrierten Kampagne<br>Betrachterin bzw. Betrachter einer orchestrierten Kampagne |

  +++Informationen dazu, wie Sie eine kampagnenbezogene Rolle zuweisen

   1. Um einer Person eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie eine der oben beschriebenen nativen, kampagnenbezogenen **[!UICONTROL Rollen]** aus.

   1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   1. Geben Sie Name oder E-Mail-Adresse der jeweiligen Benutzenden ein oder wählen Sie die Person aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

      Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzenden](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users){target="_blank"}.


  Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zu Ihrer Instanz erhalten.

  +++

## Tauchen wir tiefer in die Materie ein

Nachdem Sie sich mit Kampagnen in [!DNL Journey Optimizer] vertraut gemacht haben, ist jetzt der richtige Zeitpunkt, tiefer in diese Dokumentationsabschnitte einzusteigen und Ihre erste Kampagne zu erstellen.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="Aktionskampagnen" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Aktionskampagnen</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Kampagnen, die durch API ausgelöst werden</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrierte Kampagnen</a></td>
</tr></table>
