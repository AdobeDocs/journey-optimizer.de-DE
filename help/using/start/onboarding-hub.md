---
solution: Journey Optimizer
product: journey optimizer
title: Onboarding-Projekthandbuch | Adobe Journey Optimizer
description: Planen und verwalten Sie ein Adobe Journey Optimizer-Onboarding-Projekt für Admin-, Daten-, Entwickler- und Marketing-Rollen.
feature: Get Started
topic: Content Management
role: Admin
level: Intermediate
keywords: Journey Optimizer, Onboarding, Onboarding-Projekt, Rollout, Implementierungsplan, Admin, CSM, Implementierungspartner, Checkliste mit mehreren Phasen
source-git-commit: 6a653e1dbb00f68ff689ea3e0dc0b15abda1e21e
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 4%

---

# Onboarding-Projekthandbuch {#onboarding-hub}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Planen und koordinieren Sie einen vollständigen Adobe Journey Optimizer-Rollout mit einer stufenweisen Checkliste, die die Rollen des Administrators, des Datentechnikers, des Entwicklers und des Marketing-Experten umfasst.

>[!ENDSHADEBOX]

Diese Seite richtet sich an **Systemadministratoren und Implementierungspartner** die einen vollständigen Journey Optimizer-Rollout koordinieren. Es bietet eine schrittweise Checkliste, die alle Rollen abdeckt und Links zu den detaillierten rollenspezifischen Handbüchern enthält.

>[!NOTE]
>
>Wenn Sie ein Kontakt mit einer bestimmten Rolle sind, navigieren Sie stattdessen zu [Erste Schritte mit Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md).

## Phase 1 - Einrichtung der Umgebung (Administrator) {#phase-1}

Führen Sie diese grundlegenden Aufgaben zuerst aus, damit die anderen Rollen mit ihrer Arbeit beginnen können:

* [ ]-Bereitstellungs-Sandboxes (Entwicklung, Staging, Produktion)
* [ ] Konfigurieren von Benutzerrollen und -berechtigungen in Adobe Admin Console
* [ ] Einrichten von Produktprofilen und Zugriffssteuerung auf Objektebene
* [ ] Delegieren von Subdomains und Konfigurieren von IP-Pools
* [ ] Konfigurieren von Kanalkonfigurationen (E-Mail, SMS, Push, Web, In-App, Briefpost)
* [ ] Einrichten von Unterdrückungslisten und Einverständnisrichtlinien

➡️ Vollständige Details anzeigen: [Erste Schritte für Administratoren](path/administrator.md)

## Phase 2 - Datengrundlage (Datentechniker) {#phase-2}

Erstellen Sie die Datenschicht, die Profile, Zielgruppen und Journey-Trigger unterstützt:

* [ ] Definieren von Identity-Namespaces
* [ ] Erstellen von XDM-Schemata (Profil, Erlebnisereignisse, relationale Schemata)
* [ ] Einrichten und Aktivieren von Datensätzen für das Echtzeit-Kundenprofil
* [ ] Konfigurieren der Datenaufnahme (Batch und Streaming)
* [ ] Berechnete Attribute erstellen
* [ ] Konfigurieren von Journey-Ereignissen und Datenquellen

➡️ Vollständige Details finden Sie [Erste Schritte für Dateningenieure](path/data-engineer.md)

## Phase 3 - Technische Integrationen (Entwickler) {#phase-3}

Verbinden Sie Ihre Anwendungen, damit Journey mit Echtzeitdaten arbeiten können:

* [ ] Integrieren von Mobile SDK (iOS/Android) mit der Push-Einrichtung
* [ ] Implementieren von Web SDK für Web-Erlebnisse und Web-Push
* [ ] Implementieren des Ereignisversands von Programmen aus
* [ ] Erstellen benutzerdefinierter Aktionsendpunkte für externe Systemintegrationen
* [ ] Validieren mit Adobe Experience Platform Assurance

➡️ Vollständige Details anzeigen: [Erste Schritte für Entwickler](path/developer.md)

## Phase 4 - Erste Erfahrungen (Marketer) {#phase-4}

Nutzen Sie die Grundlage, indem Sie Ihre ersten Journey und Kampagnen starten:

* [ ] Erstellen der ersten Zielgruppe (Segmentdefinition oder CSV-Upload)
* [ ] Erstellen einer Test-Journey mit E-Mail-Aktion
* [ ] Einrichten von Inhaltsvorlagen und Fragmenten
* [ ] Veröffentlichen und Überwachen einer Kampagne
* [ ] Live-Berichte überprüfen

➡️ Vollständige Details anzeigen: [Erste Schritte für Marketing-Fachleute](path/marketer.md)

## Onboarding-Checkliste (druckbar) {#checklist}

| Phase | Besitzerin bzw. Besitzer | Status |
|-------|-------|--------|
| Einrichten der Umgebung | Administrator | |
| Datengrundlage | Datentechniker | |
| Technische Integrationen | Entwickler | |
| Erste Erlebnisse | Marketer | |

## Verwandte Ressourcen {#related-resources}

* [Rollen und Zuständigkeiten](quick-start.md) - So arbeiten die vier Rollen zusammen und die empfohlene Implementierungsreihenfolge.
* [Journey Optimizer-Tutorials](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} - Schrittweise Videos und Anleitungen zu jeder Rolle.
* [Erste Schritte mit dem Daten-Management](../data/gs-data.md) - So werden Daten aufgenommen, vereinheitlicht und aktiviert.
