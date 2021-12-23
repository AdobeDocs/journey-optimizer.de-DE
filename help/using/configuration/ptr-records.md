---
title: PTR-Einträge
description: Erfahren Sie, wie Sie PTR-Einträge verwalten
audience: administrators
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 6c200f4a162ea1a3763b353b01ce5fef74ed8462
workflow-type: ht
source-wordcount: '479'
ht-degree: 100%

---

# PTR-Einträge

## Informationen zu PTR-Einträgen

Ein PTR (Pointer Record, „Zeigereintrag“) ist ein Typ von DNS (Domain Name System)-Eintrag, der den mit einer IP-Adresse verknüpften Domain-Namen bereitstellt.

Mit PTR-Einträgen können Empfänger-E-Mail-Server die Authentizität der Sender-E-Mail-Server überprüfen, indem sie feststellen, ob ihre IP-Adressen mit den Namen übereinstimmen, mit denen sich die Server verbinden.

## Zugriff auf PTR-Einträge Ihrer Subdomains

Nachdem [eine Subdomain in Adobe Journey Optimizer zugewiesen wurde](delegate-subdomain.md), wird automatisch ein PTR-Eintrag erstellt und mit dieser Subdomain verknüpft. Sie können darauf über das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL PTR-Einträge]** zugreifen.

![](../assets/ptr-records.png)

In der Liste werden die für jede zugewiesene Subdomain generierten PTR-Einträge anhand der unten stehenden Syntax angezeigt:

* „r“ für Eintrag (record),
* „xx“ für die beiden letzten Zahlen der IP-Adresse,
* Name der Subdomain.

Sie können einen PTR-Eintrag aus der Liste öffnen, um den zugehörigen Subdomain-Namen und die IP-Adresse anzuzeigen.

## Bearbeiten eines PTR-Eintrags {#edit-ptr-record}

Sie können einen PTR-Eintrag ändern, um die mit einer IP-Adresse verknüpfte Subdomain zu bearbeiten.

>[!CAUTION]
>
>Sie können keinen PTR-Eintrag ändern, der einer Subdomain zugeordnet ist, die Adobe mit der [CNAME-Methode](delegate-subdomain.md#cname-subdomain-delegation) zugewiesen wurde.

1. Klicken Sie in der Liste auf den Namen eines PTR-Eintrags, um diesen zu öffnen.

   ![](../assets/ptr-record-select.png)

1. Bearbeiten Sie die Subdomain nach Bedarf.

   ![](../assets/ptr-record-subdomain.png)

   >[!NOTE]
   >
   >Sie können die Felder **[!UICONTROL IP]** und **[!UICONTROL PTR-Eintrag]** nicht ändern.

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre Änderungen zu speichern.

Neben dem Namen des PTR-Eintrags in der Liste wird das Symbol **[!UICONTROL Wird aktualisiert]** angezeigt.

![](../assets/ptr-record-updating.png)

Um sich die Details der PTR-Eintragsaktualisierung anzusehen, klicken Sie auf das Symbol **[!UICONTROL Wird aktualisiert]** oder **[!UICONTROL Letzte Aktualisierungen]**.

![](../assets/ptr-record-recent-update.png)

Sie können Informationen wie den Aktualisierungsstatus und die gewünschten Änderungen sehen.

![](../assets/ptr-record-updates.png)

## Aktualisieren des Status

Die Aktualisierung eines PTR-Eintrags kann die folgenden Status haben:

* **[!UICONTROL In Bearbeitung]**: Die Aktualisierung des PTR-Eintrags wurde eingereicht und durchläuft einen Verifizierungsprozess.
* **[!UICONTROL Erfolgreich]**: Der aktualisierte PTR-Eintrag wurde überprüft und die neue Subdomain ist nun mit der IP-Adresse verknüpft.
* **[!UICONTROL Fehlgeschlagen]**: Bei der Verifizierung der Aktualisierung des PTR-Eintrags sind eine oder mehrere Prüfungen fehlgeschlagen.

### In Bearbeitung

Es werden verschiedene Zustellbarkeitsprüfungen durchgeführt, um zu überprüfen, ob die neue Subdomain, die mit der IP-Adresse verknüpft werden soll, gültig ist. <!--The processing time is around **48h-72h**, and can take up to **7-10 days**. Learn more on the checks performed during the validation cycle in [this section](#create-message-preset).-->

>[!NOTE]
>
>Sie können einen PTR-Eintrag nicht ändern, während die Aktualisierung in Bearbeitung ist. Sie können weiterhin auf den Namen klicken, aber das Feld **[!UICONTROL Subdomain]** ist ausgegraut. Die Änderungen werden erst dann übernommen, wenn die Aktualisierung erfolgreich war.

Während des Validierungsprozesses ist die alte Subdomain nach wie vor mit der IP-Adresse verknüpft.

### Erfolgreich

Wenn der Validierungsprozess erfolgreich war, wird die neue Subdomain automatisch mit der IP-Adresse verknüpft.

### Fehlgeschlagen

Wenn der Validierungsprozess fehlschlägt, wird der ältere PTR-Eintrag angezeigt. Die gültige Subdomain, die zuvor mit der IP-Adresse verknüpft war, bleibt unverändert.

Folgende Arten von Fehlern sind bei der Aktualisierung möglich:
* Erstellung eines neuen Weiterleitungs-DNS für den PTR-Eintrag schlägt fehl
* Aktualisieren des Eintrags schlägt fehl
* Erneute Integration der Affinitäten schlägt fehl

Wenn die Aktualisierung fehlschlägt, kann der PTR-Eintrag wieder bearbeitet werden. Sie können auf den Namen klicken und die Subdomain erneut aktualisieren.
