---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erste Schritte mit dem Exportieren eines Angebotskatalogs
description: Erfahren Sie, wie Sie Ihren Angebotskatalog als Datensatz exportieren
badge: label="Legacy" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: ht
source-wordcount: '132'
ht-degree: 100%

---

# Erste Schritte mit dem Exportieren eines Angebotskatalogs {#export-catalog}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

Mit Journey Optimizer können Sie Ihren Angebotskatalog automatisch nach Adobe Experience Platform exportieren.

Beim Export wird für jedes Objekt Ihrer Angebotsbibliothek ein Datensatz erstellt (siehe [Zugriff auf exportierte Datensätze](../export-catalog/access-dataset.md)). Zu diesem Datensatz gehören:

* Personalisierte Angebote
* Fallback-Angebote
* Platzierungen
* Entscheidungen

Jedes Mal, wenn eines dieser Objekte in der Angebotsbibliothek geändert wird, wird automatisch ein neuer Exportauftrag ausgeführt, um die Datensätze zu aktualisieren.

>[!NOTE]
>
>Diese Funktion ist standardmäßig aktiviert. Sie können sie ohne zusätzliche Aktivierungsschritte verwenden. Nach der Aktivierung werden Exportaufträge automatisiert. Ihrerseits ist keine Aktion erforderlich.

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
