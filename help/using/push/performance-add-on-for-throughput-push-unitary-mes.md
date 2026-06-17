---
solution: Journey Optimizer
product: journey optimizer
title: Leistungs-Add-on für Durchsatz - (Push) Unitär - Nachrichtenversand
description: Erfahren Sie, wie Sie das Leistungs-Add-on für „Durchsatz - (Push) Unitär - Nachrichtenversand“ in Adobe Journey Optimizer konfigurieren und verwenden.
feature: Push
topic: Content Management
role: User
level: Intermediate
exl-id: 2d0677ad-41c8-4299-a7c8-0e4f8a1716f7
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 4%

---


# Leistungs-Add-on für Durchsatz - (Push) Unitär - Nachrichtenversand {#performance-add-on-for-throughput-push-unitary-mes}

>[!AVAILABILITY]
>
>Diese Funktion ist verfügbar unter **AJO26.7** (2026-07-27).

## Überblick {#overview}

Adobe Journey Optimizer führt **Performance-Add-on für Durchsatz - (Push) Unitär - Nachrichtenversand** ein, mit dem Unternehmen relevantere, personalisierte Kundenerlebnisse über Push-Kanäle hinweg bereitstellen können.

Auf dieser Seite wird erläutert, wie Sie diese Funktion in Ihren Kampagnen und Journey konfigurieren und verwenden.

## Voraussetzungen {#prerequisites}

Bevor Sie beginnen:

* Sie haben Zugriff auf Adobe Journey Optimizer mit den erforderlichen **Push**-Berechtigungen.
* Eine Push-Kanaloberfläche ist konfiguriert. Siehe [Konfigurieren eines Push-Kanals](../configuration/channel-surfaces.md).

## Funktionsweise {#how-it-works}

Leistungs-Add-on für Durchsatz - (Push) Unitär - Die Nachrichtenbereitstellung ist direkt mit der AJO-Ausführungs-Engine integriert. Wenn ein Profil eine Push-Aktion in einer Journey oder Kampagne erreicht, wendet die Funktion die konfigurierten Parameter zum Sendezeitpunkt an.

Wichtigste Funktionen:

* **Personalisierung auf Profilebene** - Die Einstellungen werden mithilfe von Profil- und Kontextattributen je Empfänger angepasst.
* **Journey- und Kampagnenunterstützung** - funktioniert sowohl in orchestrierten Journey- als auch in Einzelkampagnen.
* **Echtzeitmetriken** - Ergebnisse werden in den [Push-Berichten](../reports/push-report.md) angezeigt.

## Leistungs-Add-on für Durchsatz konfigurieren {#configure}

1. Navigieren Sie im linken AJO-Menü zu **Kanäle** > **Push-Konfigurationen**.
1. Wählen oder erstellen Sie eine Kanalkonfiguration.
1. Aktivieren **im Abschnitt „Leistungs-Add-on für**&quot; die Funktion.
1. Legen Sie die erforderlichen Parameter fest.
1. Klicken Sie auf **Speichern**.

>[!NOTE]
>
>Konfigurationsänderungen gelten für neue Journey-Ausführungen. Laufende Journey sind davon nicht betroffen.

## Verwandte Themen {#related-topics}

* [Erste Schritte mit Push-Benachrichtigungen](get-started-push.md)
* [Push-Benachrichtigung erstellen](create-push.md)
* [Versionshinweise zu AJO 26.7](../rn/release-notes.md)
