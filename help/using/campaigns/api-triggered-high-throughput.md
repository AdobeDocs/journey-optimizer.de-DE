---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 61%

---
Die Datei existiert nicht im Pipeline-Repository - es ist eine Dokumentationsdatei, die als Kontext bereitgestellt wird. Ich schreibe den kompletten aktualisierten Markdown direkt wie angewiesen (Ausgabe nur die Datei, keine Erklärungen).

---

Lösung: Journey Optimizer
Produkt: Journey Optimizer
Titel: Aktivieren des Modus „Hoher Durchsatz“ für API-ausgelöste Kampagnen
Beschreibung: Erfahren Sie, wie Sie den Modus „Hoher Durchsatz“ für API-ausgelöste Kampagnen aktivieren.
Funktion: Kampagnen, API
Thema: Content-Management
Rolle: Entwickler
Stufe: Erfahren
Schlüsselwörter: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
EXL-ID: 2B3E87DC-097A-4D05-873C-F421D11338C3
TQID: https://experienceleague.adobe.com/SwmK1epuhZUf4EWnaLRHTBH-eE1hEV02Z8nqXGtMb6U
product_v2:
- Kennung: CB954087-F4FC-4456-AFB9-E939CABCDC79
internal-label: Journey Optimizer
feature_v2:
- ID: D556B755-390A-43F0-BE32-A08CF6236126
internal-label: Konfiguration
- Kennung: A653CC2E-BC85-4353-A306-399E5B247978
internal-label: Journey Optimizer-Kampagnen
subfeature_v2:
- ID: F7479FA1-474B-479D-8C98-F6CEE5865A38
internal-label: API-ausgelöste Kampagnen
- Kennung: EE67BD4A-25EE-4CDD-9EAB-0D7549FDE0C6
internal-label: Kampagnenverwaltung
role_v2:
- ID: ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label: Entwickler
topic_v2:
- ID: E0EB8757-182F-49F3-94A4-1587D16F5094
internal-label: Personalization
---
# Aktivieren des Modus mit hohem Durchsatz für durch API ausgelöste Kampagnen {#high-throughput}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Aktivieren Sie den Modus „Hoher Durchsatz“ für API-ausgelöste Kampagnen, damit Sie sehr umfangreiche Echtzeit-Transaktionsnachrichten mit bis zu 5.000 Transaktionen pro Sekunde (E-Mail) oder bis zu 1.500 Transaktionen pro Sekunde (Push-Benachrichtigung) senden können, ohne auf Profile angewiesen zu sein.

>[!ENDSHADEBOX]

Der Modus „Hoher Durchsatz“ wurde für Unternehmen entwickelt **die (sehr umfangreiches Echtzeit-Transaktionsnachrichten** benötigen. Im Gegensatz zu regulären durch API ausgelösten Kampagnen werden Kampagnen mit hohem Durchsatz unabhängig von Adobe-Profilen ausgeführt und erfordern ein anderes Konfigurationsmodell.

Auf dieser Seite werden der Unterschied zwischen Kampagnen mit hohem Durchsatz und standardmäßigen durch API ausgelösten Kampagnen, die Einrichtungsanforderungen und die Gründe für die Auswahl eines Modus erläutert.

## Leitlinien und Einschränkungen

* **Zugriff**: Nur in der US-Region für Organisationen verfügbar, die mit dem Add-on für Transaktions-Messaging mit hohem Durchsatz lizenziert sind.

* **Kanäle**: Verfügbar für E-Mail- und Push-Benachrichtigungen.

* **Durchsatz**:

   * **E** Mail: Bis zu 5000 Transaktionen pro Sekunde.
   * **Push** - Bis zu 1500 Transaktionen pro Sekunde. Die folgenden mehrstufigen Durchsatzstufen sind verfügbar: 500 TPS (Basis), 1000 TPS und 1500 TPS. Höhere Ebenen erfordern die entsprechende Add-on-Berechtigung.

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
   * **Elebnisereignis-Datensatz zum AJO-E-Mail-Tracking – Kein Profil**

* **Durchsatzzuordnung**: Der Durchsatz, der im Add-on „Hoher Durchsatz“ bereitgestellt wird, ist ausschließlich für Kampagnen mit hohem Durchsatz reserviert. Es gibt keine Aufteilung des Durchsatzes zwischen durch API ausgelösten Kampagnen mit standardmäßigem und hohem Durchsatz.

## Auswahl zwischen standardmäßigen Kampagnen und Kampagnen mit hohem Durchsatz

Verwenden Sie diese Tabelle, um zu entscheiden, welcher Typ einer durch API ausgelösten Kampagne zu Ihrem Anwendungsfall passt:

| Funktion/Anforderung | Standardmäßige durch API ausgelöste Kampagne | Kampagne mit hohem Durchsatz |
|------------------------|---------------------------------|---------------------------|
| **Verfügbarkeit** | Im Basisangebot enthalten | Erfordert das Add-on für Transaktions-Messaging mit hohem Durchsatz. |
| **Durchsatz** | Bis zu 500 Transaktionen pro Sekunde | Bis zu 5.000 TPS (E-Mail); bis zu 1.500 TPS (Push-Benachrichtigung) |
| **Kanäle** | E-Mail, SMS, Push | E-Mail, Push |
| **Personalisierung** | Profil + Kontext in der API-Payload | Nur Kontext in der API-Payload |
| **Profil und Zuordnung** | Ist vorhanden oder wird mit Ereignissen erstellt, die einem Profil zugeordnet sind | Kein Profil |
| **Nachrichtenvolumen** | Standardberechtigungen und Nachrichtenpakete | Separate abgestufte Nachrichtenvolumen |
| **Infrastruktur** | Standard | Erweitert |
| **Betriebszeit** | 99,9 % | 99,99 % |
| **Konsistenzprüfungs-API** | Ja | Ja |

Mit anderen Worten:

* Gründe für die Auswahl von **standardmäßigen durch API ausgelösten** Kampagnen:
   * Es ist vertraglich kein hoher Durchsatz festgelegt.
   * Ihr Durchsatzbedarf beträgt ≤ 500 TPS.
   * Sie benötigen Personalisierung basierend auf Adobe-Profilen.
   * Kampagnendaten sollen für zukünftiges Targeting Profilen zugeordnet werden.
   * Sie benötigen SMS-Nachrichten.

* Gründe für die Auswahl von Kampagnen mit **hohem Durchsatz**:
   * Sie benötigen einen Durchsatz von >500 TPS.
   * Sie benötigen keine Profilzuordnung.
   * Sie können die gesamte Personalisierung in der API-Payload übergeben.
   * Sie möchten den E-Mail- oder Push-Kanal verwenden.

## Einrichtungsrichtlinien

Gehen Sie wie folgt vor, um Kampagnen mit hohem Durchsatz korrekt zu konfigurieren:

1. **Nur für E-Mails mit hohem Durchsatz** - Erstellen eines neuen IP-Pools. [Informationen zum Erstellen von IP-Pools](../configuration/ip-pools.md)
1. Erstellen Sie eine Kanalkonfiguration. [Informationen zum Einrichten von Kanalkonfigurationen](../configuration/channel-surfaces.md)
1. Wenden Sie sich an die Adobe-Kundenunterstützung, um die aktivierte Oberfläche anzufordern, die der Funktion für hohen Durchsatz zugeordnet werden soll. Geben Sie die Kanalkonfiguration und Details zum IP-Pool (für E-Mails) zusammen mit Ihrer Organisations-ID an.

>[!IMPORTANT]
>
>Die Kanalkonfigurationen, die für Transaktionsnachrichten mit hohem Durchsatz vorgesehen sind, dürfen ausschließlich für diesen Zweck verwendet werden und nicht mit standardmäßigen Transaktionsnachrichten, die API-ausgelöste Kampagnen oder Journey verwenden. Für E-Mails mit hohem Durchsatz muss der dafür vorgesehene IP-Pool ebenfalls ausschließlich für den Versand mit hohem Durchsatz verwendet werden.