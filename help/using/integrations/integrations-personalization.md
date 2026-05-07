---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden externer Integrationen
description: Integrieren Sie externe Integrationen in den Prozess der Kanalerstellung, um Inhalte mit personalisierten und dynamischen Informationen anzureichern.
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: Integration
source-git-commit: c672ebaf4c0616a2a2bca39bb849bb835c304449
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 22%

---


# Verwenden externer Integrationen für die Personalisierung {#integrations-personalization}

Bevor Sie externe Integrationen in Ihren Inhalten verwenden, bestätigen Sie, dass ein Administrator jede Integration **konfiguriert und aktiviert** (Endpunkt, Authentifizierung, Richtlinien, Antwort-Payload und Aktivierung) hat, wie in [Arbeiten mit Integrationen](integrations.md) beschrieben.

Sie können bis zu **3** Integrationen pro **[!UICONTROL Fragment]** und bis zu **5** der Nachricht hinzufügen. Integrationen, die nur aus Fragmenten stammen, werden nicht für die **5** gezählt.

## Anwenden der Integrationspersonalisierung auf Ihre Inhalte {#apply-integration-personalization}

Als Marketing-Fachleute können Sie konfigurierte Integrationen verwenden, um Ihre Inhalte zu personalisieren. Führen Sie folgende Schritte aus:

1. Greifen Sie auf Ihren Kampagneninhalt zu und klicken Sie in Ihren Text- oder HTML-**[!UICONTROL Komponenten]** auf **[!UICONTROL Personalisierung hinzufügen]**.

   [Weitere Informationen zu Komponenten](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Navigieren Sie zum Abschnitt **[!UICONTROL Integrationen]** und klicken Sie auf **[!UICONTROL Integrationen öffnen]**, um alle aktiven Integrationen anzuzeigen.

   Beachten Sie, dass **Journey Optimizer-Fragmente** für Integrationen verfügbar sind, aber nur ausgehende Kanäle unterstützen. Nach der Veröffentlichung eines Fragments ist das Hinzufügen und Speichern neuer Integrationen deaktiviert, um Auswirkungen auf bestehende Journey und Kampagnen zu vermeiden.

   ![](assets/external-integration-content-2.png)

1. Wählen Sie eine Integration aus und klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/external-integration-content-3.png)

1. Aktivieren Sie den **[!UICONTROL Pillen-Modus]**, um das erweiterte Integrationsmenü zu entsperren.

   ![](assets/external-integration-content-4.png)

1. Wenn Sie die Integrationspersonalisierung erstellen, enthält der Integrations-Helper ein **`required`**, das definiert, wie Fehler oder fehlende Daten mit Standardinhalten interagieren:

   * **`required=true`** (Standard): Das Rendern dieser Nachricht wird angehalten. Der Versand wird mit **`ExternalDataLookupExclusion`** ausgeschlossen und dieser Ausschluss wird im **Nachrichten-Feedback-Datensatz“**.
   * **`required=false`**: Die Ergebnisvariable wird auf **`null`** festgelegt und das Rendern wird fortgesetzt. Verwenden Sie Standardtext, Fallbacks oder bedingte Logik in Ihrer Vorlage, damit Profile keine leeren Inhalte erhalten, wenn die Integration keine Daten zurückgibt.

     ![](assets/external-integration-content-8.png)

1. Um die Einrichtung der Integration abzuschließen, definieren Sie die Integrationsattribute, die zuvor bei der [Konfiguration](integrations.md#configure) angegeben wurden.

   Sie können diesen Attributen Werte zuweisen – entweder mithilfe statischer Werte, die konstant bleiben, oder mithilfe von Profilattributen, die Informationen dynamisch aus Benutzerprofilen abrufen.

   ![](assets/external-integration-content-5.png)

1. Sobald die Integrationsattribute definiert sind, können Sie die Integrationsfelder in Ihren Inhalten für personalisierte Nachrichten verwenden, indem Sie auf das Symbol ![Hinzufügen](assets/do-not-localize/Smock_Add_18_N.svg) klicken.

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >Token in Ihrer Vorlage dürfen nur Felder verwenden, die der Administrator in der Integrationskonfiguration bereitgestellt hat. Beispielsweise ist `{{weatherResponse.temperature}}` gültig, wenn `temperature` verfügbar gemacht wird; `{{weatherResponse.humidity}}` wird im Editor abgelehnt, wenn `humidity` nicht verfügbar ist.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Ihre Integrationspersonalisierung wird jetzt erfolgreich auf Ihre Inhalte angewendet, sodass alle Empfängerinnen und Empfänger ein maßgeschneidertes, relevantes Erlebnis erhalten, das auf den von Ihnen konfigurierten Attributen basiert.

![](assets/external-integration-content-7.png)

## Einen API-Aufruf einem anderen zuordnen {#map-integration-chain}

Sie können Integrationen verketten, sodass die Ergebnisse eines Aufrufs an den nächsten weitergeleitet werden, z. B. Pfadsegmente, Kopfzeilen oder Abfrageparameter. Die Aufrufe werden in der richtigen Reihenfolge in derselben Nachricht ausgeführt, was eine umfassendere Personalisierung ohne benutzerdefinierten Code unterstützt.

Bevor Sie beginnen, stellen Sie Folgendes sicher:

* Ein Administrator hat jede benötigte Integration konfiguriert und aktiviert. Siehe [Konfigurieren der Integration](integrations.md).
* Platzhalter, Kopfzeilen und Abfrageparameter für Variablenpfade werden in der Integrationskonfiguration mit Marketer-orientierten Kennzeichnungen eingerichtet.
* Der Administrator legte die Antwortfelder offen, die Sie für jede Integration in der **[!UICONTROL Antwort-Payload]** benötigen, damit sie beim Authoring angezeigt werden.

Im folgenden Beispiel wird eine Reservierungsintegration verwendet, die eine Flugnummer aus der Buchung des Profils zurückgibt, dann eine Fluginformationsintegration, die diese Nummer für den Live-Status (Verspätungen, Ziel) verwendet. Sie ordnen die Eingaben der zweiten Integration der Antwort des ersten Aufrufs zu.

1. Öffnen Sie Ihre Nachricht oder Ihr Fragment und öffnen Sie den Personalisierungseditor.

   ![](assets/uc-integrations-1.png)

1. Klicken **[!UICONTROL unter]** auf **[!UICONTROL Integrationen öffnen]**.

   ![](assets/uc-integrations-2.png)

1. Fügen Sie die Integration hinzu, deren Antwort den nächsten Aufruf bedient, z. B. Reservierungs- oder Buchungsdaten, die die Flugkennung enthalten.

   ![](assets/uc-integrations-3.png)

1. (Optional) Öffnen Sie das Menü **[!UICONTROL Hilfsfunktion]** und fügen Sie einen Helper hinzu, z. B. die `Let`-Funktion, wenn Sie eine benannte Variable an die Reservierungsantwort binden möchten.

   >[!NOTE]
   >
   > Es sind nur Felder verfügbar, die in der vom Administrator definierten **[!UICONTROL Antwort-Payload]** verfügbar sind. Sie können nicht auf Eigenschaften verweisen, die in der Konfiguration nicht bereitgestellt wurden.

1. Wenn Sie eine Hilfsvariable verwenden, ordnen Sie diese Variable dem Feld zu, das die Reservierungsintegration für die nachgelagerte Verwendung zurückgibt, z. B. die Flugnummer in der Passagier- oder Buchungs-Payload.

   ![](assets/uc-integrations-4.png)

1. Fügen Sie im **[!UICONTROL Integrationen öffnen]** die zweite Integration hinzu, z. B. „Flugstatus“.

   ![](assets/uc-integrations-5.png)

1. Öffnen Sie in der zweiten Integration **[!UICONTROL Integrationsattribute]**. Wählen Sie für jede Eingabe, die Daten aus dem ersten Aufruf wiederverwenden muss, z. B. eine Pfadvariable, Kopfzeile oder Abfrageparameter, eine Zuordnungsquelle aus der ersten Integrationsantwort aus.

   Beim **[!UICONTROL Pillen]**-Erlebnis können Sie die Ausgabe des ersten Aufrufs direkt der Eingabe des zweiten Aufrufs ohne `Let`-Anweisung zuordnen. Wenn Sie `Let` verwendet haben, können Sie stattdessen diese Variable zuordnen.

   ![](assets/uc-integrations-6.png)

1. Fügen Sie Token aus der zweiten Integration mit dem Steuerelement ![add](assets/do-not-localize/Smock_Add_18_N.svg) in Ihren Inhalt ein, z. B. Ziel aus der Fluginformationsantwort.

   ![](assets/uc-integrations-8.png)

1. Speichern Sie Ihren Inhalt.

Beim **[!UICONTROL Simulieren]** oder Senden führt Journey Optimizer Integrationen der Reihe nach aus: Der erste Aufruf verwendet den konfigurierten Profilkontext und das Ergebnis erstellt die zweite Anfrage. Ob eine bestimmte Integration zur Simulations- oder Sendezeit ausgeführt wird, hängt von Ihrer Einrichtung und Ihrem Kanal ab.

![](assets/uc-integrations-7.png)

## Anleitungsvideo {#video}

In diesem Video wird gezeigt, wie **Integrationen** Adobe Journey Optimizer mit externen APIs verbinden, damit Sie Live-Daten und -Inhalte in **ausgehende** Kanäle, E-Mail, SMS und Push-Benachrichtigungen übertragen können, um eine relevantere Personalisierung zu erzielen.

>[!VIDEO](https://video.tv.adobe.com/v/3484118/?learn=on)
