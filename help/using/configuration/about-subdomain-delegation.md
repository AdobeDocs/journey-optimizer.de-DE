---
solution: Journey Optimizer
product: journey optimizer
title: Delegation einer Subdomain in  [!DNL Journey Optimizer]
description: Informationen zum Delegieren Ihrer Subdomains
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Optimizer, Delegation
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 316553be4f04e4fc0ae11bc767f7e48f64fc5ccd
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 84%

---

# Subdomain-Delegierung in [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="Ihre delegierten Subdomains werden hier angezeigt."
>abstract="Delegieren Sie Ihre erste Subdomain. Nach Abschluss der Delegierung werden PTR-Einträge erstellt und E-Mail-Kanäle aktiviert."

Das Einrichten einer Subdomain für E-Mail-Journey und -Kampagnen ermöglicht es Marken, unterschiedliche Arten von Traffic (z. B. Marketing-bezogenen vs. betrieblichen) in eigene IP-Pools mit eigenen Domains zu unterteilen, wodurch der IP-Warming-Prozess beschleunigt und die Zustellbarkeit insgesamt verbessert werden kann.

Wenn Sie eine einzige Domain für alle Aufgaben verwenden und diese gesperrt oder zur Blockierungsliste hinzugefügt wird, könnte dies Auswirkungen auf die Zustellung Ihrer betrieblichen E-Mails haben. Probleme mit der Reputation oder die Blockierung einer Domain, die nur für Ihre E-Mail-Marketing-Kommunikation verwendet sind, beeinträchtigen hingegen ausschließlich diesen E-Mail-Verkehr. Wenn Sie Ihre Haupt-Domain als Absenderadresse für mehrere E-Mail-Arten verwenden, kann dies auch die E-Mail-Authentifizierung behindern und dazu führen, dass Ihre Nachrichten blockiert oder in den Spam-Ordner verschoben werden.

>[!CAUTION]
>
>Es kann nicht dieselbe Versand-Domain zum Senden von Nachrichten von [!DNL Adobe Journey Optimizer] und von einem anderen Produkt, z. B. [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage], verwendet werden.

## Warum sollten Subdomains eingerichtet werden? {#why-set-up-subdomains}

Sie können Ihre Domain in Subdomains unterteilen, um Ihre Marken oder unterschiedlichen Textsorten wie etwa Transaktionsnachrichten und Marketing-Informationen voreinander zu trennen.

Nehmen wir zum Beispiel die Domain &quot;mybrand.com&quot;, die sowohl Transaktions- als auch Marketing-Nachrichten sendet. In diesem Fall können Sie zwei Subdomains einrichten:

* die Subdomain &quot;info.mybrand.com&quot; für Ihre Transaktionsnachrichten (Kaufbestätigung, Passwortzurücksetzung usw.),
* die Subdomain &quot;marketing.mybrand.com&quot; für Ihre Werbe-E-Mails.

Dies hilft Ihnen, die Reputation Ihrer Domain und anderer Subdomains zu schützen. Wenn z. B. die Subdomain &quot;marketing.mybrand.com&quot; aufgrund schlechter Zustellbarkeit von Internetdienstanbietern auf die Blockierungsliste gesetzt wird, würde dies verhindern, dass die gesamte Domain &quot;mybrand.com&quot; und die Subdomain &quot;info.mybrand.com&quot; ebenfalls auf die Blockierungsliste gesetzt werden.

Bei der Implementierung einer Lösung gibt es Anforderungen an nach außen gerichtete Komponenten: Dazu gehören das Einrichten von Links und Web-Seiten, die verfolgt werden sollen, das Anzeigen von Mirrorseiten usw.

Diese Anforderungen werden über Komponenten verwaltet, die sowohl von Adobe als auch vom Kunden gehostet werden, und enthalten URLs, die für die Empfänger der E-Mails sichtbar sind. Um URLs zu vermeiden, die auf die zugrunde liegende technische Lösung oder den Hosting-Anbieter hinweisen, können Subdomains eingerichtet werden, die diese Informationen vor den Empfängern der E-Mails verbergen.

**Weitere Informationen**

* Erfahren Sie, wie Sie [Ihre Subdomains](delegate-subdomain.md) direkt über die Benutzeroberfläche delegieren.
* Erfahren Sie, wie Sie [Ihren Subdomains TXT-Einträge von Google](google-txt.md) hinzufügen, um den erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen.
* Erfahren Sie, wie Sie [auf die für Ihre Subdomains generierten PTR-Einträge zugreifen](ptr-records.md), damit sie von E-Mail-Servern überprüft werden können.

## Methoden der Subdomain-Konfiguration {#subdomain-delegation-methods}

Mit der Subdomain-Konfiguration können Sie einen Unterabschnitt Ihrer Domain (technisch gesehen eine „DNS-Zone„) für die Verwendung mit Adobe Journey Optimizer konfigurieren.

Die folgenden Methoden sind für die Einrichtung verfügbar:

### Vollständiges Delegieren einer Subdomain an Adobe (empfohlen) {#full-subdomain-delegation}

[!DNL Journey Optimizer] ermöglicht die vollständige Delegation Ihrer Subdomains an Adobe direkt über die Benutzeroberfläche des Produkts. Auf diese Weise kann Adobe Nachrichten als Managed Service bereitstellen, indem alle DNS-Bereiche, die für die Zustellung, das Rendering und das Tracking erforderlich sind, kontrolliert und verwaltet werden.

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

Adobe stellt sicher, dass Kunden die DNS-Infrastruktur bereitgestellt wird, die zur Erfüllung der branchenüblichen Zustellbarkeitsanforderungen an Domains zum E-Mail-Marketing-Versand erforderlich ist. Gleichzeitig verwaltet und kontrolliert Adobe auch das DNS für Ihre unternehmensinternen E-Mail-Domains.

>[!IMPORTANT]
>
>Die vollständige Subdomain-Delegierung ist die bevorzugte Methode.

In [diesem Abschnitt](delegate-subdomain.md#set-up-subdomain) erfahren Sie, wie Sie eine Subdomain vollständig an Adobe delegieren können.

### Einrichten einer Subdomain mit CNAMEs {#cname-subdomain-setup}

Wenn Sie Domain-spezifische Einschränkungsrichtlinien haben und möchten, dass Adobe nur eine teilweise Kontrolle über den DNS hat, können Sie alle DNS-bezogenen Aktivitäten auf Ihrer Seite durchführen.

Mit der Einrichtung einer CNAME-Subdomain können Sie eine Subdomain erstellen und CNAMEs verwenden, um auf Adobe-spezifische Einträge zu verweisen. Mit dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich, um eine Umgebung für das Senden, Rendern und Tracking von E-Mails einzurichten.

>[!CAUTION]
>
>Die CNAME-Methode wird empfohlen, wenn die Richtlinien Ihrer Organisation die Methode der vollständigen Subdomain-Delegierung einschränken. Diese Methode erfordert, dass Sie DNS-Einträge selbst pflegen und verwalten.
>
>Adobe kann keine Unterstützung beim Ändern, Pflegen oder Verwalten von DNS für eine Subdomain anbieten, die über die CNAME-Methode konfiguriert wurde.

In [diesem Abschnitt](delegate-subdomain.md#cname-subdomain-setup) erfahren Sie, wie Sie eine Subdomain mit CNAMEs erstellen, die auf Adobe-spezifische Einträge verweisen.

### Verwenden einer benutzerdefinierten Subdomain {#custom-subdomain-delegation}

Mit der benutzerdefinierten Delegierungsmethode können Sie alle DNS-Aspekte, die für die Zustellung, das Rendering und das Tracking von Nachrichten erforderlich sind, vollständig steuern und verwalten.

In diesem Fall besitzen und verwalten Sie unsere eigenen Subdomains und haben die volle Kontrolle über die Zertifikate, die im Rahmen dieses Prozesses generiert werden.

Erfahren Sie, wie [eine benutzerdefinierte Subdomain einrichten](delegate-custom-subdomain.md). Wenn Ihre Subdomain derzeit CNAME verwendet, können Sie auch [von CNAME zur benutzerdefinierten Delegierung migrieren](custom-subdomain-migration.md).

## Vergleich der Konfigurationsmethoden

Die nachstehende Tabelle bietet eine Zusammenfassung über die Funktionsweise dieser Methoden sowie den damit verbundenen Aufwand:
<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Journey Optimizer.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Journey Optimizer DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |-->


| Konfigurationsmethode | Funktionsweise | Aufwand |
|---|---|---|
| **Vollständige Zuweisung** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe konfiguriert dann alle für Adobe Journey Optimizer erforderlichen DNS-Einträge.<br/><br/>Bei dieser Konfiguration hat Adobe die volle Verantwortung für die Pflege der Subdomain und aller DNS-Einträge. | Niedrig |
| **CNAME-Methode** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe stellt dann die Einträge bereit, die auf Ihren DNS-Servern platziert werden sollen, und konfiguriert die entsprechenden Werte in den Adobe Journey Optimizer-DNS-Servern.<br/><br/>Bei dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich. | Hoch |
| **Methode „Benutzerdefinierte Delegierung“** | Erstellen Sie den Subdomain- und Namespace-Eintrag – Adobe stellt dann die Einträge bereit, die auf Ihren DNS-Servern platziert werden sollen. Laden Sie das von der Zertifizierungsstelle erhaltene SSL-Zertifikat hoch und schließen Sie die Schritte der Feedback-Schleife ab, indem Sie Domain-Eigentümerschaft und Reporting-E-Mail-Adresse bestätigen.<br/><br/>Bei dieser Konfiguration sind Sie vollständig für die Pflege des DNS verantwortlich. | Sehr hoch |

Weitere Informationen zur Domain-Konfiguration finden Sie in [dieser Dokumentation](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=de){target="_blank"}.

Bei Fragen zu den Methoden der Subdomain-Konfiguration wenden Sie sich an Adobe oder die Kundenunterstützung, um eine Beratung zur Zustellbarkeit anzufordern.


