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
ht-degree: 100%

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
>Um die IP-Aufwärmpläne einzusehen, zu bearbeiten und zu löschen, benötigen Sie die Berechtigung **[!UICONTROL Zustellbarkeitsberater]**. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

## Vorbereiten der Datei mit dem IP-Aufwärmplan {#prepare-file}

IP-Aufwärmen ist eine Aktivität, die darin besteht, die Anzahl der E-Mails, die von Ihren IPs und Ihrer Domain an die wichtigsten Internet-Dienstanbieter (ISPs) gesendet werden, schrittweise zu erhöhen, um Ihre Reputation als legitimer Absender zu etablieren.

Diese Aktivität wird in der Regel mithilfe von Zustellbarkeitsfachleuten durchgeführt, die bei der Erstellung eines gut durchdachten Plans auf der Basis von Branchen-Domains, Anwendungsfällen, Regionen, ISPs und verschiedenen anderen Faktoren helfen.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Bevor Sie einen IP-Aufwärmplan in der Oberfläche von [!DNL Journey Optimizer] verwenden, müssen Sie eine Excel-Vorlage mit allen Daten ausfüllen, die in Ihren Plan gespeist werden.

>[!CAUTION]
>
>Arbeiten Sie mit der Person, die Sie im Hinblick auf die Zustellbarkeit berät, zusammen, um sicherzustellen, dass die Datei Ihres IP-Aufwärmplans korrekt eingerichtet ist.
>
>Achten Sie darauf, das in der Vorlage angegebene Format zu verwenden.

Nachfolgend finden Sie ein Beispiel einer Datei mit einem IP-Aufwärmplan.

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>Vorläufig sollten Sie die Zellen **Eigenschaften** und **Wert** unangetastet lassen.

### Registerkarte „IP-Aufwärmplan“ {#ip-warmup-plan-tab}

* In diesem Beispiel wurde ein Plan (mit dem Titel „**Ausführungen**“) erstellt, der sich über einen Zeitraum von 17 Tagen erstreckt, um ein Zielvolumen von über einer Million Profilen zu erreichen.

* Dieser Plan wird in 6 **Phasen** ausgeführt, die jeweils mindestens eine Ausführung enthalten.

* Sie können für die Domains, an die Sie versenden möchten, beliebig viele Spalten haben. In diesem Beispiel ist der Plan in sechs Spalten unterteilt:

   * Vier davon entsprechen **vordefinierten Domain-Gruppen** zur Verwendung in Ihrem Plan (Gmail, Microsoft, Yahoo und Orange).
   * Eine entspricht einer benutzerspezifischen Domain-Gruppe (die Sie mithilfe der Registerkarte [Benutzerspezifische Domain-Gruppe](#custom-domain-group-tab) hinzufügen müssen).
   * Die sechste Spalte, **Sonstige**, enthält alle verbleibenden Adressen aus anderen Domains, die nicht explizit im Plan behandelt werden. Diese Spalte ist optional: Wenn sie weggelassen wird, werden E-Mails nur an die angegebenen Domains gesendet.
* Die Spalte **Interaktion – Tage** zeigt an, dass nur die Profile angesprochen werden, die im letzten eingegebenen Zeitraum mit Ihrer Marke interagiert haben.

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

Angenommen, Sie möchten zwei benutzerdefinierte Domain-Gruppen haben:

* Eine nur für Hotmail-Domains.
* Und eine für alle anderen Domains aus der Domain-Gruppe Microsoft (also ohne alle Hotmail-Domains).

Beachten Sie, dass alle anderen Domains in der Spalte **[!UICONTROL Sonstige]** erfasst werden.

1. Erstellen Sie in der Registerkarte **[!UICONTROL Benutzerdefinierte Domain-Gruppen]**, eine **Hotmail**-Domain-Gruppe.

1. Fügen Sie alle Hotmail-Domains in derselben Zeile hinzu.

   Sie können alle Hotmail-Domains [kopieren und einfügen](#copy-paste), die im Abschnitt [Registerkarte „IP-Aufwärmplan“](#ip-warmup-plan-tab) aufgeführt sind.

1. Fügen Sie eine weitere Zeile hinzu.

1. Erstellen Sie eine Domain-Gruppe namens **Microsoft_X**.

1. Fügen Sie alle Microsoft-Domains, die nicht Hotmail sind, in derselben Zeile hinzu. Auf ähnliche Weise können Sie sie aus der obigen Liste kopieren und einfügen. [Weitere Informationen](#copy-paste)

1. Gehen Sie zurück zur Registerkarte **[!UICONTROL IP-Aufwärmplan]**.

1. Erstellen Sie drei Spalten: eine für **Hotmail**, eine für **Microsoft_X** und eine für **Sonstige**.

1. Füllen Sie die Spalten entsprechend Ihren Anforderungen aus.

>[!NOTE]
>
>Sobald der IP-Aufwärmplan in [!DNL Journey Optimizer] hochgeladen wurde, müssen Sie die Microsoft Domain-Gruppen nicht ausschließen.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### Kopieren und Einfügen der Standard-Domains {#copy-paste}

Wenn Sie beispielsweise eine benutzerdefinierte Domain-Gruppe erstellen möchten, die alle Hotmail-Domains enthält, können Sie die Domains aus der [oben](#ip-warmup-plan-tab) angegebenen Standardliste kopieren und einfügen.

Verwenden Sie dann das Excel-Konvertierungswerkzeug, um Text in Spalten zu konvertieren:

1. Wählen Sie **[!UICONTROL Daten]** > **[!UICONTROL Text in Spalten…]** und dann **[!UICONTROL Getrennt]** aus und klicken Sie abschließend auf **[!UICONTROL Weiter]**.

1. Wählen Sie **[!UICONTROL Semikolon]** aus und klicken Sie dann auf **[!UICONTROL Weiter]** und **[!UICONTROL Beenden]**.

Jede Domain wird nun in einer anderen Spalte in derselben Zeile angezeigt.

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
   >Nur Pläne mit dem Status **Nicht gestartet** können gelöscht werden.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Der ausgewählte IP-Aufwärmplan wird endgültig gelöscht.

## Erstellen eines IP-Aufwärmplans {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="IP-Aufwärmplan angeben"
>abstract="Die CSV-Vorlage herunterladen und sie mit Daten für IP-Aufwärmphasen und die Zielanzahl der Profile ausfüllen."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Auswählen einer Marketing-Oberfläche"
>abstract="Es muss dieselbe Oberfläche ausgewählt werden wie die in der Kampagne, die mit Ihrem IP-Aufwärmplan verbunden werden soll. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Einrichten von Kanaloberflächen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Erstellen von IP-Aufwärmkampagnen"

Um einen IP-Aufwärmplan zu erstellen, führen Sie die folgenden Schritte aus.

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL IP-Aufwärmpläne]** auf und klicken Sie dann auf **[!UICONTROL IP-Aufwärmplan erstellen]**.

   ![](assets/ip-warmup-create-plan.png)

1. Füllen Sie die Details des IP-Aufwärmplans aus: Geben Sie ihm einen Namen und eine Beschreibung.

   ![](assets/ip-warmup-plan-details.png)

1. Wählen Sie die [Oberfläche](channel-surfaces.md) aus, die Sie aufwärmen möchten. Es stehen nur Marketing-Oberflächen zur Auswahl. [Weitere Informationen zum E-Mail-Typ](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >Die Kampagnen, die Sie mit Ihrem IP-Aufwärmplan verbinden möchten, müssen dieselbe Oberfläche verwenden. [Informationen zum Erstellen einer IP-Aufwärmkampagne](ip-warmup-campaign.md)

1. Laden Sie die Excel-Datei hoch, die Ihren IP-Aufwärmplan enthält. [Weitere Informationen](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >Wenn der Upload fehlschlägt, stellen Sie sicher, dass Sie die richtige Formatierung und das richtige Dateiformat (XLS oder XLSX) verwenden. Verwenden Sie das von Adobe bereitgestellte Beispiel.

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Alle Phasen, Ausführungen, Spalten und deren Inhalte, die in der von Ihnen hochgeladenen Datei definiert sind, werden automatisch in der Oberfläche von [!DNL Journey Optimizer] angezeigt.

   ![](assets/ip-warmup-plan-uploaded.png)

Jetzt können Sie Ihren IP-Aufwärmplan ausführen. [Weitere Informationen](ip-warmup-execution.md)
