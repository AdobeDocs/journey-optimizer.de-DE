---
solution: Journey Optimizer
product: journey optimizer
title: Über Änderungen bei Time-to-Live (TTL) und Streaming-Segmentierung
description: Änderungen bei Time-to-Live und Streaming-Segmentierung in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Plattform, Data Lake, Erstellen, Lake, Datensätze, Profil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: ccb4cc944271fb197e7aee87f57b51c28cb3565f
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 100%

---

# Änderungen bei Time-to-Live und Streaming-Segmentierung {#ttl-guardrail}

## Updates bei der Streaming-Segmentierung {#segmentation-update}

Ab dem 1. November 2024 unterstützt die Streaming-Segmentierung die Verwendung von Sende- und Öffnungsereignissen aus Tracking- und Feedback-Datensätzen aus Journey Optimizer nicht mehr. Diese Änderung gilt für alle Kunden-Sandboxes und Organisationen. Informationen darüber, warum diese Praxis in der Vergangenheit nicht empfohlen wurde, finden Sie [hier](../audience/about-audiences.md#streaming-segmentation-events-guardrails).

**Häufig gestellte Fragen**

+++ Wirken sich diese Änderungen auf die Verwendung von Klicks oder anderen Tracking-Ereignissen aus?

Diese Änderung betrifft nur die Verwendung von Sende- und Öffnungsereignissen. Klicks und andere Tracking-Ereignisse können weiterhin in einem Streaming-Segment verwendet werden.

+++

+++ Wirkt sich diese Änderung auf die Batch-Segmentierung aus?

Diese Änderung betrifft nur die Streaming-Segmentierung. Sende- und Öffnungsereignisse können weiterhin in einem Batch-Segment verwendet werden. Bei Verwendung in einem Streaming-Segment werden sie auf Batch-Weise ausgewertet.

+++

+++ Wirkt sich diese Änderung auf die Erfassung von Tracking-Daten aus?

Diese Änderung betrifft nicht die Erfassung von Tracking-Daten. Versand- und Öffnungsereignisse werden weiterhin erfasst.

+++

+++ Wirkt sich diese Änderung auf Reaktionsereignisse aus?

Reaktionsereignisse in Journeys sind von dieser Änderung nicht betroffen.

+++

+++ Gilt diese Änderung nur für Produktions-Sandboxes oder auch für Entwicklungs-Sandboxes?

Diese Änderung gilt für alle Sandbox-Typen.

+++

+++ Wirkt sich die Änderung auch auf aus dem Sendeereignis resultierende Feedback-Ereignisse aus?

Diese Änderung gilt auch für Ausschlussereignisse und Bounce-/Verzögerungsereignisse, die auf den Versand zurückzuführen sind.

+++

## Stufenweise Time-to-Live(TTL)-Aktualisierung {#ttl}

Ab Februar 2025 wird in **neuen Sandboxes und neuen Organisationen** für systemgenerierte Journey Optimizer-Datensätze das folgende Time-to-Live(TTL)-Limit eingeführt:

* 90 Tage für Daten im Profilspeicher
* 13 Monate für Daten im Data Lake

Diese Änderung wird in einer nachfolgenden Phase in **bestehende Kunden-Sandboxes** integriert. 

**Häufig gestellte Fragen**

+++ Gilt diese Änderung nur für Produktions-Sandboxes oder auch für Entwicklungs-Sandboxes?

Diese Änderung gilt für alle Sandbox-Typen.

+++

+++ Sind auch die Profile selbst vom 90-tägigen TTL-Limit für Daten im Profilspeicher betroffen?

Die systemgenerierten Datensatzdaten im Profil werden nach 90 Tagen entfernt, aber nicht die Profile selbst.

+++

+++ Wenn systemgenerierte Datensatzdaten per Push an Customer Journey Analytics (CJA) gesendet werden, wirkt sich die TTL dann auch auf die Daten in CJA aus?

Daten in CJA werden mit Experience Platform synchronisiert. Daher wirkt sich eine TTL-basierte Entfernung von Daten auf systemgenerierte Datensatzdaten auch auf die Daten in CJA aus.

+++
