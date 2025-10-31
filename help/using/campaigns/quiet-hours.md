---
solution: Journey Optimizer
product: journey optimizer
title: Ruhezeiten
description: Erfahren Sie, wie Sie mithilfe von Regeln für ruhige Stunden verhindern können, dass Nachrichten zu bestimmten Zeiten gesendet werden
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: ruhige Stunden, Zeitausschlüsse, Geschäftsregeln, Regelsätze, Zeitplan, Kampagnen
exl-id: [TO BE GENERATED]
hide: yes
hidefromtoc: yes
source-git-commit: 11bccd63afa1bf5aafcd1dff70c8193ea754d256
workflow-type: tm+mt
source-wordcount: 980
ht-degree: 9%

---

# Ruhezeiten {#quiet-hours}

>[!AVAILABILITY]
>
>Regeln für Ruhezeiten sind derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Wenden Sie sich an den Adobe-Support, um auf die Warteliste gesetzt zu werden.

Mithilfe von Ruhezeiten können Sie zeitbasierte Ausschlüsse für E-Mail-, SMS-, Push- und WhatsApp-Kanäle definieren. Sie stellen sicher, dass während bestimmter Zeiträume keine Nachrichten gesendet werden, und helfen Ihnen so, Kundenpräferenzen und Compliance-Anforderungen zu erfüllen.

Ruhezeiten können über Regelsätze angewendet werden, die zur präzisen Steuerung Einzelaktionen in Kampagnen oder Journeys zugewiesen werden können. 

## Wozu dienen ruhige Stunden {#why-quiet-hours}

Mit den ruhigen Stunden können Sie das Kundenerlebnis auf verschiedene Weise verbessern und die Compliance aufrechterhalten:

* **Kundenpräferenzen respektieren**: Vermeiden Sie den Versand von Nachrichten zu unangenehmen Zeiten (z. B. spät in der Nacht oder am frühen Morgen), was sich negativ auf den Ruf der Marke und die Kundentreue auswirken kann.

* **Verbesserung der Interaktion**: Durch den Versand von Nachrichten, wenn Kunden diese mit höherer Wahrscheinlichkeit sehen und bearbeiten, erhöhen Sie die Effektivität Ihrer Kommunikation.

* **Gesetzliche Übereinstimmung**: Bestimmte Bundesstaaten und Regionen verbieten SMS-Marketing-Nachrichten während bestimmter Stunden. Ruhige Stunden helfen Ihnen, die Einhaltung von Vorschriften wie dem TCPA und bundesstaatlichen SMS-Gesetzen zu gewährleisten.

* **Optimieren des**: Wenn seit der Planung einer Nachricht zu viel Zeit vergangen ist, ist sie möglicherweise nicht mehr relevant. Ruhige Stunden ermöglichen es Ihnen, veraltete Nachrichten entweder zu verwerfen oder bis zu einem angemessenen Zeitpunkt zu speichern.

## So funktionieren ruhige Stunden {#how-quiet-hours-work}

Ruhestunden werden durch Geschäftsregeln implementiert, die Sie mithilfe von Regelsätzen erstellen und auf Ihre Kampagnen und Journey anwenden.

Wenn der Versand einer Nachricht für einen Zeitraum außerhalb der Ruhezeiten geplant ist, führt [!DNL Adobe Journey Optimizer] je nach Konfiguration eine von zwei Aktionen durch:

* **Verwerfen**: Die Nachricht wird dauerhaft unterdrückt und nie gesendet.
* **Warteschlange**: Die Nachricht wird angehalten und automatisch gesendet, sobald der Zeitraum für ruhige Stunden endet.

Das System wertet ruhige Stunden anhand der Zeitzone des Empfängers aus, die wie folgt aussehen kann:

* Die im Kundenprofil angegebene Zeitzone
* Eine auf anderen Profil- und Ereignisdaten basierende abgeleitete Zeitzone
* Eine feste Zeitzone, die Sie in der Regel angeben

>[!NOTE]
>
>Zeitfenster vor der Unterdrückung: Das System unterdrückt Kommunikationen 30 Minuten vor dem Beginn der ruhigen Stunden. Dadurch wird sichergestellt, dass keine Nachrichten gesendet werden, sobald die ruhige Phase beginnt.

## Erstellen einer Regel für ruhige Stunden {#create-quiet-hours-rule}

So erstellen Sie eine Regel für ruhige Stunden:

1. Navigieren Sie **[!UICONTROL Administration]** > **[!UICONTROL Geschäftsregeln]**.

1. Erstellen Sie **[!UICONTROL Abschnitt]** Regelsätze“ einen neuen Regelsatz oder wählen Sie einen vorhandenen Regelsatz aus, dem Sie die Regel für ruhige Stunden hinzufügen möchten.

1. Klicken Sie **[!UICONTROL Regel erstellen]** und wählen Sie **[!UICONTROL Stille Stunden]** als Regeltyp aus.

1. Konfigurieren Sie die Einstellungen für ruhige Stunden:

   * **Regelname**: Geben Sie der Regel einen beschreibenden Namen.

   * **Zeitraum**: Legen Sie fest, wann ruhige Stunden gelten sollen:
      * **Tageszeiten**: Legen Sie bestimmte Stunden fest (z. B. 20:000 bis 18:000 Uhr)
      * **Wochentage**: Wählen Sie bestimmte Tage aus (z. B. Wochenenden)
      * **Benutzerdefinierte Daten**: Wählen Sie bestimmte Kalenderdaten (z. B. Feiertage) aus

   * **Zeitzone**: Wählen Sie aus, wie die Zeitzone bestimmt werden soll:
      * **Lokale Zeitzone des Benutzers**: Verwenden Sie die Zeitzone aus dem Profil jedes Empfängers
      * **Spezifische Zeitzone**: Wenden Sie eine feste Zeitzone an (z. B. Ost, Zentral)

   * **Aktion**: Wählen Sie aus, was mit Nachrichten während ruhiger Stunden geschieht:
      * **Verwerfen**: Nachrichten werden dauerhaft unterdrückt
      * **Warteschlange**: Nachrichten werden gehalten und gesendet, wenn die Ruhezeit endet

1. Klicken Sie **[!UICONTROL Speichern]**, um die Regel zu erstellen.

## Anwenden von Ruhezeiten auf Kampagnen und Journey {#apply-quiet-hours}

Nachdem Sie eine Regel für ruhige Stunden erstellt haben, müssen Sie sie auf Ihre Kampagnen oder Journey anwenden:

1. Öffnen Sie die Kampagne oder Journey, auf die Sie ruhige Stunden anwenden möchten.

1. Navigieren Sie zu der Aktion (E-Mail, SMS, Push oder WhatsApp), die Sie steuern möchten.

1. Suchen Sie in der Aktionskonfiguration den Abschnitt **[!UICONTROL Regelsatz]** .

1. Wählen Sie den Regelsatz aus, der Ihre Regel für ruhige Stunden enthält.

1. Speichern Sie Ihre Änderungen.

Die Regel für ruhige Stunden gilt jetzt für diese spezifische Aktion. Bei allen Nachrichten, die über diese Aktion gesendet werden, wird die Konfiguration der ruhigen Stunden berücksichtigt.

>[!NOTE]
>
>Die Regeln für ruhige Stunden gelten sowohl für geplante als auch für ereignisgesteuerte Nachrichten. Stellen Sie sicher, dass Ihr Regelsatz ordnungsgemäß für Ihren Anwendungsfall konfiguriert ist.

## Überlegungen zur Zeitzone {#timezone-considerations}

Bei Verwendung der Option **Lokale Zeitzone des Benutzers** sucht [!DNL Adobe Journey Optimizer] in der folgenden Reihenfolge nach Zeitzoneninformationen:

1. **Profil-Zeitzonenattribut**: Die Zeitzone, die explizit im Kundenprofil angegeben ist
2. **Abgeleitete Zeitzone**: Eine Zeitzone, die auf der Grundlage anderer Profildaten und Verhaltenssignale berechnet wird

Wenn keines von beiden verfügbar ist, wendet das System die Stunden möglicherweise nicht korrekt an. Stellen Sie sicher, dass Ihre Kundenprofile Zeitzoneninformationen für optimale Ergebnisse enthalten.

Bei Verwendung einer **spezifischen Zeitzone** erhalten alle Empfänger Nachrichten, die auf dieser einzelnen Zeitzone basieren, unabhängig von ihrem tatsächlichen Standort.

## Leitlinien und Einschränkungen {#guardrails-limitations}

Beachten Sie bei Verwendung von geräuscharmen Stunden Folgendes:

* **Aktivierungszeit**: Es kann bis zu 20 Minuten dauern, bis eine Regel oder ein Regelsatz vollständig aktiviert ist. Planen Sie beim Erstellen oder Ändern von Regeln entsprechend.

* **Verzögerung bei der Kampagnenaktivierung**: Nachdem Sie die Geschäftsregeln verknüpft haben, warten Sie mindestens 10 Minuten, bevor Sie eine Journey aktivieren oder eine Kampagne senden, um sicherzustellen, dass die Regeln ordnungsgemäß angewendet werden.

* **Regelsatzbeschränkungen**: Derzeit können bis zu 3 aktive Regelsätze für die Kanaldomäne und 5 für die Journey-Domain verwendet werden.

* **Nachrichtenfreigaberate**: Wenn ruhige Stunden enden und Nachrichten in der Warteschlange freigegeben werden, werden sie mit einer Rate von bis zu 5.000 Nachrichten pro Sekunde und Organisation gesendet.

* **Nicht unterstützt in**: Regeln für ruhige Stunden sind derzeit nicht für die Kampagnenorchestrierung verfügbar.

* **Probelauf**: Regeln für ruhige Stunden werden beim Journey von Probelauf nicht ausgewertet.

## Reporting {#reporting}

Mit den standardmäßigen Reporting-Funktionen können Sie verfolgen, wie sich ruhige Stunden auf Ihre Kampagnen und Journey auswirken:

* **Allzeitbericht**: Im Abschnitt „Gründe für den Ausschluss“ wird die Anzahl der Kundinnen und Kunden angezeigt, die aufgrund von Regeln für ruhige Stunden keine Nachrichten erhalten haben, zusammen mit dem spezifischen Namen des Regelsatzes.

* **Live-Bericht**: (falls verfügbar) Zeigt Echtzeitstatistiken zu Profilen an, die derzeit aufgrund von ruhigen Stunden warten oder aufgrund von ruhigen Stunden verworfen werden.

## Nächste Schritte {#next-steps}

Sobald Ihre Regeln für ruhige Stunden konfiguriert und angewendet sind, können Sie:

* Überprüfen Sie Ihre Kampagne oder Ihren Journey, um sicherzustellen, dass die Regeln ordnungsgemäß verknüpft sind
* Kampagne oder Journey aktivieren
* Überwachen der Auswirkungen von ruhigen Stunden in Ihren Berichten

