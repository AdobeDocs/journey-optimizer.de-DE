---
solution: Journey Optimizer
product: journey optimizer
title: Delegieren einer benutzerdefinierten Subdomain
description: Erfahren Sie, wie Sie benutzerdefinierte Subdomains delegieren.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Delegierung, Domain, DNS
hide: true
hidefromtoc: true
exl-id: 34af1329-f0c8-4fcd-a284-f8f4214611d4
source-git-commit: 64ff860167439e1b098918cd913f2361f7365a50
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 14%

---

# Einrichten einer benutzerdefinierten Subdomain {#delegate-custom-subdomain}

Als Alternative zu den Methoden [Vollständig delegiert](about-subdomain-delegation.md#full-subdomain-delegation) und [CNAME eingerichtet](about-subdomain-delegation.md#cname-subdomain-delegation) können Sie mit der **Benutzerdefinierte Delegierung** die Verantwortung für Ihre Subdomains in Journey Optimizer übernehmen und die generierten Zertifikate vollständig kontrollieren.

Im Rahmen dieses Prozesses muss Adobe sicherstellen, dass Ihr DNS entsprechend für die Zustellung, das Rendering und das Tracking von Nachrichten konfiguriert ist. Aus diesem Grund müssen Sie das von [ Zertifizierungsstelle ](#upload-ssl-certificate) SSL-Zertifikat hochladen und die [Schritte der Feedback-Schleife) ](#feedback-loop-steps), indem Sie Domain-Eigentümerschaft und Reporting-E-Mail-Adresse überprüfen.

Gehen Sie wie folgt vor, um eine benutzerdefinierte Subdomain einzurichten.

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-]** > **[!UICONTROL Subdomains]** auf.

1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.

1. Wählen Sie **[!UICONTROL Abschnitt „Methode einrichten]** die Option **[!UICONTROL Benutzerdefinierte Delegierung]** aus.

   ![](assets/subdomain-method-custom.png){width=90%}

1. Geben Sie den Namen der zu delegierenden Subdomain an.

   >[!CAUTION]
   >
   >Es kann nicht dieselbe Versand-Domain zum Senden von Nachrichten von [!DNL Adobe Journey Optimizer] und von einem anderen Produkt, z. B. [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage], verwendet werden.

## DNS-Einträge erstellen {#create-dns-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom_dns"
>title="Erstellen der passenden DNS-Einträge"
>abstract="Um eine benutzerdefinierte Subdomain an Adobe zu delegieren, müssen Sie die in der Journey Optimizer-Benutzeroberfläche angezeigten Nameserver-Informationen kopieren und in Ihre Domain-Hosting-Lösung einfügen, um die entsprechenden DNS-Einträge zu generieren."

1. Die Liste der Einträge, die auf Ihren DNS-Servern gespeichert werden sollen, wird angezeigt. Kopieren Sie diese Datensätze entweder einzeln oder durch Herunterladen einer CSV-Datei.

1. Navigieren Sie zu Ihrer Domain-Hosting-Lösung, um die entsprechenden DNS-Einträge zu generieren.

1. Stellen Sie sicher, dass alle DNS-Einträge in Ihrer Domain-Hosting-Lösung generiert wurden.

1. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie die Checkbox „Ich bestätige…“.

   ![](assets/subdomain-custom-submit.png){width="75%"}

## Hochladen des SSL-Zertifikats {#upload-ssl-certificate}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom-ssl"
>title="Certificate Signing Request generieren"
>abstract="Beim Einrichten einer neuen benutzerdefinierten Subdomain müssen Sie die Certificate Signing Request (CSR) generieren, ausfüllen und an die Zertifizierungsstelle senden, um das SSL-Zertifikat abzurufen, das Sie in Journey Optimizer hochladen müssen."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_key_length"
>title="xxx"
>abstract=""

1. Klicken Sie im Abschnitt **[!UICONTROL SSL]** Zertifikat) auf **[!UICONTROL CSR generieren]**.

   ![](assets/subdomain-custom-ssl-certificate.png){width="85%"}

   >[!NOTE]
   >
   >Das Ablaufdatum Ihres SSL-Zertifikats wird angezeigt. Sobald das Datum erreicht ist, müssen Sie ein neues Zertifikat hochladen.

1. Füllen Sie das angezeigte Formular aus und generieren Sie die Certificate Signing Request (CSR).

   ![](assets/subdomain-custom-generate-csr.png){width="70%"}

   >[!NOTE]
   >
   >Die Schlüssellänge kann nur 2048 oder 4096 Bit betragen. Sie kann nach dem Senden der Subdomain nicht mehr geändert werden.

1. Klicken Sie **[!UICONTROL CSR herunterladen]** und speichern Sie das Formular auf Ihrem lokalen Computer. Senden Sie es an die Zertifizierungsstelle, um Ihr SSL-Zertifikat zu erhalten.

1. Klicken Sie nach dem Abrufen **[!UICONTROL SSL-Zertifikat hochladen]** und laden Sie das Zertifikat in [!DNL Journey Optimizer] im .pem-Format hoch.

## Schritte der Feedback-Schleife abschließen {#feedback-loop-steps}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_feedback-loop"
>title="Schritte der Feedback-Schleife abschließen"
>abstract="Geh auf die Yahoo! Sender Hub und füllen Sie das Formular aus, um den Domain-Besitz zu überprüfen. Geben Sie die unten aufgeführte FBL-Reporting-E-Mail-Adresse ein und verwenden Sie das OTP, das empfangen wird, um die Eigentümerschaft an der Yahoo! Sender Hub."

1. Gehen Sie auf die [Yahoo! Sender Hub](https://senders.yahooinc.com/) Website und füllen Sie das erforderliche Formular aus, um Ihre Domain-Eigentümerschaft zu überprüfen.

1. Um den Domain-Besitz zu überprüfen, Yahoo! Absender-Hub erfordert die Angabe einer E-Mail-Adresse. Geben Sie die FBL-Reporting-E-Mail-Adresse ein, die unter **[!UICONTROL Wert]** aufgeführt ist. Dies ist eine Adobe-eigene E-Mail-Adresse.

1. Wenn Yahoo! Sender Hub generiert ein Einmalkennwort (OTP), das an diese Adobe-Adresse gesendet wird.

1. Wenden Sie sich an das Zustellbarkeits-Team von Adobe, das Ihnen diesen OTP zur Verfügung stellt. <!--Specify how to reach out + any information that customer should share in the request to deliverability team to get access to the right OTP-->

   >[!CAUTION]
   >
   >Der OTP ist nur 24 Stunden lang gültig. Stellen Sie daher sicher, dass Sie sich bei der Erstellung des OTP an Adobe wenden. <!--TBC?-->
   >
   >OTP-Anfragen können nur an Wochentagen gestellt werden. Am Wochenende gibt es keinen Support. <!--Add times + timezone-->

1. Geben Sie das OTP auf Yahoo! Sender Hub.

1. Vergewissern Sie sich, dass Sie alle Schritte der Feedback-Schleife ausgeführt haben.

1. Wenn alles richtig konfiguriert ist, aktivieren Sie das Kontrollkästchen „Ich habe abgeschlossen…“.

   ![](assets/subdomain-custom-feedback-loop.png){width="85%"}

1. Klicken Sie **[!UICONTROL Weiter]** und warten Sie, bis Adobe überprüft, ob die Einträge in Ihrer Hosting-Lösung fehlerfrei generiert wurden. Dieser Vorgang kann bis zu 2 Minuten dauern.

   >[!NOTE]
   >
   >Alle fehlenden Einträge, also die noch nicht in Ihrer Hosting-Lösung erstellten Einträge, werden aufgelistet.

   Adobe generiert einen SSL-CDN-URL-Validierungseintrag. Kopieren Sie diesen Validierungseintrag in Ihre Hosting-Plattform. Wenn Sie diesen Eintrag ordnungsgemäß in Ihrer Hosting-Lösung erstellt haben, aktivieren Sie das Kontrollkästchen „Ich bestätige…“.

1. Klicken Sie **[!UICONTROL Senden]**, damit Adobe die erforderlichen Prüfungen durchführt. [Weitere Informationen](#submit-subdomain)


## Fehlerbehebung - Checkliste {#check-list}

Wenn beim Senden Ihrer benutzerdefinierten Subdomain Fehler auftreten, führen Sie die unten aufgeführten Fehlerbehebungsaktionen durch.

* Vergewissern Sie sich, dass alle DNS-Einträge mithilfe der DNS-Lookup-Tools ordnungsgemäß weitergegeben wurden.

* Vergewissern Sie sich vor dem Hochladen, dass Ihr Zertifikat alle technischen Anforderungen erfüllt.

* Stellen Sie sicher, dass Ihr Zertifikat im richtigen Format hochgeladen wird.

