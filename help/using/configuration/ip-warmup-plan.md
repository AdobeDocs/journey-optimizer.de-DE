---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen eines IP-Aufwärmplans
description: Erfahren Sie, wie Sie einen IP-Aufwärmplan in Journey Optimizer erstellen.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: IP, Gruppe, Subdomains, Zustellbarkeit
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: 82c189545ab4f37a2e4b1044c0b8cfeb539aed13
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 97%

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

## Vorbereiten der Datei mit dem IP-Aufwärmplan {#prepare-file}

IP-Aufwärmen ist eine Aktivität, die darin besteht, die Anzahl der E-Mails, die von Ihren IPs und Ihrer Domain an die wichtigsten Internet-Dienstanbieter (ISPs) gesendet werden, schrittweise zu erhöhen, um Ihre Reputation als legitimer Absender zu etablieren.

Diese Aktivität wird in der Regel mithilfe von Zustellbarkeitsfachleuten durchgeführt, die bei der Erstellung eines gut durchdachten Plans auf der Basis von Branchen-Domains, Anwendungsfällen, Regionen, ISPs und verschiedenen anderen Faktoren helfen.

Wenn Sie mit der IP-Aufwärmfunktion in [!DNL Journey Optimizer] arbeiten, besteht dieser Plan aus einer Excel-Datei, die eine Reihe vordefinierter Spalten enthalten muss. Bevor Sie einen IP-Aufwärmplan in der Oberfläche von [!DNL Journey Optimizer] verwenden, müssen Sie diese Vorlage mit allen Daten ausfüllen, die in Ihren Plan gespeist werden.

>[!CAUTION]
>
>Arbeiten Sie mit der Person, die Sie im Hinblick auf die Zustellbarkeit berät, zusammen, um sicherzustellen, dass die Datei Ihres IP-Aufwärmplans korrekt eingerichtet ist.

Nachfolgend finden Sie ein Beispiel einer Datei mit einem IP-Aufwärmplan.

![](assets/ip-warmup-sample-file.png)

### Die Registerkarte „IP-Aufwärmplan“

* In diesem Beispiel wurde ein Plan (mit dem Titel „**Ausführungen**“) erstellt, der sich über einen Zeitraum von 17 Tagen erstreckt, um ein Zielvolumen von über 1 Million Profilen zu erreichen.

* Dieser Plan wird in 6 **Phasen** ausgeführt, die jeweils mindestens eine Ausführung enthalten.

* Sie können für die Domains, an die Sie versenden möchten, beliebig viele Spalten haben. In diesem Beispiel ist der Plan in 6 Spalten unterteilt: 5 davon entsprechen den **Haupt-Domain-Gruppen**, die in Ihrem Plan verwendet werden sollen (Gmail, Microsoft, Yahoo, Orange und Apple), und in der sechsten Spalte, **Sonstige**, sind alle verbleibenden Adressen aus anderen Domains enthalten.
* Die Spalte **Interaktion – Tage** zeigt an, dass nur die Profile angesprochen werden, die in den letzten 30 Tagen mit Ihrer Marke interagiert haben.

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

### Registerkarte „Benutzerdefinierte Domain-Gruppen“

Sie können Ihrem Plan auch weitere Spalten hinzufügen, indem Sie benutzerdefinierte Domain-Gruppen hinzufügen.

Verwenden Sie die Registerkarte **[!UICONTROL Benutzerdefinierte Domain-Gruppen]**, um eine neue Domain-Gruppe zu definieren. Für jede Domain können Sie alle von ihr abgedeckten Subdomains hinzufügen.<!--TBC-->

Zum Beispiel: Wenn Sie die benutzerdefinierte Domain „Luma“ hinzufügen, sollen die folgenden Subdomains eingeschlossen sein: luma.com, luma.co.uk, luma.it, luma.fr, luma.de usw.

![](assets/ip-warmup-sample-file-custom.png)

## Aufrufen und Verwalten von IP-Aufwärmplänen {#manage-ip-warmup-plans}

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL IP-Aufwärmpläne]** auf. Es werden alle bisher erstellten IP-Aufwärmpläne angezeigt.

   ![](assets/ip-warmup-filter-list.png)

1. Sie können nach dem Status filtern. Die verschiedenen Status sind:

   * **Nicht gestartet**: Es wurde noch keine Ausführung aktiviert. [Weitere Informationen](ip-warmup-execution.md#define-runs)
   * **Live**: Der Plan erhält diesen Status, sobald die erste Ausführung in der ersten Phase erfolgreich aktiviert wurde. [Weitere Informationen](ip-warmup-execution.md#define-runs)
   * **Abgeschlossen**: Der Plan wurde als abgeschlossen gekennzeichnet. Diese Option ist nur verfügbar, wenn alle im Plan ausgeführten Vorgänge in **[!UICONTROL Abgeschlossen]** oder **[!UICONTROL Entwurf]** status (kein Run kann ausgeführt werden) **[!UICONTROL Live]**). [Weitere Informationen](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Um einen IP-Aufwärmplan zu löschen, klicken Sie auf das Symbol **[!UICONTROL Löschen]** neben dem Namen eines Plans und bestätigen Sie den Löschvorgang.

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
>abstract="Sie müssen dieselbe Oberfläche auswählen wie die in der Kampagne ausgewählte Oberfläche, die Sie mit Ihrem IP-Aufwärmplan verbinden möchten."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Einrichten von Kanaloberflächen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Erstellen von IP-Aufwärmkampagnen"

Wenn eine oder mehrere Live-Kampagnen, bei denen die Option **[!UICONTROL Aktivierung des IP-Aufwärmplan]** aktiviert ist, können Sie sie mit einem IP-Aufwärmplan verknüpfen.

>[!CAUTION]
>
>Um die IP-Aufwärmpläne zu erstellen, zu bearbeiten und zu löschen, benötigen Sie die Berechtigung **[!UICONTROL Zustellbarkeitsberater]**. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL IP-Aufwärmpläne]** auf und klicken Sie dann auf **[!UICONTROL IP-Aufwärmplan erstellen]**.

   ![](assets/ip-warmup-create-plan.png)

1. Füllen Sie die Details des IP-Aufwärmplans aus: Geben Sie ihm einen Namen und eine Beschreibung.

   ![](assets/ip-warmup-plan-details.png)

1. Wählen Sie eine [Oberfläche](channel-surfaces.md) aus. Es stehen nur Marketing-Oberflächen zur Auswahl. [Weitere Informationen zum E-Mail-Typ](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >Sie müssen dieselbe Oberfläche auswählen wie die in der Kampagne ausgewählte Oberfläche, die Sie mit Ihrem IP-Aufwärmplan verbinden möchten. [Informationen zum Erstellen einer IP-Aufwärmkampagne](ip-warmup-campaign.md)

1. Laden Sie die Excel-Datei hoch, die Ihren IP-Aufwärmplan enthält. [Weitere Informationen](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Alle Phasen, Ausführungen, Spalten und deren Inhalt, die in der von Ihnen hochgeladenen Datei definiert sind, werden automatisch in der Oberfläche von [!DNL Journey Optimizer] angezeigt. [Weitere Informationen](ip-warmup-execution.md)

   ![](assets/ip-warmup-plan-uploaded.png)
