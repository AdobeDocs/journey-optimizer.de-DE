---
solution: Journey Optimizer
product: journey optimizer
title: Aktivieren von externen Integrationen
description: Integrieren Sie externe Integrationen in den Prozess der Kanalerstellung, um Inhalte mit personalisierten und dynamischen Informationen anzureichern.
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: Integration
hide: true
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
source-git-commit: f40e030e7d14120cdbc118a8f93e2f752d713f6b
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 49%

---

# Arbeiten mit Integrationen {#external-sources}

>[!BEGINSHADEBOX]

Inhaltsverzeichnis:

* **[Arbeiten mit Integrationen](integrations.md)**
* [Erste Schritte](vendor-integration-gs.md)
* [Verfügbare Anbieter](vendor-integration.md)
* [FAQs](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## Überblick

Die **Integrationen**-Funktion verknüpft Adobe Journey Optimizer mit Drittanbietersystemen, deren Daten und zusammenstellbaren Inhalt Sie bereits an anderer Stelle verwalten. Sie können dieses Material beim Authoring und beim Versand aufdecken, was responsivere, personalisierte Erlebnisse für alle in Journey Optimizer verwendeten Kanäle unterstützt.

Sie können diese Funktion verwenden, um externe Daten und Inhalte aus Drittanbieter-Tools abzurufen, z. B.:

* **Prämienpunkte** aus Treueprogrammsystemen.
* **Preisinformationen** für Produkte.
* **Produktempfehlungen** aus Empfehlungs-Engines.
* **Logistische Updates** wie Versandstatus.

Um mit der Verwendung von Integrationen beginnen zu können, müssen Benutzenden die Berechtigungen **[!UICONTROL AJO-Integrationskonfiguration verwalten]** und **[!UICONTROL AJO-Integration anzeigen]** gewährt werden. [Weitere Informationen zu Berechtigungen](../administration/permissions.md)

+++ Erfahren Sie, wie Sie Berechtigungen für Integrationen zuweisen

1. Gehen Sie im Produkt **[!UICONTROL Berechtigungen]** zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie die gewünschte **[!UICONTROL Rolle]** aus.

1. Klicken Sie auf **[!UICONTROL Bearbeiten]**, um die Berechtigungen zu ändern.

1. Fügen Sie die Ressource **[!UICONTROL AJO-]** hinzu und wählen Sie dann die entsprechenden Integrationsberechtigungen aus dem Dropdown-Menü aus.

   ![](assets/external-integration-config-9.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um die Änderungen anzuwenden.

   Die Berechtigungen aller Benutzenden, die dieser Rolle bereits zugewiesen sind, werden automatisch aktualisiert.

1. Um diese Rolle neuen Benutzenden zuzuweisen, navigieren Sie im Dashboard **[!UICONTROL Rollen]** zur Registerkarte **[!UICONTROL Benutzer]** und klicken Sie auf **[!UICONTROL Benutzer hinzufügen]**.

1. Geben Sie den Namen und die E-Mail-Adresse der Benutzerin oder des Benutzers ein oder wählen Sie aus der Liste aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie [diese Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Konfigurieren Ihrer Integration {#configure}

>[!AVAILABILITY]
>
> Diese Integrationsfunktion ist auf ausgehende Kanäle (E-Mail, SMS und Push-Benachrichtigungen) beschränkt und stellt Daten im JSON- oder HTML-Format bereit. Beachten Sie, dass die API schreibgeschützt ist und nur Abrufvorgänge unterstützt.

Als Admin können Sie externe Integrationen einrichten, indem Sie die folgenden Schritte ausführen:

1. Navigieren Sie im linken Menü zum Abschnitt **[!UICONTROL Konfigurationen]** und klicken Sie auf der Karte **[!UICONTROL Integrationen]** auf **[!UICONTROL Verwalten]**.

   Klicken Sie dann auf **[!UICONTROL Integration erstellen]**, um eine neue Konfiguration zu starten.

   ![](assets/external-integration-config-1.png)

1. Fügen Sie optional einen **cURL**-Befehl ein, um die URL, die HTTP-Methode, die Kopfzeilen und Abfrageparameter automatisch auszufüllen.

1. Es müssen ein **[!UICONTROL Name]** und eine **[!UICONTROL Beschreibung]** für die Integration angegeben werden.

   >[!NOTE]
   >
   >Diese Felder dürfen keine Leerzeichen enthalten.

1. Geben Sie die **[!UICONTROL URL]** des API-Endpunkts ein, der Pfadparameter mit Variablen enthalten kann, die sich mithilfe von Labels und Standardwerten definieren lassen.

1. Konfigurieren Sie die **[!UICONTROL Pfadvorlage]** mit **[!UICONTROL Name]** und **[!UICONTROL Standardwert]**.

   ![](assets/external-integration-config-2.png)

1. Wählen Sie die **[!UICONTROL HTTP-Methode]** zwischen GET und POST aus.

1. Klicken Sie je nach Bedarf für Ihre Integration auf **[!UICONTROL Header hinzufügen]** und/oder **[!UICONTROL Abfrageparameter hinzufügen]**. Geben Sie für jeden Parameter die folgenden Details an:

   * **[!UICONTROL Parameter]**: Eine eindeutige Kennung, die intern verwendet wird, um auf den Parameter zu verweisen.

   * **[!UICONTROL Name]**: Der tatsächliche Name des Parameters, wie von der API erwartet.

   * **[!UICONTROL Typ]**: Wählen Sie **Konstante** für einen festen Wert oder **Variable** für eine dynamische Eingabe.

   * **[!UICONTROL Wert]**: Geben Sie für Konstanten den Wert direkt ein oder wählen Sie eine Variablenzuordnung aus.

   * **[!UICONTROL Obligatorisch]**: Geben Sie an, ob dieser Parameter obligatorisch ist.

   ![](assets/external-integration-config-3.png)

1. Wählen Sie einen **[!UICONTROL Authentifizierungstyp]**:

   * **[!UICONTROL Keine Authentifizierung]**: Bei offenen APIs, für die keine Anmeldedaten erforderlich sind.

   * **[!UICONTROL API-Schlüssel]**: Authentifizieren von Anfragen mithilfe eines statischen API-Schlüssels. Geben Sie den **[!UICONTROL API-Schlüsselnamen]**, den **[!UICONTROL API-Schlüsselwert]** und den **[!UICONTROL Speicherort]** an.

   * **[!UICONTROL Einfache Authentifizierung]**: Verwenden der einfachen HTTP-Standardauthentifizierung. Geben Sie **[!UICONTROL Benutzername]** und **[!UICONTROL Kennwort]** ein.

   * **[!UICONTROL OAuth 2.0]**: Authentifizieren mit dem OAuth 2.0-Protokoll. Klicken Sie auf das Symbol ![Bearbeiten](assets/do-not-localize/Smock_Edit_18_N.svg), um die **[!UICONTROL Payload]** zu konfigurieren oder zu aktualisieren.

   ![](assets/external-integration-config-4.png)

1. Legen Sie **[!UICONTROL Richtlinienkonfiguration]** wie **[!UICONTROL Timeout]** für API-Anfragen fest und wählen Sie die Aktivierung von Drosselung, Cache und/oder Wiederholung aus.

   Wenn die Drosselung aktiviert ist, liegen die unterstützten Raten zwischen **50** TPS (Minimum) und **5000** TPS (Maximum).
Wenn der erneute Versuch aktiviert ist, folgen andere Fehler **drei** Wiederholungsversuchen, wobei **200 ms**, **400 ms** und **800 ms** zwischen aufeinander folgenden Versuchen liegen.

1. Mit dem Feld **[!UICONTROL Antwort-Payload]** können Sie festlegen, welche Felder der Beispielausgabe für die Personalisierung von Nachrichten verwendet werden sollen.

   Klicken Sie auf das Symbol ![Bearbeiten](assets/do-not-localize/Smock_Edit_18_N.svg) und fügen Sie eine beispielhafte JSON-Antwort-Payload ein, um Datentypen automatisch zu erkennen.

1. Wählen Sie die Felder aus, die für die Personalisierung bereitgestellt werden sollen, und geben Sie die entsprechenden Datentypen an.

   ![](assets/external-integration-config-5.png)

   >[!NOTE]
   >
   >Die **[!UICONTROL Antwort-Payload]**-Konfiguration definiert die erwartete Antwort für das Authoring einschließlich aller in diesem Schritt angewendeten Schemata. Marketing-Experten dürfen nur auf offen gelegte Felder verweisen. Token für andere Pfade schlagen die Validierung im Editor fehl.

1. Verwenden Sie **[!UICONTROL Testverbindung senden]**, um die Integration zu validieren.

   Klicken Sie nach dem Validieren auf **[!UICONTROL Aktivieren]**.

### Sendezeitbeschränkungen und -verhalten {#configure-send-time}

Zum Zeitpunkt des Versands können Antworten von der externen API standardmäßig bis zu **4 MB**. Alles, was größer ist, wird als Integrationsfehler behandelt und **erneute Versuche werden nicht versucht** wenn der Fehler durch die Antwortgröße verursacht wird.

Die Aufrufe **die von** konfigurierte Drosselungsrate ein: Journey Optimizer plant Versuche bis zu diesem Limit, selbst wenn das externe System ausfällt oder Fehler zurückgibt. Wenn **cache** aktiviert ist, werden nur **erfolgreiche** Antworten gespeichert und wiederverwendet, bis der **TTL** definierte Cache abläuft. Fehlgeschlagene Antworten werden nie zwischengespeichert.

Jede Nachricht in der Warteschlange verfügt außerdem über ein Gültigkeitsfenster (TTL). Wenn die Verarbeitung fehlschlägt und eine Nachricht über dieses Fenster hinausgeht, **das System sie** und gibt ein **`MessageValidityExclusion`** aus, sodass veraltete Arbeit aus der Warteschlange entfernt wird und Ressourcen verfügbar bleiben.


## Verwenden externer Integrationen für die Personalisierung {#personalization}

Bevor Sie externe Integrationen für die Personalisierung verwenden, beachten Sie, dass die Planung und Isolierung von Integrationsaufrufen vom Ausführungskontext abhängen:

* **Batch-Ausführung** (Batch-Kampagnen, orchestrierte Kampagnen und API-ausgelöste Marketing-Kampagnen): Jeder Batch-Vorgang wird in einer dedizierten, isolierten Umgebung ausgeführt. Gleichzeitige Batch-Ausführungen, die externe Systeme aufrufen, stehen daher nicht im Konflikt miteinander oder behindern einander.

* **Einzelausführung** (einheitliche Journey, Batch-Journey und API-ausgelöste Transaktionskampagnen): Der Integrations-Traffic ist pro Marken-Sandbox isoliert, sodass eine langsame externe API für eine Marke die andere nicht verzögert. In Ihrer Sandbox können gleichzeitige Integrationen andere durch die Integration unterstützte Nachrichten kurz verzögern. Jede Nachricht wird bis zu 12 Stunden vor Ablauf des Versands bearbeitet.

Als Marketing-Fachleute können Sie konfigurierte Integrationen verwenden, um Ihre Inhalte zu personalisieren. Führen Sie folgende Schritte aus:

1. Greifen Sie auf Ihren Kampagneninhalt zu und klicken Sie in Ihren Text- oder HTML-**[!UICONTROL Komponenten]** auf **[!UICONTROL Personalisierung hinzufügen]**.

   [Weitere Informationen zu Komponenten](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Navigieren Sie zum Abschnitt **[!UICONTROL Integrationen]** und klicken Sie auf **[!UICONTROL Integrationen öffnen]**, um alle aktiven Integrationen anzuzeigen.

   Beachten Sie, dass Inhaltsfragmente mit Integrationen verfügbar sind, aber nur ausgehende Kanäle unterstützen. Eine eingehende Veröffentlichung ist nicht erfolgreich. Nach der Veröffentlichung eines Fragments ist das Hinzufügen und Speichern neuer Integrationen deaktiviert, um Auswirkungen auf bestehende Journey und Kampagnen zu vermeiden.

   ![](assets/external-integration-content-2.png)

1. Wählen Sie eine Integration aus und klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/external-integration-content-3.png)

1. Aktivieren Sie den **[!UICONTROL Pillen-Modus]**, um das erweiterte Integrationsmenü zu entsperren.

   ![](assets/external-integration-content-4.png)

1. Wenn Sie die Integrationspersonalisierung erstellen, enthält der Integrations-Helper ein **`required`**, das definiert, wie Fehler oder fehlende Daten mit Standardinhalten interagieren:

   * **`required=true`** (Standard): Das Rendern dieser Nachricht wird angehalten. Der Versand wird mit **`ExternalDataLookupExclusion`** ausgeschlossen und dieser Ausschluss wird im **Nachrichten-Feedback-Datensatz“**.
   * **`required=false`**: Die Ergebnisvariable wird auf **`null`** festgelegt und das Rendern wird fortgesetzt. Verwenden Sie Standardtext, Fallbacks oder bedingte Logik in Ihrer Vorlage, damit Profile keine leeren Inhalte erhalten, wenn die Integration keine Daten zurückgibt.

     ![](assets/external-integration-content-8.png)

1. Um die Einrichtung der Integration abzuschließen, definieren Sie die Integrationsattribute, die zuvor bei der [Konfiguration](#configure) angegeben wurden.

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

