---
title: Erste Schritte mit Entscheidungsrichtlinien
description: Erfahren Sie, wie Sie mithilfe von Entscheidungsrichtlinien Angebote unterbreiten können.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: fb35bc5a51421818297586b5e386aa75deb1c669
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 72%

---

# Erste Schritte mit Entscheidungsrichtlinien {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Was ist eine Entscheidung?"
>abstract="Entscheidungsrichtlinien enthalten die gesamte Auswahllogik, mit der die Entscheidungs-Engine den besten Inhalt auswählt. Entscheidungsrichtlinen sind kampagnenspezifisch. Ihr Ziel ist es, die besten Angebote für jedes Profil auszuwählen, während Sie bei der Kampagnenerstellung angeben können, wie die ausgewählten Entscheidungselemente dargestellt werden sollen, einschließlich der in die Nachricht aufzunehmenden Elemente."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Über Entscheidungsfindung"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="Festlegen einer Entscheidungsrichtlinie"
>abstract="Mit einer Entscheidungsrichtlinie können die besten Elemente aus der Entscheidungs-Engine ausgewählt und an die richtige Zielgruppe gesendet werden."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Über Entscheidungsfindung"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="Entscheidungsrichtlinie"
>abstract="Mit der Entscheidungsrichtlinie können die besten Elemente aus der Entscheidungs-Engine ausgewählt und an jede Zielgruppe gesendet werden."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="Platzierung"
>abstract="Eine Platzierung bestimmt, wo zurückgegebene Elemente aus der Entscheidungs-Engine in einer Nachricht angezeigt werden. Ihre Leistung kann in verschiedenen Berichten über verschiedene Platzierungen hinweg verfolgen."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="Auswählen von Entscheidungsattributen aus dem Katalog"
>abstract="Entscheidungsattribute werden im Schema des Katalogs gespeichert. Wählen Sie ein Attribut aus dem ausgewählten Katalog aus, das Sie hier verwenden möchten."

Entscheidungsrichtlinien sind Container für Ihre Angebote, die die Entscheidungs-Engine nutzen, um dynamisch die besten Inhalte für jedes Zielgruppenmitglied zurückzugeben. Ihr Ziel besteht darin, die besten Angebote für jedes Profil auszuwählen. Beim Kampagnen-/Journey-Authoring wiederum können Sie angeben, wie die ausgewählten Entscheidungselemente dargestellt werden, einschließlich der Elementattribute, die in die Nachricht aufgenommen werden sollen.

➡️ [Funktion im Video kennenlernen](#video)

## Leitlinien und Einschränkungen

* **Unterstützte Kanäle** - Entscheidungsrichtlinien sind für diese Kanäle verfügbar: Code-basierte Erlebnis-, E-Mail-, SMS- und Push-Benachrichtigungen.
* **SDK-Anforderung für Push-Benachrichtigungen** - Experience Decisioning mit Push-Benachrichtigungen erfordert eine bestimmte Version der Mobile SDK. Bevor Sie diese Funktion implementieren, überprüfen Sie die [Versionshinweise](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}, um die erforderliche Version zu identifizieren und sicherzustellen, dass Sie das Upgrade entsprechend durchgeführt haben. Sie können auch alle verfügbaren SDK-Versionen für Ihre Plattform in [diesem Abschnitt](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"} anzeigen.
* **E-Mail-Mirror-Seiten**: Derzeit werden Entscheidungselemente in E-Mail-Mirror-Seiten nicht gerendert.
* **Tracking- und Link-Typ**: Zum Nachverfolgen von Links, die von der Entscheidungsfindung generiert wurden, definieren Sie sie im Schema als „Decisioning Assets“. Attributbasierte Links können nicht nachverfolgt werden.
* **Verschachtelung von Entscheidungsrichtlinien in E-Mails**: Sie können nicht mehrere Entscheidungsrichtlinien in einer übergeordneten E-Mail-Komponente verschachteln, die bereits mit einer Entscheidungsrichtlinie verknüpft ist.
* **Duplizierte Journeys oder Kampagnen mit Entscheidungsfindung**: Wenn Sie eine Journey oder Kampagne duplizieren, die eine Entscheidungsrichtlinie enthält, verweist die duplizierte Version auf die ursprüngliche E-Mail oder das Code-basierte Erlebnis, was zu Fehlern führt. Die Entscheidungsrichtlinie muss nach einer Duplizierung immer neu konfiguriert werden.
* **Einverständnisrichtlinien**: Es dauert bist zu 48 Stunden bis Aktualisierungen von Einverständnisrichtlinien wirksam werden. Wenn eine Entscheidungsrichtlinie auf ein Attribut verweist, das mit einer kürzlich aktualisierten Einverständnisrichtlinie verknüpft ist, werden die Änderungen nicht sofort angewendet.

  Wenn neue Profilattribute, die einer Einverständnisrichtlinie unterliegen, zu einer Entscheidungsrichtlinie hinzugefügt werden, sind sie ebenfalls verwendbar, aber die mit ihnen verknüpfte Einverständnisrichtlinie wird erst erzwungen, wenn die Verzögerungszeit vorüber ist.

  Einverständnisrichtlinien sind nur für Organisationen verfügbar, die über das Zusatzangebot „Adobe Healthcare Shield“ oder „Privacy and Security Shield“ verfügen.

* **KI-Rangfolge**: Derzeit wird die KI-Rangfolge für den E-Mail-Kanal in Journeys mit Entscheidungsfindung nicht unterstützt.

* **Inhaltsvorlagen** - Jede in Ihrem Inhalt konfigurierte Entscheidungsrichtlinie wird nicht in der Vorlage gespeichert. Wenn Sie die Vorlage auf eine andere Aktion anwenden, müssen Sie die Richtlinie neu konfigurieren.

## Wichtige Schritte {#key}

Die Hauptschritte zur Nutzung von Entscheidungsrichtlinien in Nachrichten lauten wie folgt:

1. **Erstellen einer Entscheidungsrichtlinie**

   Fügen Sie Ihrer Nachricht eine Entscheidungsrichtlinie hinzu und konfigurieren Sie die Anzahl der zurückzugebenden Elemente sowie die Auswahlstrategie und die Fallback-Optionen.

   ➡️ [Informationen zum Erstellen von Entscheidungsrichtlinien](../experience-decisioning/create-decision-policy.md)

1. **Verwenden Sie die Entscheidungsrichtlinie in Ihrem Inhalt**

   Personalisieren Sie Ihren Inhalt mit der Ausgabe der Entscheidungsrichtlinie, indem Sie die Attribute aus den Entscheidungselementen einfügen, die Sie in der Nachricht anzeigen möchten

   ➡️ [Informationen zum Verwenden von Entscheidungsrichtlinien in Nachrichten](../experience-decisioning/create-decision-policy.md)

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie mit Decisioning E-Mails für Ihre Audience personalisieren können.

>[!VIDEO](https://video.tv.adobe.com/v/3476173?captions=ger&quality=12)

Erfahren Sie, wie Sie mit Decisioning Push-Benachrichtigungen für Ihre Zielgruppe personalisieren können.

>[!VIDEO](https://video.tv.adobe.com/v/3479219?captions=ger&quality=12)

Erfahren Sie, wie Sie mit Decisioning SMS-Nachrichten für Ihre Zielgruppe personalisieren können.

>[!VIDEO](https://video.tv.adobe.com/v/3479538?captions=ger&quality=12)
