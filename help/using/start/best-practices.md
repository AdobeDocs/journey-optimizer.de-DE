---
solution: Journey Optimizer
product: journey optimizer
title: Best Practices für Journey Optimizer
description: Weitere Informationen zu Best Practices für Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 5b69e8d8539e37f42d44383e32b85e651e412937
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 5%

---

# Best Practices {#best-practices}

## Anleitung zur Personalisierung von Echtzeit-Anwendungsfällen und Omnichannel {#real-time-guidance}

Nach der Aktualisierung von Identity Service 2.0 hat sich die Echtzeit-Identitätszuordnung entwickelt.

Adobe Journey Optimizer nutzt den Identitätsdienst, um Profile zusammenzuführen und Erlebnisse für den Benutzer zu personalisieren. Daher gibt es einige wichtige Aspekte für den Dienst, die Sie beim Erstellen Ihrer Anwendungsfälle beachten müssen. Als Marke möchten Sie einer Person ein Erlebnis bereitstellen. Das Identitätsdiagramm ermöglicht es Marketing-Experten zu verstehen, mit welchen Geräten eine Person über verschiedene Kanäle hinweg verbunden ist. Das Diagramm kann Identitäten enthalten, die eine Person (CRMID) oder einen Webbrowser (ECID) repräsentieren. Der Identitätsdienst verknüpft diese Informationen miteinander, was die Erstellung einer 360-Grad-Ansicht einer Person oder eines zusammengeführten Profils ermöglicht. Das bedeutet, wenn jemand Ihre Site besucht und sich dann anmeldet, können alle vorherigen Daten aus dieser Sitzung mit dem Anmeldenutzer verknüpft werden. Diese Aktion erfolgt in einigen verschiedenen Schritten:

1. Erstmalige Zuordnung von Identitäten - Wenn sich eine Person anmeldet, wird die Anmelde-ID (CRMID) mit der Webbrowser-Kennung (Web- oder mobile App-Sitzung) verknüpft:

   * Dies kann 30 bis 4 Stunden dauern.
   * Normalerweise generiert dieses Anmeldeereignis ein Identitätsdiagramm, das CRMID mit ECID verknüpft.

1. Nach der ersten Zuordnung werden alle Daten, die mit einer der beiden Identitäten gesendet werden, mit dem zusammengeführten Profil verknüpft und in Journey Optimizer zur Personalisierung in Echtzeit verfügbar gemacht. Die Aktualisierung des Profils mit den neuesten Verhaltensdaten kann bis zu 1 Minute dauern. Mehr dazu erfahren Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=de).

Beachten Sie beim Erstellen von Anwendungsfällen Folgendes:

1. Die Marke möchte 30 Minuten nach dem Abbruch (z. B. E-Mail zum Verlassen des Warenkorbs):

   Verwenden Sie die Identität mit den Daten - ECID. Wenn Sie 100 % der Besucher erfassen möchten, die ihre E-Mail-Adresse/App-Installation innerhalb der letzten 30 Minuten gesendet haben, sollten Sie die Cookie-basierte Identität verwenden, um diese Journey (ECID) zu starten. Dabei wird davon ausgegangen, dass Ihre E-Mail-Adresse, Ihr Push-Token oder eine andere Adresse für das Erlebnis mit der ECID verknüpft ist.

1. Omnichannel-Interaktion im Web, E-Mail, Push usw.:

   * Sie müssen zum Zeitpunkt der Interaktion über die Adresse für die Kommunikation im Profil verfügen. Um sicherzustellen, dass dies konsistent und zeitnah geschieht, stellen Sie sicher, dass Ihre Daten mit der Identität verknüpft sind, die Sie verwenden möchten.
   * Wenn Sie Informationen aus einer neu installierten App oder Browser-Sitzung zusammen mit bekannten oder angemeldeten Informationen verwenden müssen, muss diese Nachricht gesendet werden, nachdem diese Identitäten zugeordnet wurden. Dies kann je nach Kunde variieren. Wir empfehlen, mindestens 30 Minuten zu warten, um die höchste Profilmenge zu erhalten.

## Skalierung mit Journey-Limits {#scale}

In diesem Abschnitt erfahren Sie, wie Sie die Skalierung mit den folgenden beiden Einschränkungen durchführen:

* Journey Optimizer verfügt über einen Schutzmechanismus von 50 Aktivitäten in einer Journey-Arbeitsfläche. Diese Limits sollen Lesbarkeit, Qualitätssicherung und Fehlerbehebung unterstützen. Die Anzahl der Aktivitäten in einer Journey wird im oberen linken Bereich der Journey-Arbeitsfläche angezeigt, wenn Sie innerhalb von 10 Aktivitäten dieser Grenze liegen.

* Bei der Veröffentlichung von Journey werden die Werte von Journey Optimizer automatisch skaliert und angepasst, um einen maximalen Durchsatz und eine maximale Stabilität zu gewährleisten. Wenn Sie sich in der Nähe des Meilensteins von 100 lebenden Journey gleichzeitig in einer Sandbox befinden, werden in der Benutzeroberfläche ein orangefarbenes Overlay und Warnzeichen zu diesem Ergebnis angezeigt. Wenn Sie diese Benachrichtigung sehen, aber die Notwendigkeit besteht, Ihre Journey über 100 Live-Journeys hinaus zu erweitern, erstellen Sie bitte ein Ticket für die Kundenunterstützung, und wir helfen Ihnen bei der Erreichung Ihrer Ziele.

Es gibt eine Reihe von Best Practices, die Sie anwenden können, um innerhalb der Limits zu bleiben und das System effizient zu nutzen.

* Wenn Sie sich Ihrer Livegrenze von Journey nähern, können Sie als ersten Schritt zum **Übersicht** Registerkarte unter **Journey** um zu sehen, wie viele Journey in den letzten 24 Stunden aktiv waren (Journey mit aktiven Profilen). In diesem Abschnitt können Sie die Anzahl der Profile überprüfen, die die Journey starten und beenden, um dies zu ermitteln.

  ![](assets/journey-guardrails2.png)

* Als Nächstes können Sie im Abschnitt Journey-Inventar alle Journey nach Status = &quot;Live&quot;und Typ = &quot;Audience lesen&quot;filtern. Sortieren Sie dann nach Veröffentlichungsdatum (alt bis neu). Klicken Sie in die Journey und gehen Sie zum Zeitplan. Beenden Sie alle Live-Journey mit einem Zeitplan für die Ausführung **Einmal** oder **So bald wie möglich** die älter als einen Tag sind und nur eine Aktion haben.

  ![](assets/journey-guardrails1.png)

* Wenn **Audience lesen** Journey hat nur eine Aktion, keine Wartezeiten/Entscheidungen oder Sendezeitoptimierung, erwägen Sie, sie in Journey Optimizer-Kampagnen zu verschieben. Kampagnen eignen sich besser für die Interaktion in einem Schritt. Einer der Hauptunterschiede zwischen Campaign und Journey besteht darin, ob Sie es für wichtig halten, die Benutzerinteraktion aktiv zu überwachen, um den nächsten Schritt zu bestimmen und eine andere Aktion durchzuführen.
* Um die Anzahl der Aktivitäten innerhalb einer Journey zu verringern, überprüfen Sie die Bedingungsschritte. Es gibt viele Fälle, in denen Sie die Bedingungen in die Segmentdefinition oder die Zielgruppenzusammensetzung verschieben können.
* Wenn dieselben Bedingungen über mehrere Journey hinweg wiederholt werden (Einverständnisprüfungen, Unterdrückungen), sollten Sie erwägen, sie als Teil der Segmentdefinition zu verschieben. Wenn Sie beispielsweise die Bedingung haben, dass die E-Mail-Adresse nicht leer ist, in mehreren Journey zu überprüfen, müssen Sie diese Bedingung als Teil der Segmentdefinition einbeziehen.
* Wenn Ihre Journey mehrere Bedingungen hat, die die Zielgruppe aufteilen, um die Zahlen in jedem Schritt zu sehen, sollten Sie Customer Journey Analytics oder eine andere Berichterstellungslösung in Erwägung ziehen, die für die Analyse besser geeignet ist.
* Wenn Sie sich der Grenze der Knoten auf der Arbeitsfläche nähern, sollten Sie die Konsolidierung von Aktionen mit dynamischen Parametern oder Inhalten erwägen, um den richtigen Inhalt anstelle expliziter Knoten bereitzustellen.



