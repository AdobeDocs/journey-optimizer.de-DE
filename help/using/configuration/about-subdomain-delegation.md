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
source-git-commit: 8b755351e25ecae9a2058e63919d6512ea0bf153
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 77%

---

# Subdomain-Delegierung in [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="Ihre delegierten Subdomains werden hier angezeigt."
>abstract="Delegieren Sie Ihre erste Subdomain. Nach Abschluss der Delegierung werden PTR-Einträge erstellt und E-Mail-Kanäle aktiviert."

Das Einrichten einer Subdomain für E-Mail-Kampagnen ermöglicht es Marken, unterschiedliche Arten von Traffic (z. B. Marketing-bezogenen vs. betrieblichen) in eigene IP-Pools mit eigenen Domains zu unterteilen, wodurch der IP-Warming-Prozess beschleunigt und die Zustellbarkeit insgesamt verbessert werden kann.

Wenn Sie eine einzige Domain für alle Aufgaben verwenden und diese gesperrt oder zur Blockierungsliste hinzugefügt wird, könnte dies Auswirkungen auf die Zustellung Ihrer betrieblichen E-Mails haben. Probleme mit der Reputation oder die Blockierung einer Domain, die nur für Ihre E-Mail-Marketing-Kommunikation verwendet sind, beeinträchtigen hingegen ausschließlich diesen E-Mail-Verkehr. Wenn Sie Ihre Haupt-Domain als Absenderadresse für mehrere E-Mail-Arten verwenden, kann dies auch die E-Mail-Authentifizierung behindern und dazu führen, dass Ihre Nachrichten blockiert oder in den Spam-Ordner verschoben werden.

>[!CAUTION]
>
>Es kann nicht dieselbe Versand-Domain zum Senden von Nachrichten von [!DNL Adobe Journey Optimizer] und von einem anderen Produkt, z. B. [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage], verwendet werden.

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

Mit der Subdomain-Konfiguration können Sie einen Unterabschnitt Ihrer Domain (technisch gesehen eine „DNS-Zone„) für die Verwendung mit Adobe Campaign konfigurieren.

Die verfügbaren Einrichtungsmethoden sind wie folgt.

### Subdomain vollständig an Adobe delegieren (empfohlen) {#full-subdomain-delegation}

[!DNL Journey Optimizer] ermöglicht die vollständige Delegation Ihrer Subdomains an Adobe direkt über die Benutzeroberfläche des Produkts. Auf diese Weise kann Adobe Nachrichten als Managed Service bereitstellen, indem alle Aspekte des DNS, die für die Zustellung, das Rendering und das Tracking von E-Mail-Kampagnen erforderlich sind, kontrolliert und verwaltet werden.

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

Adobe stellt sicher, dass Kunden die DNS-Infrastruktur bereitgestellt wird, die zur Erfüllung der branchenüblichen Zustellbarkeitsanforderungen an Domains zum E-Mail-Marketing-Versand erforderlich ist. Gleichzeitig verwaltet und kontrolliert Adobe auch das DNS für Ihre unternehmensinternen E-Mail-Domains.

>[!IMPORTANT]
>
>Die vollständige Subdomain-Delegierung ist die bevorzugte Methode.

Wie Sie eine Subdomain vollständig an Adobe delegieren, erfahren Sie in [diesem Abschnitt](delegate-subdomain.md#set-up-subdomain).

### Einrichten einer Subdomain mit CNAMEs {#cname-subdomain-setup}

Wenn Sie Domain-spezifische Einschränkungsrichtlinien haben und möchten, dass Adobe nur eine teilweise Kontrolle über den DNS hat, können Sie alle DNS-bezogenen Aktivitäten auf Ihrer Seite durchführen.

Mit der Einrichtung einer CNAME-Subdomain können Sie eine Subdomain erstellen und CNAMEs verwenden, um auf Adobe-spezifische Einträge zu verweisen. Mit dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich, um eine Umgebung für das Senden, Rendern und Tracking von E-Mails einzurichten.

>[!CAUTION]
>
>Die Methode CNAME wird empfohlen, wenn die Richtlinien Ihrer Organisation die vollständige Subdomain-Delegierung nicht erlauben. Dieser Ansatz erfordert, dass Sie DNS-Einträge selbst pflegen und verwalten.
>
>Adobe kann keine Unterstützung beim Ändern, Pflegen oder Verwalten des DNS für eine Subdomain anbieten, die über die CNAME-Methode konfiguriert wurde.

In diesem Abschnitt erfahren Sie, wie Sie eine Subdomain mit CNAMEs erstellen, um auf Adobe-spezifische Einträge [ verweisen](delegate-subdomain.md#cname-subdomain-setup).

### Verwenden einer benutzerdefinierten Subdomain {#custom-subdomain-delegation}

Mit der benutzerdefinierten Delegierungsmethode können Sie alle DNS-Aspekte, die für die Zustellung, das Rendering und das Tracking von Nachrichten erforderlich sind, vollständig steuern und verwalten.

In diesem Fall besitzen und verwalten Sie unsere eigenen Subdomains und haben die volle Kontrolle über die Zertifikate, die im Rahmen dieses Prozesses generiert werden.

Erfahren Sie in ([ Abschnitt), wie Sie eine benutzerdefinierte Domain ](delegate-custom-subdomain.md).

## Vergleich der Konfigurationsmethoden

Die nachstehende Tabelle bietet eine Zusammenfassung über die Funktionsweise dieser Methoden sowie den damit verbundenen Aufwand:

| Konfigurationsmethode | Funktionsweise | Aufwand |
|---|---|---|
| **Vollständige Zuweisung** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe konfiguriert dann alle für Adobe Campaign erforderlichen DNS-Einträge.<br/><br/>Bei dieser Konfiguration hat Adobe die volle Verantwortung für die Pflege der Subdomain und aller DNS-Einträge. | Niedrig |
| **CNAME-Methode** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe stellt dann die Einträge bereit, die auf Ihren DNS-Servern abgelegt werden sollen, und konfiguriert die entsprechenden Werte in den Adobe Campaign-DNS-Servern.<br/><br/>Bei dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich. | Hoch |
| **Benutzerdefinierte Delegierungsmethode** | Subdomain- und Namespace-Eintrag erstellen - Adobe stellt dann die Einträge bereit, die auf Ihren DNS-Servern platziert werden sollen. Laden Sie das von der Zertifizierungsstelle erhaltene SSL-Zertifikat hoch und führen Sie die Schritte der Feedback-Schleife durch Überprüfen der Domain-Eigentümerschaft und der Reporting-E-Mail-Adresse aus.<br/><br/>Bei diesem Setup sind Sie vollständig für die Pflege des DNS verantwortlich. | Sehr hoch |

Weitere Informationen zur Domain-Konfiguration finden Sie in [dieser Dokumentation](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=de){target="_blank"}.

Wenn Sie Fragen zu den Konfigurationsmethoden von Subdomains haben, wenden Sie sich an Adobe oder die Kundenunterstützung, um eine Beratung zur Zustellbarkeit anzufordern.


