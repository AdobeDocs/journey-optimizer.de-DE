---
solution: Journey Optimizer
product: journey optimizer
title: Überprüfen und Aktivieren einer Kampagne
description: Überprüfen und Aktivieren von Kampagnen in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: Kampagne, Überprüfung, Validierung, Aktivierung, Aktivieren, Optimizer
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: 8cb37cf0fb9dc8048d7da8ddda0c67280477d57f
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 46%

---


# Ausführen einer Kampagne, die durch API ausgelöst wird {#execute}

Nachdem Ihre Kampagne aktiviert wurde, müssen Sie die generierte Beispiel-cURL-Anfrage abrufen und im API verwenden, um Ihre Payload zu erstellen und die Kampagne auszulösen.

## Wichtige Informationen {#must-read}

* **Start- und Enddatum einer Kampagne** – Wenn Sie bei der Erstellung der Kampagne ein bestimmtes Start- und/oder Enddatum konfiguriert haben, wird die Kampagne außerhalb dieses Zeitraums nicht ausgeführt und API-Aufrufe schlagen fehl.

* **Aufrufzeitüberschreitung** – Der Aufruf der REST-API zur Ausführung interaktiver Nachrichten hat einen Zeitüberschreitungswert von 60 Sekunden. Im Falle unerwarteter Zeitüberschreitungen gibt es jedoch interne erneute Zustellversuche, um den Versand zu gewährleisten.

## Auslösen der Kampagne {#trigger}

1. Öffnen Sie die Kampagne, kopieren Sie dann die Payload-Anfrage aus dem Abschnitt **[!UICONTROL cURL-Anfrage]** und fügen Sie diese ein. Diese Payload enthält nun alle Personalisierungsvariablen (Profil und Kontext), die in der Nachricht verwendet werden. Sie ist verfügbar, sobald die Kampagne aktiv ist.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >Die Endpunkte im cURL-Abschnitt unterscheiden sich zwischen standardmäßigen Kampagnen und [Kampagnen mit hohem Durchsatz](../campaigns/api-triggered-high-throughput.md).

1. Verwenden Sie diese cURL-Anfrage in den APIs, um Ihre Payload zu erstellen und die Kampagne auszulösen. Weitere Informationen finden Sie in der [Dokumentation zur Interactive Message Execution-API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution), wo alle Endpunkte für standardmäßige Kampagnen und Kampagnen mit hohem Durchsatz aufgelistet sind.

   Beispiele für API-Aufrufe finden Sie auch auf [dieser Seite](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

## Fehlerbehebung {#troubleshooting}

### Azure Cosmos DB-Authentifizierungsfehler (500 interner Server-Fehler) {#cosmosdb-auth-errors}

Wenn beim Auslösen von API-ausgelösten Kampagnen **500 interne Server** Fehler auftreten und die Systemprotokolle einen **403 Forbidden**-Fehler von Azure Cosmos DB mit einer Meldung wie der folgenden zeigen:

_„Der Zugriff auf Ihr Konto ist derzeit widerrufen, da der Azure Cosmos DB-Service das AAD-Authentifizierungstoken für die Standardidentität des Kontos nicht abrufen kann“_

Dieser Fehler tritt normalerweise auf, wenn der für die Cosmos-DB-Authentifizierung erforderliche Azure-Service-Prinzipal deaktiviert, gelöscht oder falsch konfiguriert wurde.

+++Wie dieses Problem behoben wird

1. **Azure-Service-Prinzipal überprüfen** - Stellen Sie sicher, dass Ihr Azure-Service-Prinzipal oder Ihre verwaltete Identität aktiviert ist und in Ihrem Azure Active Directory nicht deaktiviert oder gelöscht wurde.

1. **Berechtigungen überprüfen** - Vergewissern Sie sich, dass der Service-Prinzipal über die erforderlichen Berechtigungen für den Zugriff auf die Azure-Schlüsseltresor- und Cosmos-DB-Ressourcen verfügt. Der Service-Prinzipal muss über geeignete Rollenzuweisungen verfügen, um sich bei Azure Cosmos DB zu authentifizieren.

1. **Überprüfen Sie die Konfiguration von Azure Cosmos DB CMK** - Wenn Sie kundenverwaltete Schlüssel (CMK) verwenden, finden Sie im [Handbuch zur Fehlerbehebung bei Azure Cosmos DB CMK](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"} detaillierte Schritte zur Wiederherstellung der AAD-Token-Akquise.

1. **Erneutes Aktivieren und Testen** - Nach der Korrektur der Konfiguration müssen Sie den Service-Prinzipal erneut aktivieren, falls er deaktiviert war, und Ihre Transaktions-Campaign-API-Aufrufe erneut testen, um zu bestätigen, dass die Authentifizierung erfolgreich war und Nachrichten gesendet werden.

>[!NOTE]
>
>Dieses Problem tritt normalerweise aufgrund einer Fehlkonfiguration oder einer versehentlichen Deaktivierung des Azure-Service-Prinzipals auf, der für die Cosmos DB-Authentifizierung erforderlich ist. Wenn der Service-Prinzipal aktiviert und ordnungsgemäß konfiguriert bleibt, wird dieser Fehler in Zukunft verhindert.

+++
