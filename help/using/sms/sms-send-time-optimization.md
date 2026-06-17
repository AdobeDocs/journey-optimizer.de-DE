---
solution: Journey Optimizer
product: journey optimizer
title: Optimierung des Versandzeitpunkts für mobile Nachrichten
description: Erfahren Sie, wie Sie die Sendezeitoptimierung für mobile Nachrichten in Adobe Journey Optimizer konfigurieren und verwenden.
feature: SMS
topic: Send Time Optimization
role: User
level: Intermediate
exl-id: 56ff1000-7799-40ff-8f03-2f5868d05e7b
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: f03a3a13-9e99-4c7c-a1ae-0f4d07ced35c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 84aa39bfd480e5bcaa8a58c5ec29f1990e5ddc6f
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 1%

---


# Optimierung des Versandzeitpunkts für mobile Nachrichten {#sms-send-time-optimization}

>[!AVAILABILITY]
>
>Die Versandzeitoptimierung für mobile Nachrichten (SMS, RCS und WhatsApp) ist ab dem 2. Quartal 2026 verfügbar und gilt sowohl für Journey als auch für Kampagnen.

## Überblick {#overview}

Die Sendezeitoptimierung (STO) für Mobile Messaging ermöglicht es Marketing-Experten, über die „Batch- und Blastenzeitplanung“ hinauszugehen, indem sie KI-gesteuerte Insights verwenden, um die optimale Versandzeit für jedes einzelne Profil zu bestimmen. Anstatt Nachrichten gleichzeitig an Ihre gesamte Zielgruppe zu senden, analysiert Adobe Journey Optimizer die historischen Interaktionsmuster jedes Profils und sagt voraus, wann diese Person am ehesten eine SMS-, RCS- oder WhatsApp-Nachricht öffnen, klicken oder darauf antworten wird.

Durch den Versand von Nachrichten zum Zeitpunkt der höchsten prognostizierten Interaktion trägt STO dazu bei, die Öffnungsraten, Klickraten und den Gesamt-Kampagnen-ROI zu erhöhen, ohne dass eine manuelle Zielgruppensegmentierung nach Zeitzone oder Verhaltenskohorte erforderlich ist. STO für mobile Nachrichten wird für SMS-, RCS- und WhatsApp-Kanäle unterstützt und ist sowohl in Journey- als auch in Kampagnenausführungskontexten verfügbar.

## Voraussetzungen {#prerequisites}

Bevor Sie die Sendezeitoptimierung für mobile Nachrichten aktivieren, überprüfen Sie Folgendes:

- Ihre Organisation ist für Adobe Journey Optimizer und für mindestens einen der SMS-, RCS- oder WhatsApp-Kanäle vorgesehen.
- Für die Zielgruppe in Adobe Experience Platform (AEP) ist eine ausreichende Menge an historischen Mobile-Interaktionsdaten vorhanden, einschließlich Versandereignissen, Öffnungen, Link-Klicks und Antworten. Das KI-Modell erfordert einen früheren Interaktionsverlauf, um zuverlässige profilspezifische Prognosen zu generieren.
- Die entsprechende Kanaloberfläche (SMS, RCS oder WhatsApp) ist in Ihrer AJO-Instanz konfiguriert und aktiv. Siehe [Konfigurieren von SMS-Kanaloberflächen](../sms/sms-configuration.md) für Einrichtungsanweisungen.
- Bei Journey-basierten Anwendungsfällen muss die Journey so konzipiert sein, dass der Nachrichtenaktionsknoten nicht durch Upstream-Warte- oder Ereignisknoten eingeschränkt wird, deren Zeitüberschreitungen mit dem STO-Versandfenster kollidieren.

>[!NOTE]
>
>Profile mit unzureichenden historischen Interaktionsdaten greifen auf einen standardmäßigen Versandzeitpunkt zurück, den Sie während der Konfiguration definieren. STO-Prognosen werden auf der Ebene der einzelnen Profile generiert und bewertet.

## Funktionsweise {#how-it-works}

STO für Mobile Messaging basiert auf einem speziell entwickelten KI-Modell, das die historischen Interaktionssignale jedes Profils verarbeitet, um das optimale Versandfenster vorherzusagen. Die folgenden Schritte beschreiben den End-to-End-Fluss.

### &#x200B;1. Datenaufnahme und Modell-Training

Das KI-Modell nimmt kontinuierlich in Adobe Experience Platform gespeicherte mobile Interaktionsereignisse auf, einschließlich Zeitstempeln für das Öffnen von Nachrichten, Link-Klickereignissen, Antwortzeiten und historischen Versanddatensätzen. Diese Signale bilden die Trainingsdaten, mit denen Verhaltensmuster für jedes Profil erlernt werden - z. B. bevorzugte Interaktionsstunden, Wochentagstendenzen und Reaktionsfähigkeit über Zeitzonen hinweg. Das Modell wird auf rollierender Basis neu trainiert, um empfindlich auf Änderungen im Interaktionsverhalten zu bleiben.

### &#x200B;2. Prädiktive Punktzahl pro Profil

Nach dem Training bewertet das Modell jedes Profil in der Zielgruppe und erzeugt ein optimales Versandzeitfenster. Diese Prognose wird in AEP als berechnetes Attribut in das Profil zurückgeschrieben und steht zur Ausführungszeit sowohl Journey als auch Kampagnen zur Verfügung, ohne dass zusätzliche API-Aufrufe oder Echtzeit-Suchen während des Nachrichtenversands erforderlich sind.

### &#x200B;3. Journey-Laufzeitplanung

Wenn ein Journey mit einem STO-aktivierten SMS-, RCS- oder WhatsApp-Aktionsknoten live ist, liest die Journey-Laufzeit das prognostizierte Sendezeitattribut jedes qualifizierten Profils, wenn das Profil den Aktionsknoten erreicht. Die Nachricht wird im konfigurierten Optimierungsfenster gespeichert und gesendet, wenn die prognostizierte optimale Zeit eintrifft. Wenn die prognostizierte Zeit bereits verstrichen ist oder außerhalb des Fensters liegt, wird das konfigurierte Fallback-Verhalten angewendet.

### &#x200B;4. Verteilung der Kampagnensendungen

Bei Kampagnen verteilt STO den Versand über die Zielgruppe auf der Grundlage von profilbezogenen Prognosen, anstatt einen einzelnen Massen-Dispatch zu versenden. AJO staffelt den Versand über das konfigurierte Versandfenster der Kampagne, wobei die prognostizierte optimale Zeit jedes Profils innerhalb der von Ihnen definierten Fenstergrenzen beibehalten wird.

>[!NOTE]
>
>Wenn der prognostizierte optimale Zeitpunkt eines Profils außerhalb des konfigurierten Sendefensters liegt, wird die Nachricht an der nächsten Begrenzung gesendet - entweder am Beginn oder am Ende des Fensters - je nachdem, welcher Zeitpunkt der Prognose am nächsten liegt.

## Konfigurieren der Versandzeitoptimierung {#configure}

### STO in einer Kampagne aktivieren {#configure-campaign}

1. Navigieren Sie in Journey Optimizer zu **Kampagnen** und erstellen Sie eine neue Kampagne oder öffnen Sie einen vorhandenen Entwurf.
2. Wählen Sie **SMS**, **RCS** oder **WhatsApp** als Kanal aus und führen Sie die Schritte Zielgruppe und Nachrichteninhalt aus.
3. Wählen Sie im **Planung** die Option **Versandzeitoptimierung** anstelle eines festen Versanddatums und einer festen Versandzeit aus.
4. Verwenden Sie den Umschalter **Versandzeitoptimierung**, um die Funktion zu aktivieren.
5. Konfigurieren Sie das **Sendefenster**: Legen Sie die Start- und Endzeit fest, innerhalb derer AJO Nachrichten versenden darf. Das Fenster muss mindestens eine Stunde umfassen und kann bis zu 24 Stunden dauern.
6. Definieren Sie einen **Fallback-Sendezeitpunkt** für Profile, die nicht über einen ausreichenden Interaktionsverlauf verfügen, um eine Prognose zu generieren. Sie können den Versand sofort bei geöffnetem Fenster oder zu einer festen Zeit innerhalb des Fensters durchführen.
7. Führen Sie die Schritte zur Frequenzlimitierung, Überprüfung und Aktivierung aus und aktivieren Sie dann die Kampagne.

### STO in einem Journey aktivieren {#configure-journey}

1. Öffnen oder erstellen Sie eine Journey auf der Journey-Arbeitsfläche.
2. Fügen Sie einen Aktionsknoten **SMS**, **RCS** oder **WhatsApp** hinzu oder wählen Sie ihn aus.
3. Erweitern Sie im Konfigurationsbereich des Aktionsknotens die Einstellungen **Versandzeit**.
4. Schalten **Sendezeitoptimierung** in den aktivierten Status um.
5. Festlegen des **Optimierungsfensters**: Die maximale Dauer (in Stunden), die die Laufzeit eine Nachricht beim Warten auf die prognostizierte optimale Versandzeit enthalten kann. Das Standardfenster ist sechs Stunden, das Maximum ist 24 Stunden.
6. Konfigurieren Sie das **Fallback-Verhalten** für Profile ohne Prognosedaten, und zwar entweder sofort senden, wenn ein Profil den Knoten betritt, oder bis zum nächsten verfügbaren Prognosefenster.
7. Speichern Sie die Knotenkonfiguration und veröffentlichen Sie die Journey.

>[!NOTE]
>
>Wenn STO auf einem Journey-Aktionsknoten aktiv ist, kann die tatsächliche Versandzeit für ein Profil bis zur vollständigen Länge des konfigurierten Optimierungsfensters vom Zeitpunkt, zu dem das Profil in den Knoten eintritt, abweichen. Berücksichtigen Sie diese Verzögerung beim Entwerfen von Upstream-Warteknoten und beim Festlegen von Zeitüberschreitungen auf Journey-Ebene, um vorzeitiges Journey-Beenden zu verhindern.

## Leitlinien und Einschränkungen {#guardrails}

- STO gilt nur für ausgehende SMS-, RCS- und WhatsApp-Nachrichten. Eingehende Antwortflüsse und bidirektionale Messaging-Sitzungen unterliegen nicht der STO-Planung.
- Jeder Campaign- oder Journey-Aktionsknoten unterstützt eine Kanaloberfläche pro STO-aktivierter Nachricht. Eine kanalübergreifende STOP-Koordination (z. B. SMS und WhatsApp innerhalb eines einzelnen Knotens) wird nicht unterstützt.
- Das KI-Modell benötigt mindestens 30 Tage an historischen Mobile-Interaktionsdaten pro Profil, um eine Prognose zu erstellen. Profile unterhalb dieses Schwellenwerts verwenden den konfigurierten Fallback-Sendezeitpunkt.
- STO interagiert mit Regeln zur Frequenzlimitierung. Wenn das prognostizierte Versandfenster eines begrenzten Profils mit einer Begrenzungsregel kollidiert, wird die Nachricht gemäß der Begrenzungsregel unterdrückt und nicht für ein späteres Fenster neu geplant.
- Einverständnis-Flags, Opt-out-Datensätze und globale Unterdrückungslisten werden unabhängig von der STO-Planung immer durchgesetzt. Eine für einen optimierten Versand gespeicherte Nachricht unterliegt zum Zeitpunkt des Versands noch immer der Einverständnisprüfung.
- STO ist nicht für Transaktionsnachrichten verfügbar, bei denen aufgrund geschäftlicher oder behördlicher Anforderungen ein sofortiger Versand erforderlich ist.

## Verwandte Themen {#related-topics}

- [Erste Schritte mit SMS, RCS und WhatsApp in Journey Optimizer](../sms/create-sms.md)
- [Konfigurieren von SMS-Kanaloberflächen](../sms/sms-configuration.md)
- [Optimierung des Versandzeitpunkts für E-Mail- und Push-Benachrichtigungen](../building-journeys/send-time-optimization.md)
- [KI-gestütztes Ranking in Journey Optimizer](../offers/offer-activities/ai-ranking.md)
- [Versionshinweise zu Journey Optimizer](../rn/release-notes.md)
