---
solution: Journey Optimizer
product: journey optimizer
title: Aktivieren des Modus mit hohem Durchsatz für API-ausgelöste Kampagnen
description: Erfahren Sie, wie Sie den Modus „Hoher Durchsatz“ für API-ausgelöste Kampagnen aktivieren.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
source-git-commit: 5a6abcd48495a66496495e62c6027c2fd0fdd4c4
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 5%

---


# Aktivieren des Modus mit hohem Durchsatz für API-ausgelöste Kampagnen {#high-throughput}

Der Modus mit hohem Durchsatz wurde für Unternehmen entwickelt, die **sehr umfangreiches Echtzeit-Transaktionsnachrichten** (bis zu 5.000 Transaktionen pro Sekunde) benötigen. Im Gegensatz zu regulären API-ausgelösten Kampagnen werden Kampagnen mit hohem Durchsatz unabhängig von Adobe-Profilen ausgeführt und erfordern ein anderes Konfigurationsmodell.

Auf dieser Seite wird erläutert, wie sich Kampagnen mit hohem Durchsatz von standardmäßigen, durch APIs ausgelösten Kampagnen, Einrichtungsanforderungen und dem Zeitpunkt unterscheiden.

## Leitlinien und Einschränkungen

* **Zugriff** - Nur in der US-Region für Organisationen verfügbar, die über das Add-on „Transaktionsnachrichten mit hohem Durchsatz“ lizenziert sind.

* **Kanäle**: Derzeit nur für E-Mails verfügbar.

* **Personalization**:

   * Alle Personalisierungen müssen als (kontextuelle Daten) in **API-Payload**. [Erfahren Sie, wie Sie Inhalte mithilfe von kontextuellen Daten personalisieren können](../campaigns/api-triggered-campaign-action.md#contextual)
   * Profilbasierte Personalisierung wird nicht unterstützt. Wenn Profilvariablen verwendet werden, treten Validierungsfehler auf.

* **Personalisierte Kanalkonfigurationen** - Kanalkonfigurationen, die eine [profilbasierte Personalisierung](../email/surface-personalization.md) verwenden, können nicht mit Kampagnen mit hohem Durchsatz verwendet werden. Es können nur Oberflächen ohne Profil-Personalisierung verwendet werden.

* **API-Endpunkt** - Kampagnen mit hohem Durchsatz verwenden einen anderen Endpunkt als von einer Standard-API ausgelöste Kampagnen. Weitere Informationen finden Sie unter [Ausführen einer von einer API ausgelösten Kampagne](../campaigns/trigger-campaigns.md#trigger).

* **Kampagnenexklusivität** - Kampagnen mit hohem Durchsatz verwenden keine Adobe-Profile. Nachrichten werden unabhängig davon zugestellt, ob ein Profil vorhanden ist oder nicht.

  Darüber hinaus kann eine Kampagne nicht sowohl für Anwendungsfälle mit aktiviertem Profil als auch für Anwendungsfälle ohne Profil verwendet werden. Wenn Sie beide benötigen, erstellen Sie zwei separate Kampagnen und stellen Sie sicher, dass das aufrufende System anhand des Kontexts entscheidet, welche Kampagne Trigger werden soll.

## Auswahl zwischen standardmäßigen und Kampagnen mit hohem Durchsatz

Verwenden Sie diese Tabelle, um zu entscheiden, welcher Kampagnentyp einer API-ausgelösten Kampagne zu Ihrem Anwendungsfall passt:

| Funktion/Anforderung | Von der Standard-API ausgelöste Kampagne | Kampagne mit hohem Durchsatz |
|------------------------|---------------------------------|---------------------------|
| **Verfügbarkeit** | Im Basisangebot enthalten | Erfordert das Add-on für Transaktionsnachrichten mit hohem Durchsatz. |
| **Durchsatz** | Bis zu 500 Transaktionen pro Sekunde | Bis zu 5.000 Transaktionen pro Sekunde |
| **Kanäle** | E-Mail, SMS, Push | E-Mail |
| **Personalisierung** | Profil + Kontextuelles in der API-Payload | Nur kontextuelle in der API-Payload |
| **Profil und Stitching** | Existiert oder wird mit Ereignissen erstellt, die mit einem Profil verknüpft sind | Kein Profil |
| **Nachrichtenvolumen** | Standardberechtigungen und Message Packs | Separate Tiered Message Volumes |
| **Infrastruktur** | Standard | Erweitert |
| **Betriebszeit** | 99,9 % | 99,99 % |
| **Konsistenzprüfungs-API** | Ja | Ja |

Mit anderen Worten:

* Wählen Sie **API-ausgelöste Standard** Kampagnen aus, wenn:
   * Sie haben keinen vertraglich festgelegten hohen Durchsatz.
   * Ihr Durchsatzbedarf beträgt &lt;500 TPS.
   * Sie benötigen Personalisierung basierend auf Adobe-Profilen.
   * Die Kampagnendaten sollen für die zukünftige Zielgruppenbestimmung den Profilen zugeordnet werden.
   * Sie möchten einen anderen Kanal als E-Mail verwenden.

* Wählen Sie **Kampagnen mit hohem**) aus, wenn:
   * Sie benötigen einen Durchsatz von >500 TPS.
   * Sie benötigen keine Profilzuordnung.
   * Sie können die gesamte Personalisierung in der API-Payload übergeben.
   * Sie möchten den E-Mail-Kanal verwenden.

## Setup-Richtlinien

Gehen Sie wie folgt vor, um Kampagnen mit hohem Durchsatz korrekt zu konfigurieren:

1. Erstellen Sie einen neuen IP-Pool. [Erfahren Sie, wie Sie IP-Pools erstellen](../configuration/ip-pools.md)
1. Erstellen Sie eine neue Kanalkonfiguration. [Informationen zum Einrichten von Kanalkonfigurationen](../configuration/channel-surfaces.md)
1. Wenden Sie sich an die Adobe-Kundenunterstützung, um die aktivierte Oberfläche anzufordern, die der Funktion für hohen Durchsatz zugeordnet werden soll. Geben Sie die Kanalkonfiguration und Details zum IP-Pool zusammen mit Ihrer Organisations-ID an.

>[!IMPORTANT]
>
>Die IP-Pool- und Kanalkonfigurationen, die für Transaktionsnachrichten mit hohem Durchsatz vorgesehen sind, dürfen ausschließlich für diesen Zweck verwendet werden und nicht mit standardmäßigen Transaktionsnachrichten, bei denen API-ausgelöste Kampagnen oder Journey verwendet werden.
