---
title: Kontexte der Personalisierung in Journey Optimizer
description: Erfahren Sie, in welchen Kontexten Sie Personalisierung hinzufügen können
translation-type: tm+mt
source-git-commit: 11e73011374fee3af1c0780acf9d96f122214e8e
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 1%

---

# Personalisierungskontext und -tool {#personalization-areas}

![](../assets/do-not-localize/badge.png)

Inhalt und Anzeige der von Journey Optimizer gelieferten Nachrichten können auf verschiedene Weise personalisiert werden.

Alle mit dem Editor-Symbol verknüpften Felder können den Personalisierungseditor öffnen und Personalisierungsinhalte empfangen.

![](assets/perso_icon.png)

## E-Mails personalisieren

Wenn Sie eine E-Mail erstellen, können Sie Personalisierung im Feld **E-Mail-Betreff** der Nachricht hinzufügen.

![](assets/perso_subject.png)

Im E-Mail-Designer können Sie den Inhalt personalisieren:

* In der **Meldung**: Klicken Sie in einen Textblock, klicken Sie in der Kontextsymbolleiste auf das Symbol **Personalize** und wählen Sie das Feld **Personalisierung** einfügen. Weitere Informationen zur Benutzeroberfläche von E-Mail-Designer finden Sie in diesem Abschnitt [Abschnitt](../design-emails.md).

   ![](assets/perso_insert.png)

* Für einen **Link**: Wählen Sie Text oder Bild in einem Textblock aus und klicken Sie in der Kontextsymbolleiste auf das Symbol **Link einfügen**. Im Fenster können Sie einen Personalisierungsblock hinzufügen, indem Sie auf das Symbol **Hinzufügen Personalisierung** klicken.

   ![](assets/perso_link.png)

## Push-Benachrichtigungen personalisieren

Sie können Ihre **Push-Benachrichtigungen** auch in den folgenden Feldern personalisieren:

* **Title**
* **Body**
* **Benutzerdefinierter Sound**
* **Abzeichen**
* **Benutzerspezifische Daten**

![](assets/perso_push.png)

Weitere Informationen zur Konfiguration der Push-Benachrichtigung finden Sie in [diesem Abschnitt](../configure-push.md).

## Ausdruck-Editor verwenden

Der Ausdruck-Editor ist das Herzstück der Personalisierung in Journey Optimizer.

Es ist in jedem Kontext verfügbar, in dem Sie Personalisierung definieren müssen, wie E-Mails, Push- und Angebote.

In der Benutzeroberfläche des Ausdruck-Editors können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen.

![](assets/perso_ee1.png)

Im linken Bildschirmbereich wird ein Domänenselektor angezeigt, mit dem Sie die Quelle für die Personalisierung auswählen können.

* **Profil** : Liste aller Verweise, die mit dem Profil-Schema in der XDM-Dokumentation ( [Adobe Experience Platform Data Model) verknüpft sind](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).
* **Segmentmitgliedschaft** : Liste aller im Adobe Experience Platform-Segmentierungsdienst erstellten Segmente. Weitere Informationen zur Segmentierung finden Sie [hier](https://experienceleague.corp.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)
* **Angebote** : Liste aller Angebot, die mit einer bestimmten Platzierung verbunden sind. Wählen Sie die Platzierung aus und fügen Sie dann die Angebot in den Inhalt ein. Eine vollständige Dokumentation zum Verwalten von Angeboten finden Sie in [diesem Abschnitt](https://experienceleague.corp.adobe.com/docs/customer-journey-management/using/create-messages/deliver-personalized-offers.html?lang=en#about-offer-decisioning)
* **Kontext** : Wenn die  **** Messagesaktivität in einer Journey verwendet wird, stehen in diesem Menü kontextbezogene Journey-Felder zur Verfügung. Siehe [diesen Abschnitt](https://experienceleague.corp.adobe.com/docs/customer-journey-management/using/create-messages/deliver-personalized-offers.html?lang=en#about-offer-decisioning)

Bei Auswahl wird der Verweis im Editor hinzugefügt.

>[!NOTE]
>
>Das Infosymbol neben dem Symbol &quot;+&quot;öffnet eine QuickInfo mit weiteren Details zu jeder Variablen.

Im folgenden Beispiel können Sie mit dem Ausdruck-Editor die Profil auswählen, deren Geburtstag heute liegt, und dann die Anpassung abschließen, indem Sie ein bestimmtes Angebot einfügen, das diesem Tag entspricht.

![](assets/perso_ee2.png)




