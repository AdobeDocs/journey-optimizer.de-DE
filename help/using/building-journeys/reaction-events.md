---
solution: Journey Optimizer
product: journey optimizer
title: Reaktionsereignisse
description: Erfahren Sie, wie Sie mit Reaktionsereignissen auf Nachrichten-Tracking-Daten wie Öffnungen und Klicks in Ihren Journeys reagieren und Timeout-Pfade für nicht antwortende Profile konfigurieren können.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Ereignisse, Reaktion, Tracking, Plattform
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1030
ht-degree: 49%

---

# Reaktionsereignisse {#reaction-events}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mit der Aktivität Reaktion auf Nachrichten-Tracking-Daten wie Öffnungen und Klicks innerhalb derselben Journey reagieren und Zeitüberschreitungspfade für Einzelpersonen konfigurieren, die nicht interagieren.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Reaktionsereignisse"
>abstract="Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine innerhalb derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit, sobald sie für [!DNL Adobe Experience Platform] freigegeben werden."

## Überblick {#overview}

Unter den verschiedenen Ereignisaktivitäten, die in der Palette verfügbar sind, finden Sie das integrierte **[!UICONTROL Reaktionsereignis]**. Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine innerhalb derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit, sobald sie für [!DNL Adobe Experience Platform] freigegeben werden.

Sie können auf angeklickte oder geöffnete Nachrichten reagieren. Beispielsweise können Sie eine weitere Nachricht senden, wenn eine Person die vorherige E-Mail geöffnet oder darin geklickt hat, oder eine andere Folgenachricht senden, wenn sie nicht mit Ihrer Kommunikation interagiert hat.

Siehe [Aktionsaktivitäten](../building-journeys/about-journey-activities.md#action-activities).

Sie können die Aktivität **[!UICONTROL Reaktion]** auch verwenden, um eine Aktion auszuführen, wenn keinerlei Reaktion auf Ihre Nachrichten erfolgt. Erstellen Sie hierfür einen zweiten Pfad parallel zur Aktivität **[!UICONTROL Reaktion]** und fügen Sie eine Aktivität **[!UICONTROL Warten]** hinzu. Wenn während des in der Aktivität **[!UICONTROL Warten]** definierten Zeitraums keine Reaktion erfolgt, wird der zweite Pfad gewählt. Sie können beispielsweise eine Folgenachricht senden.

## Konfigurieren von Reaktionsereignissen {#configure}

![Konfiguration des Reaktionsereignisses mit Optionen zur Kanalauswahl und zum Ereignistyp](assets/journey45.png)

Führen Sie diese Schritte aus, um die Reaktionsereignisse zu konfigurieren:

1. Platzieren Sie eine Aktivität **[!UICONTROL Reaktion]** in der Journey-Arbeitsfläche **unmittelbar** nach einer [Kanalaktionsaktivität](journey-action.md).
1. Fügen Sie der Reaktion ein **[!UICONTROL Label]** hinzu. Dieser Schritt ist optional.
1. Wählen Sie aus der Dropdown-Liste die Aktionsaktivität aus, auf die Sie reagieren möchten. Sie können jede Aktionsaktivität auswählen, die in den vorherigen Schritten des Pfades platziert wurde.
1. Wählen Sie je nach ausgewählter Aktion, auf was Sie reagieren möchten.
1. Sie können das Timeout für ein Ereignis (zwischen 40 Sekunden und 90 Tagen) und einen Timeout-Pfad definieren. Dadurch wird ein zweiter Pfad für Personen erstellt, die nicht innerhalb der festgelegten Zeitspanne reagiert haben. Beim Testen einer Journey, die ein Reaktionseeignis verwendet, beträgt der Standard- und Mindestwert für die **[!UICONTROL Wartezeit]** im Testmodus 40 Sekunden. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/testing-the-journey.md).

## Leitlinien und Einschränkungen {#guardrails-limitations}

* Eine Aktivität **[!UICONTROL Reaktion]** muss in der Journey-Arbeitsfläche **unmittelbar** nach einer [Kanalaktionsaktivität](journey-action.md) platziert werden.
* Eine Aktivität **[!UICONTROL Reaktion]** kann nur verwendet werden, wenn zuvor eine Kanalaktionsaktivität stattgefunden hat.
* Das Platzieren einer Aktivität **[!UICONTROL Warten]** oder einer anderen Aktivität zwischen der Kanalaktion und der Aktivität **[!UICONTROL Reaktion]** wird nicht unterstützt und kann dazu führen, dass die Reaktion nicht wie erwartet funktioniert.
* Reaktionsereignisse können nur Nachrichten verfolgen, die innerhalb derselben Journey gesendet werden. Meldungen, die in einer anderen Journey stattfinden, können nicht verfolgt werden.
* Reaktionsereignisse verfolgen Klicks auf Links des Typs „verfolgt“. Abmeldungs- und Mirrorseiten-Links werden nicht berücksichtigt.
* Das Öffnen von E-Mails wird anhand eines in der E-Mail enthaltenen 0-Pixel-Bildes nachverfolgt. Wenn E-Mail-Clients (z. B. Gmail) Bilder blockieren, werden E-Mail-Öffnungen nicht berücksichtigt.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird erläutert, wie Sie die integrierte Reaktionsereignisaktivität in Adobe Journey Optimizer verwenden können, um Journey-Pfade auf der Grundlage von Echtzeit-Nachrichteninteraktionsdaten wie E-Mail-Öffnungen und Link-Klicks zu verzweigen.

**intents:**
* Fügen Sie die Ereignisaktivität Reaktion hinzu, um auf Nachrichtenöffnungen oder Klicks innerhalb eines Journey zu reagieren
* Konfigurieren Sie eine Zeitüberschreitungsdauer und einen Fallback-Pfad für Profile, die nicht interagieren
* Erstellen Sie einen parallelen Pfad mit der Aktivität Warten , um Nicht-Responder zu verarbeiten
* Wählen Sie eine bestimmte Upstream-Kanalaktionsaktivität aus, die überwacht werden soll

**Glossar:**
* **Reaktionsereignis**: Eine integrierte Journey-Ereignisaktivität, die auf Echtzeit-Tracking-Daten (Öffnungen, Klicks) aus einer Nachricht wartet, die zuvor auf derselben Journey-*gesendet wurde (produktspezifisch)*
* **Zeitüberschreitungspfad**: Eine sekundäre Journey-Verzweigung, der Profile folgen, wenn sie nicht innerhalb des definierten Zeitüberschreitungszeitraums die erwartete Reaktion erzeugen *(produktspezifisch)*

**Leitplanken:**
* Die Reaktionsaktivität muss unmittelbar nach einer Kanalaktionsaktivität platziert werden. Es kann keine andere Aktivität zwischen ihnen platziert werden.
* Eine Reaktionsaktivität kann nicht verwendet werden, wenn zuvor im Pfad keine Kanalaktionsaktivität vorhanden war.
* Reaktionsereignisse können nur Nachrichten verfolgen, die innerhalb derselben Journey gesendet werden. Cross-Journey-Tracking wird nicht unterstützt.
* Abmelde-Links und Mirrorseiten-Links werden von Reaktionsereignissen nicht verfolgt.
* Geöffnete E-Mails basieren auf einem Tracking-Bild mit 0 Pixeln. Wenn der E-Mail-Client Bilder blockiert (z. B. Gmail), werden Öffnungen nicht aufgezeichnet.
* Der maximale Zeitraum für das Ereignis liegt zwischen 40 Sekunden und 90 Tagen. Der Mindestwert im Testmodus beträgt ebenfalls 40 Sekunden.

**Terminologie:**
* Kanonischer Name: Reaktionsereignisse — Akronym: Keine — Varianten: Reaktionsaktivität, Interaktionsverfolgungsereignis
* Synonyme: „Reaktionsereignis“ = „Nachrichteninteraktions-Ereignis“ = „Tracking-Ereignis“
* Verwechseln Sie nicht: „Reaktionsereignis“ ≠ „Externes Ereignis“ (Reaktionsereignisse sind integriert und an Gleich-Journey-Nachrichten gebunden; externe Ereignisse kommen von außerhalb des Journey)

**FAQ:**
* **F: Kann ein Reaktionsereignis eine Nachricht verfolgen, die auf einer anderen Journey gesendet wird?** — Nein; Reaktionsereignisse verfolgen nur Nachrichten, die innerhalb derselben Journey gesendet werden.
* **F: Wie kann ich Profile verwalten, die sich nicht öffnen oder auf eine Nachricht klicken?** — Fügen Sie einen parallelen Pfad neben der Reaktionsaktivität mit der Warteaktivität hinzu. Profile, die nicht innerhalb der Wartezeit reagieren, folgen diesem zweiten Pfad.
* **F: Werden Abmelde-Link-Klicks von Reaktionsereignissen verfolgt?** — Nein; nur getrackte Link-Typen werden erfasst. Abmelde- und Mirrorseiten-Links sind ausgeschlossen.
* **F: Was passiert, wenn ein E-Mail-Client Bilder blockiert?** — Das über das 0-Pixel-Bild verfolgte Öffnen von E-Mails wird für Clients, die Bilder blockieren, wie z. B. Gmail, nicht aufgezeichnet.
* **F: Was ist der gültige Zeitüberschreitungsbereich für ein Reaktionsereignis?** — zwischen 40 Sekunden und 90 Tagen.

+++
