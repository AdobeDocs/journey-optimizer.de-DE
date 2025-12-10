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
source-git-commit: 24d66f146ea3ed0e89a3b928b805bc53a70a8895
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 52%

---

# Zielgruppenaktivierung in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Sie können in Kampagnen und Journeys eine beliebige Zielgruppe auswählen, die mithilfe von Segmentdefinitionen, einem benutzerdefinierten Upload, Kompositions-Workflows oder der Komposition föderierter Zielgruppen generiert wurde.

## Leitlinien und Einschränkungen {#guardrails}

* **Healthcare Shield oder Privacy and Security Shield** - Die Verwendung von Zielgruppen und Attributen aus der Zielgruppenkomposition ist derzeit nicht mit Healthcare Shield oder Privacy and Security Shield verfügbar. [Erfahren Sie, wie Sie Zielgruppen-Anreicherungsattribute in verwenden [!DNL Journey Optimizer]](../audience/about-audiences.md#enrichment)

* **Benutzerdefinierter Upload und Federated-Audience-Komposition** - Beachten Sie die folgenden Leitplanken für benutzerdefinierte Upload- und Federated-Audience-Komposition-Zielgruppen:

   * **Unterstützung von Vorschau und Testversand:** Zurzeit werden Vorschau und Testversand für Zielgruppen, die mit CSV-Uploads oder Federated Audience Composition erstellt wurden, nicht unterstützt. Berücksichtigen Sie dies bei der Planung Ihrer Kampagnen.

   * **Targeting neuer Profile:** Wenn keine Übereinstimmung zwischen einem Eintrag und einem Profil des einheitlichen Profildienstes gefunden wird, wird ein neues leeres Profil erstellt. Dieses Profil ist mit den Anreicherungsattributen verknüpft, die im Data Lake gespeichert sind. Da dieses neue Profil leer ist, sind Zielgruppenbestimmungsfelder, die normalerweise in [!DNL Journey Optimizer] verwendet werden (z. B. personalEmail.address, mobilePhone.number) leer. Daher können diese Felder nicht für die Zielgruppenbestimmung verwendet werden.

     Um dieses Problem zu lösen, können Sie das „Ausführungsfeld“ (oder je nach Kanal die „Ausführungsadresse“) in der Kanalkonfiguration als „identityMap“ angeben. Dadurch wird sichergestellt, dass beim Erstellen der Zielgruppe als Identität das Attribut ausgewählt wird, das beim Targeting in [!DNL Journey Optimizer] verwendet wird.

   * **Aktivierte Einträge und Identitätszuordnung:** Jeder Eintrag in der Zielgruppe wird aktiviert, einschließlich aller Duplikate. Beim nächsten Profilexport im Unified Profile Service durchlaufen diese Datensätze eine Identitätszuordnung. Infolgedessen kann die Anzahl der aktivierten Einträge nach der Identitätszuordnung von der Anzahl der Profile abweichen.

## Verzögerung der Zielgruppenaktivierung {#activation}

Zielgruppen können direkt nach Abschluss der Aufnahme in [!DNL Journey Optimizer] verwendet werden. Dies geschieht in der Regel innerhalb einer Stunde, kann jedoch variieren. Zielgruppen, die aus Kompositionen resultieren, sollten 24 Stunden nach der Veröffentlichung verfügbar sein.

Bei Zielgruppen, die aus Batch-Segmentierungsaufträgen resultieren, kann sich die Aktivierung aufgrund von Variabilität bei der Batch-Aufnahme verzögern. Für täglich geplante Journey mit Lesezugriff auf Zielgruppen können Sie in den Journey-Eigenschaften ein Zeitfenster definieren, um sicherzustellen, dass vor der Journey-Ausführung neue Zielgruppendaten verfügbar sind.

Wenn der Segmentierungsauftrag nicht innerhalb des definierten Zeitfensters abgeschlossen wird, wird die Journey bis zum nächsten Auftreten übersprungen. [Informationen zum Planen einer Journey vom Typ „Zielgruppe lesen“](../building-journeys/read-audience.md)

## Ansprechen von Zielgruppen in [!DNL Journey Optimizer]

Sie können Zielgruppen in **[!DNL Journey Optimizer]** auf verschiedene Weise nutzen:

* Wählen Sie eine Zielgruppe für eine **Kampagne** aus, sodass die Nachricht an alle Personen gesendet wird, die zur ausgewählten Zielgruppe gehören. [Erfahren Sie, wie Sie die Zielgruppe einer Kampagne definieren](../campaigns/create-campaign.md#define-the-audience-audience).

* Verwenden Sie die Orchestrierungsaktivität **Zielgruppe lesen** in einer Journey, damit alle Personen der Zielgruppe in die Journey eintreten und die in Ihrer Journey enthaltenen Nachrichten empfangen. Angenommen, Sie verfügen über eine Zielgruppe für „Silber-Kundinnen und -Kunden“. Mit dieser Aktivität können Sie alle Silber-Kunden auf eine Journey bringen. Sie können ihnen dann eine Reihe personalisierter Nachrichten senden. [Erfahren Sie, wie Sie eine Aktivität vom Typ „Zielgruppe lesen“ konfigurieren](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  Bei Journey, die Zielgruppen aus der Zielgruppenkomposition oder dem benutzerdefinierten Upload verwenden, sind Profilattribute so aktuell wie die letzte Batch-Auswertung beim Journey-Eintrag. Nach einer **Warten**-Aktivität aktualisiert der Journey jedoch Profilattribute vom Unified Profile Service (UPS). Dabei werden die neuesten verfügbaren Daten abgerufen, was bedeutet, dass sich die Profilattribute während der Journey-Ausführung ändern können. [Erfahren Sie mehr über die Aktualisierung von Profilen nach einer Warteaktivität](../building-journeys/wait-activity.md#profile-refresh)

* Verwenden Sie die Aktivität **Bedingung** in einer Journey, um Bedingungen zu erstellen, die auf der Zielgruppenzugehörigkeit basieren. [Erfahren Sie, wie Sie Zielgruppen in Bedingungen verwenden](../building-journeys/condition-activity.md#using-a-segment).

* Verwenden Sie die Ereignisaktivität **Zielgruppen-Qualifizierung**, um Personen auf der Grundlage von Adobe Experience Platform-Zielgruppeneintritten und -austritten zu veranlassen, in eine Journey einzutreten oder damit fortzufahren. So können Sie z. B. alle neuen Silber-Kundinnen und -Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. [Erfahren Sie, wie Sie eine Aktivität vom Typ Zielgruppenqualifizierung konfigurieren](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Aufgrund der Batch-Natur von Zielgruppen, die mithilfe von Kompositions-Workflows, einem benutzerdefinierten Upload oder der Komposition föderierter Zielgruppen erstellt wurden, können Sie diese Zielgruppen nicht in einer Aktivität „Zielgruppen-Qualifizierung“ auswählen. In dieser Aktivität können nur Zielgruppen genutzt werden, die mithilfe von Segmentdefinitionen erstellt wurden.

## Aktivierung nicht unterstützter Zielgruppentypen in [!DNL Journey Optimizer]

Nur im Zielgruppenportal erstellte Zielgruppen können direkt in [!DNL Journey Optimizer] Journey und Kampagnen angesprochen werden. [Weitere Informationen zu verfügbaren Zielgruppentypen](../audience/about-audiences.md#types).

Wenn Sie Profile aus einer nicht unterstützten Zielgruppe, z. B. einer Customer Journey Analytics-Zielgruppe, ansprechen möchten, müssen Sie sie im Zielgruppenportal in eine neue Segmentdefinition einschließen. Detaillierte Informationen zum Hinzufügen von Zielgruppen in einer Segmentdefinition finden Sie in der [Segment Builder-Dokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#adding-audiences){target="_blank"}

Warten Sie anschließend, bis die Segmentierungsbewertung abgeschlossen ist, um sie in Ihren Journey und Kampagnen zu verwenden.
