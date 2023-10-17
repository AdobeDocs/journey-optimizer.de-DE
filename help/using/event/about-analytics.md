---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics-Integration
description: Erfahren Sie, wie Sie Adobe Analytics-Daten nutzen. In Journey Optimizer
feature: Reporting, Integrations
topic: Administration
role: Admin
level: Intermediate
keywords: Analytics, Integration, Web-SDK, Plattform
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 100%

---

# Arbeiten mit Adobe Analytics-Daten {#analytics-data}

Alle verhaltensbezogenen Ereignisdaten, die in Adobe Analytics bereits erfasst und an Adobe Experience Platform gestreamt werden, können zum Auslösen von Journeys und zum Automatisieren von Kundenerlebnissen genutzt werden.

Damit dies mit Adobe Analytics funktioniert, müssen Sie:

1. Die Report Suite aktivieren, die Sie verwenden möchten. [Weitere Informationen](#leverage-analytics-data)
1. Journey Optimizer für die Verwendung Ihrer Adobe Analytics-Datenquelle aktivieren. [Weitere Informationen](#activate-analytics-data)
1. Ein bestimmtes Ereignis in Ihre Journey einfügen. [Weitere Informationen](#event-analytic)

>[!NOTE]
>
>Dieser Abschnitt gilt nur für regelbasierte Ereignisse und Kundinnen bzw. Kunden, die Adobe Analytics- oder Web SDK-Daten verwenden müssen.
> 
>Wenn Sie Adobe Customer Journey Analytics verwenden, lesen Sie [diese Seite](../reports/cja-ajo.md).
>

## Konfigurieren von Adobe Analytics- oder Web SDK-Daten {#leverage-analytics-data}

Daten aus Adobe Analytics oder dem Adobe Experience Platform Web SDK müssen aktiviert werden, damit sie in Ihren Journey verwendet werden können.

Gehen Sie dazu wie folgt vor:

1. Navigieren Sie zum Menü **[!UICONTROL Quellen]**.

1. Wählen Sie im Adobe Analytics-Bereich die Option **[!UICONTROL Daten hinzufügen]**.

   ![](assets/ajo-aa_1.png)

1. Wählen Sie aus der Liste der verfügbaren Adobe Analytics Report Suites die zu aktivierende **[!UICONTROL Report Suite]** aus. Klicken Sie dann auf **[!UICONTROL Weiter]**.

   ![](assets/ajo-aa_2.png)

1. Wählen Sie aus, ob Sie ein standardmäßiges oder benutzerdefiniertes Schema verwenden möchten.

1. Wählen Sie im Bildschirm **[!UICONTROL Datenflussdetails]** einen **[!UICONTROL Datenflussnamen]** aus.

1. Nachdem die Konfiguration abgeschlossen ist, klicken Sie auf **[!UICONTROL Beenden]**.

   ![](assets/ajo-aa_3.png)

Dadurch wird der Analytics-Quell-Connector für diese Report Suite aktiviert. Sobald die Daten eingehen, werden sie in ein Erlebnisereignis umgewandelt und an Adobe Experience Platform gesendet.

![](assets/ajo-aa_4.png)

Weitere Informationen zum Adobe Analytics-Quell-Connector finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=de){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=de){target="_blank"}.

## Aktivieren dieser Konfiguration {#activate-analytics-data}

Wenden Sie sich nach dieser Konfiguration an Adobe, um Ihre Journey Optimizer-Umgebung für die Verwendung dieser Datenquelle aktivieren zu lassen. Dieser Schritt ist nur für Adobe Analytics-Datenquellen erforderlich. Um dies durchzuführen:

1. Rufen Sie die Datenquellen-ID ab. Diese Informationen sind in der Benutzeroberfläche verfügbar: Navigieren Sie auf der Registerkarte **Datenflüsse** des Menüs **Quellen** zu der von Ihnen erstellten Datenquelle. Am einfachsten finden Sie sie durch Filtern nach Adobe Analytics-Quellen.
1. Wenden Sie sich mit den folgenden Informationen an die Kundenunterstützung von Adobe:

   * Betreff: Aktivieren von Adobe Analytics-Ereignissen für Journeys

   * Inhalt: Bitte aktivieren Sie für meine Umgebung die Verwendung von AA-Ereignissen.

      * Organisations-ID: „XXX@AdobeOrg“

      * Datenquellen-ID: „ID: xxxxx“

1. Sobald Sie eine Bestätigung erhalten haben, dass Ihre Umgebung bereit ist, können Sie Adobe Analytics-Daten in Ihren Journeys verwenden.

## Erstellen einer Journey mit einem Ereignis mithilfe von Adobe Analytics- oder Web SDK-Daten {#event-analytics}

Sie können jetzt ein Ereignis erstellen, das auf Adobe Analytics- oder Adobe Experience Platform Web SDK-Daten basiert, die in einer Journey verwendet werden sollen.

Im folgenden Beispiel erfahren Sie, wie Sie Benutzerinnen und Benutzer ansprechen können, die ein Produkt zum Warenkorb hinzugefügt haben:

* Zwei Tage nach Abschluss der Bestellung erhalten sie eine E-Mail-Folgenachricht mit der Bitte um Feedback.
* Wenn die Bestellung noch nicht abgeschlossen ist, erhalten Benutzerinnen bzw. Benutzer eine E-Mail, in der sie daran erinnert werden, die Bestellung abzuschließen.

1. Öffnen Sie über Adobe Journey Optimizer das Menü **[!UICONTROL Konfiguration]**.

1. Wählen Sie anschließend **[!UICONTROL Verwalten]** in der Karte **[!UICONTROL Ereignisse]**.

   ![](assets/ajo-aa_5.png)

1. Klicken auf **[!UICONTROL Ereignis erstellen]**. Der Bereich für die Ereigniskonfiguration wird auf der rechten Seite des Bildschirms geöffnet.

1. Füllen Sie die **[!UICONTROL Ereignis]**-Parameter aus:

   * **[!UICONTROL Name]**: Personalisieren Sie den Namen Ihres **[!UICONTROL Ereignisses]**.
   * **[!UICONTROL Typ]**: Wählen Sie den Typ **[!UICONTROL Einzelfall]**. [Weitere Informationen](../event/about-events.md)
   * **[!UICONTROL Ereignis-ID-Typ]**: Wählen Sie den Ereignis-ID-Typ **[!UICONTROL Regelbasiert]**. [Weitere Informationen](../event/about-events.md#event-id-type)
   * **[!UICONTROL Schema]**: Wählen Sie das [zuvor erstellt](#leverage-analytics-data) Analytics- oder WebSDK-Schema aus.
   * **[!UICONTROL Felder]**: Wählen Sie die Payload-Felder aus. [Weitere Informationen](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Ereignis-ID-Bedingung]**: Definieren Sie die Bedingung, um die Ereignisse zu identifizieren, die Ihre Journey auslösen werden.

     Hier wird das Ereignis ausgelöst, wenn Kundinnen bzw. Kunden einen Artikel zu ihrem Warenkorb hinzufügen.
   * **[!UICONTROL Profilkennung]**: Wählen Sie ein Feld aus Ihren Payload-Feldern aus oder definieren Sie eine Formel, um die mit dem Ereignis verknüpfte Person zu identifizieren.

   ![](assets/ajo-aa_6.png)

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Jetzt, da das Ereignis bereit ist, erstellen Sie eine Journey, um es zu verwenden.

1. Öffnen oder erstellen Sie eine Journey mithilfe des Menüs **[!UICONTROL Journey]**. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../building-journeys/journey-gs.md).

1. Fügen Sie Ihre zuvor konfigurierten Analytics-Ereignisse zu Ihrer Journey hinzu.

   ![](assets/ajo-aa_8.png)

1. Fügen Sie ein Ereignis hinzu, das ausgelöst wird, wenn eine Bestellung abgeschlossen ist.

1. Wählen Sie im **[!UICONTROL Ereignismenü]** die Optionen **[!UICONTROL Maximale Wartezeit für Ereignisse definieren]** und **[!UICONTROL Zeitüberschreitungspfad festlegen]** aus.

   ![](assets/ajo-aa_9.png)

1. Fügen Sie im Zeitüberschreitungspfad die Aktion **[!UICONTROL E-Mail]** hinzu. Dieser Pfad wird verwendet, um eine E-Mail an Kunden bzw. Kundinnen zu senden, die keine Bestellung abgeschlossen haben, um sie daran zu erinnern, dass sich noch Waren in ihrem Warenkorb befinden.

1. Fügen Sie nach Ihrem Hauptpfad die Aktivität **[!UICONTROL Warten]** hinzu und wählen Sie dafür die erforderliche Dauer aus.

   ![](assets/ajo-aa_10.png)

1. Fügen Sie dann eine **[!UICONTROL E-Mail-Aktion]** hinzu. In dieser E-Mail werden die Kunden bzw. Kundinnen aufgefordert, Feedback zur aufgegebenen Bestellung abzugeben.

Sie können Ihre Journey jetzt testen und veröffentlichen. [Weitere Informationen](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
