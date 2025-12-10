---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zu Adobe Experience Platform-Zielgruppen
description: Erfahren Sie, wie Sie mit Adobe Experience Platform-Zielgruppen arbeiten.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: c30a74ccdaec81cbbb28e3129d5c351a0fe64bfc
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 90%

---

# Zielgruppenaktivierung in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Sie können in Kampagnen und Journeys eine beliebige Zielgruppe auswählen, die mithilfe von Segmentdefinitionen, einem benutzerdefinierten Upload, Kompositions-Workflows oder der Komposition föderierter Zielgruppen generiert wurde.

>[!AVAILABILITY]
>
>Die Verwendung von Zielgruppen und Attributen aus der Zielgruppenkomposition ist derzeit nicht für die Verwendung mit Healthcare Shield oder Privacy and Security Shield verfügbar. [Erfahren Sie, wie Sie Zielgruppen-Anreicherungsattribute in Journey Optimizer verwenden.](../audience/about-audiences.md#enrichment)

## Verzögerung der Zielgruppenaktivierung {#activation}

Zielgruppen sind direkt nach Abschluss der Aufnahme für die Verwendung in Journey Optimizer bereit. Dies geschieht in der Regel innerhalb einer Stunde, kann jedoch variieren. Zielgruppen, die aus Kompositionen resultieren, sollten 24 Stunden nach der Veröffentlichung verfügbar sein.

Bei Zielgruppen, die aus Batch-Segmentierungsaufträgen resultieren, kann sich die Aktivierung aufgrund von Variabilität bei der Batch-Aufnahme verzögern. Für täglich geplante Journeys vom Typ „Zielgruppe lesen“ können Sie in den Journey-Eigenschaften ein Zeitfenster definieren, um sicherzustellen, dass vor der Journey-Ausführung neue Zielgruppendaten verfügbar sind. Wenn der Segmentierungsauftrag nicht innerhalb des definierten Zeitfensters abgeschlossen wird, wird die Journey bis zum nächsten Auftreten übersprungen. [Informationen zum Planen einer Journey vom Typ „Zielgruppe lesen“](../building-journeys/read-audience.md)

## Benutzerdefinierter Upload und Komposition föderierter Zielgruppen

Beachten Sie die folgenden Leitlinien für benutzerdefinierte Uploads und Kompositionen föderierter Zielgruppen:

* **Vorschau und Testversand:** Derzeit werden Vorschau und Testversand für Zielgruppen, die mithilfe eines CSV-Uploads oder der Komposition föderierter Zielgruppen erstellt wurden, nicht unterstützt. Berücksichtigen Sie dies bei der Planung Ihrer Kampagnen.

* **Targeting neuer Profile:** Wenn keine Übereinstimmung zwischen einem Eintrag und einem Profil des einheitlichen Profildienstes gefunden wird, wird ein neues leeres Profil erstellt. Dieses Profil ist mit den Anreicherungsattributen verknüpft, die im Data Lake gespeichert sind. Da dieses neue Profil leer ist, sind auch die Targeting-Felder, die normalerweise in Journey Optimizer verwendet werden (wie z. B. personalEmail.address, mobilePhone.number), leer und können daher nicht für das Targeting verwendet werden. 

  Um dieses Problem zu lösen, können Sie das „Ausführungsfeld“ (oder je nach Kanal die „Ausführungsadresse“) in der Kanalkonfiguration als „identityMap“ angeben. Dadurch wird sichergestellt, dass das bei der Zielgruppenerstellung als Identität ausgewählte Attribut für das Targeting in Journey Optimizer verwendet wird.

* **Aktivierte Einträge und Identitätszuordnung:** Jeder Eintrag in der Zielgruppe wird aktiviert, einschließlich aller Duplikate. Beim nächsten Export des Profils des einheitlichen Profildienstes werden diese Einträge einer Identitätszuordnung unterzogen. Infolgedessen kann die Anzahl der aktivierten Einträge nach der Identitätszuordnung von der Anzahl der Profile abweichen.

## Ansprechen von Zielgruppen in [!DNL Journey Optimizer]

Sie können Zielgruppen in **[!DNL Journey Optimizer]** auf verschiedene Weise nutzen:

* Wählen Sie eine Zielgruppe für eine **Kampagne** aus, sodass die Nachricht an alle Personen gesendet wird, die zur ausgewählten Zielgruppe gehören. [Erfahren Sie, wie Sie die Zielgruppe einer Kampagne definieren](../campaigns/create-campaign.md#define-the-audience-audience).

* Verwenden Sie die Orchestrierungsaktivität **Zielgruppe lesen** in einer Journey, damit alle Personen der Zielgruppe in die Journey eintreten und die in Ihrer Journey enthaltenen Nachrichten empfangen. Angenommen, Sie verfügen über eine Zielgruppe für „Silber-Kundinnen und -Kunden“. Mit dieser Aktivität können Sie dafür sorgen, dass alle Silber-Kundinnen und -Kunden in eine Journey eintreten, und ihnen eine Reihe personalisierter Nachrichten senden. [Erfahren Sie, wie Sie eine Aktivität vom Typ „Zielgruppe lesen“ konfigurieren](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  Bei Journey, die Zielgruppen aus der Zielgruppenkomposition oder dem benutzerdefinierten Upload verwenden, sind Profilattribute so aktuell wie die letzte Batch-Auswertung beim Journey-Eintrag. Nach einer **Warten**-Aktivität aktualisiert der Journey jedoch Profilattribute vom Unified Profile Service (UPS). Dabei werden die neuesten verfügbaren Daten abgerufen, was bedeutet, dass sich die Profilattribute während der Journey-Ausführung ändern können. [Erfahren Sie mehr über die Aktualisierung von Profilen nach einer Warteaktivität](../building-journeys/wait-activity.md#profile-refresh)

* Verwenden Sie die Aktivität **Bedingung** in einer Journey, um Bedingungen zu erstellen, die auf der Zielgruppenzugehörigkeit basieren. [Erfahren Sie, wie Sie Zielgruppen in Bedingungen verwenden](../building-journeys/condition-activity.md#using-a-segment).

* Verwenden Sie die Ereignisaktivität **Zielgruppen-Qualifizierung**, um Personen auf der Grundlage von Adobe Experience Platform-Zielgruppeneintritten und -austritten zu veranlassen, in eine Journey einzutreten oder damit fortzufahren. So können Sie z. B. alle neuen Silber-Kundinnen und -Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weitere Informationen zum Verwenden dieser Aktivität finden Sie unter [Erfahren Sie, wie Sie eine Zielgruppen-Qualifizierungsaktivität konfigurieren](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Aufgrund der Batch-Natur von Zielgruppen, die mithilfe von Kompositions-Workflows, einem benutzerdefinierten Upload oder der Komposition föderierter Zielgruppen erstellt wurden, können Sie diese Zielgruppen nicht in einer Aktivität „Zielgruppen-Qualifizierung“ auswählen. In dieser Aktivität können nur Zielgruppen genutzt werden, die mithilfe von Segmentdefinitionen erstellt wurden.
