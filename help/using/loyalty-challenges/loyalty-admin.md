---
solution: Journey Optimizer
product: journey optimizer
title: Treueprogramm konfigurieren
description: Erfahren Sie, wie Sie in Adobe Belohnungsanbieter, Ereignisdefinitionen und Einstellungen auf Unternehmensebene für Ihr Treueprogramm konfigurieren [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 3d894653dd2ac1ddd10a8772da8d5cee21af9bca
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 2%

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

Verwenden Sie die Konfiguration des Treueprogramms in [!DNL Journey Optimizer], um eine Verbindung zu Ihren externen Treuesystemen herzustellen. Marketer verwenden **[!UICONTROL Loyalty Challenges (Beta)]** um Herausforderungen, Aufgaben, Inhalte und Messaging zu entwerfen. Die Konfiguration des Treueprogramms ist ein separater, Administratoren vorbehaltener Bereich für Belohnungserfüllung, Ereigniszuordnung, Produktinventar und Ausschlüsse.

>[!NOTE]
>
>Die Konfiguration des Treueprogramms ist für Administratoren gedacht. Zusätzlich zu den für Herausforderungen im Zusammenhang mit dem Treueprogramm erforderlichen Berechtigungen benötigen Sie Zugriff auf Ihre [!DNL Journey Optimizer]-Instanz auf Administratorebene. Wenden Sie sich an Ihren Adobe-Administrator, um Zugriff anzufordern.

Navigieren Sie zum Öffnen der Konfigurationsoberfläche zu **[!UICONTROL Treue]** und wählen Sie **[!UICONTROL Treueprogramm-Administrator]** aus. Die Benutzeroberfläche ist in Registerkarten unterteilt:

* **Globale Einstellungen** - Den Identity-Namespace von Experience Platform festlegen. [Erfahren Sie, wie Sie globale Einstellungen konfigurieren](#global-settings)
* **Belohnungsanbieter** - Verbinden Sie externe APIs, die Belohnungen erfüllen, einschließlich Belohnungstypen, Proxys und Authentifizierung. [Erfahren Sie, wie Sie Belohnungsanbieter konfigurieren](#reward-providers)
* **Ereignisdefinitionen** - Ordnen Sie eingehende Erlebnisereignisse Aktivitäten zu, die Sie in Aufgaben mit **[!UICONTROL benutzerspezifischen Ereignissen]** verwenden können. [Erfahren Sie, wie Sie Ereignisdefinitionen konfigurieren](#event-definitions)
* **Produktinventar** - Laden Sie Zuordnungen von Elementen zu Gruppen hoch, damit Sie Produktgruppen in den Eignungsregeln für Aufgaben verwenden können. [Erfahren Sie, wie Sie den Produktbestand konfigurieren](#product-inventory)
* **Ausschlüsse** - Laden Sie organisationsweite Element- und Gruppenausschlüsse hoch, die gelten, wenn Marketer Aufgaben konfigurieren. [Erfahren Sie, wie Sie Ausschlüsse konfigurieren](#exclusions)

## Globale Einstellungen {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Globale Einstellungen"
>abstract="Wählen Sie den Identity-Namespace von Adobe Experience Platform für Ihr Treueprogramm aus."

Öffnen Sie die **[!UICONTROL Globale Einstellungen]**. Vorerst besteht die Hauptkonfiguration, die auf dieser Registerkarte verfügbar ist, darin, den Identity-Namespace von Adobe Experience Platform auszuwählen, der von Ihrem Treueprogramm in der Dropdown-Liste **[!UICONTROL Namespace]** verwendet wird.

![](assets/admin-global-settings.png)

➡️ [Erfahren Sie, wie Sie mit Identity-Namespaces arbeiten](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Belohnungsanbieter {#reward-providers}

Ein **Belohnungsanbieter** teilt [!DNL Journey Optimizer] mit, wohin Erfüllungsaufrufe gesendet werden sollen, wenn der Challenge-Fortschritt aufgezeichnet oder eine Challenge abgeschlossen wird, z. B. eine API, die einem Mitgliedskonto Treuepunkte oder Sterne gutschreibt.
* **[!UICONTROL Belohnungsdefinitionen]** - die Belohnungstypen, die dieser Anbieter ausgeben kann (z. B. Sterne oder Meilen).
* **[!UICONTROL Belohnungs-Proxys]** - ein Proxy-Zwischenaufruf, der anstelle Ihres Endpunkts direkt weitergeleitet wird.
* **[!UICONTROL Auth-Token-Generatoren]** - der Mechanismus, mit [!DNL Journey Optimizer] Zugriffs-Token abgerufen werden, bevor die API aufgerufen wird.

Gehen Sie wie folgt vor, um einen Belohnungsanbieter zu erstellen:

1. Öffnen Sie die Registerkarte **[!UICONTROL Belohnungsanbieter]** und wählen Sie **[!UICONTROL Belohnungsanbieter erstellen]** aus.

   ![](assets/admin-reward.png)

1. Geben Sie einen **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** ein.

1. Geben Sie im Feld **[!UICONTROL URL]** die API-URL ein, die Erfüllungsanfragen empfängt.

1. Fügen Sie **[!UICONTROL Kopfzeilen]** nach Bedarf für Ihre API hinzu (z. B. API-Schlüssel oder Inhaltstypen).

1. Konfigurieren Sie die folgenden Ressourcen, die mit Ihrem Belohnungsanbieter verknüpft sind. Erweitern Sie jeden Abschnitt, um weitere Informationen zu erhalten:

   +++Prämiendefinitionen

   Ein Eintrag pro Prämie, die von Ihrem Anbieter unterstützt wird (z. B. Programmpunkte oder Sterne, Geldguthaben). Für jede Definition gilt:

   * Geben Sie einen Namen und eine Beschreibung ein.
   * Geben Sie an, ob die Definition **[!UICONTROL Aktiviert]** ist.
   * Schalten Sie die Option **![!UICONTROL Default]** ein, um eine Definition als Standard für diesen Anbieter zu markieren.
   * Geben Sie die **Payload** an, die mit Erfüllungsaufrufen gesendet werden soll.

   ![](assets/admin-reward-definition.png)

   +++

   +++Belohnungs-Proxy

   Leitet Erfüllungsaufrufe über einen Zwischenserver anstatt direkt an den Endpunkt weiter.

   * Geben Sie einen Namen und eine Beschreibung an.
   * Geben Sie **[!UICONTROL host]**, **[!UICONTROL port]** Informationen ein.
   * Geben Sie an, ob der Proxy **[!UICONTROL aktiviert]** ist.
   * Fügen Sie den Proxy **[!UICONTROL Credential]** hinzu.

   ![](assets/admin-reward-proxies.png)

   +++

   +++Generator für Authentifizierungs-Token

   Wenn Ihre API ein Bearer-Token für die Authentifizierung benötigt.

   * Geben Sie einen Namen und eine Beschreibung ein.
   * Geben Sie im Feld Authentifizierungstyp den Authentifizierungstyp ein (z. B. Bearer).
   * Wählen Sie die zu verwendende HTTP-Methode aus (z. B. POST).
   * Geben Sie die Token-Endpunkt-URL ein. und fügen Sie den **[!UICONTROL Token-Schlüssel]** in der Antwort hinzu (z. B. `access_token`).
   * Geben Sie an, ob der Authentifizierungs-Token **[!UICONTROL Generator aktiviert]**.
   * Fügen Sie bei Bedarf Kopfzeilen hinzu, die für Ihren Token-Endpunkt erforderlich sind.

   [!DNL Journey Optimizer] verwendet diese Konfiguration, um ein neues Token zu erhalten, bevor Sie Ihre Belohnungs-API aufrufen.

   ![](assets/admin-reward-auth.png)

   +++

1. Wählen Sie **[!UICONTROL Belohnungsanbieter erstellen]** aus. Der Anbieter und alle konfigurierten Ressourcen werden zusammen gespeichert.

Nach dem Speichern wird der Anbieter in der Liste der Belohnungsanbieter angezeigt. Marketer können diesen Anbieter bei der Konfiguration von Challenge-Belohnungen auswählen. [Erfahren Sie, wie Sie Challenge Rewards konfigurieren](create-challenges.md#rewards)

Um einen vorhandenen Belohnungsanbieter zu bearbeiten, öffnen Sie die Registerkarte **[!UICONTROL Belohnungsanbieter]**, wählen Sie den Anbieter aus und aktualisieren Sie die Felder an Ort und Stelle. Änderungen an untergeordneten Ressourcen (Belohnungsdefinitionen, Proxys, Authentifizierungs-Token-Generatoren) werden gespeichert, wenn Sie sie aktualisieren.

>[!NOTE]
>
>**[!UICONTROL Bringen Sie Ihre eigenen Daten mit]** Herausforderungen erfüllen Belohnungen durch Ihre eigene Datenintegration. Die hier konfigurierten Belohnungsanbieter gelten nicht für diese Herausforderungen. [Erfahren Sie, wie Sie Ihre eigenen Herausforderungen an Daten stellen](create-challenges.md#create-the-challenge)

## Ereignisdefinitionen {#event-definitions}

**[!UICONTROL Ereignisdefinitionen]** Ordnen Sie Erlebnisereignisse aus Ihren Systemen (z. B. Kauf, Hotel-Check-in) Aktivitäten zu, für die Treueprogramm-Herausforderungen eine Rolle spielen können, insbesondere Aufgaben **[!UICONTROL benutzerspezifische Ereignisse]**. Wenn Ereignisse eintreffen, verwendet [!DNL Journey Optimizer] diese Definitionen, um zu entscheiden, ob sie verarbeitet werden sollen. Ereignisse, die keiner Definition entsprechen, werden ignoriert.

Gehen Sie wie folgt vor, um eine Ereignisdefinition zu erstellen:

1. Öffnen Sie die **[!UICONTROL Ereignisdefinitionen]** und erstellen Sie eine neue Definition.

   ![](assets/admin-event-definition.png)

1. Geben Sie einen **[!UICONTROL Namen]** für das Ereignis ein (z. B. `Coffee purchase`). Dies ist der Name, den Marketer beim Konfigurieren einer Aufgabe vom Typ **[!UICONTROL Benutzerdefiniertes Ereignis]** sehen.

1. Geben Sie an, wie [!DNL Journey Optimizer] das Ereignis in eingehenden Payloads erkennt. Geben Sie einen **[!UICONTROL Kennungspfad]** eine **[!UICONTROL XDM-Schema-ID]** oder beides an:

   * **[!UICONTROL Kennungspfad]** - Pfad zum Feld, das das Ereignis oder Element identifiziert (z. B. `data.memberId`). Verwenden Sie diese Option, wenn Sie Ereignisse anhand von Werten in der Payload abgleichen.
   * **[!UICONTROL Kennungswerte]** - Werte im Kennungspfad, die vorhanden sein müssen, damit diese Definition übereinstimmt.
   * **[!UICONTROL XDM-Schema-]**: ID des Experience Platform-XDM-Schemas für diesen Ereignistyp. Verwenden Sie diese Option, wenn Ereignisse für ein bekanntes Schema erfasst werden.

1. Wenn Marken Ereignisse im eigenen JSON-Format senden, fügen Sie Zeichenfolgen in **[!UICONTROL Schema]** und **[!UICONTROL Transformer]** ein, damit [!DNL Journey Optimizer] die Daten identifizieren, analysieren und entscheiden können, ob sie nachverfolgt werden sollen.

   * **[!UICONTROL Schema]** - Validierungszeichenfolge für die eingehende Payload.
   * **[!UICONTROL Transformer]** - Umwandlungsausdruck (z. B. JSONata), der Ihre Payload dem Format zuordnet, das die Herausforderungen im Zusammenhang mit dem Treueprogramm erwarten.

1. Speichern Sie die Ereignisdefinition. Er wird in der Liste **[!UICONTROL Ereignisdefinitionen]** angezeigt. Sie können ihn jetzt in Challenges einsetzen. [Erfahren Sie, wie Sie Herausforderungen schaffen](create-challenges.md)

## Produktinventar {#product-inventory}

Auf **[!UICONTROL Registerkarte]** Produktinventar“ können Sie Katalogelemente gruppieren, sodass Sie sie in Aufgaben auswählen können, ohne jede Element-ID aufzulisten. Sie laden eine **CSV-Datei** hoch, die jede Elementkennung einer oder mehreren **Produktgruppen** zuordnet (dasselbe Element kann in mehreren Gruppen angezeigt werden). Nach dem Import sind diese Gruppen verfügbar, wenn Sie die Aufgabeneignung konfigurieren. [Erfahren Sie, wie Sie Aufgaben erstellen](create-tasks.md)

Gehen Sie wie folgt vor, um eine Produktinventardatei hochzuladen:

1. Bereiten Sie eine CSV-Datei vor, die jede Artikelkennung einer oder mehreren Produktgruppen zuordnet. Erweitern Sie den folgenden Abschnitt, um ein Beispiel zu sehen.

   +++CSV-Beispiel für Produktinventar

   ![](assets/admin-inventory-csv.png)

   +++

1. Öffnen Sie die Registerkarte **[!UICONTROL Produktinventar]**.

1. Klicken Sie auf **[!UICONTROL Hochladen]** und wählen Sie Ihre CSV-Datei aus.

   ![](assets/admin-inventory-upload.png)

1. Überprüfen Sie die importierte Datei in der Inventarliste. Die Liste zeigt eine Zeile pro Element an. In **[!UICONTROL Spalte „Enthaltene Gruppen in]** wird jede Produktgruppe angezeigt, zu der dieses Element gehört. Jede Gruppe erscheint als eine Pille (mehrere Pillen, wenn das Element in mehreren Gruppen ist).

   ![](assets/admin-inventory-imported.png)

1. Um jedes Element in einer Produktgruppe anzuzeigen, wählen Sie die Pille dieser Gruppe in der Spalte **[!UICONTROL Gruppen enthalten in]** in einer beliebigen Zeile aus. Die Ansicht Gruppendetails listet alle Elemente in der Gruppe auf, nicht nur das Element in der ausgewählten Zeile.

   ![](assets/admin-inventory-group.png)

1. Verwenden **[!UICONTROL Upload-Verlauf]**, um frühere Uploads von CSV-Dateien anzuzeigen.

## Ausschlüsse {#exclusions}

Auf **[!UICONTROL Registerkarte]** Ausschlüsse“ können Sie Katalogelemente und Gruppen definieren, die über Ihr Treueprogramm hinweg ausgeschlossen sind, ohne jede Element-ID in jeder Aufgabe aufzulisten. Sie laden eine **CSV-Datei** hoch, die jede Elementkennung einer oder mehreren **Ausschlussgruppen** zuordnet (dasselbe Element kann in mehreren Gruppen angezeigt werden). Nach dem Import sind diese Elemente und Gruppen im Task Builder verfügbar: Ausgeschlossene Elemente werden automatisch markiert und können nicht in eine Aufgabe aufgenommen werden. Ausschlussgruppen können nur zur Ausschlussliste der Aufgabe hinzugefügt werden, nicht zur Einschlussliste. [Erfahren Sie, wie Sie geeignete Elemente und Ausschlüsse für Aufgaben definieren](create-tasks.md#eligible-items-exclusions)

Gehen Sie wie folgt vor, um eine Produktausschlussdatei hochzuladen:

1. Bereiten Sie eine CSV-Datei vor, die jede Elementkennung einer oder mehreren Ausschlussgruppen zuordnet. Erweitern Sie den folgenden Abschnitt, um ein Beispiel zu sehen.

   +++CSV-Beispiel für Ausschlüsse

   ![](assets/admin-exclusions-csv.png)

   +++

1. Öffnen Sie die **[!UICONTROL Ausschlüsse]**.

1. Klicken Sie auf **[!UICONTROL Hochladen]** und wählen Sie Ihre CSV-Datei aus.

   ![](assets/admin-exclusions-upload.png)

1. Überprüfen Sie die importierte Datei in der Ausschlussliste. Die Liste zeigt eine Zeile pro Element an. In der Spalte **[!UICONTROL Enthaltene Gruppen in]** wird jede Ausschlussgruppe angezeigt, zu der dieses Element gehört. Jede Gruppe erscheint als eine Pille (mehrere Pillen, wenn das Element in mehreren Gruppen ist).

1. Um alle Elemente in einer Ausschlussgruppe anzuzeigen, wählen Sie die Pille dieser Gruppe in der Spalte **[!UICONTROL Gruppen enthalten in]** in einer beliebigen Zeile aus. Die Ansicht Gruppendetails listet alle Elemente in der Gruppe auf, nicht nur das Element in der ausgewählten Zeile.

1. Verwenden **[!UICONTROL Upload-Verlauf]**, um frühere Uploads von CSV-Dateien anzuzeigen.
