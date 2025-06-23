---
solution: Journey Optimizer
product: journey optimizer
title: Übersicht über die Benutzerverwaltung
description: Erfahren Sie, wie Sie Berechtigungen definieren und verwalten
feature: Access Management
topic: Administration
role: Admin, Architect
level: Intermediate
keywords: Berechtigungen, Rechte, Einschränkungen, Zugriff, Sandbox
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
source-git-commit: 404fffa8d1f2ed40b18246002b67e2b533d8c19e
workflow-type: ht
source-wordcount: '438'
ht-degree: 100%

---

# Erste Schritte mit der Zugriffssteuerung {#permissions-overview}

[!DNL Journey Optimizer] ermöglicht die Definition und Verwaltung von Berechtigungen, die den verschiedenen Benutzern erteilt werden können. Berechtigungen sind eine Reihe von Rechten und Einschränkungen, die den Zugriff auf produktinterne Funktionen zulassen oder verweigern.

Die Zugriffssteuerung für [!DNL Journey Optimizer] erfolgt über die **Berechtigungen** in Adobe Experience Cloud. Diese Funktion nutzt Rollen und Richtlinien, um Benutzende mit Berechtigungen und Sandboxes zu verknüpfen.

Zum Konfigurieren der Zugriffssteuerung für Journey Optimizer werden system- oder produktbezogene Administratorrechte für Ihr Unternehmen benötigt. Zum Erteilen oder Entziehen von Berechtigungen ist mindestens eine Produktadmin-Rolle erforderlich. Zu einer anderen Administratorrolle, die Berechtigungen verwalten können, gehören die Systemadmins (keine Einschränkungen). Dieser [Artikel im Hilfezentrum von Adobe](https://helpx.adobe.com/de/enterprise/using/admin-roles.html){target="_blank"} enthält weitere Informationen zu administrativen Rollen.

<!-- A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.-->


Die Verwaltung von Benutzenden in [!DNL Journey Optimizer] basiert auf drei Schlüsselkonzepten:

* **[!UICONTROL Rollen]**: Rollen beziehen sich auf eine Sammlung von Benutzenden mit denselben Berechtigungen und Sandboxes. Mit diesen Rollen können der Zugriff und die Berechtigungen für verschiedene Gruppen von Benutzenden in Ihrer Organisation einfach verwaltet werden. Rollen sind ein Satz von Einzelrechten (Berechtigungen), die Benutzenden den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche ermöglichen.
In [!DNL Journey Optimizer] besteht die Möglichkeit, aus einer Reihe bereits vorhandener **[!UICONTROL Rollen]** zu wählen, die über jeweils unterschiedliche Berechtigungen verfügen und die Benutzenden zugewiesen werden können. Weitere Informationen zu den verfügbaren **integrierten Rollen** befinden sich auf [dieser Seite](ootb-product-profiles.md).

* **[!UICONTROL Berechtigungen]**: Berechtigungen sind Einzelrechte, mit denen die Autorisierungen definiert werden können, die **[!UICONTROL Rollen]** zugewiesen sind. Jede Berechtigung wird unter bestimmten Ressourcen erfasst, z. B. „Journey“ oder „Angebote“, die für die verschiedenen Funktionen oder Objekte in [!DNL Journey Optimizer] stehen. Weitere Informationen finden Sie im Abschnitt [Berechtigungsebenen](high-low-permissions.md).

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL Sandboxes]**: Virtuelle Sandboxes unterteilen Instanzen in separate, isolierte virtuelle Umgebungen. Sandboxes werden über Rollen unter „Berechtigungen“ zugewiesen. Weitere Informationen zur [Verwendung von Sandboxes](sandboxes.md).

* **Objektbasierte Zugriffssteuerung**: Labels zur Einschränkung des Zugriffs auf ein Objekt. Dieser Ansatz schützt sensible digitale Assets vor unbefugten Benutzenden und ermöglicht so einen weiteren Schutz personenbezogener Daten. Weitere Informationen zur [objektbasierten Zugriffsverwaltung](object-based-access.md).

* **Attributbasierte Zugriffssteuerung**: Berechtigungen zum Verwalten des Datenzugriffs für bestimmte Teams oder Gruppen von Benutzenden. Die attributbasierte Zugriffssteuerung ermöglicht es Administrierenden, den Zugriff auf bestimmte Objekte und/oder Funktionen anhand von Attributen zu steuern. Attribute können Metadaten sein, die einem Objekt hinzugefügt werden, z. B. ein Label, das einem Schemafeld oder Segment hinzugefügt wird. Administrierende definieren Zugriffsrichtlinien, die Attribute zur Verwaltung von Zugriffsberechtigungen für Benutzende enthalten. Weitere Informationen zur [attributbasierten Zugriffsverwaltung](attribute-based-access.md).


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