---
title: Subdomänen delegieren
description: Erfahren Sie, wie Sie Ihre Subdomänen delegieren
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 11%

---


# Subdomäne delegieren

Mit Journey Optimizer können Sie Ihre Subdomänen vollständig an die Adobe delegieren. Auf diese Weise kann Adobe Nachrichten als verwalteten Dienst bereitstellen, indem sie alle DNS-Aspekte kontrolliert und pflegt, die für die Bereitstellung, Wiedergabe und Verfolgung von E-Mail-Kampagnen erforderlich sind.

>[!NOTE]
>
>Sie können bis zu 10 Subdomänen delegieren.
>
>Die Verwendung von CNAMEs für Subdomänendelegation wird von Journey Optimizer derzeit nicht unterstützt.

Gehen Sie wie folgt vor, um eine neue Subdomäne zu delegieren:

1. Rufen Sie das Menü **[!UICONTROL Kanal]** / **[!UICONTROL Subdomänen]** auf und klicken Sie dann auf **[!UICONTROL Subdomäne delegieren]**.

   ![](../assets/subdomain-delegate.png)

1. Geben Sie den Namen der Subdomäne an, die delegiert werden soll.

   ![](../assets/subdomain-name.png)

1. Die Liste der Einträge, die auf Ihren DNS-Servern gespeichert werden sollen, wird angezeigt. Kopieren Sie diese Einträge entweder einzeln oder durch Herunterladen einer CSV-Datei, und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um die passenden DNS-Einträge zu generieren.

   Stellen Sie sicher, dass alle DNS-Datensätze in Ihrer Domänenhostinglösung generiert wurden. Wenn alles richtig konfiguriert ist, markieren Sie das Kästchen &quot;Ich versichere...&quot; und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Sie können die Datensätze erstellen und die Subdomänenkonfiguration später mit der Schaltfläche **[!UICONTROL Als Entwurf speichern]** übermitteln. Anschließend können Sie die Subdomänendelegation wieder aufnehmen, indem Sie sie aus der Subdomänen-Liste öffnen.

1. Sobald die Subdomänendelegation gesendet wurde, wird die Subdomäne in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt. Weitere Informationen zu den Status von Subdomänen finden Sie in [diesem Abschnitt](access-subdomains.md).

   Die folgenden Konfigurationsüberprüfungen werden durchgeführt, bis die Subdomäne überprüft wird und zum Konfigurieren von Nachrichtenvorgaben zum Senden von Nachrichten verwendet werden kann:

   1. NS records,
   1. DNS-Erstellung,
   1. URLs-Konfiguration,
   1. Prüfung der Lieferbarkeit.

   ![](../assets/subdomain-processing.png)

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, werden Sie über eine **[!DNL Journey Optimizer]**-Benachrichtigung informiert und die Subdomäne erhält den Status **[!UICONTROL Erfolg]**. Es kann jetzt verwendet werden, um Nachrichten zu senden.

   Weitere Informationen zu den Status von Subdomänen finden Sie in [diesem Abschnitt](access-subdomains.md).

   ![](../assets/subdomain-notification.png)

   Sie können auf detaillierte Informationen zur Subdomäne zugreifen, indem Sie sie in der Liste öffnen. Sie haben folgende Möglichkeiten:

   * Rufen Sie den während des Delegierungsprozesses konfigurierten Subdomänennamen (schreibgeschützt) sowie die generierten URLs (Ressourcen, Mirrorseite, Tracking-URLs) ab,
   * hinzufügen Sie einen TXT-Eintrag zur Überprüfung Ihrer Subdomäne durch Google-Site an, um sicherzustellen, dass er überprüft wird (siehe [Hinzufügen einen Google TXT-Datensatz zu einer Subdomäne](google-txt.md)).
   ![](../assets/subdomain-delegated.png)
