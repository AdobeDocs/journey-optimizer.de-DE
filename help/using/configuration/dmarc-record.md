---
solution: Journey Optimizer
product: journey optimizer
title: DMARC-Eintrag
description: Erfahren Sie, wie Sie DMARC-Datensätze in Journey Optimizer festlegen.
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Domäne, E-Mail, Dmarc, Datensatz
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# DMARC-Eintrag {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Festlegen des DMARC-Datensatzes"
>abstract="DMARC-Datensatz einrichten, um Zustellbarkeitsprobleme mit ISPs zu vermeiden"

>[!CAUTION]
>
>Nach den jüngsten Ankündigungen von Gmail und Yahoo für Massen-Absender unterstützt Journey Optimizer jetzt die DMARC-Authentifizierungstechnologie. //Sie müssen alle bereits in Ihrer Instanz erstellten Subdomains aktualisieren, um DMARC-Unterstützung einzuschließen.//

Es ist wichtig, es bis zum 1. Februar Doc wird bald kommen

Starten am

Sie haben zwei Optionen:

* Führen Sie das sofort selbst durch: Richten Sie es bei Ihrer IT-Abteilung ein - wann immer Sie möchten

* Tun Sie es in AJO - in diesem Fall müssen Sie jedoch bis zum 30. Januar warten

   * Vollständige Zuweisung: Sie können dies am 30. Januar (AJO-Version) tun.

   * CNAME plant es mit Ihrer IT-Abteilung, damit es nicht zeitaufwendig ist, aber Sie es planen müssen

Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo, dass Sie über einen DMARC-Datensatz für jede Domäne verfügen, mit der Sie E-Mails an sie senden. Diese neue Anforderung beginnt am **1. Februar 2024**.

Erfahren Sie mehr über die Anforderungen von Google und Yahoo an DMARC-Einträge in [diesem Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Erfahren Sie mehr über die angekündigten Änderungen in Google und Yahoo unter [diese Seite](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC, das für **Domänenbasierte Nachrichtenauthentifizierung, Berichterstellung und Konformität**, ist ein E-Mail-Authentifizierungsprotokoll, das den Schutz vor E-Mail-Spoofing, Phishing und anderen betrügerischen Aktivitäten bietet.

* Email authentication:

   * SPF (Sender Policy Framework): DMARC verlässt sich bei der Authentifizierung der Identität des E-Mail-Servers auf SPF. SPF hilft bei der Überprüfung, ob die E-Mail-Nachricht von einer autorisierten Quelle stammt, indem die IP-Adresse des sendenden Servers mit einer Liste autorisierter IP-Adressen für die Domäne verglichen wird.
   * DKIM (DomainKeys Identified Mail): DMARC verwendet DKIM auch zum Hinzufügen einer digitalen Signatur zu E-Mail-Nachrichten, sodass der Empfänger die Integrität und Authentizität der Nachricht überprüfen kann.

* DMARC verhindert, dass böswillige Akteure E-Mails senden, die scheinbar von Ihrer Domain stammen. Durch die Einrichtung von DMARC können Sie festlegen, wie E-Mail-Anbieter mit Nachrichten umgehen sollen, die bei Authentifizierungsprüfungen fehlschlagen, was die Wahrscheinlichkeit verringert, dass Empfänger durch Phishing-E-Mails erreicht werden.

* DMARC verbessert die Zustellbarkeit von E-Mails, indem E-Mail-Anbietern klare Richtlinien an die Hand gegeben werden, die sie befolgen müssen, wenn sie auf Nachrichten stoßen, die angeblich aus Ihrer Domain stammen. Dadurch kann sich die Wahrscheinlichkeit verringern, dass E-Mails als Spam gekennzeichnet oder abgelehnt werden.

* Durch die Implementierung von DMARC können Sie die Reputation Ihrer Marke schützen, indem Sie sicherstellen, dass nicht autorisierte Parteien Ihre Domain nicht für Phishing- oder andere schädliche Aktivitäten missbrauchen können. Dies ist besonders wichtig für Unternehmen und Organisationen, die auf die E-Mail-Kommunikation mit Kunden und Partnern angewiesen sind.

Das Einrichten eines DMARC-Eintrags umfasst das Hinzufügen eines DNS-TXT-Eintrags zu den DNS-Einstellungen Ihrer Domain. Dieser Datensatz gibt Ihre DMARC-Richtlinie an, z. B. ob Nachrichten, bei denen die Authentifizierung fehlschlägt, unter Quarantäne gestellt oder abgelehnt werden. Die Implementierung von DMARC ist ein proaktiver Schritt zur Verbesserung der E-Mail-Sicherheit und zum Schutz sowohl Ihrer Organisation als auch Ihrer Empfänger vor E-Mail-basierten Bedrohungen.

[Weitere Informationen zu DMARC finden Sie im Best Practices-Handbuch zur Zustellbarkeit .](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=de){target="_blank"} , um die Auswirkungen von DMARC auf die E-Mail-Zustellbarkeit besser zu verstehen.

Wenn Sie DMARC nicht hinzufügen, werden Sie (zumindest) unter Quarantäne gestellt.

Stellen Sie bitte sicher, dass Sie einen echten Posteingang haben, in dem Sie die Kontrolle erhalten können - Sie verwalten diesen Posteingang (sollte kein Adobe-Posteingang sein).

Empfehlung ist 24, weil im Allgemeinen, wenn weniger, bewerten Sie Ihre Kapazität / überprüfen Sie Ihre > Chat GPT.

Google und Yahoo und wahrscheinlich alle anderen wichtigen ISPs

für CNAME im Bearbeitungsfluss müssen Sie die CSV-Datei erneut herunterladen (nicht für vollständig delegierte Dateien)

neuer DMARC-Datensatz

In RN > setzen Sie es an die erste Stelle Alle Subdomains müssen mit DMARC-Unterstützung aktualisiert werden



