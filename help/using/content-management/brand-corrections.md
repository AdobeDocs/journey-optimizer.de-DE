---
solution: Journey Optimizer
product: journey optimizer
title: KI-gestützte Markenkorrekturen
description: Erfahren Sie, wie Sie KI-gestützte Markenkorrekturen in Adobe Journey Optimizer konfigurieren und verwenden.
feature: Brand Guidelines
topic: Content Management
role: User
level: Intermediate
exl-id: a872a3a4-f05b-439d-923e-5191b6e06d34
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 3%

---


# KI-gestützte Markenkorrekturen und redaktionelle Vorschläge {#brand-corrections-ai}

>[!AVAILABILITY]
>
>Diese Funktion steht Adobe Journey Optimizer-Benutzern mit aktiven Markenrichtlinien und Berechtigungen für KI-Assistenten zur Verfügung. Wenden Sie sich an den Adobe-Support, um weitere Informationen zu erhalten.

## Überblick {#overview}

Adobe Journey Optimizer erweitert seine GenAI-gestützten Marken-Compliance-Tools auf alle unterstützten Inhaltskanäle - SMS, Push-Benachrichtigungen, Web-Inhalte und E-Mails. Wenn die Qualitätssicherungs-Engine für Marken Inhalte erkennt, die gegen Markenrichtlinien verstoßen oder die redaktionellen Qualitätskriterien nicht erfüllen, generiert das System automatisch korrigierte Alternativen, die Sie direkt im Authoring-Workflow überprüfen und anwenden können.

Dadurch wird die Markenvalidierung von einer passiven Checkliste in ein aktives Erlebnis mit sofortiger Wirkung umgewandelt. Anstatt Verstöße zu identifizieren und zum Editor zurückzukehren, um jedes Problem manuell zu beheben, erhalten Inhaltsautoren zielgerichtete, KI-generierte Vorschläge, die mit der etablierten Markensprache, dem Ton und den Stilrichtlinien des Unternehmens übereinstimmen - und das alles, ohne den Inhaltseditor zu verlassen.

Diese Funktion wurde für Marketing-Experten, Werbetexter und Kampagnenverantwortliche entwickelt, die Inhalte schnell von Entwurf zu Aktivierung verschieben und gleichzeitig die Markenkonformität im benötigten Umfang aufrechterhalten müssen.

## Voraussetzungen {#prerequisites}

Bevor Sie KI-gestützte Markenkorrekturen verwenden, bestätigen Sie Folgendes:

- **Markenrichtlinien** werden in Adobe Journey Optimizer konfiguriert. Ohne ein aktives Markenprofil kann das System keine markenspezifischen Korrekturvorschläge generieren.
- Die **KI-Assistent**-Funktion ist für Ihre Adobe Experience Cloud-Organisation aktiviert.
- Sie verfügen über die entsprechenden Berechtigungen, um Inhalte für den entsprechenden Kanal (SMS, Push, Web oder E-Mail) zu erstellen und zu bearbeiten.
- Mindestens ein Inhaltselement ist im Journey Optimizer-Inhaltseditor zur Überprüfung verfügbar.

>[!NOTE]
>
>Vorschläge zur Markenkorrektur werden mithilfe der generativen KI-Infrastruktur von Adobe generiert und unterliegen den für Ihr Unternehmen geltenden Nutzungsrichtlinien für KI-Assistenten. Vor der Veröffentlichung stets die akzeptierten Vorschläge prüfen.

## Funktionsweise {#how-it-works}

Markenkorrekturen werden direkt in den Validierungsablauf für die Markenvalidierung im Journey Optimizer-Inhaltseditor integriert. Der End-to-End-Prozess funktioniert wie folgt.

**Schritt 1 - QA-** für Markenbezeichnungen: Wenn Sie eine Überprüfung Ihrer Markendarstellung durchführen (entweder manuell im Prüfungsfenster oder durch eine Workflow-Regel ausgelöst), bewertet das System jeden Inhaltsbaustein anhand Ihrer konfigurierten Markenrichtlinien. Die Prüfungen betreffen den Ton der Stimme, die Terminologie, die verbotene Sprache, redaktionelle Standards und rechtliche Anforderungen.

**Schritt 2 - Erkennung und Kennzeichnung von Verstößen**: Jedes Inhaltssegment, das nicht den Branding- oder redaktionellen Qualitätskriterien entspricht, wird mit einem Indikator für einen Verstoß gekennzeichnet. Die Art des Verstoßes - z. B. Tonabweichung, unzulässige Verwendung von Begriffen oder Nichteinhaltung von Richtlinien - wird neben dem markierten Segment angezeigt, damit Autoren genau verstehen, was geändert werden muss.

**Schritt 3 - Generieren von KI-**: Für jedes gekennzeichnete Segment generiert Journey Optimizer automatisch eine oder mehrere korrigierte Alternativen mithilfe des KI-Assistenten. Vorschläge basieren auf Ihren aktiven Markenrichtlinien und stellen sicher, dass der empfohlene Text die richtige Stimme, Terminologie und den richtigen redaktionellen Stil für Ihr Unternehmen widerspiegelt.

**Schritt 4 - Inline-Vorschau und -**: Die vorgeschlagenen Korrekturen werden inline direkt neben dem markierten Inhalt im Seitenbereich für die Markenvalidierung angezeigt. Sie können den Originaltext mit der KI-generierten Alternative vergleichen, ohne den Editor zu verlassen.

**Schritt 5 - Akzeptieren oder**: Akzeptieren eines Vorschlags mit einem Klick, um den markierten Inhalt durch die korrigierte Version zu ersetzen. Alternativ können Sie den Vorschlag ablehnen und den Inhalt manuell bearbeiten. Durch die Annahme eines Vorschlags wird der Inhaltsbaustein sofort aktualisiert und der Verstoß im QS-Bedienfeld als behoben markiert.

**Schritt 6 - Erneute Validierung**: Führen Sie nach der Anwendung der Korrekturen die Brand QA-Prüfung erneut durch, um zu bestätigen, dass alle Verstöße behoben wurden, bevor Sie den Inhalt auf einer Journey oder in einer Kampagne veröffentlichen oder aktivieren.

## Konfigurieren {#configure}

Über die Standardvoraussetzungen hinaus ist keine zusätzliche Konfiguration erforderlich. Die Funktion wird automatisch im QS-Bedienfeld „Marke“ aktiviert, wenn ein Markenprofil mit Ihrem Inhalt verknüpft und der KI-Assistent für Ihr Unternehmen aktiviert ist.

So verwenden Sie zunächst KI-gestützte Markenkorrekturen:

1. Öffnen Sie den Inhaltseditor für den entsprechenden Kanal - SMS, Push-Benachrichtigung, Web oder E-Mail.
2. Wählen Sie in der Editor-Symbolleiste **Markenrichtlinien** und wählen Sie im Dropdown-Menü das entsprechende Markenprofil aus.
3. Erstellen oder öffnen Sie Ihren Inhalt und wählen Sie dann **Marken-QA** aus dem Überprüfungsfeld aus, um einen Scan zu starten.
4. Überprüfen Sie die markierten Verstöße im seitlichen Bedienfeld **Qualitätssicherung** Marke“. Für jedes gekennzeichnete Element wird automatisch ein KI-generierter Vorschlag angezeigt.
5. Klicken Sie **Anwenden**, um einen Vorschlag anzunehmen, oder **Verwerfen**, um die Korrektur manuell vorzunehmen.
6. Führen Sie **Markenüberprüfung** erneut aus, um zu überprüfen, ob alle Verstöße behoben wurden, und fahren Sie dann mit Ihrem standardmäßigen Genehmigungs- oder Aktivierungs-Workflow fort.

### Unterstützte Kanäle {#supported-channels}

KI-gestützte Markenkorrekturen sind für die folgenden Inhaltstypen in Adobe Journey Optimizer verfügbar:

| Kanal | Unterstützte Inhaltselemente |
|---|---|
| **E-Mail** | Betreffzeile, Preheader, Textkörper, CTA-Kennzeichnungen |
| **SMS** | Nachrichtentext |
| **Push-Benachrichtigungen** | Titel, Textkörper |
| **Web** | Überschrift, Textkörper, Schaltflächenbeschriftungen |

>[!NOTE]
>
>Die unterstützten Inhaltselemente können je nach Konfiguration Ihres Kanals und den in Ihrem Markenprofil definierten Markenrichtlinien variieren. Die Validierung von Bildern und visuellen Assets ist nicht für KI-generierte Textkorrekturen vorgesehen.

## Wichtigste Vorteile {#key-benefits}

**Geringerer manueller Bearbeitungsaufwand**: Inhaltsautoren müssen nicht mehr für jedes gekennzeichnete Problem manuell auf Markenrichtlinien verweisen. KI-Vorschläge tauchen anwendungsbereite Alternativen auf, wodurch sich die im Korrekturzyklus verbrachte Zeit drastisch verkürzt.

**Konsistente Markenkonformität**: Korrekturen basieren auf denselben Markenrichtlinien, die für die Validierung verwendet werden. Akzeptierte Vorschläge gewährleisten über alle Kanäle hinweg die Konsistenz mit der genehmigten Markensprache und den redaktionellen Standards und verringern so das Risiko inkonsistenter Botschaften in Multi-Channel-Kampagnen.

**Schnellere Inhaltserstellung**: Durch die Umwandlung der Marken-QA in einen optimierten, sofort nutzbaren Workflow verschieben Teams Inhalte schneller durch den Prüfzyklus, wodurch die Durchlaufzeit zwischen Entwurf und Aktivierung verkürzt wird. Campaign-Benutzende können eine ganze Reihe von Verstößen in einem einzigen Durchgang beheben, ohne zwischen Tools wechseln zu müssen.

**Kanalübergreifende Abdeckung**: Unabhängig davon, ob eine SMS-Kampagne, eine mobile Push-Sequenz oder eine Web-In-App-Nachricht erstellt wird, sind die Vorschläge zur Markenkorrektur konsistent auf allen unterstützten Inhaltsoberflächen verfügbar, sodass sichergestellt ist, dass die Markenstandards überall eingehalten werden, wo Ihre Marke kommuniziert.

## Verwandte Themen {#related-topics}

- [Erste Schritte mit Markenrichtlinien](../content-management/brands.md)
- [Verwenden des KI-Assistenten für die Inhaltserstellung](../content-management/ai-assistant.md)
- [Erstellen einer SMS-Nachricht](../sms/create-sms.md)
- [Erstellen einer Push-Benachrichtigung](../push/create-push.md)
- [Erste Schritte mit dem Web-Kanal](../web/get-started-web.md)
- [Anzeigen einer Vorschau und Testen der Inhalte](../content-management/preview-test.md)
