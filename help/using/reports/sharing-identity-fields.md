---
title: Identitätsfelder für journeyStep-Ereignisse
description: travelStep Ereignis-Identitätsfelder
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 0%

---

# Identitätsfelder für journeyStep-Ereignisse{#sharing-identity-fields}

![](../assets/do-not-localize/badge.png)

Dieses Mixin gilt speziell für journeyStepEvent: Das Ereignis bezieht sich auf die Journey und verfügt nicht über die identityMap zur Beschreibung der Profilidentität (sofern vorhanden).

Für journeyStepEvent müssen auch Identitätsfelder hinzugefügt werden:

## profileID

Profilkennung

Typ: Zeichenfolge

## profileNamespace

Namespace der Profilkennung

Typ: string
