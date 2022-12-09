---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer - Erste Schritte für Systemadministratoren
description: Als Systemadministrator erfahren Sie mehr darüber, wie Sie mit Journey Optimizer arbeiten.
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Erste Schritte für Systemadministratoren {#get-started-sys-admins}

Bevor Sie mit der Verwendung von [!DNL Adobe Journey Optimizer], sind mehrere Schritte erforderlich, um Ihre Umgebung vorzubereiten.  Führen Sie diese Schritte aus, damit die Variable [Dateningenieur](data-engineer.md) und [Journey Practice-Verantwortlicher](marketer.md) kann mit der Arbeit mit [!DNL Adobe Journey Optimizer].


Als **Systemadministrator**, müssen Sie **Produktprofile und Berechtigungen verstehen** für die Sandbox-Verwaltung und Kanalkonfiguration. Außerdem müssen Sie Sandboxes einrichten und für die verfügbaren Produktprofile verwalten. Anschließend können Sie Produktprofilen Team-Mitglieder zuweisen.

Diese Funktionen können von **[!UICONTROL Product administrators]** , die Zugriff auf die Admin Console haben. [Weitere Informationen zur Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Informationen zur Zugriffsverwaltung finden Sie auf den folgenden Seiten:

1. **Sandboxes erstellen** , um Ihre Instanzen in separate, isolierte virtuelle Umgebungen zu unterteilen. **Sandboxes** werden in [!DNL Journey Optimizer]. Weitere Informationen finden Sie unter [Sandboxes](../../administration/sandboxes.md) Abschnitt.

   >[!NOTE]
   >Als **Systemadministrator**, wenn die **[!UICONTROL Sandboxes]** Menü in [!DNL Journey Optimizer], aktualisieren Sie Ihre Berechtigungen in der [Admin Console](https://adminconsole.adobe.com/){_blank}. Erfahren Sie, wie Sie Ihr Produktprofil aktualisieren können in [diese Seite](../../administration/permissions.md#edit-product-profile).

1. **Produktprofile verstehen**. Produktprofile sind eine Reihe von Einzelrechten, die Benutzern den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche ermöglichen. Weitere Informationen finden Sie unter [Vordefinierte Produktprofile](../../administration/ootb-product-profiles.md) Abschnitt.

1. **Berechtigungen festlegen** für Produktprofile, einschließlich **Sandboxes** und geben Sie Zugriff auf Ihre Team-Mitglieder, indem Sie sie verschiedenen Produktprofilen zuweisen. Dieser Schritt wird im [Admin Console](https://adminconsole.adobe.com/){_blank}. Berechtigungen sind Einzelrechte, mit denen Sie die Berechtigungen definieren können, die **[!UICONTROL Product profile]**. Jede Berechtigung wird unter Funktionen erfasst, z. B. Journey oder Angebote, die die verschiedenen Funktionen oder Objekte in [!DNL Journey Optimizer]. Weitere Informationen finden Sie unter [Berechtigungsebenen](../../administration/high-low-permissions.md) Abschnitt.

Darüber hinaus müssen Sie Benutzer, die Zugriff auf Assets Essentials benötigen, zum **Assets Essentials Consumer Users** oder/und **Assets Essentials-Benutzer** Produktprofile. [Weitere Informationen finden Sie in der Dokumentation zu Assets Essentials .](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

>[!NOTE]
>Für Journey Optimizer-Produkte, die vor dem 6. Januar 2022 erworben wurden, müssen Sie Folgendes bereitstellen: [!DNL Adobe Experience Manager Assets Essentials] für Ihre Organisation. Weitere Informationen finden Sie unter [Bereitstellen von Assets - Grundlagen](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html)Abschnitt {target=&quot;_blank&quot;}.

Beim Zugriff auf [!DNL Journey Optimizer] Zum ersten Mal wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.

Um Ihre Journeys zu erstellen und Nachrichten zu senden, rufen Sie die **VERWALTUNG** Menü. Durchsuchen Sie die **[!UICONTROL Channels]** Menü zum Konfigurieren Ihrer Nachrichten und Kanalflächen (d. h. der Nachrichtenvorgaben).

>[!NOTE]
>Als **Systemadministrator**, wenn die **[!UICONTROL Channels]** Menü in [!DNL Journey Optimizer], aktualisieren Sie Ihre Berechtigungen in der [Admin Console](https://adminconsole.adobe.com/){_blank}. Erfahren Sie, wie Sie Ihr Produktprofil aktualisieren können in [diese Seite](../../administration/permissions.md#edit-product-profile).

Führen Sie die folgenden Schritte aus:

1. **Nachrichten und Kanäle konfigurieren**: Definieren von Oberflächen, Anpassen und Anpassen von E-Mail-, SMS- und Push-Nachrichten-Einstellungen

   * Definieren **Push-Benachrichtigungseinstellungen** in beiden [!DNL Adobe Experience Platform] und [!DNL Adobe Experience Platform Launch]. [Weitere Infos](../../push/push-gs.md)

   * Erstellen **Kanaloberflächen** (d. h. Nachrichtenvorgaben) zum Konfigurieren aller technischen Parameter, die für E-Mail, SMS und Push-Benachrichtigungen erforderlich sind. [Weitere Infos](../../configuration/channel-surfaces.md)

   * Konfigurieren Sie die **SMS-Kanal** um alle für SMS erforderlichen technischen Parameter zu konfigurieren. [Weitere Infos](../../sms/sms-configuration.md)

   * Verwalten der Anzahl von Tagen, in denen **retries** werden durchgeführt, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Infos](../../configuration/manage-suppression-list.md)

1. **Zuweisen von Subdomains**: für jede neue Subdomain, die in Journey Optimizer verwendet werden soll, besteht der erste Schritt darin, sie zu delegieren. [Weitere Infos](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Erstellen von IP-Pools**: Verbessern Sie die Zustellbarkeit und Reputation Ihrer E-Mail, indem Sie IP-Adressen gruppieren, die mit Ihrer Instanz bereitgestellt wurden. [Weitere Infos](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Verwalten der Unterdrückungs- und Zulassungslisten**: Zustellbarkeit durch Unterdrückung und Zulassungslisten verbessern

   * A [Unterdrückungsliste](../../reports/suppression-list.md) besteht aus E-Mail-Adressen, die Sie von Ihren Sendungen ausschließen möchten, da der Versand an diese Kontakte Ihrer Reputation und den Versandraten schaden könnte. Sie können alle E-Mail-Adressen überwachen, die automatisch vom Versand in einer Journey ausgeschlossen werden, z. B. ungültige Adressen, Adressen, die konsistent Softbounce verwenden und sich negativ auf Ihre E-Mail-Reputation auswirken könnten, sowie Empfänger, die eine Spam-Beschwerde irgendeiner Art gegen eine Ihrer E-Mail-Nachrichten richten. Erfahren Sie, wie Sie die [Unterdrückungsliste](../../configuration/manage-suppression-list.md) und [retries](../../configuration/retries.md).
   ![](../assets/suppression-list-filtering-example.png)

   * Die [Zulassungsliste](../../configuration/allow-list.md) ermöglicht die Angabe einzelner E-Mail-Adressen oder Domains, die als einzige Empfänger oder Domains berechtigt sind, E-Mails zu empfangen, die Sie von einer bestimmten Sandbox aus senden. Dadurch können Sie verhindern, dass Sie in einer Testumgebung versehentlich E-Mails an echte Kundenadressen senden. Erfahren Sie, wie Sie [die Zulassungsliste aktivieren](../../configuration/allow-list.md).
   Erfahren Sie mehr über die Verwaltung der Zustellbarkeit in [!DNL Adobe Journey Optimizer] [auf dieser Seite](../../reports/deliverability.md).
