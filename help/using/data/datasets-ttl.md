---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zu Time-to-Live(TTL)-Limits für Datensätze
description: Time-to-Live-Limits für Datensätze in  [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: Plattform, Data Lake, Erstellen, Lake, Datensätze, Profil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: c4f6b7754255ce3bf0229702b10955abf9843548
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 98%

---

# Time-to-Live(TTL)-Limits für Datensätze {#ttl-guardrail}

Ab Februar 2025 werden in **neuen Sandboxes und neuen Organisationen** für systemgenerierte Journey Optimizer-Datensätze als Schutzmechanismen die folgenden Limits für die Time-to-Live (TTL) eingeführt:

* 90 Tage für Daten im Profilspeicher,
* 13 Monate für Daten im Data Lake.

Diese Änderung wird in einer nachfolgenden Phase in **bestehende Kunden-Sandboxes** integriert. 

## Betroffene Datensätze {#datasets}

In der folgenden Tabelle sind alle betroffenen Datensätze und die jeweilige Time-to-Live im Data Lake und Profilspeicher aufgelistet.

| Datensatz | TTL im Data Lake | TTL im Profilspeicher |
|------|-----|-----|
| Ereignisdatensatz mit Feedback zu AJO-Nachrichten | 13 Monate | 90 Tage |
| Ereignisdatensatz zu Erfahrungen beim AJO-E-Mail-Tracking | 13 Monate | 90 Tage |
| Ereignisdatensatz zu Erfahrungen beim AJO-Push-Tracking | 13 Monate | 90 Tage |
| AJO-Entitäts-Datensatz | 13 Monate | 90 Tage |
| AJO-Oberflächen-Datensatz | 13 Monate | k. A. |
| Ereignisdatensatz für eingehende AJO-Aktivitäten | 13 Monate | 90 Tage |
| AJO-Klassifizierungs-Datensatz | 13 Monate | k. A. |
| Ereignisdatensatz mit Feedback zu AJO-E-Mail-BCC | 13 Monate | k. A. |
| acpEntity-Ereignisdatensatz | 13 Monate | k. A. |
| Journeys | 13 Monate | k. A. |
| Journey-Schrittereignisse | 13 Monate | k. A. |
| Entscheidungsobjekt-Repository – Personalisierte Angebote | 13 Monate | k. A. |
| Entscheidungsobjekt-Repository – Fallback-Angebote | 13 Monate | k. A. |
| Entscheidungsobjekt-Repository – Platzierungen | 13 Monate | k. A. |
| Entscheidungsobjekt-Repository – Aktivitäten | 13 Monate | k. A. |
| Repository für Erlebnis-Entscheidungs-Objekte – Personalisierte Angebotselemente | 13 Monate | k. A. |
| ODE DecisionEvents – Produktions-Entscheidungsfindung | 13 Monate | k. A. |

## Häufig gestellte Fragen {#faq}

Im Folgenden finden Sie häufig gestellte Fragen zu Datensätzen, Time-to-Live (TTL).

Sie würden gerne mehr erfahren? Verwenden Sie die Feedback-Optionen unten auf dieser Seite, um Ihre Frage zu stellen, oder vernetzen Sie sich mit der [Adobe Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}.

+++Gilt diese Änderung nur für Produktions-Sandboxes oder auch für Entwicklungs-Sandboxes?

Diese Änderung gilt für alle Sandbox-Typen.

+++

+++Sind auch die Profile selbst vom 90-tägigen TTL-Limit für Daten im Profilspeicher betroffen?

Die systemgenerierten Datensatzdaten im Profil werden nach 90 Tagen entfernt, aber nicht die Profile selbst.

+++

+++Wenn systemgenerierte Datensatzdaten per Push an [!DNL Customer Journey Analytics] (CJA) gesendet werden, wirkt sich die TTL dann auch auf die Daten in CJA aus?

Daten in [!DNL Customer Journey Analytics] werden mit Experience Platform synchronisiert. Daher wirkt sich eine Entfernung von Daten aufgrund einer TTL für systemgenerierte Datensatzdaten auch auf die Daten in [!DNL Customer Journey Analytics] aus.

+++

+++ Können Kundinnen und Kunden die TTL für Systemdatensatzdaten von [!DNL Journey Optimizer] im Profilspeicher erhöhen? 

TTL-Erweiterungen werden derzeit nicht unterstützt. Es ist jedoch geplant, den TTL-Prozess zu optimieren, damit diese Erweiterungsanfragen irgendwann ab der zweiten Jahreshälfte 2025 berücksichtigt werden können.

>[!NOTE]
>
>Im Profil gespeicherte Daten unterliegen der Berechtigung für das gesamte Datenvolumen. Daher würde jede Erhöhung der Datenspeicherung im Profil infolge einer TTL-Erweiterung der Berechtigung für das gesamte Datenvolumen angerechnet werden. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/landing/license/total-data-volume){target=_blank}

+++

+++Können Kundinnen und Kunden die TTL für Systemdatensatzdaten von [!DNL Journey Optimizer] im Data Lake erhöhen? 

TTL-Erweiterungen werden derzeit nicht unterstützt. Kundinnen und Kunden können Daten über Ziele exportieren, um diese länger aufzubewahren. [Erfahren Sie mehr](https://experienceleague.adobe.com/de/docs/experience-platform/destinations/ui/activate/export-datasets){target=_blank}. Darüber hinaus können Kundinnen und Kunden mit **[!DNL Data Distiller]**-Berechtigung abgeleitete Datensätze erstellen, um die Daten ohne TTL im Data Lake zu speichern. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

+++

+++Sind die folgenden Funktionen von den TTLs betroffen? 

* **Suchspeicher**: Nein
* **Journey-Begrenzung**: Nein
* **Angebotsbegrenzung**: Nein
* **Optimierung des Versandzeitpunkts (STO)**: Nein
* **Frequenzbegrenzung für Nachrichten** (d. h. Geschäftsregeln): Nein
* **Reporting**: Nein

  >[!NOTE]
  >
  >Es ist bereits eine TTL in der [!DNL Customer Journey Analytics]-Verbindung (CJA-Verbindung) implementiert, die den maximalen effektiven Lookback-Zeitraum der betroffenen Datensatzdaten auf 13 Monate reduziert.

* **Experience Platform-Datenquelle**: Nicht anwendbar – Das Abrufen von Erlebnisereignissen wird nicht über Datenquellen unterstützt.
* **Berechnete Attribute**: Ja, die anfängliche Aufstockungsberechnung ist auf die Daten der letzten 90 Tage beschränkt. Das berechnete Attribut wird basierend auf inkrementellen Ereignissen für nachfolgende Updates aktualisiert. Sobald die nachfolgenden Updates den Lookback-Zeitraum (max. 6 Monate) erreichen, wirkt sich die TTL im Wesentlichen nicht mehr auf das berechnete Attribut aus. Weitere Informationen.
* **Segmentierung und Retargeting**: Ja, die Segmentierung hängt von den Daten im Profilspeicher ab. Daher ist der Lookback-Zeitraum der betroffenen Datensatzdaten auf 90 Tage beschränkt.
* **Tracking**: Ja, es verringert den effektiven maximalen Lookback-Zeitraum der betroffenen Datensatzdaten auf 90 Tage. Daten aus betroffenen Datensätzen bleiben für 13 Monate im Data Lake.

+++

+++Welcher Zeitstempel wird für die Durchsetzung der TTL verwendet (z. B. für Anwendungsfälle zur Aufstockung)? 

Es wird der Zeitstempel des Ereignisses verwendet (d. h. nicht das Aufnahmedatum).

+++
