---
title: Erste Schritte mit Entscheidungsrichtlinien
description: Erfahren Sie, wie Sie mithilfe von Entscheidungsrichtlinien Angebote unterbreiten können.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: c2388c84346ed9a0409270fd96f3a1458bf8ad88
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 98%

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

>[!AVAILABILITY]
>
>Derzeit stehen Entscheidungsrichtlinien allen Kundinnen und Kunden für den Kanal „Code-basierten Erlebnis“ zur Verfügung. Für den E-Mail-Kanal sind sie eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

## Wichtige Schritte {#key}

Die Hauptschritte zur Nutzung von Entscheidungsrichtlinien in Nachrichten lauten wie folgt:

1. [Erstellen einer Entscheidungsrichtlinie](../experience-decisioning/create-decision-policy.md)

   Richten Sie in Ihrer Nachricht eine Entscheidungsrichtlinie ein, indem Sie die Anzahl der zurückzugebenden Elemente auswählen und Auswahlstrategien, Fallback-Optionen und die Auswertungsreihenfolge konfigurieren.

1. [Verwenden der Entscheidungsrichtlinie in Ihren Inhalten](../experience-decisioning/use-decision-policy.md)

   Personalisieren Sie Ihren Inhalt mit der Ausgabe der Entscheidungsrichtlinie und den Attributen der Entscheidungselemente, die in der Nachricht angezeigt werden sollen.

1. [Erstellen von Reporting-Dashboards](cja-reporting.md)

   Erstellen Sie benutzerdefinierte Customer Journey Analytics-Dashboards, um die Leistung zu messen und Einblicke in die Bereitstellung und Interaktion Ihrer Entscheidungsrichtlinien und Angebote zu erhalten.

## Leitlinien und Einschränkungen

* **E-Mail-Mirror-Seiten**: Derzeit werden Entscheidungselemente in E-Mail-Mirror-Seiten nicht gerendert.
* **Tracking- und Link-Typ**: Zum Nachverfolgen von Links, die von der Entscheidungsfindung generiert wurden, definieren Sie sie im Schema als „Decisioning Assets“. Attributbasierte Links können nicht nachverfolgt werden.
* **Verschachtelung von Entscheidungsrichtlinien in E-Mails**: Sie können nicht mehrere Entscheidungsrichtlinien in einer übergeordneten E-Mail-Komponente verschachteln, die bereits mit einer Entscheidungsrichtlinie verknüpft ist.
* **Duplizierte Journeys oder Kampagnen mit Entscheidungsfindung**: Wenn Sie eine Journey oder Kampagne duplizieren, die eine Entscheidungsrichtlinie enthält, verweist die duplizierte Version auf die ursprüngliche E-Mail oder das Code-basierte Erlebnis, was zu Fehlern führt. Die Entscheidungsrichtlinie muss nach einer Duplizierung immer neu konfiguriert werden.
* **Einverständnisrichtlinien**: Es dauert bist zu 48 Stunden bis Aktualisierungen von Einverständnisrichtlinien wirksam werden. Wenn eine Entscheidungsrichtlinie auf ein Attribut verweist, das mit einer kürzlich aktualisierten Einverständnisrichtlinie verknüpft ist, werden die Änderungen nicht sofort angewendet.

  Wenn neue Profilattribute, die einer Einverständnisrichtlinie unterliegen, zu einer Entscheidungsrichtlinie hinzugefügt werden, sind sie ebenfalls verwendbar, aber die mit ihnen verknüpfte Einverständnisrichtlinie wird erst erzwungen, wenn die Verzögerungszeit vorüber ist.

  Einverständnisrichtlinien sind nur für Organisationen verfügbar, die über das Zusatzangebot „Adobe Healthcare Shield“ oder „Privacy and Security Shield“ verfügen.

* **KI-Rangfolge**: Derzeit wird die KI-Rangfolge für den E-Mail-Kanal in Journeys mit Entscheidungsfindung nicht unterstützt.

## Nächste Schritte {#next-steps}

Nachdem Sie nun wissen, wie Entscheidungsrichtlinien funktionieren und wie sie Ihnen bei der Bereitstellung personalisierter Angebote helfen, können Sie Ihre erste Entscheidungsrichtlinie erstellen.

➡️ [Informationen zum Erstellen von Entscheidungsrichtlinien](../experience-decisioning/create-decision-policy.md)

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie mit Decisioning E-Mails für Ihre Audience personalisieren können.

>[!VIDEO](https://video.tv.adobe.com/v/3479199?quality=12)
