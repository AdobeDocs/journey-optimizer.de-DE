---
solution: Journey Optimizer
product: Journey Optimizer
title: E-Mail-Subdomains delegieren
description: E-Mail-Subdomains delegieren
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 41%

---

# E-Mail-Subdomains delegieren{#section-overview}

Das Delegieren von E-Mail-Subdomains ist ein wichtiger Schritt in der [Kanalkonfiguration](../using/configuration/get-started-configuration.md), der erforderlich ist, bevor Sie E-Mails über Journey Optimizer senden können. Mit Subdomains können Sie Traffic-Typen (z. B. Marketing oder Transaktionen) isolieren, den Ruf Ihrer Haupt-Domain schützen und die [IP-Aufwärmung) ](../using/configuration/ip-warmup-gs.md). Sie arbeiten zusammen mit [E-Mail-Kanalkonfiguration](../using/email/get-started-email-config.md) und [Zustellbarkeits-Monitoring](../using/reports/deliverability.md), um sicherzustellen, dass Nachrichten die Posteingänge erreichen.

Sie können aus verschiedenen Einrichtungsmethoden auswählen: **Vollständige Delegierung** (Adobe verwaltet das DNS), **CNAME-** oder **benutzerdefinierte Delegierung** (Sie besitzen Zertifikate und DNS). Wenn Sie mit CNAME beginnen, können Sie später ([ benutzerdefinierte Delegierung) ](../using/configuration/custom-subdomain-migration.md) strengere Sicherheit migrieren. Dieser Abschnitt behandelt auch DMARC- und PTR-Einträge, Google TXT-Einträge für Gmail und IP-Pools. Eine allgemeine Anleitung zur Zustellbarkeit finden Sie unter [Erste Schritte mit der Zustellbarkeit](../using/reports/deliverability.md) und [Überwachen von E-Mail-Adressen](monitor-reputation-landing-page.md).

## Delegieren von E-Mail-Subdomains

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Erste Schritte mit der Delegierung von Subdomains

Erfahren Sie mehr über die Vorteile, Konfigurationsmethoden und Überlegungen zum Delegieren von Subdomains in Adobe Journey Optimizer.

[Mit dem Delegieren von Subdomains starten](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Delegieren einer Subdomain

Schrittweise Anleitungen zum Delegieren von Subdomains an Adobe, einschließlich vollständiger Delegierung und CNAME-Einrichtung.

[Informationen zum Delegieren](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg)

Einrichten einer benutzerdefinierten Subdomain

Übernehmen Sie die volle Verantwortung für Ihre Subdomains mit benutzerdefinierter Delegierung. Laden Sie Ihre eigenen SSL-Zertifikate hoch und behalten Sie die volle Kontrolle über die Domain-Konfiguration.

[Einrichten einer benutzerdefinierten Subdomain](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Migrieren von CNAME zur benutzerdefinierten Delegierung

Migrieren vorhandener CNAME-konfigurierter Subdomains in die benutzerdefinierte Delegierung, um Sicherheitsrichtlinien zu erfüllen und die volle Kontrolle über Zertifikate zu erlangen.

[Subdomain migrieren](../using/configuration/custom-subdomain-migration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

Festlegen von DMARC-Einträgen

Konfigurieren Sie DMARC-Einträge, um die Sicherheit und Zustellbarkeit von E-Mails für delegierte Subdomains zu verbessern.

[DMARC jetzt einrichten](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Hinzufügen eines Google TXT-Eintrags

Überprüfen Sie die Zustellbarkeit von Subdomains für Gmail, indem Sie Google TXT-Einträge in Adobe Journey Optimizer hinzufügen.

[Google TXT-Einträge hinzufügen](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Zugreifen auf und Bearbeiten von PTR-Einträgen

Verwalten Sie PTR-Einträge für delegierte Subdomains, bearbeiten Sie diese und verstehen Sie die Aktualisierungsstatus.

[PTR-Einträge bearbeiten](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Erstellen von IP-Pools

Gruppieren Sie IP-Adressen, um die Zustellbarkeit Ihrer E-Mails zu verbessern und die Reputation von Subdomains effektiv zu verwalten.

[Erstellen von IP-Pools](../using/configuration/ip-pools.md)
:::

::::

## Weitere Ressourcen

- **[Konfigurieren von Landingpage-](../using/landing-pages/lp-subdomains.md)**: Einrichten von Subdomains für Landingpages und Abonnementformulare.
- **[Konfigurieren von Web-](../using/web/web-delegated-subdomains.md)**: Delegieren von Subdomains für Web-Erlebnisse und Tracking.
- **[Erste Schritte mit der Kanalkonfiguration](../using/configuration/get-started-configuration.md)** - Übersicht über alle Schritte zur Kanaleinrichtung, einschließlich der Zuweisung von Subdomains.
