---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei Live-Aktivitäten
description: Erfahren Sie, wie Sie Live-Aktivitäten in Journey Optimizer für einzelne und Broadcast-Anwendungsfälle beheben können, einschließlich Problemen mit Profil-Token, Kampagnenkonfiguration und Versandfehlern
role: User
level: Intermediate
source-git-commit: b71dbb0e4987cfc879a7b153d5c1453d6c220bf9
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 1%

---


# Fehlerbehebung bei Live-Aktivitäten {#troubleshoot-mobile-live}

Live-Aktivitäten in Adobe Journey Optimizer ermöglichen dynamische Echtzeit-Updates auf iOS-Sperrbildschirmen und Dynamic Islands. Sie können nur über API-ausgelöste Kampagnen ausgelöst und verwaltet werden.

**Anwendungsfalltypen:**

* **Unitär**: Individuell zielgerichtet, transaktional (API-ausgelöste Transaktionskampagnen)
* **Broadcast**: Zielgruppen-bezogener Versand in großen Mengen (API-ausgelöste Marketing-Kampagnen)

Eine häufige Herausforderung bei Live-Aktivitäten besteht darin, dass der API-Aufruf an den Trigger oder die Aktualisierung einer Live-Aktivität eine **Erfolgreiche Antwort (200 OK) zurückgibt** die Live-Aktivität jedoch nicht auf dem Gerät des Benutzers angezeigt oder aktualisiert wird. Diese Trennung zwischen API-Bestätigung und tatsächlichem Geräteverhalten kann an mehreren Punkten in der Bereitstellungs-Pipeline auftreten. Dieses Handbuch bietet einen systematischen Ansatz zur Fehlerbehebung, um festzustellen, wo der Versand fehlschlägt, und um jede Phase von der Validierung der API-Anfrage bis zum Geräte-Rendering zu untersuchen.

## Voraussetzungen

Stellen Sie vor der Fehlerbehebung Folgendes sicher:

* 
  +++ Einrichten einer Assurance-Sitzung

  Richten Sie eine **Assurance-** ein, um SDK-Ereignisse zu erfassen und die Bereitstellungs-Pipeline zu überprüfen. Assurance bietet Einblicke in:

   * Edge Network-Anfragen und -Antworten
   * Profilqualifikationsereignisse
   * Push-Token-Registrierung
   * Live-Aktivitäts-Lebenszyklus-Ereignisse

  Wie Sie Assurance einrichten, erfahren Sie in der Dokumentation zu [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance).

  **Hinweis**: Stellen Sie für iOS Live-Aktivitäten sicher, dass Ihre App auf einem physischen iOS-Gerät (iOS 16.1 oder höher) oder Xcode-Simulator (iOS 16.1 oder höher) ausgeführt wird.

  +++

* 
  +++ Erfassen von Details zur API-ausgelösten Kampagne

  Navigieren Sie zu Ihrer API-ausgelösten Kampagne in Journey Optimizer und rufen Sie Folgendes ab:

   * Kampagnenname
   * In der URL oder den Kampagneneigenschaften gefundene Kampagnen-ID
   * Campaign-Version, falls zutreffend
   * Oberflächenkonfiguration, für die Live-Aktivität verwendete iOS-App-Oberfläche

  +++

* 
  +++ Erfassen von API-Anfrageinformationen

  Speichern Sie beim API-Aufruf an den Trigger die Live-Aktivität:

   * Payload der API-Anfrage, einschließlich Profilkennungen und Live-Aktivitätsdaten
   * API-Antwort einschließlich Status-Code, Nachrichten-ID, Anfrage-ID
   * Zeitstempel, der angibt, wann die API aufgerufen wurde
   * Verwendeter Endpunkt, z. B. `/campaign/{CAMPAIGN_ID}/execute`

  +++

* 
  +++ Testprofil identifizieren

  Aus Ihrer API-Anfrage können Sie Folgendes abrufen:

   * Profil-Namespace, z. B. ECID, E-Mail, Kunden-ID
   * Im API-Aufruf verwendete Profil-ID

  Stellen Sie sicher, dass Sie dieses Profil in Adobe Experience Platform nachschlagen können. Erfahren Sie in [ Dokumentation zu Experience Platform, wie Sie ein Profil ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html).

  +++

* 
  +++ Geräte- und App-Informationen

  Erfassen Sie Folgendes auf Ihrem Testgerät:

   * Gerätemodell, z. B. iPhone 14 Pro
   * iOS-Version
   * App-Bundle-Kennung
   * Push-Token für APNs
   * Status der Netzwerkverbindung zum Zeitpunkt der Tests

  +++

## Häufige Szenarien

### Probleme mit Profil- oder Push-Token {#profile-issue}

[!BADGE Gilt für einzelne und Broadcast-Anwendungsfälle]{type=Positive}

Die API gibt HTTP 200 zurück, aber die Live-Aktivität wird nicht angezeigt. Häufige Ursachen:

* Profil ist in Adobe Experience Platform nicht vorhanden.
* Live Activity Push Token wurde nicht mit dem Profil synchronisiert.
* Live-Aktivitäts-Push-Details werden synchronisiert, enthalten jedoch eine falsche Konfiguration, z. B. falsche `appId` oder `attributeType`.

**Hinweis für Broadcast-Anwendungsfälle**: Wenn einigen Profilen in Ihrer Zielgruppe Token fehlen, können nur diese Profile die Live-Aktivität nicht empfangen. Probieren Sie mehrere Profile aus Ihrer Zielgruppe aus, um Token-Probleme zu diagnostizieren. Dies gilt nur für Remote-Startereignisse, nicht für Update- oder End-Ereignisse.

#### Vorab-Prüfungen

* Voraussetzungen für das iOS-Programm:
   * iOS 16.1+
   * `NSSupportsLiveActivities` in `YES` auf `Info.plist` gesetzt
   * `ActivityAttributes` ordnungsgemäß implementiert.
* Mobile SDK-Integration:
   * Adobe Experience Platform Mobile SDK (Messaging SDK 5.11.0+)
   * `Messaging.registerLiveActivities` implementiert und mit dem Live Activity Push-Token aufgerufen.

#### Debugging-Schritte

1. 
   +++ Überprüfen, ob das Profil in Adobe Experience Platform vorhanden ist

   1. Navigieren Sie in Journey Optimizer zu **Kunde** `>` **Profile**.
   1. Suchen Sie mithilfe des Namespace und des Identitätswerts aus der API-Anfrage.
   1. Wenn das Profil nicht gefunden wird, existiert das Profil nicht oder die Aufnahme wurde nicht abgeschlossen. Erstellen Sie das Profil oder warten Sie auf die Aufnahme, bevor Sie die Live-Aktivität auslösen.
   1. Wenn ein Profil gefunden wird, fahren Sie mit Schritt 2 unten fort, um zu überprüfen, ob das Push-Token synchronisiert ist.

      +++

1. 
   +++ Überprüfen, ob das Push-Token der Live-Aktivität synchronisiert ist

   Sie können Assurance verwenden, um die Token-Registrierung zu überprüfen:

   1. Filtern Sie in Assurance über die **Ereignisse**-Liste oder suchen Sie `eventType = "liveActivity.pushToStart"` nach Ereignissen.
   1. Wählen Sie **Ereignis** aus und überprüfen Sie die Payload.
   1. Überprüfen Sie, ob die Werte für Token, appId und attributeType vorhanden sind.
   1. Bestätigen, ob das Ereignis erfolgreich gesendet wurde.

   Sie können auch das Adobe Experience Platform-Profil einchecken.

   1. Rufen Sie in Adobe Experience Platform über Ihr **Profil** die Registerkarte **Ereignisse** auf.
   1. Nach `liveActivity.pushToStart` Ereignissen suchen.
   1. Überprüfen Sie den Zeitstempel und die Payload des Ereignisses.

   Wenn keine Ereignisse gefunden werden, ruft Ihre Mobile App `Messaging.registerLiveActivity` nicht korrekt auf. Sie müssen die SDK-Integration korrigieren.

   +++

1. 
   +++ Token-Details im Profil validieren

   1. Rufen Sie von **Profil** aus die Registerkarte **Attribute** auf.
   1. Suchen Sie `liveActivityPushNotificationDetails`.
   1. Überprüfen Sie die Token-Konfiguration:

      ```json
      {
        "liveActivityPushNotificationDetails": [
          {
            "appId": "com.example.myapp",
            "token": "abc123def456...",
            "platform": "apns",
            "denylisted": false,
            "attributeType": "OrderTrackingAttributes",
            "identity": {}
          }
        ]
      }
      ```

   **Validieren jedes Felds:**

   | Feld | Anforderung | Häufige Probleme |
   |-|-|-|
   | `appId` | Muss genau mit der iOS-Bundle-Kennung übereinstimmen | Unstimmigkeit zwischen Entwicklungs-/Produktions-Paket-IDs |
   | `attributeType` | Muss genau mit dem Namen der Swift-`ActivityAttributes`-Struktur übereinstimmen (Groß-/Kleinschreibung beachten) | Tippfehler oder falscher Strukturname |
   | `platform` | Muss `"apns"` oder `"apnsSandbox"` sein | Falscher Plattformwert |
   | `denylisted` | Muss `false` sein | Token als ungültig markiert oder Benutzer hat sich abgemeldet |
   | `token` | Gültiges APNs-Push-Token | Token abgelaufen oder App neu installiert |

   Wenn ein Feld falsch ist: Aktualisieren Sie die Mobile App, registrieren Sie sich erneut mit `Messaging.registerLiveActivities`, warten Sie 5-10 Minuten und überprüfen Sie dann erneut.

   Wenn `liveActivityPushNotificationDetails` fehlt: Token wurde noch nicht synchronisiert. Warten Sie 5-10 Minuten, nachdem Sie das `liveActivity.pushToStart` Ereignis in Assurance gesehen haben.

   +++

### Probleme mit der Kampagnenkonfiguration und der Payload {#payload-issues}

[!BADGE Gilt für einzelne und Broadcast-Anwendungsfälle]{type=Positive}

Profil ist mit gültigen Token vorhanden, aber die Live-Aktivität wird nicht angezeigt. Dies kann folgende Ursachen haben:

* Falsche Oberflächen- oder Kanalkonfiguration.
* Falsche API-Payload-Struktur.
* `content-state` und `attributes` stimmen nicht mit der Implementierung der iOS-`ActivityAttributes` überein.
* Veraltete `timestamp` (wichtig für Aktualisierung/Ende).

**Hinweis für Broadcast-Anwendungsfälle**: Die Kampagne muss **API-ausgelöstes Marketing** (keine Transaktion) sein. Payload verwendet `audience` anstelle von einzelnen `profile`. Vollständige API[Spezifikationen finden Sie in diesem ](#broadcast-config) für die Broadcast-spezifische Payload-Struktur und in der [](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution) Dokumentation zu Adobe Developer.

#### Vorab-Prüfungen

* Campaign ist **API-ausgelöste Transaktion** (unitäres) oder **API-ausgelöstes Marketing** (Broadcast) und **Hoher Durchsatz** Option muss **nicht** aktiviert sein, da sie mit Live-Aktivität nicht kompatibel ist.
* Stellen Sie sicher, dass das Profil vorhanden ist und Token mit dem [ Szenario korrekt synchronisiert ](#profile-issue).

#### Debugging-Schritte

1. 
   +++ Konfiguration der Kampagnenoberfläche überprüfen

   1. Öffnen Sie in Journey Optimizer Ihre **Kampagne** und navigieren Sie zum Menü **Aktionen** .
   1. Überprüfen Sie Ihre **Konfiguration der Live-Aktivität**. Die Oberfläche muss für die iOS-App mit einer Bundle-Kennung konfiguriert werden, die mit der `appId` in der `liveActivityPushNotificationDetails` Ihres Profils übereinstimmt. Wenn Ihr Profil beispielsweise über `"appId": "com.example.myapp"` verfügt, muss die Oberfläche dieselbe App ansprechen.
   1. Vergewissern Sie sich **dass der** Aktivitätstyp“ in Ihrer Kampagnenkonfiguration genau mit dem `attributeType` in der `liveActivityPushNotificationDetails` Ihres Profils übereinstimmt. Wenn Ihr Profil beispielsweise über `"attributeType": "FoodDeliveryLiveActivityAttributes"` verfügt, muss die Kampagne denselben Aktivitätstyp angeben.

      +++

1. 
   +++Validieren der API-Payload-Struktur

   Stellen Sie beim Ausführen der Kampagne über die API sicher, dass die Payload der richtigen Struktur entspricht.

   **Unitäre Payload:**

   ```json
   {
     "campaignId": "your-campaign-id",
     "recipients": [{
       "type": "aep",
       "userId": "user@example.com",
       "namespace": "email",
       "context": {
         "requestPayload": {
           "aps": {
             "content-available": 1,
             "timestamp": 1756984054,
             "event": "start",
             "attributes-type": "FoodDeliveryLiveActivityAttributes",
             "content-state": { ... },
             "attributes": { ... }
           }
         }
       }
     }]
   }
   ```

   **Häufige Payload-Probleme:**

   | Feld | Anforderung | Häufige Probleme |
   |-|-|-|
   | `attributes-type` | Muss mit dem Kampagnenaktivitätstyp und der `attributeType` übereinstimmen | Fehlende Übereinstimmung oder Tippfehler |
   | `campaignId` | Muss mit der aktivierten Kampagnen-ID übereinstimmen | Falsche oder fehlende Kampagnen-ID |
   | `content-available` | Muss `1` sein | Fehlender oder falscher Wert |
   | `event` | Muss `"start"`, `"update"` oder `"end"` sein | Ungültiger Ereignistyp |
   | `timestamp` | Muss immer die aktuelle/neueste Unix-Epochenzeit in Sekunden sein | Verwenden eines alten/zwischengespeicherten Zeitstempels |
   | `userId` / `namespace` | Muss mit einem vorhandenen Profil in AEP übereinstimmen | Profilkennung stimmt nicht überein |

   **Kritisch: Verwenden Sie immer den neuesten Zeitstempel**

   * Das `timestamp` Feld muss **immer** zum Zeitpunkt **jeden API-Aufrufs die** aktuelle Unix-Epochenzeit) in Sekunden) sein.
   * Dies gilt für **alle Ereignistypen**: `start`, `update` und **insbesondere`end`**.
   * **Auswirkungen auf Updates/**: Die Verwendung eines veralteten oder alten Zeitstempels führt dazu, dass Update- und End-Anfragen fehlschlagen oder vom Gerät ignoriert werden.
   * Verwenden **KEINE** Zeitstempel aus früheren Anfragen wieder oder verwenden Sie zwischengespeicherte Werte.
   * Generieren Sie für jeden API-Aufruf einen neuen Zeitstempel.

   **Optionale Felder (alle Ereignistypen):**

   * `requestId`: Eindeutige Kennung für das Tracking (empfohlen).
   * `alert`: Objekt mit `title` und `body` für Benachrichtigungen (nützlich, um auf Aktualisierungen hinzuweisen).

   **Über `dismissal-date`:**

   * Optionales Feld mit Unix-Epochenzeit (Sekunden).
   * **Nur relevant, wenn`event: "end"`**.
   * Gibt an, wann die Live-Aktivität automatisch vom Gerät entfernt werden soll.
   * Wird die Live-Aktivität nicht im Endereignis angegeben, bleibt sie sichtbar, bis sie vom Benutzer geschlossen wird.
   * Muss ein zukünftiger Zeitstempel sein (nach `timestamp`).

     +++

1. 
   +++ Payload an iOS-Implementierung anpassen

   Stellen Sie sicher, dass Ihre API-Payload mit der `ActivityAttributes` Implementierung Ihrer iOS-App übereinstimmt. Das `LiveActivityAttributes`-Protokoll von Adobe SDK erweitert iOS `ActivityAttributes` und erfordert eine `liveActivityData`.

   **Validieren der Zuordnung:**

   1. Ihr `ActivityAttributes` muss das `LiveActivityAttributes`-Protokoll von Adobe implementieren. Beispiel:

      ```swift
      struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
       public struct ContentState: Codable, Hashable {
           var orderStatus: String
           var estimatedDeliveryTime: String
       }
      
       // Adobe SDK requirement
       var liveActivityData: LiveActivityData
      
       // Your custom attributes
       var restaurantName: String
      }
      ```

      **Hinweis** dass das Feld `liveActivityData` für Adobe SDK erforderlich ist und in allen Implementierungen enthalten sein muss.

   1. Ihre API-Payload muss die iOS-Struktur widerspiegeln:

      ```json
      {
        "aps": {
           "event": "start",
           "timestamp": 1756984054,
           "attributes-type": "FoodDeliveryLiveActivityAttributes",
           "content-state": {
           "orderStatus": "Preparing",
           "estimatedDeliveryTime": "20 mins"
        },
        "attributes": {
          "liveActivityData": {
            "liveActivityID": "order-12345"
          },
          "restaurantName": "Pizza Palace"
        }
        }
      }
      ```

   **Validierungs-Checkliste:**

   * Alle `ContentState` Felder in `content-state` einbeziehen (für alle Ereignistypen erforderlich).
   * Alle `LiveActivityAttributes` Felder in `attributes` einbeziehen (nur Startereignisse), einschließlich:
      * `liveActivityData` (erforderlich; enthält normalerweise `liveActivityID` oder eine ähnliche Kennung)
      * Alle benutzerdefinierten Felder aus Ihrer Struktur
   * Exakte Übereinstimmung der Feldnamen (unter Berücksichtigung von Groß- und Kleinschreibung)
   * Übereinstimmende Datentypen (String, Int, bool, verschachtelte Objekte).
   * Verschachtelte Objektstruktur beibehalten.

   **Häufige Fehler:**

   | Problem | Wirkung | Fehlerbehebung |
   |-------|--------|-----|
   | Fehlende `liveActivityData` in Attributen | Live-Aktivität wird nicht gestartet | `liveActivityData` Objekt immer in Startereignis einschließen |
   | Erforderliches Feld im Startereignis fehlt | Live-Aktivität wird nicht gestartet | Alle Felder aus der iOS-Struktur hinzufügen |
   | Falscher Feldname (Tippfehler/Groß-/Kleinschreibung) | Feld ignoriert oder Parsing-Fehler | Exakte Übereinstimmung mit iOS-Feldnamen |
   | Falscher Datentyp | Parsen des Fehlers | IOS-Datentypen abgleichen |
   | Verschachteltes Objekt fehlt | Unvollständige Daten | Alle verschachtelten Strukturen einschließen |
   | Einschließen von `attributes` in Aktualisierung/Ende | Unnötig, aber normalerweise ignoriert | Nur `attributes` in Startereignis einbeziehen |
   | Veralteter Zeitstempel bei Aktualisierung/Ende | Update/Ende vom Gerät ignoriert | Immer neuen Zeitstempel erzeugen |

   Weitere Beispiele finden Sie auf [ Seite „Live-Aktivität erstellen](create-mobile-live.md).

   +++

1. 
   +++ Testen mit Assurance

   Überprüfen der API-Ausführung und der Payload-Bereitstellung mithilfe von Assurance:

   1. Öffnen Sie Ihre Assurance-Sitzung.
   1. Ausführen des API-Aufrufs zum Trigger der Live-Aktivität.
   1. Prüfen Sie **der**-Liste nach:
      * Ausführungsereignisse der Kampagne.
      * Versandereignisse für Live-Aktivitäten.
      * Payload-Validierungsfehler-Ereignisse.
   1. Überprüfen Sie Ereignis-Payloads zur Überprüfung:
      * Payload wurde korrekt verarbeitet.
      * Keine Validierungsfehler aufgetreten.
      * Live-Aktivität wurde an APNs gesendet.

      +++

### Fehlgeschlagene Sendungen und Fehleranalyse

[!BADGE Gilt für einzelne und Broadcast-Anwendungsfälle]{type=Positive}

In diesem Szenario wurden alle vorherigen Prüfungen bestanden:

* Profil existiert mit [gültigen Push-Token für Live-Aktivität](#profile-issue)
* Campaign ist korrekt [mit der richtigen Payload konfiguriert](#payload-issues)
* [Aktualisierungs-Token werden synchronisiert](#token-not-synced) (nur für Update-/End-Ereignisse, unitäre Anwendungsfälle)

Die Live-Aktivität wird jedoch weiterhin nicht wie erwartet angezeigt, aktualisiert oder beendet. Das Problem kann auf der Ebene des Adobe-Bereitstellungssystems oder beim Push-Benachrichtigungs-Service-Provider (APNs) auftreten.

**Hinweis für Broadcast-Anwendungsfälle**: Berichte zeigen Metriken über alle Zielgruppenmitglieder hinweg an. Einige Profile sind möglicherweise erfolgreich, während andere fehlschlagen.

**Vorab-Prüfungen**

* **Vorherige validierte Szenarien:**
   * Profil existiert mit korrektem `liveActivityPushNotificationDetails`
   * Kampagnenoberfläche und Aktivitätstyp sind korrekt
   * API-Payload ist mit aktuellem Zeitstempel gültig
   * Update-Token werden synchronisiert (für Update-/End-Ereignisse)

* **API-Aufruf bestätigt:**

   * Der API-Aufruf hat HTTP 200 zurückgegeben (Erfolg)
   * Kampagnen-ID und Empfängerdetails sind korrekt

#### Debugging-Schritte

1. 
   +++ Kampagnenberichte überprüfen

   1. Navigieren Sie zu Ihrer **Live-Aktivitätskampagne**.
   1. Klicken Sie auf die **Berichte**.
   1. Wählen **Alle Zeitberichte anzeigen** aus.
   1. Sehen Sie sich die folgenden Abschnitte an:

      1. Überprüfen Sie die Metriken **Versandstatistiken**, um den Erfolg des Versands zu verstehen:

         | Metrik | Bedeutung | Worauf Sie achten sollten |
         |-|-|-|
         | Zielgruppe | Anzahl der für die Zielgruppe qualifizierten Profile | Sollte Ihr Testprofil enthalten |
         | Sendungen | Gesamtzahl der Push-Benachrichtigungen | Sollte Ihren API-Aufrufen entsprechen |
         | zugestellt | Erfolgreich an Geräte gesendet | Mit Sendungen vergleichen, um Erfolgsrate zu sehen |
         | Fehler senden | Push-Benachrichtigungen, die nicht gesendet werden konnten | Hohe Zahlen |
         | Ausschlüsse senden | Von Adobe Journey Optimizer ausgeschlossene Profile | Prüfen, ob Ihr Profil ausgeschlossen wurde |

      1. Wenn Fehler senden > 0, überprüfen Sie die **Fehlerursachen** Tabelle auf spezifische Fehler-Codes und Meldungen:

         | häufiger Fehler | Bedeutung | Lösung |
         |-|-|-|
         | Ungültiges Token | Push-Token ist ungültig oder abgelaufen | Live-Aktivitäts-Token vom Gerät erneut registrieren |
         | Token nicht gefunden | Kein gültiges Token mit Profil verknüpft | Überprüfen, ob `liveActivityPushNotificationDetails` vorhanden ist |
         | APNs abgelehnt | Apple Push Notification Service hat die Push-Benachrichtigung abgelehnt | APNs-Zertifikat, Paket-ID, Umgebung überprüfen |
         | Netzwerk-Timeout | APNs können nicht erreicht werden | Vorübergehendes Problem; API-Aufruf erneut versuchen |

      1. Wenn **Ausschlüsse senden** > 0, überprüfen Sie die Tabelle **Ausschlussgründe**:

         | gemeinsamer Ausschluss | Bedeutung | Lösung |
         |-|-|-|
         | Profil hat sich abgemeldet | Benutzer hat Benachrichtigungen abgelehnt | Einverständnisstatus des Profils überprüfen |
         | Token auf die Blockierungsliste gesetzt | Token als ungültig markiert | Token erneut registrieren oder Status der Blockierungsliste überprüfen |
         | Profil nicht geeignet | Profil erfüllt die Kampagnenkriterien nicht | Überprüfen von Zielgruppenregeln für Kampagnen |

   Weitere Informationen finden Sie auf der [Seite Live-Kampagnenbericht](../reports/campaign-global-report-cja-activity.md).

   +++

1. 
   +++ Prüfen von Nachrichten-Feedback-Ereignissen im Profil

   1. Navigieren Sie **Journey Optimizer zu** > **Profile**.
   1. Suchen Sie nach dem Profil und öffnen Sie es.
   1. Wählen Sie die **Ereignisse** aus.
   1. Filtern oder suchen Sie nach Ereignissen mit `eventType = "message.feedback"`.
   1. Suchen Sie nach Feedback-Ereignissen, die dem `liveActivityID` und `event` Ihrer Live-Aktivität entsprechen.
   1. Überprüfen Sie die folgenden Schlüsselfelder:

      | Feld | Mögliche Werte | Bedeutung |
      |-|-|-|
      | `feedbackStatus` | `sent`, `error`, `denylist` | Versandergebnis vom Dienstleister |
      | `serviceProvider` | `apns/apnsSandbox` | Sollte ein Plan für iOS Live-Aktivitäten sein |
      | `errorCode` | Numerischer Code oder `null` | APNs-spezifischer Fehler-Code, wenn fehlgeschlagen |
      | `errorMessage` | Fehlerbeschreibung oder `null` | Lesbare Fehlermeldung |

   1. **Wenn `feedbackStatus: "error"`:**
      * Überprüfen Sie die `errorCode` und `errorMessage` auf spezifische APNs-Fehler
      * Zu den häufigen APNs-Fehlern gehören abgelaufene Token, ungültiges Zertifikat und falsche Paket-ID

   1. **Wenn kein Feedback-Ereignis gefunden wird:**
      * Die Push-Benachrichtigung wurde möglicherweise nicht versucht
      * Überprüfen Sie, ob das Profil in den Kampagnenberichten ausgeschlossen wurde, wie in Schritt 1 oben beschrieben.

      +++

1. 
   +++ Überprüfen der Live-Aktivitätsbereitstellung an APNs in Assurance

   1. Öffnen Sie Ihre Assurance-Sitzung. Sie muss während des API-Aufrufs aktiv sein.
   1. Ausführen des API-Aufrufs (Starten, Aktualisieren oder Beenden).
   1. Suchen Sie in **Ereignisliste** nach Versandereignissen von Live-Aktivitäten.
   1. Suchen Sie nach Ereignissen im Zusammenhang mit dem APNs-Push-Versand.
   1. Prüfen Sie die folgenden Indikatoren:
      * **Push-Anfrage an APNs**: Bestätigt, dass Adobe die Push-Benachrichtigung an die Server von Apple gesendet hat
      * **APNs-**: Zeigt an, ob APNs die Push-Benachrichtigung akzeptiert oder abgelehnt haben
      * **Versandstatus**: Erfolgs- oder Fehleranzeige
   1. Wenn Probleme festgestellt werden, lesen Sie die folgenden häufigen Probleme bei der Bereitstellung von APNs:

      | Problem | Symptom in Assurance | Lösung |
      |-|-|-|
      | APNs-Zertifikat abgelaufen | Authentifizierungsfehler | Neues APNs-Zertifikat erneuern und hochladen |
      | Falsche Umgebung (Entwicklung vs. Produktion) | Fehler wegen nicht übereinstimmender Token | Sicherstellen, dass das Zertifikat mit dem App-Build-Typ übereinstimmt |
      | Paket-ID stimmt nicht überein | Ungültige Bundle-Kennung | Überprüfen, ob die Zertifikatpaket-ID mit der App übereinstimmt |
      | Token abgelaufen | InvalidToken-Fehler von APNs | Live-Aktivitäts-Token erneut registrieren |
      | Ratenbegrenzung | Zu viele Anfragen | Verringern der API-Aufruffrequenz |

      +++

1. 
   +++ Weitere Diagnoseprüfungen durchführen

   1. Überprüfen Sie die Lebenszyklusmetriken der Live-Aktivität im Kampagnenbericht.

      Gehen Sie im Kampagnenbericht zum Abschnitt **Lebenszyklus der Live-Aktivität**:

      | Metrik | Was zu überprüfen ist |
      |-|-|
      | Fernstart | Sollte die Anzahl der API-ausgelösten Starts anzeigen |
      | Updates | Sollte die Anzahl der Update-Ereignisse anzeigen |
      | Endet | Sollte die Anzahl der Endereignisse anzeigen |
      | Gesamtzahl der Kontakte | Gesamtes Ereignisvolumen der Live-Aktivität |

      Wenn diese Metriken null sind oder nicht mit Ihren API-Aufrufen übereinstimmen, gibt es ein Bereitstellungsproblem zwischen Adobe und APNs.

   1. Wenn Adobe einen erfolgreichen Versand anzeigt, das Gerät die Live-Aktivität jedoch nicht:

      * Überprüfen Sie die iOS-Geräteprotokolle auf Fehler bei Live-Aktivitäten.
      * Überprüfen, ob sich die App im Vordergrund oder Hintergrund befindet (nicht beendet).
      * Vergewissern Sie sich, dass das Gerät über eine Netzwerkverbindung verfügt.
      * Testen Sie auf mehreren Geräten, um gerätespezifische Probleme auszuschließen.
      * Stellen Sie sicher, dass iOS Version 16.1 oder höher ist.

      +++

1. 
   +++ Eskalation an den Adobe Support

   Wenn Sie alle Schritte ausgeführt haben und das Problem weiterhin nicht behoben ist, wenden Sie sich an die Adobe-Kundenunterstützung mit:

   **Erforderliche Informationen:**

   * Kampagnen-ID und -name
   * Profil-Namespace und ID
      * `liveActivityID` aus API-Payload
   * Zeitstempel von API-Aufrufen
   * Screenshots von:
      * Kampagnenberichte (Versandstatistiken, Fehlerursachen, Ausschlussgründe)
      * Profilereignisse (`liveActivity.updateToken`, `message.feedback`)
      * Assurance-Sitzung mit Versandereignissen
   * Payload der API-Anfrage abschließen
   * APNs-Zertifikatdetails (Ablauf, Umgebung, Paket-ID)

     +++

## Einzelne Szenarien

### Live Activity Update Token nicht synchronisiert{#token-not-synced}

Die Live-Aktivität wird auf dem Gerät erfolgreich gestartet, aber nachfolgende `update`- oder `end`-API-Aufrufe (die HTTP 200 zurückgeben) können die Live-Aktivität nicht aktualisieren oder schließen. Dies tritt auf, wenn **Live-Aktivitäts-Aktualisierungstoken** nicht ordnungsgemäß mit dem System von Adobe synchronisiert wird.

**Informationen zu Aktualisierungs-Token**

Wenn eine Live-Aktivität auf einem Gerät gestartet wird, generiert iOS ein eindeutiges Aktualisierungstoken für diese spezifische Live-Aktivitätsinstanz. Dieses Token ist erforderlich für:

* Senden von Aktualisierungen an die Live-Aktivität
* Remotebeenden der Live-Aktivität

Jede Live-Aktivitätsinstanz verfügt über ein eigenes eindeutiges Aktualisierungstoken. Adobe benötigt dieses Token, um Updates bereitzustellen und Ereignisse zu beenden.

**Erwartetes Verhalten**

Damit Aktualisierungs- und End-Ereignisse funktionieren, muss Folgendes passieren:

1. Live-Aktivität startet erfolgreich auf dem Gerät.
1. Das Gerät generiert ein Aktualisierungs-Token für diese Live Activity-Instanz.
1. Mobile SDK erfasst und sendet das Aktualisierungstoken an Adobe.
1. Das Aktualisierungstoken wird synchronisiert und im System von Adobe gespeichert.
1. Nachfolgende API-Aufrufe zur Aktualisierung/Beendigung verwenden dieses Token für die Bereitstellung.

**Vorab-Prüfungen:**

* **Benutzerberechtigung**: Wenn eine Live-Aktivität zum ersten Mal auf einem Gerät gestartet wird, zeigt iOS eine Systemaufforderung an: &quot;[App-Name“ ], Live-Aktivitätsaktualisierungen bereitzustellen?“ Der Benutzer **auf „Zulassen** tippen, damit Aktualisierungstoken generiert und synchronisiert werden. Wenn der/die Benutzende auf „Nicht zulassen“ tippt, werden keine Aktualisierungs-Token erstellt und die Aktualisierungs-/End-Anfragen schlagen fehl. Dies ist eine einmalige Berechtigung pro App.
* **Profil- und Kampagnenvalidierung**: Führen Sie [Szenario 1](#profile-issue)- und [Szenario 2](#payload-issues)-Prüfungen durch, um sicherzustellen, dass Profil, Token und Kampagnenkonfiguration korrekt sind.

#### Debugging-Schritte

1. 
   +++ Überprüfen der Update-Token-Synchronisierung in Assurance

   1. Öffnen Sie Ihre Assurance-Sitzung.
   1. Stellen Sie sicher, dass die Sitzung aktiv war, als die Live-Aktivität auf dem Gerät gestartet wurde.
   1. Filtern oder suchen Sie nach Ereignissen mit `eventType = "liveActivity.updateToken"`.
   1. Wählen Sie das Ereignis aus und überprüfen Sie die Payload:

      * Überprüfen Sie, ob das Feld `token` eine gültige Aktualisierungstoken-Zeichenfolge enthält.
      * Überprüfen Sie, ob die `liveActivityID` mit Ihrer Live Activity-Instanz übereinstimmt.
      * Vergewissern Sie sich, dass die `activityType` Ihrer `attributes-type` entspricht.

   1. Wenn das Ereignis nicht gefunden wird:

      * Das Aktualisierungs-Token wurde von SDK nicht generiert oder erfasst.
      * Überprüfen Sie, ob der Benutzer Berechtigungen für Live-Aktivitäten erteilt hat.
      * Überprüfen Sie, ob die Live-Aktivität auf dem Gerät erfolgreich gestartet wurde.
      * Vergewissern Sie sich, dass der mobile SDK ordnungsgemäß integriert ist, um Aktualisierungstoken zu erfassen.

   1. Wenn das Ereignis gefunden wird, fahren Sie mit Schritt 2 fort.

      +++

2. 
   +++ Überprüfen des Aktualisierungs-Tokens in Profilereignissen

   1. Navigieren Sie **Journey Optimizer zu** > **Profile**.
   1. Suchen Sie nach dem Profil und öffnen Sie es.
   1. Wählen Sie die **Ereignisse** aus.
   1. Suchen Sie nach `liveActivity.updateToken` Ereignissen.
   1. Überprüfen Sie die Ereignisdetails:

      * Überprüfen Sie, ob der Zeitstempel kürzlich war (stimmt überein mit dem Beginn der Live-Aktivität).
      * Bestätigen Sie, dass `token` und `liveActivityID` vorhanden sind.
      * Stellen Sie sicher, dass die `activityType` korrekt ist.

   1. Wenn das Ereignis nicht im Profil gefunden wird:

      * Das Aktualisierungstoken-Ereignis wurde möglicherweise noch nicht in das Profil aufgenommen.
      * 5-10 Minuten warten und erneut überprüfen.
      * Wenn nach 15 Minuten immer noch fehlt, kann es ein Problem bei der Ereignisaufnahme geben.

   1. Wenn das Ereignis gefunden wird, wurde das Aktualisierungstoken synchronisiert. Sie können mit Schritt 3 fortfahren.

      +++

3. 
   +++ Live-Aktivitäts-Versandereignisse in Assurance überprüfen

   1. Führen Sie in Ihrer Assurance-Sitzung einen Update- oder End-API-Aufruf aus.
   1. Suchen Sie in **Ereignisliste** nach Versandereignissen von Live-Aktivitäten (APNs und Push-Ereignisse).
   1. Prüfen Sie auf Ereignisse, die Folgendes anzeigen:
      * Push-Benachrichtigung an APNs gesendet.
      * Antwort von APNs (Erfolg oder Fehler).
      * Versandbestätigung
   1. Wenn ein APNs-Versandereignis vorhanden ist: Die Push-Benachrichtigung wurde gesendet. Wenn das Gerät immer noch nicht aktualisiert wird, liegt das Problem möglicherweise auf der Geräteseite (App verarbeitet den Push nicht, Netzwerkprobleme usw.).
   1. Wenn das APNs-Bereitstellungsereignis fehlt: Das Aktualisierungstoken ist im System von Adobe möglicherweise nicht ordnungsgemäß gespeichert oder mit dem Profil verknüpft.
   1. Wenn Fehlerereignisse vorhanden sind: Überprüfen Sie die Fehlerdetails auf bestimmte Fehlerursachen (ungültiges Token, zurückgewiesene APNs usw.).

      +++

## Broadcast-spezifische Szenarien

### Konfiguration der Broadcast-Kampagne und Payload-Probleme{#broadcast-config}

In diesem Abschnitt werden Fehlerbehebungsszenarien für Broadcast-Live-Aktivitäten beschrieben, für die andere Debugging-Ansätze als für unitäre Kampagnen erforderlich sind.

Wenn Profile gültige Token haben, die Live-Aktivität jedoch nicht wie erwartet für Zielgruppenmitglieder angezeigt, aktualisiert oder sich verhalten, hat das Problem in der Regel eine der folgenden Ursachen:

* Die Kampagne ist nicht als API-ausgelöstes Marketing konfiguriert.
* Die API-Payload verwendet eine falsche Broadcast-Struktur (fehlende `audience` oder `input-push-channel`).
* Die Felder `content-state` und `attributes` stimmen nicht mit der Implementierung der iOS-`ActivityAttributes` überein.
* Der `input-push-channel` wurde im Apple-Entwicklerportal nicht korrekt erstellt.

Dieses Fehlerbehebungsszenario gilt für alle Live-Aktivitätsereignisse in Broadcast-Kampagnen: `start`, `update` und `end`.

**Vorab-Prüfungen:**

* **Kampagnentyp**:
   * Vergewissern Sie sich, dass die Kampagne als API-ausgelöstes Marketing erstellt wurde (erforderlich für Kampagnen, die über Broadcast/Zielgruppen laufen).
   * Vergewissern Sie sich, dass in der Kampagnenkonfiguration eine Audience definiert ist.
* **Profil- und Token-**: Probieren Sie mehrere Profile aus der Zielgruppe, um zu überprüfen, ob sie gültige `liveActivityPushNotificationDetails` haben. Ausführliche Validierungsschritte finden Sie [Szenario 1](#profile-issue).

#### Debugging-Schritte

1. 
   +++ Konfiguration der Campaign-Zielgruppe überprüfen

   1. Öffnen Sie Ihre **API-ausgelöste Marketing** Kampagne in Journey Optimizer.
   1. Navigieren Sie zum Abschnitt **Zielgruppe** und überprüfen Sie Folgendes:
      * Für die Kampagne wird eine Audience ausgewählt.
      * Die Zielgruppen-ID entspricht der in Ihrer API-Payload verwendeten.
      * Die Zielgruppe enthält die erwarteten Profile.
   1. Navigieren Sie zum Abschnitt **Aktionen** .
   1. Überprüfen Sie die **Konfiguration der Live-Aktivität**:
      * Die Konfiguration muss für die iOS-App mit der richtigen Bundle-ID festgelegt werden.
      * Der Aktivitätstyp muss mit dem `attributes-type` in Ihrer API-Payload übereinstimmen. Wenn Ihre Payload beispielsweise `"attributes-type": "AirplaneTrackingAttributes"` enthält, muss die Kampagne denselben Aktivitätstyp angeben.

      +++

1. 
   +++ Validieren der Payload-Struktur der Broadcast-API

   Die Struktur der Broadcast-Payload unterscheidet sich von unitären Kampagnen. Vergewissern Sie sich, dass Ihre Payload das richtige Sendeformat verwendet.

   **Erforderliche Felder für die Übertragung:**

   ```json
   {
     "campaignId": "878a11d4-b519-47bd-8313-fecfee19857b",
     "audience": {
       "id": "8c3dbdea-2957-401f-acf0-3966fba1601e"
     },
     "context": {
       "requestPayload": {
         "aps": {
           "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
           "content-available": 1,
           "timestamp": 1771829292,
           "event": "update",
           "attributes-type": "AirplaneTrackingAttributes",
           "content-state": { ... },
           "attributes": { ... }
         }
       }
     }
   }
   ```

   **Häufige Payload-Probleme:**

   | Feld | Anforderung | Häufige Probleme |
   |-|-|-|
   | `campaignId` | Muss mit der ID der aktivierten Marketing-Kampagne übereinstimmen | Falsche Kampagnen-ID oder Verwendung der Transaktionskampagne |
   | `audience.id` | Muss mit einer bestehenden Zielgruppe in AEP übereinstimmen | Falsche Zielgruppen-ID oder Zielgruppe existiert nicht |
   | `input-push-channel` | Erforderlich für Übertragung - Eindeutige Kennung für diese Übertragungsinstanz | Fehlende oder stimmt nicht mit `channelID` in überein`liveActivityData` |
   | `timestamp` | Muss immer die aktuelle/neueste Unix-Epochenzeit in Sekunden sein | Verwenden eines alten/zwischengespeicherten Zeitstempels |
   | `event` | Muss `"start"`, `"update"` oder `"end"` sein | Ungültiger Ereignistyp |
   | `attributes-type` | Muss mit dem Kampagnenaktivitätstyp übereinstimmen | Fehlende Übereinstimmung oder Tippfehler |
   | `content-available` | Muss `1` sein | Fehlender oder falscher Wert |

   **Kritische Broadcast-spezifische Felder:**

   * **`input-push-channel`**
      * Erforderlich für alle Broadcast-Live-Aktivitäten.
      * Fungiert als eindeutige Kennung für diese spezifische Broadcast-Instanz.
      * Alle Profile in der Zielgruppe erhalten Live-Aktivitäten, die mit diesem Kanal verknüpft sind.
      * Muss mit dem `channelID` in `liveActivityData.channelID` übereinstimmen (siehe Schritt 3).
      * Muss vom Client für die `appID` im Apple-Entwicklerportal erstellt werden.
      * Nur Kanäle, die für das jeweilige `appID` erstellt wurden, können für die Übertragung der Live-Aktivität in diesem Programm verwendet werden.

   * **`audience.id`**
      * Muss auf ein in Adobe Experience Platform erstelltes gültiges Zielgruppensegment verweisen.
      * Alle Profile in dieser Zielgruppe sind für die Live-Aktivität angesprochen.
      * Die Zielgruppe muss aktiviert sein und Profile mit gültigen `liveActivityPushNotificationDetails` enthalten.

   **Verwenden Sie immer den neuesten Zeitstempel:**

   * Das Feld `timestamp` muss bei jedem API-Aufruf immer die aktuelle Unix-Epochenzeit (in Sekunden) sein.
   * Diese Anforderung gilt für alle Ereignistypen: `start`, `update` und `end`.
   * **Kritisch für Updates/Ende**: Die Verwendung veralteter Zeitstempel führt dazu, dass Update- und End-Anfragen fehlschlagen.
   * Generieren Sie für jeden Broadcast-API-Aufruf einen neuen Zeitstempel.

   **Optionale Felder:**

   * `dismissal-date`: Unix-Epochenzeit für automatische Abweisung (nur relevant für `end` Ereignisse)
   * `alert`: Objekt mit `title` und `body` zur Benachrichtigung

   Vollständige API-Spezifikationen finden Sie in der [ zur Adobe Journey Optimizer Messaging-API ](https://developer.adobe.com/journey-optimizer-apis/references/messaging).

   +++

1. 
   +++ Ausrichten von Inhaltsstatus, Attributen und Eingabe-Push-Kanal an der iOS-Implementierung

   Stellen Sie sicher, dass die Payload-Felder mit der `ActivityAttributes` Implementierung Ihrer iOS-App übereinstimmen und dass die `input-push-channel` mit der `channelID` in `liveActivityData` übereinstimmt.

   1. Überprüfen Sie Ihre iOS ActivityAttributes-Definition.

   Ihre benutzerdefinierte `ActivityAttributes` muss das `LiveActivityAttributes`-Protokoll von Adobe implementieren:

   ```swift
   struct AirplaneTrackingAttributes: LiveActivityAttributes {
    public struct ContentState: Codable, Hashable {
        var journeyProgress: Int
    }
   
    // Adobe SDK requirement
    var liveActivityData: LiveActivityData
   
    // Your custom attributes
    var arrivalAirport: String
    var departureAirport: String
    var arrivalTerminal: String
   }
   ```

   1. Ordnen Sie iOS-Felder der Broadcast-API-Payload zu.

   Schließen Sie für alle Ereignisse sowohl `attributes` als auch `content-state` ein:

   ```json
         {
         "aps": {
          "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
          "event": "start",
          "timestamp": 1771829292,
          "attributes-type": "AirplaneTrackingAttributes",
          "content-state": {
            "journeyProgress": 0
          },
          "attributes": {
            "arrivalAirport": "DEL",
            "departureAirport": "MUM",
            "arrivalTerminal": "T1",
            "liveActivityData": {
              "channelID": "FEt0NgvLEfEAAOqA6AXdIQ=="
            }
          }
         }
         }
   ```

   **Kritisch: `input-push-channel` muss mit`channelID`** übereinstimmen

   * Der `input-push-channel` am Stamm von `aps` muss genau mit dem `channelID` in `liveActivityData` übereinstimmen.
   * Im obigen Beispiel werden beide Werte `"FEt0NgvLEfEAAOqA6AXdIQ=="`.
   * Dieser Abgleich verknüpft die Broadcast-Instanz mit den Daten der Live-Aktivität.
   * Fehlende Übereinstimmung führt zu fehlgeschlagenen Sendungen.

   **Wichtige Validierungspunkte:**

   * Schließen Sie alle `ContentState` Felder in `content-state` für alle Ereignistypen ein.
   * Schließen Sie alle benutzerdefinierten `LiveActivityAttributes` nur für Startereignisse in `attributes` ein.
   * Bei Startereignissen muss `liveActivityData.channelID` mit `input-push-channel` übereinstimmen.
   * Bei Feldnamen wird zwischen Groß- und Kleinschreibung unterschieden und sie müssen genau übereinstimmen.
   * Datentypen müssen übereinstimmen (Zeichenfolge, int, bool, verschachtelte Objekte usw.).
   * Verwenden Sie für Aktualisierungs-/Endereignisse denselben `input-push-channel` wie das ursprüngliche Startereignis.

   **Häufige Fehler:**

   | Problem | Wirkung | Fehlerbehebung |
   |-|-|-|
   | Fehlende `input-push-channel` | Broadcast funktioniert nicht | Eindeutige Kanal-ID für jede Sendung hinzufügen |
   | `input-push-channel` stimmt nicht mit `channelID` überein | Live-Aktivität wird nicht gestartet | Stellen Sie sicher, dass beide Werte identisch sind |
   | Verschiedene `input-push-channel` für Aktualisierung/Ende | Aktualisierung/Ende erreicht die Live-Aktivitäten nicht | Verwenden derselben Kanal-ID während des gesamten Lebenszyklus |
   | Fehlende `liveActivityData.channelID` | Live-Aktivität wird nicht mit Übertragung verknüpft | `channelID` in Attribute für Startereignis einschließen |
   | Erforderliches Feld im Startereignis fehlt | Live-Aktivität wird nicht gestartet | Alle Felder aus der iOS-Struktur hinzufügen |
   | Falscher Feldname (Tippfehler/Groß-/Kleinschreibung) | Feld ignoriert oder Parsing-Fehler | Exakte Übereinstimmung mit iOS-Feldnamen |
   | Veralteter Zeitstempel bei Aktualisierung/Ende | Aktualisierung/Ende von Geräten ignoriert | Immer neuen Zeitstempel erzeugen |

   +++

1. 
   +++ Testen mit Assurance

   Überprüfen der API-Ausführung und der Payload-Bereitstellung mithilfe von Assurance:

   1. Öffnen Sie Ihre Assurance-Sitzung auf einem Testgerät, das Teil der Zielgruppe ist.
   1. Führt den Broadcast-API-Aufruf aus.
   1. Suchen Sie in **Ereignisliste** nach:
      * Ausführungsereignisse der Kampagne.
      * Versandereignisse für Live-Aktivitäten.
      * Fehlerereignisse, die auf Fehler bei der Payload-Validierung hinweisen.
   1. Überprüfen Sie Ereignis-Payloads zur Bestätigung:
      * Die Payload wurde korrekt verarbeitet.
      * Die `input-push-channel` ist vorhanden.
      * Keine Validierungsfehler aufgetreten.
      * Live-Aktivitäten wurden für Zielgruppenmitglieder an APNs gesendet.

      +++

### Profil nicht in Zielgruppe oder veralteter Zielgruppen-Schnappschuss

In diesem Szenario sind die Kampagne und die Payload korrekt konfiguriert, aber bestimmte Profile empfangen die Live-Aktivität nicht. Dies tritt in der Regel auf, wenn:

* Das Profil ist kein Mitglied der mit der Kampagne verknüpften Zielgruppe.
* Die Zielgruppe ist eine Batch-Zielgruppe und enthält eine veraltete Momentaufnahme der Profildaten.
* Die Live-Aktivitäts-Token des Profils wurden kürzlich hinzugefügt, werden aber noch nicht in der Zielgruppen-Momentaufnahme angezeigt.

Dieses Fehlerbehebungsszenario gilt speziell für Broadcast-Kampagnen, bei denen das zielgruppenbasierte Targeting verwendet wird.

**Grundlegendes zur Zielgruppenauswertung**

Adobe Experience Platform verwendet verschiedene Methoden zur Zielgruppenauswertung, die bestimmen, wann Profilaktualisierungen in der Zielgruppe angezeigt werden:

| Methode | Auswertungshäufigkeit | Aktualität der Daten | Geeignet für |
|-|-|-|--|
| Batch | Einmal täglich (geplant) | Kann bis zu 24 Stunden alt sein | Große Zielgruppen, nicht zeitkritisch |
| Streaming | Echtzeit (bei Profiländerungen) | Fast in Echtzeit für aktualisierte Profile | Zeitabhängig, erfordert Profilaktualisierungen |

**Vorab-Prüfungen:**

* **Validierung von Kampagnen und Payloads**:
   * Führen Sie die Prüfungen in [diesem Szenario](#broadcast-config) durch, um sicherzustellen, dass Kampagne und Payload korrekt sind.
   * Stellen Sie sicher, dass der `audience.id` in der API-Payload mit der Kampagnenkonfiguration übereinstimmt.
* **Profil vorhanden**: Bestätigen Sie mit einer gültigen `liveActivityPushNotificationDetails`, dass das Profil in AEP vorhanden ist.

#### Debugging-Schritte

1. 
   +++ Überprüfen, ob sich das Profil in der Zielgruppe befindet

   Bestätigen Sie zunächst, ob das Profil, das die Live-Aktivität erhalten soll, tatsächlich Teil der Zielgruppe ist.

   1. Navigieren Sie zu **Zielgruppen** in Adobe Experience Platform.
   1. Suchen und öffnen Sie die Audience mithilfe der `audience.id` aus Ihrer Kampagne.
   1. Klicken Sie auf **Durchsuchen** oder **Beispielprofile**, um die Mitglieder der Zielgruppe anzuzeigen.
   1. Suchen Sie mithilfe des Namespace und des Identitätswerts nach Ihrem Testprofil.
   1. **Wenn das Profil nicht in der Zielgruppe gefunden wird:**
      * Das Profil erfüllt nicht die Zielgruppenkriterien oder Segmentregeln.
      * Überprüfen Sie die Zielgruppendefinition, um die Mitgliedschaftsanforderungen zu verstehen.
      * Aktualisieren Sie die Profildaten oder die Zielgruppendefinition, um das Profil einzuschließen.
      * Warten Sie, bis die Auswertung der Zielgruppe abgeschlossen ist (siehe Schritt 2).
   1. **Wenn ein Profil in der Zielgruppe gefunden wird:** Fahren Sie mit Schritt 2 fort, um die Datenfrische zu überprüfen.

      +++

2. 
   +++ Typ und Zeitplan der Zielgruppenauswertung überprüfen

   Ermitteln Sie, ob die Zielgruppe die Batch- oder Streaming-Auswertung verwendet, da dies die Datenfrische bestimmt.

   1. Überprüfen Sie auf **Seite** Zielgruppendetails“ die **Auswertungsmethode**:
      * **Batch**: Wird einmal täglich nach einem Zeitplan ausgewertet.
      * **Streaming**: Wird in Echtzeit ausgewertet, wenn Profilaktualisierungen auftreten.
      * **Edge**: Wird an Edge-Standorten in Echtzeit ausgewertet.

   Führen Sie die entsprechenden Schritte zur Fehlerbehebung auf der Grundlage der Auswertungsmethode aus:

   **Wenn die Zielgruppe die Batch-Auswertung verwendet:**

   1. **Verstehen der Beschränkungen für Batch-Zielgruppen:**
      * Batch-Zielgruppen werden einmal täglich ausgewertet (normalerweise über Nacht).
      * Der Zielgruppen-Snapshot kann bis zu 24 Stunden alt sein.
      * Wenn ein Profil kürzlich Live-Aktivitäts-Token registriert hat, befinden sich diese Token möglicherweise nicht in der aktuellen Momentaufnahme.
      * Aktualisierungen an Profilen werden erst bei der nächsten Batch-Auswertung angezeigt.

   1. **Zeitpunkt der letzten Auswertung überprüfen:**
      * Suchen Sie in den Zielgruppendetails nach dem **Letzte Auswertung** Zeitstempel.
      * Wenn die `liveActivityPushNotificationDetails` des Profils nach diesem Zeitstempel aktualisiert wurden, verfügt die Zielgruppe über veraltete Daten.

   1. **Veraltete Daten auflösen:**
      1. **Option 1: Warten auf die geplante Batch-Auswertung**
         * Die nächste Batch-Auswertung enthält die aktualisierten Profildaten.
         * Dies geschieht automatisch einmal pro Tag.
         * Am besten geeignet für nicht dringende Szenarien.

      1. **Option 2: Trigger-On-Demand-Zielgruppenbewertung**
         1. Navigieren Sie zu **Zielgruppen** in AEP.
         1. Wählen Sie die Zielgruppe aus.
         1. Klicken Sie **Jetzt bewerten** oder **Bei Bedarf aktivieren**.
         1. Warten Sie, bis die Auswertung abgeschlossen ist (dies kann je nach Zielgruppengröße mehrere Minuten bis Stunden dauern).
         1. Stellen Sie sicher, dass das Profil jetzt aktualisierte Daten im Zielgruppen-Snapshot enthält.
         1. Wiederholen Sie den Broadcast-API-Aufruf.

   **Wenn die Zielgruppe die Streaming-Auswertung verwendet:**

   1. **Verstehen Sie das Verhalten von Streaming-Zielgruppen:**
      * Streaming-Zielgruppen werden in Echtzeit ausgewertet, wenn Profilaktualisierungen stattfinden.
      * **Neue Profile**: Qualifizieren Sie sich kurz nach der Erstellung, wenn sie die Segmentkriterien erfüllen.
      * **Aktualisierte Profile**: Kurz nach der Aktualisierung qualifizieren oder disqualifizieren.
      * **Bestehende unveränderte Profile**: werden erst dann erneut ausgewertet, wenn eine Aktualisierung erfolgt.

   1. **Identifizieren Sie das Problem:**
      * Wenn ein Profil bereits vorhanden ist und die Segmentkriterien erfüllt, bei diesem Profil jedoch keine Aktualisierung erfolgt, wird es möglicherweise nicht zu einer neu erstellten Streaming-Zielgruppe hinzugefügt.
      * Trigger Das Profil muss eine Aktualisierung (jede Attributänderung) erhalten, damit es erneut ausgewertet werden kann.

   1. **Problem beheben:**
      * **Für neue Profile**: Sie qualifizieren sich automatisch, wenn die Kriterien erfüllt sind. Keine Aktion erforderlich.
      * **Für vorhandene Profile ohne aktuelle Updates:**
         * Nehmen Sie eine kleinere Aktualisierung am Profil vor (z. B. Aktualisieren eines Zeitstempelfelds).
         * Dadurch wird die Streaming-Auswertung Trigger und das Profil zur Audience hinzugefügt.
         * Alternative: Verwenden Sie eine Batch- oder Edge-Zielgruppe für vorhandene Profile.

      +++
