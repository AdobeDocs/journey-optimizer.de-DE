---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zu Adobe Experience Platform-Zielgruppen
description: Erfahren Sie, wie Sie mit Adobe Experience Platform-Zielgruppen arbeiten.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 71c652ba-f38f-452c-9c1b-dcd728307baf
TQID: https://experienceleague.adobe.com/HkybhydJwQDHVEXCKM5o16ZNeiBk-n9mogm-2pwFKus
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 89%

---

# Benutzerdefinierter Upload {#custom-upload}

Das Adobe Experience Platform-Zielgruppenportal ermöglicht den Import einer Zielgruppe mithilfe einer CSV-Datei.

Geben Sie während des benutzerdefinierten Upload-Prozesses das CSV-Attribut, das als Identität verwendet werden soll, sowie die Profilidentität an, der es zugeordnet ist. Dadurch wird eine Verknüpfung zwischen den Zielgruppendaten und dem Profil hergestellt. Wenn die CSV-Datei einen Identitätswert enthält, der nicht im Profil gefunden wird, wird ein neues Profil mit diesem Identitätswert erstellt.

>[!NOTE]
>
>Wenn bei benutzerdefinierten Upload-Zielgruppen „Inkrementelles Lesen“ in einer wiederkehrenden Journey aktiviert ist, werden Profile nur beim ersten Intervall abgerufen, da diese Zielgruppen fest sind.

![](assets/import-audience.png)

Detaillierte Informationen zum Importieren von Zielgruppen finden Sie in der Dokumentation zum [-Service in Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}.

Mehr zum Hochladen von Zielgruppen im CSV-Format erfahren Sie in diesem Video:

>[!VIDEO](https://video.tv.adobe.com/v/3423357?captions=ger&quality=12)
