---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen eines IP-Warmup-Plans
description: Erfahren Sie, wie Sie einen IP-Warmup-Plan erstellen
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, Pools, Gruppe, Subdomains, Zustellbarkeit
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 5%

---

# Erstellen eines IP-Warmup-Plans {#ip-warmup}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit IP-Wärme](ip-warmup-gs.md)
* [Erstellen von IP-Aufwärmekampagnen](ip-warmup-campaign.md)
* **[Erstellen eines IP-Warmup-Plans](ip-warmup-plan.md)**
* [IP-Warmup-Plan ausführen](ip-warmup-running.md)

>[!ENDSHADEBOX]

## IP-Warmlaufpläne aufrufen und verwalten {#manage-ip-warmup-plans}

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL IP-Aufwärmspläne]** Menü. Alle bisher erstellten IP-Warmup-Pläne werden angezeigt.

   ![](assets/ip-warmup-filter-list.png)

1. Sie können nach Status filtern. Die verschiedenen Status sind:

   * **Nicht gestartet**: Es wurde kein Lauf ausgeführt.
   * **Gestartet**: sobald ein Lauf gestartet wurde <!--or is done?-->
   * **Ausgesetzt**
   * **Abgeschlossen**: alle Abläufe im Plan durchgeführt werden.

1. Um einen IP-Aufwärmplan zu löschen, wählen Sie die **[!UICONTROL Löschen]** neben einem Listenelement klicken und den Löschvorgang bestätigen.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Der ausgewählte IP-Warmup-Plan wird endgültig gelöscht.

## Erstellen eines IP-Warmup-Plans {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Geben Sie Ihren IP-Warmup-Plan an"
>abstract="Laden Sie die CSV-Vorlage herunter und füllen Sie sie mit Daten für IP-Warmup-Phasen und die Zielanzahl der Profile aus."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Marketing-Oberfläche auswählen"
>abstract="Sie müssen dieselbe Oberfläche auswählen wie die in der Kampagne, die Sie mit Ihrem IP-Aufwärmplan verbinden möchten."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Einrichten von Kanaloberflächen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Erstellen von IP-Aufwärmekampagnen"

>[!CAUTION]
>
>Um die IP-Aufwärmspläne zu erstellen, zu bearbeiten und zu löschen, benötigen Sie die **[!UICONTROL Zustellbarkeitsberater]** -Berechtigung.
<!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

Wenn eine oder mehrere Live-Kampagnen mit **[!UICONTROL Aktivierung des IP-Warmlaufplans]** aktiviert sind, können Sie sie mit einem IP-Warmup-Plan verknüpfen.

>[!CAUTION]
>
>Wenden Sie sich an Ihren Zustellbarkeitsberater, um sicherzustellen, dass Ihre Vorlage für den IP-Warmup-Plan korrekt eingerichtet ist. <!--TBC-->

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL IP-Aufwärmspläne]** Menü und klicken Sie auf **[!UICONTROL IP-Warmup-Plan erstellen]**.

   ![](assets/ip-warmup-create-plan.png)

1. Füllen Sie die Details des IP-Warmup-Plans aus: Geben Sie ihm einen Namen und eine Beschreibung.

   ![](assets/ip-warmup-plan-details.png)

1. Wählen Sie eine [Oberfläche](channel-surfaces.md). Es stehen nur Marketingflächen zur Auswahl. [Weitere Informationen zum E-Mail-Typ](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >Sie müssen dieselbe Oberfläche auswählen wie die in der Kampagne, die Sie mit Ihrem IP-Aufwärmplan verbinden möchten. [Erfahren Sie, wie Sie eine IP-Warmup-Kampagne erstellen.](#create-ip-warmup-campaign)

1. Laden Sie die Excel-Datei hoch, die Ihren IP-Aufwärmplan enthält.<!--which formats are allowed?-->. Sie können die vom Zustellbarkeitsteam bereitgestellte Vorlage verwenden.<!--TBC?--> [Weitere Informationen](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Die Anzahl der Phasen, die in der hochgeladenen Datei definiert sind, wird automatisch angezeigt. [Weitere Informationen](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

### Einen IP-Warmup-Plan erneut hochladen {#re-upload-plan}

Sie können einen anderen IP-Warmup-Plan über die entsprechende Schaltfläche erneut hochladen.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>Die Details des IP-Warmup-Plans ändern sich entsprechend der neu hochgeladenen Datei. Die vollständigen Ausführungen und die aktivierten Ausführungen sind nicht betroffen.

### Hochladen der Datei mit dem Plan {#upload-plan}

Nachfolgend finden Sie ein Beispiel einer Datei mit einem IP-Warmup-Plan.

![](assets/ip-warmup-sample-file.png)

Jede Phase entspricht einem Zeitraum, der aus mehreren Ausführungen besteht und dem Sie eine Kampagne zuweisen.

Sie haben für jede Ausführung eine bestimmte Anzahl von Empfängern und legen fest, ab welchem Datum diese Ausführung ausgeführt werden soll.

Sie können für die Domänen, an die Sie eine Bereitstellung durchführen möchten, so viele Spalten wie gewünscht haben. In diesem Beispiel haben Sie drei Spalten: Gmail, Adobe und andere, was bedeutet, dass

Die Idee besteht darin, in den ersten Phasen mehr Abläufe zu haben, die Anzahl der Zieladressen schrittweise zu erhöhen und gleichzeitig die Anzahl der Ausführungen zu reduzieren.
