---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer – Erste Schritte für Systemadministratoren
description: Hier erfahren Systemadministratoren mehr über die Arbeit mit Journey Optimizer.
feature: Get Started
role: Admin
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
TQID: https://experienceleague.adobe.com/D--D1ynxQx-Q9eSzjU-fwG0Hc3emaCfa2gIwizpHsQU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b856530c-d60b-42d8-a19d-df2dfd7fe62aid: c343082f-e963-4f57-a96b-b64d27f8118eid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 2dcba98da11fe6b8c86aeb0b0e3023506c1229fd
workflow-type: tm+mt
source-wordcount: 1168
ht-degree: 93%

---

# Erste Schritte für Systemadmins {#get-started-sys-admins}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Richten Sie Benutzer, Berechtigungen, Sandboxes und Kanalkonfigurationen ein, damit Ihre Teams sicher und effizient in Adobe Journey Optimizer arbeiten können.

>[!ENDSHADEBOX]

Als **Systemadmin** richten Sie die Journey Optimizer-Umgebung ein und verwalten den Zugriff, damit Ihre Teams effizient und sicher arbeiten können. Sie führen wichtige Konfigurationsschritte aus, damit [Dateningenieurinnen und -ingenieure](data-engineer.md), [Entwickelnde](developer.md) und [Marketing-Fachleute](marketer.md) mit [!DNL Adobe Journey Optimizer] arbeiten können.

Zu Ihren Hauptaufgaben gehören das Einrichten von Benutzergruppen und Berechtigungen, das Erstellen und Verwalten von Sandboxes für die Partitionierung von Daten und Journeys für verschiedene Benutzergruppen sowie das Konfigurieren von Versandkanälen und Nachrichtenvoreinstellungen, um ein konsistentes Branding für die verschiedenen über Journey Optimizer bereitgestellten Nachrichten und Assets sicherzustellen. Sie stellen sicher, dass die richtigen Personen Zugriff auf die richtigen Funktionen haben, während gleichzeitig die Sicherheit und die Governance gewahrt bleiben.

Diese Funktionen können von **[!UICONTROL Produktadmins]** verwaltet werden, die Zugriff auf das Produkt „Berechtigungen“ haben. [Weitere Informationen zu Berechtigungen](../../administration/permissions.md){target="_blank"}.

>[!NOTE]
>
>**Implementierungsreihenfolge:** Sie sind hier: **Administrator** → [Datentechniker](data-engineer.md) → → [Entwickler](developer.md) [Marketer](marketer.md)
>
>Der Administrator richtet zuerst die Umgebung ein. Datentechniker, Entwickler und Marketing-Experten sind darauf angewiesen, dass diese Arbeit abgeschlossen ist, bevor sie beginnen können.

## Einrichten von Zugriff und Berechtigungen

Führen Sie die folgenden Schritte aus, um die Zugriffsverwaltung zu konfigurieren:

1. **Erstellen Sie Sandboxes**, um Ihre Instanzen in separate, isolierte virtuelle Umgebungen zu unterteilen. **Sandboxes** werden in [!DNL Journey Optimizer] erstellt. Weitere Informationen finden Sie im Abschnitt [Sandboxes](../../administration/sandboxes.md).

   >[!NOTE]
   >Wenn Sie als **Systemadmin** das Menü **[!UICONTROL Sandboxes]** in [!DNL Journey Optimizer] nicht sehen können, müssen Sie Ihre Berechtigungen aktualisieren. Informationen zum Aktualisieren Ihrer Rolle finden Sie auf [dieser Seite](../../administration/permissions.md#edit-product-profile).

1. **Verstehen von Rollen**. Rollen sind ein Set vereinheitlichter Rechte, die Benutzenden den Zugriff auf bestimmte Funktionen oder Objekte in der Schnittstelle ermöglichen. Weitere Informationen finden Sie im Abschnitt [Vorkonfigurierte Rollen](../../administration/ootb-product-profiles.md).

1. **Legen Sie Berechtigungen für Rollen fest**, einschließlich **Sandboxes**, und gewähren Sie Ihren Team-Mitgliedern Zugriff, indem Sie sie verschiedenen Rollen zuweisen. Berechtigungen sind Einzelrechte, mit denen Sie die einer **[!UICONTROL Rolle]** zugewiesenen Genehmigungen definieren können. Jede Berechtigung wird unter bestimmten Kategorien erfasst, z. B. Journey oder Angebote, die die verschiedenen Funktionen oder Objekte in [!DNL Journey Optimizer] repräsentieren. Weitere Informationen finden Sie im Abschnitt [Berechtigungsebenen](../../administration/high-low-permissions.md).

1. **Verwenden Sie die Zugriffssteuerung auf Objektebene** (optional). Wenden Sie Zugriffs-Labels auf Objekte wie Journeys, Kampagnen und Kanalkonfigurationen an, um zu steuern, welche Benutzenden auf bestimmte Ressourcen zugreifen können. Erfahren Sie mehr über die [Zugriffssteuerung auf Objektebene (OLAC)](../../administration/object-based-access.md).

Darüber hinaus müssen Sie Benutzende, die Zugriff auf Assets Essentials benötigen, den Rollen **Assets Essentials-Endbenutzende** oder/und **Assets Essentials-Benutzende** hinzufügen. [Weitere Informationen finden Sie in der Dokumentation zu Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=de){target="_blank"}.

Beim erstmaligen Zugriff auf [!DNL Journey Optimizer] wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.

## Konfigurieren von Kanälen und Nachrichten

Damit [Marketing-Fachleute](marketer.md) Nachrichten erstellen und senden können, rufen Sie das Menü **ADMINISTRATION** auf. Durchsuchen Sie das Menü **[!UICONTROL Kanäle]**, um die Kanaleinstellungen zu konfigurieren.

>[!NOTE]
>Wenn Sie als **Systemadmin** das Menü **[!UICONTROL Kanäle]** in [!DNL Journey Optimizer] nicht sehen, aktualisieren Sie Ihre Berechtigungen im Produkt [Berechtigungen](../../administration/permissions.md){target="_blank"}.

Führen Sie folgende Schritte aus:

1. **Richten Sie Kanalkonfigurationen ein**. Definieren Sie alle technischen Parameter, die für E-Mail, SMS, Push-Benachrichtigungen, Web-Push, Direkt-Mail und andere Kanäle erforderlich sind:

   * Definieren Sie **Push-Benachrichtigungseinstellungen** sowohl in [!DNL Adobe Experience Platform] als auch in der Datenerfassung von Adobe Experience Platform. [Weitere Informationen](../../push/push-gs.md)

   * Konfigurieren Sie **Web-Push-Benachrichtigungen**, um Benachrichtigungen an Mobile- und Desktop-Browser zu senden. [Weitere Informationen](../../push/push-configuration-web.md)

   * Erstellen Sie **Kanalkonfigurationen**, um alle technischen Parameter zu konfigurieren, die für E-Mail, SMS, Push, In-App, Web und andere Kanäle erforderlich sind. [Weitere Informationen](../../configuration/channel-surfaces.md)

   * Konfigurieren Sie den **SMS-Kanal**, um alle für SMS erforderlichen technischen Parameter einzurichten. [Weitere Informationen](../../mobile/mobile-configuration.md)

   * Verwalten Sie die Anzahl der Tage, in denen **weitere Zustellversuche** unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](../../configuration/manage-suppression-list.md)

   * Aktivieren Sie den **Nachrichtenexport** auf der Kanalkonfigurationsebene, um gesendete E-Mail- und SMS-Inhalte bei Bedarf zu archivieren (Add-on-Angebot). [Weitere Informationen](../../configuration/message-export.md)

1. **Subdomains zuweisen**: Für jede neue Subdomain, die in Journey Optimizer verwendet werden soll, besteht der erste Schritt darin, sie zuzuweisen. [Weitere Informationen](../../configuration/about-subdomain-delegation.md). Sie können bei Bedarf Subdomains von CNAME zu benutzerdefinierter Delegierung migrieren. [Weitere Informationen](../../configuration/custom-subdomain-migration.md)

   ![](../assets/subdomain.png)

1. **Erstellen von IP-Pools**: Verbessern Sie die Zustellbarkeit Ihrer E-Mails und Ihre Reputation, indem Sie IP-Adressen gruppieren, die mit Ihrer Instanz bereitgestellt wurden. [Weitere Informationen](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Verwalten der Unterdrückungs- und Zulassungslisten**: Verbessern der Zustellbarkeit durch Unterdrückungs- und Zulassungslisten

   * Eine [Unterdrückungsliste](../../reports/suppression-list.md) besteht aus E-Mail-Adressen, die Sie von Ihren Sendungen ausschließen möchten, da das Senden an diese Kontakte Ihren Ruf als Versender und Ihre Versandraten beeinträchtigen könnte. Sie können alle E-Mail-Adressen überwachen, die bei einer Journey automatisch vom Versand ausgeschlossen werden, wie ungültige Adressen, Adressen, die stets zu Soft-Bounces führen und sich negativ auf Ihre E-Mail-Reputation auswirken könnten, sowie Empfänger, die eine Spam-Beschwerde gegen eine Ihrer E-Mail-Nachrichten eingelegt haben. Erfahren Sie, wie Sie die [Unterdrückungsliste](../../configuration/manage-suppression-list.md) und [weitere Zustellversuche](../../configuration/retries.md) verwalten.

   ![](../assets/suppression-list-filtering-example.png)

   * Mit der [Zulassungsliste](../../configuration/allow-list.md) können Sie einzelne E-Mail-Adressen oder Domains als die einzigen Empfänger oder Domains angeben, die zum Empfang der E-Mails berechtigt sind, die von einer bestimmten Sandbox gesendet werden. Dadurch können Sie verhindern, dass Sie in einer Testumgebung versehentlich E-Mails an echte Kundenadressen senden. Erfahren Sie, wie Sie die [Zulassungsliste aktivieren](../../configuration/allow-list.md).

   Weitere Informationen zur Verwaltung der Zustellbarkeit in [!DNL Adobe Journey Optimizer] finden Sie [auf dieser Seite](../../reports/deliverability.md).

## Zusätzliche Funktionen

Berücksichtigen Sie bei wachsenden Anforderungen Ihres Unternehmens die folgenden erweiterten Funktionen:

* **Einverständnisrichtlinien**: Wenn Ihr Unternehmen Healthcare Shield oder Privacy and Security Shield erworben hat, erstellen Sie Einverständnisrichtlinien, die kanalübergreifend die Kundenvoreinstellungen berücksichtigen. [Weitere Informationen](../../action/consent.md)

* **Data-Governance-Richtlinien**: Wenden Sie Datennutzungs-Labels und -richtlinien an, um zu steuern, wie Daten in Marketing-Aktionen verwendet werden. [Weitere Informationen](../../action/action-privacy.md)

* **IP-Aufwärmpläne**: Steigern Sie die Menge der E-Mail-Sendungen schrittweise, um die Reputation der Absendenden bei E-Mail-Anbietern aufzubauen. [Weitere Informationen](../../configuration/ip-warmup-gs.md)

* **Ruhezeiten**: Konfigurieren Sie Regelsätze für zeitbasierte Ausschlüsse, wenn Nachrichten während bestimmter Zeiträume nicht gesendet werden sollen. [Weitere Informationen](../../conflict-prioritization/quiet-hours.md)

## Rollenübergreifendes Zusammenarbeiten

Ihre administrative Arbeit ermöglicht es allen Teams, erfolgreich zu sein:

>[!BEGINTABS]

>[!TAB Unterstützen von Dateningenieurinnen und -ingenieuren]

Arbeiten Sie mit [Dateningenieurinnen und -ingenieuren](data-engineer.md) bei Verwaltung und Zugriff auf Daten zusammen. Lesen Sie den Überblick [Erste Schritte mit dem Daten-Management](../../data/gs-data.md), um mehr über die Schemata, Datensätze und Datenquellen zu erfahren, die Ihre Dateningenieurinnen und -ingenieure konfigurieren müssen.

* Erteilen von Berechtigungen für das Daten-Management und die Schemaerstellung
* Genehmigen des Sandbox-Zugriffs für Entwicklung und Tests
* Koordinieren von Datenspeicherungsrichtlinien und Governance-Regeln
* Ermöglichen des Zugriffs auf erweiterte Funktionen wie die Komposition föderierter Zielgruppen

>[!TAB Unterstützen von Entwickelnden]

Arbeiten Sie mit [Entwickelnden](developer.md) bei API-Zugriff und Tests zusammen:

* Bereitstellen von API-Anmeldedaten über Adobe Developer Console
* Einrichten von Sandbox-Umgebungen für Entwicklung und Tests
* Genehmigen von Kanalkonfigurationen (Push-Zertifikate, SMS-Anbieter)
* Koordinieren von Testumgebungen und Bereitstellungsstrategie

>[!TAB Unterstützen von Marketing-Fachleuten]

Arbeiten Sie mit [Marketing-Fachleuten](marketer.md) bei Berechtigungen und Kanaleinrichtung zusammen:

* Zuweisen der entsprechenden Berechtigungen zum Erstellen von Journeys und Kampagnen
* Konfigurieren von Kanälen, die sie verwenden werden (E-Mail, Push, SMS usw.)
* Unterstützen von Testumgebungen und Genehmigungs-Workflows
* Ermöglichen von Zugriff auf neue Funktionen

>[!ENDTABS]

## Nächste Schritte

Sobald die Umgebung konfiguriert ist, kann Folgendes geschehen:

1. **Überprüfen der Einrichtung**: Überprüfen Sie, ob alle Team-Mitglieder auf die erforderlichen Funktionen zugreifen können
2. **Überwachen der Nutzung**: Verwenden Sie die Dashboards zur Administration, um die Systemnutzung zu verfolgen und Probleme zu identifizieren
3. **Beibehalten von Berechtigungen**: Überprüfen und aktualisieren Sie Berechtigungen im Zuge der Weiterentwicklung von Team-Rollen regelmäßig

## Weitere Rollenleitfäden {#other-role-guides}

| Rolle | Handbuch |
|------|-------|
| Administrator | [Erste Schritte für Administratoren](administrator.md) |
| Datentechniker | [Erste Schritte für Dateningenieure](data-engineer.md) |
| Entwickler | [Erste Schritte für Entwickler](developer.md) |
| Marketer | [Erste Schritte für Marketing-Fachleute](marketer.md) |

Zurück zu [Überblick über Rollen und Zuständigkeiten](../quick-start.md) ・ Zurück zu [Erste Schritte](../../../rp_landing_pages/get-started-landing-page.md)
