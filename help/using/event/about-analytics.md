---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zu Adobe Analytics-Daten
description: Erfahren Sie, wie Sie Adobe Analytics-Daten nutzen.
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: a6735063ec68b40b1441b379a20cba8953b59447
workflow-type: ht
source-wordcount: '203'
ht-degree: 100%

---

# Nutzung von Adobe Analytics-Daten{#analytics-data}

Alle verhaltensbezogenen Ereignisdaten, die in Adobe Analytics bereits erfasst und an Adobe Experience Platform gestreamt werden, können zum Auslösen von Journeys und zum Automatisieren von Kundenerlebnissen genutzt werden.

>[!NOTE]
>
>Dieser Abschnitt gilt nur für regelbasierte Ereignisse und Kunden, die mit Adobe Analytics-Daten arbeiten müssen.

Voraussetzung hierfür ist, dass in Adobe Experience Platform die Report Suite aktiviert wurde, die verwendet werden soll. Gehen Sie dazu wie folgt vor:

1. Eine Verbindung mit Adobe Experience Platform herstellen und zu **[!UICONTROL Quellen]** navigieren.
1. Im Abschnitt „Adobe Analytics“ die Option **[!UICONTROL Daten hinzufügen]** wählen: Die Liste der verfügbaren Adobe Analytics Report Suites wird angezeigt.

1. Die zu aktivierende Report Suite auswählen und auf **[!UICONTROL Weiter]** und dann auf **[!UICONTROL Fertigstellen]** klicken.

1. Geben Sie die Daten-ID der Quelle für Ihren dem Betaversion-Programm zugehörigen Kontaktpunkt frei.

Dadurch wird der Analytics-Quell-Connector für diese Report Suite aktiviert. Sobald die Daten eingehen, werden sie in ein Erlebnisereignis umgewandelt und an Adobe Experience Platform gesendet.

![](assets/jo-event9.png)

Weitere Informationen zum Adobe Analytics-Quellen-Connector finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=de){target=&quot;_blank&quot;} und im [Tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=de){target=&quot;_blank&quot;}.
