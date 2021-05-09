---
title: Info zu ExperienceEvent-Schemas für Journey-Ereignis
description: Erfahren Sie mehr über ExperienceEvent-Schema für Journey-Ereignis
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Informationen zu ExperienceEvent-Schemata für [!DNL Journey Optimizer]-Ereignisse

![](../assets/do-not-localize/badge.png)

[!DNL Journey Optimizer] Ereignis sind XDM Experience Ereignis, die über Streaming Ingestion an Adobe Experience Platform gesendet werden.

Eine wichtige Voraussetzung für das Einrichten von Ereignissen für [!DNL Journey Optimizer] ist, dass Sie mit dem Adobe Experience Platform Experience Data Model (oder XDM) vertraut sind und wie Sie XDM Experience Ereignis-Schema zusammenstellen sowie wie Sie XDM-formatierte Daten an Adobe Experience Platform streamen können.

## Schemaanforderungen an [!DNL Journey Optimizer]-Ereignisse

Der erste Schritt beim Einrichten eines Ereignisses für [!DNL Journey Optimizer] besteht darin, sicherzustellen, dass ein XDM-Schema zur Darstellung des Ereignisses definiert ist und ein Datensatz, der zum Aufzeichnen von Instanzen des Ereignisses auf Adobe Experience Platform erstellt wurde. Es ist nicht unbedingt erforderlich, einen Datensatz für Ihre Ereignisse zu haben. Wenn Sie die Ereignisse jedoch an einen bestimmten Datensatz senden, können Sie den Ereignisverlauf der Benutzer zur späteren Bezugnahme und Analyse aufbewahren. Dies ist daher immer empfehlenswert. Wenn Sie noch kein geeignetes Schema und einen entsprechenden Datensatz für Ihr Ereignis haben, können beide Aufgaben in der Adobe Experience Platform-Weboberfläche durchgeführt werden.

![](../assets/schema1.png)

Jedes XDM-Schema, das für [!DNL Journey Optimizer]-Ereignisse verwendet wird, sollte die folgenden Anforderungen erfüllen:

* Das Schema muss der XDM-ExperienceEvent-Klasse angehören.

   ![](../assets/schema2.png)

* Bei vom System erstellten Ereignissen muss das Schema das eventID-Orchestrierungs-Mixin enthalten. [!DNL Journey Optimizer] verwendet dieses Feld, um Ereignisse zu identifizieren, die in Journeys verwendet werden.

   ![](../assets/schema3.png)

* Deklarieren Sie ein Identitätsfeld zur Identifizierung des Themas des Ereignisses. Wenn keine Identität angegeben ist, kann eine Identitätszuordnung (identityMap) verwendet werden. Dies wird nicht empfohlen.

   ![](../assets/schema4.png)

* Damit diese Daten später in einer Journey zur Suche verfügbar sind, markieren Sie das Schema und den Datensatz für das Profil.

   ![](../assets/schema5.png)

   ![](../assets/schema6.png)

* Sie können auch Datenfelder einschließen, um andere Kontextdaten zu erfassen, die Sie in das Ereignis aufnehmen möchten, z. B. Informationen zum Benutzer, zum Gerät, von dem das Ereignis generiert wurde, zum Ort oder andere aussagekräftige Umstände in Zusammenhang mit dem Ereignis.

   ![](../assets/schema7.png)

   ![](../assets/schema8.png)
