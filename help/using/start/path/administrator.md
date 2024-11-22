---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer – Erste Schritte für Systemadministratoren
description: Hier erfahren Systemadministratoren mehr über die Arbeit mit Journey Optimizer.
feature: Get Started
role: Admin
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 13cbb0877326b772c3750bd3339e21eee5c3f323
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 68%

---

# Erste Schritte für Systemadministratoren {#get-started-sys-admins}

Bevor Sie mit der Verwendung von [!DNL Adobe Journey Optimizer] beginnen, sind mehrere Schritte erforderlich, um Ihre Umgebung vorzubereiten.  Sie müssen diese Schritte ausführen, damit der [Dateningenieur](data-engineer.md) und der [Journey-Trainer](marketer.md) beginnen können, mit [!DNL Adobe Journey Optimizer] zu arbeiten.

Als **Systemadministrator** müssen Sie **die Rollen verstehen und Berechtigungen zuweisen** für die Sandbox-Verwaltung und die Kanalkonfiguration. Außerdem müssen Sie Sandboxes einrichten und für die verfügbaren Rollen verwalten. Anschließend können Sie Team-Mitglieder Rollen zuweisen.

Diese Funktionen können von **[!UICONTROL Produktadministratoren]** verwaltet werden, die Zugriff auf das Berechtigungsprodukt haben. [Erfahren Sie mehr über Berechtigungen](../../administration/permissions.md){target="_blank"}.

Informationen zur Zugriffsverwaltung finden Sie auf den folgenden Seiten:

1. **Erstellen Sie Sandboxes**, um Ihre Instanzen in separate, isolierte virtuelle Umgebungen zu unterteilen. **Sandboxes** werden in [!DNL Journey Optimizer] erstellt. Weitere Informationen finden Sie im Abschnitt [Sandboxes](../../administration/sandboxes.md).

   >[!NOTE]
   >Wenn Sie als **Systemadministrator** nicht das Menü **[!UICONTROL Sandboxes]** in [!DNL Journey Optimizer] sehen können, müssen Sie Ihre Berechtigungen aktualisieren. Erfahren Sie, wie Sie Ihre Rolle auf [dieser Seite](../../administration/permissions.md#edit-product-profile) aktualisieren können.

1. **Verstehen Sie die Rollen**. Rollen sind eine Reihe von Einzelrechten, die Benutzern den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche ermöglichen. Weitere Informationen finden Sie im Abschnitt [ vordefinierte Rollen](../../administration/ootb-product-profiles.md) .

1. **Legen Sie Berechtigungen fest** für Rollen, einschließlich **Sandboxes**, und gewähren Sie Zugriff auf Ihre Team-Mitglieder, indem Sie sie verschiedenen Rollen zuweisen. Berechtigungen sind Einzelrechte, mit denen Sie die **[!UICONTROL Rolle]** zugewiesenen Berechtigungen definieren können. Jede Berechtigung wird unter bestimmten Kategorien erfasst, z. B. Journey oder Angebote, die die verschiedenen Funktionen oder Objekte in [!DNL Journey Optimizer] repräsentieren. Weitere Informationen finden Sie im Abschnitt [Berechtigungsebenen](../../administration/high-low-permissions.md).

Darüber hinaus müssen Sie den Benutzerrollen **Assets Essentials- und/oder** Assets Essentials-Benutzer **Benutzer hinzufügen, die Zugriff auf Assets Essentials benötigen.** [Weitere Informationen finden Sie in der Dokumentation zu Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=de){target="_blank"}.

>[!NOTE]
>Für Journey Optimizer-Produkte, die vor dem 6. Januar 2022 erworben wurden, müssen Sie [!DNL Adobe Experience Manager Assets Essentials] für Ihre Organisation bereitstellen. Weitere Informationen finden Sie im Abschnitt [Bereitstellen von Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=de){target="_blank"}.

Beim erstmaligen Zugriff auf [!DNL Journey Optimizer] wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.

Um Journeys erstellen und Nachrichten senden zu können, rufen Sie das Menü **ADMINISTRATION** auf. Gehen Sie das Menü **[!UICONTROL Kanäle]** durch, um Ihre Nachrichten- und Kanalkonfigurationen (d. h. Nachrichtenvoreinstellungen) festzulegen.

>[!NOTE]
>Wenn Sie als **Systemadministrator** nicht das Menü **[!UICONTROL Kanäle]** in [!DNL Journey Optimizer] sehen können, aktualisieren Sie Ihre Berechtigungen im Produkt [Berechtigungen](../../administration/permissions.md){target="_blank"}.
>

Führen Sie dazu folgende Schritte durch:

1. **Konfigurieren von Nachrichten und Kanälen**: Definieren von Konfigurationen und Anpassen der Einstellungen für E-Mails, SMS und Push-Benachrichtigungen

   * Definieren Sie **Push-Benachrichtigungseinstellungen** sowohl in [!DNL Adobe Experience Platform] als auch in [!DNL Adobe Experience Platform Launch]. [Weitere Informationen](../../push/push-gs.md)

   * Erstellen Sie **Kanalkonfigurationen** (d. h. Nachrichtenvoreinstellungen) zum Konfigurieren aller technischen Parameter, die für E-Mails, SMS und Push-Benachrichtigungen erforderlich sind.  [Weitere Informationen](../../configuration/channel-surfaces.md)

   * Konfigurieren Sie den **SMS-Kanal**, um alle für SMS erforderlichen technischen Parameter zu konfigurieren. [Weitere Informationen](../../sms/sms-configuration.md)

   * Verwalten Sie die Anzahl der Tage, in denen **weitere Zustellversuche** unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](../../configuration/manage-suppression-list.md)

1. **Subdomains zuweisen**: Für jede neue Subdomain, die in Journey Optimizer verwendet werden soll, besteht der erste Schritt darin, sie zuzuweisen. [Weitere Informationen](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Erstellen von IP-Pools**: Verbessern Sie die Zustellbarkeit Ihrer E-Mails und Ihre Reputation, indem Sie IP-Adressen gruppieren, die mit Ihrer Instanz bereitgestellt wurden. [Weitere Informationen](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Verwalten der Unterdrückungs- und Zulassungslisten**: Verbessern der Zustellbarkeit durch Unterdrückungs- und Zulassungslisten

   * Eine [Unterdrückungsliste](../../reports/suppression-list.md) besteht aus E-Mail-Adressen, die Sie von Ihren Sendungen ausschließen möchten, da das Senden an diese Kontakte Ihren Ruf als Versender und Ihre Versandraten beeinträchtigen könnte. Sie können alle E-Mail-Adressen überwachen, die bei einer Journey automatisch vom Versand ausgeschlossen werden, wie ungültige Adressen, Adressen, die stets zu Soft-Bounces führen und sich negativ auf Ihre E-Mail-Reputation auswirken könnten, sowie Empfänger, die eine Spam-Beschwerde gegen eine Ihrer E-Mail-Nachrichten eingelegt haben. Erfahren Sie, wie Sie die [Unterdrückungsliste](../../configuration/manage-suppression-list.md) und [weitere Zustellversuche](../../configuration/retries.md) verwalten.

   ![](../assets/suppression-list-filtering-example.png)

   * Mit der [Zulassungsliste](../../configuration/allow-list.md) können Sie einzelne E-Mail-Adressen oder Domains als die einzigen Empfänger oder Domains angeben, die zum Empfang der E-Mails berechtigt sind, die von einer bestimmten Sandbox gesendet werden. Dadurch können Sie verhindern, dass Sie in einer Testumgebung versehentlich E-Mails an echte Kundenadressen senden. Erfahren Sie, wie Sie die [Zulassungsliste aktivieren](../../configuration/allow-list.md).

   Sie erfahren mehr über die Zustellbarkeitsverwaltung in [!DNL Adobe Journey Optimizer] [auf dieser Seite](../../reports/deliverability.md).
