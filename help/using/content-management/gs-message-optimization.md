---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Inhaltsoptimierung
description: Erfahren Sie, wie Sie mit der Inhaltsoptimierung personalisierte und optimierte Inhalte in Ihren Kampagnen und Journey bereitstellen können.
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: Optimierung, Zielgruppenbestimmung, Experimentieren, A/B-Tests, Kampagnen, Journey, Personalisierung
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
TQID: https://experienceleague.adobe.com/zJTy0y-AhGMaFPzA379m4D9RxyzUfzCLZkr1B1ffuZM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ea4139d9-3405-4b34-ad6e-c3ca120cc269
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: f29a52db-c90c-4345-902e-b586d1406d8d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 16%

---

# Erste Schritte mit Inhaltsoptimierung {#message-optimization}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_optimization"
>title="Inhaltsoptimierung"
>abstract="Mit der Inhaltsoptimierung in Journey Optimizer können Sie verschiedene Versionen Ihrer Inhalte testen, um zu ermitteln, welche Version die beste Leistung bietet. Sie können Targeting verwenden, um personalisierte Inhalte für bestimmte Segmente bereitzustellen, Experimente durchführen, um mehrere Varianten zu testen, oder beide Ansätze für anspruchsvolle Optimierungsstrategien kombinieren."

Mit der Inhaltsoptimierung können Sie die richtige Botschaft zur richtigen Zeit an die richtige Zielgruppe senden. Durch die Kombination datengesteuerter Einblicke mit leistungsstarken Personalisierungsfunktionen können Sie die Interaktion und Konversionen in all Ihren Kampagnen und Journey maximieren.

Die Inhaltsoptimierung ist sowohl in [Kampagnen](../campaigns/create-campaign.md) als auch in [Journey](../building-journeys/journey-gs.md) verfügbar, sodass Sie auf all Ihre Kunden-Touchpoints dieselben Optimierungsstrategien anwenden können.

➡️ [Erfahren Sie in diesem Video, wie Sie die Inhaltsoptimierung innerhalb einer Kampagne nutzen können](#video)

## Optimierungsfunktionen {#capabilities}

Mit der Inhaltsoptimierung in Journey Optimizer können Sie:

* [Zielgruppenbestimmung verwenden](optimization-targeting.md) um personalisierte Inhalte für bestimmte Zielgruppensegmente basierend auf Profilattributen, Kontextdaten oder der Zielgruppenzugehörigkeit bereitzustellen.

* [Führen Sie Experimente &#x200B;](optimization-experimentation.md), um mehrere Inhaltsvarianten zu testen und anhand Ihrer Erfolgsmetriken zu ermitteln, welche am besten abschneidet.

* [Kombinieren Sie beide Ansätze](optimization-combination.md) um komplexe Optimierungsstrategien zu erstellen, mit denen Sie verschiedene Varianten für jedes Zielsegment testen können.

## Targeting vs. Experimentieren {#targeting-vs-experimentation}

Wenn Sie den Unterschied zwischen Targeting und Experimentieren verstehen, können Sie den richtigen Optimierungsansatz für Ihre Ziele wählen.

**Targeting** verwendet deterministische Regeln, um personalisierte Inhalte basierend auf bekannten Profilattributen, dem Kontext oder der Zielgruppenzugehörigkeit für bestimmte Segmente bereitzustellen. Dadurch wird sichergestellt, dass die richtige Botschaft die richtige Zielgruppe erreicht.

**Experimentieren** verwendet die zufällige Zuweisung, um mehrere Inhaltsvarianten zu testen und festzustellen, welche am besten funktioniert. So erfahren Sie durch datengesteuerte Tests, was bei Ihrer Zielgruppe am meisten Anklang findet.

In der folgenden Tabelle sind die wichtigsten Unterschiede zusammengefasst:

| Funktion | Targeting | Experimentieren |
|--------|-----------|-----------------|
| **Zuweisungsmethode** | Deterministisch - basierend auf Regeln | Zufällig - basierend auf der Traffic-Zuordnung |
| **basierend auf** | Profilattribute, Kontext, Zielgruppen | Zufällige Verteilung |
| **Anwendungsfall** | Bereitstellen relevanter Inhalte für bekannte Segmente | Finden Sie heraus, welche Inhalte am besten funktionieren |
| **Beispiel** | Unterschiedliche Promotions nach Standort anzeigen | Testen Sie zwei Betreffzeilen, um zu sehen, welche mehr Öffnungen erhalten |
| **Geeignet für** | Personalization im großen Maßstab | Optimierung und Lernen |

![](../campaigns/assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## Häufige Anwendungsfälle {#use-cases}

Im Folgenden finden Sie einige typische Szenarien, in denen die Inhaltsoptimierung zu besseren Ergebnissen führen kann:

Zielgruppenbestimmung:

* **Geo-Targeting** - Senden Sie standortspezifische Angebote, je nachdem, wo sich Ihre Kunden befinden. Werben Sie beispielsweise für Wintermäntel in kälteren Regionen und für Badebekleidung in wärmeren Klimazonen.

* **Geräteoptimierung** - Stellen Sie gerätespezifische Inhalte bereit, z. B. Desktop-optimierte Layouts für Desktop-Benutzer und für Smartphones optimierte Layouts.

Experimentieren:

* **A/B-Tests** - Testen Sie verschiedene E-Mail-Betreffzeilen, call-to-action-Schaltflächen oder Werbeangebote, um herauszufinden, welche die meisten Konversionen fördern.

* **Lifecycle Marketing** - Testen Sie verschiedene Onboarding-Nachrichten für neue Kunden im Vergleich zu Archivierungsangeboten für bestehende Kunden.

Kombination:

* **Erweiterte Segmentierung** Targeting von Kundinnen und Kunden nach Treuestufe und Testen verschiedener Belohnungsbotschaften innerhalb jeder Stufe, um die Interaktion über alle Segmente hinweg zu maximieren.

## Erste Schritte {#get-started}

So optimieren Sie Ihren Inhalt:

1. **Erstellen einer Kampagne oder Journey**: Richten Sie Ihre [Kampagne](../campaigns/create-campaign.md) oder [Journey ein &#x200B;](../building-journeys/journey-gs.md) fügen Sie mindestens eine Aktion hinzu.

1. **Wählen Sie Ihren Optimierungsansatz**:
   * [Verwenden Sie Targeting](optimization-targeting.md) um Inhalte für bestimmte Segmente zu personalisieren.
   * [Experimentieren](optimization-experimentation.md) um mehrere Varianten zu testen.
   * [Kombinieren Sie beide](optimization-combination.md) für eine erweiterte Optimierung.

1. **Inhalt definieren**: Erstellen Sie die verschiedenen Inhaltsvarianten für Ihre Optimierungsstrategie.

1. **Aktivieren und Überwachen**: Starten Sie Ihre optimierte Kampagne oder Ihr optimiertes Journey und verfolgen Sie die Leistung in den [Berichten](../reports/campaign-global-report-cja.md).

## Funktionsweise {#how-it-works}

Sobald Ihr Journey oder Ihre Kampagne live ist, werden die Profile anhand der von Ihnen definierten Kriterien bewertet. Basierend auf diesen Auswertungen erhält jedes Profil die am besten geeignete Inhaltsversion:

1. **Profilevaluierung** - Wenn ein Profil in Ihre Kampagne oder Ihr Journey eintritt, wertet Journey Optimizer seine Attribute und den Kontext aus.

1. **Inhaltszuweisung** - basierend auf Ihrer Optimierungskonfiguration:
   * Beim **Targeting** erhalten Profile, die bestimmten Kriterien entsprechen, die entsprechenden personalisierten Inhalte.
   * Für **Experimentieren** werden Profile auf der Grundlage Ihrer Traffic-Zuordnungseinstellungen nach dem Zufallsprinzip verschiedenen Inhaltsvarianten zugewiesen.
   * Für **Kombinationen** stimmen Profile zunächst mit einer Zielgruppenbestimmungsregel überein und werden dann nach dem Zufallsprinzip einer der Experimentvarianten für dieses Segment zugewiesen.

1. **Leistungs-Tracking** - Journey Optimizer verfolgt automatisch Interaktionsmetriken und Konversionsdaten, um festzustellen, welche Inhalte am besten funktionieren.

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie die Inhaltsoptimierung in durch eine Aktion oder API ausgelösten Kampagnen nutzen können. Sie erfahren, wie Sie Teilzielgruppen ansprechen, Nachrichtenvarianten je nach Standort erstellen, Fallback-Inhalte aktivieren und mehrere Experimente innerhalb einer Kampagne durchführen. In diesem Tutorial wird außerdem beschrieben, wie Sie Multi-Channel-Kampagnen verwalten und dabei die Konsistenz der Nachrichten beibehalten können.

>[!VIDEO](https://video.tv.adobe.com/v/3470368?quality=12)

**Verwandte Themen**

* [Erstellen einer Kampagne](../campaigns/create-campaign.md)
* [Erstellen einer Journey](../building-journeys/journey-gs.md)
* [Inhaltsexperimente](../content-management/get-started-experiment.md)
