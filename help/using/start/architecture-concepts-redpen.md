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
ht-degree: 100%

---

# Architektur

## Das große Bild: Welche Rolle Adobe Journey Optimizer spielt

Adobe Journey Optimizer (AJO) und Adobe Experience Platform (AEP) arbeiten zusammen, um eine skalierte, datengesteuerte Personalisierung im benötigten Umfang zu ermöglichen. Dieses Ökosystem fungiert als kontinuierlicher Fluss, in dem Daten erfasst, analysiert und zur Erstellung personalisierter Customer Journeys angewendet werden.

![](../assets/do-not-localize/get-started-big-picture.png)


### Fundament: Adobe Experience Platform (AEP)

Adobe Experience Platform dient als Backbone, mit dem Marken Kundendaten zentralisieren und für personalisierte Erlebnisse aktivieren können.

- **Datenplattform**: AEP fungiert als zentrale Drehscheibe für die Erfassung, Verwaltung und Strukturierung von Kundendaten, um systemübergreifende Konsistenz zu gewährleisten.
- **Datenaufnahme (Quellen)**: Marken importieren Daten mithilfe vordefinierter Connectoren aus verschiedenen Systemen wie CRM-Plattformen, Websites, Mobile Apps und Cloud-Speicher. Beispielsweise nimmt ein Quell-Connector Kaufdaten aus einer E-Commerce-Plattform auf.
- **Echtzeit-Kundenprofil**: Diese Funktion erstellt einheitliche Profile, indem Daten aus verschiedenen Quellen zusammengeführt werden. Ein Profil kombiniert beispielsweise E-Mail-Interaktionen und Ladeneinkäufe, um eine vollständige Ansicht einer Kundin bzw. eines Kunden zu schaffen.
- **Governance-Ebene**: Diese Ebene regelt den Datenzugriff, die Einhaltung von Datenschutzbestimmungen und die Sicherheit. Damit wird sichergestellt, dass Marken Kundendaten sicher und unter Einhaltung von Vorschriften nutzen.

### Orchestrierungs-Engine: Adobe Journey Optimizer (AJO)

Adobe Journey Optimizer wendet die Daten und Erkenntnisse aus AEP an, um in verschiedenen Kanälen intelligente, personalisierte Kundenerlebnisse bereitzustellen.

- **Kundenverständnis**: Echtzeit-Kundenprofile ermöglichen eine Segmentierung in Zielgruppen für gezieltes Messaging. Eine Zielgruppe enthält beispielsweise regelmäßige Käuferinnen und Käufer, die über den Kaufverlauf identifiziert werden.
- **Inhalte und Angebote**:
   - **Content-Management**: Diese Funktion bietet Tools zum kanalübergreifenden Erstellen, Verwalten und Personalisieren von Inhalten. Sie können beispielsweise ein wiederverwendbares Inhaltsfragment für die Kopfzeile einer Werbe-E-Mail erstellen.
   - **Entscheidungs-Management**: Dieses System nutzt Echtzeit-Logik, um das beste Angebot oder die beste Nachricht für einzelne Kontakte auszuwählen. Beispielsweise erhält eine geeignete Person auf der Grundlage des Navigationsverlaufs ggf. ein Rabattangebot.
- **Journey- und Kampagnen-Management**: Diese Funktion automatisiert Interaktionssequenzen (Journeys) oder plant einmalige gezielte Nachrichten (Kampagnen). Zum Beispiel kann eine Journey nach einer Produktansicht Folge-E-Mails auslösen.
- **Versand (Verbindungen)**:
   - **Kanäle**: Diese Funktion liefert Nachrichten und Angebote über Kommunikationsplattformen wie E-Mail, SMS, Push-Benachrichtigungen und Briefpost.
   - **Ziele**: Diese Funktion exportiert Profil- und Zielgruppendaten zur Aktivierung oder Analyse in externe Systeme. Beispielsweise werden Zielgruppendaten zum Anzeigen-Targeting an eine Social-Media-Plattform gesendet.
- **Messung und Analyse**: Diese Funktion verfolgt Kundeninteraktion und die Kampagnenleistung mit Berichten. Die entsprechenden Erkenntnisse ermöglichen eine kontinuierliche Verbesserung.

## Kontinuierlicher Optimierungszyklus

Dieses Ökosystem funktioniert als kontinuierlicher Optimierungszyklus. Daten fördern das Kundenverständnis, das in personalisierte Inhalte und Entscheidungen einfließt. Diese werden in Journeys orchestriert, kanalübergreifend bereitgestellt, auf Effektivität getestet und im Laufe der Zeit verfeinert.

![](../assets/do-not-localize/get-started-flow.png)

## Detaillierte Architektur

![Architektur von Adobe Journey Optimizer](assets/ajo-architecture.png)


## Datenschutz und Sicherheit

Die Datenschutz- und Sicherheitspraktiken von Adobe Experience Cloud gelten auch für Adobe Journey Optimizer. Diese Praktiken gewährleisten die Einhaltung von Datenschutzbestimmungen und ermöglichen es Marken, für personalisierte Erlebnisse zu sorgen und gleichzeitig das Kundenvertrauen zu wahren.
