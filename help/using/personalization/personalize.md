---
solution: Journey Optimizer
product: journey optimizer
title: Personalisieren von Inhalten in Journey Optimizer
description: Erste Schritte mit der Personalisierung
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: Ausdruck, Editor, Start, Personalisierung
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 78c1464ccddec75e4827cbb1877d8fab5ac08b90
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 38%

---

# Erste Schritte bei der Personalisierung{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalisieren von Erlebnissen"
>abstract="Passen Sie Ihre Nachrichten mit **Adobe Journey Optimizer** mithilfe der über die jeweiligen Empfängerinnen und Empfänger verfügbaren Daten und Informationen an sie an. Dabei kann es sich z. B. um den Vornamen der Person, ihre Interessen, ihren Wohnort oder zuvor gekaufte Artikel handeln."

[!DNL Adobe Journey Optimizer] Personalisierungsfunktionen ermöglichen es Ihnen, Ihre Nachrichten für jeden einzelnen Empfänger anzupassen, indem Sie die vorhandenen Daten und Informationen nutzen. Dabei kann es sich z. B. um den Vornamen der Person, ihre Interessen, ihren Wohnort oder zuvor gekaufte Artikel handeln.

## Funktionsweise der Personalisierung

Mit dem **Personalisierungseditor** können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen, und verschiedene Tools wie Hilfsfunktionen oder vordefinierte Ausdrücke nutzen, um Nachrichten effektiv anzupassen.

Journey Optimizer verwendet eine Inline-Personalisierungssyntax, die auf Handlebars basiert. Damit können Sie Ausdrücke mit Inhalten erstellen, die von geschweiften Klammern **{{}}** eingeschlossen sind.

Bei der Verarbeitung der Nachricht ersetzt Journey Optimizer den Ausdruck durch die im Experience Platform-Datensatz enthaltenen Daten. Beispielsweise wird `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` dynamisch zu `Hello John Doe`.

Mit dieser Syntax können Sie Nachrichten über mehrere Felder hinweg personalisieren, einschließlich E-Mail-Betreffzeilen, Nachrichtentexten, Push-Benachrichtigungen oder URLs.

## Für die Personalisierung verwendete Daten

Personalization basiert auf den Profildaten, die von dem in Adobe Experience Platform definierten Schema **XDM Individual Profile** verwaltet werden. Das Schema **XDM Individual Profile** ist das einzige, das Sie zum Personalisieren von Inhalten in [!DNL Journey Optimizer] verwenden können. Weitere Informationen finden Sie in der [Dokumentation zum Adobe Experience Platform-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}.

Sie können auch &quot;**Attribute“**, um Ihre Inhalte zu personalisieren. Berechnete Attribute ermöglichen es Ihnen, einzelne Verhaltensereignisse in berechnete Profilattribute zusammenzufassen, die in Adobe Experience Platform verfügbar sind. [Erfahren Sie, wie Sie mit berechneten Attributen arbeiten](../audience/computed-attributes.md)

Darüber hinaus können Sie mit [!DNL Journey Optimizer] Daten aus Adobe Experience Platform im Personalisierungseditor nutzen, um Ihre Inhalte zu personalisieren. Hierzu müssen Datensätze, die für die Personalisierung der Suche erforderlich sind, zunächst über einen API-Aufruf aktiviert werden. Anschließend können Sie deren Daten verwenden, um Ihre Inhalte in Journey Optimizer zu personalisieren. Diese Funktion ist derzeit in der Beta-Version verfügbar. [Weitere Informationen](../personalization/lookup-aep-data.md)

## Tauchen wir tiefer in die Materie ein

Nachdem Sie nun über ein Verständnis der Personalisierung in **[!DNL Journey Optimizer]** verfügen, ist es an der Zeit, diese Dokumentationsabschnitte zu vertiefen, um mit der Funktion zu arbeiten.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="personalization-build-expressions.md">
<img alt="Personalisierung hinzufügen" src="assets/do-not-localize/add.png">
</a>
<div>
<a href="personalization-build-expressions.md"><strong>Hinzufügen von Personalisierung</strong></a>
</div>
<p>
</td>
<td>
<a href="../personalization/personalization-syntax.md">
<img alt="Lead" src="assets/do-not-localize/syntax.png">
</a>
<div><a href="../personalization/personalization-syntax.md"><strong>Personalization-Syntax</strong>
</div>
<p>
</td>
<td>
<a href="../personalization/functions/functions.md">
<img alt="Gelegentlich" src="assets/do-not-localize/functions.png">
</a>
<div>
<a href="../personalization/functions/functions.md"><strong>Liste der Hilfsfunktionen</strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-use-case.md">
<img alt="Gelegentlich" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-use-case.md"><strong>Anwendungsfälle für Personalization</strong></a>
</div>
<p></td>
</tr></table>

## Anleitungsvideos{#video-perso}

Erfahren Sie, wie Sie kontextuelle Ereignisinformationen von einer Journey verwenden können, um eine Nachricht zu personalisieren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Erfahren Sie, wie Sie einer Nachricht eine profilbasierte Personalisierung hinzufügen und die Zielgruppenzugehörigkeit als Vorbedingung für einen Personalisierungsbaustein verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

