---
solution: Journey Optimizer
product: journey optimizer
title: Aktivieren des Modus mit hohem Durchsatz für durch API ausgelöste Kampagnen
description: Erfahren Sie, wie Sie den Modus mit hohem Durchsatz für durch API ausgelöste Kampagnen aktivieren.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
source-git-commit: 81e54a3e3428d58818805b5dcb397ede4039436a
workflow-type: ht
source-wordcount: '622'
ht-degree: 100%

---


# Aktivieren des Modus mit hohem Durchsatz für durch API ausgelöste Kampagnen {#high-throughput}

Der Modus mit hohem Durchsatz wurde für Unternehmen entwickelt, die **sehr umfangreiches Echtzeit-Transaktions-Messaging** (bis zu 5.000 Transaktionen pro Sekunde) benötigen. Im Gegensatz zu regulären durch API ausgelösten Kampagnen werden Kampagnen mit hohem Durchsatz unabhängig von Adobe-Profilen ausgeführt und erfordern ein anderes Konfigurationsmodell.

Auf dieser Seite werden der Unterschied zwischen Kampagnen mit hohem Durchsatz und standardmäßigen durch API ausgelösten Kampagnen, die Einrichtungsanforderungen und die Gründe für die Auswahl eines Modus erläutert.

## Leitlinien und Einschränkungen

* **Zugriff**: Nur in der US-Region für Organisationen verfügbar, die mit dem Add-on für Transaktions-Messaging mit hohem Durchsatz lizenziert sind.

* **Kanäle**: Derzeit nur für E-Mails verfügbar.

* **Personalisierung**:

   * Die gesamte Personalisierung muss als **kontextuelle Daten** in der API-Payload enthalten sein. [Informationen zum Personalisieren von Inhalten mit kontextuellen Daten](../campaigns/api-triggered-campaign-content.md#contextual)
   * Profilbasierte Personalisierung wird nicht unterstützt. Wenn Profilvariablen verwendet werden, treten Validierungsfehler auf.

* **Personalisierte Kanalkonfigurationen**: Kanalkonfigurationen, die eine [profilbasierte Personalisierung](../email/surface-personalization.md) verwenden, können nicht mit Kampagnen mit hohem Durchsatz verwendet werden. Es können nur Oberflächen ohne Profilpersonalisierung verwendet werden.

* **API-Endpunkt**: Kampagnen mit hohem Durchsatz verwenden einen anderen Endpunkt als standardmäßige durch API ausgelöste Kampagnen. Weitere Informationen finden Sie unter [Ausführen einer durch API ausgelösten Kampagne](../campaigns/trigger-campaigns.md#trigger).

* **Kampagnenexklusivität**: Kampagnen mit hohem Durchsatz verwenden keine Adobe-Profile. Nachrichten werden unabhängig davon versendet, ob ein Profil vorhanden ist oder nicht.

  Darüber hinaus kann eine Kampagne nicht sowohl für Anwendungsfälle mit aktiviertem Profil als auch für Anwendungsfälle ohne Profil verwendet werden. Wenn Sie beides benötigen, erstellen Sie zwei separate Kampagnen und stellen Sie sicher, dass das aufrufende System anhand des Kontexts entscheidet, welche Kampagne ausgelöst werden soll.

* **Datensätze für Feedback und Tracking**: Feedback- und Tracking-Daten für Kampagnen mit hohem Durchsatz werden in entsprechenden Datensätzen gespeichert, die nicht für Profile aktiviert sind. Daher werden diese Ereignisse nicht mit Profilen verknüpft, selbst wenn ein passendes Profil vorhanden ist.

  Die verwendeten Datensätze sind:

   * **Ereignisdatensatz zu AJO-Nachrichten-Feedback – Kein Profil**
   * **Ereignisdatensatz zu Erfahrungen beim AJO-E-Mail-Tracking – Kein Profil**

* **Durchsatzzuordnung**: Der Durchsatz, der im Add-on „Hoher Durchsatz“ bereitgestellt wird, ist ausschließlich für Kampagnen mit hohem Durchsatz reserviert. Es gibt keine Aufteilung des Durchsatzes zwischen durch API ausgelösten Kampagnen mit standardmäßigem und hohem Durchsatz.

## Auswahl zwischen standardmäßigen Kampagnen und Kampagnen mit hohem Durchsatz

Verwenden Sie diese Tabelle, um zu entscheiden, welcher Typ einer durch API ausgelösten Kampagne zu Ihrem Anwendungsfall passt:

| Funktion/Anforderung | Standardmäßige durch API ausgelöste Kampagne | Kampagne mit hohem Durchsatz |
|------------------------|---------------------------------|---------------------------|
| **Verfügbarkeit** | Im Basisangebot enthalten | Erfordert das Add-on für Transaktions-Messaging mit hohem Durchsatz. |
| **Durchsatz** | Bis zu 500 Transaktionen pro Sekunde | Bis zu 5.000 Transaktionen pro Sekunde |
| **Kanäle** | E-Mail, SMS, Push | E-Mail |
| **Personalisierung** | Profil + Kontext in der API-Payload | Nur Kontext in der API-Payload |
| **Profil und Zuordnung** | Ist vorhanden oder wird mit Ereignissen erstellt, die einem Profil zugeordnet sind | Kein Profil |
| **Nachrichtenvolumen** | Standardberechtigungen und Nachrichtenpakete | Separate abgestufte Nachrichtenvolumen |
| **Infrastruktur** | Standard | Erweitert |
| **Betriebszeit** | 99,9 % | 99,99 % |
| **Konsistenzprüfungs-API** | Ja | Ja |

Mit anderen Worten:

* Gründe für die Auswahl von **standardmäßigen durch API ausgelösten** Kampagnen:
   * Es ist vertraglich kein hoher Durchsatz festgelegt.
   * Ihre Anforderungen an den Durchsatz betragen &lt;500 TPS.
   * Sie benötigen Personalisierung basierend auf Adobe-Profilen.
   * Kampagnendaten sollen für zukünftiges Targeting Profilen zugeordnet werden.
   * Sie möchten einen anderen Kanal als E-Mail verwenden.

* Gründe für die Auswahl von Kampagnen mit **hohem Durchsatz**:
   * Sie benötigen einen Durchsatz von >500 TPS.
   * Sie benötigen keine Profilzuordnung.
   * Sie können die gesamte Personalisierung in der API-Payload übergeben.
   * Sie möchten den E-Mail-Kanal verwenden.

## Einrichtungsrichtlinien

Gehen Sie wie folgt vor, um Kampagnen mit hohem Durchsatz korrekt zu konfigurieren:

1. Erstellen Sie einen neuen IP-Pool. [Informationen zum Erstellen von IP-Pools](../configuration/ip-pools.md)
1. Erstellen Sie eine Kanalkonfiguration. [Informationen zum Einrichten von Kanalkonfigurationen](../configuration/channel-surfaces.md)
1. Wenden Sie sich an die Adobe-Kundenunterstützung, um die aktivierte Oberfläche anzufordern, die der Funktion für hohen Durchsatz zugeordnet werden soll. Geben Sie die Kanalkonfiguration und Details zum IP-Pool zusammen mit Ihrer Organisations-ID an.

>[!IMPORTANT]
>
>Die IP-Pool- und Kanalkonfigurationen, die für Transaktionsnachrichten mit hohem Durchsatz vorgesehen sind, dürfen ausschließlich für diesen Zweck verwendet werden. Sie dürfen nicht für standardmäßiges Transaktions-Messaging mit durch API ausgelösten Kampagnen oder Journeys verwendet werden.
