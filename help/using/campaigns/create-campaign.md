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
source-git-commit: f9f2cd339680d0dbff1812e64c5082ca97a34771
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 68%

---

# Erstellen einer Kampagne {#create-campaign}

Um eine neue Kampagne zu erstellen, klicken Sie im Menü **[!UICONTROL Kampagnen]** auf **[!UICONTROL Kampagne erstellen]**. Sie können auch eine bestehende Live-Kampagne duplizieren, um eine neue Kampagne zu erstellen. [Weitere Informationen](modify-stop-campaign.md#duplicate)

>[!NOTE]
>
>Bevor Sie eine neue Kampagne erstellen, überprüfen Sie, ob Sie über eine einsatzbereite Kanalkonfiguration (d. h. Nachrichtenoberfläche) und Adobe Experience Platform-Zielgruppe verfügen. Weitere Informationen finden Sie in den folgenden Abschnitten:
>
>* [Erstellen von Kanalkonfigurationen](../configuration/channel-surfaces.md)
>* [Erste Schritte mit Zielgruppen](../audience/about-audiences.md)

## Kampagnentyp auswählen {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Kampagnentyp"
>abstract="**Geplante Kampagnen** werden sofort oder an einem bestimmten Datum ausgeführt und dienen zum Senden von Nachrichten des Typs „Marketing“. **API-ausgelöste** Kampagnen werden mithilfe eines API-Aufrufs ausgeführt. Sie dienen dem Versand von Marketing-Nachrichten (Werbenachrichten, für die eine Benutzerzustimmung erforderlich ist) oder von Transaktionsnachrichten (nicht kommerzielle Nachrichten, die in bestimmten Kontexten auch an Profile mit storniertem Abo gesendet werden können)."

1. Wählen Sie den Typ der Kampagne aus, die Sie ausführen möchten.

   * **[!UICONTROL Geplant – Marketing]**: die Kampagne wird sofort oder an einem bestimmten Datum ausgeführt. Geplante Kampagnen dienen dem Versand von Nachrichten des Typs **Marketing**. Sie werden über die Benutzeroberfläche konfiguriert und ausgeführt.

   * **[!UICONTROL API-ausgelöst – Marketing/Transaktion]**: die Kampagne wird mithilfe eines API-Aufrufs ausgeführt.  API-ausgelöste Kampagnen zielen auf den Versand von Nachrichten des Typs **Marketing** oder **Transaktion** ab. Beim Typ „Transaktion“ handelt es sich um Nachrichten, die nach einer von einem Kontakt durchgeführten Aktion verschickt werden: Zurücksetzen des Passworts, Verlassen des Warenkorbs usw. [Erfahren Sie, wie Sie eine Kampagne mithilfe von APIs auslösen](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um die Kampagne zu erstellen.

## Definieren der Kampagneneigenschaften {#create}

1. Geben Sie im Abschnitt **[!UICONTROL Eigenschaften]** den Namen und eine Beschreibung für Ihre Kampagne ein.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. Verwenden Sie das Feld **Tags** , um Ihrer Kampagne Adobe Experience Platform Unified Tags zuzuweisen. Dies ermöglicht eine einfache Klassifizierung und verbesserte Suche über die Kampagnenliste. [Erfahren Sie, wie Sie mit Tags arbeiten](../start/search-filter-categorize.md#tags).

1. Sie können den Zugriff auf diese Kampagne anhand von Zugriffsbeschriftungen einschränken. Um eine Zugriffsbeschränkung hinzuzufügen, navigieren Sie zur Schaltfläche **[!UICONTROL Zugriff verwalten]** oben auf dieser Seite. Stellen Sie sicher, dass Sie nur Beschriftungen auswählen, für die Sie berechtigt sind. [Erfahren Sie mehr über die Zugriffssteuerung auf Objektebene](../administration/object-based-access.md).

## Definieren der Zielgruppe einer Kampagne {#audience}

Eine Zielgruppe ist eine Gruppe von Personen, die ähnliche Verhaltensweisen und/oder Merkmale aufweisen. Gehen Sie wie folgt vor, um die Zielgruppe der Kampagne festzulegen:

1. Klicken Sie im Abschnitt **Zielgruppe** auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Liste der verfügbaren Adobe Experience Platform-Zielgruppen anzuzeigen. Weitere Informationen zu Zielgruppen finden Sie in [diesem Abschnitt](../audience/about-audiences.md).

1. Wählen Sie im Feld **[!UICONTROL Identitätstyp]** den Schlüsseltyp aus, der zum Identifizieren der Kontakte aus der ausgewählten Zielgruppe verwendet werden soll. Sie können entweder einen vorhandenen Identitätstyp verwenden oder mit dem Adobe Experience Platform Identity-Dienst einen neuen erstellen. Standard-Identitäts-Namespaces werden auf [dieser Seite](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} aufgeführt.

   Pro Kampagne ist nur ein Identitätstyp zulässig. Einzelpersonen, die zu einem Segment gehören, das nicht den ausgewählten Identitätstyp unter ihren verschiedenen Identitäten hat, können nicht als Ziel für die Kampagne ausgewählt werden.

   ![](assets/create-campaign-namespace.png)

   Weitere Informationen zu Identitätstypen und Namespaces finden Sie in der Dokumentation zu [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de){target="_blank"} .

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

>[!IMPORTANT]
>
>* Zielgruppen und Attribute aus der [Zielgruppenkomposition](../audience/get-started-audience-orchestration.md) stehen derzeit nicht zur Verwendung mit Healthcare Shield oder Privacy und Security Shield zur Verfügung
>
>* Für API-ausgelöste Kampagnen muss die Zielgruppe über einen API-Aufruf festgelegt werden.


## Erstellen der Nachricht und Konfigurieren der Tracking-Funktion {#content}

1. Wählen Sie im Abschnitt **[!UICONTROL Aktionen]** den Kanal aus.

   Die Liste der verfügbaren Kanäle hängt von Ihrem Lizenzmodell ab. Für API-gesteuerte Transaktionskampagnen sind nur die Kanäle E-Mail, SMS und Push-Benachrichtigung verfügbar.

1. Wählen Sie die Kanalkonfiguration aus.

   Eine Konfiguration wird durch [Systemadmins](../start/path/administrator.md) definiert. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Weitere Informationen](../configuration/channel-surfaces.md).

   In der Dropdown-Liste werden nur Kanalkonfigurationen aufgeführt, die mit dem Typ der Marketing-Kampagne kompatibel sind.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Wenn Sie eine Push-Benachrichtigungskampagne erstellen, können Sie den **[!UICONTROL Schnellversandmodus]** verwenden, ein Add-on zu Journey Optimizer, das den sehr schnellen Versand großer Mengen von Push-Nachrichten ermöglicht. [Weitere Informationen](../push/create-push.md#rapid-delivery)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**, um Ihre Nachricht zu erstellen und zu gestalten. Auf den folgenden Seiten erfahren Sie, wie Sie Ihren Nachrichteninhalt erstellen:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Lead" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>Erstellen von E-Mails</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Gelegentlich" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>Push-Benachrichtigungen erstellen</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="Validierung" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>Erstellen von SMS-Nachrichten</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

   Nachdem Ihr Inhalt definiert ist, verwenden Sie die Schaltfläche **[!UICONTROL Inhalt simulieren]**, um eine Vorschau anzuzeigen und Ihren Inhalt mit Testprofilen zu testen. [Weitere Informationen](../content-management/preview-test.md). Klicken Sie auf den Linkspfeil, um zum Bildschirm zur Erstellung der Kampagne zurückzukehren.

   ![](assets/create-campaign-design.png)

1. Im Abschnitt **[!UICONTROL Inhaltsexperiment]** können Sie mit der Schaltfläche **[!UICONTROL Experiment erstellen]** testen, welcher Inhalt besser funktioniert. Die Funktionen zur Inhaltserprobung werden in [diesem Abschnitt](../content-management/content-experiment.md) beschrieben.

1. Geben Sie im Bereich **[!UICONTROL Aktions-Tracking]** an, ob Sie verfolgen möchten, wie Ihre Empfänger(innen) auf Ihren Versand reagieren: Sie können Klicks und/oder Öffnungen verfolgen.

   Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report-cja.md)

## Planen der Kampagne {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Kampagnenzeitplan"
>abstract="Standardmäßig starten Kampagnen bei manueller Aktivierung und enden unmittelbar nach dem einmaligen Versand der Nachricht. Sie haben die Flexibilität, ein bestimmtes Datum und eine bestimmte Uhrzeit für den Versand der Nachricht festzulegen. Darüber hinaus können Sie ein Enddatum für wiederkehrende oder API-gesteuerte Kampagnen angeben. In den Aktionsauslösern können Sie auch die Versandhäufigkeit der Nachrichten nach eigenen Wünschen konfigurieren."

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

Standardmäßig starten Kampagnen, sobald sie manuell aktiviert wurden, und enden, sobald die Nachricht einmal gesendet wurde.

Sie können aber auch festlegen, mit welcher Häufigkeit die Nachricht der Kampagne gesendet werden soll. Verwenden Sie dazu die Option **[!UICONTROL Aktions-Trigger]** im Bildschirm zur Kampagnenerstellung, um festzulegen, ob die Kampagne täglich, wöchentlich oder monatlich ausgeführt werden soll.

Wenn Sie Ihre Kampagne nicht direkt nach der Aktivierung ausführen möchten, können Sie das Datum und die Uhrzeit für den Versand der Nachricht mit der Option **[!UICONTROL Kampagnenstart]** angeben. Über die Option **[!UICONTROL Kampagnenende]** können Sie angeben, wann die Ausführung einer wiederkehrenden Kampagne beendet werden soll.

![](assets/create-campaign-schedule.png)

Sobald Ihre Kampagne fertig ist, können Sie sie überprüfen und aktivieren. [Weitere Informationen](review-activate-campaign.md)
