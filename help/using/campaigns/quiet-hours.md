---
solution: Journey Optimizer
product: journey optimizer
title: Ruhezeiten
description: Erfahren Sie, wie Sie mithilfe von Regeln für Ruhezeiten verhindern können, dass Nachrichten zu bestimmten Zeiten gesendet werden
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: Ruhezeiten, zeitbasierte Ausschlüsse, Geschäftsregeln, Regelsätze, Zeitplan, Kampagnen
hide: true
hidefromtoc: true
source-git-commit: e5243565241551fab98a79fa118618535ce58de8
workflow-type: ht
source-wordcount: '980'
ht-degree: 100%

---

# Ruhezeiten {#quiet-hours}

>[!AVAILABILITY]
>
>Regeln für Ruhezeiten sind derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Wenden Sie sich an den Adobe-Support, um auf die Warteliste gesetzt zu werden.

Mithilfe von Ruhezeiten können Sie zeitbasierte Ausschlüsse für E-Mail-, SMS-, Push- und WhatsApp-Kanäle definieren. Sie stellen sicher, dass während bestimmter Zeiträume keine Nachrichten gesendet werden, und helfen Ihnen so, Kundenpräferenzen und Compliance-Anforderungen zu erfüllen.

Ruhezeiten können über Regelsätze angewendet werden, die zur präzisen Steuerung Einzelaktionen in Kampagnen oder Journeys zugewiesen werden können. 

## Dazu dienen Ruhezeiten {#why-quiet-hours}

Mit Ruhezeiten können Sie das Kundenerlebnis auf verschiedene Weise verbessern und Compliance gewährleisten:

* **Respektieren von Kundenwünschen**: Vermeiden Sie den Versand von Nachrichten zu unpassenden Zeiten (z. B. spät in der Nacht oder am frühen Morgen). Dies kann sich negativ auf den Ruf der Marke und die Kundentreue auswirken.

* **Verbessern der Interaktion**: Durch den Versand von Nachrichten zu einem Zeitpunkt, zu dem Kundinnen und Kunden diese mit höherer Wahrscheinlichkeit sehen und auf sie reagieren, erhöhen Sie die Effektivität Ihrer Kommunikation.

* **Einhaltung gesetzlicher Vorgaben**: In einigen Staaten und Regionen ist der Versand von SMS-Marketing-Nachrichten zu bestimmten Zeiten verboten. Ruhezeiten helfen Ihnen, die Einhaltung von Vorschriften wie dem Telephone Consumer Protection Act (TCPA) und SMS-Gesetzen in bestimmten Regionen zu gewährleisten.

* **Optimieren von Timing**: Wenn zwischen Planung und Versand einer Nachricht zu viel Zeit vergeht, ist sie möglicherweise nicht mehr relevant. Ruhezeiten ermöglichen es Ihnen, nicht mehr aktuelle Nachrichten entweder zu verwerfen oder bis zu einem passenden Zeitpunkt zu speichern.

## So funktionieren Ruhezeiten {#how-quiet-hours-work}

Ruhezeiten werden durch Geschäftsregeln implementiert, die Sie mithilfe von Regelsätzen erstellen und auf Ihre Kampagnen und Journeys anwenden.

Wenn der Versand einer Nachricht für einen Zeitraum außerhalb der Ruhezeiten geplant ist, führt [!DNL Adobe Journey Optimizer] je nach Konfiguration eine von zwei Aktionen durch:

* **Verwerfen**: Die Nachricht wird dauerhaft unterdrückt und nicht gesendet.
* **Warteschlange**: Die Nachricht wird angehalten und automatisch gesendet, sobald die Ruhezeit endet.

Das System legt Ruhezeiten anhand der Zeitzone der empfangenden Person fest, die eine der folgenden sein kann:

* Die im Kundenprofil angegebene Zeitzone
* Eine auf anderen Profil- und Ereignisdaten basierende abgeleitete Zeitzone
* Eine feste Zeitzone, die Sie in der Regel angeben

>[!NOTE]
>
>Zeitfenster vor der Unterdrückung: Das System unterdrückt Nachrichten 30 Minuten vor dem Beginn der Ruhezeit. Dadurch wird sichergestellt, dass keine Nachrichten gesendet werden, sobald die Ruhezeit beginnt.

## Erstellen einer Regel für Ruhezeiten {#create-quiet-hours-rule}

So erstellen Sie eine Regel für Ruhezeiten:

1. Navigieren Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Geschäftsregeln]**.

1. Erstellen Sie im Abschnitt **[!UICONTROL Regelsätze]** einen neuen Regelsatz oder wählen Sie einen vorhandenen Regelsatz aus, dem Sie die Regel für Ruhezeiten hinzufügen möchten.

1. Klicken Sie auf **[!UICONTROL Regel erstellen]** und wählen Sie **[!UICONTROL Ruhezeiten]** als Regeltyp aus.

1. Konfigurieren Sie die Einstellungen für Ruhezeiten:

   * **Regelname**: Geben Sie der Regel einen beschreibenden Namen.

   * **Zeitraum**: Legen Sie fest, wann Ruhezeiten gelten sollen:
      * **Tageszeiten**: Legen Sie bestimmte Stunden fest (z. B. 20:00:00Uhr bis 8:00:00 Uhr)
      * **Wochentage**: Wählen Sie bestimmte Tage aus (z. B. Wochenenden)
      * **Benutzerdefinierte Daten**: Wählen Sie bestimmte Kalenderdaten aus (z. B. Feiertage)

   * **Zeitzone**: Wählen Sie aus, wie die Zeitzone festgelegt werden soll:
      * **Lokale Zeitzone der Benutzenden**: Verwenden Sie die Zeitzone aus dem Profil jeder empfangenden Person
      * **Spezifische Zeitzone**: Wenden Sie eine feste Zeitzone an (z. B. Eastern, Central)

   * **Aktion**: Wählen Sie aus, was während Ruhezeiten mit Nachrichten geschieht:
      * **Verwerfen**: Nachrichten werden dauerhaft unterdrückt
      * **Warteschlange**: Nachrichten werden angehalten und gesendet, wenn die Ruhezeit endet

1. Klicken Sie anschließend auf **[!UICONTROL Speichern]**, um die Regel zu erstellen.

## Anwenden von Ruhezeiten auf Kampagnen und Journeys {#apply-quiet-hours}

Nachdem Sie eine Regel für Ruhezeiten erstellt haben, müssen Sie sie auf Ihre Kampagnen oder Journeys anwenden:

1. Öffnen Sie die Kampagne oder Journey, auf die Sie Ruhezeiten anwenden möchten.

1. Navigieren Sie zur Aktion (E-Mail, SMS, Push oder WhatsApp), die Sie steuern möchten.

1. Suchen Sie in der Aktionskonfiguration den Abschnitt **[!UICONTROL Regelsatz]** .

1. Wählen Sie den Regelsatz aus, der Ihre Regel für Ruhezeiten enthält.

1. Speichern Sie Ihre Änderungen.

Die Regel für Ruhezeiten gilt jetzt für diese spezifische Aktion. Bei allen über diese Aktion gesendeten Nachrichten wird die Konfiguration der Ruhezeiten berücksichtigt.

>[!NOTE]
>
>Die Regeln für Ruhezeiten gelten sowohl für geplante als auch für ereignisgesteuerte Nachrichten. Stellen Sie sicher, dass Ihr Regelsatz ordnungsgemäß für Ihren Anwendungsfall konfiguriert ist.

## Überlegungen zur Zeitzone {#timezone-considerations}

Bei Verwendung der Option **Lokale Zeitzone der Benutzenden** sucht [!DNL Adobe Journey Optimizer] in der folgenden Reihenfolge nach Zeitzoneninformationen:

1. **Profil-Zeitzonenattribut**: Die Zeitzone, die explizit im Kundenprofil angegeben ist
2. **Abgeleitete Zeitzone**: Eine Zeitzone, die auf der Grundlage anderer Profildaten und Verhaltenssignale berechnet wird

Wenn keine der beiden verfügbar ist, wendet das System die Ruhezeiten möglicherweise nicht korrekt an. Stellen Sie für optimale Ergebnisse sicher, dass Ihre Kundenprofile Zeitzoneninformationen enthalten.

Bei Verwendung einer **spezifischen Zeitzone** erhalten alle Empfängerinnen und Empfänger Nachrichten, die auf dieser bestimmten Zeitzone basieren, unabhängig von ihrem tatsächlichen Standort.

## Leitlinien und Einschränkungen {#guardrails-limitations}

Beachten Sie bei Verwendung von Ruhezeiten Folgendes:

* **Aktivierungszeit**: Es kann bis zu 20 Minuten dauern, bis eine Regel oder ein Regelsatz vollständig aktiviert ist. Planen Sie dies beim Erstellen oder Ändern von Regeln ein.

* **Verzögerung bei der Kampagnenaktivierung**: Warten Sie nach dem Verknüpfen einer Geschäftsregel mindestens 10 Minuten, bevor Sie eine Journey aktivieren oder eine Kampagne senden, um sicherzustellen, dass die Regeln ordnungsgemäß angewendet werden.

* **Regelsatzeinschränkungen**: Derzeit können bis zu 3 aktive Regelsätze für die Kanal-Domain und 5 für die Journey-Domain verwendet werden.

* **Veröffentlichungsrate von Nachrichten**: Wenn die Ruhezeiten enden und Nachrichten aus der Warteschlange veröffentlicht werden, werden sie mit einer Rate von bis zu 5.000 Nachrichten pro Sekunde und Organisation gesendet.

* **Nicht unterstützt in**: Regeln für Ruhezeiten sind derzeit nicht für die Kampagnenorchestrierung verfügbar.

* **Probelauf**: Regeln für Ruhezeiten werden bei Journey-Probeläufen nicht ausgewertet.

## Reporting {#reporting}

Mit den standardmäßigen Reporting-Funktionen können Sie verfolgen, wie sich Ruhezeiten auf Ihre Kampagnen und Journeys auswirken:

* **Bericht für die gesamte Zeit**: Im Abschnitt „Gründe für Ausschluss“ wird die Anzahl der Kundinnen und Kunden angezeigt, die aufgrund von Regeln für Ruhezeiten keine Nachrichten erhalten haben, zusammen mit dem Namen des konkreten Regelsatzes.

* **Live-Bericht** (falls verfügbar): Zeigt Echtzeitstatistiken zu Profilen an, die derzeit aufgrund von Ruhezeiten warten oder aufgrund von Ruhezeiten verworfen werden.

## Nächste Schritte {#next-steps}

Sobald Ihre Regeln für Ruhezeiten konfiguriert und angewendet sind, können Sie:

* Ihre Kampagne oder Journey prüfen, um sicherzustellen, dass die Regeln ordnungsgemäß verknüpft sind
* Ihre Kampagne oder Journey aktivieren
* Die Auswirkungen von Ruhezeiten in Ihren Berichten überwachen

