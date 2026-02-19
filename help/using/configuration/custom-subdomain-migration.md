---
solution: Journey Optimizer
product: journey optimizer
title: E-Mail-Subdomain von CNAME zur benutzerdefinierten Delegierung migrieren
description: Erfahren Sie, wie Sie eine E-Mail- oder Landingpage-Subdomain von der CNAME-Delegierung zur benutzerdefinierten Delegierung in Journey Optimizer migrieren.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Intermediate
keywords: Subdomain, Zuweisung, Migration, CNAME, benutzerdefinierte Zuweisung
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 316553be4f04e4fc0ae11bc767f7e48f64fc5ccd
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 22%

---

# E-Mail-Subdomain von CNAME zur benutzerdefinierten Delegierung migrieren {#migrate-cname-to-custom}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Wenn Ihre Subdomain derzeit mit [CNAMEs](about-subdomain-delegation.md#cname-subdomain-setup) eingerichtet ist, können Sie sie zur Methode der **[!UICONTROL benutzerdefinierten Delegierung]** migrieren, um die Sicherheitsrichtlinien Ihres Unternehmens zu erfüllen. Dadurch erhalten Sie vollständige Eigentümerschaft und Kontrolle über Ihre Subdomains und Zertifikate in [!DNL Journey Optimizer]. [Weitere Informationen zu benutzerdefinierten Subdomains](delegate-custom-subdomain.md)

Im Rahmen dieses Prozesses müssen Sie:

* [Löschen der vorhandenen DNS-Einträge](#delete-dns) aus Ihrer Hosting-Lösung
* [Hochladen des SSL-](#upload-ssl-certificate), das von der Zertifizierungsstelle abgerufen wurde
* Schließen Sie die [Schritte der Feedback-Schleife](#feedback-loop) ab, indem Sie Domain-Eigentümerschaft und Reporting-E-Mail-Adresse überprüfen
* [Kopieren Sie den von Adobe generierten SSL](#copy-ssl-cdn-url-record)CDN-URL-Validierungseintrag in Ihre Hosting-Plattform.

Gehen Sie wie folgt vor, um Ihre Subdomain zu migrieren.

## Voraussetzungen {#before-you-begin}

Bevor Sie mit dem Migrationsprozess beginnen, lesen Sie die folgenden wichtigen Informationen.

>[!IMPORTANT]
>
>Eine Subdomain, die eingerichtet wurde, kann nur mit der [CNAME-Methode) migriert ](delegate-subdomain.md#cname-subdomain-setup).

* Stellen Sie sicher, dass die **Methode der benutzerdefinierten Delegierung“ für** Unternehmen aktiviert ist (diese Funktion ist derzeit nur eingeschränkt verfügbar. Bitte den Adobe-Support kontaktieren, um Zugang zu erhalten). [Weitere Informationen](delegate-custom-subdomain.md)
* Stellen Sie sicher, dass diese Subdomain nicht von aktiven Kanalkonfigurationen verwendet wird. Der Migrationsprozess unterbricht ihre Funktionalität.
* Vergewissern Sie sich, dass keine aktiven Kampagnen oder Journey eine mit dieser Subdomain verknüpfte Kanalkonfiguration verwenden, da dies zu Versandunterbrechungen führen kann.
* Beachten Sie, dass Ausfallzeiten beginnen, sobald Sie den Migrationsfluss starten. Die Subdomain wechselt während **[!UICONTROL Prozesses zu &quot;]**&quot; und ist erst nach Abschluss des Setups verfügbar.
* Daher wird empfohlen, **die Schritte vor der Migration auszuführen, bevor der Migrationsprozess gestartet wird** - um Ihr SSL-Zertifikat bereit zu haben und Ausfallzeiten zu reduzieren. [Weitere Informationen](#start-migration)

## Starten der Migration {#start-migration}

Gehen Sie wie folgt vor, um mit der Migration einer bestimmten Subdomain zu beginnen.

1. Navigieren Sie **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** > **[!UICONTROL Subdomains]**.

1. Wählen Sie eine mit CNAMEs eingerichtete Subdomain aus und öffnen Sie sie.

1. Sie können den Abschnitt **[!UICONTROL CSR-Generierung vor der Migration]** verwenden, um die CSR zum Senden an die Zertifizierungsstelle zu generieren und das SSL-Zertifikat bereit zu haben, wenn der Migrationsprozess beginnt. [Weitere Informationen](#send-csr-to-ca)

   >[!IMPORTANT]
   >
   >Die Schritte vor der Migration sind in dieser Phase optional, werden jedoch dringend empfohlen. Wenn Sie diese **vor** Start der Migration abschließen, reduzieren Sie Ausfallzeiten und gewährleisten einen reibungslosen Übergang.

   ![](assets/subdomain-migrate-pre-migration-csr.png){width="70%"}

1. Wählen **[!UICONTROL Jetzt migrieren]** im entsprechenden Abschnitt aus.

   <!--![](assets/subdomain-migrate-to-custom.png){width=90%}-->

1. Überprüfen Sie die [angezeigten Informationen](#before-you-begin).

   >[!WARNING]
   >
   >Ausfallzeiten beginnen sofort nach dem Eintritt in den Migrationsfluss. Stellen Sie daher sicher, dass sich dies nicht auf Ihre aktiven Kampagnen und Journey auswirkt.

1. Klicken Sie **[!UICONTROL Ja]**. Die Subdomain wechselt in den Status **[!UICONTROL Entwurf]** und ist erst nach Abschluss des Setups verfügbar.

## CSR generieren und an die Zertifizierungsstelle senden {#send-csr-to-ca}

Um die Migration abzuschließen, benötigen Sie ein SSL-Zertifikat, das von einer Zertifizierungsstelle (CA) ausgestellt wurde. Um dieses SSL-Zertifikat zu erhalten, müssen Sie zunächst ein Certificate Signing Request (CSR) generieren und an die Zertifizierungsstelle senden.

Unabhängig davon, ob Sie den Migrationsprozess bereits gestartet haben oder nicht, führen Sie die folgenden Schritte aus, um Ihre neue CSR zu generieren und zu senden.

1. Klicken Sie **[!UICONTROL CSR neu erstellen]**.

1. Füllen Sie das angezeigte Formular aus und generieren Sie die Certificate Signing Request (CSR) neu.

   ![](assets/subdomain-migrate-regenerate-csr.png){width="60%"}

   >[!NOTE]
   >
   >Die Schlüssellänge kann nur 2.048 oder 4.096 Bit betragen. Sie kann nach dem Senden der Subdomain nicht mehr geändert werden.

1. Klicken Sie auf **[!UICONTROL CSR herunterladen]** und speichern Sie das Formular lokal auf Ihrem Computer. 

1. Senden Sie es an die Zertifizierungsstelle (CA), um Ihr SSL-Zertifikat zu erhalten. Bevor Sie diese CSR zur Signierung an Ihre Zertifizierungsstelle senden, sollten Sie einige wichtige Punkte beachten:

   * Die heruntergeladene CSR aus Schritt 3 gilt nur für data.subdomain.com.

   * Das Zertifikat sollte jedoch sowohl data.subdomain.com als auch cdn.subdomain.com als Subject Alternative Names (SAN)-Einträge in einem einzigen Zertifikat abdecken. Wenn Sie beispielsweise example.adobe.com delegieren, entspricht data.subdomain.com dem Eintrag data.example.adobe.com und cdn.subdomain.com entspricht cdn.example.adobe.com.

   * Die Subdomains „Data“ (data.example.adobe.com) und „CDN“ (cdn.example.adobe.com) müssen als Peer-Einträge im selben Zertifikat hinzugefügt werden.

   * Die meisten Zertifizierungsstellen ermöglichen es Ihnen, während des Signiervorgangs zusätzliche SANs hinzuzufügen (z. B. die Subdomain „CDN“).

      * Das ist über das CA-Portal (empfohlen, falls verfügbar) oder
      * durch manuelles Anfragen beim Support-Team möglich, sollte die Portaloption nicht verfügbar sein.

   * Nach der Signierung stellt die Zertifizierungsstelle ein einziges Zertifikat aus, das sowohl die Domain „Data“ als auch die Subdomain „CDN“ umfasst.

## Löschen vorhandener DNS-Einträge {#delete-dns}

Nach dem Start des Migrationsprozesses müssen Sie die vorhandenen DNS-Einträge aus Ihrer Hosting-Lösung löschen. Gehen Sie wie folgt vor.

1. Die Liste der derzeit auf Ihren DNS-Servern konfigurierten Einträge wird angezeigt.

1. Navigieren Sie zu Ihrer Domain-Hosting-Lösung und löschen Sie die vorhandenen CNAME-Einträge aus Ihrem DNS-Hosting.

1. Stellen Sie sicher, dass alle DNS-Einträge gelöscht wurden. Aktivieren Sie abschließend das Kontrollkästchen „Ich bestätige, dass ich die erforderlichen Einträge von der Hosting-Site gelöscht habe“.

   ![](assets/subdomain-migrate-delete-dns.png){width="75%"}

## Hochladen des SSL-Zertifikats {#upload-ssl-certificate}

Im Abschnitt **[!UICONTROL SSL-Zertifikat]** müssen Sie ein neues SSL-Zertifikat in [!DNL Journey Optimizer] hochladen.

Überprüfen Sie davor Folgendes:

* Wenn Sie Ihre CSR bereits im Rahmen der [Schritte vor der Migration“ an die Zertifizierungsstelle gesendet ](#start-migration), stellen Sie sicher, dass Sie Ihr SSL-Zertifikat erhalten haben.

* Wenn Sie dies noch nicht getan haben, führen Sie die Schritte zum [Generieren, Herunterladen und Senden der CSR](#send-csr-to-ca) aus.

<!--
    * Click **[!UICONTROL Regenerate CSR]** and fill the form to generate the Certificate Signing Request.

    * Click **[!UICONTROL Download CSR]** to save the form to your local computer.

    * Send the CSR to the Certificate Authority to get your SSL certificate.-->

1. Nachdem Sie Ihr SSL-Zertifikat abgerufen haben, klicken Sie auf **[!UICONTROL Zertifikat hochladen]**.

   ![](assets/subdomain-migrate-ssl-certificate.png){width="75%"}

1. Laden Sie das SSL-Zertifikat mit der vollständigen Zertifikatskette im .pem-Format in [!DNL Journey Optimizer] hoch. Im Folgenden finden Sie ein Beispiel für ein .pem-Dateiformat:

   ```
   -----BEGIN CERTIFICATE-----
   MIIDXTCCAkWgAwIBAgIJALc3... (base64 encoded data)
   -----END CERTIFICATE-----
   ```
1. Markieren Sie das Kästchen „Ich bestätige, dass ich das SSL-Zertifikat hochgeladen habe“.

## Vollständige Feedback-Schleife {#feedback-loop}

Führen Sie dann die Schritte der Feedback-Schleife aus, um Domain-Eigentümerschaft und Reporting-E-Mail-Adresse zu überprüfen.

![](assets/subdomain-migrate-feedback-loop.png){width="75%"}

Der Prozess ist der gleiche wie beim Einrichten einer neuen benutzerdefinierten Subdomain. Befolgen Sie die auf der Seite [Einrichten einer benutzerdefinierten Subdomain](delegate-custom-subdomain.md#feedback-loop-steps) beschriebenen Schritte.

## Kopieren des SSL-CDN-URL-Validierungseintrags {#copy-ssl-cdn-url-record}

Um den Migrationsprozess abzuschließen, kopieren Sie den von Adobe generierten SSL-CDN-URL-Validierungseintrag in Ihre Hosting-Plattform. Der Prozess ist der gleiche wie beim Einrichten einer neuen benutzerdefinierten Subdomain. Befolgen Sie die auf der Seite [Einrichten einer benutzerdefinierten Subdomain](delegate-custom-subdomain.md#copy-ssl-cdn-url-record) beschriebenen Schritte.

Nach dem Senden müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was bis zu 3 Stunden dauern kann. [Weitere Informationen](delegate-subdomain.md#submit-subdomain)

Sobald die Subdomain wieder aktiv ist, müssen keine Änderungen an vorhandenen Kanalkonfigurationen vorgenommen werden, die sie verwenden. Sie funktionieren weiterhin wie zuvor.

**Siehe auch**

* [Einrichten einer benutzerdefinierten Subdomain](delegate-custom-subdomain.md)
* [Methoden der Subdomain-Zuweisung](about-subdomain-delegation.md#subdomain-delegation-methods)
