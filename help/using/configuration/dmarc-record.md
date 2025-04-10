---
solution: Journey Optimizer
product: journey optimizer
title: DMARC-Eintrag
description: Erfahren Sie, wie Sie einen DMARC-Eintrag in Journey Optimizer festlegen
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Domain, Mail, DMARC, Eintrag
exl-id: f9e217f8-5aa8-4d3a-96fc-65defcb5d340
source-git-commit: 7ca149d420f802a6230e699cffefddc4117cb85e
workflow-type: ht
source-wordcount: '1482'
ht-degree: 100%

---

# DMARC-Eintrag {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Einrichten des DMARC-Eintrags"
>abstract="DMARC ist eine E-Mail-Authentifizierungsmethode, mit der Inhaberinnen und Inhaber einer Domain ihre Domain vor unbefugter Verwendung schützen und Zustellbarkeitsprobleme mit Postfachanbietern vermeiden können.<br>Zur Einhaltung der Best Practices in der Branche verlangen Google und Yahoo! beide einen DMARC-Eintrag für jede Domain, die Sie zum Senden von E-Mails an sie verwenden."

## Was ist DMARC? {#what-is-dmarc}

Die Domain-basierte Nachrichtenauthentifizierung, Berichte und Konformität (DMARC) ist eine E-Mail-Authentifizierungsmethode, mit der der Inhaberinnen und Inhaber einer Domain ihre Domain vor unbefugter Verwendung schützen können. Durch eine klare Richtlinie für E-Mail-Anbieter/Internet-Dienstanbieter (Internet Service Providers, ISPs) verhindert sie, dass auf böswillige Weise E-Mails gesendet werden, die scheinbar von Ihrer Domain stammen. Die Implementierung von DMARC verringert das Risiko, dass legitime E-Mails als Spam gekennzeichnet oder abgelehnt werden, und verbessert die Zustellbarkeit Ihrer E-Mails.

DMARC bietet außerdem Berichte zu Nachrichten, die bei der Authentifizierung fehlschlagen, sowie Kontrolle über die Verarbeitung von E-Mails, die die DMARC-Validierung nicht bestehen. Je nach der implementierten [DMARC-Richtlinie](#dmarc-policies) können diese E-Mails überwacht, unter Quarantäne gestellt oder abgelehnt werden. Mit diesen Funktionen können Sie Maßnahmen ergreifen, um potenzielle Fehler zu vermeiden und zu beheben.

Um Probleme mit der Zustellbarkeit zu vermeiden und gleichzeitig die Kontrolle über E-Mails zu erhalten, die nicht authentifiziert werden können, unterstützt [!DNL Journey Optimizer] jetzt die DMARC-Technologie direkt in seiner Administrationsoberfläche. [Weitere Informationen](#implement-dmarc)

### Wie funktioniert DMARC? {#how-dmarc-works}

SPF und DKIM werden verwendet, um eine E-Mail mit einer Domain zu verknüpfen und gemeinsam E-Mails zu authentifizieren. DMARC geht noch einen Schritt weiter und hilft, das Spoofing zu verhindern, indem die von DKIM und SPF überprüfte Domain abgeglichen wird.

>[!NOTE]
>
>In Journey Optimizer sind SPF und DKIM für Sie konfiguriert.

Um DMARC zu durchlaufen, muss eine Nachricht SPF oder DKIM durchlaufen:

* SPF (Sender Policy Framework) hilft bei der Überprüfung, ob die E-Mail-Nachricht von einer autorisierten Quelle stammt, indem die IP-Adresse des sendenden Servers mit einer Liste autorisierter IP-Adressen für die Domain abgeglichen wird.
* DKIM (DomainKeys Identified Mail) fügt den E-Mail-Nachrichten eine digitale Signatur hinzu, die es den Empfängerinnen und Empfängern ermöglicht, die Integrität und Authentizität der Nachricht zu überprüfen.

Wenn bei einem von ihnen oder beiden die Authentifizierung fehlschlägt, schlägt DMARC fehl und die E-Mail wird gemäß der von Ihnen gewählten DMARC-Richtlinie zugestellt.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### DMARC-Richtlinien {#dmarc-policies}

Wenn die DMARC-Authentifizierung einer E-Mail fehlschlägt, können Sie entscheiden, welche Aktion auf diese Nachricht angewendet wird. DMARC verfügt über drei Richtlinienoptionen:

* Überwachen (p=none): Weist den Postfachanbieter/ISP an, mit der Nachricht zu verfahren, wie er es normalerweise tun würde.
* Quarantäne (p=quarantine): Weist den Postfachanbieter/ISP an, E-Mails zu senden, die DMARC nicht an den Spam- oder Junk-Ordner des Empfangenden weitergeben.
* Ablehnen (p=reject): Weist den Postfachanbieter/ISP an, E-Mails zu blockieren, die DMARC nicht weiterleiten und zu einem Bounce führen.

>[!NOTE]
>
>In [diesem Abschnitt](#set-up-dmarc) erfahren Sie, wie Sie die DMARC-Richtlinie mit [!DNL Journey Optimizer] einrichten.

## Aktualisierung der DMARC-Anforderungen {#dmarc-update}

Zur Einhaltung der Best Practices in der Branche verlangen Google und Yahoo! beide einen **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails an sie verwenden. Diese neue Anforderung gilt seit dem **1. Februar 2024**.

>[!CAUTION]
>
>Bei Nichteinhaltung dieser neuen Anforderung von Gmail und Yahoo! werden E-Mails wahrscheinlich im Spam-Ordner landen oder blockiert.

Daher empfiehlt Adobe dringend, die folgenden Maßnahmen zu ergreifen:

* Stellen Sie sicher, dass der **DMARC-Eintrag** für **alle Subdomains eingerichtet ist, die Sie bereits in [!DNL Journey Optimizer] an Adobe delegiert haben**. [Weitere Informationen](#check-subdomains-for-dmarc)

* Wenn Sie **eine neue Subdomain** an Adobe delegieren, können Sie direkt **in der [!DNL Journey Optimizer]-Administrationsoberfläche** **DMARC einrichten**. [Weitere Informationen](#implement-dmarc)

## Implementieren von DMARC in [!DNL Journey Optimizer] {#implement-dmarc}

Über die [!DNL Journey Optimizer]-Administrationsschnittstelle können Sie einen DMARC-Eintrag für alle Subdomains einrichten, die Sie bereits an Adobe delegiert haben oder delegieren werden. Die detaillierten Schritte werden nachfolgend beschrieben.

### Überprüfen Sie Ihre vorhandenen Subdomains auf DMARC {#check-subdomains-for-dmarc}

Um sicherzustellen, dass Sie den DMARC-Eintrag für alle Subdomains, die Sie in [!DNL Journey Optimizer] delegiert haben, eingerichtet haben, führen Sie die folgenden Schritte aus.

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** > **[!UICONTROL Subdomains]** auf und klicken Sie dann auf **[!UICONTROL Subdomain einrichten]**.

1. Überprüfen Sie für jede delegierte Subdomain die Spalte **[!UICONTROL DMARC-Eintrag]**. Wenn für eine bestimmte Subdomain kein Eintrag gefunden wurde, wird ein Warnhinweis angezeigt.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Um die neue Anforderung von Gmail und Yahoo zu erfüllen und Zustellbarkeitsprobleme mit wichtigen ISPs zu vermeiden, wird empfohlen, für alle delegierten Subdomains einen DMARC-Eintrag einzurichten. [Weitere Informationen](dmarc-record-update.md)

1. Wählen Sie eine Subdomain ohne zugehörigen DMARC-Eintrag aus und füllen Sie den Abschnitt **[!UICONTROL DMARC-Eintrag]** entsprechend den Anforderungen Ihres Unternehmens aus. Die Schritte zum Befüllen des Felds „DMARC-Eintrag“ sind in [diesem Abschnitt](#implement-dmarc) beschrieben.

   <!--![](assets/dmarc-record-edit-full.png)-->

   >[!NOTE]
   >
   >Je nachdem, ob ein DMARC-Eintrag bei der übergeordneten Domain gefunden wird oder nicht, können Sie die Werte aus der übergeordneten Domain verwenden oder den DMARC-Eintrag von Adobe verwalten lassen. [Weitere Informationen](#implement-dmarc)

1. Wenn Sie eine Subdomain bearbeiten, die:

   * [vollständig an Adobe delegiert](delegate-subdomain.md#full-subdomain-delegation) wurde, ist keine weitere Aktion erforderlich,

   * mit [CNAME](delegate-subdomain.md#cname-subdomain-delegation) eingerichtet wurde, müssen Sie den DNS-Eintrag für DMARC in Ihre Hosting-Lösung kopieren, um die entsprechenden DNS-Einträge zu generieren.

     ![](assets/dmarc-record-edit-cname.png)

     Stellen Sie sicher, dass der DNS-Eintrag in Ihrer Domain-Hosting-Lösung generiert wurde, und aktivieren Sie das Kontrollkästchen „Ich bestätige …“.

1. Speichern Sie Ihre Änderungen.

### Einrichten von DMARC für neue Subdomains {#set-up-dmarc}

Beim Delegieren neuer Subdomains zu Adobe in [!DNL Journey Optimizer] wird für Ihre Domain ein DMARC-Eintrag in DNS erstellt. Gehen Sie wie folgt vor, um DMARC zu implementieren.

>[!CAUTION]
>
>Um die neue Anforderung von Gmail und Yahoo zu erfüllen und Zustellbarkeitsprobleme mit wichtigen ISPs zu vermeiden, wird empfohlen, für alle delegierten Subdomains einen DMARC-Eintrag einzurichten. [Weitere Informationen](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Einrichten einer neuen Subdomain [Weitere Informationen](delegate-subdomain.md)

1. Navigieren Sie zum Abschnitt **[!UICONTROL DMARC-Eintrag]**.

1. Wenn in der Ihrer Subdomain zugeordneten übergeordneten Domain ein DMARC-Eintrag verfügbar ist, werden zwei Optionen angezeigt:

   ![](assets/dmarc-record-found.png)

   * **[!UICONTROL Mit Adobe verwalten]**: Sie können den DMARC-Eintrag für Ihre Subdomain von Adobe verwalten lassen. Befolgen Sie die in [diesem Abschnitt](#manage-dmarc-with-adobe) beschriebenen Schritte.

   * **[!UICONTROL Eigenständig verwalten]**: <!--This option is selected by default.-->Mit dieser Option können Sie den DMARC-Eintrag außerhalb von [!DNL Journey Optimizer] verwalten, indem Sie die Werte aus Ihrer übergeordneten Domain verwenden. Diese Werte werden in der Benutzeroberfläche angezeigt, können jedoch nicht bearbeitet werden.

     ![](assets/dmarc-record-found-own.png){width="80%"}

1. Wenn in der übergeordneten Domain kein DMARC-Eintrag gefunden wird, ist nur die Option **[!UICONTROL Mit Adobe verwalten]** verfügbar. Führen Sie die [nachstehenden](#manage-dmarc-with-adobe) Schritte durch, um einen DMARC-Eintrag für Ihre Subdomain einzurichten.

   ![](assets/dmarc-record-not-found.png){width="80%"}

### Verwalten von DMARC-Einträgen mit Adobe {#manage-dmarc-with-adobe}

Damit Adobe den DMARC-Eintrag für Sie verwalten kann, wählen Sie die Option **[!UICONTROL Mit Adobe verwalten]** aus und führen Sie die nachfolgenden Schritte aus.

>[!NOTE]
>
>Erfolgt der Abruf über [!DNL Journey Optimizer], können Sie dieselben Werte verwenden, die in der Benutzeroberfläche hervorgehoben sind, oder sie nach Bedarf ändern.

![](assets/dmarc-record-with-adobe-ex.png){width="80%"}

>[!NOTE]
>
>Wenn Sie keine Werte hinzufügen, werden die vorausgefüllten Standardwerte verwendet.

1. Legen Sie die Aktion fest, die der Empfänger-Server ausführen soll, wenn DMARC fehlschlägt. Wählen Sie je nach der [DMARC-Richtlinie](#dmarc-policies), die Sie anwenden möchten, eine der drei Optionen aus:

   * **[!UICONTROL Keines]** (Standardwert): Weist den Empfänger an, keine Aktionen für Nachrichten durchzuführen, die bei der DMARC-Authentifizierung fehlschlagen, aber trotzdem E-Mail-Berichte an den Absender zu senden.
   * **[!UICONTROL Quarantäne]**: Weist den E-Mail-Empfangs-Server an, E-Mails unter Quarantäne zu stellen, die bei der DMARC-Authentifizierung fehlschlagen. Dies bedeutet im Allgemeinen, dass diese Nachrichten im Spam- oder Junk-Ordner des Empfängers ankommen.
   * **[!UICONTROL Ablehnen]**: Weist den Empfänger an, jede E-Mail für die Domain, bei der die Authentifizierung fehlschlägt, komplett zu verweigern (Bounce). Wenn diese Richtlinie aktiviert ist, haben nur E-Mails, die von Ihrer Domain zu 100 % authentifiziert wurden, überhaupt die Möglichkeit, in den Posteingang zu gelangen.

   >[!NOTE]
   >
   >Als Best Practice wird empfohlen, die DMARC-Implementierung langsam einzuführen, indem Sie Ihre DMARC-Richtlinie von **Keine** auf **Quarantäne** auf **Ablehnen** anheben, während Sie sich mit den potenziellen Auswirkungen von DMARC vertraut machen.

1. Fügen Sie optional eine oder mehrere E-Mail-Adressen Ihrer Wahl hinzu, um anzugeben, wo in Ihrer Organisation die **DMARC-Berichte** zu E-Mails, bei denen die [Authentifizierung fehlschlägt](#how-dmarc-works), ankommen sollen. Sie können für jeden Bericht bis zu fünf Adressen hinzufügen.

   >[!NOTE]
   >
   >Stellen Sie sicher, dass Sie über einen eigenen Posteingang (nicht Adobe) verfügen, in dem Sie diese Berichte empfangen können.

   Es gibt zwei verschiedene Berichte, die von ISPs generiert werden und die Absenderinnen und Absender über die RUA/RUF-Tags in ihrer DMARC-Richtlinie empfangen können:

   * **Aggregierte Berichte** (RUA): Sie enthalten keine personenbezogenen Daten (PII), bei denen es sich im Sinne der DSGVO um sensible Daten handeln könnte.
   * **Forensische Fehlerberichte** (RUF): Sie enthalten E-Mail-Adressen, bei denen es sich im Sinne der DSGVO um sensible E-Mail-Adressen handelt. Prüfen Sie vor der Verwendung intern, wie mit Informationen umgegangen werden soll, die DSGVO-konform sein müssen.

   >[!NOTE]
   >
   >Diese hochtechnischen Berichte bieten einen Überblick über E-Mails, bei denen es sich um versuchtes Spoofing handelt. Sie sollten am besten mit einem Tool eines Drittanbieters verarbeitet werden.

1. Wählen Sie den **anwendbaren Prozentsatz** von E-Mails für DMARC aus.

   Dieser Prozentsatz hängt von Ihrem Vertrauen in Ihre E-Mail-Infrastruktur und der Toleranz gegenüber Fehlalarmen (legitime E-Mails, die als betrügerisch gekennzeichnet werden) ab. Es ist üblich, dass Unternehmen mit einer DMARC-Richtlinie beginnen, die auf **none** (keine) eingestellt ist, dann schrittweise den Prozentsatz der DMARC-Richtlinien erhöhen und die Auswirkungen auf den legitimen E-Mail-Versand überwachen.

   >[!NOTE]
   >
   >Arbeiten Sie mit Ihren E-Mail-Admins und Ihrem IT-Team zusammen, um den Prozentsatz schrittweise zu erhöhen, sobald Sie Vertrauen in Ihren E-Mail-Authentifizierungsprozess haben.

   Als Best Practice sollten Sie eine hohe DMARC-Konformitätsrate anstreben, die idealerweise nahe bei 100 % liegt, um die Sicherheitsvorteile zu maximieren und gleichzeitig das Risiko von Fehlalarmen zu minimieren.

1. Wählen Sie eine **Berichtsintervall** zwischen 24 und 168 Stunden aus. Eigentümerinnen und Eigentümer von Domains können damit regelmäßige Updates zu E-Mail-Authentifizierungsergebnissen erhalten und die erforderlichen Maßnahmen zur Verbesserung der E-Mail-Sicherheit ergreifen.

<!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

The default value (24 hours) is generally the email providers' expectation.

**********

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.

-->
