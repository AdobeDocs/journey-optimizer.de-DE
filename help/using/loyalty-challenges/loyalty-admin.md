---
solution: Journey Optimizer
product: journey optimizer
title: Treueprogramm konfigurieren
description: Erfahren Sie, wie Sie in Adobe Belohnungsanbieter, Ereignisdefinitionen, das Produktinventar, Ausschlüsse und Einstellungen auf Unternehmensebene für Ihr Treueprogramm konfigurieren [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 9383220dd57f6a3ebfe67d0d1081b8834b524293
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 1%

---

# Treueprogramm konfigurieren {#loyalty-admin}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md)
* [Zugriff und Verwaltung von Herausforderungen und Aufgaben](access-loyalty-challenges.md)
* [Herausforderungen schaffen](create-challenges.md)
* [Aufgaben erstellen](create-tasks.md)
* [Überwachen der Leistung beim Treueprogramm](loyalty-reporting.md)
* **Treueprogramm konfigurieren** ◀︎ **Sie sind hier**
* [API-Referenz für Herausforderungen im Treueprogramm](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **privaten Betaversion**. Umfassende Informationen über den Veröffentlichungszyklus und die Verfügbarkeitsphasen in [!DNL Journey Optimizer] finden Sie [Veröffentlichungszyklus](../rn/releases.md).

## Überblick {#access-loyalty-admin}

Die Konfiguration des Treueprogramms verbindet [!DNL Journey Optimizer] mit Ihren externen Treuesystemen, indem Belohnungserfüllung, Ereigniszuordnung, Produktinventar und Ausschlüsse eingerichtet werden, bevor Marketer Herausforderungen erstellen können.

>[!NOTE]
>
>Die Konfiguration des Treueprogramms erfordert zusätzlich zu den für Herausforderungen im Zusammenhang mit dem Treueprogramm erforderlichen Berechtigungen Administratorzugriff auf Ihre [!DNL Journey Optimizer]. Wenden Sie sich an Ihren Adobe-Administrator, um Zugriff zu erhalten.

Navigieren Sie zum Öffnen der Konfigurationsoberfläche zu **[!UICONTROL Treue]** und wählen Sie **[!UICONTROL Treueprogramm-Administrator]** aus. Die Benutzeroberfläche ist in Registerkarten unterteilt:

* **Globale Einstellungen** - Wählen Sie den Identity-Namespace von Experience Platform für Ihr Programm aus. [Erfahren Sie, wie Sie globale Einstellungen konfigurieren](#global-settings)
* **Belohnungsanbieter** - Verbinden Sie die APIs, die die Belohnungen erfüllen, wenn Kunden Fortschritte machen oder Herausforderungen meistern. [Erfahren Sie, wie Sie Belohnungsanbieter konfigurieren](#reward-providers)
* **Ereignisdefinitionen** - Ordnen Sie eingehende Erlebnisereignisse Aktivitäten zu, die in Aufgaben **[!UICONTROL Benutzerdefiniertes AEP-Ereignis]** verwendet werden. [Erfahren Sie, wie Sie Ereignisdefinitionen konfigurieren](#event-definitions)
* **Produktinventar** - Laden Sie Zuordnungen von Elementen zu Gruppen hoch, um sie in Eignungsregeln für Aufgaben zu verwenden. [Erfahren Sie, wie Sie den Produktbestand konfigurieren](#product-inventory)
* **Ausnahmen** - Laden Sie organisationsweite Element- und Gruppenausschlüsse für die Aufgabenkonfiguration hoch. [Erfahren Sie, wie Sie Ausschlüsse konfigurieren](#exclusions)

## Globale Einstellungen {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Globale Einstellungen"
>abstract="Wählen Sie den Identity-Namespace von Adobe Experience Platform für Ihr Treueprogramm aus."

Öffnen Sie die **[!UICONTROL Globale Einstellungen]** und wählen Sie den Adobe Experience Platform [Identity-Namespace](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces) **[!UICONTROL für Ihr Treueprogramm in der Dropdown-]** Namespace“ aus. Dieser Namespace muss mit der Art und Weise übereinstimmen, wie Mitgliederprofile in Ihren Daten identifiziert werden.

![](assets/admin-global-settings.png)

➡️ [Erfahren Sie, wie Sie mit Identity-Namespaces arbeiten](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Belohnungsanbieter {#reward-providers}

Ein **Belohnungsanbieter** teilt [!DNL Journey Optimizer] mit, wohin Erfüllungsanrufe gesendet werden sollen, wenn der Challenge-Fortschritt aufgezeichnet oder eine Challenge abgeschlossen ist. Beispielsweise eine API, die Treuepunkte oder Sterne einem Mitgliedskonto gutschreibt.

Gehen Sie wie folgt vor, um einen Belohnungsanbieter zu erstellen:

1. Öffnen Sie die Registerkarte **[!UICONTROL Belohnungsanbieter]** und wählen Sie **[!UICONTROL Belohnungsanbieter erstellen]** aus.

   ![](assets/admin-reward.png)

1. Geben Sie **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** ein.

1. Geben Sie im Feld **[!UICONTROL URL]** den API-Endpunkt ein, der Erfüllungsanfragen empfängt.

1. Fügen Sie **[!UICONTROL Kopfzeilen]** nach Bedarf für Ihre API hinzu (z. B. API-Schlüssel oder Inhaltstypen).

1. Konfigurieren Sie die Ressourcen, die Ihrem Belohnungsanbieter zugeordnet sind. Erweitern Sie die folgenden Abschnitte, um Felddetails anzuzeigen:

   +++Prämiendefinitionen

   Fügen Sie pro Belohnungstyp, den Ihr Anbieter unterstützt, einen Eintrag hinzu (z. B. Programmpunkte, Sterne oder Geldguthaben). Für jede Definition gilt:

   * Geben Sie **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** ein.
   * Geben Sie an, ob die Definition **[!UICONTROL Aktiviert]** ist.
   * Stellen Sie **[!UICONTROL Standard]** ein, um eine Definition als Standard für diesen Anbieter zu markieren.
   * Definieren Sie die **Payload** die mit Erfüllungsaufrufen gesendet wird.

   ![](assets/admin-reward-definition.png)

   +++

   +++Belohnungs-Proxy

   Routet Erfüllungsaufrufe über einen Zwischenserver, anstatt sie direkt an Ihren Endpunkt zu senden. Verwenden Sie auf den Bildschirmen Belohnungsanbieter und **[!UICONTROL Proxy erstellen]** das Feld **[!UICONTROL Anmeldeinformationen]** für die Proxy-Authentifizierung.

   * Geben Sie **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** ein.
   * Geben Sie **[!UICONTROL Host]** und **[!UICONTROL Port]** ein.
   * Geben Sie an, ob der Proxy **[!UICONTROL aktiviert]** ist.
   * Geben **[!UICONTROL unter]** den Proxy-Benutzernamen und das Kennwort als JSON ein. Der Wert der Anmeldeinformationen sieht in der Regel wie folgt aus:

     ```json
     { "userName": "test", "password": "xxxx" }
     ```

   ![](assets/admin-reward-proxies.png)

   +++

   +++Auth-Token-Generator

   Verwenden Sie , wenn Ihre API ein Bearer-Token oder eine ähnliche Authentifizierung erfordert.

   * Geben Sie **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** ein.
   * Geben **[!UICONTROL unter „Authentifizierungstyp]** den Authentifizierungstyp ein (z. B. Bearer).
   * Wählen Sie die HTTP-Methode aus (z. B. POST).
   * Geben Sie die Token-Endpunkt-URL und den **[!UICONTROL Token-Schlüssel]** in der Antwort ein (z. B. `access_token`).
   * Geben Sie an, ob der Authentifizierungs-Token **[!UICONTROL Generator aktiviert]**.
   * Fügen Sie alle Kopfzeilen hinzu, die für Ihren Token-Endpunkt erforderlich sind.

   [!DNL Journey Optimizer] verwendet diese Konfiguration, um vor jedem Aufruf Ihrer Belohnungs-API ein neues Token zu erhalten.

   ![](assets/admin-reward-auth.png)

   +++

1. Wählen Sie **[!UICONTROL Belohnungsanbieter erstellen]** aus. Der Anbieter und alle konfigurierten Ressourcen werden zusammen gespeichert.

Nach dem Speichern wird der Anbieter in der Liste der Belohnungsanbieter angezeigt. Marketer können es bei der Konfiguration von Challenge-Belohnungen auswählen. [Erfahren Sie, wie Sie Challenge Rewards konfigurieren](create-challenges.md#rewards)

Um einen Belohnungsanbieter zu bearbeiten, öffnen Sie die Registerkarte **[!UICONTROL Belohnungsanbieter]**, wählen Sie den Anbieter aus und aktualisieren Sie die Felder an Ort und Stelle. Änderungen an Belohnungsdefinitionen, Proxys und Authentifizierungs-Token-Generatoren werden automatisch gespeichert, wenn Sie sie aktualisieren.

>[!NOTE]
>
>**[!UICONTROL Bringen Sie Ihre eigenen Daten mit]** Herausforderungen erfüllen Belohnungen durch Ihre eigene Datenintegration. Die hier konfigurierten Belohnungsanbieter gelten nicht für diese Herausforderungen. [Erfahren Sie, wie Sie Ihre eigenen Herausforderungen an Daten stellen](create-challenges.md#create-the-challenge)

## Ereignisdefinitionen {#event-definitions}

**[!UICONTROL Ereignisdefinitionen]** teilen [!DNL Journey Optimizer] mit, welche eingehenden Adobe Experience Platform-Erlebnisereignisse verarbeitet werden sollen. Zum Beispiel ein Kauf oder ein Check-in im Hotel. Marketing-Experten verweisen auf diese Definitionen, wenn sie **[!UICONTROL benutzerdefiniertes AEP-]**) erstellen. Ereignisse, die keiner Definition entsprechen, werden ignoriert.

Wenn Ihr Unternehmen Ereignisse im eigenen JSON-Format sendet, helfen **[!UICONTROL Schema]** und **[!UICONTROL Transformer]** dabei, die Payload [!DNL Journey Optimizer] validieren, sie zu analysieren und zu entscheiden, ob die Aktivität verfolgt werden soll.

Gehen Sie wie folgt vor, um eine Ereignisdefinition zu erstellen:

1. Öffnen Sie die **[!UICONTROL Ereignisdefinitionen]** und erstellen Sie eine neue Definition.

   ![](assets/admin-event-definition.png)

1. Geben Sie einen **[!UICONTROL Namen]** für das Ereignis ein (z. B. `Coffee purchase`). Marketing-Experten sehen diesen Namen beim Konfigurieren einer Aufgabe **[!UICONTROL Benutzerdefiniertes AEP-]**).

1. Geben Sie an, wie [!DNL Journey Optimizer] das Ereignis in eingehenden Payloads erkennt. Geben Sie einen **[!UICONTROL Kennungspfad]** eine **[!UICONTROL XDM-Schema-ID]** oder beides an:

   * **[!UICONTROL Kennungspfad]** - Pfad zu einem Feld in der Payload (z. B. `data.memberId`). Verwenden Sie diese Option, wenn Sie Ereignisse anhand von Werten in der Payload abgleichen.
   * **[!UICONTROL Kennungswerte]** - Werte im Kennungspfad, die vorhanden sein müssen, damit diese Definition übereinstimmt.
   * **[!UICONTROL XDM-Schema-]**: ID des Experience Platform-XDM-Schemas für diesen Ereignistyp. Verwenden Sie diese Option, wenn Ereignisse für ein bekanntes Schema erfasst werden.

1. Fügen Sie bei Bedarf Zeichenfolgen in &quot;**[!UICONTROL &quot;]** &quot;**[!UICONTROL &quot;]**:

   * **[!UICONTROL Schema]** - Validierungszeichenfolge für die eingehende Payload.
   * **[!UICONTROL Transformer]** - Umwandlungsausdruck (z. B. JSONata), der Ihre Payload dem Format zuordnet, das die Herausforderungen im Zusammenhang mit dem Treueprogramm erwarten.

1. Speichern Sie die Ereignisdefinition. Er wird in der Liste **[!UICONTROL Ereignisdefinitionen]** angezeigt und ist verfügbar, wenn Marketer **[!UICONTROL benutzerdefiniertes AEP-Ereignis)]**. [Erfahren Sie, wie Sie Aufgaben erstellen](create-tasks.md#choose-activity)

## Produktinventar {#product-inventory}

Die Registerkarte **[!UICONTROL Produktinventar]** gruppiert Katalogelemente, damit Marketing-Experten sie in Aufgaben auswählen können, ohne jede Element-ID einzugeben. Laden Sie eine **CSV-Datei** hoch, die jede Elementkennung einer oder mehreren **Produktgruppen** zuordnet (dasselbe Element kann mehreren Gruppen angehören). Importierte Gruppen sind bei der Konfiguration der Aufgabeneignung verfügbar. [Erfahren Sie, wie Sie Aufgaben erstellen](create-tasks.md)

Gehen Sie wie folgt vor, um eine Produktinventardatei hochzuladen:

1. Bereiten Sie eine CSV-Datei vor, die jede Artikelkennung einer oder mehreren Produktgruppen zuordnet. Erweitern Sie den folgenden Abschnitt, um ein Beispiel zu sehen.

   +++CSV-Beispiel für Produktinventar

   ![](assets/admin-inventory-csv.png)

   +++

1. Öffnen Sie die Registerkarte **[!UICONTROL Produktinventar]**.

1. Wählen Sie **[!UICONTROL Hochladen]** und wählen Sie Ihre CSV-Datei aus.

   ![](assets/admin-inventory-upload.png)

1. Überprüfen Sie die importierten Daten in der Inventarliste. Die Liste zeigt eine Zeile pro Element an. Die Spalte **[!UICONTROL Gruppen enthalten in]** zeigt jede Produktgruppe für dieses Element als Pille oder mehrere Pillen an, wenn das Element zu mehreren Gruppen gehört.

   ![](assets/admin-inventory-imported.png)

1. Um alle Elemente in einer Produktgruppe anzuzeigen, wählen Sie die Pille dieser Gruppe in der Spalte **[!UICONTROL Gruppen enthalten in]** in einer beliebigen Zeile aus. Die Ansicht Gruppendetails listet jedes Element in der Gruppe auf.

   ![](assets/admin-inventory-group.png)

1. Öffnen Sie **[!UICONTROL Upload-Verlauf]**, um frühere CSV-Uploads anzuzeigen.

## Ausschlüsse {#exclusions}

Die Registerkarte **[!UICONTROL Ausschlüsse]** definiert Katalogelemente und Gruppen, die programmweit ausgeschlossen sind, sodass Marketing-Experten nicht bei jeder Aufgabe dieselben Ausschlüsse auflisten müssen. Laden Sie eine **CSV-Datei** hoch, die jede Elementkennung einer oder mehreren **Ausschlussgruppen** zuordnet (dasselbe Element kann mehreren Gruppen angehören).

Nach dem Import werden ausgeschlossene Elemente und Gruppen im Task Builder angezeigt, wenn Marketing-Fachleute **[!UICONTROL Mögliche Elemente und Ausschlüsse]** konfigurieren. [Erfahren Sie, wie Sie geeignete Elemente und Ausschlüsse für Aufgaben definieren](create-tasks.md#eligible-items-exclusions)

Gehen Sie wie folgt vor, um Ausschlüsse hochzuladen:

1. Bereiten Sie eine CSV-Datei vor, die jede Elementkennung einer oder mehreren Ausschlussgruppen zuordnet. Erweitern Sie den folgenden Abschnitt, um ein Beispiel zu sehen.

   +++CSV-Beispiel für Ausschlüsse

   ![](assets/admin-exclusions-csv.png)

   +++

1. Öffnen Sie die **[!UICONTROL Ausschlüsse]**.

1. Wählen Sie **[!UICONTROL Hochladen]** und wählen Sie Ihre CSV-Datei aus.

   ![](assets/admin-exclusions-upload.png)

1. Überprüfen Sie die importierten Daten in der Ausschlussliste. Die Liste zeigt eine Zeile pro Element an. Die Spalte **[!UICONTROL Gruppen enthalten in]** zeigt jede Ausschlussgruppe für dieses Element als Pille oder mehrere Pillen an, wenn das Element zu mehreren Gruppen gehört.

<!-- SCREENSHOT: Exclusions list after CSV upload -->

1. Um alle Elemente in einer Ausschlussgruppe anzuzeigen, wählen Sie die Pille dieser Gruppe in der Spalte **[!UICONTROL Gruppen enthalten in]** in einer beliebigen Zeile aus. Die Ansicht Gruppendetails listet jedes Element in der Gruppe auf.

<!-- SCREENSHOT: Exclusion group details -->

1. Öffnen Sie **[!UICONTROL Upload-Verlauf]**, um frühere CSV-Uploads anzuzeigen.
