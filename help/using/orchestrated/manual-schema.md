---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie relationale Schemata direkt über die Benutzeroberfläche erstellen können.
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 5%

---


# Einrichten eines manuellen relationalen Schemas {#manual-schema}

Relationale Schemata können direkt über die Benutzeroberfläche erstellt werden, was eine detaillierte Konfiguration von Attributen, Primärschlüsseln, Versionierungsfeldern und Beziehungen ermöglicht.

Im folgenden Beispiel wird das Schema **Treueprogramm-Zugehörigkeit** manuell definiert, um die erforderliche Struktur für orchestrierte Kampagnen zu veranschaulichen.

1. [Erstellen eines relationalen Schemas manuell](#schema) mithilfe der Adobe Experience Platform-Oberfläche.

1. [Attribute hinzufügen](#schema-attributes) wie Kunden-ID, Mitgliedschaftsstufe und Statusfelder.

1. [Verknüpfen Sie Ihr ](#link-schema) mit integrierten Schemata, wie z. B. Empfangende für Kampagnen-Targeting.

1. [Erstellen Sie einen ](#dataset) basierend auf Ihrem Schema und aktivieren Sie ihn für die Verwendung in orchestrierten Kampagnen.

1. [Aufnehmen von ](ingest-data.md) aus unterstützten Quellen in Ihren Datensatz.

## Erstellen eines Schemas {#schema}

Erstellen Sie zunächst manuell ein neues relationales Schema in Adobe Experience Platform. Mit diesem Prozess können Sie die Schemastruktur von Grund auf neu definieren, einschließlich des Namens und Verhaltens.

1. Melden Sie sich bei Adobe Experience Platform an.

1. Navigieren Sie zum Menü **[!UICONTROL Daten]** > **[!UICONTROL Schema]** .

1. Klicken Sie **[!UICONTROL Schema erstellen]**.

1. Wählen Sie **[!UICONTROL Relational]** als **Schematyp** aus.

   ![](assets/admin_schema_1.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Manuell erstellen]**, um ein Schema durch manuelles Hinzufügen von Feldern zu erstellen.

1. Geben Sie Ihren **[!UICONTROL Anzeigenamen des Schemas]** ein.

   ![](assets/schema_manual_8.png){zoomable="yes"}

1. Klicken Sie **Beenden**, um mit der Schemaerstellung fortzufahren.

Sie können jetzt mit dem Hinzufügen von Attributen zu Ihrem Schema beginnen, um dessen Struktur zu definieren.

## Hinzufügen von Attributen zu Ihrem Schema {#schema-attributes}

Fügen Sie als Nächstes Attribute hinzu, um die Struktur Ihres Schemas zu definieren. Diese Felder stellen die wichtigsten Datenpunkte dar, die in orchestrierten Kampagnen verwendet werden, z. B. Kundenkennungen, Mitgliedschaftsdetails und Aktivitätsdaten. Sie genau zu definieren, stellt eine zuverlässige Personalisierung, Segmentierung und Verfolgung sicher.

Jedes Schema, das für die Zielgruppenbestimmung verwendet wird, muss mindestens ein Identitätsfeld des Typs `String` mit einem zugehörigen Identity-Namespace enthalten. Dadurch wird die Kompatibilität mit den Targeting- und Identitätsauflösungsfunktionen von Adobe Journey Optimizer sichergestellt.

+++Beim Erstellen relationaler Schemata in Adobe Experience Platform werden die folgenden Funktionen unterstützt

* **ENUM**\
  ENUM-Felder werden sowohl bei der DDL-basierten als auch bei der manuellen Schemaerstellung unterstützt, sodass Sie Attribute mit einem festen Satz zulässiger Werte definieren können.

* **Schemakennzeichnung für Data Governance**\
  Die Kennzeichnung wird auf der Ebene der Schemafelder unterstützt, um Data-Governance-Richtlinien wie Zugriffskontrolle und Nutzungsbeschränkungen durchzusetzen. Weitere Informationen sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) verfügbar.

* **Zusammengesetzter Schlüssel**\
  Zusammengesetzte Primärschlüssel werden in relationalen Schemadefinitionen unterstützt, sodass mehrere Felder zusammen verwendet werden können, um Datensätze eindeutig zu identifizieren.

+++

1. Klicken Sie auf der Arbeitsfläche auf ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) neben Ihrem **Schemanamen**, um Attribute hinzuzufügen.

   ![](assets/schema_manual_1.png){zoomable="yes"}

1. Geben Sie Ihr Attribut **[!UICONTROL Feldname]**, **[!UICONTROL Anzeigename]** und **[!UICONTROL Typ]** ein.

   In diesem Beispiel haben wir die in der folgenden Tabelle beschriebenen Attribute zum Schema **Treueprogramm-**&quot; hinzugefügt.

+++ Beispiele für Attribute

   | Attributname | Datentyp | Zusätzliche Attribute |
   |-|-|-|
   | Kundin bzw. Kunde | ZEICHENFOLGE | Primärschlüssel |
   | Membership_level | ZEICHENFOLGE | Erforderlich |
   | points_balance | GANZZAHL | Erforderlich |
   | enrollment_date | DATUM | Erforderlich |
   | last_status_change | DATUM | Erforderlich |
   | expiration_date | DATUM | – |
   | is_active | BOOLEAN | Erforderlich |
   | zuletzt geändert | DATETIME | Erforderlich |

+++

1. Weisen Sie die entsprechenden Felder als **[!UICONTROL Primären Schlüssel]** und **[!UICONTROL Versionsdeskriptor)]**.

   Stellen Sie beim Erstellen eines manuellen Schemas sicher, dass die folgenden wichtigen Felder enthalten sind:

   * Mindestens einen Primärschlüssel,
   * eine Versionskennung, z. B. ein `lastmodified`-Feld vom Typ `datetime` oder `number`.
   * Bei der Aufnahme von Change Data Capture (CDC) gibt eine spezielle Spalte mit dem Namen `_change_request_type` vom Typ `String` den Typ der Datenänderung an (z. B. Einfügen, Aktualisieren, Löschen) und ermöglicht die inkrementelle Verarbeitung.

   ![](assets/schema_manual_2.png){zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Nachdem Attribute erstellt wurden, müssen Sie Ihr neu erstelltes Schema mit einem integrierten Schema verknüpfen.

## Verknüpfen von Schemata {#link-schema}

Wenn Sie eine Beziehung zwischen zwei Schemata erstellen, können Sie Ihre orchestrierten Kampagnen mit Daten anreichern, die außerhalb des primären Profilschemas gespeichert sind.

1. Wählen Sie in Ihrem neu erstellten Schema das Attribut aus, das Sie als Link verwenden möchten, und klicken Sie auf **[!UICONTROL Beziehung hinzufügen]**.

   ![](assets/schema_manual_3.png){zoomable="yes"}

1. Wählen Sie die **[!UICONTROL Referenzschema]** und **[!UICONTROL Referenzfeld]**, mit denen die Beziehung hergestellt werden soll.

   In diesem Beispiel ist das `customer` mit dem `recipients` verknüpft.

   ![](assets/schema_manual_4.png){zoomable="yes"}

1. Geben Sie einen Beziehungsnamen aus dem aktuellen Schema und aus dem Referenzschema ein.

1. Klicken Sie **[!UICONTROL der Konfiguration auf]**&#x200B;Übernehmen“.

Nachdem die Beziehung hergestellt wurde, müssen Sie einen Datensatz basierend auf Ihrem Schema erstellen.

## Erstellen eines Datensatzes für das Schema {#dataset}

Nachdem Sie Ihr Schema definiert haben, besteht der nächste Schritt darin, einen Datensatz basierend darauf zu erstellen. Dieser Datensatz speichert Ihre aufgenommenen Daten und muss für orchestrierte Kampagnen aktiviert sein, damit sie in Adobe Journey Optimizer verfügbar sind. Durch Aktivierung dieser Option wird sichergestellt, dass der Datensatz für die Verwendung in Echtzeit-Orchestrierungs- und Personalisierungs-Workflows erkannt wird.

1. Navigieren Sie zum Menü **[!UICONTROL Daten]** > **[!UICONTROL Datensätze]** und klicken Sie auf **[!UICONTROL Datensatz erstellen]**.

   ![](assets/schema_manual_5.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Datensatz aus Schema erstellen]** aus.

1. Wählen Sie Ihr zuvor erstelltes Schema hier **Treueprogramm-Mitgliedschaften** und klicken Sie auf **[!UICONTROL Weiter]**.

   ![](assets/schema_manual_6.png){zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Namen]** für Ihren **[!UICONTROL Datensatz]** ein und klicken Sie auf **[!UICONTROL Beenden]**.

Jetzt müssen Sie Ihren Datensatz für Kampagnen orchestrieren aktivieren.

## Datensatz für orchestrierte Kampagnen aktivieren {#enable}

Nachdem Sie Ihren Datensatz erstellt haben, müssen Sie ihn explizit für orchestrierte Kampagnen aktivieren. Dadurch wird sichergestellt, dass Ihr Datensatz für die Echtzeit-Orchestrierung und -Personalisierung in Adobe Journey Optimizer verfügbar ist.

1. Suchen Sie Ihren Datensatz in der **[!UICONTROL Datensätze]**-Liste.

1. Aktivieren Sie in **[!UICONTROL Einstellungen]** Datensätze“ die Option **Orchestrierte Kampagnen**, um den Datensatz für die Verwendung in Ihren orchestrierten Kampagnen verfügbar zu machen.

   ![](assets/schema_manual_7.png){zoomable="yes"}

1. Warten Sie einige Minuten, bis der Aktivierungsprozess abgeschlossen ist. Beachten Sie, dass die Datenaufnahme und Kampagnennutzung erst möglich sind, wenn diese Einstellung vollständig aktiviert ist.

Sie können jetzt mit der Aufnahme von Daten in Ihr Schema beginnen, indem Sie die Quelle Ihrer Wahl verwenden.

➡️ [Informationen zur Datenaufnahme](ingest-data.md)
