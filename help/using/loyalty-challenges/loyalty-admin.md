---
solution: Journey Optimizer
product: journey optimizer
title: Treueprogramm konfigurieren
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Prämienanbieter, Ereignisdefinitionen und Einstellungen auf Organisationsebene für Ihr Treueprogramm konfigurieren.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: a4ad533e54f3692eb0483138a8cfd1cee0e77ba1
workflow-type: tm+mt
source-wordcount: '1128'
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
>Diese Funktion befindet sich derzeit in der **privaten Betaversion**. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](../rn/releases.md).

Im **[!UICONTROL Treueprogramm-Admin]** konfigurieren Sie, wie Journey Optimizer eine Verbindung zu Ihren externen Treuesystemen herstellt. Marketer verwenden **[!UICONTROL Loyalty Challenges (Beta)]** um Herausforderungen, Aufgaben, Inhalte und Messaging zu entwerfen. **[!UICONTROL Treueprogramm-Administrator]** ist ein separater, Administratoren vorbehaltener Bereich für die Belohnungserfüllung, die Ereigniszuordnung und die Produktinventarisierung.

Wenn eine Kundin oder ein Kunde eine Challenge abschließt oder einen Prämienmeilenstein erreicht, ruft Journey Optimizer den Prämienanbieter an, den Sie für die Vergabe von Punkten oder anderen Prämien konfiguriert haben. Die Konfiguration in **[!UICONTROL Treueprogramm-]**) wirkt sich nicht auf die Einstellungen **[!UICONTROL Inhalt]**, **[!UICONTROL Messaging]** oder **[!UICONTROL Zielgruppe]** aus, die weiterhin unter der Kontrolle des Marketing-Experten stehen.

## Was Sie hier im Vergleich zu den Herausforderungen im Zusammenhang mit der Treue konfigurieren {#scope}

| Bereich | Konfiguriert in Treue-Admin | Konfiguriert in Herausforderungen bezüglich der Treue |
|------|----------------------------|----------------------------------|
| Belohnungs-Erfüllungs-API | Ja — Belohnungsanbieter | Nein — nur Dienstleister und Beträge auswählen |
| Ereignis-Mapping für benutzerdefinierte Aktivitäten | Ja - Ereignisdefinitionen | Nein - Ereignisnamen für benutzerdefinierte Ereignisaufgaben auswählen |
| Produktgruppen-Zuordnungen | Ja — Produktbestand | Nein - Benutzen Sie Gruppen beim Erstellen von Kauf-/Ausgabenaufgaben. |
| Challenge-Struktur, Inhalt, Audience | Nein | Ja |

Adobe Journey Optimizer sendet Erfüllungsaufrufe an Ihren Belohnungsanbieter, wenn Kunden Belohnungen erhalten. Die Treueplattform ist für die Gutschrift auf dem Mitgliedskonto verantwortlich.

## Voraussetzungen {#prerequisites}

**[!UICONTROL Loyalty Admin]** ist für eine geringe Anzahl von Administratoren pro Organisation vorgesehen. Zusätzlich zu den Berechtigungen, die für [Herausforderungen im Zusammenhang mit dem Treueprogramm](get-started.md#prerequisites) erforderlich sind, benötigen Sie Zugriff auf Administratorebene für Ihre Journey Optimizer-Instanz. Wenden Sie sich an Ihren Adobe-Administrator, um Zugriff anzufordern.

## Auf Treueprogramm-Administrator zugreifen {#access-loyalty-admin}

Um **[!UICONTROL Treueprogramm-Administrator]** zu öffnen, wählen Sie es über die linke Navigationsleiste in Journey Optimizer aus.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

**[!UICONTROL Treue-Administrator]** ist in Registerkarten unterteilt: **[!UICONTROL Globale Einstellungen]**, **[!UICONTROL Belohnungsanbieter]**, **[!UICONTROL Ereignisdefinitionen]** und **[!UICONTROL Produktinventar]**. Die verfügbaren Registerkarten hängen von den Berechtigungen und der Funktionskonfiguration Ihres Unternehmens ab.

## Globale Einstellungen {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Globale Einstellungen"
>abstract="Wählen Sie den Identity-Namespace von Adobe Experience Platform für Ihr Treueprogramm aus und kopieren Sie Ihre Konfigurations-ID. Diese Einstellungen auf Organisationsebene sind erforderlich, damit die Belohnungsanbieter die Belohnungen korrekt erfüllen können."

Verwenden Sie **[!UICONTROL Globale Einstellungen]** um organisationsweite Optionen für Herausforderungen im Zusammenhang mit der Treue zu konfigurieren.

1. Öffnen Sie die **[!UICONTROL Globale Einstellungen]**.

1. Wählen Sie in **[!UICONTROL Dropdown]** Namespace den [Identity-Namespace](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces) aus, der von Ihrem Treueprogramm verwendet wird.

1. Wählen Sie **[!UICONTROL Speichern]**, um den Namespace auf Ihre Konfiguration der Herausforderungen im Treueprogramm anzuwenden.

1. Kopieren Sie die **[!UICONTROL Konfigurations-ID]**, wenn Sie sie für Ihr Implementierungsteam oder externe Systeme freigeben müssen, z. B. bei der Konfiguration der Bereitstellung eingehender Ereignisse.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Belohnungsanbieter {#reward-providers}

Ein **Belohnungsanbieter** teilt Journey Optimizer mit, wohin Erfüllungsanrufe gesendet werden sollen, wenn der Challenge-Fortschritt aufgezeichnet oder eine Challenge abgeschlossen wird. Dies kann z. B. eine API sein, die einem Mitgliedskonto Treuepunkte oder Sterne gutschreibt.

Die Konfiguration eines Belohnungsanbieters umfasst:

* Grundlegende Verbindungsdetails (Name, Beschreibung, API-URL, Kopfzeilen)
* **[!UICONTROL Belohnungsdefinitionen]** - die Belohnungstypen, die dieser Anbieter ausgeben kann (z. B. Sterne oder Meilen)
* **[!UICONTROL Belohnungs-Proxys]** (optional) - Ein zwischengeschalteter Proxy, über den Aufrufe anstelle direkt an Ihren Endpunkt geleitet werden
* **[!UICONTROL Auth-Token-Generatoren]** - der Mechanismus, den Journey Optimizer verwendet, um Zugriffstoken abzurufen, bevor es Ihre API aufruft

### Belohnungsanbieter erstellen {#create-reward-provider}

1. Öffnen Sie die Registerkarte **[!UICONTROL Belohnungsanbieter]** und wählen Sie **[!UICONTROL Belohnungsanbieter erstellen]** aus.

1. Geben Sie **[!UICONTROL Name]**, **[!UICONTROL Beschreibung]** und die **[!UICONTROL API-URL]** ein, die Erfüllungsanfragen empfängt.

1. Fügen Sie **[!UICONTROL Kopfzeilen]** nach Bedarf für Ihre API hinzu (z. B. API-Schlüssel oder Inhaltstypen).

1. Konfigurieren Sie **[!UICONTROL Belohnungsdefinitionen]** - einen Eintrag pro Belohnungstyp, den Ihr Anbieter unterstützt (z. B. Programmpunkte oder Sterne). Für jede Definition gilt:

   * Geben Sie die **Payload** an, die mit Erfüllungsaufrufen gesendet werden soll.
   * Optional können Sie eine Definition als **Standard** für diesen Anbieter markieren.

1. Konfigurieren Sie optional einen **[!UICONTROL Reward-Proxy]**, um Erfüllungsaufrufe über einen Zwischen-Server zu leiten:

   * **[!UICONTROL Name]**, **[!UICONTROL Beschreibung]** und ob der Proxy **aktiviert**
   * **[!UICONTROL Host]**, **[!UICONTROL Port]** und Anmeldeinformationen

1. Konfigurieren Sie einen **[!UICONTROL Auth-Token-Generator]** wenn Ihre API ein Bearer-Token für die Authentifizierung benötigt:

   * Token-Endpunkt-URL und HTTP-Methode (z. B **„POST** für Flüsse im OAuth-Stil)
   * **[!UICONTROL Token-Schlüssel]** in der Antwort (z. B. `access_token`)
   * Für Ihren Token-Endpunkt erforderliche Kopfzeilen

   Journey Optimizer verwendet diese Konfiguration, um ein neues Token zu erhalten, bevor es Ihre Belohnungs-API aufruft.

1. Wählen Sie **[!UICONTROL Belohnungsanbieter erstellen]** aus. Der Anbieter und alle konfigurierten untergeordneten Ressourcen werden zusammen gespeichert.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Nach dem Speichern wird der Anbieter in der Liste der Belohnungsanbieter angezeigt. Marketer wählen diesen Anbieter beim [Konfigurieren von Challenge-Belohnungen](create-challenges.md#rewards).

Um einen vorhandenen Belohnungsanbieter zu bearbeiten, öffnen Sie die Registerkarte **[!UICONTROL Belohnungsanbieter]**, wählen Sie den Anbieter aus und aktualisieren Sie die Felder an Ort und Stelle. Änderungen an untergeordneten Ressourcen (Belohnungsdefinitionen, Proxys, Authentifizierungs-Token-Generatoren) werden gespeichert, wenn Sie sie aktualisieren.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>**[!UICONTROL Bringen Sie Ihre eigenen Daten mit]** Herausforderungen erfüllen Belohnungen durch Ihre eigene Datenintegration. Die hier konfigurierten Belohnungsanbieter gelten nicht für diese Herausforderungen. [Erfahren Sie mehr über die Herausforderungen, vor denen Ihre eigenen Daten stehen](create-challenges.md#create-the-challenge).

## Ereignisdefinitionen (optional) {#event-definitions}

**[!UICONTROL Ereignisdefinitionen]** Ordnen Sie Erlebnisereignisse aus Ihren Systemen - in welchem JSON- oder XDM-Format auch immer Ihre Marke verwendet - Aktivitäten zu, auf die Treueprogramm-Herausforderungen reagieren können, insbesondere **[!UICONTROL benutzerspezifische Ereignisse]**-Aufgaben. Wenn Ereignisse eintreffen, verwendet Journey Optimizer diese Definitionen, um zu entscheiden, ob sie verarbeitet werden sollen. Ereignisse, die keiner Definition entsprechen, werden ignoriert.

### Erstellen einer Ereignisdefinition {#create-event-definition}

1. Öffnen Sie die **[!UICONTROL Ereignisdefinitionen]** und erstellen Sie eine neue Definition.

1. Geben Sie einen **[!UICONTROL Namen]** für das Ereignis ein (z. B. `Coffee purchase`). Dies ist der Name, den Marketer beim Konfigurieren einer Aufgabe vom Typ **[!UICONTROL Benutzerdefiniertes Ereignis]** sehen.

1. Angeben, wie das Ereignis in eingehenden Payloads identifiziert werden soll:

   * **[!UICONTROL Kennungspfad]** - JSON-Pfad zum Feld, das das Ereignis oder Element identifiziert (z. B. `data.memberId`)
   * **[!UICONTROL Kennungswerte]** - Werte, die vorhanden sein müssen, damit diese Definition übereinstimmt

1. Geben Sie optional eine **[!UICONTROL XDM-Schema-ID]** an, wenn Ihre Ereignis-Payloads einem Experience Platform-Schema entsprechen.

1. Verwenden Sie optional die Felder **[!UICONTROL Schema]** und **[!UICONTROL Transformer]** um benutzerdefinierte Schema- und Umwandlungszeichenfolgen zum Analysieren und Überprüfen eingehender JSON-Dateien bereitzustellen.

   Je nach Strukturierung der Ereignisse können Sie eine XDM-Schema-ID, einen Kennungspfad oder beides angeben.

1. Speichern Sie die Ereignisdefinition.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

Die meisten Unternehmen erstellen mehrere Ereignisdefinitionen - eine pro Aktivität, die sie verfolgen möchten (z. B. Kauf, Check-in oder Site-Besuch). [Erfahren Sie, wie Sie in Challenges benutzerdefinierte Ereignisaufgaben verwenden](create-tasks.md#choose-activity).

## Produktbestand (optional) {#product-inventory}

Verwenden Sie die **[!UICONTROL Produktinventar]**, um eine CSV-Datei hochzuladen, die Produkt- oder Artikelkennungen (z. B. MPG-IDs) Produktgruppen zuordnet. Marketing-Experten können dann diese Gruppen in Regeln für die Aufgabeneignung referenzieren, anstatt einzelne SKUs einzugeben.

1. Öffnen Sie die Registerkarte **[!UICONTROL Produktinventar]**.

1. Laden Sie Ihre Zuordnungsdatei hoch.

1. Überprüfen Sie die importierten Zuordnungen in der Inventarliste. Wählen Sie eine Produktgruppe aus, um alle Elemente in dieser Gruppe anzuzeigen, oder verwenden Sie die Suche, um Elemente nach Namen oder ID zu suchen.

1. Verwenden Sie **[!UICONTROL Upload-Verlauf]**, um frühere Uploads anzuzeigen.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Globale Ausschlüsse]** für den Produktbestand ist für eine zukünftige Version geplant und wird hier nicht dokumentiert.
