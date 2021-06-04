---
title: Zuweisen von Subdomains
description: Erfahren Sie, wie Sie Ihre Subdomains zuweisen
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: e569e992530df5429ffb96f78ba28b53de0ded81
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 17%

---


# Zuweisen einer Subdomain

Der Eigentümer eines Domain-Namens (technisch: einer DNS-Zone) kann einer anderen Entität eine Untergliederung des Domain-Namens (technisch: eine untergeordnete DNS-Zone) zuzuweisen. Wenn ein Kunde die Zone &quot;example.com&quot;verarbeitet, kann er die Unterzone &quot;marketing.example.com&quot;an Adobe delegieren.

Durch die Zuweisung einer Subdomain zur Verwendung mit Adobe Optimizer können sich Kunden auf die Adobe verlassen, die DNS-Infrastruktur zu verwalten, die erforderlich ist, um die branchenüblichen Zustellbarkeitsanforderungen für ihre E-Mail-Marketing-Versanddomänen zu erfüllen, und gleichzeitig das DNS für ihre E-Mail-Marketing-Subdomains zu verwalten und zu kontrollieren.
interne E-Mail-Domänen.

Mit Journey Optimizer können Sie Ihre Subdomains vollständig der Adobe zuweisen. Dadurch kann Adobe Nachrichten als verwalteten Dienst bereitstellen, indem alle DNS-Bereiche kontrolliert und gewartet werden, die für die Zustellung, das Rendering und die Verfolgung von E-Mail-Kampagnen erforderlich sind.

>[!NOTE]
>
>Standardmäßig können Sie mit dem Lizenzvertrag [!DNL Journey Optimizer] bis zu 10 Subdomains zuweisen. Wenden Sie sich an Ihren Ansprechpartner bei der Adobe, wenn Sie diese Einschränkung erhöhen möchten.
>
>Die Verwendung von CNAMEs für die Zuweisung von Subdomains wird von Journey Optimizer derzeit nicht unterstützt.

Gehen Sie wie folgt vor, um eine neue Subdomain zuzuweisen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Subdomains]** auf und klicken Sie dann auf **[!UICONTROL Subdomain delegieren]**.

   ![](../assets/subdomain-delegate.png)

1. Geben Sie den Namen der zu delegierenden Subdomain an.

   ![](../assets/subdomain-name.png)

1. Die Liste der Einträge, die auf Ihren DNS-Servern gespeichert werden sollen, wird angezeigt. Kopieren Sie diese Einträge entweder einzeln oder durch Herunterladen einer CSV-Datei, und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um die passenden DNS-Einträge zu generieren.

   Stellen Sie sicher, dass alle DNS-Einträge in Ihrer Domain-Hosting-Lösung generiert wurden. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie das Kontrollkästchen &quot;Ich bestätigen..&quot; und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Sie können die Datensätze erstellen und die Subdomain-Konfiguration später über die Schaltfläche **[!UICONTROL Als Entwurf speichern]** übermitteln. Anschließend können Sie die Zuweisung der Subdomain fortsetzen, indem Sie sie über die Liste der Subdomains öffnen.

1. Nachdem die Subdomain-Zuweisung gesendet wurde, wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](access-subdomains.md).

   Die folgenden Prüfungen und Aktionen werden durchgeführt, bis die Subdomain verifiziert ist und zum Senden von Nachrichten verwendet werden kann.

   Dieser Schritt wird von der Adobe ausgeführt und kann bis zu 3 Stunden dauern.

   1. Überprüfen Sie, ob die Subdomain an das Adobe DNS (NS-Eintrag, SOA-Datensatz, Zone-Setup, Eigentümerdatensatz) delegiert wurde.
   1. DNS für die Domäne konfigurieren,
   1. Erstellen von Tracking- und Mirror-URLs,
   1. Bereitstellung der CDN Cloud-Front,
   1. Erstellen, validieren und anhängen des CDN-SSL-Zertifikats,
   1. Weiterleitungs-DNS erstellen,
   1. Erstellen Sie einen PTR-Datensatz.

   ![](../assets/subdomain-processing.png)

1. Sobald die Prüfungen erfolgreich sind, erhält die Subdomain den Status **[!UICONTROL Erfolg]**. Es kann zum Versand von Nachrichten verwendet werden.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)


