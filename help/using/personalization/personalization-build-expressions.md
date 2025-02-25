---
solution: Journey Optimizer
product: journey optimizer
title: Über den Personalisierungseditor
description: Erfahren Sie, wie Sie mit dem Personalisierungseditor arbeiten.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor, Über, Start
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 19d33bf2d455aaca3fd0e961bebe5dd1d1f5b32c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 93%

---

# Erste Schritte mit dem Personalisierungseditor {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Über den Personalisierungseditor"
>abstract="Mit dem Personalisierungseditor können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen."

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Automatisch vervollständigen"
>abstract="Wenn Sie diese Option aktivieren, kann das System Ihren Code automatisch vervollständigen und Vorschläge unterbreiten, während Sie Ihren Ausdruck eingeben. Diese Option ist nur für HTML- und Textformate verfügbar."

Der Personalisierungseditor ist die Kernkomponente der Personalisierung in [!DNL Journey Optimizer]. Er ist in jedem Kontext verfügbar, in dem Sie eine Personalisierung definieren müssen, wie z. B. E-Mails, Push-Benachrichtigungen und Angebote.

In der Benutzeroberfläche des Personalisierungseditors können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen.

![](assets/perso_ee1.png)

## Verfügbare Personalisierungsquellen {#sources}

Im linken Bildschirmbereich wird ein Domain-Selektor angezeigt, mit dem Sie die Quelle für die Personalisierung auswählen können. Verfügbare Quellen sind:

* **[!UICONTROL Profilattribute]**: Listet alle Verweise auf, die mit dem Profilschema verknüpft sind, das in der [Dokumentation des Adobe Experience Platform-Datenmodells (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"} beschrieben wird.
* **[!UICONTROL Zielgruppen]**: Listet alle im Segmentierungs-Service von Adobe Experience Platform erstellten Zielgruppen auf. Weitere Informationen zur Segmentierung finden Sie [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de){target="_blank"}.
* **[!UICONTROL Angebotsentscheidungen]**: Listet alle Angebote auf, die mit einer bestimmten Platzierung verbunden sind. Wählen Sie die Platzierung aus und fügen Sie dann die Angebote in den Inhalt ein. Eine vollständige Dokumentation zum Verwalten von Angeboten finden Sie in [diesem Abschnitt](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Kontextattribute]**: Wenn eine Kanalaktionsaktivität (E-Mail, Push, SMS) in einer Journey oder Kampagne verwendet wird, stehen für die Personalisierung Kontextattribute im Zusammenhang mit Ereignissen und Eigenschaften zur Verfügung. Ein Beispiel für die Personalisierung mit kontextuellen Attributen finden Sie in [diesem Abschnitt](personalization-use-case.md).
* **[!UICONTROL Hilfsfunktionen]**: listet alle Hilfsfunktionen auf, die für die Durchführung von Datenoperationen wie Berechnungen, Datenformatierungen oder -konvertierungen, Bedingungen und die Bearbeitung von Daten im Rahmen der Personalisierung verfügbar sind. Weiterführende Informationen finden Sie in [diesem Abschnitt](functions/functions.md).

## Hinzufügen von Personalisierungsattributen {#add}

Klicken Sie auf die Schaltfläche „+“, um Ihrem Personalisierungsausdruck ein Attribut hinzuzufügen.

Über das Menü mit den Auslassungspunkten neben dem Symbol „+“ können Sie weitere Details für jede Variable abrufen und Ihre am häufigsten verwendeten Attribute zu den Favoriten hinzufügen. [Erfahren Sie, wie Sie Attribute zu den Favoriten hinzufügen können](personalization-favorites.md)

>[!NOTE]
>
>Beim Targeting einer Zielgruppe mit Anreicherungsattributen, die mithilfe eines Kompositions-Workflows generiert wurden, können Sie diese Anreicherungsattribute nutzen, um Ihre Nachricht zu personalisieren. [Erfahren Sie, wie Sie Zielgruppen-Anreicherungsattribute verwenden.](../audience/about-audiences.md#enrichment)

Darüber hinaus können Sie einen standardmäßigen Fallback-Text definieren, der angezeigt wird, wenn ein Profilattribut vom Typ Zeichenfolge leer ist. Klicken Sie dazu auf die Schaltfläche mit den Auslassungspunkten neben dem Attribut und wählen Sie **[!UICONTROL Einfügen mit Fallback-Text]**. Schreiben Sie den Text, der standardmäßig angezeigt werden soll, wenn der Wert des Attributs für ein Profil leer ist, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

![](assets/attribute-details.png)

Im folgenden Beispiel können Sie mit dem Personalisierungseditor die Profile auswählen, die heute Geburtstag haben, und dann die Anpassung vervollständigen, indem Sie ein spezifisches Angebot einfügen, das zu diesem Tag passt.

![](assets/perso_ee2.png)

Wenn Ihr Personalisierungsausdruck fertig ist, müssen Sie ihn vom Personalisierungseditor validieren lassen.  Weiterführende Informationen finden Sie in [diesem Abschnitt](personalization-validation.md).
