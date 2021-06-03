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
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 72%

---


# Erste Schritte mit der Zuweisung von Subdomains

## Isolieren Sie Ihre Marken, um Ihre Reputation zu schützen.

Sie können Ihre Domain in Subdomains unterteilen, um Ihre Marken oder unterschiedlichen Textsorten (Transaktionsnachrichten, Marketing-Informationen usw.) voreinander zu trennen.
Nehmen wir zum Beispiel die Domain &quot;mybrand.com&quot;, die sowohl Transaktions- als auch Marketing-Nachrichten sendet. In diesem Fall können Sie zwei Subdomains einrichten:

* die Subdomain &quot;info.mybrand.com&quot; für Ihre Transaktionsnachrichten (Kaufbestätigung, Passwortzurücksetzung usw.),
* die Subdomain &quot;marketing.mybrand.com&quot; für Ihre Werbe-E-Mails.

Dies hilft Ihnen, die Reputation Ihrer Domain und anderer Subdomains zu schützen. Wenn z. B. die Subdomain &quot;marketing.mybrand.com&quot; aufgrund schlechter Zustellbarkeit von Internetdienstanbietern auf die Blockierungsliste gesetzt wird, würde dies verhindern, dass die gesamte Domain &quot;mybrand.com&quot; und die Subdomain &quot;info.mybrand.com&quot; ebenfalls auf die Blockierungsliste gesetzt werden.

## Lassen Sie die Ressourcen-URLs für Kunden transparent.

Bei der Implementierung einer Lösung gibt es Anforderungen an nach außen gerichtete Komponenten: Dazu gehören das Einrichten von Links und Webseiten, die verfolgt werden sollen, das Anzeigen von Mirror-Seiten usw.

Diese Anforderungen werden über Komponenten verwaltet, die sowohl von Adobe als auch vom Kunden gehostet werden, und enthalten URLs, die für die Empfänger der E-Mails sichtbar sind. Um URLs zu vermeiden, die auf die zugrunde liegende technische Lösung oder den Hosting-Anbieter hinweisen, können Subdomains eingerichtet werden, die diese Informationen vor den Empfängern der E-Mails verbergen. [Erfahren Sie mehr über die Zuweisung von Domains](https://helpx.adobe.com/de/campaign/kb/domain-name-delegation.html).

## Zuweisung von Subdomains in Journey Optimizer

Journey Optimizer bietet mehrere Funktionen, mit denen Sie Subdomains verwalten können:

* [Delegieren Sie Ihre ](delegate-subdomain.md) Subdomains direkt über die Benutzeroberfläche.
* [Fügen Sie Ihren Subdomains Google TXT-](google-txt.md) Aufzeichnungen hinzu, um den erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen.
* [Greifen Sie auf die für Ihre Subdomains generierten PTR-](ptr-records.md) Aufzeichnungen zu, damit sie von E-Mail-Servern überprüft werden können.
