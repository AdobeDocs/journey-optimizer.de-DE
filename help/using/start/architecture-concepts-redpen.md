---
solution: Journey Optimizer
product: journey optimizer
title: AJO-Architektur
description: Architektur und Beziehung zu AEP
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: f792fdf9-8038-4dd7-a7d5-d931dbf35c3e
hide: true
source-git-commit: f94067ffb421bfd095ed3fcb3001af0e5dc44ab3
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Architektur

## Das große Ganze: Wie Adobe Journey Optimizer zusammenpasst

Adobe Journey Optimizer (AJO) und Adobe Experience Platform (AEP) arbeiten zusammen, um eine skalierte, datengesteuerte Personalisierung zu ermöglichen. Dieses Ökosystem fungiert als kontinuierlicher Fluss, in dem Daten erfasst, analysiert und zur Erstellung personalisierter Kunden-Journey angewendet werden.

![](../assets/do-not-localize/get-started-big-picture.png)


### Foundation: Adobe Experience Platform (AEP)

Adobe Experience Platform dient als Rückgrat, mit dem Marken Kundendaten zentralisieren und für personalisierte Erlebnisse aktivieren können.

- **Datenplattform**: AEP fungiert als zentraler Knotenpunkt für die Erfassung, Verwaltung und Strukturierung von Kundendaten, um die systemübergreifende Konsistenz sicherzustellen.
- **Datenaufnahme (Quellen)** Marken importieren Daten aus verschiedenen Systemen wie CRM-Plattformen, Websites, mobilen Apps und Cloud-Speicher mithilfe vordefinierter Connectoren. Beispielsweise nimmt ein Source-Connector Kaufdaten aus einer E-Commerce-Plattform auf.
- **Echtzeit-Kundenprofil**: Diese Funktion erstellt einheitliche Profile, indem Daten aus mehreren Quellen zusammengeführt werden. Ein Profil kombiniert beispielsweise E-Mail-Interaktionen und In-Store-Käufe, um eine vollständige Ansicht eines Kunden zu erhalten.
- **Governance-Ebene**: Diese Ebene regelt den Datenzugriff, die Einhaltung von Datenschutzbestimmungen und die Sicherheit. Dadurch wird sichergestellt, dass Marken Kundendaten sicher und unter Einhaltung von Vorschriften nutzen.

### Orchestrierungs-Engine: Adobe Journey Optimizer (AJO)

Adobe Journey Optimizer wendet die Daten und Erkenntnisse aus AEP an, um auf verschiedenen Kanälen intelligente, personalisierte Kundenerlebnisse bereitzustellen.

- **Kundenverständnis**: Echtzeit-Kundenprofile ermöglichen die Segmentierung in Zielgruppen für zielgerichtetes Messaging. Eine Zielgruppe enthält beispielsweise häufige Käufer, die über den Kaufverlauf identifiziert werden.
- **Inhalte und Angebote**:
   - **Content-Management**: Diese Funktion bietet Tools zum kanalübergreifenden Erstellen, Verwalten und Personalisieren von Inhalten. Sie können beispielsweise ein wiederverwendbares Inhaltsfragment für eine Werbe-E-Mail-Kopfzeile erstellen.
   - **Entscheidungs-Management**: Dieses System verwendet Echtzeit-Logik, um das beste Angebot oder die beste Nachricht für jede Person auszuwählen. Beispielsweise erhält eine berechtigte Kundin oder ein berechtigter Kunde möglicherweise ein Rabattangebot auf der Grundlage des Navigationsverlaufs.
- **Journey- und Kampagnenverwaltung**: Diese Funktion automatisiert Interaktionssequenzen (Journey) oder plant einmalige zielgerichtete Nachrichten (Kampagnen). Zum Beispiel eine Folgenachricht für Journey-Trigger nach einer Produktansicht.
- **Versand (Verbindungen)**:
   - **Kanäle**: Diese Funktion liefert Nachrichten und Angebote über Kommunikationsplattformen wie E-Mail, SMS, Push-Benachrichtigungen und Briefpost.
   - **Ziele**: Diese Funktion exportiert Profil- und Zielgruppendaten zur Aktivierung oder Analyse in externe Systeme. Beispielsweise werden Zielgruppendaten zum Anzeigen-Targeting an eine Social-Media-Plattform gesendet.
- **Messung und Analyse**: Diese Funktion verfolgt die Kundeninteraktion und die Kampagnenleistung mit Berichten. Diese Erkenntnisse ermöglichen eine kontinuierliche Verbesserung.

## Kontinuierlicher Optimierungszyklus

Dieses Ökosystem funktioniert als kontinuierlicher Optimierungszyklus. Daten fördern das Verständnis der Kunden, das in personalisierte Inhalte und Entscheidungen einfließt. Diese werden in Journey orchestriert, kanalübergreifend bereitgestellt, auf Effektivität getestet und im Laufe der Zeit verfeinert.

![](../assets/do-not-localize/get-started-flow.png)

## Detaillierte Architektur

![Adobe Journey Optimizer-Architektur](assets/ajo-architecture.png)


## Datenschutz und Sicherheit

Die Datenschutz- und Sicherheitspraktiken von Adobe Experience Cloud gelten auch für Adobe Journey Optimizer. Diese Maßnahmen gewährleisten die Einhaltung von Datenschutzbestimmungen und ermöglichen es Marken, personalisierte Erlebnisse bereitzustellen und gleichzeitig das Vertrauen der Kunden zu wahren.
