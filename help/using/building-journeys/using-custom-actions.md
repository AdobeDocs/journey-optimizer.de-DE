---
title: Verwenden benutzerdefinierter Aktionen
description: Erfahren Sie, wie Sie benutzerdefinierte Aktionen verwenden
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 100%

---

# Verwenden benutzerdefinierter Aktionen {#section_f2c_hbg_nhb}

Im Konfigurationsbereich für die Aktivität werden die URL-Konfigurationsparameter und die Authentifizierungsparameter angezeigt, die für die benutzerdefinierte Aktion konfiguriert sind. [Weitere Informationen](../action/about-custom-action-configuration.md).

>[!NOTE]
>
>Eine Kollektion kann nicht in benutzerdefinierten Aktionsparametern übergeben werden. Komplexere Kollektionsfelder (Arrays von Objekten) werden nicht unterstützt.  Beachten Sie außerdem, dass die Parameter ein erwartetes Format haben (Beispiel: Zeichenfolge, Dezimalzahl usw.). Sie müssen darauf achten, dass diese erwarteten Formate eingehalten werden.

## URL-Konfiguration

### Dynamischer Pfad

Wenn die URL einen dynamischen Pfad enthält, geben Sie den Pfad im Feld **[!UICONTROL Pfad]** an.

>[!NOTE]
>
>Sie können den statischen Teil der URL nicht in der Journey, sondern in der globalen Konfiguration der benutzerdefinierten Aktion einrichten. [Weitere Informationen](../action/about-custom-action-configuration.md).

Verwenden Sie zum Verketten von Feldern und Nur-Text-Zeichenfolgen die Zeichenfolgen-Funktionen oder das Pluszeichen (+) im erweiterten Ausdruckseditor. Schließen Sie Nur-Text-Zeichenfolgen in einfachen Anführungszeichen (&#39;) oder in doppelten Anführungszeichen (&quot;) ein. [Weitere Informationen](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=de){target=&quot;_blank&quot;}.

Die folgende Tabelle zeigt ein Beispiel für die Konfiguration:

| Feld | Wert |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Pfad | `The id of marketingCampaign + '/messages'` |

Die verkettete URL hat dieses Format:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign ID\>`/messages`

![](../assets/journey-custom-action-url.png)

### Header

Im Abschnitt **[!UICONTROL URL-Konfiguration]** werden die dynamischen, nicht aber die konstanten Header-Felder angezeigt. Dynamische Header-Felder sind HTTP-Header-Felder, deren Wert als Variable konfiguriert ist. [Weitere Informationen](../action/about-custom-action-configuration.md).

Geben Sie bei Bedarf den Wert der dynamischen Header-Felder an:

1. Wählen Sie die benutzerdefinierte Aktion in der Journey aus.
1. Klicken Sie im Konfigurationsbereich neben dem Header-Feld im Abschnitt **[!UICONTROL URL-Konfiguration]** auf das Stiftsymbol.

   ![](../assets/journey-dynamicheaderfield.png)

1. Wählen Sie ein Feld aus und klicken Sie auf **[!UICONTROL OK]**.

## Aktionsparameter

Im Abschnitt **[!UICONTROL Aktionsparameter]** sehen Sie die Nachrichtenparameter, die als _Variable_ definiert sind. Für diese Parameter können Sie festlegen, wo diese Informationen abgerufen werden sollen (Beispiel: Ereignisse, Datenquellen), Werte manuell übergeben oder den erweiterten Ausdruckseditor für erweiterte Anwendungsfälle verwenden. Erweiterte Anwendungsfälle können Datenmanipulationen und andere Funktionen sein. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html){target=&quot;_blank&quot;}.

**Verwandte Themen**

[Konfigurieren einer Aktion](../action/about-custom-action-configuration.md)
