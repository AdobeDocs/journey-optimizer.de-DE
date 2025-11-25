---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen zu Journeys
description: Häufig gestellte Fragen zu Journeys in Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: Journey, Fragen, Antworten, Fehlerbehebung, Hilfe, Anleitung
version: Journey Orchestration
source-git-commit: dff732d14dd143f085b1287274f7571a900a0c87
workflow-type: tm+mt
source-wordcount: '5226'
ht-degree: 95%

---


# Häufig gestellte Fragen {#faq-journeys}

Im Folgenden finden Sie häufig gestellte Fragen zu Journeys in Adobe Journey Optimizer.

Sie würden gerne mehr erfahren? Verwenden Sie die Feedback-Optionen unten auf dieser Seite, um Ihre Frage zu stellen, oder vernetzen Sie sich mit der [Adobe Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}.

## Allgemeine Konzepte

+++ Was ist eine Journey in Adobe Journey Optimizer?

Eine Journey ist eine mehrstufige Orchestrierung, mit der Sie Echtzeit-Kundenerlebnisse kanalübergreifend entwerfen und ausführen können. Journeys kombinieren Ereignisse, Orchestrierungsaktivitäten, Aktionen und Nachrichten, um basierend auf Kundenverhalten und Geschäftsereignissen personalisierte, kontextuelle Erlebnisse zu schaffen.

Erfahren Sie mehr über [Journeys](journey.md).

+++

+++ Welche verschiedenen Journey-Typen gibt es?

Adobe Journey Optimizer unterstützt vier Journey-Typen:

* **Unitäre Journeys**: Werden einzeln durch ein Ereignis ausgelöst (z. B. Kauf, App-Anmeldung). Die Profile treten jeweils zu dem Zeitpunkt in die Journey ein, zu dem das Ereignis stattfindet.
* **Journeys des Typs „Zielgruppe lesen“**: Beginnen Sie mit einer Zielgruppe aus Adobe Experience Platform und senden Sie Nachrichten im Batch an alle Profile in dieser Zielgruppe.
* **Journeys des Typs „Zielgruppenqualifizierung“**: Werden ausgelöst, wenn Profile sich für ein bestimmtes Zielgruppensegment qualifizieren (oder daraus aussteigen). Profile treten in die Journey ein, wenn sie die Zielgruppenkriterien erfüllen.
* **Geschäftsereignis-Journeys**: Werden durch Geschäftsereignisse ausgelöst (z. B. Bestandsaktualisierungen, Wetterwarnungen), die mehrere Profile gleichzeitig betreffen.

Erfahren Sie mehr über [Journey-Typen](entry-management.md#types-of-journeys).

+++

+++ Was ist der Unterschied zwischen einer Journey und einer Kampagne?

**[Journeys](journey.md)** sind mehrstufige Orchestrierungen, die auf Ereignisse oder Zielgruppen reagieren und über den gesamten Kundenzyklus hinweg eine komplexe Logik, Bedingungen, Wartezeiten und mehrere Touchpoints ermöglichen.

Es gibt drei Typen von **[Kampagnen](../campaigns/get-started-with-campaigns.md)**:

* **[Aktionskampagnen](../campaigns/create-campaign.md)**: Einmalige oder wiederkehrende Nachrichten, die an eine bestimmte Zielgruppe gesendet werden. Sie eignen sich ideal für eigenständige Nachrichten wie Werbeanzeigen oder Newsletter.
* **[Durch API ausgelöste Kampagnen](../campaigns/api-triggered-campaigns.md)**: Durch API-Aufrufe ausgelöste Kampagnen, die die Integration mit externen Systemen ermöglichen, um Nachrichten basierend auf Echtzeit-Ereignissen oder Geschäftslogik zu senden.
* **[Orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)**: Mehrstufige, zielgruppenbasierte Kampagnen auf einer Arbeitsfläche, die Bedingungen, Wartezeiten und mehrere Aktionen zur Erstellung geplanter, koordinierter Erlebnisse enthalten können.

**Best Practice**: Verwenden Sie [Journeys](journey.md) für komplexe, ereignisgesteuerte Interaktionen mit erweiterter Orchestrierung, [Aktionskampagnen](../campaigns/create-campaign.md) für geplante, zielgruppenbasierte Kommunikation, [durch API ausgelöste Kampagnen](../campaigns/api-triggered-campaigns.md) für die programmgesteuerte Auslösung aus externen Systemen und [orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) für mehrstufige Kommunikation mit kampagnenspezifischen Anforderungen.

+++

+++ Was sind die Hauptkomponenten einer Journey?

Eine Journey besteht aus:

* **Ereignissen**: Eintrittspunkte, die die Journey auslösen (z. B. Profilqualifizierung, Geschäftsereignisse)
* **Orchestrierungsaktivitäten**: Logikkomponenten wie Bedingungen, Wartezeiten, Lesen der Zielgruppe und Beenden
* **Aktionen**: Aktivitäten, die Aufgaben ausführen, z. B. Senden von Nachrichten, Aktualisieren von Profilen oder Aufrufen externer APIs
* **Native Kanalaktionen**: Native Messaging-Funktionen für E-Mail, SMS, Push und andere Kanäle
* **Benutzerdefinierte Aktionen**: Integration mit Drittanbietersystemen

Erfahren Sie mehr über [Journey-Aktivitäten](about-journey-activities.md).

+++

+++ Welche Zielgruppentypen werden in Journeys unterstützt und welche Einschränkungen gelten für sie?

Adobe Journey Optimizer unterstützt vier Arten von Zielgruppen mit jeweils unterschiedlichen Eigenschaften und Leitlinien:

**1. Streaming-Zielgruppen**

* **Beschreibung**: Zielgruppen, die in Echtzeit ausgewertet werden, wenn sich die Profildaten ändern
* **Auswertung**: Kontinuierliche Auswertung, wenn Profilattribute oder Ereignisse den Segmentkriterien entsprechen
* **Journey-Nutzung**: Bei Aktivitäten vom Typ „Zielgruppe lesen“, „Zielgruppenqualifizierung“ und „Bedingung“ unterstützt
* **Am besten geeignet für**: Echtzeit-Interaktion basierend auf Verhaltensänderungen oder Profilaktualisierungen
* **Leitlinien**:
   * Die maximale Zielgruppengröße hängt von Ihrer Journey Optimizer-Lizenz ab
   * Auswertungslatenz normalerweise unter 5 Minuten
   * Komplexe Segmentlogik kann die Auswertungsleistung beeinträchtigen

**2. Batch-Zielgruppen**

* **Beschreibung**: Zielgruppen, die auf geplanter Basis ausgewertet werden (normalerweise täglich)
* **Auswertung**: In geplanten Intervallen in Batch-Aufträgen verarbeitet
* **Journey-Nutzung**: Bei Aktivitäten vom Typ „Zielgruppe lesen“ und „Bedingung“ unterstützt; eingeschränkte Unterstützung bei Journeys von Typ „Zielgruppenqualifizierung“
* **Am besten geeignet für**: Regelmäßige Kampagnen, Newsletter, geplante Kommunikation
* **Leitlinien**:
   * Die Auswertung erfolgt einmal täglich (Standard) oder nach einem konfigurierten Zeitplan
   * Profile spiegeln möglicherweise erst bei der nächsten Auswertung Echtzeitänderungen wider
   * Die Aktivität „Zielgruppe lesen“ kann große Batch-Zielgruppen effizient verarbeiten

**3. Upload-Zielgruppen (benutzerdefinierter Upload)**

* **Beschreibung**: Zielgruppen, die durch Hochladen von CSV-Dateien mit Profilkennungen erstellt werden
* **Evaluierung**: Statische Liste wird nur aktualisiert, wenn neue Dateien hochgeladen werden
* **Journey-Nutzung**: Bei Aktivitäten vom Typ „Zielgruppe lesen“ und „Bedingung“ unterstützt; **nicht unterstützt** in Journeys vom Typ „Zielgruppenqualifizierung“
* **Am besten geeignet für**: Einmalige Kampagnen, Importe externer Listen, zielgerichtete Kommunikation
* **Leitlinien**:
   * Es gelten CSV-Dateigrößenbeschränkungen (in der Produktdokumentation finden Sie die aktuellen Limits)
   * Zielgruppenmitglieder sind statisch, bis sie mit neuem Upload aktualisiert werden
   * Identity-Namespace muss mit Journey-Namespace übereinstimmen
   * Profile müssen in Adobe Experience Platform vorhanden sein

**4. Zielgruppen für die Komposition föderierter Zielgruppen (Federated Audience Composition, FAC)**

* **Beschreibung**: Zielgruppen, die mit föderierten Daten erstellt wurden, sodass Sie Zielgruppen aus externen Data Warehouses abfragen und erstellen können, ohne Daten in Adobe Experience Platform kopieren zu müssen
* **Auswertung**: Statische Komposition wird aktualisiert, wenn die Komposition föderierter Zielgruppen ausgeführt wird
* **Journey-Nutzung**: Bei Aktivitäten vom Typ „Zielgruppe lesen“ und „Bedingung“ unterstützt; **nicht unterstützt** in Journeys vom Typ „Zielgruppenqualifizierung“ (ähnlich wie bei Upload-Zielgruppen aus einer Backend-Perspektive)
* **Am besten geeignet für**: Data Warehouse-Integration für Unternehmen, Zielgruppenkomposition unter Verwendung externer Datenquellen, Szenarien, in denen Daten in externen Systemen verbleiben müssen
* **Leitlinien**:
   * Zielgruppenmitglieder sind bis zur nächsten Ausführung der föderierten Komposition statisch
   * Identity-Namespace muss mit Journey-Namespace übereinstimmen
   * Die Leistung hängt von den Abfragefunktionen des externen Data Warehouse ab
   * Erfordert das Add-on „Komposition föderierter Zielgruppen“

**CJA-Zielgruppen (Customer Journey Analytics)**:

Obwohl CJA-Zielgruppen in Journeys nicht direkt unterstützt werden, können Sie das Problem **umgehen**, indem Sie eine CJA-Zielgruppe in eine Segmentierungsregel „einschließen“. Dadurch wird eine Batch-UPS-Zielgruppe (Unified Profile Service) erstellt, die auf die CJA-Zielgruppe verweist und sie für die Verwendung in Journeys als Batch-Zielgruppentyp verfügbar macht.

**Journey-spezifische Überlegungen**:

* **Journeys vom Typ „Zielgruppe lesen“**: Alle vier Zielgruppentypen werden unterstützt; der Batch-Export erfolgt bei den Ausführungen der Journeys
* **Journeys vom Typ „Zielgruppenqualifizierung“**: Streaming-Zielgruppen empfohlen; Batch-Zielgruppen haben eine verzögerte Qualifizierungserkennung; Upload- und FAC-Zielgruppen werden nicht unterstützt
* **Aktivitäten vom Typ „Bedingung“**: Alle Zielgruppentypen können zur Überprüfung der Zugehörigkeit verwendet werden
* **Namespace-Ausrichtung**: Der Identity-Namespace der Zielgruppe muss mit dem Namespace der Journey übereinstimmen, damit die Profile ordnungsgemäß identifiziert werden können

**Best Practices**:

* Verwenden Sie **Streaming-Zielgruppen** für in Echtzeit ereignisgesteuerte Journeys, die eine sofortige Reaktion erfordern
* Verwenden Sie **Batch-Zielgruppen** für geplante Kommunikationen, bei denen eine tägliche Auswertung ausreicht
* Verwenden Sie **Upload-Zielgruppen** für zielgerichtete einmalige Kampagnen mit externen Listen
* Verwenden Sie **FAC-Zielgruppen**, wenn Sie Enterprise Data Warehouse-Funktionen ohne Datenduplizierung nutzen müssen
* Überwachen der Zielgruppengröße und der Auswertungsleistung in umfangreichen Bereitstellungen
* Berücksichtigen Sie beim Festlegen des Journey-TImings und der Einstiegsbedingungen die Aktualisierungsraten der Zielgruppe

Erfahren Sie mehr über [Zielgruppen](../audience/about-audiences.md), [das Erstellen von Segmenten](../audience/creating-a-segment-definition.md), [benutzerdefinierte Upload-Zielgruppen](../audience/custom-upload.md) und [die Komposition föderierter Zielgruppen](../audience/federated-audience-composition.md).

+++

+++ Wie wähle ich zwischen einer unitären Journey und einer Journey des Typs „Zielgruppe lesen“ aus?

Verwendung **unitärer Journeys**:

* Sie müssen in Echtzeit auf individuelle Kundenaktionen reagieren (z. B. Kaufbestätigung, Warenkorbabbruch)
* Jede Kundin bzw. jeder Kunde sollte in ihrem bzw. seinem eigenen Tempo fortschreiten
* Sie möchten basierend auf bestimmten Ereignissen auslösen

Verwendung von **Journeys des Typs „Zielgruppe lesen“**:

* Sie senden Batch-Nachrichten an eine Gruppe (z. B. monatlicher Newsletter, Werbekampagnen)
* Alle Kundinnen und Kunden sollten die Nachricht etwa zur selben Zeit erhalten
* Beim Ziel handelt es sich um ein vordefiniertes Zielgruppensegment

+++

## Erstellen von Journeys

+++ Wie erstelle ich meine erste Journey?

Führen Sie folgende wichtige Schritte aus:

1. **Einrichten der Voraussetzungen**: Konfigurieren Sie Ereignisse, Datenquellen und Aktionen nach Bedarf
2. **Erstellen der Journey**: Navigieren Sie zum Menü „Journeys“ und klicken Sie auf „Journey erstellen“
3. **Definieren der Journey-Eigenschaften**: Legen Sie den Journey-Namen, die Beschreibung und andere Einstellungen fest
4. **Entwerfen der Journey**: Ziehen Sie Aktivitäten per Drag-and-Drop aus der Palette in die Arbeitsfläche
5. **Testen der Journey**: Verwenden Sie den Testmodus zur Validierung der Journey-Logik
6. **Probelauf der Journey**: Verwenden Sie den Probelauf, um die Journey mit echten Produktionsdaten zu testen, ohne echte Kundinnen und Kunden zu kontaktieren oder Profilinformationen zu aktualisieren
7. **Veröffentlichen der Journey**: Aktivieren Sie die Journey, um sie live zu schalten

Befolgen Sie die [detaillierte Anleitung](journey-gs.md).

+++

+++ Welche Voraussetzungen müssen erfüllt sein, damit eine Journey erstellt werden kann?

Die Voraussetzungen hängen von Ihrem Journey-Typ ab:

* **Durch Ereignis ausgelöste Journeys**: Konfigurieren Sie Ereignisse, um zu definieren, wann Profile in die Journey eintreten sollen
* **Zielgruppenbasierte Journeys**: Erstellen Sie Zielgruppen in Adobe Experience Platform
* **Datenanreicherung**: Richten Sie Datenquellen ein, um zusätzliche Informationen abzurufen
* **Integrationen von Drittanbietern**: Konfigurieren Sie benutzerdefinierte Aktionen bei Verwendung externer Systeme

Erfahren Sie mehr über die [Journey-Konfiguration](../configuration/about-data-sources-events-actions.md).

+++

+++ Kann ich in meiner Journey Daten von externen Systemen verwenden?

Ja, es gibt mehrere Ansätze zur Nutzung externer Daten:

**Best Practices**:

* **Benutzerdefinierte Aktionen**: Rufen Sie externe APIs über benutzerdefinierte Aktionen auf, um Daten abzurufen oder an Drittanbietersysteme zu senden. Dies ist der empfohlene Ansatz für Echtzeit-Interaktionen mit externen Systemen.
* **Datensatzsuche**: Wenn Sie Daten aus externen Systemen in Adobe Experience Platform laden können, verwenden Sie die Datensatzsuchfunktion, um in Experience Platform-Datensätzen gespeicherte Informationen abzurufen.
* **Externe Datenquellen**: Konfigurieren Sie externe Datenquellen, um Informationen aus API-Services von Drittanbietern abzurufen (weniger empfohlen als die oben genannten Ansätze).

Mit diesen Optionen können Sie das Kundenerlebnis mit Daten aus CRM, Treuesystemen, Wetterdiensten oder anderen externen Plattformen anreichern.

Erfahren Sie mehr über [benutzerdefinierte Aktionen](using-custom-actions.md) und [Datensatzsuche](dataset-lookup.md).

+++

+++ Wie füge ich meiner Journey Bedingungen hinzu?

Sie können Bedingungen mithilfe der **Bedingungsaktivität** aus der Orchestrierungspalette hinzufügen. Bedingungen ermöglichen Folgendes:

* Erstellen einfacher oder erweiterter Bedingungen mithilfe des Ausdruckseditors
* Aufspalten der Journey in mehrere Pfade basierend auf Profilattributen, Zielgruppenzugehörigkeit, Ereignissen oder kontextuellen Daten
* Definieren von Timeout-Pfaden für Profile, die die Bedingung nicht innerhalb einer bestimmten Zeit erfüllen

Erfahren Sie mehr über [Bedingungen](condition-activity.md).

+++

+++ Kann ich Nachrichten an Profile in einer Journey senden?

Ja. Es gibt **integrierte Kanalaktionen** in Journey Optimizer, mit denen Sie Nachrichten per E-Mail, Push-Benachrichtigungen, SMS/MMS/RCS, In-App-Nachrichten, Web-Erlebnisse, Code-basierte Erlebnisse, Direkt-Mail, Inhaltskarten, WhatsApp und LINE senden können. Sie können Nachrichteninhalte direkt in Journey Optimizer entwerfen und als Aktionsaktivitäten in Ihrer Journey hinzufügen.

Bei Kanälen, die nativ nicht unterstützt werden, können Sie **benutzerdefinierte Aktionen** verwenden, um sie in externe Messaging-Plattformen zu integrieren und Nachrichten über einen beliebigen Drittanbieterkanal zu senden.

Erfahren Sie mehr über [Nachrichten in Journeys](journeys-message.md) und [benutzerdefinierte Aktionen](using-custom-actions.md).

+++

+++ Wie warte ich auf eine bestimmte Zeit oder ein bestimmtes Ereignis in einer Journey?

Verwenden Sie die **Warteaktivität**, um die Journey für eine bestimmte Dauer oder bis zu einem bestimmten Datum/zu einer bestimmten Uhrzeit anzuhalten. Warteaktivitäten sind nützlich für:

* Senden von Folgenachrichten nach einer Verzögerung (z. B. 3 Tage nach dem Kauf)
* Erstellen von graduellen Kampagnen mit Zeitintervallen
* Kombinieren mit Bedingungen zum Erstellen von Timeout-Szenarien

Erfahren Sie mehr über [Warteaktivitäten](wait-activity.md).

+++

+++ Kann ich Profilinformationen in einer Journey aktualisieren?

Ja. Verwenden Sie die Aktivität **Profil aktualisieren**, um Profilattribute in Adobe Experience Platform auf der Grundlage von Journey-Ereignissen oder -Bedingungen zu ändern. Dies ist nützlich für das Aktualisieren von Treuepunkten, das Aufzeichnen von Journey-Meilensteinen, das Ändern von Voreinstellungen oder das Verfolgen von Kundeninteraktionswerten.

Erfahren Sie mehr über [Profilaktualisierungen](update-profiles.md).

+++

+++ Wie sende ich eine E-Mail, sobald jemand einen Kauf tätigt?

Erstellen Sie eine **unitäre, durch ein Ereignis ausgelöste Journey**:

1. Konfigurieren Sie ein Ereignis des Typs „Kauf“ mit den Bestelldetails.
2. Fügen Sie das Ereignis als Eintrittspunkt für Ihre Journey hinzu.
3. Legen Sie für sofort danach eine E-Mail-Aktion fest.
4. Gestalten Sie Ihre Bestellbestätigungs-E-Mail mit personalisierten Bestelldetails.
5. Veröffentlichen Sie die Journey.

Die Journey wird bei Erhalt eines Kaufereignisses automatisch ausgelöst und die Bestätigungs-E-Mail wird in Echtzeit gesendet.

Erfahren Sie mehr über [Ereigniskonfiguration](../event/about-events.md) und [E-Mail-Aktionen](journeys-message.md).

+++

+++ Kann ich eine Nachricht erneut senden, wenn jemand sie nicht öffnet oder nicht darauf klickt?

Ja. Verwenden **[!UICONTROL „Reaktion]**-Ereignisses mit einer **Zeitüberschreitung**:

1. Fügen Sie nach dem Versand Ihrer Nachricht ein **[!UICONTROL Reaktion]**-Ereignis **sofort** nach der Kanalaktion hinzu (ohne **[!UICONTROL Warte]**-Aktivität dazwischen)
2. Konfigurieren Sie einen Timeout-Zeitraum (z. B. 3 Tage) für das Ereignis **[!UICONTROL Reaktion]** zum Überwachen von E-Mail-Öffnungen oder -Klicks
3. Erstellen Sie zwei Pfade:
   * **Bei Öffnung/Klick**: Weiter mit den nächsten Schritten oder Beenden der Journey
   * **Timeout-Pfad (keine Öffnung/Klick)**: Versand einer Erinnerungs-E-Mail mit anderer Betreffzeile

**Best Practice**: Begrenzen Sie die Anzahl der erneuten Sendungen, um das Auftreten von Spam zu vermeiden (in der Regel maximal 1–2 Erinnerungen).

Weitere Informationen zu [Reaktionsereignissen](reaction-events.md).

+++

+++ Wie erstelle ich eine Warenkorbabbruch-Journey?

Erstellen Sie eine ereignisausgelöste Journey mit einem **[!UICONTROL Reaktion]**-Ereignis mit einer Zeitüberschreitung:

1. **Konfigurieren eines Ereignisses des Typs „Warenkorbabbruch“**: Wird ausgelöst, wenn Artikel hinzugefügt werden, der Checkout jedoch nicht innerhalb eines bestimmten Zeitraums abgeschlossen wird
2. **Erste Nachricht senden** (optional): E-Mail zur Bestätigung von Artikeln im Warenkorb
3. **Ereignis [!UICONTROL Reaktion] unmittelbar nach der Kanalaktion hinzufügen**: Konfigurieren Sie es so, dass es auf ein Kaufereignis wartet
4. **Zeitüberschreitungszeitraum festlegen**: Definieren Sie eine Zeitüberschreitung (z. B. 1-2 Stunden) für das Ereignis **[!UICONTROL Reaktion]**, um dem Kunden Zeit für einen natürlichen Abschluss zu geben
5. **Erstellen Sie zwei Pfade**:
   * **Wenn ein Kaufereignis eintritt**: Beenden der Journey oder weiter mit dem Ablauf nach dem Kauf
   * **Timeout-Pfad (kein Kauf)**: Senden einer E-Mail mit Erinnerung an Abbruch mit Warenkorbinhalten
6. **Optional**: Fügen Sie ein weiteres **[!UICONTROL Reaktion]**-Ereignis **unmittelbar nach** der Erinnerungs-E-Mail mit Zeitüberschreitung (24 Stunden) hinzu und senden Sie eine zweite Erinnerung mit einem Anreiz (z. B. 10 % Rabatt)

>[!IMPORTANT]
>
>**[!UICONTROL Reaktion]** Ereignisse müssen sofort nach „Kanalaktionen[ platziert ](journeys-message.md). Platzieren Sie keine **[!UICONTROL Warten]**-Aktivitäten zwischen der Kanalaktion und der **[!UICONTROL Reaktion]**-Aktivität.

Erfahren Sie mehr über [Journey-Anwendungsfälle](jo-use-cases.md) und [Reaktionsereignisse](reaction-events.md).

+++

+++ Wie spalte ich Kundinnen und Kunden je nach Kaufverlauf in verschiedene Pfade auf?

Verwenden Sie eine **Bedingungsaktivität** mit Zielgruppenzugehörigkeit oder Profilattributen:

1. Fügen Sie der Journey eine Bedingungsaktivität hinzu.
2. Erstellen Sie mehrere Pfade basierend auf Kriterien:
   * **Pfad 1**: Hochwertige Kundinnen und Kunden (Gesamtkäufe > 1.000 $)
   * **Pfad 2**: Stammkundinnen und -kunden (Gesamtkäufe zwischen 100 und 1.000 $)
   * **Pfad 3**: Neue Kundinnen und Kunden (Gesamteinkäufe &lt; 100 $)
3. Fügen Sie für jeden Pfad unterschiedliche Nachrichten oder Angebote hinzu.

Erfahren Sie mehr über [Bedingungen](condition-activity.md) und [Zielgruppenqualifizierung](audience-qualification-events.md).

+++

+++ Wie gehe ich mit verschiedenen Zeitzonen in meiner Journey um?

Journey Optimizer bietet mehrere Optionen für die Zeitzonenverwaltung:

* **Zeitzone des Profils**: Nachrichten werden basierend auf der Zeitzone gesendet, die im Profil eines Kontakts gespeichert ist
* **Feste Zeitzone**: Alle Nachrichten verwenden eine bestimmte von Ihnen definierte Zeitzone

Erfahren Sie mehr über die [Zeitzonenverwaltung](timezone-management.md).

+++

+++ Wie lange sollte ich zwischen den Nachrichten in meiner Journey warten?

**Best Practices für Wartezeiten**:

* **Transaktionsnachrichten** (Auftragsbestätigungen): sofortiger Versand
* **Begrüßungsserie**: 1–3 Tage zwischen den E-Mails
* **Schulungsinhalte**: 3–7 Tage zwischen den Nachrichten
* **Werbekampagnen**: mindestens 7 Tage zwischen den Angeboten
* **Wiederaufnahme der Interaktion**: 14–30 Tage für inaktive Benutzende

**Zu berücksichtigende Faktoren**:

* Branchenstandards und Kundenerwartungen
* Dringlichkeit und Bedeutung der Nachricht
* Ihre allgemeine Nachrichtenfrequenz über alle Kanäle hinweg
* Kundeninteraktionsmuster

**Tipp**: Verwenden Sie Journey-Begrenzungsregeln, um die Gesamtzahl der Nachrichten zu begrenzen, die ein Kontakt über alle Journeys hinweg erhält.

Erfahren Sie mehr über [Warteaktivitäten](wait-activity.md) und [Journey-Begrenzung](../conflict-prioritization/journey-capping.md).

+++

## Testen und Veröffentlichen

+++ Wie kann ich meine Journey vor der Veröffentlichung testen?

Journey Optimizer bietet zwei Testansätze:

* **Testmodus**: Simulieren Sie, wie sich die einzelnen Profile durch die Journey bewegen, um Logik, Bedingungen und Aktionen zu überprüfen, bevor Sie veröffentlichen.
* **Probelaufmodus**: Führen Sie Ihre Journey mit echten Produktionsdaten aus, ohne tatsächliche Kundinnen und Kunden zu kontaktieren oder Profilinformationen zu aktualisieren. Dies stärkt Ihr Vertrauen in Zielgruppen-Targeting und Journey-Design.

**Best Practice**: Testen Sie Journeys vor der Veröffentlichung immer, um sicherzustellen, dass sie wie erwartet funktionieren, und um Probleme frühzeitig zu erkennen.

Erfahren Sie mehr über [Testmodus](testing-the-journey.md) und [Probelauf](journey-dry-run.md).

+++

+++ Was passiert, wenn ich eine Journey veröffentliche?

Veröffentlichen einer Journey:

* Die Journey ist **Live** und kann neue Profile akzeptieren
* Profile können basierend auf den Eintrittskriterien (Ereignis oder Zielgruppe) eintreten
* Nachrichten und Aktionen werden für Profile ausgeführt, die sich durch die Journey bewegen
* Sie können Elemente in einer veröffentlichten Journey nur eingeschränkt bearbeiten (Sie müssen eine neue Version erstellen, wenn Sie mehr bearbeiten möchten)

Erfahren Sie mehr über das [Veröffentlichen von Journeys](publish-journey.md).

+++

+++ Kann ich eine bereits veröffentlichte Journey bearbeiten?

Ja, aber mit Einschränkungen. Sie können bestimmte Elemente einer Live-Journey bearbeiten:

**Folgende Elemente können bearbeitet werden**:

* Journey-Eigenschaften (Name, Beschreibung)
* Nachrichteninhalt in vorhandenen Nachrichtenaktivitäten
* Einige Journey-Einstellungen

**Folgende Elemente können nicht bearbeitet werden**:

* Journey-Struktur (Hinzufügen/Entfernen von Aktivitäten)
* Eintrittsbedingungen
* Logik der Journey-Arbeitsfläche

**Vornehmen struktureller Änderungen**:

1. **Erstellen einer neuen Version**: Duplizieren Sie die veröffentlichte Journey, um eine Entwurfsversion zu erstellen
2. **Vornehmen von Änderungen**: Bearbeiten Sie die Entwurfsversion nach Bedarf
3. **Testen der neuen Version**: Verwenden Sie den Testmodus, um Änderungen zu validieren
4. **Veröffentlichen der neuen Version**: Dadurch wird die vorherige Version automatisch geschlossen und die neue aktiviert

Profile, die sich bereits in der Journey befinden, schließen die Originalversion ab, während neue Profile in die neue Version eintreten.

Erfahren Sie mehr über [Journey-Versionen](journey-ui.md#journey-filter).

+++

+++ Wie stoppe ich eine Journey?

Sie können die Journey-Ausführung auf verschiedene Arten verwalten:

* **Schließen für neue Eintritte**: Stoppen Sie den Eintritt neuer Profile und erlauben Sie vorhandenen Profilen, die Journey abzuschließen
* **Sofortiges Stoppen**: Beenden Sie die Journey und lassen Sie alle aktuell darin enthaltenen Profile aussteigen
* **Pausieren**: Halten Sie die Journey vorübergehend an und setzen Sie sie später fort

Erfahren Sie mehr über das [Beenden von Journeys](end-journey.md).

+++

+++ Was ist der Unterschied zwischen „Schließen für neue Eintritte“ und „Stoppen“?

**Schließen für neue Eintritte**:

* Neue Profile können nicht in die Journey eintreten
* Profile, die sich bereits in der Journey befinden, fahren fort und schließen ihren Pfad ab
* Verwenden Sie diese Option, wenn Sie eine Journey langsam beenden möchten
* Beispiel: Saisonale Kampagne, die beendet wurde, bei der bestehende Kundinnen und Kunden jedoch ihr Erlebnis abschließen sollen

**Stoppen**:

* Beendet die Journey sofort für alle Profile
* Alle Profile, die sich derzeit in der Journey befinden, müssen aussteigen
* Verwenden Sie dies für dringende Situationen oder kritische Fehler
* Beispiel: Produktrückruf, der einen sofortigen Stopp der Werbenachrichten erfordert

Erfahren Sie mehr über das [Beenden von Journeys](end-journey.md) und das [Veröffentlichen von Journeys](publish-journey.md).

+++

## Journey-Ausführung und -Monitoring

+++ Wie kann ich den Profilfortschritt durch eine Journey verfolgen?

Sie können die Journey-Ausführung wie folgt überwachen:

* **Journey-Live-Bericht**: Zeigen Sie Echtzeitmetriken und KPIs für Ihre Journey an. Hier können Sie auch die Ergebnisse der Testausführung des Probelaufs überprüfen.
* **Journey-Bericht über die gesamte Zeit**: Analysieren Sie die Journey-Leistung mit Customer Journey Analytics. Hier können Sie auch die Ergebnisse der Testausführung des Probelaufs überprüfen.
* **Journey-Schrittereignisse**: Greifen Sie auf detaillierte Daten zur Ausführung zu, um benutzerdefiniertes Reporting zu erhalten.

Erfahren Sie mehr über [Journey-Reporting](report-journey.md).

+++

+++ Warum ist ein Profil nicht in meine Journey eingetreten?

Häufige Gründe, warum Profile möglicherweise nicht in eine Journey eintreten:

* **Ereignis nicht empfangen**: Das auslösende Ereignis wurde nicht gesendet oder ordnungsgemäß konfiguriert
* **Zielgruppenkriterien nicht erfüllt**: Das Profil ist nicht für die Eintrittszielgruppe qualifiziert
* **Regeln für den erneuten Eintritt**: Das Profil hat kürzlich die Journey abgeschlossen und der erneute Eintritt ist gesperrt
* **Journey nicht veröffentlicht**: Die Journey befindet sich im Entwurfsstatus
* **Ungültiger Namespace**: Der Journey-Namespace entspricht nicht der Profilidentität
* **Journey geschlossen**: Die Journey akzeptiert keine neuen Eintritte mehr
* **Zeitpunkt der Streaming-Zielgruppenqualifizierung**: Bei Journey, die die Zielgruppenqualifizierung mit Streaming-Zielgruppen verwenden, können Profile möglicherweise nicht eintreten, wenn sie sich bereits in der Zielgruppe befanden, bevor die Journey veröffentlicht wurde, oder wenn die Journey die Aktivierungsdauer nicht abgeschlossen hat (bis zu 10 Minuten nach der Veröffentlichung)

Erfahren Sie mehr über [Einstiegsverwaltung](entry-management.md) und [Überlegungen zur Qualifizierung von Streaming-Zielgruppen](audience-qualification-events.md#streaming-entry-caveats).

+++

+++ Was sind Journey-Schrittereignisse und wie kann ich sie verwenden?

Journey-Schrittereignisse sind automatisch generierte Datensätze, die detaillierte Informationen über jeden Schritt erfassen, den ein Profil in einer Journey durchläuft. Dazu gehören Eintritts- und Ausstiegsereignisse, Aktionsausführung (gesendete Nachrichten, aufgerufene benutzerdefinierte Aktionen), Journey-Übergänge (Wechseln zwischen Aktivitäten) sowie Fehler und Timeouts.

**Anwendungsfälle**:

* Erstellen benutzerdefinierter Berichte in Customer Journey Analytics- oder BI-Tools
* Debuggen von Journey-Ausführungsproblemen
* Nachverfolgen des detaillierten Profilverhaltens
* Erstellen erweiterter Analyse- und Attributionsmodelle

Erfahren Sie mehr über [Journey-Schrittereignisse](../reports/sharing-overview.md).

+++

+++ Wie kann ich eine Fehlerbehebung bei einer Journey durchführen, die nicht erwartungsgemäß funktioniert?

Journey Optimizer bietet mehrere Ressourcen zur Fehlerbehebung:

* **Fehlerindikatoren**: Visuelle Warnhinweise auf der Journey-Arbeitsfläche zeigen Konfigurationsprobleme an
* **Testmodus**: Durchlaufen Sie die Journey, um Probleme zu erkennen
* **Probelaufmodus**: Testen Sie die Journey mit echten Produktionsdaten, ohne Kundinnen und Kunden zu kontaktieren, um Targeting und Ausführung zu überprüfen
* **Journey-Berichte**: Überprüfen Sie die Ausführungsmetriken, um Engpässe oder Fehler zu ermitteln
* **Journey-Schrittereignisse**: Analysieren Sie detaillierte Ausführungsdaten, um das Profilverhalten zu verstehen

**Häufige Probleme**:

* Falsch konfigurierte Ereignisse oder Zielgruppen
* Fehlende Verbindungen zu Datenquellen
* Ungültige Ausdrücke in Bedingungen oder Personalisierung
* Zu kurze Timeout-Einstellungen

Erfahren Sie mehr über die [Fehlerbehebung bei Journeys](troubleshooting.md).

+++

<!--
+++ What happens if an action fails in a journey?

When an action fails (e.g., API call timeout, message delivery error), the journey continues by default unless configured otherwise. You can define condition activities to handle failure scenarios, and errors are logged in journey reports and step events for monitoring.

**Best practice**: Set appropriate timeout values for external actions and define alternative paths for critical failure scenarios.

Learn more about [action responses](../action/action-response.md).

+++
-->

+++ Kann ich sehen, wer sich gerade in meiner Journey befindet?

Ja. Verwenden Sie den **Journey-Live-Bericht**, um Folgendes anzuzeigen:

* Anzahl der Profile, die sich derzeit in der Journey befinden
* Anzahl der Profile pro Aktivität
* Profile, die in den letzten 24 Stunden eingetreten sind
* Echtzeit-Ausführungsmetriken

Verwenden Sie zum Anzeigen einzelner Profile **Journey-Schrittereignisse** in Customer Journey Analytics oder fragen Sie die Schrittereignisdatensätze direkt ab.

Erfahren Sie mehr über [Journey-Live-Reporting](report-journey.md).

+++

+++ Warum werden meine Nachrichten in meiner Journey nicht versendet?

**Häufige Gründe und Lösungen**:

* **Einverständnisprobleme**: Empfangende haben sich nicht für den Empfang von Nachrichten angemeldet
Lösung: Überprüfen Sie Einverständnisrichtlinien und Opt-in-Status

* **Unterdrückungsliste**: E-Mail-Adressen befinden sich auf der Unterdrückungsliste
Lösung: Überprüfen Sie die Unterdrückungsliste auf Bounces oder Beschwerden

* **Ungültige Kontaktinformationen**: Fehlende oder falsch formatierte E-Mail-Adressen/Telefonnummern
Lösung: Validieren Sie die Profildatenqualität

* **Journey nicht veröffentlicht**: Die Journey befindet sich noch im Entwurfsmodus
Lösung: Veröffentlichen Sie die Journey, um sie zu aktivieren

<!-- 
* **Message not approved**: Message content requires approval before sending
  Solution: Submit for approval or check approval status-->

* **Kanalkonfigurationsproblem**: E-Mail-/SMS-Konfiguration ist falsch
Lösung: Überprüfen Sie die Kanalkonfigurationen und -authentifizierung

Erfahren Sie mehr über [Fehlerbehebung](troubleshooting.md) und [Einverständnisverwaltung](../action/consent.md).

+++

+++ Wie personalisiere ich Nachrichten in meiner Journey?

Sie können mir dem **Personalisierungseditor** Nachrichten personalisieren.

**Verfügbare Personalisierungsdaten**:

* **Profilattribute**: Vorname, Nachname, E-Mail, benutzerdefinierte Felder
* **Ereignisdaten**: Kaufdetails, Suchverhalten, App-Aktivität
* **Kontextuelle Daten**: Journey-Variablen, Daten externer API
* **Zielgruppenzugehörigkeit**: Segmentqualifizierungen
* **Berechnete Attribute**: Vorberechnete Werte

**Beispiel für Personalisierung**:

* „Hallo `{{profile.firstName}}`, vielen Dank für Ihren Kauf von `{{event.productName}}`“
* „Entsprechend Ihrer Treuestufe (`{{profile.loyaltyTier}}`) erhalten Sie hier ein Sonderangebot“
* Dynamische Inhaltsbausteine, die sich je nach Kundenvorlieben ändern

Erhalten Sie mehr über [Personalisierung](../personalization/personalize.md). 

+++

+++ Kann ich je nach bevorzugtem Kanal verschiedene Nachrichten senden?

Ja. Verwenden Sie eine **[Bedingungsaktivität](condition-activity.md)**, um Profile basierend auf ihrem bevorzugten Kanal weiterzuleiten:

1. Fügen Sie der Journey eine [Bedingungsaktivität](condition-activity.md) hinzu.
2. Erstellen Sie einen Pfad für jeden Kanal, indem Sie das Profilattribut des bevorzugten Kanals überprüfen (z. B. `profile.preferredChannel`).
3. Konfigurieren von kanalspezifischen Pfaden:
   * **E-Mail-Pfad**: Fügen Sie eine [E-Mail-Aktion](../email/create-email.md) mit für E-Mails optimierten Inhalten hinzu
   * **SMS-Pfad**: Fügen Sie eine [SMS-Aktion](../sms/create-sms.md) mit kurzem Nachrichteninhalt hinzu
   * **Push-Pfad**: Fügen Sie eine [Push-Benachrichtigungsaktion](../push/create-push.md) mit kurzen, verwertbaren Inhalten hinzu
   * **In-App-Pfad**: Fügen Sie eine [In-App-Nachrichtenaktion](../in-app/create-in-app.md) für interaktive App-Benutzende hinzu
4. Fügen Sie einen Standardpfad für Profile ohne Voreinstellung hinzu und leiten Sie sie an Ihren primären Kanal weiter.

**Best Practices**:

* Stellen Sie sicher, dass Ihre Profildaten genaue Kanalvoreinstellungen enthalten
* Entwerfen Sie Inhalte, die für die Stärken und Einschränkungen jedes Kanals geeignet sind
* Verwenden Sie [Kanaloberflächen](../configuration/channel-surfaces.md) zum Verwalten von Kanalkonfigurationen
* Testen Sie alle Pfade, um einen ordnungsgemäßen Nachrichtenversand sicherzustellen

Erfahren Sie mehr über [Bedingungen](condition-activity.md), [Nachrichtenaktionen](journeys-message.md) und [Kanalauswahl](../channels/gs-channels.md).

+++

+++ Kann ich bestimmte Kundinnen und Kunden von meiner Journey ausschließen?

Ja, es gibt mehrere Möglichkeiten, Kundinnen und Kunden auszuschließen:

**Bei Journey-Eintritt**:

* Verwenden von [Zielgruppendefinitionen](../audience/creating-a-segment-definition.md) mit Ausschlussregeln
* Hinzufügen von [Eintrittsbedingungen](entry-management.md), die bestimmte Profile herausfiltern
* Konfigurieren von [auf Profilattributen basierenden Ausstiegskriterien](journey-properties.md) in Journey-Eigenschaften, um Profile basierend auf bestimmten Attributen automatisch auszuschließen

**In der Journey**:

* Hinzufügen einer [Bedingungsaktivität](condition-activity.md) früh in der Journey, um unerwünschte Profile aussteigen zu lassen
* Prüfen auf Ausschlussattribute (z. B. VIP-Status, Testkonten)
* Verwenden der [Zielgruppenqualifizierung](audience-qualification-events.md), um auszuschließende Profile zu ermitteln

**Beispiel für Ausschlussszenarien**:

* Ausschließen von Kundinnen und Kunden, die kürzlich etwas gekauft haben
* Ausschließen von VIP-Kundinnen und -Kunden von Standardwerbeaktionen
* Ausschließen von Mitarbeitenden und Testkonten
* Ausschließen von Kundinnen und Kunden in bestimmten Regionen

+++

## Erweiterte Konzepte

+++ Was ist ein Journey-Namespace und warum ist er wichtig?

Ein **Namespace** ist ein Identitätstyp (z. B. E-Mail, ECID, Telefonnummer), der bestimmt, wie Profile in der Journey identifiziert werden. Der Namespace definiert, welche Kennung zum Abgleichen von Profilen verwendet wird, muss über Eregnisse, Zielgruppen und Profildaten hinweg konsistent sein und wirkt sich auf das Verhalten beim Eintritt und erneuten Eintritt in Journeys aus.

**Best Practice**: Wählen Sie einen Namespace aus, mit dem Ihre Kundinnen und Kunden über alle Touchpoints hinweg zuverlässig identifiziert werden.

Erfahren Sie mehr über [Identity-Namespaces](../audience/get-started-identity.md).

+++

+++ Können Profile mehrmals in dieselbe Journey eintreten?

Ja, abhängig von den **Einstellungen für den erneuten Eintritt**:

* **Zulassen von erneutem Eintritt**: Profile können mehrmals nach Abschluss in die Journey eintreten
* **Wartezeit bis zum erneuten Eintritt**: Definieren Sie eine Mindestzeit zwischen den Journey-Eintritten (z. B. 7 Tage)
* **Erzwingen eines erneuten Eintritts bei einem Ereignis**: Lösen Sie eine neue Journey-Instanz aus, auch wenn sich das Profil bereits in der Journey befindet
* **Zusätzliche Kennung**: Verwenden Sie eine zusätzliche ID, damit Profile für verschiedene Entitäten (z. B. verschiedene Bestellungen, Buchungen oder Transaktionen) mehrmals in die Journey eintreten können, selbst wenn sie sich bereits in der Journey befinden

**Best Practice**: Verwenden Sie Regeln für den erneuten Eintritt, um Nachrichtenermüdung zu verhindern und eine angemessene Geschwindigkeit sicherzustellen. Erwägen Sie die Verwendung zusätzlicher Kennungen für Transaktions-Journeys, bei denen Profile mehrmals eintreten müssen, um verschiedene Transaktionen durchzuführen.

Erfahren Sie mehr über [Eintrittsverwaltung](entry-management.md) und [zusätzliche Kennungen](supplemental-identifier.md).

+++

+++ Was ist Versandzeitoptimierung?

**Versandzeitoptimierung (Send-Time Optimization, STO)** verwendet KI, um die beste Zeit zum Senden einer Nachricht an jedes einzelne Profil vorherzusagen und so Öffnungsraten und Interaktion zu maximieren. STO analysiert Muster im Interaktionsverlauf, um zu bestimmen, wann Empfangende mit der größten Wahrscheinlichkeit mit Ihrer Nachricht interagieren.

**Vorteile**:

* Verbesserte Öffnungs- und Klickraten
* Besseres Kundenerlebnis durch zeitlich optimal abgestimmte Nachrichten
* Reduzierte Abmelderaten

Erfahren Sie mehr über [Versandzeitoptimierung](send-time-optimization.md).

+++

+++ Was sind Journey-Begrenzungsregeln?

**Journey-Begrenzung** ermöglicht die Steuerung der Interaktion von Profilen mit Journeys, wodurch Nachrichtenermüdung verhindert und ein optimales Kundenerlebnis sichergestellt wird:

* **Eintrittsbegrenzung**: Begrenzt die Anzahl der Eintritte eines Profils in Journeys innerhalb eines bestimmten Zeitraums
* **Gleichzeitigkeitsbegrenzung**: Begrenzt die Anzahl der Journeys, in denen sich ein Profil gleichzeitig befinden kann

Sie können die maximale Anzahl von Eintritten oder die gleichzeitigen Eintritte pro Profil für alle Journeys oder für eine bestimmte Journey festlegen, Zeitfenster (täglich, wöchentlich, monatlich) definieren und Journeys priorisieren, wenn mehrere Journeys um dasselbe Profil konkurrieren.

Erfahren Sie mehr über [Journey-Begrenzung](../conflict-prioritization/journey-capping.md).

+++

+++ Kann ich meine Journey mit externen Systemen integrieren?

Ja. Verwenden Sie **benutzerspezifische Aktionen**, um APIs von Drittanbietern (CRM, Marketing-Automatisierung, Treuesysteme) aufzurufen, Daten an externe Systeme zu senden, Echtzeit-Informationen für die Entscheidungsfindung abzurufen und Workflows in externen Plattformen auszulösen.

Benutzerdefinierte Aktionen unterstützen Authentifizierung (API-Schlüssel, benutzerdefinierte Authentifizierung), Anpassung der Anfrage-/Antwort-Payload, Fehlerbehandlung und Timeouts sowie dynamische Parameter aus dem Journey-Kontext.

Weitere Informationen über [benutzerdefinierte Aktionen](using-custom-actions.md).

+++

+++ Wie kann ich Adobe Campaign mit Journeys verwenden?

Journey Optimizer lässt sich nativ mit Adobe Campaign integrieren, um erweiterte Funktionen zu nutzen:

* **Adobe Campaign Standard**: Verwenden Sie Campaign Standard-Aktionen, um Transaktionsnachrichten zu senden
* **Adobe Campaign v7/v8**: Lösen Sie Campaign-Workflows aus und verwenden Sie die Versandinfrastruktur von Campaign

**Best Practice**: Verwenden Sie diese Integration, wenn Sie bereits über Campaign-Vorlagen und -Datenmodelle verfügen oder Campaign-spezifische Funktionen benötigen.

Erfahren Sie mehr über die [Campaign-Integration](ajo-ac.md).

+++

+++ Was ist die Sprungaktivität?

Mit der **Sprungaktivität** können Profile von einer Journey in eine andere wechseln und es werden wiederverwendbare Journey-Muster, Journey-Orchestrierung über mehrere Journeys hinweg, vereinfachte Journey-Wartung und progressive Interaktionsstrategien ermöglicht.

Wenn ein Profil eine Sprungaktivität erreicht, steigt es aus der aktuellen Journey aus und tritt am Startpunkt der Ziel-Journey ein.

Erfahren Sie mehr über die [Sprungaktivität](jump.md).

+++

+++ Wie erstelle ich eine Journey für Begrüßungsserien?

Eine typische Begrüßungsserie umfasst mehrere Touchpoints über mehrere Tage:

**Beispielstruktur**:

1. **Eintritt**: Zielgruppe neuer Abonnierender oder Ereignis, wenn sich jemand anmeldet
2. **E-Mail 1 – Umgehende Begrüßung**: Dankeschön und Einführung
3. **Wartezeit**: 2 Tage
4. **E-Mail 2 – Erste Schritte**: Tutorial oder Produkthandbuch
5. **Wartezeit**: 3 Tage
6. **Bedingung**: Hat die Kundin bzw. der Kunde einen Kauf getätigt?
   * **Ja**: Beenden oder weiter zu Customer Journey
   * **Nein**: Fortsetzen der Begrüßungsserie
7. **E-Mail 3 – Incentive**: Spezieller Rabatt für erstmalige Käuferinnen und Käufer
8. **Wartezeit**: 5 Tage
9. **E-Mail 4 – Interaktion**: Bestseller oder beliebte Inhalte

**Best Practices**:

* 3–5 E-Mails über 2–3 Wochen
* Jede E-Mail sollte einen klaren Zweck haben sowie einen Handlungsaufruf enthalten
* Überwachen Sie Öffnungsraten und passen Sie Timing/Inhalt entsprechend an
* Lassen Sie Kundinnen und Kunden frühzeitig aussteigen, wenn eine Konversion erfolgt oder sie stark interagieren

Erfahren Sie mehr über [Journey-Anwendungsfälle](jo-use-cases.md).

+++

+++ Kann ich A/B-Tests für verschiedene Pfade in meiner Journey durchführen?

Ja. Verwenden Sie die **Optimierungsaktivität** (eingeschränkte Verfügbarkeit) oder erstellen Sie manuell Testaufspaltungen:

**Verwenden der Optimierungsaktivität** mit der Experimentmethode:

* Spaltet den Traffic zufällig auf verschiedene Pfade auf, um zu ermitteln, welcher am besten funktioniert
* Testet verschiedene Nachrichten, Angebote, Wartezeiten oder ganze Journey-Pfade
* Misst die Leistung anhand vordefinierter Erfolgsmetriken und gibt einen Gewinner aus

**Verwenden der Optimierungsaktivität** mit der Methode der Datenquellenbedingung:

* Erstellt eine Bedingung, die Profile nach dem Zufallsprinzip aufspaltet (z. B. mithilfe einer Zufallszahlenfunktion)
* Sendet verschiedene Erlebnisse an jede Aufspaltung
* Misst Ergebnisse mithilfe von Journey-Berichten

**Folgendes kann getestet werden**:

* Unterschiedliche E-Mail-Betreffzeilen
* Alternative Nachrichtinhalte
* Unterschiedliche Wartezeiten
* Verschiedene Angebote oder Incentives
* Ganz andere Journey-Pfade

Erfahren Sie mehr über die [Optimierungsaktivität](optimize.md) und [Inhaltsexperimente](../content-management/content-experiment.md).

+++

+++ Wie kann ich eine Journey auslösen, wenn das Inventar niedrig ist?

Erstellen Sie eine **Geschäftsereignis-Journey**:

1. **Konfigurieren eines Geschäftsereignisses**: Richten Sie ein Ereignis ein, das von Ihrem Inventarsystem ausgelöst wird, wenn der Bestand unter einen Schwellenwert fällt
2. **Auswählen der Zielgruppe**: Wählen Sie Profile aus, die benachrichtigt werden sollen (z. B. Kundinnen und Kunden, die das Produkt angesehen haben; Abonnierende für den Hinweis, wieder aufzustocken).
3. **Hinzufügen einer Nachrichtenaktion**: Senden Sie eine E-Mail- oder Push-Benachrichtigung
4. **Personalisieren von Inhalten**: Schließen Sie Produktdetails, aktuelle Inventarebene, Dringlichkeitsnachrichten ein

**Beispiel für Geschäftsereignisse**:

* Warnhinweis bei niedrigem Inventar
* Benachrichtigung bei Preisnachlass
* Produkt wieder auf Lager
* Ankündigung von Blitzverkauf
* Wetterbasierte Angebote

Erfahren Sie mehr über [Geschäftsereignisse](general-events.md).

+++

+++ Was sind Zusammenführungsrichtlinien und wie wirken sie sich auf Journeys aus?

**Zusammenführungsrichtlinien** bestimmen, wie Adobe Experience Platform Daten aus mehreren Quellen kombiniert, um eine einheitliche Profilansicht zu erstellen. Sie definieren Regeln für die Datenpriorisierung und Identitätszuordnung, wenn Profilfragmente in verschiedenen Datensätzen vorhanden sind.

**Auswirkungen auf Journeys**:

* Journeys verwenden die mit der Zielgruppe oder dem Ereignis verknüpfte Zusammenführungsrichtlinie, um zu bestimmen, welche Profildaten verfügbar sind
   * In Journeys vom Typ „Zielgruppe lesen“ oder „Zielgruppenqualifizierung“ wird die Zusammenführungsrichtlinie aus der Zielgruppe verwendet
   * In Journeys für unitäre Ereignisse wird die standardmäßige Zusammenführungsrichtlinie verwendet
   * In Journeys für Geschäftsereignisse wird die Zusammenführungsrichtlinie aus der Zielgruppe in der Aktivität „Zielgruppe lesen“ verwendet.

* Die Zusammenführungsrichtlinie wirkt sich darauf aus, auf welche Attribute in Journey-Bedingungen, Personalisierung und Aktionen zugegriffen werden kann
* Verschiedene Zusammenführungsrichtlinien können dazu führen, dass unterschiedliche Profildaten in der Journey verwendet werden

**Best Practices**:

* Stellen Sie sicher, dass die von Ihrer Journey verwendete Zusammenführungsrichtlinie mit Ihren Data Governance-Anforderungen übereinstimmt
* Machen Sie sich mit den Datensätzen in Ihrer Zusammenführungsrichtlinie vertraut, damit Sie wissen, welche Daten verfügbar sind
* Verwenden Sie konsistente Zusammenführungsrichtlinien für verwandte Zielgruppen und Journeys, um Ergebnisse zu prognostizieren

Erfahren Sie mehr über [Zusammenführungsrichtlinien](../audience/get-started-profiles.md) und [Identitätsverwaltung](../audience/get-started-identity.md).

+++

+++ Was ist der Unterschied zwischen einer Bedingungs- und einer Warteaktivität?

| | **Bedingungsaktivität** | **Warteaktivität** |
|---|---|---|
| **Zweck** | Erstellt verschiedene Pfade basierend auf Logik (wenn/dann) | Hält die Journey für einen bestimmten Zeitraum an |
| **Funktion** | Wertet Daten aus und leitet Profile entsprechend weiter | Hält Profile an einem bestimmten Punkt, bevor Sie fortfahren |
| **Anwendungsfall** | Segmentieren von Kundschaft, Überprüfen von Status, Verzweigen basierend auf Verhalten | Timing zwischen Nachrichten, Warten auf Geschäftszeiten, Erstellen von Verzögerungen |
| **Beispiel** | Wenn es sich um eine VIP-Kundin bzw. einen VIP-Kunden handelt, wird ein Premium-Angebot gesendet, andernfalls ein Standardangebot | Warten Sie 3 Tage nach der Begrüßungs-E-Mail, bevor Sie die nächste Nachricht senden |

**Zusammenarbeit**:

* Warten Sie eine bestimmte Zeit und überprüfen Sie dann mithilfe einer Bedingung, ob während der Wartezeit etwas passiert ist
* Beispiel: Warten Sie 7 Tage und überprüfen Sie dann, ob die Kundin bzw. der Kunde einen Kauf getätigt hat

Erfahren Sie mehr über [Bedingungen](condition-activity.md) und [Warteaktivitäten](wait-activity.md).

+++

## Best Practices und Einschränkungen

+++ Was sind die wichtigsten Einschränkungen, die ich beachten sollte?

Die wichtigsten Leitlinien sind folgende:

* **Journey-Komplexität**: Maximale Aktivitäten, Pfade und Verschachtelungsebenen
* **Durchsatz**: Nachrichtenübertragungsraten und API-Aufrufbeschränkungen
* **Time-to-Live**: Maximale Journey-Dauer (z. B. 91 Tage)
* **Zielgruppengröße**: Beschränkungen für die Batch-Größe von „Zielgruppe lesen“
* **Ausdruckskomplexität**: Zeichenbeschränkungen in Bedingungen und Personalisierung

Weitere Informationen finden Sie in den vollständigen [Leitlinien und Einschränkungen](../start/guardrails.md).

+++

+++ Was sind die Best Practices für das Journey-Design?

**Struktur und Organisation**:

* Konzentrieren Sie Journeys auf bestimmte Anwendungsfälle
* Verwenden Sie beschreibende Benennungen für Aktivitäten
* Fügen Sie Beschreibungen und Labels für komplexe Logik hinzu
* Gruppieren Sie verwandte Journeys mit Tags

**Leistung**:

* Optimieren Sie Wartezeiten, um Interaktion und Volumen auszugleichen
* Beschränken Sie externe API-Aufrufe auf wichtige Anwendungsfälle
* Verwenden Sie Begrenzungsregeln, um Nachrichtenermüdung zu verhindern
* Überprüfen Sie Journey-Metriken regelmäßig

**Testen**:

* Testen Sie Journeys vor der Veröffentlichung immer
* Verwenden Sie den Testmodus, um die Journey-Logik zu überprüfen und die Journey zu durchlaufen
* Verwenden Sie den Probelaufmodus, um mit echten Produktionsdaten zu testen, ohne Kundinnen und Kunden zu kontaktieren
* Testen Sie alle bedingten Pfade und Szenarien
* Verwenden Sie Testprofile
* Prüfen Sie Personalisierung und dynamische Inhalten

**Wartung**:

* Überprüfen Sie die Journey-Leistung regelmäßig
* Stoppen oder schließen Sie nicht verwendete Journeys
* Dokumentieren Sie Journey-Logik und Geschäftsregeln
* Planen Sie die Journey-Versionierung

Erfahren Sie mehr über [Best Practices für das Journey-Design](using-the-journey-designer.md).

+++

+++ Wie viele Aktivitäten kann ich einer Journey hinzufügen?

Journeys sind auf maximal 50 Aktivitäten beschränkt. Es wird jedoch empfohlen, die Journey einfacher zu halten, um bessere Wartung und Leistung zu gewährleisten.

Wenn Journeys etwa 50 Aktivitäten enthalten, können Wartung, Fehlerbehebung und Verständnis komplex und schwierig werden. Große Journeys mit vielen Verzweigungen und Bedingungen können sich auch auf die Verarbeitungszeit, die Lesbarkeit und die Team-Zusammenarbeit auswirken.

**Best Practice**: Stellen Sie sicher, dass Ihre Journeys fokussiert und verwaltbar sind. Wenn Ihre Journey immer komplexer wird, sollten Sie Folgendes in Betracht ziehen:

* Unterteilen in mehrere Journeys mithilfe der Sprungaktivität
* Erstellen von wiederverwendbaren Mustern in einfacheren Journeys
* Vereinfachen der Logik mit effizienteren Bedingungen
* Überprüfen der Notwendigkeit aller Aktivitäten

Erfahren Sie mehr über [Journey-Design](using-the-journey-designer.md) und [Leitlinien und Einschränkungen](../start/guardrails.md).

+++

+++ Wie stelle ich sicher, dass meine Journey eine gute Leistung im benötigten Umfang erzielt?

**Überlegungen zum Design**:

* Verwenden Sie [zielgruppenbasierten Eintritt](read-audience.md) für Batch-Nachrichten anstelle von einzelnen Ereignissen
* Implementieren Sie angemessene [Wartezeiten](wait-activity.md), um Nachrichtenvolumen zu verteilen
* Nutzen Sie [Begrenzungsregeln](../conflict-prioritization/journey-capping.md), um eine Systemüberlastung zu vermeiden
* Optimieren Sie [Bedingungslogik](condition-activity.md), um die Verarbeitungskomplexität zu reduzieren

**Monitoring**:

* Überprüfen Sie [Journey-Metriken](report-journey.md) regelmäßig
* Überwachen Sie die API-Leistung für [benutzerdefinierte Aktionen](using-custom-actions.md)
* Überprüfen Sie Fehlerraten und Timeout-Ereignisse mit [Tools zur Fehlerbehebung](troubleshooting.md)
* Abonnieren Sie [Journey-Warnhinweise](../reports/alerts.md) für kritische Journey-Fehler

**Optimierung**:

* Verwenden Sie [Testmodus](testing-the-journey.md) und [Probelauf](journey-dry-run.md), um die Leistung vor der Veröffentlichung zu überprüfen
* Minimieren Sie externe API-Aufrufe durch [benutzerdefinierte Aktionen](using-custom-actions.md), um Latenz und Abhängigkeit von Drittanbietersystemen zu vermeiden
* Speichern Sie wenn möglich häufig verwendete Daten in Adobe Experience Platform mithilfe der [Datensatzsuche](dataset-lookup.md), anstatt externe Aufrufe durchzuführen
* Überprüfen und optimieren Sie die Leistung des [Nachrichtenversands](journeys-message.md)

Erfahren Sie mehr über [Leitlinien und Einschränkungen](../start/guardrails.md).

+++

## Weitere Ressourcen

Detailliertere Informationen und Updates finden Sie in den folgenden Ressourcen:

* [Erste Schritte mit Journeys](journey.md)
* [Erstellen Ihrer ersten Journey](journey-gs.md)
* [Handbücher zur Fehlerbehebung](troubleshooting.md)
* [Anwendungsfälle für Journeys](jo-use-cases.md)
* [Produktbeschreibung zu Journey Optimizer](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
