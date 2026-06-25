---
solution: Journey Optimizer
product: journey optimizer
title: Durchführen von Datenlebenszyklusvorgängen
description: Erfahren Sie, wie Sie Datenlebenszyklusvorgänge durchführen
feature: Privacy, Monitoring
role: User
level: Intermediate
exl-id: 8045b559-bf5e-4b5f-9da4-accd44641a68
TQID: https://experienceleague.adobe.com/-zue9aNrWtfL3MGs7OjH-1CF436mzPh50fsru8OSEq8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2: id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56id: f365ec33-2b99-4b7f-b4ee-c743dd7f615fid: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4e89993a998268ae2810c949d0669bf6dc458dd6
workflow-type: ht
source-wordcount: 262
ht-degree: 100%

---

# Durchführen von Datenlebenszyklusvorgängen {#data-hygiene}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Konfigurieren und planen Sie Datenlebenszyklusvorgänge, damit Ihre Einträge korrekt sind, wie vorgesehen verwendet und gemäß Ihren Organisationsrichtlinien gelöscht werden können.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Datenlebenzyklus-Funktionen sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote **Healthcare Shield** und **Privacy and Security Shield** erworben haben.

Da Daten kontinuierlich in Adobe Experience Platform aufgenommen werden, ist es wichtig sicherzustellen, dass Ihre Daten wie vorgesehen verwendet, bei Bedarf aktualisiert und gemäß den Richtlinien der Organisation gelöscht werden.

Diese Aufgaben können mit dem Menü **[!UICONTROL Datenlebenszyklus]** durchgeführt werden, das die Konfiguration und Planung von Datenlebenszyklusvorgängen ermöglicht und sicherstellt, dass Ihre Einträge ordnungsgemäß gepflegt werden.

![](assets/data-hygiene.png)


## Empfehlungen {#data-hygiene-recommendations}

Beachten Sie bei der Durchführung von Datenhygienevorgängen (z. B. beim Löschen von Identitäten oder Datensätzen), dass historische Versandereignisse, die mit gelöschten Identitäten verknüpft sind, nicht mehr in standardmäßigen Reporting- oder DataLake-Abfragen angezeigt werden. Dies kann zu Diskrepanzen zwischen der Anzahl der als **Zugestellt** gemeldeten E-Mails und der Anzahl der **empfangenen** E-Mails in den Posteingängen der Empfangenden führen, insbesondere bei älteren Journeys.

Validieren und exportieren Sie vor dem Ausführen umfangreicher Löschvorgänge alle erforderlichen Versand- oder Berichtsdaten. Wenn nach der Datenhygiene eine Abstimmung erforderlich ist, stimmen Sie sich mit dem Adobe-Support ab, um auf archivierte Protokolle zuzugreifen, oder verwenden Sie Abfragen zum Ereignisdatensatz mit Feedback zu Nachrichten für aktuelle Daten.

## Weitere Informationen {#data-hygiene-learn-more}

Weitere Informationen zum Privacy Service und zum Durchführen von Datenlebenszyklusvorgängen finden Sie in der Dokumentation zu Adobe Experience Platform:

* [Überblick über Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de)
* [Datenlebenszyklus in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/home.html?lang=de)
