---
title: Zuweisen von Subdomains
description: Informationen zum Zuweisen Ihrer Subdomains
internal: n
snippet: y
feature: Anwendungskonfiguration
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 94%

---


# Subdomain-Erstellung in [!DNL Journey Optimizer]

Das Einrichten einer Subdomain für E-Mail-Kampagnen ermöglicht es Marken, unterschiedliche Arten von Traffic (z. B. Marketing-bezogenen vs. betrieblichen) in eigene IP-Pools mit eigenen Domains zu unterteilen, wodurch der IP-Warming-Prozess beschleunigt und die Zustellbarkeit insgesamt verbessert werden kann. Wenn Sie eine einzige Domain für alle Aufgaben verwenden und diese gesperrt oder zur Blockierungsliste hinzugefügt wird, könnte dies Auswirkungen auf die Zustellung Ihrer betrieblichen E-Mails haben. Probleme mit der Reputation oder die Blockierung einer Domain, die nur für Ihre E-Mail-Marketing-Kommunikation verwendet sind, beeinträchtigen hingegen ausschließlich diesen E-Mail-Verkehr. Wenn Sie Ihre Haupt-Domain als Absenderadresse für mehrere E-Mail-Arten verwenden, kann dies auch die E-Mail-Authentifizierung behindern und dazu führen, dass Ihre Nachrichten blockiert oder in den Spam-Ordner verschoben werden.

Sie können Ihre Domain in Subdomains unterteilen, um Ihre Marken oder unterschiedlichen Textsorten wie etwa Transaktionsnachrichten und Marketing-Informationen voreinander zu trennen.

Nehmen wir zum Beispiel die Domain &quot;mybrand.com&quot;, die sowohl Transaktions- als auch Marketing-Nachrichten sendet. In diesem Fall können Sie zwei Subdomains einrichten:

* die Subdomain &quot;info.mybrand.com&quot; für Ihre Transaktionsnachrichten (Kaufbestätigung, Passwortzurücksetzung usw.),
* die Subdomain &quot;marketing.mybrand.com&quot; für Ihre Werbe-E-Mails.

Dies hilft Ihnen, die Reputation Ihrer Domain und anderer Subdomains zu schützen. Wenn z. B. die Subdomain &quot;marketing.mybrand.com&quot; aufgrund schlechter Zustellbarkeit von Internetdienstanbietern auf die Blockierungsliste gesetzt wird, würde dies verhindern, dass die gesamte Domain &quot;mybrand.com&quot; und die Subdomain &quot;info.mybrand.com&quot; ebenfalls auf die Blockierungsliste gesetzt werden.

Bei der Implementierung einer Lösung gibt es Anforderungen an nach außen gerichtete Komponenten: Dazu gehören das Einrichten von Links und Web-Seiten, die verfolgt werden sollen, das Anzeigen von Mirror-Seiten usw.

Diese Anforderungen werden über Komponenten verwaltet, die sowohl von Adobe als auch vom Kunden gehostet werden, und enthalten URLs, die für die Empfänger der E-Mails sichtbar sind. Um URLs zu vermeiden, die auf die zugrunde liegende technische Lösung oder den Hosting-Anbieter hinweisen, können Subdomains eingerichtet werden, die diese Informationen vor den Empfängern der E-Mails verbergen.

**Weitere Informationen**

* Erfahren Sie, wie Sie [Ihre Subdomains](delegate-subdomain.md) direkt über die Benutzeroberfläche erstellen.
* Erfahren Sie, wie Sie [Ihren Subdomains Google TXT-Einträge](google-txt.md) hinzufügen, um einen erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen.
* Erfahren Sie, wie Sie [auf die für Ihre Subdomains generierten PTR-Datensätze](ptr-records.md) zugreifen, damit sie von E-Mail-Servern überprüft werden können.
