---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen zu Journey
description: Häufig gestellte Fragen zu Journey Optimizer Journey
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: Journey, Fragen, Antworten, Fehlerbehebung, Hilfe, Anleitung
version: Journey Orchestration
source-git-commit: fa4849cfbb43d74ab85437f00acf6da750080cca
workflow-type: tm+mt
source-wordcount: '5125'
ht-degree: 2%

---


# Häufig gestellte Fragen {#faq-journeys}

Im Folgenden finden Sie häufig gestellte Fragen zu Adobe Journey Optimizer Journey.

Sie würden gerne mehr erfahren? Verwenden Sie die Feedback-Optionen unten auf dieser Seite, um Ihre Frage zu stellen, oder vernetzen Sie sich mit der [Adobe Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}.

## Allgemeine Konzepte

+++ Was ist eine Journey in Adobe Journey Optimizer?

Eine Journey ist eine mehrstufige Orchestrierung, mit der Sie Echtzeit-Kundenerlebnisse kanalübergreifend entwerfen und ausführen können. Journey kombinieren Ereignisse, Orchestrierungsaktivitäten, Aktionen und Nachrichten, um basierend auf Kundenverhalten und Geschäftsereignissen personalisierte, kontextuelle Erlebnisse zu schaffen.

Weitere Informationen zu [Journey](journey.md).

+++

+++ Was sind die verschiedenen Arten von Journey?

Adobe Journey Optimizer unterstützt vier Typen von Journey:

* **Unitäre Journey**: Wird einzeln durch ein Ereignis ausgelöst (z. B. Kauf, App-Anmeldung). Die Profile wechseln jeweils zu einem Zeitpunkt zum Journey, wenn das Ereignis eintritt.
* **Audience-Journey lesen**: Beginnen Sie mit einer Audience aus Adobe Experience Platform und senden Sie Nachrichten im Batch an alle Profile in dieser Audience.
* **Journey zur Zielgruppenqualifizierung** Wird ausgelöst, wenn Profile sich für ein bestimmtes Zielgruppensegment qualifizieren (oder daraus austreten). Profile treten in die Journey ein, wenn sie die Zielgruppenkriterien erfüllen.
* **Geschäftsereignis-Journey**: Ausgelöst durch Geschäftsereignisse (z. B. Stock-Updates, Wetterwarnungen), die mehrere Profile gleichzeitig betreffen.

Weitere Informationen zu [Journey-Typen](entry-management.md#types-of-journeys).

+++

+++ Was ist der Unterschied zwischen einer Journey und einer Kampagne?

**[Journey](journey.md)** sind mehrstufige Orchestrierungen, die auf Ereignisse oder Zielgruppen reagieren und über den gesamten Kundenlebenszyklus hinweg eine komplexe Logik, Bedingungen, Wartezeiten und mehrere Berührungspunkte ermöglichen.

**[Kampagnen](../campaigns/get-started-with-campaigns.md)** gibt es in drei Typen:

* **[Aktionskampagnen](../campaigns/create-campaign.md)**: Einmalige oder wiederkehrende Nachrichten, die an eine bestimmte Zielgruppe gesendet werden, eignen sich ideal für eigenständige Nachrichten wie Werbeanzeigen oder Newsletter.
* **[API-ausgelöste Kampagnen](../campaigns/api-triggered-campaigns.md)**: Über API-Aufrufe ausgelöste Kampagnen, die die Integration mit externen Systemen ermöglichen, um Nachrichten basierend auf Echtzeit-Ereignissen oder Geschäftslogik zu senden.
* **[Orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)**: Mehrstufige, zielgruppenbasierte Kampagnen auf einer Arbeitsfläche, die Bedingungen, Wartezeiten und mehrere Aktionen zur Erstellung geplanter, koordinierter Erlebnisse enthalten können.

**Best Practice**: Verwenden Sie [Journey](journey.md) für komplexe, ereignisgesteuerte Interaktionen mit erweiterter Orchestrierung; [Aktionskampagnen](../campaigns/create-campaign.md) für geplante, zielgruppenbasierte Kommunikationen; [API-ausgelöste Kampagnen](../campaigns/api-triggered-campaigns.md) für die programmgesteuerte Auslösung aus externen Systemen; [orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) für mehrstufige Kommunikation mit kampagnenspezifischen Anforderungen.

+++

+++ Was sind die Hauptkomponenten einer Journey?

Eine Journey besteht aus:

* **Events**: Einstiegspunkte, an denen die Journey Trigger wird (z. B. Profilqualifizierung, Geschäftsereignisse)
* **Orchestrierungsaktivitäten**: Logikkomponenten wie Bedingungen, Warten, Zielgruppe lesen und Beenden
* **Aktionen**: Aktivitäten, die Aufgaben ausführen, z. B. Nachrichten senden, Profile aktualisieren oder externe APIs aufrufen
* **Integrierte Kanalaktionen**: Native Messaging-Funktionen für E-Mail, SMS, Push und andere Kanäle
* **Benutzerdefinierte Aktionen**: Integration mit Drittanbietersystemen

Weitere Informationen zu [Journey-Aktivitäten](about-journey-activities.md).

+++

+++ Welche Zielgruppentypen werden in Journey unterstützt und welche Einschränkungen gelten für sie?

Adobe Journey Optimizer unterstützt vier Arten von Zielgruppen mit jeweils unterschiedlichen Eigenschaften und Leitplanken:

**1. Streaming-Zielgruppen**

* **Beschreibung**: Zielgruppen, die in Echtzeit ausgewertet werden, wenn sich die Profildaten ändern
* **Auswertung**: Kontinuierliche Auswertung, wenn Profilattribute oder Ereignisse den Segmentkriterien entsprechen
* **Journey-Nutzung**: Wird bei Aktivitäten vom Typ „Zielgruppe lesen“, „Zielgruppen-Qualifizierung“ und „Bedingung“ unterstützt
* **Am besten geeignet für**: Echtzeit-Interaktion basierend auf Verhaltensänderungen oder Profilaktualisierungen
* **Schutzmaßnahmen**:
   * Die maximale Zielgruppengröße hängt von Ihrer Journey Optimizer-Lizenz ab
   * Auswertungslatenz normalerweise unter 5 Minuten
   * Komplexe Segmentlogik kann die Auswertungsleistung beeinträchtigen

**2. Batch-Zielgruppen**

* **Beschreibung**: Zielgruppen, die auf geplanter Basis ausgewertet werden (normalerweise täglich)
* **Auswertung**: In geplanten Intervallen in Batch-Vorgängen verarbeitet
* **Journey-Nutzung**: Unterstützt bei Aktivitäten vom Typ „Zielgruppe lesen“ und „Bedingung“; eingeschränkte Unterstützung bei Journey zur Zielgruppenqualifizierung
* **Am besten geeignet für**: Regelmäßige Kampagnen, Newsletter, geplante Nachrichten
* **Schutzmaßnahmen**:
   * Die Auswertung erfolgt einmal täglich (Standard) oder nach einem konfigurierten Zeitplan
   * Profile spiegeln möglicherweise erst bei der nächsten Auswertung Echtzeitänderungen wider
   * Die Aktivität „Zielgruppe lesen“ kann große Batch-Zielgruppen effizient verarbeiten

**3. Audiences hochladen (benutzerdefinierter Upload)**

* **Beschreibung**: Zielgruppen, die durch Hochladen von CSV-Dateien mit Profilkennungen erstellt werden
* **Evaluierung**: Statische Liste wird nur aktualisiert, wenn neue Dateien hochgeladen werden
* **Journey-Nutzung**: Wird in Aktivitäten vom Typ „Zielgruppe lesen“ und „Bedingung“ unterstützt; **nicht unterstützt** in Journey zur Zielgruppenqualifizierung
* **Am besten für**: Einmalige Kampagnen, externe Listenimporte, zielgerichtete Kommunikation
* **Schutzmaßnahmen**:
   * Es gelten CSV-Dateigrößenbeschränkungen (in der Produktdokumentation finden Sie aktuelle Beschränkungen)
   * Zielgruppenmitglieder sind statisch, bis sie mit neuem Upload aktualisiert werden
   * Identity-Namespace muss mit Journey-Namespace übereinstimmen
   * Profile müssen in Adobe Experience Platform vorhanden sein

**4. Federated Audience Composition (FAC)-Zielgruppen**

* **Beschreibung**: Zielgruppen, die mit Federated Data Warehouse erstellt wurden, sodass Sie Zielgruppen aus externen Data Warehouses abfragen und erstellen können, ohne Daten in Adobe Experience Platform kopieren zu müssen
* **Auswertung**: Statische Komposition wird aktualisiert, wenn die Federated-Audience-Komposition ausgeführt wird
* **Journey-Nutzung**: Unterstützt bei Aktivitäten vom Typ „Zielgruppe lesen“ und „Bedingung“; **nicht unterstützt** in Journey zur Zielgruppenqualifizierung (ähnlich wie beim Hochladen von Zielgruppen aus einer Backend-Perspektive)
* **Best for**: Enterprise Data Warehouse-Integration, Zielgruppenkomposition unter Verwendung externer Datenquellen, Szenarien, in denen Daten in externen Systemen verbleiben müssen
* **Schutzmaßnahmen**:
   * Zielgruppenmitglieder sind bis zur nächsten Ausführung der Federated-Komposition statisch
   * Identity-Namespace muss mit Journey-Namespace übereinstimmen
   * Die Leistung hängt von den Abfragefunktionen des externen Data Warehouse ab
   * Erfordert das Add-on „Federated Audience Composition“

**Customer Journey Analytics (CJA)-Zielgruppen**:

Obwohl CJA-Zielgruppen in Journey nicht direkt unterstützt werden, können Sie eine **„Problemumgehung“**, indem Sie eine CJA-Zielgruppe in eine Segmentierungsregel „einschließen“. Dadurch wird eine Batch-UPS-Zielgruppe (Unified Profile Service) erstellt, die auf die CJA-Zielgruppe verweist und sie für die Verwendung in Journey als Batch-Zielgruppentyp verfügbar macht.

**Journey-spezifische Überlegungen**:

* **Audience-Journey lesen**: Alle vier Audience-Typen werden unterstützt. Der Batch-Export erfolgt bei der Ausführung von Journey
* **Journey zur Zielgruppenqualifizierung**: Streaming-Zielgruppen empfohlen; Batch-Zielgruppen haben eine verzögerte Qualifizierungserkennung; Upload- und FAC-Zielgruppen werden nicht unterstützt
* **Bedingungsaktivitäten**: Alle Zielgruppentypen können zur Überprüfung der Mitgliedschaft verwendet werden
* **Namespace-Ausrichtung**: Der Identity-Namespace der Zielgruppe muss mit dem Namespace der Journey übereinstimmen, damit die Profile ordnungsgemäß identifiziert werden können

**Best Practices**:

* Verwenden **Streaming-Zielgruppen** für ereignisgesteuerte Journey in Echtzeit, die eine sofortige Reaktion erfordern
* Verwenden **Batch-Zielgruppen** für geplante Kommunikationen, bei denen eine tägliche Auswertung ausreicht
* Verwenden **Zielgruppen hochladen** für zielgerichtete einmalige Kampagnen mit externen Listen
* Verwenden Sie **FAC-Zielgruppen** wenn Sie Enterprise Data Warehouse-Funktionen ohne Datenduplizierung nutzen müssen
* Überwachen der Zielgruppengröße und der Auswertungsleistung in umfangreichen Bereitstellungen
* Berücksichtigen Sie beim Entwerfen von Journey-Zeiten und Einstiegsbedingungen die Aktualisierungsraten der Zielgruppe

Erfahren Sie mehr über [Zielgruppen](../audience/about-audiences.md), [Erstellen von &#x200B;](../audience/creating-a-segment-definition.md), [benutzerdefinierte Upload-Zielgruppen](../audience/custom-upload.md) und [Federated-Zielgruppen-Komposition](../audience/federated-audience-composition.md).

+++

+++ Wie wähle ich zwischen einer unitären Journey und einer gelesenen Zielgruppen-Journey?

Verwenden **unitären Journey** wenn:

* Sie müssen in Echtzeit auf individuelle Kundenaktionen reagieren (z. B. Kaufbestätigung, Warenkorbabbruch)
* Jeder Kunde sollte in seinem eigenen Tempo voranschreiten
* Sie einen Trigger auf der Grundlage bestimmter Ereignisse erstellen möchten

Verwenden Sie **Zielgruppen-Journey lesen** wenn:

* Sie senden Batch-Nachrichten an eine Gruppe (z. B. monatlicher Newsletter, Werbekampagnen)
* Alle Kunden sollten die Nachricht etwa zur selben Zeit erhalten
* Sie zielen auf ein vordefiniertes Zielgruppensegment ab

+++

## Erstellen von Journey

+++ Wie baue ich meine erste Journey?

Führen Sie die folgenden wichtigen Schritte aus:

1. **Voraussetzungen einrichten**: Konfigurieren Sie Ereignisse, Datenquellen und Aktionen nach Bedarf
2. **Journey erstellen**: Navigieren Sie zum Menü Journey und klicken Sie auf &quot;Journey erstellen“
3. **Journey-Eigenschaften definieren**: Legen Sie den Journey-Namen, die Beschreibung und andere Einstellungen fest
4. **Journey entwerfen**: Ziehen Sie Aktivitäten per Drag-and-Drop aus der Palette in die Arbeitsfläche
5. **Journey testen**: Testmodus zur Validierung der Journey-Logik verwenden
6. **Probelauf der Journey**: Verwenden Sie Probelauf, um die Journey mit echten Produktionsdaten zu testen, ohne echte Kunden zu kontaktieren oder Profilinformationen zu aktualisieren
7. **Journey veröffentlichen**: Aktivieren der Journey, um sie live zu schalten

Befolgen Sie [Schritt-für-Schritt-Anleitung](journey-gs.md).

+++

+++ Welche Voraussetzungen müssen erfüllt sein, damit eine Journey erstellt werden kann?

Die Voraussetzungen hängen von Ihrem Journey-Typ ab:

* **Ereignisausgelöste Journey**: Konfigurieren Sie Ereignisse, um zu definieren, wann Profile in die Journey eintreten sollen
* **Zielgruppenbasierte Journey**: Erstellen von Zielgruppen in Adobe Experience Platform
* **Datenanreicherung**: Einrichten von Datenquellen, um zusätzliche Informationen abzurufen
* **Integrationen von Drittanbietern**: Konfigurieren von benutzerdefinierten Aktionen bei Verwendung externer Systeme

Weitere Informationen zur Konfiguration von [Journey](../configuration/about-data-sources-events-actions.md).

+++

+++ Kann ich auf meinem Journey Daten von externen Systemen verwenden?

Ja, es gibt mehrere Ansätze zur Nutzung externer Daten:

**Best Practices**:

* **Benutzerdefinierte Aktionen**: Rufen Sie externe APIs über benutzerdefinierte Aktionen auf, um Daten abzurufen oder an Drittanbietersysteme zu senden. Dies ist der empfohlene Ansatz für Echtzeit-Interaktionen mit externen Systemen.
* **Datensatzsuche**: Wenn Sie Daten aus externen Systemen in Adobe Experience Platform laden können, verwenden Sie die Datensatzsuchfunktion, um in Experience Platform-Datensätzen gespeicherte Informationen abzurufen.
* **Externe Datenquellen**: Konfigurieren Sie externe Datenquellen, um Informationen aus API-Services von Drittanbietern abzurufen (weniger empfohlen als die oben genannten Ansätze).

Mit diesen Optionen können Sie das Kundenerlebnis mit Daten aus Ihrem CRM, Treuesystemen, Wetter-Services oder anderen externen Plattformen anreichern.

Weitere Informationen zu [benutzerdefinierten Aktionen](using-custom-actions.md) und [Datensatzsuche](dataset-lookup.md).

+++

+++ Wie füge ich Bedingungen zu meinem Journey hinzu?

Sie können Bedingungen mithilfe der Aktivität **Bedingung** aus der Orchestrierungspalette hinzufügen. Bedingungen ermöglichen Folgendes:

* Erstellen einfacher oder erweiterter Bedingungen mithilfe des Ausdruckseditors
* Aufspaltung der Journey in mehrere Pfade basierend auf Profilattributen, Zielgruppenzugehörigkeit, Ereignissen oder kontextuellen Daten
* Zeitüberschreitungspfade für Profile definieren, die die Bedingung nicht innerhalb einer bestimmten Zeit erfüllen

Weitere Informationen zu [Bedingungen](condition-activity.md).

+++

+++ Kann ich Nachrichten auf einer Journey an Profile senden?

Ja. Journey Optimizer umfasst **integrierte Kanalaktionen** mit denen Sie Nachrichten per E-Mail, Push-Benachrichtigungen, SMS/MMS/RCS, In-App-Nachrichten, Web-Erlebnisse, Code-basierte Erlebnisse, Briefpost, Inhaltskarten, WhatsApp und LINE senden können. Sie können Nachrichteninhalte direkt in Journey Optimizer entwerfen und als Aktionsaktivitäten in Ihrem Journey hinzufügen.

Bei Kanälen, die nativ nicht unterstützt werden, können Sie **benutzerdefinierte Aktionen** verwenden, um sie in externe Messaging-Plattformen zu integrieren und Nachrichten über einen beliebigen Drittanbieterkanal zu senden.

Weitere Informationen zu [Nachrichten in Journey](journeys-message.md) und [benutzerdefinierten Aktionen](using-custom-actions.md).

+++

+++ Wie warte ich auf eine bestimmte Zeit oder ein bestimmtes Ereignis auf einer Journey?

Verwenden Sie die **Warteaktivität**, um die Journey für eine bestimmte Dauer oder bis zu einem bestimmten Datum/zu einer bestimmten Uhrzeit anzuhalten. Warteaktivitäten sind nützlich für:

* Versand von Folgenachrichten nach einer Verzögerung (z. B. 3 Tage nach dem Kauf)
* Erstellen von Drip-Kampagnen mit Zeitintervallen
* Kombination mit Bedingungen zum Erstellen von Zeitüberschreitungsszenarien

Weitere Informationen zu [Warteaktivitäten](wait-activity.md).

+++

+++ Kann ich Profilinformationen auf einer Journey aktualisieren?

Ja. Verwenden Sie die Aktivität **Profil aktualisieren**, um Profilattribute in Adobe Experience Platform auf der Grundlage von Journey-Ereignissen oder -Bedingungen zu ändern. Dies ist nützlich für die Aktualisierung von Treuepunkten, die Aufzeichnung von Journey-Meilensteinen, die Änderung der Präferenzeinstellungen oder die Verfolgung der Kundeninteraktionswerte.

Weitere Informationen zu [Profilaktualisierungen](update-profiles.md).

+++

+++ Wie sende ich eine E-Mail, sobald jemand einen Kauf tätigt?

Erstellen Sie **unitäre ereignisgesteuerte Journey**:

1. Konfigurieren eines „Kauf“-Ereignisses mit den Bestelldetails
2. Ereignis als Einstiegspunkt für Journey hinzufügen
3. Sofort mit einer E-Mail -Aktion folgen
4. Gestalten Ihrer Bestellbestätigungs-E-Mail mit personalisierten Bestelldetails
5. Veröffentlichen der Journey

Die Journey wird bei Erhalt eines Kaufereignisses automatisch Trigger und sendet die Bestätigungs-E-Mail in Echtzeit.

Weitere Informationen zu [Ereigniskonfiguration](../event/about-events.md) und [E-Mail-Aktionen](journeys-message.md).

+++

+++ Kann ich eine Nachricht erneut senden, wenn jemand sie nicht öffnet oder anklickt?

Ja. Verwenden Sie ein **Reaktionsereignis** mit einem **Timeout**:

1. Fügen Sie nach dem Versand Ihrer Nachricht ein Reaktionsereignis hinzu, das auf E-Mail-Öffnungen oder -Klicks wartet
2. Konfigurieren Sie eine maximale Wartezeit (z. B. 3 Tage) für das Reaktionsereignis.
3. Erstellen Sie zwei Pfade:
   * **Wenn geöffnet/geklickt**: Mit den nächsten Schritten fortfahren oder die Journey beenden
   * **Zeitüberschreitungspfad (nicht geöffnet/angeklickt)**: Erinnerungs-E-Mail mit anderer Betreffzeile senden

**Best Practice**: Begrenzen Sie die Anzahl der erneuten Sendungen, um das Auftreten von Spam zu vermeiden (in der Regel maximal 1-2 Erinnerungen).

Weitere Informationen zu [Reaktionsereignissen](reaction-events.md).

+++

+++ Wie erstelle ich eine Warenkorbabbruch-Journey?

Erstellen Sie eine ereignisausgelöste Journey mit einem Reaktionsereignis mit einer Zeitüberschreitung:

1. **Konfigurieren eines Ereignisses „Warenkorbabbruch“**: Wird ausgelöst, wenn Artikel hinzugefügt werden, der Checkout jedoch nicht innerhalb eines bestimmten Zeitraums abgeschlossen ist
2. **Reaktionsereignis hinzufügen**: Konfigurieren, um auf ein Kaufereignis zu warten
3. **Zeitüberschreitungszeitraum festlegen**: Definieren Sie eine maximale Wartezeit (z. B. 1-2 Stunden) für das Reaktionsereignis, damit der Kunde Zeit hat, den Vorgang natürlich abzuschließen
4. **Erstellen Sie zwei Pfade**:
   * **Wenn ein Kaufereignis auftritt**: Beenden Sie das Journey oder fahren Sie mit dem Nachkaufsfluss fort
   * **Zeitüberschreitungspfad (kein Kauf)**: Senden Sie eine E-Mail zur Abbruchserinnerung mit Warenkorbinhalt
5. **Optional**: Fügen Sie ein weiteres Reaktionsereignis mit Timeout (24 Stunden) hinzu und senden Sie eine zweite Erinnerung mit einem Anreiz (z. B. 10 % Rabatt)

Erfahren Sie mehr über [Journey-Anwendungsfälle](jo-use-cases.md) und [Reaktionsereignisse](reaction-events.md).

+++

+++ Wie unterteile ich Kundinnen und Kunden je nach Kaufverlauf in verschiedene Pfade?

Verwenden Sie eine **Bedingungsaktivität** mit Zielgruppenzugehörigkeit oder Profilattributen:

1. Hinzufügen einer Aktivität vom Typ Bedingung zu Ihrem Journey
2. Erstellen Sie mehrere Pfade basierend auf Kriterien:
   * **Path 1**: Hochwertige Kunden (Gesamtkäufe > 1.000 USD)
   * **Path 2**: Stammkunden (Gesamtkäufe zwischen 100 und 1000 $)
   * **Pfad 3**: Neue Kunden (Gesamteinkäufe &lt; 100 $)
3. Fügen Sie für jeden Pfad unterschiedliche Nachrichten oder Angebote hinzu

Weitere Informationen zu [Bedingungen](condition-activity.md) und [Zielgruppen-Qualifizierung](audience-qualification-events.md).

+++

+++ Wie handhabe ich verschiedene Zeitzonen in meinem Journey?

Journey Optimizer bietet mehrere Optionen für die Zeitzonenverwaltung:

* **Zeitzone des Profils**: Nachrichten werden basierend auf der Zeitzone eines jeden Kontakts gesendet, die in seinem Profil gespeichert ist
* **Feste Zeitzone**: Alle Nachrichten verwenden eine bestimmte von Ihnen definierte Zeitzone

Weitere Informationen über [Zeitzonenverwaltung](timezone-management.md).

+++

+++ Wie lange sollte ich zwischen den Nachrichten auf meinem Journey warten?

**Best Practices für Wartezeiten**:

* **Transaktionsnachrichten** (Auftragsbestätigungen): Sofort versenden
* **Begrüßungsserie**: 1-3 Tage zwischen den E-Mails
* **Schulungsinhalte**: 3-7 Tage zwischen den Nachrichten
* **Werbekampagnen**: mindestens 7 Tage zwischen den Angeboten
* **Erneute Interaktion**: 14-30 Tage für inaktive Benutzer

**Zu berücksichtigende**:

* Branchenstandards und Kundenerwartungen
* Dringlichkeit und Wichtigkeit der Botschaft
* Ihre allgemeine Nachrichtenfrequenz über alle Kanäle hinweg
* Kundeninteraktionsmuster

**Tipp**: Verwenden Sie Journey-Begrenzungsregeln, um die Gesamtzahl der Nachrichten zu begrenzen, die ein Kunde über alle Journey hinweg erhält.

Weitere Informationen zu [Warteaktivitäten](wait-activity.md) und [Journey-Begrenzung](../conflict-prioritization/journey-capping.md).

+++

## Testen und Veröffentlichen

+++ Wie kann ich meinen Journey vor der Veröffentlichung testen?

Journey Optimizer bietet zwei Testansätze:

* **Testmodus**: Simulieren Sie die einzelnen Profile, die sich Schritt für Schritt durch den Journey bewegen, sodass Sie Logik, Bedingungen und Aktionen überprüfen können, bevor Sie live gehen.
* **Probelauf-Modus**: Führen Sie Ihren Journey mit echten Produktionsdaten aus, ohne sich an tatsächliche Kunden zu wenden oder Profilinformationen zu aktualisieren. Dies gibt Ihnen Vertrauen in Zielgruppen-Targeting und Journey-Design.

**Best Practice**: Testen Sie Journey immer vor der Veröffentlichung, um sicherzustellen, dass sie wie erwartet funktionieren, und um Probleme frühzeitig zu identifizieren.

Weitere Informationen über [Testmodus](testing-the-journey.md) und [Probelauf](journey-dry-run.md).

+++

+++ Was passiert, wenn ich eine Journey veröffentliche?

Beim Veröffentlichen einer Journey:

* Die Journey wird **Live** und kann neue Profile akzeptieren
* Profile können basierend auf den Einstiegskriterien (Ereignis oder Zielgruppe) eintreten
* Nachrichten und Aktionen werden für Profile ausgeführt, die sich durch den Journey bewegen
* Sie können nur eingeschränkte Elemente auf einer veröffentlichten Journey bearbeiten (Sie müssen eine neue Version erstellen, wenn Sie mehr bearbeiten möchten)

Weitere Informationen über [Veröffentlichen von Journey](publishing-the-journey.md).

+++

+++ Kann ich eine bereits veröffentlichte Journey modifizieren?

Ja, aber mit Einschränkungen. Sie können bestimmte Elemente einer Live-Journey bearbeiten:

**Was Sie bearbeiten können**:

* Journey-Eigenschaften (Name, Beschreibung)
* Nachrichteninhalt in vorhandenen Nachrichtenaktivitäten
* Einige Journey-Einstellungen

**Was Sie nicht bearbeiten können**:

* Journey-Struktur (Hinzufügen/Entfernen von Aktivitäten)
* Einreisebedingungen
* Journey Canvas-Logik

**So nehmen Sie strukturelle Änderungen vor**:

1. **Neue Version erstellen**: Duplizieren Sie die veröffentlichte Journey, um eine Entwurfsversion zu erstellen
2. **Änderungen vornehmen**: Bearbeiten Sie die Entwurfsversion nach Bedarf
3. **Neue Version testen**: Verwenden Sie den Testmodus, um Änderungen zu validieren
4. **Neue Version veröffentlichen**: Dadurch wird die vorherige Version automatisch geschlossen und die neue aktiviert

Profile, die sich bereits auf der Journey befinden, vervollständigen die Originalversion, während neue Profile in die neue Version eintreten.

Weitere Informationen zu [Journey-Versionen](journey-ui.md#journey-versions).

+++

+++ Wie stoppe ich eine Journey?

Sie können die Journey-Ausführung auf verschiedene Weise verwalten:

* **Für neue Eintritte schließen**: Stoppen Sie den Eintritt neuer Profile, während Sie vorhandenen Profilen erlauben, ihren Journey abzuschließen
* **Sofort anhalten**: Beenden Sie den Journey und beenden Sie alle aktuell darin enthaltenen Profile.
* **Pause**: Journey vorübergehend anhalten und später fortsetzen

Weitere Informationen zum [&#x200B; von Journey](end-journey.md).

+++

+++ Was ist der Unterschied zwischen „Für neue Eintritte schließen“ und „Anhalten“?

**Für neue Eintritte schließen**:

* Neue Profile können nicht auf die Journey zugreifen
* Profile, die sich bereits auf der Journey befinden, fahren fort und schließen ihren Pfad ab
* Verwenden Sie diese Option, wenn Sie eine Journey elegant herunterladen möchten
* Beispiel: Saisonale Kampagne, die beendet wurde, bei der bestehende Kundinnen und Kunden jedoch ihr Erlebnis abschließen sollen

**Anhalten**:

* Beendet die Journey für alle Profile sofort
* Alle Profile, die sich derzeit auf der Journey befinden, werden beendet
* Verwenden Sie dies für dringende Situationen oder kritische Fehler
* Beispiel: Produkt-Rückruf, der einen sofortigen Stopp der Werbenachrichten erfordert

Erfahren Sie mehr über [Beenden von Journey](end-journey.md) und [Veröffentlichen von Journey](publishing-the-journey.md).

+++

## Ausführung und Überwachung von Journey

+++ Wie kann ich den Profilfortschritt auf einer Journey verfolgen?

Sie können die Journey-Ausführung überwachen mit:

* **Journey-Live-Bericht**: Zeigen Sie Echtzeitmetriken und KPIs für Ihren Journey an. Hier können Sie auch die Ergebnisse der Testausführung überprüfen.
* **Journey-All-Time-Bericht**: Analysieren Sie die Journey-Leistung mit Customer Journey Analytics. Hier können Sie auch die Ergebnisse der Testausführung überprüfen.
* **Journey-Schrittereignisse**: Zugriff auf detaillierte Ausführungsdaten für benutzerdefinierte Berichte

Weitere Informationen zum [Journey-Reporting](report-journey.md).

+++

+++ Warum hat kein Profil meinen Journey eingegeben?

Häufige Gründe, warum Profile möglicherweise keine Journey eingeben:

* **Ereignis nicht empfangen**: Das auslösende Ereignis wurde nicht gesendet oder ordnungsgemäß konfiguriert
* **Zielgruppenkriterien nicht erfüllt**: Das Profil ist nicht für die Einstiegszielgruppe qualifiziert
* **Regeln für den erneuten Eintritt**: Das Profil hat kürzlich die Journey abgeschlossen und der erneute Eintritt ist blockiert
* **Journey nicht veröffentlicht**: Die Journey befindet sich im Entwurfsstatus
* **Ungültiger Namespace**: Der Journey-Namespace entspricht nicht der Profilidentität
* **Journey geschlossen**: Die Journey akzeptiert keine neuen Eintritte mehr

Weitere Informationen über [Einstiegsverwaltung](entry-management.md).

+++

+++ Was sind Journey-Schrittereignisse und wie kann ich sie verwenden?

Journey-Schrittereignisse sind automatisch generierte Datensätze, die detaillierte Informationen über jeden Schritt erfassen, den ein Profil auf einem Journey unternimmt. Dazu gehören Eintritts- und Ausstiegsereignisse, Aktionsausführung (gesendete Nachrichten, benutzerdefinierte Aktionen, die aufgerufen werden), Journey-Übergänge (Wechseln zwischen Aktivitäten) sowie Fehler und Zeitüberschreitungen.

**Anwendungsfälle**:

* Erstellen benutzerdefinierter Berichte in Customer Journey Analytics- oder BI-Tools
* Debuggen von Journey-Ausführungsproblemen
* Nachverfolgen des detaillierten Profilverhaltens
* Erstellen erweiterter Analyse- und Attributionsmodelle

Weitere Informationen zu [Journey-Schrittereignissen](../reports/sharing-overview.md).

+++

+++ Wie kann ich eine Fehlerbehebung bei einem Journey durchführen, der nicht erwartungsgemäß funktioniert?

Journey Optimizer bietet mehrere Ressourcen zur Fehlerbehebung:

* **Fehlerindikatoren**: Visuelle Warnhinweise auf der Journey-Arbeitsfläche zeigen Konfigurationsprobleme an
* **Testmodus**: Durchlaufen Sie die Journey, um Probleme zu identifizieren.
* **Dry Run Mode**: Testen Sie den Journey mit echten Produktionsdaten, ohne sich an Kunden zu wenden, um Zielgruppenbestimmung und Ausführung zu validieren
* **Journey-Berichte**: Überprüfen Sie die Ausführungsmetriken, um Engpässe oder Fehler zu finden
* **Journey-Schrittereignisse**: Analysieren Sie detaillierte Ausführungsdaten, um das Profilverhalten zu verstehen

**Häufige Probleme**:

* Falsch konfigurierte Ereignisse oder Zielgruppen
* Fehlende Datenquellenverbindungen
* Ungültige Ausdrücke in Bedingungen oder Personalisierung
* Zu kurze Zeitüberschreitungseinstellungen

Weitere Informationen zu [Fehlerbehebung bei Journey](troubleshooting.md).

+++

<!--
+++ What happens if an action fails in a journey?

When an action fails (e.g., API call timeout, message delivery error), the journey continues by default unless configured otherwise. You can define condition activities to handle failure scenarios, and errors are logged in journey reports and step events for monitoring.

**Best practice**: Set appropriate timeout values for external actions and define alternative paths for critical failure scenarios.

Learn more about [action responses](../action/action-response.md).

+++
-->

+++ Kann ich sehen, wer gerade auf meinem Journey ist?

Ja. Verwenden Sie den **Journey-Live** Bericht, um Folgendes anzuzeigen:

* Anzahl der Profile, die sich derzeit auf der Journey befinden
* Anzahl der Profile pro Aktivität
* Profile, die in den letzten 24 Stunden eingetreten sind
* Echtzeit-Ausführungsmetriken

Verwenden Sie zum Anzeigen einzelner Profile **Journey-Schrittereignisse** in Customer Journey Analytics oder fragen Sie die Schrittereignisdatensätze direkt ab.

Weitere Informationen zu [Journey-Live-Berichten](report-journey.md).

+++

+++ Warum werden meine Nachrichten nicht auf meinem Journey versendet?

**Häufige Gründe und Lösungen**:

* **Einverständnisprobleme**: Empfänger haben sich nicht für den Erhalt von Nachrichten angemeldet
Lösung: Einverständnisrichtlinien und Opt-in-Status überprüfen

* **Unterdrückungsliste**: E-Mail-Adressen befinden sich auf der Unterdrückungsliste
Lösung: Überprüfen Sie die Unterdrückungsliste auf Bounces oder Beschwerden

* **Ungültige Kontaktinformationen**: Fehlende oder falsch formatierte E-Mail-Adressen/Telefonnummern
Lösung: Validieren der Profildatenqualität

* **Journey nicht veröffentlicht**: Die Journey befindet sich noch im Entwurfsmodus
Lösung: Veröffentlichen Sie die Journey, um sie zu aktivieren

<!-- 
* **Message not approved**: Message content requires approval before sending
  Solution: Submit for approval or check approval status-->

* **Kanalkonfigurationsproblem**: E-Mail-/SMS-Konfiguration ist falsch
Lösung: Überprüfen der Kanalkonfigurationen und -authentifizierung

Weitere Informationen zu [Fehlerbehebung](troubleshooting.md) und [Einverständnisverwaltung](../action/consent.md).

+++

+++ Wie kann ich Nachrichten auf meinem Journey personalisieren?

Sie können Nachrichten mit dem **Personalisierungseditor** personalisieren:

**Verfügbare Personalisierungsdaten**:

* **Profilattribute**: Vorname, Nachname, E-Mail, benutzerdefinierte Felder
* **Ereignisdaten**: Kaufdetails, Browser-Verhalten, App-Aktivität
* **Kontextdaten**: Journey-Variablen, externe API-Daten
* **Zielgruppenzugehörigkeit**: Segmentqualifikationen
* **Berechnete Attribute**: Vorberechnete Werte

**Beispiel für Personalisierung**:

* „Hallo `{{profile.firstName}}`, vielen Dank für Ihren Kauf von `{{event.productName}}`&quot;
* „Je nach Treuestufe (`{{profile.loyaltyTier}}`) finden Sie hier ein Sonderangebot.“
* Dynamische Inhaltsbausteine, die sich je nach Kundenvorlieben ändern

Erhalten Sie mehr über [Personalisierung](../personalization/personalize.md). 

+++

+++ Kann ich je nach bevorzugtem Kanal verschiedene Nachrichten senden?

Ja. Verwenden Sie eine **[Aktivität Bedingung](condition-activity.md)**, um Profile basierend auf ihrem bevorzugten Kanal zu routen:

1. Fügen Sie eine [Aktivität vom Typ Bedingung](condition-activity.md) in Ihren Journey ein
2. Erstellen Sie einen Pfad für jeden Kanal, indem Sie das bevorzugte Kanalprofilattribut überprüfen (z. B. `profile.preferredChannel`)
3. Kanalspezifische Pfade konfigurieren:
   * **E-Mail-**: Fügen Sie eine [E-Mail-Aktion](../email/create-email.md) mit E-Mail-optimierten Inhalten hinzu
   * **SMS-Pfad**: Hinzufügen einer [SMS-Aktion](../sms/create-sms.md) mit knappem Messaging
   * **Push-Pfad**: Fügen Sie eine [Push-Benachrichtigungsaktion](../push/create-push.md) mit kurzen, umsetzbaren Inhalten hinzu
   * **In-App-Pfad**: Hinzufügen einer [In-App-Nachrichtenaktion](../in-app/create-in-app.md) für interaktive App-Benutzer
4. Fügen Sie einen Standardpfad für Profile ohne Voreinstellung hinzu und leiten Sie sie an Ihren primären Kanal weiter.

**Best Practices**:

* Stellen Sie sicher, dass Ihre Profildaten genaue Kanalvoreinstellungen enthalten
* Entwerfen Sie Inhalte, die für die Stärken und Einschränkungen jedes Kanals geeignet sind
* Verwenden [Kanaloberflächen](../configuration/channel-surfaces.md) zum Verwalten von Kanalkonfigurationen
* Testen aller Pfade, um einen ordnungsgemäßen Nachrichtenversand sicherzustellen

Erfahren Sie mehr über [Bedingungen](condition-activity.md), [Nachrichtenaktionen](journeys-message.md) und [Kanalauswahl](../channels/gs-channels.md).

+++

+++ Kann ich bestimmte Kunden von meinem Journey ausschließen?

Ja, es gibt mehrere Möglichkeiten, Kunden auszuschließen:

**Bei Journey-Eintrag**:

* Verwenden [Zielgruppendefinitionen](../audience/creating-a-segment-definition.md) mit Ausschlussregeln
* Hinzufügen [Einstiegsbedingungen](entry-management.md) die bestimmte Profile herausfiltern
* Konfigurieren Sie [auf Profilattributen basierende Beendigungskriterien](journey-properties.md) in Journey-Eigenschaften, um Profile basierend auf bestimmten Attributen automatisch auszuschließen

**Innerhalb der Journey**:

* Fügen Sie zu Beginn [&#x200B; Journey eine Aktivität &#x200B;](condition-activity.md)Bedingung“ hinzu, um unerwünschte Profile zu verlassen
* Prüfen auf Ausschlussattribute (z. B. VIP-Status, Testkonten)
* Identifizieren [&#x200B; auszuschließenden Profile mithilfe &#x200B;](audience-qualification-events.md)Zielgruppenqualifizierung“

**Beispielausschlussszenarien**:

* Kunden ausschließen, die kürzlich gekauft haben
* VIP-Kunden von Standard-Promotions ausschließen
* Mitarbeiter und Testkonten ausschließen
* Kunden in bestimmten Regionen ausschließen

+++

## Erweiterte Konzepte

+++ Was ist ein Journey-Namespace und warum ist er wichtig?

Ein **Namespace** ist ein Identitätstyp (z. B. E-Mail, ECID, Telefonnummer), der bestimmt, wie Profile in der Journey identifiziert werden. Der Namespace definiert, welche Kennung zum Abgleichen von Profilen verwendet wird, muss ereignisübergreifend konsistent sein und sich auf das Verhalten beim Eintritt und erneuten Eintritt von Journey auswirken.

**Best Practice**: Wählen Sie einen Namespace aus, mit dem Ihre Kundinnen und Kunden über alle Berührungspunkte hinweg zuverlässig identifiziert werden.

Weitere Informationen zu [Identity-Namespaces](../audience/get-started-identity.md).

+++

+++ Können Profile mehrmals auf denselben Journey zugreifen?

Ja, abhängig von den **Einstellungen für den erneuten Eintritt**:

* **Erneuten Eintritt erlauben**: Profile können die Journey mehrmals nach Abschluss aufrufen
* **Wartezeit bis zum erneuten Eintritt**: Legen Sie eine Mindestzeit zwischen den Journey-Einträgen (z. B. 7 Tage) fest.
* **Erneuten Eintritt bei Ereignis erzwingen**: Trigger einer neuen Journey-Instanz, auch wenn sich das Profil bereits auf der Journey befindet
* **Zusätzliche Kennung**: Verwenden Sie eine zusätzliche ID, damit Profile für verschiedene Entitäten (z. B. verschiedene Bestellungen, Buchungen oder Transaktionen) mehrmals auf die Journey zugreifen können, selbst wenn sie sich bereits auf der Journey befinden

**Best Practice**: Verwenden Sie Regeln für den erneuten Eintritt, um das Ermüden von Nachrichten zu verhindern und eine angemessene Geschwindigkeit sicherzustellen. Erwägen Sie die Verwendung zusätzlicher Kennungen für Transaktions-Journey, bei denen Profile mehrmals für verschiedene Transaktionen eingeben müssen.

Erfahren Sie mehr über [Eintragsverwaltung](entry-management.md) und [zusätzliche Kennungen](supplemental-identifier.md).

+++

+++ Was ist die Optimierung des Versandzeitpunkts?

**Sendezeitoptimierung (STO)** KI, um die beste Sendezeit für jedes einzelne Profil vorherzusagen und so Öffnungsraten und Interaktion zu maximieren. STO analysiert historische Interaktionsmuster, um zu bestimmen, wann jeder Empfänger mit der größten Wahrscheinlichkeit mit Ihrer Nachricht interagiert.

**Vorteile**:

* Verbesserte Öffnungs- und Klickraten
* Besseres Kundenerlebnis durch zeitlich optimal abgestimmte Nachrichten
* Reduzierte Abmelderaten

Weitere Informationen über [Sendezeitoptimierung](send-time-optimization.md).

+++

+++ Was sind Journey-Begrenzungsregeln?

**Journey-Begrenzung** Ermöglicht die Steuerung der Interaktion von Profilen mit Journeys, wodurch die Nachrichtenermüdung verhindert und ein optimales Kundenerlebnis sichergestellt wird:

* **Eintragsbegrenzung**: Begrenzt die Anzahl der Eintritte eines Profils in Journey innerhalb eines bestimmten Zeitraums.
* **Parallelitätsbegrenzung**: Begrenzt die Anzahl der Journey, in denen sich ein Profil gleichzeitig befinden kann

Sie können die maximale Anzahl von Einträgen oder die gleichzeitige Nutzung pro Profil für Journey oder bestimmte Journey festlegen, Zeitfenster (täglich, wöchentlich, monatlich) definieren und Journey priorisieren, wenn mehrere Journey um dasselbe Profil konkurrieren.

Weitere Informationen zur [Journey-Begrenzung](../conflict-prioritization/journey-capping.md).

+++

+++ Kann ich meinen Journey mit externen Systemen integrieren?

Ja. Verwenden Sie **benutzerspezifische Aktionen** um APIs von Drittanbietern (CRM, Marketing-Automatisierung, Treueprogramm-Systeme) aufzurufen, Daten an externe Systeme zu senden, Echtzeit-Informationen für Entscheidungen abzurufen und Trigger-Workflows in externen Plattformen zu erstellen.

Benutzerdefinierte Aktionen unterstützen die Authentifizierung (API-Schlüssel, benutzerdefinierte Authentifizierung), die Anpassung der Anfrage-/Antwort-Payload, die Fehlerbehandlung und Zeitüberschreitungen sowie dynamische Parameter aus dem Journey-Kontext.

Weitere Informationen über [benutzerdefinierte Aktionen](using-custom-actions.md).

+++

+++ Wie kann ich Adobe Campaign mit Journey verwenden?

Journey Optimizer lässt sich nativ mit Adobe Campaign integrieren, um seine erweiterten Funktionen zu nutzen:

* **Adobe Campaign Standard**: Verwenden Sie Campaign Standard-Aktionen, um Transaktionsnachrichten zu senden
* **Adobe Campaign v7/v8**: Trigger-Campaign-Workflows und Verwendung der Versandinfrastruktur von Campaign

**Best Practice**: Verwenden Sie diese Integration, wenn Sie bereits über Campaign-Vorlagen und -Datenmodelle verfügen oder Campaign-spezifische Funktionen benötigen.

Weitere Informationen zur [Campaign-Integration](ajo-ac.md).

+++

+++ Was ist die Sprungaktivität?

Die **Sprungaktivität** ermöglicht den Übergang von Profilen von einer Journey auf eine andere und ermöglicht wiederverwendbare Journey-Muster, die Journey-Orchestrierung über mehrere Journey hinweg, eine vereinfachte Journey-Wartung und progressive Interaktionsstrategien.

Wenn ein Profil eine Sprungaktivität erreicht, verlässt es die aktuelle Journey und gelangt an ihrem Startpunkt auf die Ziel-Journey.

Weitere Informationen über [Sprungaktivität](jump.md).

+++

+++ Wie erstelle ich eine Welcome Series Journey?

Eine typische Begrüßungsserie umfasst mehrere Touchpoints über mehrere Tage:

**Beispielstruktur**:

1. **Eintritt**: Zielgruppe neuer Abonnenten oder Ereignis, wenn sich jemand anmeldet
2. **E-Mail 1 - Sofort willkommen**: Vielen Dank und Einführung
3. **Warten**: 2 Tage
4. **E-Mail 2 - Erste Schritte**: Tutorial oder Produkthandbuch
5. **Warten**: 3 Tage
6. **Bedingung**: Hat der Kunde einen Kauf getätigt?
   * **Ja**: Beenden oder Umstieg auf Kunden-Journey
   * **Nein**: Begrüßungsserie fortsetzen
7. **E-Mail 3 - Incentive**: Spezieller Erstkäufer-Rabatt
8. **Warten**: 5 Tage
9. **E-Mail 4 - Interaktion**: Bestseller oder beliebte Inhalte

**Best Practices**:

* Beibehaltung von 3-5 E-Mails über 2-3 Wochen
* Jede E-Mail sollte einen klaren Zweck haben und call-to-action enthalten
* Öffnungsraten überwachen und Timing/Inhalt entsprechend anpassen
* Beenden Sie Kunden frühzeitig, wenn sie konvertieren oder tief interagieren

Weitere Informationen zu [Journey-Anwendungsfällen](jo-use-cases.md).

+++

+++ Kann ich auf meinem Journey verschiedene A/B-Pfade testen?

Ja. Verwenden Sie die Aktivität **Optimieren** (eingeschränkte Verfügbarkeit) oder erstellen Sie manuell Testaufteilungen:

**Verwenden der Aktivität „Optimieren** mit der Experiment-Methode:

* Teilt den Traffic zufällig auf verschiedene Pfade auf, um zu bestimmen, welcher am besten funktioniert
* Testet verschiedene Nachrichten, Angebote, Wartezeiten oder ganze Journey-Pfade
* Misst die Leistung anhand vordefinierter Erfolgsmetriken und gibt einen Gewinner aus

**Verwenden der Aktivität &quot;**&quot; mit der Bedingungsmethode „Datenquelle“:

* Erstellen einer Bedingung, die Profile nach dem Zufallsprinzip aufteilt (z. B. mithilfe einer Zufallszahlenfunktion)
* An jede Teilung unterschiedliche Erlebnisse senden
* Messen von Ergebnissen mithilfe von Journey-Berichten

**Was Sie testen können**:

* Unterschiedliche E-Mail-Betreffzeilen
* Alternativer Nachrichteninhalt
* Unterschiedliche Wartezeiten
* Verschiedene Angebote oder Incentives
* Ganz andere Journey-Pfade

Erfahren Sie mehr über [Aktivität optimieren](optimize.md) und [Inhaltsexperimente](../content-management/content-experiment.md).

+++

+++ Wie kann ich eine Journey in Trigger nehmen, wenn der Bestand niedrig ist?

Erstellen Sie eine **Geschäftsereignis-Journey**:

1. **Geschäftsereignis konfigurieren**: Richten Sie ein Ereignis ein, das von Ihrem Inventarsystem ausgelöst wird, wenn der Bestand unter einen Schwellenwert fällt
2. **Zielgruppe auswählen**: Wählen Sie Profile aus, die benachrichtigt werden sollen (z. B. Kunden, die das Produkt angesehen haben, Abonnenten, um Warnhinweise wiederzubeleben).
3. **Aktion „Nachricht hinzufügen**: E-Mail oder Push-Benachrichtigung senden
4. **Inhalt personalisieren**: Produktdetails, aktuelle Inventarebene, Dringlichkeitsnachrichten einschließen

**Beispiel für Geschäftsereignisse**:

* Warnhinweis bei niedrigem Bestand
* Benachrichtigung bezüglich Preisverfall
* Produkt wieder auf Lager
* Flash-Verkaufsankündigung
* Wetterbasierte Angebote

Weitere Informationen zu [Geschäftsereignissen](general-events.md).

+++

+++ Was sind Zusammenführungsrichtlinien und wie wirken sie sich auf Journey aus?

**Zusammenführungsrichtlinien** bestimmen, wie Adobe Experience Platform Daten aus mehreren Quellen kombiniert, um eine einheitliche Profilansicht zu erstellen. Sie definieren Regeln für die Datenpriorisierung und Identitätszuordnung, wenn Profilfragmente in verschiedenen Datensätzen vorhanden sind.

**Auswirkungen auf Journey**:

* Journey verwenden die mit der Zielgruppe oder dem Ereignis verknüpfte Zusammenführungsrichtlinie, um zu bestimmen, welche Profildaten verfügbar sind
   * In den Journeys „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ wird die Zusammenführungsrichtlinie aus der Zielgruppe verwendet
   * In Journeys für unitäre Ereignisse wird die standardmäßige Zusammenführungsrichtlinie verwendet
   * In Journeys für Geschäftsereignisse wird die Zusammenführungsrichtlinie aus der Zielgruppe in der Aktivität „Zielgruppe lesen“ verwendet.

* Die Zusammenführungsrichtlinie wirkt sich darauf aus, auf welche Attribute in Journey-Bedingungen, Personalisierung und Aktionen zugegriffen werden kann
* Verschiedene Zusammenführungsrichtlinien können dazu führen, dass unterschiedliche Profildaten auf der Journey verwendet werden

**Best Practices**:

* Stellen Sie sicher, dass die von Ihrem Journey verwendete Zusammenführungsrichtlinie mit Ihren Data Governance-Anforderungen übereinstimmt
* Erfahren Sie, welche Datensätze in Ihrer Zusammenführungsrichtlinie enthalten sind, um zu wissen, welche Daten verfügbar sind
* Verwenden konsistenter Zusammenführungsrichtlinien für verwandte Zielgruppen und Journey für vorhersehbare Ergebnisse

Weitere Informationen zu [Zusammenführungsrichtlinien](../audience/get-started-profiles.md) und [Identitätsverwaltung](../audience/get-started-identity.md).

+++

+++ Was ist der Unterschied zwischen einer Bedingung und einer Warteaktivität?

| | **Bedingungsaktivität** | **Warteaktivität** |
|---|---|---|
| **Zweck** | Erstellt verschiedene Pfade basierend auf der Logik (if/then) | Hält die Journey für einen bestimmten Zeitraum an |
| **Funktion** | Wertet Daten aus und leitet Profile entsprechend weiter | Profile werden an einem bestimmten Punkt gespeichert, bevor der Vorgang fortgesetzt wird |
| **Anwendungsfall** | Segmentieren von Kunden, Überprüfen des Status, Verzweigung basierend auf dem Verhalten | Timing zwischen Nachrichten, Warten auf Geschäftszeiten, Verzögerungen verursachen |
| **Beispiel** | Wenn der Kunde VIP ist, senden Sie ein Premium-Angebot; andernfalls senden Sie ein Standardangebot. | 3 Tage nach der Begrüßungs-E-Mail warten, bevor die nächste Nachricht gesendet wird |

**Sie arbeiten zusammen**:

* Warten Sie einen Zeitraum und überprüfen Sie dann mithilfe einer Bedingung, ob während des Wartens etwas passiert ist
* Beispiel: 7 Tage warten und dann überprüfen, ob der Kunde einen Kauf getätigt hat

Weitere Informationen zu [Bedingungen](condition-activity.md) und [Warteaktivitäten](wait-activity.md).

+++

## Best Practices und Einschränkungen

+++ Was sind die wichtigsten Einschränkungen, die ich beachten sollte?

Zu den wichtigen Leitplanken gehören:

* **Journey-Komplexität**: Maximale Aktivitäten, Pfade und Verschachtelungsebenen
* **Durchsatz**: Nachrichtenübertragungsraten und API-Aufrufbeschränkungen
* **Time-to-Live**: Maximale Journey-Dauer (z. B. 91 Tage)
* **Zielgruppengröße**: Beschränkungen für die Größe von gelesenen Zielgruppen-Batches
* **Ausdruckskomplexität**: Zeichenbeschränkungen in Bedingungen und Personalisierung

Vollständige Ansicht [Leitplanken und &#x200B;](../start/guardrails.md))

+++

+++ Was sind die Best Practices für das Journey-Design?

**Struktur und**:

* Konzentrieren der Journey auf bestimmte Anwendungsfälle
* Beschreibende Benennung für Aktivitäten verwenden
* Hinzufügen von Beschreibungen und Beschriftungen für komplexe Logik
* Gruppieren verwandter Journey mit Tags

**Performance**:

* Optimieren Sie Wartezeiten, um Interaktion und Volumen auszugleichen
* Beschränken von externen API-Aufrufen auf wichtige Anwendungsfälle
* Verwenden von Begrenzungsregeln, um das Ermüden von Nachrichten zu verhindern
* Journey-Metriken regelmäßig überwachen

**Testen**:

* Journey vor der Veröffentlichung immer testen
* Testmodus verwenden, um die Journey-Logik zu validieren und das Journey schrittweise durchzuführen
* Verwenden Sie den Dry-Run-Modus, um mit echten Produktionsdaten zu testen, ohne Kunden zu kontaktieren
* Alle bedingten Pfade und Szenarien testen
* Verwenden realistischer Testprofile
* Validieren von Personalisierung und dynamischen Inhalten

**Wartung**:

* Regelmäßige Überprüfung der Journey-Performance
* Nicht verwendete Journey stoppen oder schließen
* Journey-Logik und Geschäftsregeln dokumentieren
* Planen der Journey-Versionierung

Erfahren Sie mehr über die Best Practices für das [Journey-Design](using-the-journey-designer.md).

+++

+++ Wie viele Aktivitäten kann ich einer Journey hinzufügen?

Journey sind auf maximal 50 Aktivitäten beschränkt. Es wird jedoch empfohlen, die Journey einfacher zu halten, um eine bessere Wartung und Leistung zu erzielen.

Wenn sich Journey 50 Aktivitäten nähern, können sie sehr komplex und schwierig zu verwalten, zu beheben und zu verstehen werden. Große Journey mit vielen Verzweigungen und Bedingungen können sich auch auf die Verarbeitungszeit, die Lesbarkeit und die Team-Zusammenarbeit auswirken.

**Best Practice**: Halten Sie Ihre Journey fokussiert und verwaltbar. Wenn Ihr Journey immer komplexer wird, sollten Sie Folgendes berücksichtigen:

* Unterteilen in mehrere Journey mithilfe der Sprungaktivität
* Erstellen wiederverwendbarer Muster in einfacheren Journey
* Vereinfachung der Logik mit effizienteren Bedingungen
* Überprüfen, ob alle Aktivitäten erforderlich sind

Erfahren Sie mehr über das [Journey](using-the-journey-designer.md)Design und [Leitplanken und Einschränkungen](../start/guardrails.md).

+++

+++ Wie stelle ich sicher, dass mein Journey im großen Maßstab eine gute Leistung erzielt?

**Überlegungen zum Design**:

* Verwenden [zielgruppenbasierten Eintrags](read-audience.md) für Batch-Nachrichten anstelle von einzelnen Ereignissen
* Angemessene Wartezeiten [, um &#x200B;](wait-activity.md) Nachrichtenvolumen zu verteilen
* Nutzen Sie [Begrenzungsregeln](../conflict-prioritization/journey-capping.md) um eine Systemüberlastung zu vermeiden
* Optimieren [Bedingungslogik](condition-activity.md) um die Verarbeitungskomplexität zu reduzieren

**Überwachung**:

* [Journey-Metriken nachverfolgen](report-journey.md) regelmäßig
* Überwachen der API-Leistung für [benutzerdefinierte Aktionen](using-custom-actions.md)
* Überprüfen der Fehlerquoten und Zeitüberschreitungsereignisse mit [Tools zur Fehlerbehebung](troubleshooting.md)
* [Journey-Warnhinweise abonnieren](../reports/alerts.md) kritische Journey-Fehler

**Optimierung**:

* Verwenden Sie [Testmodus](testing-the-journey.md) und [Probelauf](journey-dry-run.md), um die Leistung vor der Veröffentlichung zu überprüfen
* Minimieren Sie externe API-Aufrufe durch [benutzerdefinierte Aktionen](using-custom-actions.md) um Latenz und Abhängigkeit von Drittanbietersystemen zu vermeiden
* Häufig verwendete Daten in Adobe Experience Platform mit [Datensatzsuche“ speichern](dataset-lookup.md) anstatt nach Möglichkeit externe Aufrufe durchzuführen
* Überprüfen und Optimieren [Nachrichtenversand](journeys-message.md) Leistung

Weitere Informationen zu [Leitplanken und Einschränkungen](../start/guardrails.md).

+++

## Weitere Ressourcen

Detailliertere Informationen und Updates finden Sie in den folgenden Ressourcen:

* [Erste Schritte mit Journeys](journey.md)
* [Erstellen Ihrer ersten Journey](journey-gs.md)
* [Handbücher zur Fehlerbehebung](troubleshooting.md)
* [Journey-Anwendungsfälle](jo-use-cases.md)
* [Produktbeschreibung zu Journey Optimizer](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
