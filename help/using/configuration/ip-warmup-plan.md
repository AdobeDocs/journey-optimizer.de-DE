---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen eines IP-Aufwärmplans
description: Erfahren Sie, wie Sie einen IP-Aufwärmplan in Journey Optimizer erstellen.
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, Gruppe, Subdomains, Zustellbarkeit
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: eb4a4929de17f0b57216f69e00da6314f7b59b07
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 53%

---

# Erstellen eines IP-Aufwärmplans {#ip-warmup}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit IP-Aufwärmen](ip-warmup-gs.md)
* [Erstellen von IP-Aufwärmkampagnen](ip-warmup-campaign.md)
* **[Erstellen eines IP-Aufwärmplans](ip-warmup-plan.md)**
* [Ausführen des IP-Aufwärmplans](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Nachdem Sie eine oder mehrere [IP-Aufwärmkampagnen](ip-warmup-campaign.md) mit einer dedizierten Oberfläche und der entsprechenden Option erstellt haben, können Sie mit der Erstellung Ihres IP-Aufwärmplans beginnen.

>[!CAUTION]
>
>Um auf die IP-Aufwärmspläne zugreifen, sie erstellen, bearbeiten und löschen zu können, benötigen Sie die **[!UICONTROL Zustellbarkeitsberater]** -Berechtigung. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

## Vorbereiten der Datei mit dem IP-Aufwärmplan {#prepare-file}

IP-Aufwärmen ist eine Aktivität, die darin besteht, die Anzahl der E-Mails, die von Ihren IPs und Ihrer Domain an die wichtigsten Internet-Dienstanbieter (ISPs) gesendet werden, schrittweise zu erhöhen, um Ihre Reputation als legitimer Absender zu etablieren.

Diese Aktivität wird in der Regel mithilfe von Zustellbarkeitsfachleuten durchgeführt, die bei der Erstellung eines gut durchdachten Plans auf der Basis von Branchen-Domains, Anwendungsfällen, Regionen, ISPs und verschiedenen anderen Faktoren helfen.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Bevor Sie einen IP-Warmup-Plan im [!DNL Journey Optimizer] müssen Sie eine Excel-Vorlage mit allen Daten ausfüllen, die für Ihren Plan bestimmt sind.

>[!CAUTION]
>
>Arbeiten Sie mit der Person, die Sie im Hinblick auf die Zustellbarkeit berät, zusammen, um sicherzustellen, dass die Datei Ihres IP-Aufwärmplans korrekt eingerichtet ist.
>
>Achten Sie darauf, das in der Vorlage angegebene Format zu verwenden.

Nachfolgend finden Sie ein Beispiel einer Datei mit einem IP-Aufwärmplan.

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>Vorerst sollten Sie die **Eigenschaften** und **Wert** unberührt.

### Die Registerkarte „IP-Aufwärmplan“ {#ip-warmup-plan-tab}

* In diesem Beispiel wurde ein Plan über einen Zeitraum von 17 Tagen erstellt (mit der Bezeichnung **läutet**&quot;) , um ein Zielvolumen von über einer Million Profilen zu erreichen.

* Diese geplante Maßnahme wird über sechs Jahre durchgeführt **Phasen**, die jeweils mindestens eine Ausführung enthalten.

* Sie können für die Domains, an die Sie versenden möchten, beliebig viele Spalten haben. In diesem Beispiel ist der Plan in sechs Spalten unterteilt:

   * Vier davon entsprechen **vordefinierte Domänengruppen** zur Verwendung in Ihrem Plan (Gmail, Microsoft, Yahoo und Orange).
   * Eine entspricht einer benutzerspezifischen Domain-Gruppe (die Sie mithilfe der [Benutzerspezifische Domänengruppe](#custom-domain-group-tab) Registerkarte).
   * sechste Spalte, **sonstige** enthält alle verbleibenden Adressen aus anderen Domänen, die nicht explizit im Plan behandelt werden. Diese Spalte ist optional: Wenn keine E-Mails gesendet werden, werden nur die angegebenen Domains angezeigt.
* Die **Interaktionstage** zeigt an, dass nur die Profile angesprochen werden, die während des letzten Zeitraums mit Ihrer Marke interagiert haben.

Die Idee besteht darin, die Anzahl der Zieladressen in jeder Ausführung schrittweise zu erhöhen und gleichzeitig die Anzahl der Ausführungen in jeder Phase zu reduzieren.

Die nativen Haupt-Domain-Gruppen, die Sie Ihrem Plan hinzufügen können, sind hier aufgeführt:

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Orange
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple

<!--
+++ Gmail
gmail.com;gmail.fr;gmail.de;gmail.co.uk;gmail.it
+++

+++ Adobe
adobe.com;adobe.fr;adobe.es
+++

+++WP
+++

+++Comcast
+++

+++Yahoo
+++

+++Bigpond
+++

+++Orange
+++

+++Softbank
+++

+++Docomo
+++

+++United Internet
+++

+++Microsoft
+++

+++KDDI
+++

+++Italia Online
+++

+++La Poste
+++
-->

### Registerkarte „Benutzerdefinierte Domain-Gruppen“ {#custom-domain-group-tab}

Sie können Ihrem Plan auch weitere Spalten hinzufügen, indem Sie benutzerdefinierte Domain-Gruppen hinzufügen.

Verwenden Sie die Registerkarte **[!UICONTROL Benutzerdefinierte Domain-Gruppen]**, um eine neue Domain-Gruppe zu definieren. Für jede Domain können Sie alle von ihr abgedeckten Subdomains hinzufügen.<!--TBC-->

Zum Beispiel: Wenn Sie die benutzerdefinierte Domain „Luma“ hinzufügen, sollen die folgenden Subdomains eingeschlossen sein: luma.com, luma.co.uk, luma.it, luma.fr, luma.de usw.

![](assets/ip-warmup-sample-file-custom.png)

### Beispiel {#example}

Angenommen, Sie möchten zwei benutzerdefinierte Domänengruppen haben:

* Nur eine für Hotmail-Domänen.
* Eine für alle anderen Domänen aus der Domain-Gruppe Microsoft (also ohne alle Hotmail-Domänen).

Beachten Sie, dass alle anderen Domänen im **[!UICONTROL sonstige]** Spalte.

1. Im **[!UICONTROL Benutzerspezifische Domänengruppe]** erstellen Sie die **Hotmail** Domänengruppe.

1. Fügen Sie alle Hotmail-Domänen in derselben Zeile hinzu.

   Sie können [Kopieren und Einfügen](#copy-paste) alle Hotmail-Domänen, die im [Registerkarte &quot;IP-Warmup-Plan&quot;](#ip-warmup-plan-tab) Abschnitt.

1. Fügen Sie eine weitere Zeile hinzu.

1. Erstellen Sie die **Microsoft_X** Domänengruppe.

1. Fügen Sie alle Microsoft-Domänen, die nicht Hotmail sind, in derselben Zeile hinzu. Auf ähnliche Weise können Sie sie aus der obigen Liste kopieren und einfügen. [Weitere Informationen](#copy-paste)

1. Gehen Sie zurück zu **[!UICONTROL IP-Warmup-Plan]** Registerkarte.

1. Erstellen Sie drei Spalten: eine für **Hotmail**, einer für **Microsoft_X** und eines für **sonstige**.

1. Füllen Sie die Spalten nach Bedarf aus.

>[!NOTE]
>
>Sobald der IP-Warmup-Plan in hochgeladen wurde [!DNL Journey Optimizer]müssen Sie die Microsoft-Domänengruppen nicht ausschließen.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### Standarddomänen kopieren und einfügen {#copy-paste}

Wenn Sie beispielsweise eine benutzerdefinierte Domain-Gruppe erstellen möchten, die alle Hotmail-Domänen enthält, können Sie die Domänen aus der angegebenen Standardliste kopieren und einfügen [above](#ip-warmup-plan-tab).

Verwenden Sie dann das Excel-Konvertierungstool, um Text in Spalten zu konvertieren:

1. Auswählen **[!UICONTROL Daten]** > **[!UICONTROL Text in Spalten...]** auswählen **[!UICONTROL Getrennt]** und wählen **[!UICONTROL Nächste]**.

1. Auswählen **[!UICONTROL Semikolon]** klicken **[!UICONTROL Nächste]** und **[!UICONTROL Beenden]**.

Jede Domäne wird nun in einer anderen Spalte in derselben Zeile angezeigt.

## Aufrufen und Verwalten von IP-Aufwärmplänen {#manage-ip-warmup-plans}

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL IP-Aufwärmpläne]** auf. Es werden alle bisher erstellten IP-Aufwärmpläne angezeigt.

   ![](assets/ip-warmup-filter-list.png)

1. Sie können nach dem Status filtern. Die verschiedenen Status sind:

   * **Nicht gestartet**: Es wurde noch keine Ausführung aktiviert. [Weitere Informationen](ip-warmup-execution.md#define-runs)
   * **Live**: Der Plan erhält diesen Status, sobald die erste Ausführung in der ersten Phase erfolgreich aktiviert wurde. [Weitere Informationen](ip-warmup-execution.md#define-runs)
   * **Abgeschlossen**: Der Plan wurde als abgeschlossen gekennzeichnet. <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [Weitere Informationen](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Um einen IP-Aufwärmplan zu löschen, klicken Sie auf das Symbol **[!UICONTROL Löschen]** neben dem Namen eines Plans und bestätigen Sie den Löschvorgang.

   >[!NOTE]
   >
   >Nur Pläne mit **Nicht gestartet** -Status gelöscht werden.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Der ausgewählte IP-Aufwärmplan wird endgültig gelöscht.

## Erstellen eines IP-Aufwärmplans {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Angeben Ihres IP-Aufwärmplans"
>abstract="Laden Sie die CSV-Vorlage herunter und füllen Sie sie mit Daten für IP-Aufwärmphasen und die Zielanzahl der Profile aus."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Auswählen einer Marketing-Oberfläche"
>abstract="Es muss dieselbe Oberfläche ausgewählt werden wie die in der Kampagne, die mit Ihrem IP-Aufwärmplan verbunden werden soll. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Einrichten von Kanaloberflächen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Erstellen von IP-Aufwärmkampagnen"

Gehen Sie wie folgt vor, um einen IP-Warmup-Plan zu erstellen.

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL IP-Aufwärmpläne]** auf und klicken Sie dann auf **[!UICONTROL IP-Aufwärmplan erstellen]**.

   ![](assets/ip-warmup-create-plan.png)

1. Füllen Sie die Details des IP-Aufwärmplans aus: Geben Sie ihm einen Namen und eine Beschreibung.

   ![](assets/ip-warmup-plan-details.png)

1. Wählen Sie die [Oberfläche](channel-surfaces.md) dass du dich aufwärmen willst. Es stehen nur Marketing-Oberflächen zur Auswahl. [Weitere Informationen zum E-Mail-Typ](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >Die Kampagnen, die Sie mit Ihrem IP-Warmup-Plan verbinden möchten, müssen dieselbe Oberfläche verwenden. [Informationen zum Erstellen einer IP-Aufwärmkampagne](ip-warmup-campaign.md)

1. Laden Sie die Excel-Datei hoch, die Ihren IP-Aufwärmplan enthält. [Weitere Informationen](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >Wenn der Upload fehlschlägt, stellen Sie sicher, dass Sie die richtige Formatierung und das richtige Dateiformat (.xls oder .xlsx) verwenden. Verwenden Sie das von Adobe bereitgestellte Beispiel.

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Alle Phasen, Ausführungen, Spalten und deren Inhalt, die in der von Ihnen hochgeladenen Datei definiert sind, werden automatisch in der Oberfläche von [!DNL Journey Optimizer] angezeigt.

   ![](assets/ip-warmup-plan-uploaded.png)

Jetzt können Sie Ihren IP-Warmup-Plan ausführen. [Weitere Informationen](ip-warmup-execution.md)
