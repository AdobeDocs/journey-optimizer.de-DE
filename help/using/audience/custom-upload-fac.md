---
solution: Journey Optimizer
product: journey optimizer
title: Benutzerdefinierter Upload (CSV) und Zusammengestellte Zielgruppenkomposition
description: Erfahren Sie wichtige Informationen und Best Practices beim Arbeiten mit benutzerdefinierten Upload-Zielgruppen (CSV) und Federated Audience Komposition-Zielgruppen.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 26d311802236a1f9e8f6273c1291bcb54138aad2
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 38%

---

# Benutzerdefinierter Upload (CSV) und Zusammengestellte Zielgruppenkomposition {#csv-fac}

## Über benutzerdefinierte Uploads und Zusammenstellungen von Zielgruppen {#about}

Zusätzlich zu den Segmentdefinitionen und der Zielgruppenzusammensetzung können Sie mit [!DNL Journey Optimizer] Zielgruppen generieren und auswählen, indem Sie sie aus einer CSV-Datei importieren oder Daten aus Ihrem Data Warehouse nutzen.

* **Benutzerdefinierter Upload**: Importieren einer Zielgruppe mithilfe einer CSV-Datei. In der [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"} erfahren Sie, wie Sie Zielgruppen in Adobe Experience Platform importieren.

* **Komposition föderierter Zielgruppen**: Führen Sie Datensätze direkt aus Ihrem bestehenden Data Warehouse zusammen, um Adobe Experience Platform Zielgruppen und Attribute in einem System aufzubauen und anzureichern. Lesen Sie das Handbuch zu [Komposition föderierter Zielgruppen](https://experienceleague.adobe.com/de/docs/federated-audience-composition/using/home).

  >[!AVAILABILITY]
  >
  >Die Komposition föderierter Zielgruppen ist derzeit nur für eine Reihe von Organisationen verfügbar (begrenzte Verfügbarkeit). Weitere Informationen erhalten Sie beim Adobe-Support.

Sie können diese Zielgruppen in Journey Optimizer auswählen oder für ein von Adobe Experience Platform unterstütztes Ziel aktivieren

➡️ [Entdecken Sie diese Funktionen im Video](#video)

## Wichtige Informationen {#must-read}

Dieser Abschnitt enthält wichtige Informationen, die Sie beim Arbeiten mit benutzerdefinierten Upload-Zielgruppen (CSV-Dateien) und Federated Audience Komposition beachten sollten.

* **Vorschau- und Testversandunterstützung:** Derzeit werden Vorschau und Testversand für Zielgruppen, die mit CSV-Upload oder Federated Audience Komposition erstellt wurden, nicht unterstützt. Berücksichtigen Sie dies bei der Planung Ihrer Kampagnen.

* **Aktivierungsverzögerung:** Zielgruppen können direkt nach Abschluss der Aufnahme in Journey Optimizer verwendet werden. Dies geschieht in der Regel innerhalb einer Stunde, kann jedoch variieren.

* **Aktivierte Datensätze und Identitätszusammenfügung:** Jeder Datensatz in der Zielgruppe wird aktiviert, einschließlich aller Duplikate. Beim nächsten UPS-Profilexport durchlaufen diese Datensätze die Identitätszuordnung. Daher kann die Anzahl der aktivierten Datensätze von der Anzahl der Profile nach der Identitätszusammenfügung abweichen.

* **Targeting neuer Profile:** Wenn zwischen einem Datensatz und einem UPS-Profil keine Übereinstimmung gefunden wird, wird ein neues leeres Profil erstellt. Dieses Profil ist mit den Anreicherungsattributen verknüpft, die im Data Lake gespeichert sind. Da dieses neue Profil leer ist, sind auch die Targeting-Felder, die normalerweise in Journey Optimizer verwendet werden (wie z. B. personalEmail.address, mobilePhone.number), leer und können daher nicht für das Targeting verwendet werden. 

  Um dieses Problem zu lösen, können Sie das „Ausführungsfeld“ (oder je nach Kanal die „Ausführungsadresse“) in der Kanalkonfiguration als „identityMap“ angeben. Dadurch wird sichergestellt, dass das bei der Zielgruppenerstellung als Identität gewählte Attribut für das Targeting in Journey Optimizer verwendet wird.

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie Zielgruppen im CSV-Format in Adobe Experience Platform hochladen.

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

Erfahren Sie mehr über die Komposition von Federated Audience.

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
