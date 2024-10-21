---
solution: Journey Optimizer
product: journey optimizer
title: Änderungen der Time-to-Live (TTL)- und Streaming-Segmentierung
description: Änderungen der Live-Zeit und Streaming-Segmentierung in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Plattform, Data Lake, Erstellen, Lake, Datensätze, Profil
source-git-commit: a88cb8fbf324bc9c03bc7570b6637e8c95f43a20
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Änderungen der Streaming-Segmentierung (Time-to-Live) {#ttl-guardrail}

## TTL-Limits (Time-to-Live) {#ttl}

Ab dem 1. November 2024 wird in den vom Journey Optimizer-System erstellten Datensätzen in **neuen Sandboxes und neuen Organisationen** ein TTL-Schutzschild (Time-to-Live) bereitgestellt:

* 90 Tage für Daten im Profilspeicher
* 13 Monate für Daten im Data Lake

Diese Änderung wird in einer späteren Phase in **vorhandene Kunden-Sandboxes** eingeführt.

**Häufig gestellte Fragen**

+++ Gilt diese Änderung nur für Produktions-Sandboxes oder auch für Entwicklungs-Sandboxes?

Diese Änderung gilt für alle Sandbox-Typen.

+++


+++ Sind Profile selbst betroffen während der 90-Tage-TTL im Profilspeicher?

Die vom System generierten Datensatzdaten im Profil werden nach 90 Tagen und nicht aus den Profilen selbst abgelegt.

+++

+++ Wenn systemgenerierte Datensatzdaten an Customer Journey Analytics (CJA) gesendet werden, werden dann auch die Daten in CJA von der TTL beeinflusst?

Daten in CJA werden mit Experience Platform synchronisiert. Daher wirkt sich eine Entfernung von Daten aufgrund einer TTL auf systemgenerierte Datensatzdaten auch auf die Daten in CJA aus.

+++

## Aktualisierungen der Streaming-Segmentierung {#segmentation-update}

Darüber hinaus unterstützt Streaming-Segmentierung ab dem 1. November die Verwendung von Sende- und Feedback-Ereignissen aus Tracking- und Feedback-Datensätzen nicht mehr.  Informationen darüber, warum diese Praxis in der Vergangenheit nicht empfohlen wurde, finden Sie [hier](../audience/about-audiences.md#streaming-segmentation-events-guardrails). Diese Änderung gilt für alle Kunden-Sandboxes und -Organisationen zu diesem Zeitpunkt.

**Häufig gestellte Fragen**

+++ Wirken sich diese Änderungen auf die Verwendung von Klicks oder anderen Tracking-Ereignissen aus?

Diese Änderung betrifft nur die Verwendung von Sende- und Öffnungs-Ereignissen. Klicks und andere Tracking-Ereignisse können weiterhin in einem Streaming-Segment verwendet werden.

+++

+++ Wird sich diese Änderung auf die Batch-Segmentierung auswirken?

Diese Änderung betrifft nur Streaming-Segmentierung. Sende- und geöffnete Ereignisse können weiterhin in einem Batch-Segment verwendet werden. Wenn sie in einem Streaming-Segment verwendet werden, werden sie auf Batch-Weise bewertet.

+++

+++ Wird sich diese Änderung auf die Erfassung von Tracking-Daten auswirken?

Diese Änderung wirkt sich nicht auf die Erfassung von Tracking-Daten aus. Versand- und Öffnungs-Ereignisse werden weiterhin erfasst.

+++


+++ Sind Reaktionsereignisse von dieser Änderung betroffen?

Reaktionsereignisse in Journey sind von dieser Änderung nicht betroffen.

+++


+++ Gilt diese Änderung nur für Produktions-Sandboxes oder auch für Entwicklungs-Sandboxes?

Diese Änderung gilt für alle Sandbox-Typen.

+++