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
source-git-commit: 6a32a60f153ff4880ce974e77bc11eed1e20a7c7
workflow-type: tm+mt
source-wordcount: '1518'
ht-degree: 99%

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
>abstract="Erstellen Sie Ihren Segmentierungsfluss, gestalten Sie Ihre kanalübergreifenden Nachrichten und planen Sie Ihre Kampagnen. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigungen, Briefpost."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Kampagnen"
>abstract="Führen Sie einzelne oder wiederkehrende ausgehende Sendungen bzw. fortlaufende eingehende Aktionen aus."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Kampagnen"
>abstract="Stellen Sie einzelne oder wiederkehrende ausgehende Transaktionsaktionen bereit. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigungen."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Kampagnen"
>abstract="Stellen Sie personalisierte Marketing-Nachrichten für ausgewählte Zielgruppen bereit. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigungen."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Kampagnen"
>abstract="Senden Sie Transaktionsnachrichten an einzelne Profile oder Profilgruppen. Unterstützte Kanäle: E-Mail, SMS, Push-Benachrichtigungen."

Adobe Journey Optimizer ermöglicht es Ihnen, zielgerichtete, einmalige Inhalte für bestimmte Zielgruppen über verschiedene Kanäle hinweg bereitzustellen. Mithilfe von Kampagnen können Sie koordinierte Marketing-Aktionen gleichzeitig durchführen und Ihre Zielgruppe mit der richtigen Botschaft zum richtigen Zeitpunkt erreichen.

Dieses Handbuch bietet eine klare Roadmap, die Ihnen hilft, die Grundlagen von Kampagnen zu verstehen, den richtigen Kampagnentyp für Ihren Anwendungsfall auszuwählen und souverän Kampagnen zu entwerfen, die eindrucksvolle Kundenerlebnisse bieten.

## Was sind Kampagnen?

**Kampagnen** sind koordinierte Marketing-Aktionen, die Inhalte für eine bestimmte Zielgruppe über einen oder mehrere Kanäle bereitstellen. Im Gegensatz zu Journeys, bei denen Aktionen sequenziell ausgeführt werden, führen Kampagnen Aktionen gleichzeitig durch – entweder sofort oder nach einem definierten Zeitplan.

[!DNL Journey Optimizer]-Kampagnen ermöglichen Ihnen Folgendes:

* Bereitstellen **einmaliger oder wiederkehrender Inhalte** für ausgewählte Zielgruppensegmente
* Ausführen **koordinierter Multi-Channel-Kommunikationen** über E-Mail, Push, SMS, In-App, Web und mehr
* Auslösen **automatisierter Antworten** über API-Aufrufe für ereignisgesteuertes Messaging in Echtzeit
* Entwerfen **komplexer Marketing-Workflows** mit visuellen Orchestrierungs-Tools

![](assets/gs-campaigns.png)

➡️ **Bereit, mit dem Erstellen zu beginnen?** [Erstellen Sie Ihre erste Kampagne](create-campaign.md) in wenigen Minuten.

## Auswählen des Kampagnentyps {#campaign-types}

**Bevor Sie mit der Erstellung beginnen**, müssen Sie wissen, welcher Kampagnentyp zu Ihrem Anwendungsfall passt. Adobe Journey Optimizer unterstützt drei Kampagnentypen, die jeweils für unterschiedliche Szenarien und Aktivierungsmechanismen konzipiert sind:

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Orchestrierte Kampagnen]

**Verwendung:** Komplexe, mehrstufige Marketing-Workflows

**Orchestrierte Kampagnen** stellen eine visuelle Drag-and-Drop-Arbeitsfläche bereit, auf der komplexe Marketing-Workflows entworfen und automatisiert werden können. Von der Zielgruppensegmentierung bis hin zum kanalübergreifenden Versand personalisierter Nachrichten erfolgt alles in einer intuitiven Umgebung, die auf Geschwindigkeit und Kontrolle ausgelegt ist.

**Ideal für:** Mehrstufige Kundeninteraktionsprogramme, komplexe Segmentierungs- und Targeting-Strategien, Cross-Channel-Kampagnenorchestrierung, markenkonformes Marketing im benötigten Umfang und erweiterte Workflow-Automatisierung mit mehreren Entscheidungspunkten.

➡️ [Erfahren Sie mehr über orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

>[!TAB Aktionskampagnen (geplant)]

**Verwendung:** Einfache, geplante Batch-Nachrichten

**Aktionskampagnen** (auch als „geplante Kampagnen“ bezeichnet) eignen sich ideal für einfache, einmalige oder wiederkehrende Batch-Nachrichten, die zu einem bestimmten Zeitpunkt ausgeführt werden.

**Zwei Kategorien:**

* **Marketing** – Werbeangebote, Interaktionskampagnen, Ankündigungen, rechtliche Hinweise oder Richtlinienaktualisierungen. Erfordert, dass Empfängerinnen und Empfänger zugestimmt haben.
* **Transaktion** – Störungen, Notfälle, Stornierungen. Erfordert kein Opt-in.

**Ideal für:** Monatliche Newsletter an Kundensegmente, zeitkritische Werbeanzeigen, saisonale Marketing-Kampagnen, Mitteilungen zu Produkteinführungen und Benachrichtigungen über Service-Unterbrechungen.

➡️ [Erfahren Sie mehr über Aktionskampagnen](create-campaign.md)

>[!TAB Durch API ausgelöste Kampagnen]

**Verwendung:** Ereignisgesteuertes Messaging in Echtzeit mit externen Systemen

**Durch API ausgelöste Kampagnen** werden über API-Aufrufe aktiviert und ermöglichen automatisiertes Messaging direkt aus externen Systemen. Diese Kampagnen unterstützen die Personalisierung sowohl unter Verwendung von Profilattributen als auch von Echtzeit-Kontextdaten aus der API-Payload.

**Zwei Kategorien:**

* **Marketing** – Personalisierte Marketing-Kommunikationen für ausgewählte Zielgruppen
* **Transaktion** – Nachrichten, die auf einzelne Aktionen folgen (Passwortzurücksetzungen, Warenkorbkäufe usw.)

**Ideal für:** Bestätigungen bei Passwortzurücksetzungen, Wiederherstellung bei Warenkorbabbrüchen, Bestellbestätigungen und Versandaktualisierungen, Benachrichtigungen über Kontoaktivitäten und personalisierte Empfehlungen in Echtzeit.

➡️ [Erfahren Sie mehr über durch API ausgelöste Kampagnen](api-triggered-campaigns.md)

>[!ENDTABS]

>[!NOTE]
>
>Sie wissen nicht genau, welchen Typ sie wählen sollen? Beginnen Sie mit **Aktionskampagnen** für geplante Batch-Nachrichten oder **durch API ausgelösten Kampagnen** für Echtzeit-Messaging. Diese decken die häufigsten Anwendungsfälle ab.

## Voraussetzungen {#prerequisites}

Stellen Sie vor der Arbeit mit Kampagnen sicher, dass die folgenden Voraussetzungen erfüllt sind:

* **Zielgruppen** – Zielgruppen müssen in Adobe Experience Platform verfügbar sein, bevor Kampagnen erstellt werden. [Erste Schritte mit Zielgruppen →](../audience/about-audiences.md)

* **Kanalkonfigurationen** – Kanalkonfigurationen (Voreinstellungen) müssen erstellt werden und für die Kanäle verfügbar sein, die Sie verwenden möchten. [Einrichten von Kanalkonfigurationen →](../configuration/channel-surfaces.md)

* **Berechtigungen** – Sie benötigen die entsprechenden Berechtigungen basierend auf dem Kampagnentyp. Wenden Sie sich an Ihre bzw. Ihren Admin, wenn Sie nicht auf Kampagnenfunktionen zugreifen können. [Informationen zu integrierten Rollen →](../administration/ootb-product-profiles.md)

  +++Liste der Kampagnenberechtigungen

  | Kampagnentyp | Berechtigungen |
  |-------------|---------------|
  | **Aktionskampagnen** und **durch API ausgelöste Kampagnen** | Admin einer Kampagne<br>Genehmigende Person einer Kampagne<br>Managerin bzw. Manager einer Kampagne<br>Betrachterin bzw. Betrachter einer Kampagne |
  | **Orchestrierte Kampagnen** | Admin einer orchestrierten Kampagne<br>Genehmigende Person einer orchestrierten Kampagne<br>Managerin bzw. Manager einer orchestrierten Kampagne<br>Betrachterin bzw. Betrachter einer orchestrierten Kampagne |

  +++

  +++So weisen Sie Kampagnenberechtigungen zu

   1. Navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** im Produkt [!DNL Permissions] und wählen Sie eine der integrierten kampagnenbezogenen **[!UICONTROL Rollen]** aus.

   1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   1. Geben Sie Name oder E-Mail-Adresse der jeweiligen Benutzenden ein oder wählen Sie die Person aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

  Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzenden](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users){target="_blank"}.

  Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zu Ihrer Instanz erhalten.

  +++

## Workflow zur Kampagnenerstellung {#workflow}

Das Erstellen erfolgreicher Kampagnen folgt einem klaren, wiederholbaren Prozess. Im Folgenden finden Sie den Schritt-für-Schritt-Workflow:

+++&#x200B;1. Planen Ihrer Kampagne

Klären Sie Ihre Ziele, bevor Sie beginnen:

* **Was ist das Ziel?** (z. B. Konversionen steigern, Interaktion erhöhen, Kundschaft benachrichtigen)
* **Wer ist die Zielgruppe?** (z. B. in Adobe Experience Platform erstellen oder daraus auswählen)
* **Welcher Kampagnentyp ist am besten geeignet?** (Siehe [Kampagnentypen](#campaign-types) oben)
* **Welche Kanäle möchten Sie verwenden?** (E-Mail, Push, SMS, In-App, Web usw.) → Siehe [Unterstützte Kanäle nach Kampagnentyp](../channels/gs-channels.md#channels)
* **Wann soll die Ausführung erfolgen?** (Sofort, geplant oder durch API ausgelöst)

+++

+++&#x200B;2. Konfigurieren der Kampagneneigenschaften

Legen Sie die Grundlage für Ihre Kampagne fest:

1. **Benennen und beschreiben** Sie Ihre Kampagne zur einfachen Identifizierung
2. **Wählen Sie den Kampagnentyp aus** (Aktion, durch API ausgelöst oder orchestriert)
3. **Wählen Sie Ihre Zielgruppe aus**
4. **Legen Sie die Priorität fest**, falls Sie das Konflikt-Management nutzen
5. **Konfigurieren Sie den Zeitplan** (für Aktionskampagnen) oder die API-Details (für durch API ausgelöste Kampagnen)

**Typspezifische Handbücher:** [Eigenschaften von Aktionskampagnen](campaign-properties.md) | [Eigenschaften von durch API ausgelösten Kampagnen](api-triggered-campaign-properties.md) | [Einrichten orchestrierter Kampagnen](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;3. Gestalten von Inhalten

Erstellen Sie überzeugende Nachricht für Ihre Zielgruppe:

* Verwenden Sie den **E-Mail-Designer** für hochwertige E-Mail-Erlebnisse
* Konfigurieren Sie **Push-Benachrichtigungen** mit Bildern und Deep-Links
* Gestalten Sie **SMS/MMS-Nachrichten** mit Personalisierung
* Erstellen Sie **In-App-** und **Web-** Erlebnisse
* Fügen Sie **Personalisierungen** mithilfe von Profilattributen und kontextuellen Daten hinzu

**Typspezifische Handbücher:** [Inhalte für Aktionskampagnen](campaign-content.md) | [Inhalte für durch API ausgelöste Kampagnen](api-triggered-campaign-content.md) | [Inhalte für orchestrierte Kampagnen](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;4. Überprüfen und Testen

Überprüfen Sie Ihre Kampagne immer vor der Aktivierung:

* **Erstellen Sie eine Vorschau von Inhalten** mit Testprofilen
* **Überprüfen Sie das Targeting**, um die richtige Zielgruppe sicherzustellen
* **Verifizieren Sie den Zeitplan** und die Aktivierungseinstellungen
* **Fordern Sie die Genehmigung an**, falls Sie den Genehmigungs-Workflow verwenden
* **Testen Sie die Zustellbarkeit** mit Testadressenlisten

**Typspezifische Handbücher:** [Überprüfen von Aktionskampagnen](review-activate-campaign.md) | [Überprüfen von durch API ausgelösten Kampagnen](review-activate-api-triggered-campaign.md) | [Überprüfen von orchestrierten Kampagnen](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;5. Aktivieren Ihrer Kampagne

Aktivieren Sie Ihre Kampagne nach Abschluss der Überprüfung:

* **Manuelle Aktivierung** – Aktivieren Sie die Kampagne sofort oder zum geplanten Zeitpunkt
* **Aktivierung durch API** – Verwenden Sie bei durch API ausgelösten Kampagnen den Aktivierungsendpunkt
* **Genehmigungsprozess** – Falls erforderlich, warten Sie auf die Genehmigung durch die Stakeholder

Hinweis: Aktive Kampagnen können nicht bearbeitet werden (Sie müssen diese duplizieren, um Änderungen vorzunehmen)

**Typspezifische Handbücher:** [Aktivieren von Aktionskampagnen](review-activate-campaign.md) | [Aktivieren von durch API ausgelösten Kampagnen](review-activate-api-triggered-campaign.md) | [Aktivieren von orchestrierten Kampagnen](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;6. Überwachen und Analysieren

Verfolgen Sie die Leistung Ihrer Kampagne:

* Zeigen Sie Kampagnenberichte und Analysen an
* Überwachen Sie die Versandraten und Interaktionsmetriken
* Verfolgen Sie Fehlern und Bounces nach
* Analysieren Sie Konversion und ROI
* Verwenden Sie Erkenntnisse zur Optimierung

**Typspezifische Handbücher:** [Berichte für Aktionskampagnen](../reports/campaign-global-report-cja.md) | [Monitoring für durch API ausgelöste Kampagnen](api-triggered-campaigns.md#monitor) | [Analyse für orchestrierte Kampagnen](../orchestrated/create-orchestrated-campaign.md)

+++

## Tauchen wir tiefer in die Materie ein {#get-started-types}

Nachdem Sie nun mit Kampagnen in [!DNL Journey Optimizer] vertraut sind, wählen Sie Ihren Kampagnentyp aus, um zu beginnen:

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="Aktionskampagnen" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Aktionskampagnen</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Kampagnen, die durch API ausgelöst werden</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrierte Kampagnen</a></td>
</tr></table>

Sobald Sie mit Kampagnen vertrauter sind, erkunden Sie diese leistungsstarken Funktionen:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**Planung und Timing**

Planen Sie Kampagnen für bestimmte Daten/Uhrzeiten, legen Sie wiederkehrende Sendungen fest und optimieren Sie die Versandzeiten für maximale Wirkung. (Aktions- und durch API ausgelöste Kampagnen)

[Informationen zur Planung](campaign-schedule.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Ratensteuerung**

Begrenzen Sie den Nachrichtendurchsatz, um eine Überlastung nachgelagerter Systeme wie Landingpages oder Plattformen für die Kundenunterstützung zu verhindern. 

[Ratenbegrenzungen steuern](create-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Zielgruppen-Targeting**

Sprechen Sie bestimmte Adobe Experience Platform-Zielgruppen präzise an und verwalten Sie Qualifikationen für die Zielgruppe dynamisch.

[Zielgruppe einer Kampagne auswählen](campaign-audience.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**Genehmigungs-Workflows**

Implementieren Sie Überprüfungs- und Genehmigungsprozesse, bevor Sie Kampagnen live schalten, um Qualität und Compliance sicherzustellen. (Aktions- und durch API ausgelöste Kampagnen)

[Prüfen und aktivieren](review-activate-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**Ruhezeiten**

Respektieren Sie Kundenpräferenzen, indem Sie den Versand von Nachrichten innerhalb festgelegter Zeitfenster vermeiden. (Aktions- und durch API ausgelöste Kampagnen)

[Ruhezeiten konfigurieren](../conflict-prioritization/quiet-hours.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Optimierung**

Verwenden Sie Targeting-Regeln und Inhaltsexperimente, um personalisierte Inhalte bereitzustellen und die Interaktion zu maximieren.

[Optimieren von Kampagnen](../content-management/gs-message-optimization.md)
:::

::::
