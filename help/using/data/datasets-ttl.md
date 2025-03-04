---
solution: Journey Optimizer
product: journey optimizer
title: Über Schutzmaßnahmen bei der Time-to-Live (TTL) von Datensätzen
description: 'Datensätze: Schutzmaßnahmen bei der Time-to-Live [!DNL Adobe Journey Optimizer]'
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Plattform, Data Lake, Erstellen, Lake, Datensätze, Profil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: 0e164877044430509fc7b2f2bf3ca2eda8e7497b
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 27%

---

# Schutzmaßnahmen bei der Time-to-Live (TTL) von Datensätzen {#ttl-guardrail}

Ab Februar 2025 wird eine TTL-Schutzmaßnahme (Time-to-Live) wie folgt für Journey Optimizer-systemgenerierte Datensätze in **neuen Sandboxes und neuen** bereitgestellt:

* 90 Tage für Daten im Profilspeicher,
* 13 Monate für Daten im Data Lake.

Diese Änderung wird in einer nachfolgenden Phase in **bestehende Kunden-Sandboxes** integriert. 

## Betroffene Datensätze {#datasets}

In der folgenden Tabelle sind alle betroffenen Datensätze und die jeweilige Time-to-Live im Data Lake und Profilspeicher aufgeführt.

| Datensatz | Data Lake-TTL | TTL des Profilspeichers |
|------|-----|-----|
| Ereignisdatensatz mit Feedback zu AJO-Nachrichten | 13 Monate | 90 Tage |
| Ereignisdatensatz zu Erfahrungen beim AJO-E-Mail-Tracking | 13 Monate | 90 Tage |
| Erlebnisereignisdatensatz beim AJO-Push-Tracking | 13 Monate | 90 Tage |
| AJO-Entitäts-Datensatz | 13 Monate | 90 Tage |
| AJO-Oberflächen-Datensatz | 13 Monate | n. z. |
| Ereignisdatensatz für eingehende AJO-Aktivitäten | 13 Monate | 90 Tage |
| AJO-Klassifizierungs-Datensatz | 13 Monate | n. z. |
| AJO-E-Mail-BCC-Feedback-Ereignisdatensatz | 13 Monate | n. z. |
| acpEntity-Ereignisdatensatz | 13 Monate | n. z. |
| Journeys | 13 Monate | n. z. |
| Journey-Schrittereignisse | 13 Monate | n. z. |
| Entscheidungsobjekt-Repository – Personalisierte Angebote | 13 Monate | n. z. |
| Entscheidungsobjekt-Repository – Fallback-Angebote | 13 Monate | n. z. |
| Entscheidungsobjekt-Repository – Platzierungen | 13 Monate | n. z. |
| Entscheidungsobjekt-Repository – Aktivitäten | 13 Monate | n. z. |
| ODE DecisionEvents – Produktions-Entscheidungsfindung | 13 Monate | n. z. |

## Häufig gestellte Fragen {#faq}

Im Folgenden finden Sie eine Liste von Antworten auf häufig gestellte Fragen zur Datensatz-TTL.

+++Gilt diese Änderung nur für Produktions-Sandboxes oder auch für Entwicklungs-Sandboxes?

Diese Änderung gilt für alle Sandbox-Typen.

+++

+++Sind bei der 90-tägigen TTL im Profilspeicher die Profile selbst betroffen?

Die systemgenerierten Datensatzdaten im Profil werden nach 90 Tagen entfernt, aber nicht die Profile selbst.

+++

+++Wenn systemgenerierte Datensatzdaten an [!DNL Customer Journey Analytics] (CJA) gepusht werden, sind die Daten in CJA auch von der TTL betroffen?

Daten in [!DNL Customer Journey Analytics] werden mit Experience Platform synchronisiert. Daher wirkt sich ein Entfernen von Daten aufgrund einer TTL auf systemgenerierte Datensatzdaten auch auf die Daten in [!DNL Customer Journey Analytics] aus.

+++

+++ Können Kunden die TTL für [!DNL Journey Optimizer] Systemdatensatzdaten im Profilspeicher erhöhen?

TTL-Erweiterungen werden derzeit nicht unterstützt. Es ist jedoch geplant, den TTL-Prozess zu optimieren, damit diese Erweiterungsanfragen irgendwann ab der zweiten Jahreshälfte 2025 berücksichtigt werden können.

>[!NOTE]
>
>Im Profil gespeicherte Daten unterliegen der Berechtigung für das gesamte Datenvolumen . Daher würde jede Erhöhung der Datenspeicherung im Profil infolge einer TTL-Erweiterung auf die Berechtigung für das gesamte Datenvolumen angerechnet. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html){target="_blank}

+++

+++Können Kunden die TTL für [!DNL Journey Optimizer] Systemdatensatzdaten im Data Lake erhöhen?

TTL-Erweiterungen werden derzeit nicht unterstützt. Kunden mit einer Real-Time CDP-Berechtigung können Daten über Ziele exportieren, um Daten länger aufzubewahren. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=de){target="_blank}

+++

+++Sind die folgenden Funktionen von den TTLs betroffen?

* **Lookup Store**: Nein
* **Journey-Begrenzung**: Nein
* **Angebotsbegrenzung**: Nein
* **Sendezeitoptimierung (STO)**: Nein
* **Begrenzung der Nachrichtenfrequenz** (d. h. Geschäftsregeln): Nein
* **Berichterstellung**: Nein

  >[!NOTE]
  >
  >Eine TTL ist bereits in der [!DNL Customer Journey Analytics]-Verbindung (CJA) implementiert, wodurch der effektive maximale Lookback-Zeitraum der betroffenen Datensatzdaten auf 13 Monate reduziert wird.

* **Experience Platform-Datenquelle**: Ja, der Abruf von Erlebnisereignissen unterliegt der 90-tägigen TTL.
* **Berechnete Attribute**: Ja - Die anfängliche Aufstockungsberechnung ist auf die Daten der letzten 90 Tage beschränkt. Das berechnete Attribut wird auf der Grundlage von inkrementellen Ereignissen für nachfolgende Aktualisierungen aktualisiert. Sobald die nachfolgenden Aktualisierungen den Lookback-Zeitraum (max. 6 Monate) erreichen, wirkt sich die TTL im Wesentlichen nicht mehr auf das berechnete Attribut aus. Weitere Informationen.
* **Segmentierung und Retargeting**: Ja - Die Segmentierung hängt von den Daten im Profilspeicher ab. Daher ist der Rückblick auf die betroffenen Datensatzdaten auf 90 Tage beschränkt.
* **Tracking**: Ja - Verringert den effektiven maximalen Lookback-Zeitraum der betroffenen Datensatzdaten auf 90 Tage. Daten aus betroffenen Datensätzen befinden sich 13 Monate im Data Lake.

+++

+++Welcher Zeitstempel wird für die TTL-Durchsetzung verwendet (z. B. für Aufstockungs-Anwendungsfälle)?

Der Zeitstempel des Ereignisses wird verwendet (d. h. nicht das Aufnahmedatum).

+++
