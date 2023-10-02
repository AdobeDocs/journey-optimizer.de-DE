---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer Kampagne
description: Erfahren Sie, wie Sie in Journey Optimizer Kampagnen erstellen
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: Erstellen, Optimizer, Kampagne, Oberfläche, Nachrichten
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: a2aaf6bff4af8dff451eb64d68700efda0892c71
workflow-type: ht
source-wordcount: '869'
ht-degree: 100%

---

# Erstellen einer Kampagne {#create-campaign}

>[!NOTE]
>
>Bevor Sie eine neue Kampagne erstellen, überprüfen Sie, ob Sie über eine einsatzbereite Kanaloberfläche (d. h. Nachrichtenvoreinstellung) und Adobe Experience Platform-Zielgruppe verfügen. Weitere Informationen finden Sie in den folgenden Abschnitten:
>
>* [Erstellen von Kanaloberflächen](../configuration/channel-surfaces.md)
>* [Erste Schritte mit Zielgruppen](../audience/about-audiences.md)

Um eine neue Kampagne zu erstellen, klicken Sie im Menü **[!UICONTROL Kampagnen]** auf **[!UICONTROL Kampagne erstellen]**. Sie können auch eine bestehende Live-Kampagne duplizieren, um eine neue Kampagne zu erstellen. [Weitere Informationen](modify-stop-campaign.md#duplicate)

## Auswählen von Kampagnentyp und -kanal {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Kampagnentyp"
>abstract="**Geplante Kampagnen** werden sofort oder an einem bestimmten Datum ausgeführt und dienen zum Senden von Nachrichten des Typs „Marketing“. **API-ausgelöste** Kampagnen werden mithilfe eines API-Aufrufs ausgeführt. Sie dienen dem Versand von Marketing-Nachrichten (Werbenachrichten, für die eine Benutzerzustimmung erforderlich ist) oder von Transaktionsnachrichten (nicht kommerzielle Nachrichten, die in bestimmten Kontexten auch an Profile mit storniertem Abo gesendet werden können)."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Kampagnenkategorie"
>abstract="Wenn Sie eine geplante Kampagne erstellen, wird der Typ **Marketing** automatisch ausgewählt. Für API-ausgelöste Kampagnen wählen Sie, ob Sie eine **Marketing-Nachricht** (Werbenachrichten, für die eine Benutzerzustimmung erforderlich ist) oder eine **Transaktionsnachricht** (nicht kommerzielle Nachrichten, die in bestimmten Kontexten auch an Profile mit storniertem Abo gesendet werden können) senden möchten."

1. Geben Sie im Abschnitt **[!UICONTROL Eigenschaften]** an, wann Sie die Kampagne ausführen möchten. Es stehen zwei Kampagnentypen zur Verfügung:

   * **[!UICONTROL Geplant]**: die Kampagne wird sofort oder an einem bestimmten Datum ausgeführt. Geplante Kampagnen dienen dem Versand von Nachrichten des Typs **Marketing**. Sie werden über die Benutzeroberfläche konfiguriert und ausgeführt.

   * **[!UICONTROL API-ausgelöst]**: die Kampagne wird mithilfe eines API-Aufrufs ausgeführt. API-ausgelöste Kampagnen zielen auf den Versand von Nachrichten des Typs **Marketing** oder **Transaktion** ab. Beim Typ „Transaktion“ handelt es sich um Nachrichten, die nach einer von einem Kontakt durchgeführten Aktion verschickt werden: Zurücksetzen des Passworts, Verlassen des Warenkorbs usw. [Erfahren Sie, wie Sie eine Kampagne mithilfe von APIs auslösen](api-triggered-campaigns.md)

1. Wenn Sie eine geplante Kampagne erstellen, wird der Typ **Marketing** automatisch ausgewählt. Wählen Sie für API-ausgelöste Kampagnen aus, ob Sie eine Nachricht des Typs **Marketing** oder **Transaktion** senden möchten.

1. Wählen Sie im Bereich **[!UICONTROL Aktionen]** den Kanal und die Kanaloberfläche aus, die Sie zum Senden Ihrer Nachricht verwenden möchten.

   Eine Oberfläche ist eine Konfiguration, die durch [Systemadmins](../start/path/administrator.md) definiert worden ist. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Weitere Informationen](../configuration/channel-surfaces.md).

   In der Dropdown-Liste werden nur Kanaloberflächen aufgeführt, die mit dem Typ der Marketing-Kampagne kompatibel sind.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Wenn Sie eine Push-Benachrichtigungskampagne erstellen, können Sie den **[!UICONTROL Schnellversandmodus]** verwenden, ein Add-on zu Journey Optimizer, das den sehr schnellen Versand großer Mengen von Push-Nachrichten ermöglicht. [Weitere Informationen](../push/create-push.md#rapid-delivery)

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um die Kampagne zu erstellen.

## Definieren der Kampagneneigenschaften {#create}

1. Geben Sie im Abschnitt **[!UICONTROL Eigenschaften]** einen Namen und eine Beschreibung für die Kampagne an.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Über das Feld **Tags** können Sie Ihrer Kampagne einheitliche Adobe Experience Platform-Tags zuweisen. Dies ermöglicht eine einfache Klassifizierung und verbesserte Suche über die Kampagnenliste. [Erfahren Sie, wie Sie mit Tags arbeiten.](../start/search-filter-categorize.md#tags)

1. Um der Kampagne benutzerdefinierte oder Core-Bezeichnungen für die Datennutzung zuzuweisen, klicken Sie auf die Schaltfläche **[!UICONTROL Zugriff verwalten]**. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLA)](../administration/object-based-access.md)

## Erstellen der Nachricht und Konfiguration des Trackings {#content}

Erstellen Sie im Bereich **[!UICONTROL Aktionen]** die Nachricht, die mit der Kampagne gesendet werden soll.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**, um den Nachrichteninhalt zu erstellen und zu gestalten.

   Auf den folgenden Seiten erfahren Sie, wie Sie Ihren Nachrichteninhalt erstellen:

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

1. Nachdem Ihr Inhalt definiert ist, verwenden Sie die Schaltfläche **[!UICONTROL Inhalt simulieren]**, um eine Vorschau anzuzeigen und Ihren Inhalt mit Testprofilen zu testen. [Weitere Informationen](../email/preview.md).

1. Klicken Sie auf den Pfeil, um zum Bildschirm für die Kampagnenerstellung zurückzukehren.

   ![](assets/create-campaign-design.png)

1. Geben Sie im Bereich **[!UICONTROL Aktions-Tracking]** an, ob Sie verfolgen möchten, wie Ihre Empfänger(innen) auf Ihren Versand reagieren: Sie können Klicks und/oder Öffnungen verfolgen.

   Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report.md)

## Audience definieren {#audience}

Klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**, um die Liste der verfügbaren Adobe Experience Platform-Segmente anzuzeigen. [Weitere Informationen zu Segmenten](../audience/about-audiences.md)

>[!NOTE]
>
>Für API-ausgelöste Kampagnen muss die Audience über einen API-Aufruf festgelegt werden. [Weitere Informationen](api-triggered-campaigns.md)

Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll. [Weitere Informationen über Namespaces](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

>[!NOTE]
>
>Personen, die zu einem Segment gehören, das nicht die ausgewählte Identität (den ausgewählten Namespace) hat, werden nicht in die Kampagne einbezogen.

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Planen der Kampagne {#schedule}

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

Nachdem Ihre Kampagne fertiggestellt ist, können Sie sie überprüfen und veröffentlichen. [Weitere Informationen](review-activate-campaign.md)
