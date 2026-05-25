---
solution: Journey Optimizer
product: journey optimizer
title: Treuedaten und -datensätze
description: Erfahren Sie, welche Adobe Experience Platform-Profildaten und -Datensätze bei Problemen mit der Treue erforderlich sind und wie sich die Time-to-Live (TTL) des Datensatzes auf die Aufbewahrung auswirkt.
feature: Journeys
topic: Content Management
role: Admin, Developer
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: a7c4e1b2-8f3d-4a6c-9e0b-1d2e3f4a5b6c
source-git-commit: 894dd7f811e87a8551f92654e5b913a459c1382e
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 6%

---

# Treuedaten und -datensätze {#loyalty-data-and-datasets}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit Treue**

[Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md)

+++Herausforderungen erstellen und verwalten

* [Zugriff und Verwaltung von Herausforderungen und Aufgaben](access-loyalty-challenges.md)
* [Herausforderungen schaffen](create-challenges.md)
* [Aufgaben erstellen](create-tasks.md)
* [Überwachen der Leistung beim Treueprogramm](loyalty-reporting.md)

+++

+++Konfigurieren und Integrieren

<!-- * [Configure loyalty challenges](loyalty-admin.md) -->
* **Treuedaten und Datensätze** ◀︎ **Sie sind hier**
* [API-Referenz für Herausforderungen im Treueprogramm](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

+++

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **privaten Betaversion**. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](../rn/releases.md).

## Überblick {#overview}

Herausforderungen im Zusammenhang mit der Treue ergeben sich aus Adobe Experience Platform für Identität, Profilattribute, Erlebnisereignisse und Zielgruppen. Auf dieser Seite erfahren Sie, welche Daten vorbereitet werden müssen, welche Datensätze betroffen sind und wie **Time-to-Live (TTL)** die Datenspeicherung beeinflusst, bevor Sie Herausforderungen erstellen oder die Loyalty Challenges-APIs verwenden.

Wenden Sie sich zur Einrichtung des Journey Optimizer-Programms (Belohnungserfüllung und Ereigniszuordnung) an Ihren Adobe-Administrator. Informationen zu REST-Endpunkten und zur Authentifizierung finden Sie in der [API-Referenz für Treueprogramm-Herausforderungen](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}.

## Adobe Experience Platform-Daten {#aep-data}

### Profilattribute {#profile-attributes}

Herausforderungen für Zielgruppen, Personalisierung und Reporting: Verwenden Sie Profile in der **[!DNL XDM Individual Profile]**. Passen Sie die Identität [Namespace](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces){target="_blank"} die Sie für Herausforderungen im Zusammenhang mit der Treue verwenden, an die Art und Weise an, wie Mitglieder in Ihren Profildaten identifiziert werden.

Verwenden Sie für Standardattribute vom Profil (Punkte, Ebene, Programm, Status und zugehörige Felder) die Schemafeldgruppe **[Treuedetails](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}** von Experience Platform. Diese Feldergruppe definiert das `loyalty` und seine Eigenschaften (z. B. `points`, `tier`, `program` und `status`).

➡️ [Schemafeldgruppe Treuedetails](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}

### Erlebnisereignisse {#experience-events}

**[!UICONTROL Kauf]**, **[!UICONTROL Ausgaben]** und **[!UICONTROL benutzerspezifische Ereignisse]** hängen von Erlebnisereignissen ab, die in Adobe Experience Platform aufgenommen werden. Bei Aufgaben **[!UICONTROL Benutzerspezifisches Ereignis]** muss Ihr Administrator übereinstimmende Ereignisdefinitionen (Kennungspfad, optionale XDM-Schema-ID, Schema und Transformator) konfigurieren, bevor Sie sie in Task Builder auswählen können.

Stellen Sie sicher, dass Ereignis-Payloads denselben Identity-Namespace verwenden wie Ihre Konfiguration zu Treueprogramm-Herausforderungen , damit der Fortschritt dem richtigen Profil zugeordnet werden kann.

### Zielgruppen und Reporting {#audiences-reporting}

Marketing-Experten wählen Platform [Zielgruppen](../audience/about-audiences.md) beim Konfigurieren der Anfechtungseignung für Herausforderungen aus. Für Reporting-Dashboards zum Treueprogramm wird Adobe Customer Journey Analytics verwendet. [Erfahren Sie, wie Sie die Leistung der Herausforderung „Treue“ überwachen](loyalty-reporting.md)

## Datensatz-TTL (Time-to-Live) {#dataset-ttl}

Herausforderungen im Zusammenhang mit dem Treueprogramm speichern Betriebs- und Berichtsdaten in Adobe Experience Platform-Datensätzen (einschließlich Ereignis- und Personalisierungsdatensätzen, die für Ihr Programm erstellt wurden). Der Datensatz **Time-to-Live (TTL)** steuert, wie lange Daten im Data Lake und gegebenenfalls im Profilspeicher aufbewahrt werden.

Journey Optimizer wendet TTL-Schutzmechanismen auf viele systemgenerierte Datensätze an. Treuedatensätze folgen demselben Platform-Aufbewahrungsmodell für Ihre Sandbox.

➡️ [Leitplanken für Datensätze (Time-to-Live, TTL) in Journey Optimizer](../data/datasets-ttl.md)

>[!NOTE]
>
>Die Konfiguration der Treue auf Unternehmensebene kann Archivierungs- und Aufbewahrungseinstellungen (z. B. die Archivdauer) enthalten, die über den Metadaten-Service der Treue verwaltet werden. Stimmen Sie sich mit Ihrem Adobe-Administrator ab, wenn Sie die Beibehaltung für Ihre private Beta-Umgebung anpassen müssen.

<!-- For UI-based setup (reward providers, event definitions, product inventory, and exclusions), see [Configure loyalty challenges](loyalty-admin.md). -->
