---
solution: Journey Optimizer
product: journey optimizer
title: Über den Ausdruckseditor
description: Erfahren Sie, wie der Ausdruckseditor funktioniert.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: ht
source-wordcount: '350'
ht-degree: 100%

---

# Über den Ausdruckseditor {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Über den Ausdruckseditor"
>abstract="Mit dem Ausdruckseditor können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen."

Der Ausdruckseditor ist die Kernkomponente der Personalisierung in [!DNL Journey Optimizer]. Er ist in jedem Kontext verfügbar, in dem Sie eine Personalisierung definieren müssen, wie z. B. E-Mails, Push-Benachrichtigungen und Angebote.

In der Benutzeroberfläche des Ausdruckseditors können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen.

![](assets/perso_ee1.png)

Im linken Bildschirmbereich wird ein Domain-Selektor angezeigt, mit dem Sie die Quelle für die Personalisierung auswählen können.

![](assets/perso_ee3.png)

Verfügbare Quellen sind:

* **[!UICONTROL Profilattribute]**: Listet alle Verweise auf, die mit dem Profilschema verknüpft sind, das in der [Dokumentation des Adobe Experience Platform-Datenmodells (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target=&quot;_blank&quot;} beschrieben wird.
* **[!UICONTROL Segmentzugehörigkeit]**: Listet alle im Segmentierungs-Service von Adobe Experience Platform erstellten Segmente auf. Weitere Informationen zur Segmentierung finden Sie [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de){target=&quot;_blank&quot;}.
* **[!UICONTROL Angebotsentscheidungen]**: Listet alle Angebote auf, die mit einer bestimmten Platzierung verbunden sind. Wählen Sie die Platzierung aus und fügen Sie dann die Angebote in den Inhalt ein. Eine vollständige Dokumentation zum Verwalten von Angeboten finden Sie in [diesem Abschnitt](../design/deliver-personalized-offers.md).
* **[!UICONTROL Kontextbezogene Attribute]**: Wenn eine Kanalaktionsaktivität (E-Mail, Push, SMS) in einer Journey verwendet wird, stehen in diesem Menü kontextbezogene Journey-Felder zur Verfügung. Weiterführende Informationen finden Sie in [diesem Abschnitt](personalization-use-case.md).
* **[!UICONTROL Hilfsfunktionen]**: listet alle Hilfsfunktionen auf, die für die Durchführung von Datenoperationen wie Berechnungen, Datenformatierungen oder -konvertierungen, Bedingungen und die Bearbeitung von Daten im Rahmen der Personalisierung verfügbar sind. Weiterführende Informationen finden Sie in [diesem Abschnitt](functions/functions.md).

Klicken Sie auf die Schaltfläche „+“, um dem Editor ein Attribut hinzuzufügen.

>[!NOTE]
>
>Über das Drei-Punkt-Menü neben dem Symbol „+“ können Sie weitere Details für jede Variable abrufen und Ihre am häufigsten verwendeten Attribute zu den [Favoriten](personalization-favorites.md) hinzufügen.

![](assets/attribute-details.png)

Im folgenden Beispiel können Sie mit dem Ausdruckseditor die Profile auswählen, die heute Geburtstag haben, und dann die Konfiguration vervollständigen, indem Sie ein spezifisches Angebot einfügen, das zu diesem Tag passt.

![](assets/perso_ee2.png)

Sobald Ihr Personalisierungsausdruck fertig ist, müssen Sie ihn vom Ausdruckseditor validieren lassen. Weiterführende Informationen finden Sie in [diesem Abschnitt](personalization-validation.md).
