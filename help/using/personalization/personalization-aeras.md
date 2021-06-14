---
title: Kontexte der Personalisierung in Journey Optimizer
description: Erfahren Sie, in welchen Kontexten Sie Personalisierung hinzufügen können
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 80%

---

# Personalisierungskontext und -tool {#personalization-areas}

![](../assets/do-not-localize/badge.png)

Es gibt verschiedene Möglichkeiten, um den Inhalt und die Darstellung von Nachrichten in Journey Optimizer zu personalisieren.

Alle mit dem Editor-Symbol verknüpften Felder können den Personalisierungs-Editor öffnen und Personalisierungsinhalte empfangen.

![](assets/perso_icon.png)

## E-Mails personalisieren

Wenn Sie eine E-Mail erstellen, können Sie im Feld **E-Mail-Betreff** der Nachricht eine Personalisierung hinzufügen.

![](assets/perso_subject.png)

In Email Designer können Sie den Inhalt personalisieren:

* In der **Nachricht**: Klicken Sie in einen Textblock, klicken Sie auf das Symbol **Personalisieren** in der kontextbezogenen Symbolleiste und wählen Sie **Personalisierungfeld einfügen** aus. Weiterführende Informationen zur Benutzeroberfläche von Email Designer finden Sie in [diesem Abschnitt](../design-emails.md).

   ![](assets/perso_insert.png)

* Für einen **Link**: Wählen Sie Text oder ein Bild in einem Textblock aus und klicken Sie in der kontextbezogenen Symbolleiste auf das Symbol **Link einfügen**. Im Fenster können Sie einen Personalisierungsblock hinzufügen, indem Sie auf das Symbol **Personalisierung hinzufügen** klicken.

   ![](assets/perso_link.png)

## Push-Benachrichtigungen personalisieren

Sie können **Push-Benachrichtigungen** auch in den folgenden Feldern personalisieren:

* **Titel**
* **Textkörper**
* **Benutzerdefinierter Benachrichtigungston**
* **Badges**
* **Benutzerspezifische Daten**

![](assets/perso_push.png)

Weitere Informationen zur Konfiguration von Push-Benachrichtigungen finden Sie in [diesem Abschnitt](../create-push.md).

## Ausdruckseditor verwenden

Der Ausdruckseditor ist das Herzstück der Personalisierung in Journey Optimizer.

Er ist in jedem Kontext verfügbar, in dem Sie eine Personalisierung definieren müssen, wie z. B. E-Mails, Push-Benachrichtigungen und Angebote.

In der Benutzeroberfläche des Ausdruckseditors können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen.

![](assets/perso_ee1.png)

Im linken Bildschirmbereich wird ein Domain-Selektor angezeigt, mit dem Sie die Quelle für die Personalisierung auswählen können.

* **Profil**: Listet alle Verweise auf, die mit dem Profilschema, das in der [Dokumentation des Adobe Experience Platform-Datenmodells (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) beschrieben ist, verknüpft sind.
* **Segmentzugehörigkeit**: Listet alle im Adobe Experience Platform-Segmentierungs-Service erstellten Segmente auf. Weitere Informationen zur Segmentierung finden Sie [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de)
* **Angebote**: Listet alle Angebot auf, die mit einer bestimmten Platzierung verbunden sind. Wählen Sie die Platzierung aus und fügen Sie dann die Angebote in den Inhalt ein. Eine vollständige Dokumentation zum Verwalten von Angeboten finden Sie in [diesem Abschnitt](../deliver-personalized-offers.md)
* **Kontext** : Wenn die  **** Nachrichtentätigkeit in einer Journey verwendet wird, stehen in diesem Menü kontextbezogene Journey-Felder zur Verfügung. Siehe [diesen Abschnitt](personalization-use-case.md)
* **Hilfsfunktionen** : listet alle Hilfsfunktionen auf, die für die Durchführung von Datenvorgängen wie Berechnungen, Datenformatierungen oder Konvertierungen, Bedingungen und deren Bearbeitung im Kontext der Personalisierung verfügbar sind. [Weitere Infos](functions/functions.md)



Bei der Auswahl wird die Referenz im Editor hinzugefügt.

>[!NOTE]
>
>Das Infosymbol neben dem Symbol „+“ öffnet eine QuickInfo mit weiteren Details zu jeder Variablen.

Im folgenden Beispiel können Sie mit dem Ausdruckseditor die Profile auswählen, die heute Geburtstag haben, und dann die Anpassung vervollständigen, indem Sie ein spezifisches Angebot einfügen, das zu diesem Tag passt.

![](assets/perso_ee2.png)




