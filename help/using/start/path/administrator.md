---
title: Journey Optimizer – Erste Schritte für Systemadministratoren
description: Hier erfahren Systemadministratoren mehr über die Arbeit mit Journey Optimizer.
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 7a07f2348f08b4582a1310fb65d431c55451d9b6
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 100%

---

# Erste Schritte für Systemadministratoren {#get-started-sys-admins}

![Administrator](assets/do-not-localize/user-2.png)

Bevor Sie mit der Verwendung von [!DNL Adobe Journey Optimizer] beginnen, sind mehrere Schritte erforderlich, um Ihre Umgebung vorzubereiten.  Sie müssen diese Schritte ausführen, damit [Datentechniker](data-engineer.md) und [Journey-Anwender](marketer.md) [!DNL Adobe Journey Optimizer] verwenden können.


Als **Systemadministrator** müssen Sie **Produktprofile verstehen und Berechtigungen für die Sandbox-Administration und Kanalkonfiguration zuweisen**. Außerdem müssen Sie Sandboxes einrichten und entsprechend den verfügbaren Produktprofilen verwalten. Anschließend können Sie Produktprofilen Team-Mitglieder zuweisen.

Diese Funktionen können von **[!UICONTROL Produktadministratoren]** verwaltet werden, die Zugriff auf Admin Console haben. [Erfahren Sie mehr über Adobe Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Informationen zur Zugriffsverwaltung finden Sie auf den folgenden Seiten:

1. **Erstellen Sie Sandboxes**, um Ihre Instanzen in separate, isolierte virtuelle Umgebungen zu unterteilen. **Sandboxes** werden in [!DNL Journey Optimizer] erstellt. Weitere Informationen finden Sie im Abschnitt [Sandboxes](../../administration/sandboxes.md).

   >[!NOTE]
   >Wenn Sie als **Systemadministrator** das Menü **[!UICONTROL Sandboxes]** in [!DNL Journey Optimizer] nicht sehen können, aktualisieren Sie Ihre Berechtigungen in [Admin Console](https://adminconsole.adobe.com/){_blank}. Auf [dieser Seite](../../administration/permissions.md#edit-product-profile) erfahren Sie, wie Sie Ihr Produktprofil aktualisieren können.

1. **Verwendung von Produktprofilen**. Produktprofile sind eine Reihe von Einzelberechtigungen, die Benutzern den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche ermöglichen. Weitere Informationen finden Sie im Abschnitt [Vordefinierte Produktprofile](../../administration/ootb-product-profiles.md).

1. **Definieren Sie Berechtigungen für Produktprofile**, einschließlich **Sandboxes**, und geben Sie Ihren Team-Mitgliedern Zugriff, indem Sie sie verschiedenen Produktprofilen zuweisen. Dieser Schritt wird in [Admin Console](https://adminconsole.adobe.com/){_blank} ausgeführt. Berechtigungen sind Einzelrechte, mit denen Sie die einem **[!UICONTROL Produktprofil]** zugewiesenen Genehmigungen definieren können. Jede Berechtigung wird unter bestimmten Kategorien erfasst, z. B. Journey, Nachrichten oder Angebote, die die verschiedenen Funktionen oder Objekte in [!DNL Journey Optimizer] repräsentieren. Weitere Informationen finden Sie im Abschnitt [Berechtigungsebenen](../../administration/high-low-permissions.md).

Darüber hinaus müssen Sie Benutzer, die Zugriff auf Assets Essentials benötigen, zu den Produktprofilen **Assets Essentials Consumer Users** oder/und **Assets Essentials Users** hinzufügen. [Weitere Informationen finden Sie in der Dokumentation zu Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=de){target=&quot;_blank&quot;}.

>[!NOTE]
>Für Journey Optimizer-Produkte, die vor dem 6. Januar 2022 erworben wurden, müssen Sie [!DNL Adobe Experience Manager Assets Essentials] für Ihre Organisation bereitstellen. Weitere Informationen finden Sie im Abschnitt [Bereitstellen von Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

Beim erstmaligen Zugriff auf [!DNL Journey Optimizer] wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.

Um Journeys erstellen und Nachrichten senden zu können, rufen Sie das Menü **ADMINISTRATION** auf. Durchsuchen Sie das Menü **[!UICONTROL Kanäle]**, um Ihre E-Mail-Nachrichten und Voreinstellungen zu konfigurieren.

>[!NOTE]
>Wenn Sie als **Systemadministrator** das Menü **[!UICONTROL Kanäle]** in [!DNL Journey Optimizer] nicht sehen, aktualisieren Sie Ihre Berechtigungen in [Admin Console](https://adminconsole.adobe.com/){_blank}. Auf [dieser Seite](../../administration/permissions.md#edit-product-profile) erfahren Sie, wie Sie Ihr Produktprofil aktualisieren können.

Führen Sie dazu folgende Schritte durch:

1. **Konfigurieren von Nachrichten und Kanälen**: Definieren Sie Voreinstellungen und passen Sie Einstellungen für E-Mail-Nachrichten und Push-Benachrichtigungen an.

   * Definieren Sie **Push-Benachrichtigungseinstellungen** sowohl in [!DNL Adobe Experience Platform] als auch in [!DNL Adobe Experience Platform Launch]. [Weitere Informationen](../../messages/push-gs.md)

   * Erstellen Sie **Nachrichtenvoreinstellungen**, um alle technischen Parameter zu konfigurieren, die für E-Mail-Nachrichten und Push-Benachrichtigungen erforderlich sind. [Weitere Informationen](../../configuration/message-presets.md)

   * Verwalten Sie die Anzahl der Tage, in denen **weitere Zustellversuche** unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](../../configuration/manage-suppression-list.md)

1. **Subdomains zuweisen**: Für jede neue Subdomain, die in Journey Optimizer verwendet werden soll, besteht der erste Schritt darin, sie zuzuweisen. [Weitere Informationen](../../configuration/about-subdomain-delegation.md)

   ![](../../assets/subdomain.png)

1. **Erstellen von IP-Pools**: Verbessern Sie die Zustellbarkeit Ihrer E-Mails und Ihre Reputation, indem Sie IP-Adressen gruppieren, die mit Ihrer Instanz bereitgestellt wurden. [Weitere Informationen](../../configuration/ip-pools.md)

   ![](../../assets/ip-pool.png)

1. **Verwalten der Unterdrückungs- und Zulassungsliste**: Verbessern Sie Ihre Zustellbarkeit durch Unterdrückungs- und Zulassungslisten.

   * Eine [Unterdrückungsliste](../../messages/suppression-list.md) besteht aus E-Mail-Adressen, die Sie von Ihren Sendungen ausschließen möchten, da das Senden an diese Kontakte Ihren Ruf als Versender und Ihre Versandraten beeinträchtigen könnte. Sie können alle E-Mail-Adressen überwachen, die bei einer Journey automatisch vom Versand ausgeschlossen werden, wie ungültige Adressen, Adressen, die stets zu Soft-Bounces führen und sich negativ auf Ihre E-Mail-Reputation auswirken könnten, sowie Empfänger, die eine Spam-Beschwerde gegen eine Ihrer E-Mail-Nachrichten eingelegt haben. Erfahren Sie, wie Sie die [Unterdrückungsliste](../../configuration/manage-suppression-list.md) und [weitere Zustellversuche](../../configuration/retries.md) verwalten.
   ![](../../assets/suppression-list-filtering-example.png)

   * Mit der [Zulassungsliste](../../messages/allow-list.md) können Sie einzelne E-Mail-Adressen oder Domains als die einzigen Empfänger oder Domains angeben, die zum Empfang der E-Mails berechtigt sind, die von einer bestimmten Sandbox gesendet werden. Dadurch können Sie verhindern, dass Sie in einer Testumgebung versehentlich E-Mails an echte Kundenadressen senden. Erfahren Sie, wie Sie die [Zulassungsliste aktivieren](../../messages/allow-list.md).
   Sie erfahren mehr über die Zustellbarkeitsverwaltung in [!DNL Adobe Journey Optimizer] [auf dieser Seite](../../messages/deliverability.md).
