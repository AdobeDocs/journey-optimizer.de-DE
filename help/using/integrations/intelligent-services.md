---
solution: Journey Optimizer
product: journey optimizer
title: Integrieren mit Intelligent Services
description: Erfahren Sie, wie Sie Adobe Intelligent Services und Prognosen zur Kunden-KI in Journey Optimizer nutzen können
feature: Journeys, Integrations
topic: Artificial Intelligence
role: User
level: Intermediate
keywords: künstlich, KI, intelligent, Journey, Service
exl-id: 20da09e1-0611-4d27-a589-30552011e06c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/rTKcWHwfwleQtD68fcdeqYK2AMQHVaknKtsNDFsOldI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 16%

---

# Integration mit Intelligent Services {#ai-overview}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Adobe Intelligent Services- und Kunden-KI-Prognosen mit Journey Optimizer integrieren, um Abwanderungs- und Konversionswerte als Profilattribute für Entscheidungen, Aktionen und die Segmenterstellung zu verwenden.

>[!ENDSHADEBOX]

Die Integration mit **[!DNL Adobe Intelligent Services]** ermöglicht die Nutzung von künstlicher Intelligenz und maschinellem Lernen in Anwendungsfällen mit Kundenerlebnissen. So können Marketing-Analystinnen und -Analysten mithilfe von Konfigurationen auf Unternehmensebene spezifische Prognosen für die Anforderungen der Firma erstellen, ohne dass hierfür Kenntnisse aus der Datenwissenschaft erforderlich sind.

[!DNL Intelligent Services], das auf [!DNL Adobe Experience Platform] basiert, bietet KI als Service für Kundenerlebnis-Teams. Es hilft bei der Vorhersage des Kundenverhaltens, der Messung der Kampagnenwirkung und der Verbesserung des ROI. Weitere Informationen finden Sie in der [[!DNL Adobe Experience Platform] Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/home.html?lang=de){target="_blank"}.

Durch die Integration von [!DNL Journey Optimizer] mit [!DNL Intelligent Services] können Sie Kundenprognosen nutzen.

Kunden-KI, eine Komponente von [!DNL Adobe Intelligent Services], sagt wahrscheinliche Kundenaktionen voraus. Weitere Informationen finden Sie in der [[!DNL Adobe Experience Platform] Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/overview.html?lang=de){target="_blank"}.

Mit Kunden-KI können Marken auf maschinellem Lernen basierende Abwanderungs- oder Konversionsbewertungen erstellen. Diese Bewertungen sind als Profilattribute in [!DNL Adobe Experience Platform] (Echtzeit-Kundenprofil) verfügbar.

Daher können diese Attribute wie alle anderen Profilattribute in Journey Optimizer verwendet werden. Verwenden Sie sie in Bedingungen für Entscheidungen, Aktionen oder die Segmenterstellung.

![Kunden-KI-Integration mit Tendenzwerten und Prognosen](assets/customer-ai.png)

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

- **TL;DR:** Auf dieser Seite wird erläutert, wie Journey Optimizer mit Adobe Intelligent Services integriert wird, insbesondere mit Kunden-KI, um auf maschinellem Lernen basierende Tendenzwerte als Profilattribute in Journey zu nutzen.

**intents:**
- Integration von Adobe Intelligent Services mit Journey Optimizer
- Kunden-KI-Tendenzwerte als Profilattribute in Journey-Bedingungen oder -Aktionen verwenden
- KI-gestützte Prognosen für Abwanderung oder Konversion ermöglichen, ohne dass datenwissenschaftliche Kenntnisse erforderlich sind
- Anwenden von maschinellen Lernergebnissen auf die Segmenterstellung in Journey Optimizer

**Glossar:**
- **Adobe Intelligent Services**: Eine Suite von KI-/ML-Services, die auf Adobe Experience Platform basieren und Kundenerlebnisprognosen ermöglichen, ohne dass datenwissenschaftliches Fachwissen erforderlich ist *(produktspezifisch)*
- **Kunden-KI**: Eine Komponente von Adobe Intelligent Services, die auf maschinellem Lernen basierende Abwanderungs- oder Konversionsneigungswerte für Kundenprofile generiert *(produktspezifisch)*
- **Tendenzwert**: Ein auf maschinellem Lernen basierender Wert, der die Wahrscheinlichkeit darstellt, dass ein Kunde eine bestimmte Aktion ausführt (z. B. Abwanderung oder Konversion) und als Profilattribut *produktspezifisch) gespeichert wird*

**Leitplanken:**
- Es ist kein datenwissenschaftliches Fachwissen erforderlich, aber die Konfiguration auf Unternehmensebene muss von Marketing-Analysten abgeschlossen werden
- Kunden-KI-Bewertungen müssen zunächst in Adobe Experience Platform konfiguriert werden, bevor sie als Profilattribute in Journey Optimizer verfügbar sind

**Terminologie:**
- Kanonischer Name: Adobe Intelligent Services — Akronym: none — Varianten: Intelligent Services, KI-Services
- Kanonischer Name: Kunden-KI — Akronym: Keine — Varianten: Kunden-KI-Bewertungen, Tendenz-Bewertungen
- Synonyme: „churn score“ = „churn propensity“ ; „conversion score“ = „conversion propensity“
- Verwechseln Sie nicht: &quot;Adobe Intelligent Services“ ≠ „KI-Assistent“ (Intelligent Services ist eine prädiktive ML-Plattform; KI-Assistent ist eine Gesprächsoberfläche)

**FAQ:**
- **F: Was ist Kunden-KI im Kontext von Journey Optimizer?** - Kunden-KI ist eine Adobe Intelligent Services-Komponente, die auf maschinellem Lernen basierende Abwanderungs- oder Konversionswerte erstellt, die als Profilattribute verfügbar werden, die in Journey Optimizer-Bedingungen, -Aktionen und bei der Segmenterstellung verwendet werden können.
- **F: Benötige ich datenwissenschaftliche Kenntnisse, um Adobe Intelligent Services zu nutzen?** - Nein, Marketing-Analysten können Prognosen mithilfe von Einstellungen auf Unternehmensebene konfigurieren, ohne dass datenwissenschaftliche Kenntnisse erforderlich sind.
- **F: Wo werden Kunden-KI-Bewertungen gespeichert?** - Sie werden als Profilattribute im Echtzeit-Kundenprofil von Adobe Experience Platform gespeichert und sind somit wie jedes andere Profilattribut in Journey Optimizer verfügbar.
- **F: Wie kann ich Kunden-KI-Werte in einem Journey verwenden?** — Sobald als Profilattribute verfügbar, können die Bewertungen in Bedingungen für die Entscheidungsfindung, in Aktionskonfigurationen oder zum Erstellen von Zielgruppensegmenten verwendet werden.

+++
