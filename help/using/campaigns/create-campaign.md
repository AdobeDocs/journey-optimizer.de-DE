---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer Kampagne
description: Erfahren Sie, wie Sie in Journey Optimizer Kampagnen erstellen
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: Erstellen, Optimizer, Kampagne, Oberfläche, Nachrichten
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 03cb3298c905766bc059e82c58969a2111379345
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 42%

---

# Erstellen einer Kampagne {#create-campaign}

Um eine neue Kampagne zu erstellen, navigieren Sie in der linken Leiste zum Menü **[!UICONTROL Kampagnen]** und klicken Sie dann auf **[!UICONTROL Kampagne erstellen]** . Sie können auch eine bestehende Live-Kampagne duplizieren, um eine neue Kampagne zu erstellen. [Erfahren Sie, wie ](modify-stop-campaign.md#duplicate).

Bevor Sie beginnen, lesen Sie die Kampagnenvoraussetzungen auf [dieser Seite](get-started-with-campaigns.md#before-starting-campaign-prerequisites) durch.

## Auswählen des Kampagnentyps {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Kampagnentyp"
>abstract="**Geplante Kampagnen** werden sofort oder an einem bestimmten Datum ausgeführt und dienen zum Senden von Nachrichten des Typs „Marketing“. **API-ausgelöste** Kampagnen werden mithilfe eines API-Aufrufs ausgeführt. Sie dienen dem Versand von Marketing-Nachrichten (Werbenachrichten, für die eine Benutzerzustimmung erforderlich ist) oder von Transaktionsnachrichten (nicht kommerzielle Nachrichten, die in bestimmten Kontexten auch an Profile mit storniertem Abo gesendet werden können)."

Bei der Erstellung einer neuen Kampagne muss zunächst der Kampagnentyp ausgewählt werden. Es stehen drei Kampagnentypen zur Verfügung:

1. **[!UICONTROL Geplant - Marketing]** - Diese Kampagnen werden sofort oder an einem bestimmten Datum ausgeführt. Geplante Kampagnen zielen darauf ab, **Marketing** -Nachrichten zu senden oder eingehende Aktionen zu erstellen. Sie werden über die Benutzeroberfläche konfiguriert und ausgeführt.

1. **[!UICONTROL API-ausgelöst - Marketing]** - Diese Kampagnen werden mithilfe eines API-Aufrufs ausgeführt. Wählen Sie diesen Kampagnentyp aus, um personalisierte Marketingnachrichten an Zielgruppen zu senden.  [Erfahren Sie, wie Sie eine Kampagne mithilfe von APIs auslösen](api-triggered-campaigns.md)

1. **[!UICONTROL API-ausgelöst - Transaktion]** - Wie bei API-ausgelösten Marketing-Kampagnen werden diese Kampagnen mithilfe eines API-Aufrufs ausgeführt. API-gesteuerte Transaktionskampagnen zielen darauf ab, **Transaktionsnachrichten** zu senden, d. h. Nachrichten, die aufgrund einer von einer Person durchgeführten Aktion gesendet werden: Anforderung zum Zurücksetzen des Kennworts, Warenkorb usw.  [Erfahren Sie, wie Sie eine Kampagne mithilfe von APIs auslösen](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

## Definieren der Kampagneneigenschaften {#create}

Nach der Erstellung der Kampagne müssen deren Eigenschaften definiert werden. Führen Sie dazu folgende Schritte durch:

1. Geben Sie im Abschnitt **[!UICONTROL Eigenschaften]** den Namen und eine Beschreibung für Ihre Kampagne ein.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. (Optional) Verwenden Sie das Feld **Tags** , um Ihrer Kampagne Adobe Experience Platform Unified Tags zuzuweisen. Dies ermöglicht eine einfache Klassifizierung und verbesserte Suche über die Kampagnenliste. [Erfahren Sie, wie Sie mit Tags arbeiten](../start/search-filter-categorize.md#tags).

1. (Optional) Sie können den Zugriff auf diese Kampagne anhand von Zugriffsbeschriftungen einschränken. Um eine Zugriffsbeschränkung hinzuzufügen, navigieren Sie zur Schaltfläche **[!UICONTROL Zugriff verwalten]** oben auf dieser Seite. Stellen Sie sicher, dass Sie nur Beschriftungen auswählen, für die Sie berechtigt sind. [Erfahren Sie mehr über die Zugriffssteuerung auf Objektebene](../administration/object-based-access.md).

## Definieren der Zielgruppe einer Kampagne {#audience}

Jetzt können Sie die Audience Ihrer Kampagne auswählen. Eine Zielgruppe ist eine Gruppe von Personen, die ähnliche Verhaltensweisen und/oder Merkmale aufweisen.

>[!IMPORTANT]
>
>* Zielgruppen und Attribute aus der [Zielgruppenkomposition](../audience/get-started-audience-orchestration.md) stehen derzeit nicht zur Verwendung mit Healthcare Shield oder Privacy und Security Shield zur Verfügung
>
>* Bei API-ausgelösten Kampagnen muss die Zielgruppe über einen API-Aufruf festgelegt werden.


Gehen Sie wie folgt vor, um die Zielgruppe einer geplanten Marketing-Kampagne zu definieren:

1. Klicken Sie im Abschnitt **Zielgruppe** auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Liste der verfügbaren Adobe Experience Platform-Zielgruppen anzuzeigen. Weitere Informationen zu Zielgruppen finden Sie in [diesem Abschnitt](../audience/about-audiences.md).

1. Wählen Sie im Feld **[!UICONTROL Identitätstyp]** den Schlüsseltyp aus, der zum Identifizieren der Kontakte aus der ausgewählten Zielgruppe verwendet werden soll. Sie können entweder einen vorhandenen Identitätstyp verwenden oder mit dem Adobe Experience Platform Identity-Dienst einen neuen erstellen. Standard-Identitäts-Namespaces werden auf [dieser Seite](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} aufgeführt.

   Pro Kampagne ist nur ein Identitätstyp zulässig. Einzelpersonen, die zu einem Segment gehören, das nicht den ausgewählten Identitätstyp unter ihren verschiedenen Identitäten hat, können nicht als Ziel für die Kampagne ausgewählt werden.

   ![](assets/create-campaign-namespace.png)

   Weitere Informationen zu Identitätstypen und Namespaces finden Sie in der Dokumentation zu [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de){target="_blank"} .

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->


## Kanal auswählen {#channel}

Jetzt können Sie den Kanal und seine Konfiguration auswählen. Führen Sie dazu folgende Schritte durch:

1. Wählen Sie im Abschnitt **[!UICONTROL Aktion]** den Kommunikationskanal aus.

   Die Liste der verfügbaren Kanäle hängt von Ihrem Lizenzmodell und Ihren Add-ons ab. Für API-gesteuerte Kampagnen sind nur die Kanäle E-Mail, SMS und Push-Benachrichtigung verfügbar.

1. Wählen Sie die Kanalkonfiguration aus.

   Eine Konfiguration wird durch [Systemadmins](../start/path/administrator.md) definiert. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Weitere Informationen](../configuration/channel-surfaces.md).

   In der Dropdown-Liste werden nur Kanalkonfigurationen aufgeführt, die mit dem Typ der Marketing-Kampagne kompatibel sind.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Wenn Sie eine Push-Benachrichtigungskampagne erstellen, können Sie den **[!UICONTROL Schnellversandmodus]** verwenden, ein Add-on zu Journey Optimizer, das den sehr schnellen Versand großer Mengen von Push-Nachrichten ermöglicht. [Weitere Informationen](../push/create-push.md#rapid-delivery)

## Inhalt bearbeiten {#content}

Sie können jetzt den Inhalt der Nachricht über die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** definieren. Der Inhaltserstellungsprozess hängt vom ausgewählten Kanal ab.

Auf den folgenden Seiten erfahren Sie, wie Sie Ihren Nachrichteninhalt erstellen:


<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="E-Mail" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>E-Mail</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="Push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>Push-Benachrichtigung</strong></a></div></td>
<td><a href="../direct-mail/create-direct-mail.md"><img alt="Briefpost" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><a href="../direct-mail/create-direct-mail.md"><strong>Briefpost</strong></a></div></td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../in-app/create-in-app.md"><img alt="in der App" src="../channels/assets/do-not-localize/inapp.jpg"></a>
<div align="center"><a href="../in-app/create-in-app.md"><strong> In-App</strong></a></div></td>
<td><a href="../web/create-web.md"><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></a>
<div align="center"><a href="../web/create-web.md"><strong>Web</strong></a></div></td>
<td><a href="../code-based/create-code-based.md"><img alt="code-basiertes Erlebnis" src="../channels/assets/do-not-localize/code.png"></a>
<div align="center"><a href="../code-based/create-code-based.md"><strong>Code-basiertes Erlebnis</strong></a></div></td>
<td><a href="../content-card/create-content-card.md"><img alt="Inhaltskarten" src="../channels/assets/do-not-localize/cards.png"></a>
<div align="center"><a href="../content-card/create-content-card.md"><strong>Inhaltskarten</strong></a></div></td>
</tr></table>

Sobald Ihr Inhalt definiert ist, verwenden Sie die Schaltfläche **[!UICONTROL Inhalt simulieren]** , um Ihren Inhalt mit Testprofilen oder Beispieleingabedaten, die aus einer CSV-/JSON-Datei hochgeladen oder manuell hinzugefügt wurden, in der Vorschau anzuzeigen und zu testen. [Weitere Informationen](../content-management/preview-test.md). Klicken Sie auf den Linkspfeil, um zum Bildschirm zur Erstellung der Kampagne zurückzukehren.

![](assets/create-campaign-design.png)

Zusätzlich zum Nachrichteninhalt selbst können Sie die folgenden Einstellungen konfigurieren:

1. (optional) Im Abschnitt **[!UICONTROL Inhaltserlebnis]** können Sie mit der Schaltfläche **[!UICONTROL Experiment erstellen]** testen, welche Inhalte besser funktionieren. Die Funktionen zur Inhaltserprobung werden in [diesem Abschnitt](../content-management/content-experiment.md) beschrieben.

1. Geben Sie im Bereich **[!UICONTROL Aktions-Tracking]** an, ob Sie verfolgen möchten, wie die Empfangenden auf Ihren Versand reagieren: Sie können Klicks und/oder Öffnungen verfolgen.

   Die Tracking-Ergebnisse sind nach Ausführung der Kampagne über den Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report-cja.md)

## Planen der Kampagne {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Kampagnenzeitplan"
>abstract="Standardmäßig starten Kampagnen bei manueller Aktivierung und enden unmittelbar nach dem einmaligen Versand der Nachricht. Sie können ein bestimmtes Datum und eine Uhrzeit für den Versand der Nachricht festlegen. Darüber hinaus können Sie ein Enddatum für wiederkehrende oder API-gesteuerte Kampagnen angeben. In den Aktionsauslösern können Sie auch die Versandhäufigkeit der Nachrichten nach eigenen Wünschen konfigurieren."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Kampagnenstart"
>abstract="Geben Sie ein Datum und eine Uhrzeit an, zu der die Nachricht gesendet werden soll."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Kampagnenende"
>abstract="Geben Sie an, wann die Ausführung einer wiederkehrenden Kampagne beendet werden soll."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Auslöser für Kampagnenaktionen"
>abstract="Definieren Sie, wie häufig die Nachricht der Kampagne gesendet werden soll."

Geplante Kampagnen beginnen standardmäßig, sobald sie manuell aktiviert werden, und enden, sobald die Nachricht einmal gesendet wurde.

Wenn Sie Ihre Kampagne nicht direkt nach der Aktivierung ausführen möchten, können Sie das Datum und die Uhrzeit für den Versand der Nachricht mit der Option **[!UICONTROL Kampagnenstart]** angeben. Mit der Option **[!UICONTROL Kampagnenende]** können Sie festlegen, wann die Ausführung einer Kampagne beendet werden soll.

![](assets/create-campaign-schedule.png)

Bei E-Mail-, SMS- und Push-Benachrichtigungs-Kampagnen können Sie festlegen, mit welcher Häufigkeit die Nachricht der Kampagne gesendet werden soll. Verwenden Sie dazu die Option **[!UICONTROL Aktions-Trigger]** im Bildschirm zur Kampagnenerstellung, um festzulegen, ob die Kampagne täglich, wöchentlich oder monatlich ausgeführt werden soll.

## Andere Einstellungen {#settings}

Einige Einstellungen beziehen sich auf den Kommunikationskanal, der für die Kampagne ausgewählt oder für bestimmte Anwendungsfälle verwendet wird. Sie werden nachfolgend beschrieben.

* Für E-Mails können Sie spezifische Aktivierungskampagnen für IP-Aufwärmspläne erstellen. Weiterführende Informationen finden Sie in [diesem Abschnitt](../configuration/ip-warmup-campaign.md).
* Für Web-, In-App- und code-basierte Kanäle können Sie Ihrer Kampagne eine Prioritätsbewertung zuweisen. Weiterführende Informationen finden Sie in [diesem Abschnitt](../conflict-prioritization/priority-scores.md).
* Für Inhaltskampagnenkampagnen können Sie zusätzliche Versandregeln aktivieren, um die Ereignisse und Kriterien auszuwählen, durch die Ihre Nachricht Trigger wird. Weiterführende Informationen finden Sie in [diesem Abschnitt](../content-card/create-content-card.md).
* Bei In-App-Nachrichten können Sie über die Schaltfläche **[!UICONTROL Trigger bearbeiten]** die Ereignisse und Kriterien auswählen, auf die Ihre Nachricht Trigger wird. Weiterführende Informationen finden Sie in [diesem Abschnitt](../in-app/create-in-app.md).

## Nächste Schritte {#next}

Sobald Ihre Kampagnenkonfiguration und Ihr Inhalt fertig sind, können Sie sie überprüfen und aktivieren. [Weitere Informationen](review-activate-campaign.md)
