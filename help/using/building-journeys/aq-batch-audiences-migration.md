---
solution: Journey Optimizer
product: journey optimizer
title: Migrieren von Batch-Zielgruppen aus Zielgruppen-Qualifizierungs-Journey
description: Erfahren Sie, wie Sie Journey migrieren, die Batch-Zielgruppen in einem Zielgruppen-Qualifizierungsknoten vor dem Erzwingungsdatum August 2026 verwenden.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: Zielgruppen-Qualifizierung, Batch-Zielgruppe, Einstellung, Migration, Zielgruppe lesen, Streaming-Zielgruppe
exl-id: f3c2a7d1-b58e-4a92-c3d5-0e871f2a9b4c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: cea41add5b86adb3b447ce606e73248adce0f731
workflow-type: tm+mt
source-wordcount: 869
ht-degree: 0%

---


# Migrieren von Batch-Zielgruppen aus Zielgruppen-Qualifizierungs-Journey {#aq-batch-migration}

Ab August 2026 blockiert Journey Optimizer die Veröffentlichung für Journeys, die eine Batch-Zielgruppe in einem Zielgruppen-Qualifizierungsknoten verwenden. Identifizieren Sie Ihren Anwendungsfall unten und folgen Sie dem empfohlenen Migrationspfad.

>[!CAUTION]
>
>**Erzwingungsdatum: August 2026.** Neue, entworfene und duplizierte Journey, die eine Batch-Zielgruppe in einem Zielgruppen-Qualifizierungsknoten verwenden, können nach diesem Datum nicht mehr veröffentlicht werden. Seit der Veröffentlichung vom Juni 2026 wird auf der Journey-Arbeitsfläche bereits eine Validierungswarnung angezeigt.

## Gründe für diese Änderung {#why}

Der Knoten **[Zielgruppenqualifizierung](audience-qualification-events.md)** soll nahezu in Echtzeit reagieren, wenn einzelne Profile eine Zielgruppe betreten oder verlassen. Qualifizierungsereignisse werden kontinuierlich, einzeln, eintreffen. Es ist für **[Streaming-Zielgruppen](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)** vorgesehen.

Wenn eine Batch-Zielgruppe stattdessen mit einem Zielgruppen-Qualifizierungsknoten verwendet wird, werden alle Qualifizierungsereignisse gleichzeitig während des Aufnahmefensters empfangen. Dies kann Zehntausende oder Millionen von Journey-Einträgen gleichzeitig in Trigger bringen und zu erheblichen Systembelastungen und unvorhersehbarem Verhalten in nachgelagerten Systemen führen. Dies ist nicht das beabsichtigte Design des Zielgruppen-Qualifizierungsknotens.

Die **[Audience lesen](read-audience.md)**-Aktivität ist das richtige Tool für Batch-basierte Anwendungsfälle: Sie wurde entwickelt, um die geplante Massenverarbeitung auf kontrollierte und vorhersehbare Weise zu verarbeiten.

## Wie Ihre Journey betroffen sind {#impact}

Eine Live-Journey, die eine Batch-Zielgruppe in einem Zielgruppen-Qualifizierungsknoten verwendet, wird nach August 2026 weiterhin ausgeführt. Wenn Sie die Journey jedoch stoppen, duplizieren oder erneut veröffentlichen, wird sie blockiert, bis die Konfiguration aktualisiert wird.


| Journey-Status | Auswirkungen nach August 2026 |
| --- | --- |
| **Live-Journey** | Nicht betroffen. Vorhandene Live-Journey werden weiterhin ausgeführt. Kein automatisches Anhalten. |
| **Neue Journey** | Veröffentlichungssperre, bis die Batch-Zielgruppe ersetzt wurde. |
| **Journey** | Veröffentlichungssperre, bis die Batch-Zielgruppe ersetzt wurde. |
| **Duplizierte Journey** | Veröffentlichungssperre, bis die Batch-Zielgruppe ersetzt wurde. |


## Migrationshandbuch {#migration-paths}

Wenn Sie eine Batch-Zielgruppe in einem Zielgruppen-Qualifizierungsknoten verwenden, identifizieren Sie Ihren Anwendungsfall unten und folgen Sie dem empfohlenen Migrationspfad.

### Anwendungsfall 1: Zielgruppe, die auf Nachrichten-Tracking-Ereignissen in AJO basiert {#use-case-1}

**So sieht es aus:** Ihre Zielgruppen-Qualifizierungs-Zielgruppe verwendet Bedingungen, die auf E-Mail-Sendungen, -Öffnungen oder -Klicks aus den internen Tracking-Datensätzen von Journey Optimizer basieren, z. B. *„Profil hat eine E-Mail erhalten“* oder *„Profil hat eine E-Mail geöffnet“*

>[!NOTE]
>
>Seit November 2024 unterstützt die Streaming-Segmentierung nicht mehr das Senden und Öffnen von Ereignissen aus Journey Optimizer-Tracking-Datensätzen. Auf diesen Ereignissen basierende Zielgruppen werden jetzt im Batch-Modus ausgewertet. [Erfahren Sie mehr über Methoden zur Zielgruppenauswertung](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)

**Empfohlene Alternativen:**

* **Reaktion auf Öffnungen oder Klicks innerhalb derselben Journey** - Verwenden Sie den **[Reaktionsereignis](reaction-events.md)**-Knoten. Sie wurde entwickelt, um auf Öffnungen und Klicks auf Nachrichten zu reagieren, die innerhalb derselben Journey versendet werden, ohne dass eine separate Audience erforderlich ist. [Siehe ein End-to-End-Beispiel mit Reaktionsereignissen](journeys-uc.md#send-multi-channel-messages)

* **Cross-Journey-Klick-Targeting** - Erstellen Sie aus Klick](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)Ereignissen eine [Streaming-Zielgruppe) und verwenden Sie stattdessen den Zielgruppen-Qualifizierungsknoten mit dieser Streaming-Zielgruppe.

* **Bounce-basierte Unterdrückung** - Verwenden Sie die native Unterdrückungsliste [ Journey Optimizer, ](../configuration/manage-suppression-list.md) das Bounce-Verhalten als Zielgruppenbedingung zu modellieren.

* **Beliebige verbleibende Send/Open-Logik** — Wechseln Sie bei einer geplanten Ausführung auf eine **[Zielgruppe lesen](read-audience.md)**-Journey, um die Batch-Zielgruppe sicher zu verarbeiten.


### Anwendungsfall 2: Journey wartet auf neue Batch-Segmentierungsdaten {#use-case-2}

**So sieht es aus:** Sie planen die Ausführung einer Journey nach einem täglichen Segmentierungsauftrag und verwenden einen Zielgruppen-Qualifizierungsknoten, um sicherzustellen, dass die Journey nur ausgelöst wird, wenn die neuesten Zielgruppendaten verfügbar sind.

**Empfohlene Alternative:**

Verwenden Sie eine **[Zielgruppe lesen](read-audience.md)** Journey, wobei die Option **[!UICONTROL Trigger nach der Batch-Zielgruppenbewertung]** aktiviert ist. Diese integrierte Funktion sorgt für die Journey-Ausführung, bis der Segmentierungsvorgang abgeschlossen ist, und beginnt dann sofort, wenn neue Daten verfügbar sind - ohne dass ein Zielgruppen-Qualifizierungsknoten erforderlich ist. [Erfahren Sie, wie Sie diese Option konfigurieren](read-audience.md#schedule)


### Anwendungsfall 3: Aktivierung großer periodischer Batch-Zielgruppen {#use-case-3}

**So sieht es aus:** Sie aktivieren oder aktualisieren regelmäßig eine große Zielgruppe (möglicherweise Millionen von Profilen), und die Journey Zielgruppen-Qualifizierung wird für alle neu qualifizierten Profile gleichzeitig ausgelöst.

**Empfohlene Alternative:**

Verwenden Sie eine **[Zielgruppe lesen](read-audience.md)**-Journey. Sie wurde speziell für die Massenverarbeitung großer Zielgruppen entwickelt, um Profile in kontrollierten Batches zu verarbeiten und eine vorhersehbarere, zuverlässigere Journey-Ausführung im benötigten Umfang zu ermöglichen. [Siehe ein End-to-End-Beispiel](message-to-subscribers-uc.md)

## Was ist, wenn keine der Alternativen für Ihren Anwendungsfall funktioniert? {#exceptions}

Wenn Ihr Anwendungsfall mit keinem der oben genannten Migrationspfade gelöst werden kann, wenden Sie sich an den Adobe-Support. Fälle, die nicht mit bestehenden Alternativen behandelt werden können, werden einzeln geprüft.

## Verwandte Ressourcen {#related}

* [Zielgruppen-Qualifizierungsereignisse](audience-qualification-events.md) — Vollständiges Konfigurationshandbuch und Leitplanken
* [Aktivität „Zielgruppe lesen](read-audience.md) - Konfigurieren des Eintrags für geplante Batch-Zielgruppe
* [Reaktionsereignisse](reaction-events.md) — wie man auf Öffnungen und Klicks innerhalb derselben Journey reagiert
* [Methoden zur Zielgruppenauswertung](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) - Batch-, Streaming- und Edge-Segmentierung erläutert
* [Über Zielgruppen](../audience/about-audiences.md) - Zielgruppentypen und wie sie in Journey Optimizer erstellt werden
* [Verwalten der Unterdrückungsliste](../configuration/manage-suppression-list.md) — Zugreifen auf und Konfigurieren der Bounce-Unterdrückung
* [Schutzmechanismen und Einschränkungen beim Journey](limitations.md)
* [Ein- und Ausstiegskriterien für Journey](entry-exit-criteria-guide.md) — Verstehen Sie anhand von realen Beispielen Einstiegsmuster in Echtzeit vs. Batch
* [Senden von Multi-Channel-Nachrichten](journeys-uc.md#send-multi-channel-messages) - End-to-End-Anwendungsfall mit einer Kombination aus „Zielgruppe lesen“, Reaktionsereignissen, E-Mail und Push-Benachrichtigung
* [Nachricht an Abonnenten senden](message-to-subscribers-uc.md) — End-to-End-Anwendungsfall für die Massenaktivierung von Zielgruppen mit „Zielgruppe lesen“
