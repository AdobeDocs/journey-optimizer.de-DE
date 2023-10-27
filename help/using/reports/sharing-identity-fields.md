---
solution: Journey Optimizer
product: journey optimizer
title: Identitätsfelder für journeyStep-Ereignisse
description: Identitätsfelder für journeyStep-Ereignisse
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: c447fcf0-51ec-4d88-8b2d-f15db076bfbc
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: ht
source-wordcount: '60'
ht-degree: 100%

---

# Identitätsfelder für journeyStep-Ereignisse {#sharing-identity-fields}

Diese Feldergruppe gilt speziell für journeyStepEvent: Das Ereignis bezieht sich auf die Journey und verfügt nicht über identityMap zur Beschreibung der Profilidentität (sofern vorhanden).

Für journeyStepEvent müssen auch Identitätsfelder hinzugefügt werden:

## profileID

Profilkennung

Typ: Zeichenfolge

## profileNamespace

Namespace der Profilkennung

Typ: Zeichenfolge
