---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von Landingpage-Subdomains
description: Erfahren Sie, wie Sie mit Journey Optimizer Subdomains von Landingpages konfigurieren
feature: Landing Pages, Subdomains
role: Admin
level: Experienced
keywords: Landing, Landingpage, Subdomains, Konfiguration
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 1aa2ac109cdbf0ba6af58204926f1cd5add334b0
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 70%

---

# Konfigurieren von Landingpage-Subdomains {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="Delegieren einer Subdomain der Landingpage"
>abstract="Sie richten Ihre Subdomain für die Verwendung einer Landingpage ein. Es kann eine Subdomain verwendet werden, die bereits an Adobe delegiert ist, oder eine andere Subdomain konfiguriert werden."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="Delegieren einer Subdomain der Landingpage"
>abstract="Für Landingpages muss eine Subdomain konfiguriert werden, da diese Subdomain für die Erstellung einer Landingpage-Voreinstellung benötigt wird. Es kann eine Subdomain verwendet werden, die bereits an Adobe delegiert ist, oder eine andere Subdomain konfiguriert werden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets?lang=de#lp-create-preset" text="Erstellen von Landingpage-Voreinstellungen"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Erstellen einer Landingpage-Voreinstellung"
>abstract="Um eine Landingpage-Voreinstellung erstellen zu können, müssen Sie zuvor mindestens eine Landingpage-Subdomain konfiguriert haben, die aus der Liste „Name der Subdomain“ ausgewählt werden kann."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets?lang=de#lp-create-preset" text="Erstellen von Landingpage-Voreinstellungen"

## Erste Schritte mit Landingpage-Subdomains {#gs-lp-subdomains}

Um Landingpage[Voreinstellungen erstellen zu können](lp-presets.md) müssen Sie die Subdomains einrichten, die Sie für Ihre Landingpages verwenden werden.

Sie können eine Subdomain verwenden, die bereits an Adobe delegiert wurde, oder eine andere Subdomain konfigurieren. Weitere Informationen zum Delegieren von Subdomains an Adobe finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md).

Die Konfiguration der Landingpage-Subdomain ist **in allen Umgebungen**. Daher gilt:

* Um auf Landingpage-Subdomains zuzugreifen und diese zu bearbeiten, benötigen Sie die Berechtigung zum **[!UICONTROL Verwalten von Landpingpage-Subdomains]** in der Produktions-Sandbox.

* Jede Änderung an einer Landingpage-Subdomain wirkt sich auch auf die Produktions-Sandboxes aus.

## Verwenden einer vorhandenen Subdomain {#lp-use-existing-subdomain}

Gehen Sie wie folgt vor, um eine Subdomain zu verwenden, die bereits an Adobe delegiert ist:

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** auf und wählen Sie **[!UICONTROL Landingpage-Einstellungen]** > **[!UICONTROL Subdomains der Landingpage]** aus.

1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.

   ![](assets/lp_set-up-subdomain.png)

1. Wählen Sie **[!UICONTROL Delegierte Domain verwenden]** im Abschnitt **[!UICONTROL Konfigurationstyp]**.

   ![](assets/lp_use-delegated-subdomain.png)

1. Geben Sie das Präfix ein, das in Ihrer Landingpage-URL angezeigt werden soll.

   Nur alphanumerische Zeichen und Bindestriche sind zulässig.

1. Wählen Sie aus der Liste eine delegierte Subdomain aus.

   Sie können keine Subdomain auswählen, die bereits als Landingpage-Subdomain verwendet wird.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/lp_prefix-and-subdomain.png)

   Beachten Sie, dass Sie nicht mehrere delegierte Subdomains derselben übergeordneten Domain verwenden können. Wenn zum Beispiel „marketing1.meinefirma.com“ bereits für Ihre Landingpages an Adobe delegiert wurde, können Sie „marketing2.meinefirma.com“ nicht verwenden. Da jedoch mehrstufige Subdomains für Landingpages unterstützt werden, können Sie eine Subdomain von „marketing1.meinefirma.com“ (z. B. „email.marketing1.meinefirma.com“) oder ansonsten eine andere übergeordnete Domain verwenden.

   >[!CAUTION]
   >
   >Wenn Sie eine Domain auswählen, die mit der [CNAME-Methode](../configuration/delegate-subdomain.md#cname-subdomain-delegation) an Adobe delegiert wurde, müssen Sie den DNS-Eintrag auf Ihrer Hosting-Plattform erstellen. Um den DNS-Eintrag zu generieren, gehen Sie genauso vor wie bei der Konfiguration einer neuen Landingpage-Subdomain. Weitere Informationen dazu finden Sie in [diesem Abschnitt](#lp-configure-new-subdomain).

1. Klicken Sie auf **[!UICONTROL Senden]**.

1. Nach der Übermittlung wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   Bevor Sie diese Subdomain zum Senden von Nachrichten verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was **bis zu 4 Stunden**.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Subdomain den Status **[!UICONTROL Erfolg]**. Sie können jetzt damit Landingpage-Voreinstellungen erstellen.

## Konfigurieren einer neuen Subdomain {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="Erstellen des passenden DNS-Eintrags"
>abstract="Um eine neue Landingpage-Subdomain zu konfigurieren, müssen Sie die auf der Journey Optimizer-Benutzeroberfläche angezeigten Adobe-Nameserver-Informationen kopieren und in Ihre Domain-Hosting-Lösung einfügen, um den passenden DNS-Eintrag zu generieren. Nachdem die Prüfungen erfolgreich waren, kann die Subdomain zur Erstellung von Landingpage-Voreinstellungen verwendet werden."

Gehen Sie wie folgt vor, um eine neue Subdomain zu konfigurieren.

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** auf und wählen Sie **[!UICONTROL Landingpage-Einstellungen]** > **[!UICONTROL Subdomains der Landingpage]** aus.

1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.

1. Wählen Sie **[!UICONTROL Eigene Domain hinzufügen]** im Abschnitt **[!UICONTROL Konfigurationstyp]**.

   ![](assets/lp_add-your-own-subdomain.png)

1. Geben Sie die zu delegierende Subdomain an.

   >[!CAUTION]
   >
   >* Sie können keine schon vorhandene Landingpage-Subdomain verwenden.
   >
   >* Großbuchstaben sind in Subdomains nicht zulässig.

   Es ist nicht zulässig, Adobe eine ungültige Subdomain zuzuweisen. Vergewissern Sie sich, dass Sie eine gültige Subdomain eingeben, die Ihrem Unternehmen gehört, z. B. marketing.ihrunternehmen.com.

   Bei Landingpages werden mehrstufige Subdomains unterstützt. Sie können beispielsweise „email.marketing.meinefirma.com“ verwenden.

1. Die Liste der Einträge, die auf Ihren DNS-Servern gespeichert werden sollen, wird angezeigt. Kopieren Sie diesen Datensatz oder laden Sie eine CSV-Datei herunter und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um den entsprechenden DNS-Eintrag zu generieren.

1. Stellen Sie sicher, dass in Ihrer Domain-Hosting-Lösung ein DNS-Eintrag generiert wurde. Wenn alles ordnungsgemäß konfiguriert ist, aktivieren Sie die Checkbox „Ich bestätige...“ und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   Wenn Sie eine neue Landingpage-Subdomain konfigurieren, verweist sie immer auf einen CNAME-Eintrag.

1. Nachdem die Subdomain-Zuweisung übermittelt wurde, wird die Subdomain in der Liste mit dem Status **[!UICONTROL Verarbeitung läuft]** angezeigt. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   Bevor Sie diese Subdomain für Ihre Landingpages verwenden können, müssen Sie warten, bis Adobe die erforderlichen Prüfungen durchgeführt hat, was **bis zu 4 Stunden**.<!--Learn more in [this section](#subdomain-validation).-->

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Subdomain den Status **[!UICONTROL Erfolg]**. Sie können jetzt damit Landingpage-Voreinstellungen erstellen.

   Beachten Sie, dass die Subdomain als **[!UICONTROL Fehlgeschlagen]** markiert wird, wenn Sie den Validierungseintrag in Ihrer Hosting-Lösung nicht erstellen können.

## Delegierung einer Subdomain aufheben {#undelegate-subdomain}

Wenn Sie die Delegierung einer Landingpage-Subdomain aufheben möchten, wenden Sie sich an den Adobe-Support.

Sie müssen jedoch mehrere Schritte in der Benutzeroberfläche ausführen, bevor Sie sich an Adobe wenden.

>[!NOTE]
>
>Die Delegierung von Subdomains kann nur mit dem Status **[!UICONTROL Erfolg]** aufgehoben werden. Subdomains mit dem Status **[!UICONTROL Entwurf]** und **[!UICONTROL Fehlgeschlagen]** können einfach aus der Benutzeroberfläche gelöscht werden.

Führen Sie zunächst die folgenden Schritte in [!DNL Journey Optimizer] aus:

1. Machen Sie die Veröffentlichung aller mit der Subdomain verknüpften Landingpages rückgängig. [Weitere Informationen](create-lp.md#access-landing-pages)

1. Deaktivieren Sie alle Kanalkonfigurationen, die mit der Subdomain verknüpft sind. [Weitere Informationen](../configuration/channel-surfaces.md#deactivate-a-surface)

<!--
1. If the landing page subdomain is using an email subdomain that was [already delegated](#lp-use-existing-subdomain) to Adobe, undelegate the email subdomain. [Learn how](../configuration/delegate-subdomain.md#undelegate-subdomain)

1. Stop the active campaigns associated with the subdomains. [Learn how](../campaigns/modify-stop-campaign.md#stop)

1. Stop the active journeys associated with the subdomains. [Learn how](../building-journeys/end-journey.md#stop-journey)
-->

Wenden Sie sich anschließend mit der Subdomain, deren Delegierung Sie aufheben möchten, an den Adobe-Support.

Nachdem Ihre Anfrage von Adobe verarbeitet wurde, wird die nicht delegierte Domain nicht mehr auf der Subdomain-Inventarseite angezeigt.

>[!CAUTION]
>
>Nachdem die Delegierung einer Subdomain aufgehoben wurde:
>
>   * Die Kanalkonfigurationen, die diese Subdomain verwendet haben, können nicht reaktiviert werden.
>
>   * Die exakte Subdomain kann nicht erneut über die Benutzeroberfläche delegiert werden. Wenden Sie sich in diesem Fall an Ihren Adobe-Support-Mitarbeiter.