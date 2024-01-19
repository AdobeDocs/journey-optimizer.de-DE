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
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 1%

---

# DMARC-Eintrag {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Festlegen des DMARC-Datensatzes"
>abstract="Legen Sie DMARC-Datensatz fest, um Zustellbarkeitsprobleme mit ISPs zu vermeiden. Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo, dass Sie über einen DMARC-Datensatz für jede Domäne verfügen, mit der Sie E-Mails an sie senden."

>[!CAUTION]
>
>Nach den jüngsten Ankündigungen von Gmail und Yahoo für Massen-Absender unterstützt Journey Optimizer jetzt die DMARC-Authentifizierungstechnologie.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo von Ihnen, dass Sie über eine **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails verwenden. Diese neue Anforderung beginnt am **1. Februar 2024**.

Erfahren Sie mehr über die Anforderungen von Google und Yahoo in [diesem Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Wenn diese neue Anforderung von Gmail und Yahoo nicht erfüllt wird, wird erwartet, dass E-Mails in den Spam-Ordner gelangen oder blockiert werden.

Daher empfiehlt Adobe dringend, sicherzustellen, dass Sie DMARC-Datensätze für alle Subdomains eingerichtet haben, die Sie zum Adobe in [!DNL Journey Optimizer]. Führen Sie eine der beiden folgenden Optionen aus:

* Richten Sie DMARC in Ihren Subdomains oder in der übergeordneten Domäne Ihrer Subdomains ein. **in Ihrer Hosting-Lösung**.

* Richten Sie DMARC auf Ihren zugewiesenen Subdomains ein **mit der neuen Funktion in der [!DNL Journey Optimizer] Administration-Benutzeroberfläche** - ohne zusätzliche Arbeit an Ihrer Hosting-Lösung. [Weitere Informationen](#implement-dmarc)

  >[!CAUTION]
  >
  >Wenn Sie [CNAME-Zuweisung](delegate-subdomain.md#cname-subdomain-delegation) Für Ihre sendenden Subdomains ist auch ein Eintrag in Ihre Hosting-Lösung erforderlich. Stellen Sie sicher, dass Sie sich mit Ihrer IT-Abteilung abstimmen, damit diese die Aktualisierung so bald wie möglich durchführen kann [!DNL Journey Optimizer] ist verfügbar (am 30. Januar 2024). <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>Erfahren Sie mehr über die Implementierung von DMARC im [Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} , um die Auswirkungen auf die Zustellbarkeit von E-Mails besser zu verstehen.

## Was ist DMARC?

DMARC, das für **Domänenbasierte Nachrichtenauthentifizierung, Berichterstellung und Konformität**, ist ein E-Mail-Authentifizierungsprotokoll, das den Schutz vor E-Mail-Spoofing, Phishing und anderen betrügerischen Aktivitäten bietet.

* Email authentication:

   * SPF (Sender Policy Framework): DMARC verlässt sich bei der Authentifizierung der Identität des E-Mail-Servers auf SPF. SPF hilft bei der Überprüfung, ob die E-Mail-Nachricht von einer autorisierten Quelle stammt, indem die IP-Adresse des sendenden Servers mit einer Liste autorisierter IP-Adressen für die Domäne verglichen wird.
   * DKIM (DomainKeys Identified Mail): DMARC verwendet DKIM auch zum Hinzufügen einer digitalen Signatur zu E-Mail-Nachrichten, sodass der Empfänger die Integrität und Authentizität der Nachricht überprüfen kann.

* DMARC verhindert, dass böswillige Akteure E-Mails senden, die scheinbar von Ihrer Domain stammen. Durch die Einrichtung von DMARC können Sie festlegen, wie E-Mail-Anbieter mit Nachrichten umgehen sollen, die bei Authentifizierungsprüfungen fehlschlagen, was die Wahrscheinlichkeit verringert, dass Empfänger durch Phishing-E-Mails erreicht werden.

* DMARC verbessert die Zustellbarkeit von E-Mails, indem E-Mail-Anbietern klare Richtlinien an die Hand gegeben werden, die sie befolgen müssen, wenn sie auf Nachrichten stoßen, die angeblich aus Ihrer Domain stammen. Dadurch kann sich die Wahrscheinlichkeit verringern, dass E-Mails als Spam gekennzeichnet oder abgelehnt werden.

* Durch die Implementierung von DMARC können Sie die Reputation Ihrer Marke schützen, indem Sie sicherstellen, dass nicht autorisierte Parteien Ihre Domain nicht für Phishing- oder andere schädliche Aktivitäten missbrauchen können. Dies ist besonders wichtig für Unternehmen und Organisationen, die auf die E-Mail-Kommunikation mit Kunden und Partnern angewiesen sind.

Das Einrichten eines DMARC-Eintrags umfasst das Hinzufügen eines DNS-TXT-Eintrags zu den DNS-Einstellungen Ihrer Domain. Dieser Datensatz gibt Ihre DMARC-Richtlinie an, z. B. ob Nachrichten, bei denen die Authentifizierung fehlschlägt, unter Quarantäne gestellt oder abgelehnt werden. Die Implementierung von DMARC ist ein proaktiver Schritt zur Verbesserung der E-Mail-Sicherheit und zum Schutz sowohl Ihrer Organisation als auch Ihrer Empfänger vor E-Mail-basierten Bedrohungen.

## Implementieren von DMARC {#implement-dmarc}

* Wenn Sie DMARC nicht hinzufügen, werden Sie (zumindest) unter Quarantäne gestellt.

* Stellen Sie sicher, dass Sie einen echten Posteingang haben, in dem Sie den Posteingang empfangen können - Sie verwalten diesen Posteingang (sollte kein Adobe-Posteingang sein).

Die Empfehlung lautet 24, da ISPs dies im Allgemeinen haben.
falls weniger, bewerten Sie Ihre Kapazität / überprüfen Sie Ihr > Chat-GPT.

Wenn ein DMARC-Datensatz erkannt wird, können Sie dieselben Werte kopieren und einfügen oder bei Bedarf ändern.

Wenn Sie nichts eingeben, werden Standardwerte verwendet.

### Vollständig delegierte Subdomains

### Mit CNAME delegierte Subdomains

für CNAME im Bearbeitungsfluss müssen Sie die CSV-Datei erneut herunterladen (nicht vollständig delegiert)





