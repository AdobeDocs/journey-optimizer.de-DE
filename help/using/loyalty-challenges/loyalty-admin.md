---
solution: Journey Optimizer
product: journey optimizer
title: Treueprogramm konfigurieren
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Prämienanbieter, Ereignisdefinitionen und Organisationseinstellungen für Ihr Treueprogramm konfigurieren.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: aea783bd8f2351d4a5d8aa6b84c24a713a6c0306
workflow-type: tm+mt
source-wordcount: '1221'
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

Im **[!UICONTROL Treueprogramm-]**) konfigurieren Sie, wie Journey Optimizer eine Verbindung zu Ihrem Treueprogramm-Backend herstellt. Marketing-Experten verwenden **[!UICONTROL Loyalty Challenges (Beta]**, um Herausforderungen, Aufgaben, Inhalte und Messaging zu entwerfen. „Loyalty Admin“ ist eine separate, einmalige Einrichtung für die Belohnungserfüllung und die Ereigniszuordnung.

Wenn ein Kunde eine Challenge abschließt (oder einen Prämienmeilenstein erreicht), ruft Journey Optimizer den hier konfigurierten Prämienanbieter auf, um Punkte oder andere Prämien zu erhalten. Die Einstellungen **[!UICONTROL Herausforderung]** Inhalt **[!UICONTROL Nachrichten]** und **[!UICONTROL Zielgruppe]** sind von der Konfiguration der Treueprogramm-Admins nicht betroffen.

## Auf Treueprogramm-Administrator zugreifen {#access-loyalty-admin}

Um Loyalty Admin zu öffnen, melden Sie sich bei Journey Optimizer an und wählen Sie **[!UICONTROL Loyalty Admin]** im linken Navigationsbereich aus.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

Die Admin-Benutzeroberfläche ist in Registerkarten unterteilt. Je nach Unternehmen werden möglicherweise **[!UICONTROL Globale Einstellungen]**, **[!UICONTROL Belohnungsanbieter]**, **[!UICONTROL Ereignisdefinitionen]** und **[!UICONTROL Produktinventar]**.

## Globale Einstellungen {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Globale Einstellungen"
>abstract="Wählen Sie den Identity-Namespace von Adobe Experience Platform für Ihr Treueprogramm aus und kopieren Sie Ihre Konfigurations-ID. Diese Einstellungen auf Organisationsebene sind erforderlich, damit die Belohnungsanbieter die Belohnungen korrekt erfüllen können."

Verwenden Sie **[!UICONTROL Globale Einstellungen]** um organisationsweite Optionen für Herausforderungen im Zusammenhang mit der Treue zu konfigurieren.

1. Öffnen Sie die **[!UICONTROL Globale Einstellungen]**.

1. Wählen Sie in **[!UICONTROL Dropdown]** Namespace den [Identity-Namespace](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces) aus Adobe Experience Platform aus, den Ihr Treueprogramm verwendet. Wählen Sie **[!UICONTROL Speichern]**, um den Namespace in der Konfiguration der Herausforderungen im Zusammenhang mit dem Treueprogramm Ihres Unternehmens zu aktualisieren.

1. Kopieren Sie die **[!UICONTROL Konfigurations-ID]**, wenn Sie sie für Ihr Implementierungsteam oder externe Systeme freigeben müssen.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Belohnungsanbieter {#reward-providers}

Ein **Belohnungsanbieter** teilt Journey Optimizer mit, wohin Erfüllungsanrufe gesendet werden sollen, wenn der Challenge-Fortschritt aufgezeichnet oder eine Challenge abgeschlossen wird. Dies kann z. B. eine API sein, die einem Mitgliedskonto Treuepunkte oder Sterne gutschreibt.

Ein Belohnungsanbieter umfasst:

* Grundlegende Verbindungsdetails (Name, Beschreibung, API-URL, Kopfzeilen)
* **[!UICONTROL Belohnungsdefinitionen]** — Belohnungstypen, die dieser Anbieter ausgeben kann (z. B. Sterne oder Meilen)
* **[!UICONTROL Belohnungs-Proxys]** (optional) - Routet Aufrufe über einen Proxy anstatt direkt an Ihren Endpunkt.
* **[!UICONTROL Auth-Token-Generatoren]** - So ruft Journey Optimizer Zugriffstoken ab, bevor es Ihre API aufruft

### Belohnungsanbieter erstellen {#create-reward-provider}

Führen Sie diese Schritte aus, um einen neuen Belohnungsanbieter und die zugehörigen Ressourcen zu registrieren.

1. Öffnen Sie die Registerkarte **[!UICONTROL Belohnungsanbieter]** und erstellen Sie einen Anbieter.

1. Geben Sie **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** gefolgt von der **[!UICONTROL API-]** ein, an die Erfüllungsanfragen gesendet werden.

1. Fügen Sie **[!UICONTROL Kopfzeilen]** nach Bedarf für Ihre API hinzu (z. B. API-Schlüssel oder Inhaltstypen). Sie können Kopfzeilen in der Benutzeroberfläche hinzufügen oder entfernen.

1. Konfigurieren Sie **[!UICONTROL Belohnungsdefinitionen]**:

   * Definieren Sie jeden Belohnungstyp, den Ihr Anbieter unterstützt (z. B. Programmpunkte oder Sterne).
   * Optional können Sie eine Definition als **Standard** für diesen Anbieter markieren.
   * Geben Sie für jede Definition **Payload** an, die mit Erfüllungsaufrufen gesendet werden soll.

1. Konfigurieren Sie optional einen **[!UICONTROL Reward-Proxy]**:

   * **[!UICONTROL Host]**, **[!UICONTROL Port]** und Anmeldeinformationen
   * **[!UICONTROL Name]**, **[!UICONTROL Beschreibung]** und ob der Proxy **aktiviert**

1. Konfigurieren Sie einen **[!UICONTROL Auth-Token-Generator]** wenn Ihre API vor jedem Aufruf ein Token benötigt:

   * Token-Endpunkt-URL und HTTP-Methode (z. B **„POST** für Flüsse im OAuth-Stil)
   * **[!UICONTROL Token-Schlüssel]** in der Antwort (z. B. `access_token`)
   * Für Ihren Token-Endpunkt erforderliche Kopfzeilen

   Journey Optimizer fordert ein Token von dieser Konfiguration an, bevor es Ihre Reward-API aufruft, sodass Aufrufe eine aktuelle Berechtigung verwenden.

1. Wählen Sie **[!UICONTROL Belohnungsanbieter erstellen]** aus. Der Anbieter und seine untergeordneten Ressourcen (Definitionen, Proxy und Token-Generator) werden gemeinsam erstellt.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Nach der Erstellung wird der Anbieter in der Liste der Belohnungsanbieter angezeigt. Marketer wählen diesen Anbieter beim [Konfigurieren von Challenge-Belohnungen](create-challenges.md#rewards).

### Belohnungsanbieter bearbeiten {#edit-reward-provider}

1. Öffnen Sie die Registerkarte **[!UICONTROL Belohnungsanbieter]** und wählen Sie einen Anbieter aus.

1. Aktualisieren Sie den Namen, die Beschreibung, die URL oder die Kopfzeilen des Anbieters nach Bedarf.

1. Um **[!UICONTROL Belohnungsdefinitionen]**, **[!UICONTROL Belohnungs-Proxys]** oder **[!UICONTROL Auth-Token-Generatoren) zu ändern,]** Sie den entsprechenden Abschnitt und bearbeiten Sie die Felder. Änderungen an diesen untergeordneten Ressourcen werden gespeichert, wenn Sie sie im Kontext aktualisieren.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>Bei Herausforderungen **[!UICONTROL Eigene Daten einbringen]** bei denen Aufgaben und Belohnungen vollständig von Ihrer Datenintegration stammen, können die hier konfigurierten Belohnungsanbieter möglicherweise keine Anwendung finden. [Erfahren Sie mehr über die Herausforderungen, vor denen Ihre eigenen Daten stehen](create-challenges.md#create-the-challenge).

## Ereignisdefinitionen {#event-definitions}

**[!UICONTROL Ereignisdefinitionen]** Ordnen Sie eingehende Erlebnisereignisse im Format Ihrer Marke Aktivitäten zu, die Challenges im Rahmen des Treueprogramms verwenden können, insbesondere **[!UICONTROL benutzerspezifische Ereignisse]**-Aufgaben. Wenn Daten von Ihren Kanälen eingehen, verwendet Journey Optimizer diese Definitionen, um zu entscheiden, ob ein Ereignis relevant ist und wie es interpretiert werden soll. Ereignisse, die keiner Definition entsprechen, werden ignoriert.

### Erstellen einer Ereignisdefinition {#create-event-definition}

1. Öffnen Sie die **[!UICONTROL Ereignisdefinitionen]** und erstellen Sie eine neue Definition.

1. Geben Sie einen **[!UICONTROL Namen]** für das Ereignis ein (z. B. `Coffee purchase`). Marketing-Experten wählen diesen Namen, wenn sie eine Aufgabe **[!UICONTROL Benutzerspezifisches Ereignis]** konfigurieren.

1. Angeben, wie das Ereignis in eingehenden Payloads identifiziert werden soll:

   * **[!UICONTROL Kennungspfad]** - JSON-Pfad zum Feld, das das Ereignis oder Element identifiziert (z. B. `data.memberId`)
   * **[!UICONTROL Kennungswerte]** - Werte, die vorhanden sein müssen, damit diese Definition übereinstimmt

1. Geben Sie optional eine **[!UICONTROL XDM-Schema-ID]** an und/oder verwenden Sie die Felder **[!UICONTROL Schema]** und **[!UICONTROL Transformer]** zum Einfügen von Schema- und Transformationszeichenfolgen, die Ihr Team verwendet, um eingehende JSON-Dateien vor der Verarbeitung zu analysieren und zu validieren.

   Je nach Strukturierung der Ereignisse können Sie eine XDM-Schema-ID, einen Kennungspfad oder beides angeben.

1. Speichern Sie die Ereignisdefinition.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

Die meisten Unternehmen erstellen mehrere Ereignisdefinitionen - eine pro Aktivität, die sie verfolgen möchten (z. B. Kauf, Check-in oder Site-Besuch). [Erfahren Sie, wie Sie in Challenges benutzerdefinierte Ereignisaufgaben verwenden](create-tasks.md#choose-activity).

## Produktinventar {#product-inventory}

Auf **[!UICONTROL Registerkarte]** Produktinventar“ können Sie eine CSV-Datei hochladen, um Produkt- oder Elementkennungen (z. B. MPG-IDs) Produktgruppen zuzuordnen, die in der Aufgabeneignung verwendet werden. Dies unterstützt Szenarien, in denen Aufgaben auf gruppierte Produkte anstatt auf einzelne manuell eingegebene SKUs verweisen.

1. Öffnen Sie die Registerkarte **[!UICONTROL Produktinventar]**.

1. Laden Sie Ihre Zuordnungsdatei hoch, indem Sie sie in den Upload-Bereich ziehen oder zur Auswahl navigieren.

1. Überprüfen Sie die importierten Zuordnungen in der Inventarliste. Wählen Sie eine Produktgruppe aus, um alle Elemente in dieser Gruppe anzuzeigen. Verwenden Sie die Suche, um Elemente nach Namen oder ID zu suchen.

1. Verwenden Sie **[!UICONTROL Upload-Verlauf]**, um frühere Uploads anzuzeigen.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Globale Ausschlüsse]** für den Produktbestand ist für eine zukünftige Version geplant und wird hier nicht dokumentiert.

## Zusammenhang zwischen Treue-Administrator und Herausforderungen {#how-admin-relates-to-challenges}

| Bereich | Konfiguriert in Treue-Admin | Konfiguriert in Herausforderungen bezüglich der Treue |
|------|----------------------------|----------------------------------|
| Belohnungs-Erfüllungs-API | Ja — Belohnungsanbieter | Nein — nur Dienstleister und Beträge auswählen |
| Ereignis-Mapping für benutzerdefinierte Aktivitäten | Ja - Ereignisdefinitionen | Nein - Ereignisnamen für benutzerdefinierte Ereignisaufgaben auswählen |
| Produktgruppen-Zuordnungen | Ja — Produktbestand | Nein - Benutzen Sie Gruppen beim Erstellen von Kauf-/Ausgabenaufgaben. |
| Challenge-Struktur, Inhalt, Audience | Nein | Ja |

Typische Setup-Reihenfolge:

1. Konfigurieren Sie **[!UICONTROL Globale Einstellungen]** und mindestens einen **[!UICONTROL Belohnungsanbieter]** in Treueprogramm-Admin.
1. Fügen Sie optional **[!UICONTROL Ereignisdefinitionen]** und **[!UICONTROL Produktinventar“ hinzu]** wenn Ihr Programm benutzerdefinierte Ereignisse oder CSV-basierte Produktgruppen verwendet.
1. Erstellen Sie [Aufgaben](create-tasks.md) und [Herausforderungen](create-challenges.md) in **[!UICONTROL Treueprogramm-Herausforderungen (Beta)]**, indem Sie den Prämienanbieter und die von Ihnen konfigurierten Definitionen auswählen.

Adobe Journey Optimizer sendet Erfüllungsaufrufe an Ihren Provider, wenn Kunden Prämien verdienen. Ihre Treueplattform ist für die Gutschrift auf dem Mitgliedskonto verantwortlich.

## Voraussetzungen {#prerequisites}

Loyalty Admin richtet sich an eine kleine Gruppe von Administratoren in Ihrem Unternehmen. Zusätzlich zu den Berechtigungen, die für „Herausforderungen im Zusammenhang mit [Treue](get-started.md#prerequisites) erforderlich sind, benötigen Sie Zugriff, um Treueeinstellungen auf Organisationsebene zu konfigurieren.

Wenden Sie sich an Ihren Administrator **[!UICONTROL wenn]** Treueprogramm-Administrator“ nicht im linken Navigationsbereich angezeigt wird oder Sie keine globalen Einstellungen oder Belohnungsanbieter speichern können.
