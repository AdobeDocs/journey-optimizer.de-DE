---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden benutzerdefinierter Aktionen
description: Erfahren Sie, wie Sie benutzerdefinierte Aktionen verwenden
feature: Actions
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Verwenden benutzerdefinierter Aktionen {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Benutzerdefinierte Aktionen"
>abstract="Mit benutzerdefinierten Aktionen können Sie die Verbindung eines Drittanbietersystems konfigurieren, um Nachrichten oder API-Aufrufe zu senden. Eine Aktion kann mit jedem Dienst eines beliebigen Anbieters konfiguriert werden, der über eine REST-API mit einer JSON-formatierten Payload aufgerufen werden kann."

Mit benutzerdefinierten Aktionen können Sie die Verbindung eines Drittanbietersystems konfigurieren, um Nachrichten oder API-Aufrufe zu senden. Eine Aktion kann mit jedem Dienst eines beliebigen Anbieters konfiguriert werden, der über eine REST-API mit einer JSON-formatierten Payload aufgerufen werden kann.

## Einverständnis und Data Governance {#privacy}

In Journey Optimizer können Sie Data Governance- und Zustimmungsrichtlinien auf Ihre benutzerdefinierten Aktionen anwenden, um zu verhindern, dass bestimmte Felder in Drittanbietersysteme exportiert werden, oder Kunden ausschließen, die dem Empfang von E-Mail-, Push- oder SMS-Nachrichten nicht zugestimmt haben. Weitere Informationen finden Sie auf den folgenden Seiten:

* [Data Governance](../action/action-privacy.md).
* [Einverständnis](../action/consent.md).

## URL-Konfiguration

Der Konfigurationsbereich des **Benutzerdefinierte Aktion** -Aktivität zeigt die URL-Konfigurationsparameter und die Authentifizierungsparameter an, die für die benutzerdefinierte Aktion konfiguriert sind. Sie können den statischen Teil der URL nicht in der Journey, sondern in der globalen Konfiguration der benutzerdefinierten Aktion einrichten. [Weitere Infos](../action/about-custom-action-configuration.md).

### Dynamischer Pfad

Wenn die URL einen dynamischen Pfad enthält, geben Sie den Pfad im **[!UICONTROL Path]** -Feld.

Verwenden Sie zum Verketten von Feldern und Nur-Text-Zeichenfolgen die Zeichenfolgen-Funktionen oder das Pluszeichen (+) im erweiterten Ausdruckseditor. Schließen Sie Nur-Text-Zeichenfolgen in einfachen Anführungszeichen (&#39;) oder in doppelten Anführungszeichen (&quot;) ein. [Weitere Infos](expression/expressionadvanced.md).

Die folgende Tabelle zeigt ein Beispiel für die Konfiguration:

| Feld | Wert |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Pfad | `The id of marketingCampaign + '/messages'` |

Die verkettete URL hat folgendes Formular:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### Kopfzeilen

Die **[!UICONTROL URL Configuration]** zeigt die dynamischen Kopfzeilenfelder, jedoch nicht die konstanten Kopfzeilenfelder an. Dynamische Header-Felder sind HTTP-Header-Felder, deren Wert als Variable konfiguriert ist. [Weitere Infos](../action/about-custom-action-configuration.md).

Geben Sie bei Bedarf den Wert der dynamischen Header-Felder an:

1. Wählen Sie die benutzerdefinierte Aktion in der Journey aus.
1. Klicken Sie im Konfigurationsbereich auf das Stiftsymbol neben dem Kopfzeilenfeld im **[!UICONTROL URL Configuration]** Abschnitt.

   ![](assets/journey-dynamicheaderfield.png)

1. Wählen Sie ein Feld aus und klicken Sie auf **[!UICONTROL OK]**.

## Aktionsparameter

Im **[!UICONTROL Action parameters]** -Abschnitt, werden die Nachrichtenparameter angezeigt, die als _&quot;Variable&quot;_. Für diese Parameter können Sie definieren, wo diese Informationen abgerufen werden sollen (Beispiel: Ereignisse, Datenquellen), manuell übergeben oder den erweiterten Ausdruckseditor für erweiterte Anwendungsfälle verwenden. Erweiterte Anwendungsfälle können Datenmanipulationen und andere Funktionen sein. Siehe hierzu [page](expression/expressionadvanced.md).

**Verwandte Themen**

[Konfigurieren einer Aktion](../action/about-custom-action-configuration.md)
