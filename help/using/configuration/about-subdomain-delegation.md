---
title: Subdomänen delegieren
description: Erfahren Sie, wie Sie Ihre Subdomänen delegieren
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
translation-type: tm+mt
source-git-commit: a65cefd0bbd15ffa389bac910eaceb40181cb38d
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Erste Schritte mit der Subdomänendelegation

## Info zur Subdomänenübertragung

### Isolieren Sie Ihre Marken, um Ihren Ruf zu schützen.

Sie können Ihre Domain in Subdomains unterteilen, um Ihre Marken oder unterschiedlichen Textsorten (Transaktionsnachrichten, Marketing-Informationen usw.) voreinander zu trennen.
Nehmen wir zum Beispiel die Domain &quot;mybrand.com&quot;, die sowohl Transaktions- als auch Marketing-Nachrichten sendet. In diesem Fall können Sie zwei Subdomains einrichten:

* die Subdomain &quot;info.mybrand.com&quot; für Ihre Transaktionsnachrichten (Kaufbestätigung, Passwortzurücksetzung usw.),
* die Subdomain &quot;marketing.mybrand.com&quot; für Ihre Werbe-E-Mails.

Dies hilft Ihnen, die Reputation Ihrer Domain und anderer Subdomains zu schützen. Wenn z. B. die Subdomains &quot;marketing.mybrand.com&quot; aufgrund schlechter Zustellbarkeit von Internetdienstanbietern auf die Blockierungsliste gesetzt werden, würde dies verhindern, dass die gesamte Domain &quot;mybrand.com&quot; und die Subdomain &quot;info.mybrand.com&quot; ebenfalls auf die Blockierungsliste gesetzt werden.

### Transparenz der Ressourcen-URLs für Kunden

Bei der Implementierung einer Lösung gibt es Anforderungen an nach außen gerichtete Komponenten: Dazu gehören das Einrichten von Links und Webseiten, die verfolgt werden sollen, das Anzeigen von Mirrorseiten usw.

Während diese Anforderungen über Komponenten verwaltet werden, die sowohl von der Adobe als auch vom Kunden gehostet werden, enthalten sie URLs, die vom Empfänger der E-Mails gesehen werden können. Um zu vermeiden, dass URLs vorhanden sind, die die zugrunde liegende technische Lösung oder den Hosting-Anbieter angeben, können Subdomänen eingerichtet werden, um dies für den Empfänger der E-Mails transparent zu machen. [Erfahren Sie mehr über die Domänendelegation](https://helpx.adobe.com/de/campaign/kb/domain-name-delegation.html).

## Subdomänendelegation in Journey Optimizer

Journey Optimizer bietet mehrere Funktionen zur Verwaltung von Subdomänen:

* [Delegieren Sie Ihre ](delegate-subdomain.md) Unterdomänen direkt über die Oberfläche,
* [hinzufügen Google TXT-](google-txt.md) Aufzeichnungen Ihrer Subdomänen, um den erfolgreichen Versand von E-Mails an Gmail-Adressen sicherzustellen,
* [Greifen Sie auf die für Ihre Subdomänen generierten PTR-](ptr-records.md) Aufzeichnungen zu, damit sie durch Senden von E-Mail-Servern überprüft werden können.
