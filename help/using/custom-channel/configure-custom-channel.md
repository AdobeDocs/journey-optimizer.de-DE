---
title: Konfigurieren eines benutzerdefinierten Kanals - Übersicht
description: Erfahren Sie, welche Schritte ein Administrator zur Konfiguration eines benutzerdefinierten Kanals in Adobe Journey Optimizer ausführen muss, von der Erstellung des Kanals bis zur Einrichtung einer Kanalkonfiguration.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 9%

---


# Konfigurieren eines benutzerdefinierten Kanals {#custom-channel-configuration}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Die Konfiguration eines benutzerdefinierten Kanals ist eine Administratoraufgabe, die einmal pro Kanal stattfindet. Nachdem der Kanal konfiguriert wurde, können Marketing-Fachleute ihn sofort in Kampagnen, Journey und orchestrierten Kampagnen auswählen - genau wie in jedem nativen [!DNL Journey Optimizer].

Der Konfigurationsprozess umfasst vier Schritte: Definieren des Kanals selbst (Endpunkt, Authentifizierung, Payload), Verwalten der zur Authentifizierung von Anfragen verwendeten API-Anmeldeinformationen, optional Delegieren einer Subdomain für das Linktracking und schließlich Erstellen einer Kanalkonfiguration, die Marketer zum Zeitpunkt der Bearbeitung auswählen.

>[!NOTE]
>
>Bevor Sie beginnen, überprüfen Sie die Voraussetzungen und Leitplanken für benutzerdefinierte Kanäle, einschließlich der erforderlichen Berechtigungen und unterstützten Authentifizierungsmethoden.

## Konfigurationsschritte {#steps}

Der Konfigurationsprozess für einen benutzerdefinierten Kanal besteht aus vier Schritten. Jeder Schritt wird in den folgenden verlinkten Artikeln detailliert beschrieben.

| Schritt | Was Sie tun | Warum dies wichtig ist | Link |
| --- | --- | --- | --- |
| **1. Erstellen Sie den benutzerdefinierten Kanal** | Definieren Sie die Endpunkt-URL, die Kopfzeilen, die Drosselungsrichtlinie, den Authentifizierungstyp und die Payload-Struktur der Nachricht im Channel Builder. | Dies ist die Kerndefinition Ihres Kanals. Sie sagt [!DNL Journey Optimizer], wie eine Nachricht gesendet wird und wie diese Nachricht aussieht. | [Weitere Informationen](create-custom-channel.md) |
| **2. API-Anmeldeinformationen verwalten** | Erstellen und verwalten Sie die Sätze von Anmeldeinformationen, die zum Authentifizieren von Anfragen an Ihren Endpunkt verwendet werden. | Mit mehreren Berechtigungssätzen können Sie dieselbe Kanaldefinition in verschiedenen Marken oder Umgebungen wiederverwenden, ohne den Kanal zu duplizieren. | [Weitere Informationen](custom-channel-api-credentials.md) |
| **3. Subdomain delegieren** *(optional)* | Delegieren Sie eine Subdomain speziell für Ihren benutzerdefinierten Kanal. | Nur erforderlich, wenn die Payload der Nachricht verfolgbare Links enthält. Ohne delegierte Subdomain ist das Linktracking für diesen Kanal nicht verfügbar. | [Weitere Informationen](custom-channel-subdomains.md) |
| **4. Erstellen Sie eine Kanalkonfiguration** | Erstellen Sie eine benannte Voreinstellung, die den benutzerdefinierten Kanal mit einem bestimmten Satz von Anmeldeinformationen, einer Subdomain und optionalen Payload-Standardwerten verknüpft. | Beim Erstellen von Kampagnen oder Journey wählen Marketing-Experten einen benutzerdefinierten Kanal und eine zugehörige Kanalkonfiguration aus. Sie können mehrere Konfigurationen für denselben Kanal erstellen (z. B. eine pro Marke oder Region). | [Weitere Informationen](custom-channel-configuration.md) |

<!--
## Get started {#get-started}

1. [Create the custom channel](create-custom-channel.md) by defining its endpoint, authentication method, and message payload structure in the Channel Builder.
1. [Set up API credentials](custom-channel-api-credentials.md) to authenticate requests sent to your endpoint — required for all authentication types other than **None**.
1. [Delegate a subdomain](custom-channel-subdomains.md) if your message payload includes trackable links and you want them served from a branded domain.
1. [Create a channel configuration](custom-channel-configuration.md) to produce the named preset that marketers will select when building campaigns and journeys.


-->