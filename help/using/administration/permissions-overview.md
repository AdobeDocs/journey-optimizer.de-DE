---
solution: Journey Optimizer
product: journey optimizer
title: Übersicht über die Benutzerverwaltung
description: Erfahren Sie, wie Sie Berechtigungen definieren und verwalten
feature: Access Management
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: Berechtigungen, Rechte, Einschränkungen, Zugriff, Sandbox
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
TQID: https://experienceleague.adobe.com/VRUXM-o41h44PxMAKyafwqSHKmduyt48j4sr11Gh-EQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2:
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 873
ht-degree: 40%

---

# Erste Schritte mit der Zugriffssteuerung {#permissions-overview}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Machen Sie sich mit den grundlegenden Konzepten der Zugriffssteuerung in Journey Optimizer vertraut, einschließlich Rollen, Berechtigungen, Sandboxes und objektbasierter und attributbasierter Zugriffssteuerung, damit Sie planen können, wie Sie Benutzenden den richtigen Zugriff gewähren.

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] ermöglicht die Definition und Verwaltung von Berechtigungen, die den verschiedenen Benutzenden erteilt werden können. Berechtigungen sind eine Reihe an Rechten und Einschränkungen, die den Zugriff auf produktinterne Funktionen zulassen oder verweigern.

Die Zugriffssteuerung für [!DNL Journey Optimizer] wird in [!DNL Adobe CX Enterprise] über **Berechtigungen** bereitgestellt. Diese Funktion nutzt Rollen und Richtlinien, um Benutzende mit Berechtigungen und Sandboxes zu verknüpfen.

Zum Konfigurieren der Zugriffssteuerung für Journey Optimizer werden system- oder produktbezogene Administratorrechte für Ihr Unternehmen benötigt. Zum Erteilen oder Entziehen von Berechtigungen ist mindestens eine Produktadmin-Rolle erforderlich. Zu einer anderen Administratorrolle, die Berechtigungen verwalten können, gehören die Systemadmins (keine Einschränkungen). Dieser [Artikel im Hilfezentrum von Adobe](https://helpx.adobe.com/de/enterprise/using/admin-roles.html){target="_blank"} enthält weitere Informationen zu administrativen Rollen.

<!--
 A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.
-->


Die Verwaltung von Benutzenden in [!DNL Journey Optimizer] basiert auf drei Schlüsselkonzepten:

* **[!UICONTROL Rollen]**: Rollen beziehen sich auf eine Sammlung von Benutzern, die dieselben Berechtigungen und Sandboxes verwenden. Mit diesen Rollen können Sie den Zugriff und die Berechtigungen für verschiedene Benutzergruppen innerhalb Ihrer Organisation einfach verwalten. Eine Rolle verfügt über eine Reihe von Einzelrechten (Berechtigungen), die Benutzern den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche ermöglichen.
Mit [!DNL Journey Optimizer] können Sie aus einer Reihe bereits vorhandener **[!UICONTROL Rollen]** mit unterschiedlichen Berechtigungsebenen auswählen, die Sie Ihren Benutzenden zuweisen können. Weitere Informationen zu den verfügbaren **integrierten Rollen** finden Sie auf [dieser Seite](ootb-product-profiles.md).

* **[!UICONTROL Berechtigungen]**: Berechtigungen sind Einzelrechte, mit denen die Autorisierungen definiert werden können, die **[!UICONTROL Rollen]** zugewiesen sind. Jede Berechtigung wird unter bestimmten Ressourcen erfasst, z. B. „Journey“ oder „Angebote“, die für die verschiedenen Funktionen oder Objekte in [!DNL Journey Optimizer] stehen. Weitere Informationen finden Sie im Abschnitt [Berechtigungsebenen](high-low-permissions.md).

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL Sandboxes]**: Virtuelle Sandboxes unterteilen Instanzen in separate, isolierte virtuelle Umgebungen. Sandboxes werden über Rollen unter „Berechtigungen“ zugewiesen. Weitere Informationen zur [Verwendung von Sandboxes](sandboxes.md).

* **Objektbasierte Zugriffssteuerung**: Labels zur Einschränkung des Zugriffs auf ein Objekt. Dieser Ansatz schützt sensible digitale Assets vor unbefugten Nutzern und sorgt für einen weiteren Schutz personenbezogener Daten. Weitere Informationen zur [objektbasierten Zugriffsverwaltung](object-based-access.md).

* **Attributbasierte Zugriffssteuerung**: Berechtigungen zum Verwalten des Datenzugriffs für bestimmte Teams oder Gruppen von Benutzenden. Die attributbasierte Zugriffssteuerung ermöglicht es Administrierenden, den Zugriff auf bestimmte Objekte und/oder Funktionen anhand von Attributen zu steuern. Attribute können Metadaten sein, die einem Objekt hinzugefügt werden, z. B. ein Label, das einem Schemafeld oder Segment hinzugefügt wird. Administrierende definieren Zugriffsrichtlinien, die Attribute zur Verwaltung von Benutzerzugriffsberechtigungen enthalten. Weitere Informationen zur [attributbasierten Zugriffsverwaltung](attribute-based-access.md).


## Tauchen wir tiefer in die Materie ein

Da Sie nun über Kenntnisse zu den Konzepten der Zugriffssteuerung in **[!DNL Journey Optimizer]** verfügen, können Sie sich umfassender mit diesen Dokumentationsabschnitte befassen, um mit der Konfiguration von Berechtigungen zu beginnen.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="Berechtigungen" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong>Gewähren von Zugriff</strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="Integrierte Berechtigungen" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong>Integrierte Berechtigungen</strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="Verwalten von Sandboxes" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong>Verwalten von Sandboxes</strong></a>
</div>
<p></td>
<td>
<a href="attribute-based-access.md">
<img alt="Attributbasierte Zugriffssteuerung" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong>Attributbasierte Zugriffssteuerung</strong></a>
</div>
<p>
</td>
</tr></table>

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* Die **TL;DR:**-Zugriffssteuerung in Journey Optimizer basiert auf Rollen, Berechtigungen und Sandboxes, die über Adobe CX Enterprise-Berechtigungen verwaltet werden, und bietet zusätzliche Ebenen der objektbasierten Zugriffssteuerung (OLAC) und der attributbasierten Zugriffssteuerung (ABAC) für einen differenzierten Datenschutz.

**intents:**

* Machen Sie sich mit den fünf Konzepten der Kernzugriffssteuerung vertraut: Rollen, Berechtigungen, Sandboxes, objektbasierte Zugriffssteuerung und attributbasierte Zugriffssteuerung
* Wissen, wer die Zugriffskontrolle konfigurieren kann (System- oder Produktadministrator)
* Navigieren Sie zum rechten Dokumentationsabschnitt für jedes Thema zur Zugriffssteuerung
* Planen einer Zugriffssteuerungsstrategie für die Organisation

**Glossar:**

* **Rollen**: Sammlungen von Benutzern, die dieselben Berechtigungen und Sandboxes nutzen; bereits vorhandene integrierte Rollen sind verfügbar, und benutzerdefinierte Rollen können *(produktspezifisch) erstellt werden*
* **Berechtigungen**: Einzelrechte, die die den Rollen zugewiesenen Berechtigungen definieren, gruppiert unter Ressourcen wie Journey oder Angebote *(produktspezifisch)*
* **Sandboxes**: Virtuelle Umgebungen, die die Journey Optimizer-Instanz in separate, isolierte virtuelle Arbeitsbereiche unterteilen; über Rollen in Berechtigungen zugewiesen *(produktspezifisch)*
* **Objektbasierte Zugriffssteuerung**: Kennzeichnungen, die auf bestimmte Journey Optimizer-Objekte (Journey, Kampagnen, Angebote) angewendet werden, um den Zugriff auf autorisierte Benutzende zu beschränken *(produktspezifisch)*
* **Attributbasierte Zugriffssteuerung**: Richtlinien zur Steuerung des Zugriffs auf Objekte oder Funktionen basierend auf Attributen wie Kennzeichnungen, die Schemafeldern oder Segmenten hinzugefügt werden *(produktspezifisch)*

**Leitplanken:**

* Das Konfigurieren der Zugriffssteuerung erfordert System- oder Produktadministratorrechte (Voraussetzung)
* Die Mindestrolle, die Berechtigungen erteilen oder entziehen kann, ist ein Produktadministrator (wie auf der Seite angegeben)

**Terminologie:**

* Kanonischer Name: Attributbasierte Zugriffssteuerung — Akronym: ABAC — Varianten: Attributbasierte Zugriffsverwaltung
* Kanonischer Name: Objektbasierte Zugriffssteuerung — Akronym: OLAC — Varianten: Zugriffssteuerung auf Objektebene, objektbasierte Zugriffsverwaltung
* Verwechseln Sie nicht: „Objektbasierte Zugriffssteuerung“ (beschränkt den Zugriff auf bestimmte AJO-Objekte wie Journey, Kampagnen und Angebote mithilfe von Kennzeichnungen) ≠ „Attributbasierte Zugriffssteuerung“ (beschränkt den Zugriff auf Datenattribute wie Schemafelder und Segmente basierend auf Kennzeichnungsrichtlinien)
* Verwechseln Sie nicht: „Rollen“ (eine Sammlung von Benutzern mit freigegebenen Berechtigungen und Sandboxes) ≠ „Berechtigungen“ (die Einzelrechte, die unter Ressourcen gruppiert sind, die Rollen zugewiesen sind)

**FAQ:**

* **F: Wer kann die Zugriffssteuerung in Journey Optimizer konfigurieren?** — Benutzende mit Systemadministrator- oder Produktadministrator-Berechtigungen.
* **F: Was ist die Mindestadministratorstufe, die erforderlich ist, um Berechtigungen zu erteilen oder zu entziehen?** — Produkt-Administrator.
* **F: Werden Sandboxes unabhängig von Rollen verwaltet?** — Nein. Sandboxes werden über Rollen im Produkt „Berechtigungen“ zugewiesen.
* **F: Wo wird die Zugriffssteuerung für Journey Optimizer verwaltet?** - Über Berechtigungen in Adobe CX Enterprise, die Benutzende über Rollen und Richtlinien mit Berechtigungen und Sandboxes verknüpfen.

+++
<!-- ai-accordion-version: 1 | source-hash: 14be1dc6 -->