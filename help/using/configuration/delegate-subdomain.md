---
title: Zuweisen von Subdomains
description: Informationen zum Zuweisen Ihrer Subdomains
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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 848b6e84e0a4469be438e89dfc3e3e4a72dc6b6c
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 56%

---


# Zuweisen einer Subdomain

Der Eigentümer eines Domain-Namens (technisch: einer DNS-Zone) kann einer anderen Entität eine Untergliederung des Domain-Namens (technisch: eine untergeordnete DNS-Zone) zuzuweisen. Wenn also ein Kunde die Zone „example.com“ verwaltet, kann er Adobe die untergeordnete Zone „marketing.example.com“ zuweisen.

Durch das Zuweisen einer Subdomain an [!DNL Journey Optimizer] kann Adobe sicherstellen, dass Kunden die DNS-Infrastruktur bereitgestellt wird, die zur Erfüllung der branchenüblichen Zustellbarkeits-Anforderungen an Domains zum E-Mail-Marketing-Versand erforderlich ist. Gleichzeitig verwaltet und kontrolliert Adobe auch das DNS für die unternehmensinternen E-Mail-Domains.

[!DNL Journey Optimizer] ermöglicht die vollständige Zuweisung Ihrer Subdomains an Adobe direkt über die Benutzeroberfläche des Produkts. Auf diese Weise kann Adobe Nachrichten als Managed Service bereitstellen, indem alle Aspekte des DNS, die für die Zustellung, das Rendering und das Tracking von E-Mail-Kampagnen erforderlich sind, kontrolliert und verwaltet werden.

>[!NOTE]
>
>Standardmäßig können Sie mit dem Lizenzvertrag für [!DNL Journey Optimizer] bis zu 10 Subdomains zuweisen. Wenden Sie sich an Ihren Ansprechpartner bei Adobe, wenn Sie diese Einschränkung erhöhen möchten.
>
>Die Verwendung von CNAMEs für die Zuweisung von Subdomains wird von Journey Optimizer derzeit nicht unterstützt.

Gehen Sie wie folgt vor, um eine neue Subdomain zuzuweisen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]**/**[!UICONTROL Subdomains]** auf und klicken Sie dann auf **[!UICONTROL Subdomain zuweisen]**.

   ![](../assets/subdomain-delegate.png)

1. Geben Sie den Namen der zuzuweisenden Subdomain an.

   ![](../assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Es ist nicht zulässig, Adobe eine ungültige Subdomain zuzuweisen. Vergewissern Sie sich, dass Sie eine gültige Subdomain eingeben, die Ihrem Unternehmen gehört, z. B. marketing.ihrunternehmen.com.
   >
   >Beachten Sie, dass Subdomains mit mehreren Ebenen, wie email.marketing.ihrunternehmen.com, derzeit nicht unterstützt werden.

1. Die Liste der Einträge, die auf Ihren DNS-Servern gespeichert werden sollen, wird angezeigt. Kopieren Sie diese Einträge entweder einzeln oder durch Herunterladen einer CSV-Datei, und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um die passenden DNS-Einträge zu generieren.

1. Stellen Sie sicher, dass alle DNS-Einträge aus den vorherigen Schritten in Ihrer Domain-Hosting-Lösung generiert wurden. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie die Checkbox „Ich bestätige...“ und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Sie können die Einträge erstellen und die Subdomain-Konfiguration später über die Schaltfläche **[!UICONTROL Als Entwurf speichern]** übermitteln. Anschließend können Sie die Zuweisung der Subdomain fortsetzen, indem Sie sie über die Liste der Subdomains öffnen.

1. Nachdem die Subdomain-Zuweisung übermittelt wurde, wird die Subdomain in der Liste mit dem Status **[!UICONTROL In Verarbeitung]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](access-subdomains.md).

   ![](../assets/subdomain-processing.png)

   Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchführt, die bis zu 3 Stunden dauern können. Weiterführende Informationen finden Sie in diesem [Abschnitt](#subdomain-validation).

1. Sobald die Prüfungen erfolgreich abgeschlossen wurden, erhält die Subdomain den Status **[!UICONTROL Erfolgreich]**. Sie kann nun zum Versand von Nachrichten verwendet werden.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)

## Subdomain-Validierung {#subdomain-validation}

Die folgenden Prüfungen und Aktionen werden durchgeführt, bis die Subdomain verifiziert ist und zum Senden von Nachrichten verwendet werden kann.

>[!NOTE]
>
>Diese Schritte werden nach Adobe ausgeführt und können bis zu 3 Stunden dauern.

1. **Vorab validieren**: Adobe prüft, ob die Subdomain an Adobe DNS (NS-Eintrag, SOA-Datensatz, Zone-Setup, Eigentumsdatensatz) delegiert wurde. Wenn der Vorab-Validierungsschritt fehlschlägt, wird ein Fehler zusammen mit dem entsprechenden Grund zurückgegeben. Andernfalls wird die Adobe mit dem nächsten Schritt fortgesetzt.

1. **Konfigurieren des DNS für die Domain**:

   * **MX-Eintrag**: E-Mail-eXchange-Datensatz - Mail-Serverdatensatz, der eingehende E-Mails verarbeitet, die an die Subdomain gesendet werden.
   * **SPF-Eintrag**: Sender Policy Framework-Datensatz - Listet die IPs der E-Mail-Server auf, die E-Mails von der Subdomain senden können.
   * **DKIM-Datensatz**: DomainKeys Identified Mail-Standarddatensatz - Verwendet eine Verschlüsselung mit öffentlichem und privatem Schlüssel zur Authentifizierung der Nachricht, um das Spoofing zu vermeiden.
   * **A**: Standard-IP-Zuordnung.

1. **Erstellen von Tracking- und Mirror-URLs**: Wenn die Domäne email.example.com ist, lautet die tracking/mirror-Domäne data.email.example.com. Sie wird durch die Installation des SSL-Zertifikats gesichert.

1. **Bereitstellung von CDN CloudFront**: Wenn CDN noch nicht eingerichtet ist, stellt Adobe es für die Imsorg bereit.

1. **Erstellen einer CDN-Domäne**: Wenn die Domäne email.example.com ist, lautet die CDN-Domäne cdn.email.example.com.

1. **Erstellen und Anfügen eines CDN-SSL-Zertifikats**: Adobe erstellt das CDN-Zertifikat für die CDN-Domäne und hängt das Zertifikat an die CDN-Domäne an.

1. **Forward DNS** erstellen: Wenn dies die erste Subdomain ist, die Sie delegieren, erstellt Adobe das Weiterleitungs-DNS, das zum Erstellen von PTR-Datensätzen erforderlich ist - eine für jede Ihrer IPs.

1. **PTR-Datensatz erstellen**: PTR-Einträge, auch als Reverse-DNS-Eintrag bezeichnet, werden von den ISPs benötigt, damit sie die E-Mails nicht als Spam markieren. Gmail empfiehlt auch, für jede IP-Adresse PTR-Einträge zu haben. Adobe erstellt PTR-Datensätze nur, wenn Sie die erste Subdomain, eine für jede IP-Adresse, alle IP-Adressen, die auf die erste Subdomain verweisen, zuweisen. Wenn die IP beispielsweise *192.1.2.1* lautet und die Subdomain *email.example.com* lautet, lautet der PTR-Datensatz: *192.1.2.1 PTR r1.email.example.com*. Sie können den PTR-Datensatz anschließend aktualisieren, um auf die neue zugewiesene Domäne zu verweisen.