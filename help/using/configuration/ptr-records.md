---
title: PTR-Einträge
description: Erfahren Sie, wie Sie PTR-Einträge verwalten
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 5596c851b70cc38cd117793d492a15fd4ce175ef
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 80%

---

# PTR-Einträge {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="PTR-Datensätze der Subdomains"
>abstract="Ein Zeigerdatensatz (PTR) ist ein DNS-Record-Typ, der den mit einer IP-Adresse verknüpften Domänennamen bereitstellt, der den E-Mail-Servern beim Überprüfen der IP-Adressen der Absender hilft."

## Informationen zu PTR-Einträgen {#about-ptr-records}

Ein PTR (Pointer Record, „Zeigereintrag“) ist ein Typ von DNS (Domain Name System)-Eintrag, der den mit einer IP-Adresse verknüpften Domain-Namen bereitstellt.

Mit PTR-Datensätzen können Empfänger-E-Mail-Server die Authentizität der E-Mail-Server überprüfen, indem sie feststellen, ob ihre IP-Adressen den Namen entsprechen, mit denen die Server verbunden sind.

## Zugriff auf PTR-Einträge Ihrer Subdomains {#access-ptr-records}

Nachdem [eine Subdomain in Adobe Journey Optimizer zugewiesen wurde](delegate-subdomain.md), wird automatisch ein PTR-Eintrag erstellt und mit dieser Subdomain verknüpft. Sie können darauf über das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL PTR-Einträge]** zugreifen.

![](assets/ptr-records.png)

In der Liste werden die für jede zugewiesene Subdomain generierten PTR-Einträge anhand der unten stehenden Syntax angezeigt:

* „r“ für Eintrag (record),
* „xx“ für die beiden letzten Zahlen der IP-Adresse,
* Name der Subdomain.

Sie können einen PTR-Eintrag aus der Liste öffnen, um den zugehörigen Subdomain-Namen und die IP-Adresse anzuzeigen.

## Bearbeiten eines PTR-Eintrags {#edit-ptr-record}

Sie können einen PTR-Eintrag ändern, um die mit einer IP-Adresse verknüpfte Subdomain zu bearbeiten.

>[!CAUTION]
>
>Gehen Sie bei der Bearbeitung von PTR-Datensätzen mit größter Sorgfalt vor. Wenden Sie sich im Zweifel an einen Zustellbarkeitsexperten.<!--why?-->

>[!NOTE]
>
>Sie können die Felder **[!UICONTROL IP]** und **[!UICONTROL PTR-Eintrag]** nicht ändern.

### Vollständig delegierte Subdomains {#fully-delegated-subdomains}

Um einen PTR-Eintrag mit einer Subdomain zu bearbeiten, die [vollständig an Adobe delegiert](delegate-subdomain.md#full-subdomain-delegation) ist, führen Sie die folgenden Schritte aus.

1. Klicken Sie in der Liste auf den Namen eines PTR-Eintrags, um diesen zu öffnen.

   ![](assets/ptr-record-select.png)

1. Wählen Sie aus der Liste eine Subdomain aus, die [vollständig an Adobe delegiert](delegate-subdomain.md#full-subdomain-delegation) ist.

   ![](assets/ptr-record-subdomain.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre Änderungen zu speichern.

### Delegierte Subdomains mit der CNAME-Methode {#edit-ptr-subdomains-cname}

Führen Sie die folgenden Schritte aus, um einen PTR-Eintrag mit einer Subdomain zu bearbeiten, die mithilfe der [CNAME-Methode](delegate-subdomain.md#cname-subdomain-delegation) an Adobe delegiert ist.

1. Klicken Sie in der Liste auf den Namen eines PTR-Eintrags, um diesen zu öffnen.

   ![](assets/ptr-record-select-cname.png)

1. Wählen Sie in der Liste eine Subdomain aus, die mithilfe der [CNAME-Methode](delegate-subdomain.md#cname-subdomain-delegation) an Adobe delegiert wurde.

   ![](assets/ptr-record-subdomain-cname.png)

1. Sie müssen einen neuen Forward-DNS-Eintrag auf Ihrer Hosting-Plattform erstellen. Kopieren Sie dazu den von Adobe generierten Eintrag. Aktivieren Sie abschließend das Kontrollkästchen „Ich bestätige...“.

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >Falls Sie die Nachricht „Bitte erstellen Sie zunächst ein Forward-DNS und versuchen Sie es dann erneut“ erhalten, führen Sie die folgenden Schritte aus:
   >   * Überprüfen Sie beim DNS-Provider, ob der Forward-DNS-Eintrag erfolgreich erstellt wurde.
   >   * Einträge im DNS werden möglicherweise nicht sofort synchronisiert. Warten Sie einige Minuten und versuchen Sie es erneut.


1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre Änderungen zu speichern.

## Prüfen der Aktualisierungsdetails der PTR-Einträge {#check-ptr-record-update}

Nachdem Sie die Bearbeitung des PTR-Datensatzes bestätigt haben, wird die **[!UICONTROL Verarbeitung]** neben dem Namen des PTR-Datensatzes in der Liste angezeigt.

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>Die [Update-Verarbeitung](#processing) kann bis zu ein paar Stunden dauern.

Um die Details der PTR-Datensatz-Aktualisierung zu überprüfen, klicken Sie auf das Symbol daneben. Erfahren Sie mehr über die Status, die den verschiedenen Symbolen zugeordnet sind in [diesem Abschnitt](#ptr-record-update-statuses).

![](assets/ptr-record-recent-update.png)

Sie können Informationen wie den Aktualisierungsstatus und die gewünschten Änderungen sehen.

![](assets/ptr-record-updates.png)

## Aktualisierungsstatus von PTR-Einträgen {#ptr-record-update-statuses}

Die Aktualisierung eines PTR-Eintrags kann die folgenden Status haben:

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL In Bearbeitung]**: Die Aktualisierung des PTR-Eintrags wurde eingereicht und durchläuft einen Verifizierungsprozess.
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL Erfolgreich]**: Der aktualisierte PTR-Eintrag wurde überprüft und die neue Subdomain ist nun mit der IP-Adresse verknüpft.
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL Fehlgeschlagen]**: Bei der Verifizierung der Aktualisierung des PTR-Eintrags sind eine oder mehrere Prüfungen fehlgeschlagen.

### In Bearbeitung {#processing}

Es werden verschiedene Zustellbarkeitsprüfungen durchgeführt, um zu überprüfen, ob die neue Subdomain, die mit der IP-Adresse verknüpft werden soll, gültig ist. Dies kann bis zu ein paar Stunden dauern.

>[!NOTE]
>
>Sie können einen PTR-Eintrag nicht ändern, während die Aktualisierung in Bearbeitung ist. Sie können weiterhin auf den Namen klicken, aber das Feld **[!UICONTROL Subdomain]** ist ausgegraut. Die Änderungen werden erst dann übernommen, wenn die Aktualisierung erfolgreich war.

Während des Validierungsprozesses ist die alte Subdomain nach wie vor mit der IP-Adresse verknüpft.

### Erfolgreich {#success}

Wenn der Validierungsprozess erfolgreich war, wird die neue Subdomain automatisch mit der IP-Adresse verknüpft.

### Fehlgeschlagen {#failes}

Wenn der Validierungsprozess fehlschlägt, wird der ältere PTR-Eintrag angezeigt. Die gültige Subdomain, die zuvor mit der IP-Adresse verknüpft war, bleibt unverändert.

Folgende Arten von Fehlern sind bei der Aktualisierung möglich:
* Erstellung eines neuen Weiterleitungs-DNS für den PTR-Eintrag schlägt fehl
* Aktualisieren des Eintrags schlägt fehl
* Erneute Integration der Affinitäten schlägt fehl

Wenn die Aktualisierung fehlschlägt, kann der PTR-Eintrag wieder bearbeitet werden. Sie können auf den Namen klicken und die Subdomain erneut aktualisieren.
