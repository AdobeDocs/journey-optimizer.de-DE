---
solution: Journey Optimizer
product: journey optimizer
title: Attributbasierte Zugriffssteuerung
description: Mit der attributbasierten Zugriffssteuerung können Sie Berechtigungen definieren, um den Datenzugriff für bestimmte Teams oder Benutzergruppen zu verwalten.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: ABAC, Attribut, Berechtigungen, Daten, Zugriff, vertraulich, Assets
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
TQID: https://experienceleague.adobe.com/PrmjDN7KDV5Y1NRxfEyQ-3ADOIWjgMv2OuRXitt-Wzk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2: id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 1644
ht-degree: 65%

---

# Attributbasierte Zugriffssteuerung {#attribute-based-access}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Verwenden Sie die attributbasierte Zugriffssteuerung in Adobe Journey Optimizer, um vertrauliche Schemafelder, Profilattribute und Zielgruppen auf autorisierte Rollen zu beschränken, damit Sie personenbezogene Daten schützen und nicht autorisierte Benutzende daran hindern können, sie zu bearbeiten.

>[!ENDSHADEBOX]

Mit der Funktion der attributbasierten Zugriffssteuerung können Berechtigungen definiert werden, um den Datenzugriff für bestimmte Teams oder Gruppen von Benutzenden zu verwalten. Dies dient dem Schutz sensibler digitaler Assets vor unbefugten Benutzenden und ermöglicht so einen weiteren Schutz personenbezogener Daten.

Verwenden Sie die attributbasierte Zuriffssteuerung in Adobe Journey Optimizer, um Daten zu schützen und spezifischen Zugriff auf bestimmte Feldelemente zu gewähren, darunter Experience-Datenmodell(XDM)-Schemata, Profilattribute und Zielgruppen.

Eine detailliertere Liste der bei der attributbasierten Zugriffssteuerung verwendeten Begriffe ist in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=de){target="_blank"} verfügbar.

In diesem Beispiel wird dem Schemafeld **Staatsangehörigkeit** ein Label hinzugefügt, um nicht autorisierte Benutzende an der Verwendung zu hindern. Damit dies funktioniert, müssen die folgenden Schritte ausgeführt werden:

1. Erstellen Sie eine neue **[!UICONTROL Rolle]** und weisen Sie ihr das entsprechenden **[!UICONTROL Label]** zu, damit Benutzer auf das Schemafeld zugreifen und es verwenden können.

1. Weisen Sie dem Schemafeld **Staatsangehörigkeit** in Adobe Experience Platform ein **[!UICONTROL Label]** zu.

1. Verwenden Sie das **[!UICONTROL Schemafeld]** in Adobe Journey Optimizer.

Beachten Sie, dass der Zugriff auf **[!UICONTROL Rollen]**, **[!UICONTROL Richtlinien]** und **[!UICONTROL Produkte]** auch über das attributbasierte Zugriffssteuerungs-API möglich ist. Weitere Informationen sind in dieser [Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html?lang=de){target="_blank"} verfügbar.

## Erstellen einer Rolle und Zuweisen von Labels {#assign-role}

>[!IMPORTANT]
>
>>Vor dem Verwalten von Berechtigungen für eine Rolle muss eine Richtlinie erstellt werden. Weitere Informationen sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html?lang=de){target="_blank"} verfügbar.

**[!UICONTROL Rollen]** sind eine Gruppe von Benutzenden, die innerhalb Ihrer Organisation dieselben Berechtigungen, Labels und Sandboxes verwenden. Alle Benutzenden, die einer **[!UICONTROL Rolle]** angehören, haben die Berechtigung für die Adobe-Anwendungen und -Dienste, die im Produkt enthalten sind. Eigene **[!UICONTROL Rollen]** können erstellt werden, wenn der Zugriff der Benutzenden auf bestimmte Funktionen oder Objekte in der Oberfläche präziser definiert werden soll.

Um ausgewählten Benutzenden Zugriff auf das Feld **Staatsangehörigkeit** mit der Bezeichnung „C2“ zu gewähren, muss eine neue **[!UICONTROL Rolle]** mit bestimmten Benutzenden erstellt werden, der das Label „C2“ zugewiesen wird. Dies ermöglicht den Benutzenden die Verwendung der **Staatsangehörigkeits**-Details in einer **[!UICONTROL Journey]**.

1. Wählen Sie aus dem [!DNL Permissions]-Produkt im Menü des linken Fensterbereichs die Option **[!UICONTROL Rolle]** und klicken Sie auf **[!UICONTROL Rolle erstellen]**. Beachten Sie, dass Sie auch **[!UICONTROL Labels]** zu integrierten Rollen hinzufügen können.

   ![Erstellen einer neuen Rolle im Produkt „Berechtigungen“](assets/role_1.png)

1. Fügen Sie hier einen **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** zu Ihrer neuen **[!UICONTROL Rolle]** hinzu, hier: Eingeschränkte Rolle „Demografisch“.

1. Wählen Sie Ihre **[!UICONTROL Sandbox]** aus der Dropdown-Liste.

   ![](assets/role_2.png)

1. Klicken Sie im Menü **[!UICONTROL Ressourcen]** auf **[!UICONTROL Adobe Experience Platform]**, um die verschiedenen Funktionen zu öffnen. Hier wählen wir **[!UICONTROL Journeys]** aus.

   ![](assets/role_3.png)

1. Wählen Sie aus der Dropdown-Liste die **[!UICONTROL Berechtigungen]** aus, die mit der ausgewählten Funktion verknüpft sind, z. B. **[!UICONTROL Anzeigen von Journeys]** oder **[!UICONTROL Veröffentlichen von Journeys]**.

   ![](assets/role_6.png)

1. Nach dem Speichern der neu erstellten **[!UICONTROL Rolle]** klicken Sie auf **[!UICONTROL Eigenschaften]**, um den Zugriff auf Ihre Rolle weiter zu konfigurieren.

   ![](assets/role_7.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   ![](assets/role_8.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Labels]** auf **[!UICONTROL Label hinzufügen]**.

   ![](assets/role_9.png)

1. Wählen Sie das **[!UICONTROL Label]** aus, das Sie Ihrer Rolle hinzufügen möchten, und klicken Sie auf **[!UICONTROL Speichern]**. In diesem Beispiel wird den Benutzenden das Label „C2“ gewährt, damit sie Zugriff auf das zuvor eingeschränkte Feld des Schemas haben.

   ![Speichern der Label-Konfiguration](assets/role_4.png)

Die Benutzenden in der **Eingeschränkten Rolle „Demografisch“** haben nun Zugriff auf die Objekte mit dem Label „C2“.

## Zuweisen von Labels zu einem Objekt in Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>Die falsche Verwendung von Labels kann den Zugriff für Personen unterbrechen und zu Richtlinienverstößen führen.

**[!UICONTROL Labels]** können verwendet werden, um bestimmte Funktionsbereiche mithilfe der attributbasierten Zugriffssteuerung zuzuweisen. In diesem Beispiel ist der Zugriff auf das Feld **Staatsangehörigkeit** eingeschränkt. Auf dieses Feld können nur Benutzende mit dem entsprechenden **[!UICONTROL Label]** in ihrer **[!UICONTROL Rolle]** zugreifen.

Beachten Sie, dass Sie **[!UICONTROL Label]** auch zu **[!UICONTROL Schemata]**, **[!UICONTROL Datensätzen]** und **[!UICONTROL Zielgruppen]** hinzufügen können.

1. Erstellen Sie Ihr **[!UICONTROL Schema]**. Weitere Informationen sind in dieser [Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de){target="_blank"} verfügbar.

   ![](assets/label_1.png)

1. Im neu erstellten **[!UICONTROL Schema]** fügen wir zunächst die Feldergruppe **[!UICONTROL Demografische Details]** hinzu, die das Feld **Staatsangehörigkeit** enthält.

   ![](assets/label_2.png)

1. Überprüfen Sie auf der Registerkarte **[!UICONTROL Label]** den Namen des eingeschränkten Feldes, hier **Staatsangehörigkeit**. Wählen Sie dann im Menü des rechten Fensterbereichs die Option **[!UICONTROL Bearbeiten von Governance-Titeln]**.

   ![Bearbeiten von Governance-Labels für ein Feld](assets/label_3.png)

1. Wählen Sie die entsprechenden **[!UICONTROL Labels]** aus. In diesem Fall können die C2-Daten nicht an einen Drittanbieter exportiert werden. Eine detaillierte Liste der verfügbaren Labels finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=de#contract-labels){target="_blank"}.

   ![](assets/label_4.png)

1. Das Schema kann bei Bedarf weiter personalisiert und dann aktiviert werden. Die detaillierten Schritte zum Aktivieren des Schemas befinden sich auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=de#profile){target="_blank"}.

Das Feld des Schemas ist nun nur noch für Benutzende sichtbar und verwendbar, die Teil eines Rollensatzes mit dem Label „C2“ sind. Beim Anwenden eines **[!UICONTROL Labels]** auf den **[!UICONTROL Feldnamen]**, wird das **[!UICONTROL Label]** automatisch auf das Feld **Staatsangehörigkeits** in jedem erstellten Schema angewendet.

![](assets/label_5.png)

## Zugriff auf Objekte mit Labels in Adobe Journey Optimizer {#attribute-access-ajo}

Nachdem der Feldname **Staatsangehörigkeit** in einem neuen Schema und einer neuen Rolle gekennzeichnet wurde, kann die Auswirkung dieser Einschränkung in Adobe Journey Optimizer beobachtet werden. In diesem Beispiel:

* Die bzw. der Benutzende X, die bzw. der Zugriff auf Objekte mit dem Label „C2“ hat, erstellt eine Journey mit einer Bedingung, die auf den eingeschränkten **[!UICONTROL Feldnamen]** abzielt.
* Eine zweite Benutzende bzw. ein zweiter Benutzender Y ohne Zugriff auf Objekte mit dem Label „C2“ versucht, die Journey zu veröffentlichen.


1. In Adobe Journey Optimizer muss zunächst die **[!UICONTROL Datenquelle]** mit dem neuen Schema konfiguriert werden.

   ![Konfigurieren der Datenquelle](assets/journey_1.png)

1. Fügen Sie eine neue **[!UICONTROL Feldergruppe]** Ihres neu erstellten **[!UICONTROL Schemas]** zur integrierten **[!UICONTROL Datenquelle]** hinzu. Sie können auch eine neue externe **[!UICONTROL Datenquelle]** und zugehörige **[!UICONTROL Feldergruppen]** erstellen.

   ![Hinzufügen einer Feldergruppe zur Datenquelle](assets/journey_2.png)

1. Nach Auswahl des zuvor erstellten **[!UICONTROL Schemas]** klicken Sie in der Kategorie **[!UICONTROL Felder]** auf **[!UICONTROL Bearbeiten]**.

   ![](assets/journey_3.png)

1. Wählen Sie den **[!UICONTROL Feldnamen]** aus, den Sie ansprechen möchten. Hier wählen wir das eingeschränkte Feld **Staatsangehörigkeit**.

   ![](assets/journey_4.png)

1. Erstellen Sie eine Journey, die Benutzenden mit einer bestimmten Staatsangehörigkeit eine E-Mail sendet. Fügen Sie ein **[!UICONTROL Ereignis]** und dann eine **[!UICONTROL Bedingung]** hinzu.

   ![](assets/journey_5.png)

1. Wählen Sie das eingeschränkte Feld **Staatsangehörigkeit** aus, um mit der Erstellung Ihres Ausdrucks zu beginnen.

   ![](assets/journey_6.png)

1. Bearbeiten Sie Ihre **[!UICONTROL Bedingung]**, um eine bestimmte Population mit eingeschränktem Feld **Staatsangehörigkeit** anzusprechen.

   ![](assets/journey_7.png)

1. Personalisieren Sie Ihre Journey nach Bedarf. Hier fügen wir die Aktion **[!UICONTROL E-Mail]** hinzu.

   ![Hinzufügen einer E-Mail-Aktion zur Journey](assets/journey_8.png)

Wenn die bzw. der Benutzende Y ohne Zugriff auf Objekte mit dem Label „C2“ auf diese Journey mit dem eingeschränkten Feld zugreifen muss, geschieht Folgendes:

* Die bzw. der Benutzende Y kann den eingeschränkten Feldnamen nicht verwenden, da er nicht sichtbar ist.
* Die bzw. der Benutzende Y kann den Ausdruck mit dem eingeschränkten Feldnamen im erweiterten Modus nicht bearbeiten. Der folgende Fehler wird angezeigt: `The expression is invalid. Field is no longer available or you do not have enough permission to see it`.
* Die bzw. der Benutzende Y kann den Ausdruck löschen.
* Die bzw. der Benutzende Y kann die Journey nicht testen.
* Die bzw. der Benutzende Y kann die Journey nicht veröffentlichen.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Schützen Sie sensible Datenfelder in Journey Optimizer, indem Sie Governance-Kennzeichnungen auf Schemafelder anwenden und Rollen entsprechende Kennzeichnungen zuweisen, sodass nicht autorisierte Benutzende keine Journey anzeigen, bearbeiten, testen oder veröffentlichen können, die diese eingeschränkten Felder verwenden.

**intents:**

* Erstellen Sie eine Rolle und weisen Sie eine Governance-Kennzeichnung zu, um den Zugriff auf bestimmte Schemafelder zu beschränken
* Anwenden einer Kennzeichnung auf ein Schemafeld in Adobe Experience Platform, um Zugriffsbeschränkungen zu erzwingen
* Verwenden eines gekennzeichneten Schemafelds auf einer Journey Optimizer-Journey
* Erfahren Sie, wie Benutzende ohne die erforderliche Kennzeichnung in Journey auf Zugriffsbeschränkungen zugreifen können
* Verwalten von Rollen, Richtlinien und Produkten über die attributbasierte Zugriffssteuerungs-API

**Glossar:**

* **ABAC (Attribute-based Access Control, attributbasierte Zugriffssteuerung)**: Eine Funktion zur Definition von Berechtigungen zum Verwalten des Datenzugriffs für bestimmte Teams oder Benutzergruppen basierend auf Attributen wie Kennzeichnungen *(produktspezifisch)*
* **Rolle**: Eine Gruppe von Benutzern mit denselben Berechtigungen, Kennzeichnungen und Sandboxes innerhalb einer Organisation *(produktspezifisch)*
* **Label**: Eine Governance-Markierung (z. B. C2), die auf Schemafelder, Datensätze oder Zielgruppen angewendet wird, um zu steuern, welche Rollen auf sie zugreifen können *(produktspezifisch)*
* **Policy**: Eine Konfiguration, die vor der Verwaltung von Berechtigungen für eine Rolle erstellt werden muss - Voraussetzung für ABAC *(produktspezifisch)*
* **XDM-Schema**: Experience-Datenmodellschema, das zum Definieren der Datenstruktur in Adobe Experience Platform verwendet wird *(produktspezifisch)*

**Leitplanken:**

* Eine Richtlinie muss erstellt werden, bevor Berechtigungen für eine Rolle verwaltet werden können (Voraussetzung, wie im wichtigen Hinweis auf der Seite angegeben)
* Eine falsche Verwendung von Kennzeichnungen kann den Zugriff für Personen- und Trigger-Richtlinienverletzungen unterbrechen (wie in der Warnung auf der Seite angegeben)
* Benutzende ohne einer Kennzeichnung, die mit einem eingeschränkten Feld übereinstimmt, können den eingeschränkten Feldnamen nicht anzeigen, Ausdrücke bearbeiten, die im erweiterten Modus darauf verweisen, die Journey testen oder die Journey veröffentlichen

**Terminologie:**

* Kanonischer Name: Attributbasierte Zugriffssteuerung — Akronym: ABAC — Varianten: Attributbasierte Zugriffsverwaltung
* Kanonischer Name: Experience-Datenmodell — Akronym: XDM — Varianten: XDM-Schema, XDM-Schemata
* Synonyme: „Label“ = „Governance-Kennzeichnung“ = „Data Governance-Kennzeichnung“
* Verwechseln Sie nicht: „Rolle“ (eine Benutzergruppe mit freigegebenen Berechtigungen und Beschriftungen) ≠ „Richtlinie“ (Regeln zur Durchsetzung des Datenzugriffs basierend auf Beschriftungen)
* Verwechseln Sie nicht: ABAC (steuert den Zugriff auf Schemafelder, Datensätze und Zielgruppen über Kennzeichnungsrichtlinien auf Plattformebene) ≠ OLAC (steuert den Zugriff auf bestimmte Journey Optimizer-Objekte wie Journey und Kampagnen)

**FAQ:**

* **F: Können Kennzeichnungen zu integrierten Rollen hinzugefügt werden?** — Ja, Kennzeichnungen können sowohl benutzerdefinierten als auch integrierten Rollen hinzugefügt werden.
* **F: Was geschieht mit einem Anwender, dem die Bezeichnung für ein eingeschränktes Feld auf einer Journey fehlt?** — Das Feld ist für sie nicht sichtbar; sie können keine Ausdrücke bearbeiten, die darauf verweisen, die Journey testen oder die Journey veröffentlichen.
* **F: Können Kennzeichnungen auf andere Objekte als Schemafelder angewendet werden?** — Ja. Kennzeichnungen können auch auf Schemata, Datensätze und Zielgruppen angewendet werden.
* **F: Gibt es eine API zum Verwalten von Rollen, Richtlinien und Produkten mit ABAC?** — Ja; auf Rollen, Richtlinien und Produkte kann über die attributbasierte Zugriffssteuerungs-API zugegriffen werden.

+++
<!-- ai-accordion-version: 1 | source-hash: aa94c226 -->