---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen von kontextuellen Attributen zu veröffentlichten Fragmenten
description: Erfahren Sie, wie Sie veröffentlichte Fragmente kontextuelle Attribute hinzufügen (eingeschränkte Verfügbarkeit)
feature: Fragments
topic: Content Management
role: User
level: Intermediate, Experienced
hide: true
exl-id: a274656e-2570-4a9c-b72b-4e8e920b7462
TQID: https://experienceleague.adobe.com/yweu8QtcWU42ZI2z93vIf5-LUGP7pQ16bJUQnmDKNGY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 4bae03291d44603ab1648416f34dd1a8b414a07a
workflow-type: tm+mt
source-wordcount: 363
ht-degree: 8%

---

# Hinzufügen von kontextuellen Attributen zu veröffentlichten Fragmenten {#adding-contextual-attributes}

>[!AVAILABILITY]
>
>Diese Funktion steht nur ausgewählten Kunden zur Verfügung und birgt erhebliche Risiken. Vergewissern Sie sich bei Ihrem Adobe-Support-Mitarbeiter, dass diese Funktion für Ihr Unternehmen aktiviert ist.

Standardmäßig wird das Hinzufügen neuer [Personalisierungsattribute](../personalization/personalization-build-expressions.md) zu einem veröffentlichten Fragment nicht unterstützt. Nach der Veröffentlichung eines Fragments wird der Satz von Profil- oder Kontextattributen für alle Kampagnen und Journey gesperrt.

Bei ausgewählten Kunden ist es jedoch möglich, **kontextuelle Attribute** nur veröffentlichten Fragmenten hinzuzufügen.

>[!WARNING]
>
>Beim Hinzufügen von Personalisierungsattributen zu einem veröffentlichten Fragment ist der Validierungsprozess weniger streng und es werden möglicherweise keine Fehler erkannt. Dies könnte unbeabsichtigte Brüche in allen Journey und Kampagnen verursachen, die dieses Fragment im benötigten Umfang verwenden.

## Leitlinien und Einschränkungen {#limitations}

* Stellen Sie sicher, dass alle Journey und Kampagnen, die das Fragment derzeit verwenden, die neuen Kontexteigenschaften verarbeiten können.
* Profilattribute können nicht zu veröffentlichten Fragmenten hinzugefügt werden. Es werden nur kontextuelle Attribute unterstützt.
* Kontextuelle Attribute müssen manuell in den Code-Editor eingegeben werden - sie können nicht in der Benutzeroberfläche des Personalisierungseditors ausgewählt werden.
* Beim Hinzufügen personalisierter Attribute zu Live-Fragmenten werden die Validierungen gelockert, was bedeutet, dass Fehler möglicherweise nicht erkannt werden und unbeabsichtigte Brüche im großen Maßstab verursachen können.
* Nach der Veröffentlichung wirken sich Fehler sofort auf alle Kommunikationen aus, die dieses Fragment verwenden.

## Hinzufügen von Kontextattributen {#add-contextual-attributes}

Gehen Sie wie folgt vor, um einem veröffentlichten Fragment kontextuelle Attribute hinzuzufügen.

>[!IMPORTANT]
>
>Fahren Sie nur fort, wenn Sie [ Auswirkungen auf Journey und Kampagnen, ](#limitations) auf das Fragment verweisen, vollständig verstehen.

1. Navigieren Sie **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]**.

1. Wählen Sie das veröffentlichte Fragment aus und klicken Sie auf **[!UICONTROL Ändern]**, um eine Entwurfsversion zu erstellen.

   ![](assets/fragment-live-modify.png){width="70%"}

1. Klicken Sie **[!UICONTROL Bearbeiten]**, um den Inhaltsfragment-Editor zu öffnen.

1. Wechseln Sie **[!UICONTROL Personalisierungseditor]** den **[!UICONTROL Erweiterter Modus]**.

1. Geben Sie das kontextuelle Attribut manuell ein (kopieren Sie es) oder fügen Sie es mithilfe der `{{context.attribute_name}}` ein:

   Beispiel für ein `promotionCode`:

   ```
   {{context.promotionCode}}
   ```

   >[!CAUTION]
   >
   >Überprüfen Sie den Attributpfad auf Genauigkeit. Fehler werden möglicherweise nicht erkannt und können die Journey- oder Kampagnenkommunikation in großem Umfang stören.

1. Speichern Sie Ihre Änderungen.

1. Klicken Sie nach der Bestätigung auf **[!UICONTROL Veröffentlichen]**, um Ihre Änderungen live zu schalten.

>[!NOTE]
>Um unbeabsichtigte Brüche zwischen Journey und Kampagnen zu vermeiden, können Sie die kontextuellen Attributpfade in einer Nicht-Produktionsumgebung testen.

## Verwandte Themen {#related-topics}

* [Verwalten von Fragmenten](manage-fragments.md)
* [Bearbeiten eines Fragments](manage-fragments.md#edit-fragments)
* [Durch API ausgelöste Kampagnen](../campaigns/api-triggered-campaigns.md)
* [Personalisierungssyntax](../personalization/personalization-syntax.md)
