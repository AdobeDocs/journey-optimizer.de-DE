---
solution: Journey Optimizer
product: journey optimizer
title: Zeitzonen-Management
description: Erfahren Sie mehr über das Zeitzonen-Management
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: Zeitzone, Eigenschaften, Journey, Bedingung, Uhrzeit, Datum, benutzerdefiniert
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PdwGEuWqJcncbkokE0eOhMaEk9L0AmCJ--VZBxxtDDU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 996
ht-degree: 30%

---

# Zeitzonen-Management {#timezone_management}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie eine Zeitzone für eine Journey festlegen - entweder eine feste Zeitzone oder eine Zeitzone, die jedem Profil entnommen wird -, um zu steuern, wann zeitbasierte Aktivitäten wie Zeitbedingungen, Datumsbedingungen und benutzerdefinierte Wartezeiten ausgeführt werden.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Journey-Zeitzone"
>abstract="Die Zeitzoneneinstellung definiert die Zeitzone der Journey. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Kontakte gleich, die in die Journey eintreten."


Sie können eine Zeitzone in den [Eigenschaften](../building-journeys/journey-properties.md#timezone) Ihrer Journey festlegen.

Um die Eigenschaften der Journey aufzurufen, wählen Sie das Stiftsymbol oben rechts im Bildschirm aus.

Diese Zeitzone wird für jede Aktivität der Journey verwendet, die ein Zeitelement enthält, z. B.:

* [Zeitbedingung](../building-journeys/conditions.md#time_condition)
* [Bedingung für das Datum](../building-journeys/conditions.md#date_condition)
* [Benutzerdefinierte Wartezeit](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Sie können eine [feste Zeitzone](#fixed-timezone) auswählen oder die Zeitzone verwenden, die [im Benutzerprofil definiert ist](#timezone-from-profiles).

## Definieren einer festen Zeitzone {#fixed-timezone}

Die Zeitzone kann fest definiert werden. Löschen Sie die vordefinierte Zeitzone und wählen Sie eine aus der Dropdown-Liste aus. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Kontakte gleich, die die Journey beginnen.

Wählen Sie dazu im Bereich **[!UICONTROL Journey-Eigenschaften]** eine Zeitzone aus.

![Dropdown-Liste zur Zeitzonenauswahl in Journey-Eigenschaften](assets/journey72.png)

## Zeitzone des Profils verwenden {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Zeitzone des Profils verwenden"
>abstract="Diese Option verwendet die Zeitzone des Echtzeitprofils in den Aktivitäten **Warten** und **Bedingung**. Wenn für ein Profil eine Zeitzone definiert wurde, wird diese abgerufen und in der Journey verwendet. Andernfalls wird die im Zeitzonenfeld definierte Zeitzone verwendet."

Wenn das Eintrittsereignis der Journey über einen Namespace verfügt, d. h. die Journey den Echtzeit-Kundenprofil-Service von [!DNL Adobe Experience Platform] erreichen kann, empfiehlt es sich, die auf Profilebene definierte Zeitzone zu verwenden. Aktivieren Sie dazu in den **Eigenschaften** die Option **Zeitzone des Profils für Wartezeiten und Bedingungen verwenden**. Diese Option ist nicht standardmäßig aktiviert.

Wenn für ein Profil eine Zeitzone definiert wurde, wird diese abgerufen und von der Journey verwendet. Ist dies nicht der Fall, wird die im Zeitzonenfeld definierte Zeitzone verwendet.

![Konfiguration der Zeitzone des Profils in Datenquellen für personalisierte Zeitplanung](assets/journey73.png)

>[!NOTE]
>
>Die Zeitzone des Profils verwendet das Feld **timeZone** in der Feldergruppe **Voreinstellungsdetails**.

## Verwenden von Zeitzonen in Ausdrücken {#timezone-in-expressions}

Das Start- und Enddatum einer Journey kann nicht mit einer bestimmten Zeitzone verknüpft werden. Es wird automatisch mit der Zeitzone der Instanz verbunden.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird erläutert, wie Sie Zeitzoneneinstellungen in den Journey-Eigenschaften von Adobe Journey Optimizer konfigurieren und dabei zwischen einer festen Zeitzone, die auf alle Profile angewendet wird, oder einer pro Profil festgelegten Zeitzone, die aus dem Echtzeit-Kundenprofil bezogen wird, wählen.

**intents:**
* Festlegen einer festen Zeitzone auf einer Journey, sodass alle Profile demselben Zeitverweis für Bedingungen und Wartezeiten folgen
* Aktivieren Sie die Zeitzone pro Profil, sodass die Warte- und Bedingungsaktivitäten die gespeicherte Zeitzoneneinstellung jedes Kontakts verwenden.
* Verstehen, welche Journey-Aktivitäten von der Zeitzoneneinstellung für das Journey beeinflusst werden
* Identifizieren Sie die Profilfeldgruppe, in der der einzelne Zeitzonenwert gespeichert wird

**Glossar:**
* **Feste Zeitzone**: Eine in den Journey-Eigenschaften ausgewählte Zeitzone, die für jedes Profil, das auf die Journey-*zugreift, einheitlich gilt (produktspezifisch)*
* **Zeitzone des Profils**: Die im Feld &quot;`timeZone`&quot; der Feldergruppe „Voreinstellungsdetails“ gespeicherte Zeitzone, die verwendet wird, wenn die Option „Zeitzone des Profils für Wartezeiten und Bedingungen verwenden“ *(produktspezifisch) aktiviert ist*
* **Feldergruppe „Voreinstellungsdetails“**: Die XDM-Feldergruppe, die das `timeZone` enthält, das für die Zeitzonenauflösung auf Profilebene verwendet wird

**Leitplanken:**
* Die Option „Zeitzone des Profils in Wartezeiten und Bedingungen verwenden“ ist nur verfügbar, wenn das Eintrittsereignis der Journey einen Namespace hat (d. h. die Journey kann den Echtzeit-Kundenprofil-Service erreichen)
* Die Option ist standardmäßig nicht aktiviert. Die feste Zeitzone wird verwendet, sofern sie nicht explizit aktiviert ist
* Wenn die Option aktiviert ist, aber keine Zeitzone für das Profil definiert ist, wird die feste Zeitzone für den Journey in den Journey-Eigenschaften verwendet
* Start- und Enddatum von Journey können nicht mit einer bestimmten Zeitzone verknüpft werden. Sie werden automatisch mit der Zeitzone der Instanz verknüpft

**Terminologie:**
* Kanonischer Name: Zeitzonenverwaltung — Akronym: none — Varianten: Zeitzonenkonfiguration, Journey-Zeitzone
* Synonyme: „Feste Zeitzone“ = „Für alle Personen gleich“; „Zeitzone des Profils“ = „Zeitzone des Profils für Wartezeiten und Bedingungen verwenden“
* Verwechseln Sie nicht: &quot;Journey-Zeitzone“ (gilt für Aktivitäten) ≠ „Zeitzone der Instanz“ (gilt für Start-/Enddaten der Journey, wird automatisch festgelegt)

**FAQ:**
* **F: Wo kann ich die Zeitzone für eine Journey festlegen?** - Im Bereich Journey-Eigenschaften, der über das Stiftsymbol oben rechts auf der Journey-Arbeitsfläche zugänglich ist.
* **F: Welche Aktivitäten verwenden die Journey-Zeitzone?** — Zeitbedingungen, Datumsbedingungen und benutzerdefinierte Warteaktivitäten.
* **F: Wie kann ich jedes Profil dazu bringen, seiner eigenen lokalen Zeitzone zu folgen?** — Aktivieren Sie in den Journey-Eigenschaften die Option „Zeitzone des Profils für Wartezeiten und Bedingungen verwenden“. Dazu muss die Journey über einen Namespace verfügen, damit sie den Echtzeit-Kundenprofil-Service erreichen kann.
* **F: Was passiert, wenn für ein Profil keine Zeitzone definiert ist und die Option für die Zeitzone des Profils aktiviert ist?** — Die Journey wird auf die feste Zeitzone zurückgesetzt, die im Zeitzonenfeld in den Journey-Eigenschaften definiert ist.
* **F: In welchem Profilfeld wird die Zeitzone des Kontakts gespeichert?** - Das `timeZone` Feld innerhalb der Feldergruppe „Voreinstellungsdetails“ im Profilschema.
* **F: Kann ich das Start- und Enddatum der Journey auf eine bestimmte Zeitzone festlegen?** — Nein. Start- und Enddatum des Journey werden automatisch mit der Zeitzone der Instanz verknüpft und können nicht mit einer benutzerdefinierten Zeitzone verknüpft werden.

+++
