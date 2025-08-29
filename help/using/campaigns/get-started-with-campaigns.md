---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Kampagnen
description: Weitere Informationen zu Kampagnen in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: Kampagne, Vorgehensweise, Starten, Optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '735'
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
>abstract="Legen Sie die Ratensteuerung für die Kampagne fest, indem Sie die gewünschten Ratenbegrenzungen angeben. Diese Funktion ist besonders nützlich, um eine Überlastung nachgelagerter Systeme zu verhindern, beispielsweise Landingpages oder Plattformen für die Kundenunterstützung."

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
>abstract="**Geplante Kampagnen** werden sofort oder an einem bestimmten Datum ausgeführt und dienen zum Senden von Nachrichten des Typs „Marketing“. **API-ausgelöste** Kampagnen werden mithilfe eines API-Aufrufs ausgeführt. Sie dienen dem Versand von Marketing-Nachrichten (Werbenachrichten, für die eine Benutzerzustimmung erforderlich ist) oder von Transaktionsnachrichten (nicht kommerzielle Nachrichten, die in bestimmten Kontexten auch an Profile mit storniertem Abo gesendet werden können)."

Verwenden Sie Journey Optimizer-Kampagnen, um mithilfe verschiedener Kanäle einmalige Inhalte für eine bestimmte Zielgruppe bereitzustellen. Bei Verwendung von Journeys werden die Aktionen nacheinander ausgeführt. Bei Kampagnen werden die Aktionen gleichzeitig ausgeführt, entweder sofort oder nach einem bestimmten Zeitplan.

![](assets/gs-campaigns.png)

In Journey Optimizer können Sie verschiedene Kampagnentypen erstellen:

* **Aktionskampagnen**

  Aktionskampagnen (oder geplante Kampagnen) ermöglichen einfache, im Batch versendete Ad-hoc-Nachrichten für Marketing-Zwecke wie Werbeangebote, Interaktionskampagnen, Ankündigungen, rechtliche Hinweise oder Richtlinienaktualisierungen.

* **Kampagnen, die durch API ausgelöst werden**

  Kampagnen, die durch API ausgelöst werden, ermöglichen den Versand von Marketing-Kommunikation an eine Zielgruppe zum richtigen Zeitpunkt oder den Versand von Transaktions-/Betriebsnachrichten an einen Kontakt, z. B. zum Zurücksetzen des Passworts. Dabei kann eine Personalisierung erforderlich sein, bei der nicht nur das Profilattribut, sondern auch die Echtzeit-Kontextdaten im Trigger verwendet werden, der eine REST-API-Payload ist.

* **Orchestrierte Kampagnen**

  Die Kampagnenorchestrierung in Adobe Journey Optimizer ermöglicht kanalübergreifend anspruchsvolle, markeninitiierte Marketing-Kampagnen und hilft Ihnen so, die Interaktion, den Umsatz und die Kundentreue im benötigten Umfang zu fördern.

  Kanalübergreifendes Marketing ist unerlässlich, und orchestrierte Kampagnen machen es nahtlos. Auf einer visuellen Drag-and-Drop-Oberfläche können Sie komplexe Marketing-Workflows, von der Segmentierung bis hin zum Nachrichtenversand, über mehrere Kanäle hinweg entwerfen und automatisieren. Alles geschieht in einer intuitiven Umgebung, die auf Geschwindigkeit, Kontrolle und Effizienz ausgelegt ist.

## Voraussetzungen {#prerequisites}

Stellen Sie vor der Erstellung Ihrer Kampagne sicher, dass Sie die folgenden Voraussetzungen überprüft haben.

### Berechtigungen

Kampagnen stehen nur Benutzenden mit den entsprechenden Berechtigungen zur Verfügung, wie unten aufgeführt. [Weitere Informationen über native Rollen in Journey Optimizer](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB Aktionskampagnen]

Admin einer Kampagne
Genehmigende Person einer Kampagne
Managerin bzw. Manager einer Kampagne
Betrachterin bzw. Betrachter einer Kampagne

>[!TAB Kampagnen, die durch API ausgelöst werden]

Admin einer Kampagne
Genehmigende Person einer Kampagne
Managerin bzw. Manager einer Kampagne
Betrachterin bzw. Betrachter einer Kampagne

>[!TAB Orchestrierte Kampagnen]

Admin einer orchestrierten Kampagne
Genehmigende Person einer orchestrierten Kampagne
Managerin bzw. Manager einer orchestrierten Kampagne
Betrachterin bzw. Betrachter einer orchestrierten Kampagne

>[!ENDTABS]

Wenn Sie nicht auf bestimmte Kampagnenfunktionen zugreifen können, wenden Sie sich an Ihre bzw. Ihren Admin, um die erforderlichen Berechtigungen anzufordern.

+++Erfahren Sie, wie Sie kampagnenbezogene Rollen zuweisen

1. Um einer Person eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie eine der oben beschriebenen nativen, kampagnenbezogenen **[!UICONTROL Rollen]** aus.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

1. Geben Sie den Namen oder die E-Mail-Adresse der jeweiligen Person ein oder wählen Sie sie aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzenden](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users).

Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zu Ihrer Instanz erhalten.

+++

### Zielgruppe

Zielgruppen müssen vor der Erstellung der Kampagne verfügbar sein. [Erste Schritte mit Zielgruppen](../audience/about-audiences.md).

### Kanalkonfiguration

Um einen Kanal auswählen zu können, muss die entsprechende Kanalkonfiguration (d. h. Voreinstellung) erstellt worden sein und verfügbar sein. [Erfahren Sie, wie Sie die Kanalkonfiguration einrichten](../configuration/channel-surfaces.md).

## Tauchen wir tiefer in die Materie ein

Nachdem Sie sich mit Kampagnen in [!DNL Journey Optimizer] vertraut gemacht haben, ist jetzt der richtige Zeitpunkt, tiefer in diese Dokumentationsabschnitte einzusteigen und Ihre erste Kampagne zu erstellen.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="Aktionskampagnen" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Aktionskampagnen</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Kampagnen, die durch API ausgelöst werden</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrierte Kampagnen</a></td>
</tr></table>
