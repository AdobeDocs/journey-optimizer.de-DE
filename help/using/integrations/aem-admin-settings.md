---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von AEM-Repository-Einstellungen
description: Erfahren Sie, wie Administratoren AEM-Repositorys, benutzerdefinierte Domains, authentifizierte Veröffentlichungen und den Nur-Autoren-Zugriff auf Inhaltsfragmente in Journey Optimizer konfigurieren.
feature: Integrations
topic: Administration
role: Admin
level: Experienced
hide: true
keywords: AEM, Inhaltsfragmente, Administration, Repository, Authentifizierung, Autor, Veröffentlichung
source-git-commit: acbc63b37802bfe27a24246d4701efb00ac95940
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Konfigurieren des Adobe Experience Manager-Repository-Zugriffs {#aem-admin-settings}

Adobe Journey Optimizer lässt sich mit **[!DNL Adobe Experience Manager as a Cloud Service]** integrieren, sodass Sie **Inhaltsfragmente** in Journey und Kampagnen verwenden können. **Inhaltsfragmente** werden standardmäßig aus dem Adobe Experience Manager-Veröffentlichungs-Repository gelesen. Administratoren können im Menü **[!UICONTROL AEM-Integration} auf den]** wechseln oder den Veröffentlichungszugriff anpassen.

➡️ Wenn das Repository konfiguriert ist, fahren Sie mit [Arbeiten mit Experience Manager-Inhaltsfragmenten](../integrations/aem-fragments.md) für Authoring- und Auswahlaufgaben in Journey Optimizer fort.

## Konfigurieren von Repositorys {#configure-ui}

>[!NOTE]
>
> **[!UICONTROL AEM-Integration]** speichert Repository-Einstellungen **pro Sandbox**. Jede Sandbox behält ihre eigenen Integrationen bei und gilt nicht für alle Sandboxes.

Journey Optimizer speichert eine Integration pro Organisation, Sandbox und Adobe Experience Manager-Repository. Wenn Sie eine neue Integration für dieselbe Kombination speichern, ersetzt sie die vorherigen Einstellungen, nur die neueste Konfiguration wird beibehalten.

So konfigurieren Sie Ihr Repository:

1. Rufen Sie **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL AEM-Integration]** auf.

1. Klicken Sie **[!UICONTROL Integration erstellen]**.

   ![](assets/aem-admin-settings-1.png)

1. Wählen Sie das zu konfigurierende Repository aus und klicken Sie auf **[!UICONTROL Weiter]**.

   Darüber hinaus können Sie auf **[!UICONTROL Anzeigen]** klicken, um auf dieses Repository zuzugreifen.

   >[!IMPORTANT]
   >
   >Das Speichern einer neuen Konfiguration für dieselbe Organisation, Sandbox und dasselbe Repository **ersetzt** die Standardkonfiguration, d. h. **publish** Repository.

   ![](assets/aem-admin-settings-2.png)

1. Geben Sie **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** ein.

1. Wählen Sie Ihr Setup:

   +++ Setup nur für Autor

   Wählen Sie **[!UICONTROL Nur Autoren-Setup]** aus, wenn Journey Optimizer nur Inhaltsfragmente aus der Adobe Experience Manager-**Autoren**-Umgebung lesen soll. Die Replikation von Autoren- zu Veröffentlichungs- und Live-Veröffentlichungsaktualisierungen wird nicht unterstützt.

   ![](assets/aem-admin-settings-3.png)

   +++

   +++ Einrichtung der Veröffentlichungsinstanz

   1. Wählen Sie **[!UICONTROL Veröffentlichungsinstanz einrichten]** aus, um die Einstellungen der Veröffentlichungsinstanz zu aktivieren.

      ![](assets/aem-admin-settings-4.png)

   1. Aktivieren Sie optional **[!UICONTROL Token an Veröffentlichungsinstanz senden]** damit Service-Anmeldeinformationen in Anfragen an die Veröffentlichungsinstanz eingeschlossen werden.

   1. Fügen Sie eine gültige **[!UICONTROL Dienstanmeldeinformations-JSON]** zur Authentifizierung ein.

   1. Geben Sie optional eine benutzerdefinierte Domain an, wenn Ihr Unternehmen den standardmäßigen AEM-Veröffentlichungs-Host (`publish-XX-XX.adobeaemcloud.com`) zum Abrufen von Inhalten nicht erreichen kann.

      ![](assets/aem-admin-settings-5.png)

   +++

1. Klicken Sie auf **[!UICONTROL Speichern]**.

1. Um diese Repository-Integration zu bearbeiten oder zu deaktivieren, rufen Sie Ihre zuvor erstellte Konfiguration über das Menü **[!UICONTROL AEM-Integration]** auf.

Beim Speichern verwendet diese Sandbox das Repository für den Inhaltsfragmentselektor und **Adobe Experience Manager Content Advisor**.

